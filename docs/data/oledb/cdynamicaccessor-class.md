---
title: "CDynamicAccessor 클래스 | Microsoft Docs"
ms.custom: ""
ms.date: "11/04/2016"
ms.reviewer: ""
ms.suite: ""
ms.technology: 
  - "devlang-cpp"
ms.tgt_pltfrm: ""
ms.topic: "article"
f1_keywords: 
  - "ATL.CDynamicAccessor"
  - "ATL::CDynamicAccessor"
  - "CDynamicAccessor"
dev_langs: 
  - "C++"
helpviewer_keywords: 
  - "CDynamicAccessor 클래스"
ms.assetid: 374b13b7-1f09-457d-9e6b-df260ff4d178
caps.latest.revision: 10
author: "mikeblome"
ms.author: "mblome"
manager: "ghogen"
caps.handback.revision: 10
---
# CDynamicAccessor 클래스
[!INCLUDE[vs2017banner](../../assembler/inline/includes/vs2017banner.md)]

Allows you to access a data source when you have no knowledge of the database schema \(the database's underlying structure\).  
  
## 구문  
  
```  
class CDynamicAccessor : public CAccessorBase  
```  
  
## 멤버  
  
### 메서드  
  
|||  
|-|-|  
|[AddBindEntry](../../data/oledb/cdynamicaccessor-addbindentry.md)|Adds a bind entry to the output columns when overriding the default accessor.|  
|[CDynamicAccessor](../../data/oledb/cdynamicaccessor-class.md)|Instantiates and initializes the `CDynamicAccessor` object.|  
|[닫기](../../data/oledb/cdynamicaccessor-close.md)|Unbinds all the columns, releases the allocated memory, and releases the [IAccessor](https://msdn.microsoft.com/en-us/library/ms719672.aspx) interface pointer in the class.|  
|[GetBookmark](../../data/oledb/cdynamicaccessor-getbookmark.md)|Retrieves the bookmark for the current row.|  
|[GetBlobHandling](../../data/oledb/cdynamicaccessor-getblobhandling.md)|Retrieves the BLOB handling value for the current row.|  
|[GetBlobSizeLimit](../../data/oledb/cdynamicaccessor-getblobsizelimit.md)|Retrieves the maximum BLOB size in bytes.|  
|[GetColumnCount](../../data/oledb/cdynamicaccessor-getcolumncount.md)|Retrieves the number of columns in the rowset.|  
|[GetColumnFlags](../../data/oledb/cdynamicaccessor-getcolumnflags.md)|Retrieves the column characteristics.|  
|[GetColumnInfo](../../data/oledb/cdynamicaccessor-getcolumninfo.md)|Retrieves the column metadata.|  
|[GetColumnName](../../data/oledb/cdynamicaccessor-getcolumnname.md)|Retrieves the name of a specified column.|  
|[GetColumnType](../../data/oledb/cdynamicaccessor-getcolumntype.md)|Retrieves the data type of a specified column.|  
|[GetLength](../../data/oledb/cdynamicaccessor-getlength.md)|Retrieves the maximum possible length of a column in bytes.|  
|[GetOrdinal](../../data/oledb/cdynamicaccessor-getordinal.md)|Retrieves the column index given a column name.|  
|[GetStatus](../../data/oledb/cdynamicaccessor-getstatus.md)|Retrieves the status of a specified column.|  
|[GetValue](../../data/oledb/cdynamicaccessor-getvalue.md)|Retrieves the data from the buffer.|  
|[SetBlobHandling](../../data/oledb/cdynamicaccessor-setblobhandling.md)|Sets the BLOB handling value for the current row.|  
|[SetBlobSizeLimit](../../data/oledb/cdynamicaccessor-setblobsizelimit.md)|Sets the maximum BLOB size in bytes.|  
|[SetLength](../../data/oledb/cdynamicaccessor-setlength.md)|Sets the length of the column in bytes.|  
|[SetStatus](../../data/oledb/cdynamicaccessor-setstatus.md)|Sets the status of a specified column.|  
|[SetValue](../../data/oledb/cdynamicaccessor-setvalue.md)|Stores the data to the buffer.|  
  
## 설명  
 Use `CDynamicAccessor` methods to obtain column information such as column names, column count, data type, and so on.  You then use this column information to create an accessor dynamically at run time.  
  
 열 정보는 이 클래스에서 만들고 관리하는 버퍼에 저장됩니다.  Obtain data from the buffer using [GetValue](../../data/oledb/cdynamicaccessor-getvalue.md).  
  
 For a discussion and examples of using the dynamic accessor classes, see [Using Dynamic Accessors](../../data/oledb/using-dynamic-accessors.md).  
  
## 요구 사항  
 **Header**: atldbcli.h  
  
## 참고 항목  
 [OLE DB 소비자 템플릿](../../data/oledb/ole-db-consumer-templates-cpp.md)   
 [OLE DB 소비자 템플릿 참조](../../data/oledb/ole-db-consumer-templates-reference.md)   
 [CAccessor 클래스](../../data/oledb/caccessor-class.md)   
 [CDynamicParameterAccessor 클래스](../../data/oledb/cdynamicparameteraccessor-class.md)   
 [CManualAccessor 클래스](../../data/oledb/cmanualaccessor-class.md)