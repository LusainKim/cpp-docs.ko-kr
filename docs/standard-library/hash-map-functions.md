---
title: "&lt;hash_map&gt; 함수 | Microsoft 문서"
ms.custom: 
ms.date: 11/04/2016
ms.reviewer: 
ms.suite: 
ms.tgt_pltfrm: 
ms.topic: article
f1_keywords:
- hash_map/std::swap
- hash_map/std::swap (hash_map)
ms.assetid: 28748cd0-71f7-41b9-b068-579183645fba
caps.latest.revision: "9"
manager: ghogen
ms.openlocfilehash: 4b98135f1b72c66938d00f16649d011a27369473
ms.sourcegitcommit: ca2f94dfd015e0098a6eaf5c793ec532f1c97de1
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 10/31/2017
---
# <a name="lthashmapgt-functions"></a>&lt;hash_map&gt; 함수
|||  
|-|-|  
|[swap](#swap)|[swap(hash_map)](#swap_hash_map)|  
  
##  <a name="swap_hash_map"></a>  swap(hash_map)  
  
> [!NOTE]
>  이 API는 더 이상 사용되지 않습니다. [unordered_map 클래스](../standard-library/unordered-map-class.md)를 대신 사용하는 것이 좋습니다.  
  
 두 hash_map의 요소를 교환합니다.  
  
```
void swap(
    hash_map <Key, Type, Traits, Alloctor>& left,
    hash_map <Key, Type, Traits, Allocator>& right);
```  
  
### <a name="parameters"></a>매개 변수  
 `right`  
 map `left`와 요소를 교환할 hash_map입니다.  
  
 `left`  
 map `right`와 요소를 교환할 hash_map입니다.  
  
### <a name="remarks"></a>설명  
 템플릿 함수는 멤버 함수 `left.`[swap](../standard-library/basic-ios-class.md#swap)*(right*)을 실행하기 위해 컨테이너 클래스 hash_map에서 특수화된 알고리즘입니다. 이 함수는 컴파일러에서 지정하는 함수 템플릿의 부분 순서 인스턴스입니다. 함수를 호출할 때 템플릿이 고유하게 일치하지 않는 방식으로 템플릿 함수가 오버로드되면 컴파일러는 템플릿 함수의 가장 특수화된 버전을 선택합니다. 알고리즘 헤더 파일에 있는 템플릿 함수의 일반 버전인 **template \<class T> void swap(T&, T&)**은 할당을 기준으로 작동하는 속도가 느린 작업입니다. 각 컨테이너의 특수화된 버전은 컨테이너 클래스의 내부 표현을 사용할 수 있으므로 속도가 훨씬 빠릅니다.  
  
##  <a name="swap"></a>  swap  
  
> [!NOTE]
>  이 API는 더 이상 사용되지 않습니다. [unordered_multimap 클래스](../standard-library/unordered-multimap-class.md)를 대신 사용하는 것이 좋습니다.  
  
 두 hash_multimap의 요소를 교환합니다.  
  
```
void swap(
    hash_multimap <Key, Type, Traits, Alloctor>& left,
    hash_multimap <Key, Type, Traits, Allocator>& right);
```  
  
### <a name="parameters"></a>매개 변수  
 `right`  
 map `left`와 요소를 교환할 hash_multimap입니다.  
  
 `left`  
 map `right`와 요소를 교환할 hash_multimap입니다.  
  
### <a name="remarks"></a>설명  
 템플릿 함수는 멤버 함수 `left.`[swap](../standard-library/hash-multimap-class.md#swap)*(right*`)`을 실행하기 위해 컨테이너 클래스 hash_multimap에서 특수화된 알고리즘입니다. 이 함수는 컴파일러에서 지정하는 함수 템플릿의 부분 순서 인스턴스입니다. 함수를 호출할 때 템플릿이 고유하게 일치하지 않는 방식으로 템플릿 함수가 오버로드되면 컴파일러는 템플릿 함수의 가장 특수화된 버전을 선택합니다. 알고리즘 헤더 파일에 있는 템플릿 함수의 일반 버전인 **template \<class T> void swap(T&, T&)**은 할당을 기준으로 작동하는 속도가 느린 작업입니다. 각 컨테이너의 특수화된 버전은 컨테이너 클래스의 내부 표현을 사용할 수 있으므로 속도가 훨씬 빠릅니다.  
  
## <a name="see-also"></a>참고 항목  
 [<hash_map>](../standard-library/hash-map.md)



