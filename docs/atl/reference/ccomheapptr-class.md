---
title: "CComHeapPtr 클래스 | Microsoft Docs"
ms.custom: 
ms.date: 11/04/2016
ms.reviewer: 
ms.suite: 
ms.technology: cpp-windows
ms.tgt_pltfrm: 
ms.topic: reference
f1_keywords:
- CComHeapPtr
- ATLBASE/ATL::CComHeapPtr
- ATLBASE/ATL::CComHeapPtr::CComHeapPtr
dev_langs: C++
helpviewer_keywords: CComHeapPtr class
ms.assetid: bd08b53d-da2b-43ab-a79c-e7c8dbbc5994
caps.latest.revision: "19"
author: mikeblome
ms.author: mblome
manager: ghogen
ms.workload: cplusplus
ms.openlocfilehash: 8619c050ecc356e1445991b625da00c04f462848
ms.sourcegitcommit: 8fa8fdf0fbb4f57950f1e8f4f9b81b4d39ec7d7a
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 12/21/2017
---
# <a name="ccomheapptr-class"></a>CComHeapPtr 클래스
스마트 포인터는 힙에 대 한 포인터를 관리 하기 위한 클래스입니다.  
  
## <a name="syntax"></a>구문  
  
```
template<typename T>  
class CComHeapPtr : public CHeapPtr<T, CComAllocator>
```  
  
#### <a name="parameters"></a>매개 변수  
 `T`  
 힙에 저장 될 개체 형식입니다.  
  
## <a name="members"></a>멤버  
  
### <a name="public-constructors"></a>Public 생성자  
  
|이름|설명|  
|----------|-----------------|  
|[CComHeapPtr::CComHeapPtr](#ccomheapptr)|생성자입니다.|  
  
## <a name="remarks"></a>설명  
 `CComHeapPtr`파생 `CHeapPtr`, 하지만 사용 하 여 [CComAllocator](../../atl/reference/ccomallocator-class.md) COM 루틴을 사용 하 여 메모리를 할당 합니다. 참조 [CHeapPtr](../../atl/reference/cheapptr-class.md) 및 [CHeapPtrBase](../../atl/reference/cheapptrbase-class.md) 사용할 수 있는 방법에 대 한 합니다.  
  
## <a name="inheritance-hierarchy"></a>상속 계층  
 [CHeapPtrBase](../../atl/reference/cheapptrbase-class.md)  
  
 [CHeapPtr](../../atl/reference/cheapptr-class.md)  
  
 `CComHeapPtr`  
  
## <a name="requirements"></a>요구 사항  
 **헤더:** atlbase.h  
  
##  <a name="ccomheapptr"></a>CComHeapPtr::CComHeapPtr  
 생성자입니다.  
  
```
CComHeapPtr() throw();
explicit CComHeapPtr(T* pData) throw();
```  
  
### <a name="parameters"></a>매개 변수  
 `pData`  
 기존 `CComHeapPtr` 개체입니다.  
  
### <a name="remarks"></a>설명  
 기존 힙 포인터를 만들 수 있습니다 `CComHeapPtr` 개체입니다. 이 경우 새 `CComHeapPtr` 새 포인터 및 리소스 관리에 대 한 책임을 지지 하는 개체입니다.  
  
## <a name="see-also"></a>참고 항목  
 [CHeapPtr 클래스](../../atl/reference/cheapptr-class.md)   
 [CHeapPtrBase 클래스](../../atl/reference/cheapptrbase-class.md)   
 [CComAllocator 클래스](../../atl/reference/ccomallocator-class.md)   
 [클래스 개요](../../atl/atl-class-overview.md)
