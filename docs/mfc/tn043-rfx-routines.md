---
title: "TN043: RFX 루틴 | Microsoft Docs"
ms.custom: ""
ms.date: "12/03/2016"
ms.prod: "visual-studio-dev14"
ms.reviewer: ""
ms.suite: ""
ms.technology: 
  - "devlang-cpp"
ms.tgt_pltfrm: ""
ms.topic: "article"
f1_keywords: 
  - "RFX"
dev_langs: 
  - "C++"
helpviewer_keywords: 
  - "RFX(레코드 필드 교환)"
  - "RFX(레코드 필드 교환), 아키텍처"
  - "TN043"
ms.assetid: f552d0c1-2c83-4389-b472-42c9940aa713
caps.latest.revision: 10
caps.handback.revision: 6
author: "mikeblome"
ms.author: "mblome"
manager: "ghogen"
---
# TN043: RFX 루틴
[!INCLUDE[vs2017banner](../assembler/inline/includes/vs2017banner.md)]

> [!NOTE]
>  다음 기술 노트는 온라인 설명서에 먼저 포함되어 있었으므로 업데이트되지 않았습니다.  따라서 일부 절차 및 항목은 만료되거나 올바르지 않을 수 있습니다.  최신 정보를 보려면 온라인 설명서 색인에서 관심 있는 항목을 검색하는 것이 좋습니다.  
  
 This note describes the record field exchange \(RFX\) architecture.  It also describes how you write an **RFX\_** procedure.  
  
## Overview of Record Field Exchange  
 All recordset field functions are done with C\+\+ code.  There are no special resources or magic macros.  The heart of the mechanism is a virtual function that must be overridden in every derived recordset class.  It is always found in this form:  
  
```  
void CMySet::DoFieldExchange(CFieldExchange* pFX)  
{  
  //{{AFX_FIELD_MAP(CMySet)  
  <recordset exchange field type call>  
  <recordset exchange function call>  
  //}}AFX_FIELD_MAP  
}  
```  
  
 The special format AFX comments allow ClassWizard to locate and edit the code within this function.  Code that is not compatible with ClassWizard should be placed outside of the special format comments.  
  
 In the above example, \<recordset\_exchange\_field\_type\_call\> is in the form:  
  
```  
pFX->SetFieldType(CFieldExchange::outputColumn);  
```  
  
 and \<recordset\_exchange\_function\_call\> is in the form:  
  
```  
RFX_Custom(pFX, "Col2", m_Col2);  
```  
  
 Most **RFX\_** functions have three arguments as shown above, but some \(e.g.  `RFX_Text` and `RFX_Binary`\) have additional optional arguments.  
  
 More than one **RFX\_** may be included in each `DoDataExchange` function.  
  
 See 'afxdb.h' for a list of all the recordset field exchange routines provided with MFC.  
  
 Recordset field calls are a way of registering memory locations \(usually data members\) to store field data for a **CMySet** class.  
  
## 참고  
 Recordset field functions are designed to work only with the `CRecordset` classes.  They are not generally usable by any other MFC classes.  
  
 Initial values of data are set in the standard C\+\+ constructor, usually in a block with `//{{AFX_FIELD_INIT(CMylSet)` and `//}}AFX_FIELD_INIT` comments.  
  
 Each **RFX\_** function must support various operations, ranging from returning the dirty status of the field to archiving the field in preparation for editing the field.  
  
 Each function that calls `DoFieldExchange` \(for instance `SetFieldNull`, `IsFieldDirty`\), does its own initialization around the call to `DoFieldExchange`.  
  
## How Does It Work?  
 You do not need to understand the following in order to use record field exchange.  However, understanding how this works behind the scenes will help you write your own exchange procedure.  
  
 The `DoFieldExchange` member function is much like the `Serialize` member function — it is responsible for getting or setting data to\/from an external form \(in this case columns from the result of an ODBC query\) from\/to member data in the class.  The `pFX` parameter is the context for doing data exchange and is similar to the `CArchive` parameter to `CObject::Serialize`.  The `pFX` \(a `CFieldExchange` object\) has an operation indicator, which is similar to, but a generalization of the `CArchive` direction flag.  An RFX function may have to support the following operations:  
  
-   **BindParam** — Indicate where ODBC should retrieve parameter data  
  
-   **BindFieldToColumn** — Indicate where ODBC must retrieve\/deposit outputColumn data  
  
-   **Fixup** — Set **CString\/CByteArray** lengths, set NULL status bit  
  
-   **MarkForAddNew** — Mark dirty if value has changed since AddNew call  
  
-   **MarkForUpdate** — Mark dirty if value has changed since Edit call  
  
