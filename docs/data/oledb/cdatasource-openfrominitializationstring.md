---
title: "CDataSource::OpenFromInitializationString | Microsoft Docs"
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
  - "CDataSource.OpenFromInitializationString"
  - "OpenFromInitializationString"
  - "CDataSource::OpenFromInitializationString"
  - "ATL::CDataSource::OpenFromInitializationString"
  - "ATL.CDataSource.OpenFromInitializationString"
dev_langs: 
  - "C++"
helpviewer_keywords: 
  - "OpenFromInitializationString 메서드"
ms.assetid: 5ef1f1fd-92a9-4e1c-ad80-d3601b094b8c
caps.latest.revision: 10
caps.handback.revision: 10
author: "mikeblome"
ms.author: "mblome"
manager: "ghogen"
---
# CDataSource::OpenFromInitializationString
[!INCLUDE[vs2017banner](../../assembler/inline/includes/vs2017banner.md)]

Opens a data source specified by the user\-supplied initialization string.  
  
## 구문  
  
```  
  
      HRESULT OpenFromInitializationString(   
   LPCOLESTR szInitializationString,   
   bool fPromptForInfo = false    
) throw( );  
```  
  
#### 매개 변수  
 *szInitializationString*  
 \[in\] The initialization string.  
  
 *fPromptForInfo*  
 \[in\] If this argument is set to **true**, then `OpenFromInitializationString` will set the **DBPROP\_INIT\_PROMPT** property to **DBPROMPT\_COMPLETEREQUIRED**, which specifies that the user be prompted only if more information is needed.  This is useful for situations in which the initialization string specifies a database that requires a password, but the string does not contain the password.  The user will be prompted for a password \(or any other missing information\) when trying to connect to the database.  
  
 The default value is **false**, which specifies that the user never be prompted \(sets **DBPROP\_INIT\_PROMPT** to **DBPROMPT\_NOPROMPT**\).  
  
## 반환 값  
 A standard `HRESULT`.  
  
## 설명  
 This method opens a data source object using the service components in oledb32.dll; this DLL contains the implementation of Service Components features such as Resource Pooling, Automatic Transaction Enlistment, and so on.  
  
## 요구 사항  
 **헤더:** atldbcli.h  
  
## 참고 항목  
 [CDataSource 클래스](../../data/oledb/cdatasource-class.md)