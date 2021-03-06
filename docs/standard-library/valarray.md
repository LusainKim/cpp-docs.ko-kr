---
title: '&lt;valarray&gt; | Microsoft Docs'
ms.custom: 
ms.date: 11/04/2016
ms.reviewer: 
ms.suite: 
ms.technology: cpp-standard-libraries
ms.tgt_pltfrm: 
ms.topic: article
f1_keywords: <valarray>
dev_langs: C++
helpviewer_keywords: valarray header
ms.assetid: 30835415-21c1-4801-8f24-6bbef7dd8ecd
caps.latest.revision: "19"
author: corob-msft
ms.author: corob
manager: ghogen
ms.workload: cplusplus
ms.openlocfilehash: 917dfbf870959b6934eaa49cbaab05e27304fb77
ms.sourcegitcommit: 8fa8fdf0fbb4f57950f1e8f4f9b81b4d39ec7d7a
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 12/21/2017
---
# <a name="ltvalarraygt"></a>&lt;valarray&gt;
템플릿 클래스 valarray 및 다양한 지원 템플릿 클래스와 함수를 정의합니다.  
  
## <a name="syntax"></a>구문  
  
```  
#include <valarray>  
  
```  
  
## <a name="remarks"></a>설명  
 이러한 템플릿 클래스와 함수는 향상된 성능을 위해 특이한 방식으로 허용됩니다. 특히 **valarray\<**T1**>** 형식을 반환하는 함수는 다른 형식 T2의 개체를 반환할 수 있습니다. 이 경우 **valarray\<**T2**>** 형식의 인수를 하나 이상 사용하는 함수에는 각각 T2 형식의 인수로 대체된 이러한 인수의 임의 조합을 허용하는 오버로드가 있어야 합니다.  
  
### <a name="functions"></a>함수  
  