-   **Name** — Append field names for fields marked dirty  
  
-   **NameValue** — Append "\<column name\>\=?" for fields marked dirty  
  
-   **Value** — Append "?" followed by separator, like ',' or ' '  
  
-   `SetFieldDirty` — Set status bit dirty \(i.e. changed\) field  
  
-   `SetFieldNull` — Set status bit indicating null value for field  
  
-   `IsFieldDirty` — Return value of dirty status bit  
  
-   `IsFieldNull` — Return value of null status bit  
  
-   `IsFieldNullable` — Return TRUE if field can hold NULL values  
  
-   **StoreField** — Archive field value  
  
-   **LoadField** — Reload archived field value  
  
-   **GetFieldInfoValue** — Return general information on a field  
  
-   **GetFieldInfoOrdinal** — Return general information on a field  
  
## User Extensions  
 There are several ways to extend the default RFX mechanism.  옵션  
  
-   Add new data types.  예를 들면 다음과 같습니다.  
  
    ```  
    CBookmark  
    ```  
  
-   Add new exchange procedures \(RFX\_???\).  
  
    ```  
    void AFXAPI RFX_Bigint(CFieldExchange* pFX, const char *szName,  
        BIGINT& value);  
    ```  
  
-   Have the `DoFieldExchange` member function conditionally include additional RFX calls or any other valid C\+\+ statements.  
  
    ```  
    while (posExtraFields != NULL)  
    {  
        RFX_Text(pFX, m_listName.GetNext(posExtraFields),   
            m_listValue.GetNext(posExtraValues));  
    }  
    ```  
  
> [!NOTE]
>  Such code cannot be edited by ClassWizard and should be used only outside of the special format comments.  
  
## Writing a Custom RFX  
 To write your own Custom RFX function, it is suggested that you copy an existing RFX function and modify it to your own purposes.  Selecting the right RFX to copy can make your job much easier.  Some RFX functions have some unique properties that you should take into account when deciding which to copy.  
  
 **RFX\_Long and RFX\_Int**:  
 These are the simplest RFX functions.  The data value does not need any special interpretation, and the data size is fixed.  
  
 **RFX\_Single and RFX\_Double**:  
 Like RFX\_Long and RFX\_Int above, these functions are simple and can make use of the default implementation extensively.  They are stored in dbflt.cpp instead of dbrfx.cpp, however, to enable loading the runtime floating point library only when they are explicitly reference.  
  
 **RFX\_Text and RFX\_Binary**:  
 These two functions preallocate a static buffer to hold string\/binary information, and must register these buffers with ODBC SQLBindCol instead of registering &value.  Because of this, these two functions have lots of special\-case code.  
  
 `RFX_Date`:  
 ODBC returns date and time information in their own TIMESTAMP\_STRUCT data structure.  This function dynamically allocates a TIMESTAMP\_STRUCT as a "proxy" for sending and receiving date time data.  Various operations must transfer the date and time information between the C\+\+ `CTime` object and the TIMESTAMP\_STRUCT proxy.  This complicates this function considerably, but it is a good example of how to use a proxy for data transfer.  
  
 `RFX_LongBinary`:  
 This is the only class library RFX function that does not use column binding to receive and send data.  This function ignores the BindFieldToColumn operation and instead, during the Fixup operation, allocates storage to hold the incoming SQL\_LONGVARCHAR or SQL\_LONGVARBINARY data, then performs an SQLGetData call to retrieve the value into the allocated storage.  When preparing to send data values back to the data source \(such as NameValue and Value operations\), this function uses ODBC's DATA\_AT\_EXEC functionality.  See [Technical Note 45](../mfc/tn045-mfc-database-support-for-long-varchar-varbinary.md) for more information on working with SQL\_LONGVARBINARY and SQL\_LONGVARCHARs.  
  
 When writing your own **RFX\_** function, you will often be able to use **CFieldExchange::Default** to implement a given operation.  Look at the implementation of Default for the operation in question.  If it performs the operation you would be writing in your **RFX\_** function you can delegate to the **CFieldExchange::Default.** You can see examples of calling **CFieldExchange::Default** in dbrfx.cpp  
  
 It is important to call `IsFieldType` at the start of your RFX function, and return immediately if it returns FALSE.  This mechanism keeps parameter operations from being performed on **outputColumns**, and vice versa \(like calling **BindParam** on an **outputColumn**\).  In addition, `IsFieldType` automatically keeps track of the count of **outputColumns** \(`m_nFields`\) and params \(`m_nParams`\).  
  
## 참고 항목  
 [번호별 기술 참고 사항](../mfc/technical-notes-by-number.md)   
 [범주별 기술 참고 사항](../mfc/technical-notes-by-category.md)