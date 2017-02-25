---
title: "CUtlProps::OnInterfaceRequested | Microsoft Docs"
ms.custom: ""
ms.date: "11/04/2016"
ms.reviewer: ""
ms.suite: ""
ms.technology: 
  - "devlang-cpp"
ms.tgt_pltfrm: ""
ms.topic: "article"
f1_keywords: 
  - "CUtlProps"
dev_langs: 
  - "C++"
helpviewer_keywords: 
  - "OnInterfaceRequested 메서드"
ms.assetid: a5e1a879-cff3-4e01-b902-2249a152984f
caps.latest.revision: 8
author: "mikeblome"
ms.author: "mblome"
manager: "ghogen"
caps.handback.revision: 8
---
# CUtlProps::OnInterfaceRequested
[!INCLUDE[vs2017banner](../../assembler/inline/includes/vs2017banner.md)]

Handles requests for an optional interface when a consumer calls a method on one of the object creation interfaces.  
  
## 구문  
  
```  
  
      virtual HRESULT CUtlPropsBase::OnInterfaceRequested(  
   REFIID riid  
);  
```  
  
#### 매개 변수  
 `riid`  
 \[in\] The IID for the requested interface.  For more details, see the description of the `riid` parameter of `ICommand::Execute` in the *OLE DB Programmer's Reference* \(in the *MDAC SDK*\).  
  
## 설명  
 **OnInterfaceRequested** handles consumer requests for an optional interface when a consumer calls a method on one of the object creation interfaces \(such as **IDBCreateSession**, **IDBCreateCommand**, `IOpenRowset`, or `ICommand`\).  It sets the corresponding OLE DB property for the requested interface.  For example, if the consumer requests **IID\_IRowsetLocate**, **OnInterfaceRequested** sets the **DBPROP\_IRowsetLocate** interface.  Doing so maintains the correct state during rowset creation.  
  
 This method is called when the consumer calls **IOpenRowset::OpenRowset** or `ICommand::Execute`.  
  
 If a consumer opens an object and requests an optional interface, the provider should set the property associated with that interface to `VARIANT_TRUE`.  To allow property\-specific processing, **OnInterfaceRequested** is called before the provider's **Execute** method is called.  By default, **OnInterfaceRequested** handles the following interfaces:  
  
-   `IRowsetLocate`  
  
-   `IRowsetChange`  
  
-   `IRowsetUpdate`  
  
-   **IConnectionPointContainer**  
  
-   `IRowsetScroll`  
  
 If you wish to handle other interfaces, override this function in your data source, session, command, or rowset class to process functions.  Your override should go through the normal set\/get properties interfaces to ensure that setting properties also sets any chained properties \(see [OnPropertyChanged](../../data/oledb/cutlprops-onpropertychanged.md)\).  
  
## 요구 사항  
 **Header:** atldb.h  
  
## 참고 항목  
 [CUtlProps 클래스](../../data/oledb/cutlprops-class.md)