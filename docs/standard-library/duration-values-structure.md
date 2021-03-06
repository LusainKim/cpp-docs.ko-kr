---
title: "duration_values 구조체 | Microsoft 문서"
ms.custom: 
ms.date: 11/04/2016
ms.reviewer: 
ms.suite: 
ms.technology: cpp-standard-libraries
ms.tgt_pltfrm: 
ms.topic: article
f1_keywords:
- chrono/std::chrono::duration_values
- chrono/std::chrono::duration_values::max
- chrono/std::chrono::duration_values::min
- chrono/std::chrono::duration_values::zero
dev_langs: C++
ms.assetid: 7f66d2e3-1faf-47c3-b47e-08f2a87f20e8
caps.latest.revision: "13"
author: corob-msft
ms.author: corob
manager: ghogen
ms.workload: cplusplus
ms.openlocfilehash: a0f06646975d694ab76477a64642c03c20769c54
ms.sourcegitcommit: 8fa8fdf0fbb4f57950f1e8f4f9b81b4d39ec7d7a
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 12/21/2017
---
# <a name="durationvalues-structure"></a>duration_values 구조체
[duration](../standard-library/duration-class.md) 템플릿 매개 변수 `Rep`에 대한 특정 값을 제공합니다.  
  
## <a name="syntax"></a>구문  
  
```  
template <class Rep>  
struct duration_values;  
```  
  
## <a name="members"></a>멤버  
  
### <a name="public-methods"></a>Public 메서드  
  
|이름|설명|  
|----------|-----------------|  
|[max](#max)|정적. `Rep` 형식 값의 상한을 지정합니다.|  
|[분](#min)|정적. `Rep` 형식 값의 하한을 지정합니다.|  
|[0](#zero)|정적. `Rep(0)`를 반환합니다.|  
  
## <a name="requirements"></a>요구 사항  
 **헤더:** \<c h >  
  
 **네임스페이스:** std::chrono  
  
##  <a name="max"></a>  duration_values::max  
 형식 `Ref`의 값에 대한 상한을 반환하는 정적 메서드입니다.  
  
```  
static constexpr Rep max();
```  
  
### <a name="return-value"></a>반환 값  
 실제로 `numeric_limits<Rep>::max()`를 반환합니다.  
  
### <a name="remarks"></a>설명  
 `Rep`가 사용자 정의 형식인 경우 반환 값은 [duration_values::zero](#zero)보다 커야 합니다.  
  
##  <a name="min"></a>  duration_values::min  
 `Ref` 형식의 값에 대한 하한값을 반환하는 정적 메서드입니다.  
  
```  
static constexpr Rep min();
```  
  
### <a name="return-value"></a>반환 값  
 실제로 `numeric_limits<Rep>::lowest()`를 반환합니다.  
  
### <a name="remarks"></a>설명  
 `Rep`가 사용자 정의 형식인 경우 반환 값은 [duration_values:: zero](#zero)보다 작아야 합니다.  
  
##  <a name="zero"></a>  duration_values::zero  
 `Rep(0)`를 반환합니다.  
  
```  
static constexpr Rep zero();
```  
  
### <a name="remarks"></a>설명  
 `Rep`가 사용자 정의 형식인 경우 반환 값은 가산적 무한대를 나타내야 합니다.  
  
## <a name="see-also"></a>참고 항목  
 [헤더 파일 참조](../standard-library/cpp-standard-library-header-files.md)   
 [\<chrono>](../standard-library/chrono.md)

