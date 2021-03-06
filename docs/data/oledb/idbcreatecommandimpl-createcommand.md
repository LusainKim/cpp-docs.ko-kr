---
title: 'Idbcreatecommandimpl:: Createcommand | Microsoft Docs'
ms.custom: 
ms.date: 11/04/2016
ms.reviewer: 
ms.suite: 
ms.technology: cpp-windows
ms.tgt_pltfrm: 
ms.topic: article
f1_keywords:
- IDBCreateCommandImpl.CreateCommand
- CreateCommand
- IDBCreateCommandImpl::CreateCommand
dev_langs: C++
helpviewer_keywords: CreateCommand method
ms.assetid: 50ffbf8b-2c07-4bcb-96c5-ffce4519c7f7
caps.latest.revision: "8"
author: mikeblome
ms.author: mblome
manager: ghogen
ms.workload:
- cplusplus
- data-storage
ms.openlocfilehash: ff1f7e9815ae5cea9a96c95f7faad30340bf548d
ms.sourcegitcommit: 8fa8fdf0fbb4f57950f1e8f4f9b81b4d39ec7d7a
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 12/21/2017
---
# <a name="idbcreatecommandimplcreatecommand"></a>IDBCreateCommandImpl::CreateCommand
새 명령을 만들고 요청된 된 인터페이스를 반환 합니다.  
  
## <a name="syntax"></a>구문  
  
```  
  
      STDMETHOD(CreateCommand)(   
   IUnknown * pUnkOuter,   
   REFIID riid,   
   IUnknown ** ppvCommand    
);  
```  
  
#### <a name="parameters"></a>매개 변수  
 참조 [idbcreatecommand:: Createcommand](https://msdn.microsoft.com/en-us/library/ms709772.aspx) 에 *OLE DB Programmer's Reference*합니다.  
  
 에 해당 하는 일부 매개 변수 *OLE DB Programmer's Reference* 매개 변수에서 설명 하는 다른 이름의 **idbcreatecommand:: Createcommand**:  
  
|OLE DB 템플릿 매개 변수|*OLE DB Programmer's Reference* 매개 변수|  
|--------------------------------|------------------------------------------------|  
|*ppvCommand*|*ppCommand*|  
  
## <a name="requirements"></a>요구 사항  
 **헤더:** atldb.h  
  
## <a name="see-also"></a>참고 항목  
 [IDBCreateCommandImpl 클래스](../../data/oledb/idbcreatecommandimpl-class.md)