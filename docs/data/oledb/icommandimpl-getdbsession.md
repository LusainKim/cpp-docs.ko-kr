---
title: "ICommandImpl::GetDBSession | Microsoft Docs"
ms.custom: ""
ms.date: "11/04/2016"
ms.reviewer: ""
ms.suite: ""
ms.technology: 
  - "devlang-cpp"
ms.tgt_pltfrm: ""
ms.topic: "article"
f1_keywords: 
  - "ICommandImpl::GetDBSession"
  - "GetDBSession"
  - "ICommandImpl.GetDBSession"
dev_langs: 
  - "C++"
helpviewer_keywords: 
  - "GetDBSession 메서드"
ms.assetid: e5b1cb13-453f-4698-90bf-f6bfe6814a54
caps.latest.revision: 8
author: "mikeblome"
ms.author: "mblome"
manager: "ghogen"
caps.handback.revision: 8
---
# ICommandImpl::GetDBSession
[!INCLUDE[vs2017banner](../../assembler/inline/includes/vs2017banner.md)]

Returns an interface pointer to the session that created the command.  
  
## 구문  
  
```  
  
      STDMETHOD (GetDBSession) (  
   REFIID riid,  
   IUnknown** ppSession   
);  
```  
  
#### 매개 변수  
 See [ICommand::GetDBSession](https://msdn.microsoft.com/en-us/library/ms719622.aspx) in the *OLE DB Programmer's Reference*.  
  
## 설명  
 Useful for retrieving properties from the session.  
  
## 요구 사항  
 **Header:** atldb.h  
  
## 참고 항목  
 [ICommandImpl 클래스](../../data/oledb/icommandimpl-class.md)