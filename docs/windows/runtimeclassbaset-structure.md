---
title: "RuntimeClassBaseT 구조체 | Microsoft Docs"
ms.custom: 
ms.date: 11/04/2016
ms.reviewer: 
ms.suite: 
ms.technology: cpp-windows
ms.tgt_pltfrm: 
ms.topic: reference
f1_keywords: implements/Microsoft::WRL::Details::RuntimeClassBaseT
dev_langs: C++
ms.assetid: a62775fb-3359-4f45-9ff1-c07fa8da464b
caps.latest.revision: "5"
author: mikeblome
ms.author: mblome
manager: ghogen
ms.workload:
- cplusplus
- uwp
ms.openlocfilehash: 8798372b96074cb8424b4e747b188abcaf826849
ms.sourcegitcommit: 8fa8fdf0fbb4f57950f1e8f4f9b81b4d39ec7d7a
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 12/21/2017
---
# <a name="runtimeclassbaset-structure"></a>RuntimeClassBaseT 구조체
WRL 인프라를 지원하며 사용자 코드에서 직접 사용할 수 없습니다.  
  
## <a name="syntax"></a>구문  
  
```  
template <  
   unsigned int RuntimeClassTypeT  
>  
friend struct Details::RuntimeClassBaseT;  
```  
  
#### <a name="parameters"></a>매개 변수  
 `RuntimeClassTypeT`  
 플래그의 하나 이상 지정 하는 필드 [RuntimeClassType](../windows/runtimeclasstype-enumeration.md) 열거자입니다.  
  
## <a name="remarks"></a>설명  
 도우미 메서드를 제공 `QueryInterface` 작업과 가져오는 인터페이스 Id입니다.  
  
## <a name="members"></a>멤버  
  
## <a name="inheritance-hierarchy"></a>상속 계층  
 `RuntimeClassBaseT`  
  
## <a name="requirements"></a>요구 사항  
 **헤더:** implements.h  
  
 **Namespace:** Microsoft::WRL::Details  
  
## <a name="see-also"></a>참고 항목  
 [참조 (Windows 런타임 라이브러리)](http://msdn.microsoft.com/en-us/00000000-0000-0000-0000-000000000000)   
 [Microsoft::WRL::Details 네임스페이스](../windows/microsoft-wrl-details-namespace.md)