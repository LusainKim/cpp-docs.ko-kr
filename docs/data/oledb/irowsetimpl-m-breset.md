---
title: "IRowsetImpl::m_bReset | Microsoft Docs"
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
  - "ATL.IRowsetImpl.m_bReset"
  - "IRowsetImpl.m_bReset"
  - "m_bReset"
  - "IRowsetImpl::m_bReset"
  - "ATL::IRowsetImpl::m_bReset"
dev_langs: 
  - "C++"
helpviewer_keywords: 
  - "m_bReset"
ms.assetid: d423f9f3-4d48-4d0c-b152-684c81a0b34e
caps.latest.revision: 8
caps.handback.revision: 8
author: "mikeblome"
ms.author: "mblome"
manager: "ghogen"
---
# IRowsetImpl::m_bReset
[!INCLUDE[vs2017banner](../../assembler/inline/includes/vs2017banner.md)]

A bit flag used to determine if the cursor position is defined on the rowset.  
  
## 구문  
  
```  
  
unsigned m_bReset:1;  
  
```  
  
## 설명  
 If the consumer calls [GetNextRows](../../data/oledb/irowsetimpl-getnextrows.md) with a negative `lOffset` or *cRows* and `m_bReset` is true, `GetNextRows` moves to the end of the rowset.  If `m_bReset` is false, the consumer receives an error code, in conformance with the OLE DB specification.  The `m_bReset` flag gets set to **true** when the rowset is first created and when the consumer calls [IRowsetImpl::RestartPosition](../../data/oledb/irowsetimpl-restartposition.md).  It gets set to **false** when you call `GetNextRows`.  
  
## 요구 사항  
 **Header:** atldb.h  
  
## 참고 항목  
 [IRowsetImpl 클래스](../../data/oledb/irowsetimpl-class.md)