---
title: 'Ierrorrecordsimpl:: Adderrorrecord | Microsoft Docs'
ms.custom: 
ms.date: 11/04/2016
ms.reviewer: 
ms.suite: 
ms.technology: cpp-windows
ms.tgt_pltfrm: 
ms.topic: article
f1_keywords:
- IErrorRecordsImpl.AddErrorRecord
- AddErrorRecord
- IErrorRecordsImpl::AddErrorRecord
dev_langs: C++
helpviewer_keywords: AddErrorRecord method
ms.assetid: b5f8e9ae-509d-454f-b511-4bda7e972607
caps.latest.revision: "9"
author: mikeblome
ms.author: mblome
manager: ghogen
ms.workload:
- cplusplus
- data-storage
ms.openlocfilehash: 9e31b40bd710a5b1bfeef398ea23f7c6fe9e8ce6
ms.sourcegitcommit: 8fa8fdf0fbb4f57950f1e8f4f9b81b4d39ec7d7a
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 12/21/2017
---
# <a name="ierrorrecordsimpladderrorrecord"></a>IErrorRecordsImpl::AddErrorRecord
OLE DB 오류 개체에 레코드를 추가합니다.  
  
## <a name="syntax"></a>구문  
  
```  
  
      STDMETHOD( AddErrorRecord )(  
   ERRORINFO *pErrorInfo,  
   DWORD dwLookupID,  
   DISPPARAMS *pdispparams,  
   IUnknown *punkCustomError,  
   DWORD dwDynamicErrorID   
);  
```  
  
#### <a name="parameters"></a>매개 변수  
 참조 [IErrorRecords::AddErrorRecord](https://msdn.microsoft.com/en-us/library/ms725362.aspx) 에 *OLE DB Programmer's Reference*합니다.  
  
## <a name="requirements"></a>요구 사항  
 **헤더:** atldb.h  
  
## <a name="see-also"></a>참고 항목  
 [IErrorRecordsImpl 클래스](../../data/oledb/ierrorrecordsimpl-class.md)