|||  
|-|-|  
|[abs](../standard-library/valarray-functions.md#abs)|입력 valarray의 요소에서 작동하고 요소가 입력 valarray 요소의 절대값과 같은 valarray를 반환합니다.|  
|[acos](../standard-library/valarray-functions.md#acos)|입력 valarray의 요소에서 작동하고 요소가 입력 valarray 요소의 아크코사인과 같은 valarray를 반환합니다.|  
|[asin](../standard-library/valarray-functions.md#asin)|입력 valarray의 요소에서 작동하고 요소가 입력 valarray 요소의 아크사인과 같은 valarray를 반환합니다.|  
|[atan](../standard-library/valarray-functions.md#atan)|입력 valarray의 요소에서 작동하고 요소가 입력 valarray 요소의 아크탄젠트 주요 값과 같은 valarray를 반환합니다.|  
|[atan2](../standard-library/valarray-functions.md#atan2)|요소가 valarray의 요소 및 상수 조합에 의해 지정된 데카르트 구성 요소의 아크탄젠트와 같은 valarray를 반환합니다.|  
|[cos](../standard-library/valarray-functions.md#cos)|입력 valarray의 요소에서 작동하고 요소가 입력 valarray 요소의 코사인과 같은 valarray를 반환합니다.|  
|[cosh](../standard-library/valarray-functions.md#cosh)|입력 valarray의 요소에서 작동하고 요소가 입력 valarray 요소의 쌍곡 코사인과 같은 valarray를 반환합니다.|  
|[exp](../standard-library/valarray-functions.md#exp)|입력 valarray의 요소에서 작동하고 요소가 입력 valarray 요소의 자연 지수와 같은 valarray를 반환합니다.|  
|[log](../standard-library/valarray-functions.md#log)|입력 valarray의 요소에서 작동하고 요소가 입력 valarray 요소의 자연 로그와 같은 valarray를 반환합니다.|  
|[log10](../standard-library/valarray-functions.md#log10)|입력 valarray의 요소에서 작동하고 요소가 입력 valarray 요소의 base 10 또는 상용 로그와 같은 valarray를 반환합니다.|  
|[pow](../standard-library/valarray-functions.md#pow)|입력 valarray 및 상수의 요소에서 작동하고 요소가 입력 valarray의 요소로 지정된 밑수 또는 입력 valarray 또는 상수의 요소로 지정된 지수의 상수 거듭제곱과 같은 valarray를 반환합니다.|  
|[sin](../standard-library/valarray-functions.md#sin)|입력 valarray의 요소에서 작동하고 요소가 입력 valarray 요소의 사인과 같은 valarray를 반환합니다.|  
|[sinh](../standard-library/valarray-functions.md#sinh)|입력 valarray의 요소에서 작동하고 요소가 입력 valarray 요소의 쌍곡 사인과 같은 valarray를 반환합니다.|  
|[sqrt](../standard-library/valarray-functions.md#sqrt)|입력 valarray의 요소에서 작동하고 요소가 입력 valarray 요소의 제곱근과 같은 valarray를 반환합니다.|  
|[swap](../standard-library/valarray-functions.md#swap)||  
|[tan](../standard-library/valarray-functions.md#tan)|입력 valarray의 요소에서 작동하고 요소가 입력 valarray 요소의 탄젠트와 같은 valarray를 반환합니다.|  
|[tanh](../standard-library/valarray-functions.md#tanh)|입력 valarray의 요소에서 작동하고 요소가 입력 valarray 요소의 쌍곡 탄젠트와 같은 valarray를 반환합니다.|  
  
### <a name="operators"></a>연산자  
  
|||  
|-|-|  
|[operator!=](../standard-library/valarray-operators.md#op_neq)|크기가 같은 두 valarray의 해당 요소가 서로 같지 않은지 또는 valarray의 모든 요소가 valarray 요소 형식의 지정된 값과 같지 않은지 테스트합니다.|  
|[operator%](../standard-library/valarray-operators.md#op_mod)|크기가 같은 두 valarray의 해당 요소를 나눈 나머지 또는 valarray를 valarray 요소 형식의 지정된 값으로 나누거나 지정된 값을 valarray로 나눈 나머지를 가져옵니다.|  
|[operator&](../standard-library/valarray-operators.md#op_amp)|크기가 같은 두 valarray의 해당 요소 간이나 valarray와 요소 형식의 지정된 값 간에 비트 **AND**를 가져옵니다.|  
|[operator&&](../standard-library/valarray-operators.md#op_amp_amp)|크기가 같은 두 valarray의 해당 요소 간이나 valarray와 valarray 요소 형식의 지정된 값 간에 논리적 **AND**를 가져옵니다.|  
|[operator>](../standard-library/valarray-operators.md#op_gt)|한 valarray의 요소가 크기가 같은 valarray의 요소보다 큰지 또는 valarray의 모든 요소가 valarray 요소 형식의 지정된 값보다 크거나 작은지 테스트합니다.|  
|[operator>=](../standard-library/valarray-operators.md#op_gt_eq)|한 valarray의 요소가 크기가 같은 valarray의 요소보다 크거나 같은지 또는 valarray의 모든 요소가 지정된 값보다 크거나 같거나 작거나 같은지 테스트합니다.|  
|[operator>>](../standard-library/valarray-operators.md#op_gt_gt)|valarray의 각 요소에 대한 비트를 지정된 위치 수 또는 두 번째 valarray에 지정된 요소 양만큼 오른쪽으로 이동합니다.|  
|[operator<](../standard-library/valarray-operators.md#op_lt)|한 valarray의 요소가 크기가 같은 valarray의 요소보다 작은지 또는 valarray의 모든 요소가 지정된 값보다 크거나 작은지 테스트합니다.|  
|[operator<=](../standard-library/valarray-operators.md#op_lt_eq)|한 valarray의 요소가 크기가 같은 valarray의 요소보다 작거나 같은지 또는 valarray의 모든 요소가 지정된 값보다 크거나 같거나 작거나 같은지 테스트합니다.|  
|[operator<<](../standard-library/valarray-operators.md#op_lt_lt)|valarray의 각 요소에 대한 비트를 지정된 위치 수 또는 두 번째 valarray에 지정된 요소 양만큼 왼쪽으로 이동합니다.|  
|[operator*](../standard-library/valarray-operators.md#op_star)|크기가 같은 두 valarray의 해당 요소 간이나 valarray와 valarray 요소 형식의 지정된 값 간에 요소 곱을 가져옵니다.|  
|[operator+](../standard-library/valarray-operators.md#op_add)|크기가 같은 두 valarray의 해당 요소 간이나 valarray와 valarray 요소 형식의 지정된 값 간에 요소 합계를 가져옵니다.|  
|[operator-](../standard-library/valarray-operators.md#operator-)|크기가 같은 두 valarray의 해당 요소 간이나 valarray와 valarray 요소 형식의 지정된 값 간에 요소 차이를 가져옵니다.|  
|[operator/](../standard-library/valarray-operators.md#op_div)|크기가 같은 두 valarray의 해당 요소 간이나 valarray와 valarray 요소 형식의 지정된 값 간에 요소 몫을 가져옵니다.|  
|[operator==](../standard-library/valarray-operators.md#op_eq_eq)|크기가 같은 두 valarray의 해당 요소가 서로 같은지 또는 valarray의 모든 요소가 valarray 요소 형식의 지정된 값과 같은지 테스트합니다.|  
|[operator^](../standard-library/valarray-operators.md#op_xor)|크기가 같은 두 valarray의 해당 요소 간이나 valarray와 요소 형식의 지정된 값 간에 비트 배타적 `OR`을 가져옵니다.|  
|[operator&#124;](../standard-library/valarray-operators.md#op_or)|크기가 같은 두 valarray의 해당 요소 간이나 valarray와 요소 형식의 지정된 값 간에 비트 `OR`을 가져옵니다.|  
|[operator&#124;&#124;](../standard-library/valarray-operators.md#op_lor)|크기가 같은 두 valarray의 해당 요소 간이나 valarray와 valarray 요소 형식의 지정된 값 간에 논리적 `OR`을 가져옵니다.|  
  
### <a name="classes"></a>클래스  
  
|||  
|-|-|  
|[gslice 클래스](../standard-library/gslice-class.md)|valarray의 다차원 조각을 정의하는 데 사용되는 valarray에 대한 유틸리티 클래스입니다.|  
|[gslice_array 클래스](../standard-library/gslice-array-class.md)|valarray의 일반 조각으로 정의된 하위 집합 배열 간의 작업을 제공하여 일반 조각 개체를 지원하는 내부 보조 템플릿 클래스입니다.|  
|[indirect_array 클래스](../standard-library/indirect-array-class.md)|부모 valarray의 인덱스 하위 집합을 지정하여 정의된 하위 집합 배열 간의 작업을 제공하여 valarray의 하위 집합인 개체를 지원하는 내부 보조 템플릿 클래스입니다.|  
|[mask_array 클래스](../standard-library/mask-array-class.md)|하위 집합 배열 간의 작업을 제공하여 부울 식으로 지정된 부모 valarray의 하위 집합인 개체를 지원하는 내부 보조 템플릿 클래스입니다.|  
|[slice 클래스](../standard-library/slice-class.md)|valarray의 벡터와 유사한 1차원 하위 집합을 정의하는 데 사용되는 valarray에 대한 유틸리티 클래스입니다.|  
|[slice_array 클래스](../standard-library/slice-array-class.md)|valarray의 조각으로 정의된 하위 집합 배열 간의 작업을 제공하여 조각 개체를 지원하는 내부 보조 템플릿 클래스입니다.|  
|[valarray 클래스](../standard-library/valarray-class.md)|템플릿 클래스는 배열로 저장되어 고속 수치 연산을 수행하도록 설계되고 컴퓨팅 성능에 최적화된 **Type** 형식의 요소 시퀀스를 제어하는 개체를 설명합니다.|  
  
### <a name="specializations"></a>특수화  
  
|||  
|-|-|  
|[valarray\<bool> 클래스](../standard-library/valarray-bool-class.md)|`bool` 형식의 요소에 대한 템플릿 클래스 valarray\<**Type**>의 특수 버전입니다.|  
  
## <a name="see-also"></a>참고 항목  
 [헤더 파일 참조](../standard-library/cpp-standard-library-header-files.md)   
 [C++ 표준 라이브러리의 스레드 보안](../standard-library/thread-safety-in-the-cpp-standard-library.md)



