---
title: 'Idbschemarowsetimpl:: Getschemas | Microsoft Docs'
ms.custom: 
ms.date: 11/04/2016
ms.reviewer: 
ms.suite: 
ms.technology: cpp-windows
ms.tgt_pltfrm: 
ms.topic: article
f1_keywords:
- ATL::IDBSchemaRowsetImpl::GetSchemas
- GetSchemas
- IDBSchemaRowsetImpl<SessionClass>::GetSchemas
- ATL.IDBSchemaRowsetImpl.GetSchemas
- ATL::IDBSchemaRowsetImpl<SessionClass>::GetSchemas
- IDBSchemaRowsetImpl.GetSchemas
- IDBSchemaRowsetImpl::GetSchemas
dev_langs: C++
helpviewer_keywords: GetSchemas method
ms.assetid: fbe725a6-3acd-45f8-bcaf-10a6c1239cd2
caps.latest.revision: "9"
author: mikeblome
ms.author: mblome
manager: ghogen
ms.workload:
- cplusplus
- data-storage
ms.openlocfilehash: ce07c59eb9dd806d2f297591e8f3b389b3f4ce54
ms.sourcegitcommit: 8fa8fdf0fbb4f57950f1e8f4f9b81b4d39ec7d7a
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 12/21/2017
---
# <a name="idbschemarowsetimplgetschemas"></a>IDBSchemaRowsetImpl::GetSchemas
[IDBSchemaRowsetImpl::GetRowset](../../data/oledb/idbschemarowsetimpl-getrowset.md)에서 액세스할 수 있는 스키마 행 집합 목록을 반환합니다.  
  
## <a name="syntax"></a>구문  
  
```  
  
      STDMETHOD ( GetSchema s )(  
   ULONG * pcSchemas,  
   GUID ** prgSchemas,  
   ULONG** prgRest  
);  
```  
  
#### <a name="parameters"></a>매개 변수  
 *pcSchemas*  
 [out] 스키마 수로 채워진 **ULONG** 의 포인터입니다.  
  
 *prgSchemas*  
 [out] 스키마 행 집합 GUID 배열의 포인터로 채워진 GUID 배열의 포인터입니다.  
  
 *prgRest*  
 [out] 제한 배열로 채울 **ULONG**배열의 포인터입니다.  
  
## <a name="remarks"></a>설명  
 이 메서드는 공급자가 지원하는 모든 스키마 행 집합의 배열을 반환합니다. 참조 [idbschemarowset:: Getschemas](https://msdn.microsoft.com/en-us/library/ms719605.aspx) in the Windows SDK입니다.  
  
 이 함수를 구현하려면 사용자에게 세션 클래스의 스키마 맵이 있어야 합니다. 스키마 맵 정보를 사용하는 경우 맵의 스키마에 대한 GUID 배열로 응답합니다. 이는 공급자가 지원하는 스키마를 나타냅니다.  
  
## <a name="requirements"></a>요구 사항  
 **헤더:** atldb.h  
  
## <a name="see-also"></a>참고 항목  
 [IDBSchemaRowsetImpl 클래스](../../data/oledb/idbschemarowsetimpl-class.md)   
 [IDBSchemaRowsetImpl 클래스 멤버](http://msdn.microsoft.com/en-us/e74f6f82-541c-42e7-b4c6-e2d4656a0649)   
 [Idbschemarowsetimpl:: Getrowset](../../data/oledb/idbschemarowsetimpl-getrowset.md)   
 [Idbschemarowset:: Getrowset](https://msdn.microsoft.com/en-us/library/ms722634.aspx)   
 [스키마 행 집합 클래스 및 Typedef 클래스](../../data/oledb/schema-rowset-classes-and-typedef-classes.md)