---
title: "연산자 주소 및 간접 참조 | Microsoft Docs"
ms.custom: 
ms.date: 11/04/2016
ms.reviewer: 
ms.suite: 
ms.technology: cpp-language
ms.tgt_pltfrm: 
ms.topic: article
dev_langs: C++
helpviewer_keywords:
- address-of operator (&)
- '* operator'
- operators [C++], address-of
- ampersand operator (&)
- '* operator, indirection operator'
- addresses [C++], indirection
- addresses [C++]
- indirection operator
- '& operator, address-of operator'
- null pointers [C++]
- '* operator, address-of operator'
- operators [C++], indirection
ms.assetid: 10d62b00-12ba-4ea9-a2d5-09ac29ca2232
caps.latest.revision: "6"
author: mikeblome
ms.author: mblome
manager: ghogen
ms.workload: cplusplus
ms.openlocfilehash: 715221da8ea960f19e9c4ab0e386afc61c3439fc
ms.sourcegitcommit: 8fa8fdf0fbb4f57950f1e8f4f9b81b4d39ec7d7a
ms.translationtype: HT
ms.contentlocale: ko-KR
ms.lasthandoff: 12/21/2017
---
# <a name="indirection-and-address-of-operators"></a>연산자 주소 및 간접 참조
간접 참조 연산자(**\***)는 포인터를 통해 값에 간접 액세스합니다. 피연산자는 포인터 값이어야 합니다. 연산 결과는 피연산자가 가리키는 주소에 있는 값입니다. 결과의 형식은 피연산자가 표시하는 형식과 동일합니다.  
  
 피연산자가 함수를 가리키는 경우 결과는 함수 지정자입니다. 저장소 위치를 가리키는 경우 결과는 저장소 위치를 지정하는 l-value입니다.  
  
 포인터 값이 잘못된 경우 결과가 정의되지 않습니다. 다음 목록은 포인터 값을 무효화하는 가장 일반적인 조건의 일부입니다.  
  
-   포인터가 null 포인터입니다.  
  
-   포인터가 참조 시 표시되지 않는 로컬 항목의 주소를 지정합니다.  
  
-   포인터가 가리키는 개체의 형식에 대해 부적절하게 정렬된 주소를 지정합니다.  
  
-   포인터가 실행 중인 프로그램에서 사용되지 않는 주소를 지정합니다.  
  
 주소 연산자(**&**)는 피연산자의 주소를 제공합니다. 주소 연산자의 피연산자는 함수 지정자 또는 l-value가 될 수 있습니다. 이때, l-value가 지정하는 개체는 비트 필드가 아니며 **register** 저장소 클래스 지정자로 선언되지 않습니다.  
  
 주소 연산의 결과는 피연산자에 대한 포인터입니다. 포인터가 표시하는 형식은 피연산자의 형식입니다.  
  
 주소 연산자는 파일 범위 수준에서 선언된 기본, 구조체 또는 공용 구조체 형식의 변수 또는 첨자된 배열 참조에만 적용될 수 있습니다. 이러한 식에서는 주소 연산자가 없는 상수 식을 주소 식에 추가하거나 뺄 수 있습니다.  
  
## <a name="examples"></a>예제  
 다음은 이러한 선언이 사용된 예제입니다.  
  
```  
int *pa, x;  
int a[20];  
double d;  
```  
  
 이 문은 주소 연산자를 사용합니다.  
  
```  
pa = &a[5];  
```  
  
 주소 연산자(**&**)는 `a` 배열의 여섯 번째 요소의 주소를 가져옵니다. 결과는 포인터 변수 `pa`에 저장됩니다.  
  
```  
x = *pa;  
```  
  
 이 예제에서는 간접 참조 연산자(**\***)를 사용하여 `pa`에 저장된 주소의 `int` 값에 액세스합니다. 값이 정수 변수 `x`에 할당됩니다.  
  
```  
if( x == *&x )  
    printf( "True\n" );  
```  
  
 이 예는 단어 `True`를 출력하여 `x`의 주소에 간접 연산자를 적용한 결과가 `x`와 동일하다는 것을 나타냅니다.  
  
```  
int roundup( void );     /* Function declaration */  
  
int  *proundup  = roundup;  
int  *pround  = &roundup;  
```  
  
 함수 `roundup`이 선언되면 `roundup`에 대한 두 개의 포인터가 선언되고 초기화됩니다. 첫 번째 포인터, `proundup`은 해당 함수의 이름만을 사용하여 초기화되지만 두 번째 포인터, `pround`는 초기화 시 주소 연산자를 사용합니다. 초기화는 동일합니다.  
  
## <a name="see-also"></a>참고 항목  
 [간접 참조 연산자: *](../cpp/indirection-operator-star.md)   
 [주소 연산자: &](../cpp/address-of-operator-amp.md)