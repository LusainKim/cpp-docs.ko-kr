---
title: "CSimpleMapEqualHelperFalse 클래스 | Microsoft Docs"
ms.custom: 
ms.date: 11/04/2016
ms.reviewer: 
ms.suite: 
ms.technology: cpp-windows
ms.tgt_pltfrm: 
ms.topic: reference
f1_keywords:
- CSimpleMapEqualHelperFalse
- ATLSIMPCOLL/ATL::CSimpleMapEqualHelperFalse
- ATLSIMPCOLL/ATL::CSimpleMapEqualHelperFalse::IsEqualKey
- ATLSIMPCOLL/ATL::CSimpleMapEqualHelperFalse::IsEqualValue
dev_langs: C++
helpviewer_keywords: CSimpleMapEqualHelperFalse class
ms.assetid: a873eea3-e130-45cc-a476-61ee79511c3b
caps.latest.revision: "19"
author: mikeblome
ms.author: mblome
manager: ghogen
ms.workload: cplusplus
ms.openlocfilehash: c1418114233b59112fcffb58ef4ae7c437af5ab3
ms.sourcegitcommit: 8fa8fdf0fbb4f57950f1e8f4f9b81b4d39ec7d7a
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 12/21/2017
---
# <a name="csimplemapequalhelperfalse-class"></a>CSimpleMapEqualHelperFalse 클래스
이 클래스는에 대 한 도우미는 [CSimpleMap](../../atl/reference/csimplemap-class.md) 클래스입니다.  
  
## <a name="syntax"></a>구문  
  
```
template <class TKey, class TVal>  
class CSimpleMapEqualHelperFalse
```  
  
## <a name="members"></a>멤버  
  
### <a name="public-methods"></a>Public 메서드  
  
|이름|설명|  
|----------|-----------------|  
|[CSimpleMapEqualHelperFalse::IsEqualKey](#isequalkey)|(정적) 두 키가 같은지 테스트합니다.|  
|[CSimpleMapEqualHelperFalse::IsEqualValue](#isequalvalue)|(정적) False를 반환 합니다.|  
  
## <a name="remarks"></a>설명  
 이 특성 클래스는 적용 하기 위해는 `CSimpleMap` 클래스입니다. 에 포함 된 두 개의 요소를 비교 하기 위한 방법을 제공는 `CSimpleMap` 개체, 특히 두 개의 값 요소 또는 두 가지 주요 요소입니다.  
  
 값 비교는 항상 false를 반환 하 고 호출 또한 `ATLASSERT` 적이 참조 하는 경우 false 인수를 사용 합니다. 이 클래스를 대부분의 메서드에서 올바르게 작동 하지만에서 같은 비교에 의존 하는 방법에 대 한 잘 정의 된 오류가 발생 하는 키/값 쌍을 포함 하는 맵을 사용 하면 같음 테스트가 되지 충분히 정의 되어 없는 경우에 [CSimpleMap:: FindVal](../../atl/reference/csimplemap-class.md#findval)합니다.  
  
## <a name="requirements"></a>요구 사항  
 **헤더:** atlsimpcoll.h  
  
##  <a name="isequalkey"></a>CSimpleMapEqualHelperFalse::IsEqualKey  
 두 키가 같은지 테스트합니다.  
  
```
static bool IsEqualKey(const TKey& k1, const TKey& k2);
```  
  
### <a name="parameters"></a>매개 변수  
 `k1`  
 첫 번째 키입니다.  
  
 `k2`  
 두 번째 키입니다.  
  
### <a name="return-value"></a>반환 값  
 키가 같으면 false를 반환 하지 않으면 true를 반환 합니다.  
  
### <a name="remarks"></a>설명  
 이 메서드를 호출 [CSimpleArrayEqualHelper](../../atl/reference/csimplearrayequalhelper-class.md)합니다.  
  
##  <a name="isequalvalue"></a>CSimpleMapEqualHelperFalse::IsEqualValue  
 false를 반환합니다.  
  
```
static bool IsEqualValue(const TVal&, const TVal&);
```  
  
### <a name="return-value"></a>반환 값  
 false를 반환합니다.  
  
### <a name="remarks"></a>설명  
 이 메서드는 항상 false를 반환 하며 호출 합니다 `ATLASSERT` 적이 참조 하는 경우 false 인수를 사용 합니다. 목적은 `CSimpleMapEqualHelperFalse::IsEqualValue` 같음 테스트 적절 하 게 정의 하지 않은 경우 잘 정의 된 방식으로 실패할 비교를 사용 하는 방법을 강제 적용 하는 것입니다.  
  
## <a name="see-also"></a>참고 항목  
 [CSimpleMapEqualHelper 클래스](../../atl/reference/csimplemapequalhelper-class.md)   
 [클래스 개요](../../atl/atl-class-overview.md)
