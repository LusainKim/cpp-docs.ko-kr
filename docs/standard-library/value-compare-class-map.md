---
title: "value_compare 클래스(&lt;map&gt;) | Microsoft Docs"
ms.custom: 
ms.date: 11/04/2016
ms.reviewer: 
ms.suite: 
ms.technology: cpp-standard-libraries
ms.tgt_pltfrm: 
ms.topic: article
f1_keywords:
- std::value_compare
- std.value_compare
- map/std::value_compare
- value_compare
dev_langs: C++
helpviewer_keywords: std::value_compare
ms.assetid: ea97c1d0-04b2-4d42-8d96-23522c04cc41
caps.latest.revision: "21"
author: corob-msft
ms.author: corob
manager: ghogen
ms.workload: cplusplus
ms.openlocfilehash: 1e05f4e0f4431ac9911f98c10540b7aa03a3f486
ms.sourcegitcommit: 8fa8fdf0fbb4f57950f1e8f4f9b81b4d39ec7d7a
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 12/21/2017
---
# <a name="valuecompare-class-ltmapgt"></a>value_compare 클래스(&lt;map&gt;)
키 값 비교를 통해 맵의 요소를 비교하여 map 내의 상대 순서를 확인할 수 있는 함수 개체를 제공합니다.  
  
## <a name="syntax"></a>구문  
  
```
class value_compare : public binary_function<value_type, value_type, bool>
{
public:
    bool operator()(const value_type& left, const value_type& right) const;
    value_compare(key_compare pred) : comp(pred);
protected:
    key_compare comp;
};
```  
  
## <a name="remarks"></a>설명  
 map에 포함된 전체 요소의 **value_types** 간에 `value_compare`가 제공하는 비교 기준은 보조 클래스 생성에 의한 개별 요소의 키 간 비교에서 제공됩니다. 구성원 함수 연산자는 `value_compare`에서 제공하는 함수 개체에 저장된 `key_compare` 형식의 개체 **comp**를 사용하여 두 요소의 정렬 키 구성 요소를 비교합니다.  
  
 키 값이 요소 값과 동일한 단순 컨테이너인 sets 및 multisets의 경우 `value_compare`는 `key_compare`와 동일합니다. 반면 maps 및 multimaps의 경우에는 `pair` 형식 요소의 값이 요소 키의 값과 동일하지 않으므로 value_compare가 key_compare와 동일하지 않습니다.  
  
## <a name="example"></a>예  
  `value_compare`를 선언하고 사용하는 방법의 예제는 [value_comp](../standard-library/map-class.md#value_comp)의 예제를 참조하세요.  
  
## <a name="requirements"></a>요구 사항  
 **헤더:** \<map>  
  
 **네임스페이스:** std  
  
## <a name="see-also"></a>참고 항목  
 [binary_function 구조체](../standard-library/binary-function-struct.md)   
 [C++ 표준 라이브러리의 스레드 보안](../standard-library/thread-safety-in-the-cpp-standard-library.md)   
 [C++ 표준 라이브러리 참조](../standard-library/cpp-standard-library-reference.md)



