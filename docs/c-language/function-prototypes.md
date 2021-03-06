---
title: "함수 프로토타입 | Microsoft Docs"
ms.custom: 
ms.date: 11/04/2016
ms.reviewer: 
ms.suite: 
ms.technology: cpp-language
ms.tgt_pltfrm: 
ms.topic: article
dev_langs: C++
helpviewer_keywords:
- function prototypes
- function return types, function prototypes
- data types [C], function return types
- functions [C], return types
- prototypes [C++], function
ms.assetid: d152f8e6-971e-432c-93ca-5a91400653c2
caps.latest.revision: "9"
author: mikeblome
ms.author: mblome
manager: ghogen
ms.workload: cplusplus
ms.openlocfilehash: ea02b5b3bb1517623a0c3fc67a752d203f81c5a8
ms.sourcegitcommit: 8fa8fdf0fbb4f57950f1e8f4f9b81b4d39ec7d7a
ms.translationtype: HT
ms.contentlocale: ko-KR
ms.lasthandoff: 12/21/2017
---
# <a name="function-prototypes"></a>함수 프로토타입
함수 선언은 함수 정의 앞에 오고 이름, 반환 형식, 저장소 클래스 및 함수의 다른 특성을 지정합니다. 프로토타입이 되려면 함수 선언은 함수 인수에 대한 형식 및 식별자도 설정해야 합니다.  
  
## <a name="syntax"></a>구문  
 `declaration`:  
 *declaration-specifiers attribute-seq* opt*init-declarator-list* opt**;**  
  
 /\* *attribute-seq* opt는 Microsoft 전용임 */  
  
 *declaration-specifiers*:  
 *storage-class-specifier declaration-specifiers* opt  
  
 *type-specifier declaration-specifiers* opt  
  
 *type-qualifier declaration-specifiers* opt  
  
 *init-declarator-list*:  
 *init-declarator*  
  
 *init-declarator-list*  **,**  *init-declarator*  
  
 *init-declarator*:  
 *declarator*  
  
 *declarator = initializer*  
  
 `declarator`:  
 *pointer* opt*direct-declarator*  
  
 *direct-declarator*: /\* 함수 선언자 \*/  
 *direct-declarator*  **(**  *parameter-type-list*  **)**  /* 새로운 스타일의 선언자 \*/  
  
 *direct-declarator*  **(**  *identifier-list* opt**)** /* 사용되지 않는 스타일의 선언자 \*/  
  
 프로토타입은 닫는 괄호 바로 다음에 오는 세미콜론으로 종료되므로 본문이 없다는 점을 제외하고 함수 정의와 형태가 동일합니다. 어떤 경우든 간에 반환 형식은 함수 정의에 지정된 반환 형식과 일치해야 합니다.  
  
 함수 프로토타입에는 다음과 같은 중요한 용도가 있습니다.  
  
-   `int` 이외의 형식을 반환하는 함수의 반환 형식을 설정합니다. `int` 값을 반환하는 함수에는 프로토타입이 필요하지 않지만 프로토타입을 사용하는 것이 좋습니다.  
  
-   전체 프로토타입이 없는 경우 표준 변환이 수행되지만 매개 변수의 수에 대해 인수의 수나 형식이 확인되지 않습니다.  
  
-   프로토타입은 함수를 정의하기 전에 해당 함수에 대한 포인터를 초기화하는 데 사용됩니다.  
  
-   매개 변수 목록은 함수 호출의 인수가 함수 정의의 매개 변수와 대응되는지를 확인하는 데 사용됩니다.  
  
 각 매개 변수의 변환된 형식에 따라 함수 호출이 스택에 배치하는 인수의 해석이 결정됩니다. 인수와 매개 변수의 형식이 일치하지 않으면 스택에 있는 인수가 잘못 해석될 수 있습니다. 예를 들어 16비트 컴퓨터에서 16비트 포인터가 인수로 전달된 후 **long** 매개 변수로 선언되면 스택의 첫 번째 32비트는 **long** 매개 변수로 해석됩니다. 이 오류는 **long** 매개 변수뿐만 아니라 그 뒤의 모든 매개 변수에서 문제를 발생시킵니다. 모든 함수에 대한 전체 함수 프로토타입을 선언하여 이러한 종류의 오류를 감지할 수 있습니다.  
  
 프로토타입은 함수 정의 앞에 오는(또는 다른 소스 파일에서 발생하는) 함수 호출에 대한 인수 형식과 반환 형식의 불일치를 확인할 수 있도록 함수의 특성을 설정합니다. 예를 들어 프로토타입에서 **static** 저장소 클래스 지정자를 지정하는 경우 함수 정의에서도 **static** 저장소 클래스를 지정해야 합니다.  
  
 전체 매개 변수 선언(`int a`)은 동일한 선언에서 추상 선언자(`int`)와 함께 사용할 수 있습니다. 예를 들어 다음 선언은 유효합니다.  
  
```  
int add( int a, int );  
```  
  
 프로토타입은 인수로 전달되는 각 식의 형식과 식별자를 둘 다 포함할 수 있습니다. 하지만 이러한 식별자는 선언의 끝까지만 범위를 갖습니다. 또한 프로토타입은 인수의 수가 가변적이거나 전달되는 인수가 없다는 사실도 반영할 수 있습니다. 이러한 목록이 없으면 불일치가 드러나지 않을 수 있으므로 컴파일러는 불일치와 관련된 진단 메시지를 생성할 수 없습니다. 형식 검사에 대한 자세한 내용은 [인수](../c-language/arguments.md)를 참조하세요.  
  
 Microsoft C 컴파일러에서 프로토타입 범위는 이제 /Za 컴파일러 옵션으로 컴파일할 때 ANSI 규격입니다. 즉, 프로토타입 내에서 `struct` 또는 **union** 태그를 선언하는 경우 태그는 전역 범위가 아니라 해당 범위에서 입력됩니다. 예를 들어 ANSI 규격을 따르기 위해 /Za를 사용하여 컴파일하는 경우 형식 불일치 오류를 발생시키지 않고는 다음 함수를 호출할 수 없습니다.  
  
```  
void func1( struct S * );  
```  
  
 코드를 수정하려면 함수 프로토타입 전에 `struct` 또는 **union**을 전역 범위에서 정의하거나 선언합니다.  
  
```  
struct S;  
void func1( struct S * );  
```  
  
 /Ze를 사용하는 경우 태그는 여전히 전역 범위에서 입력됩니다.  
  
## <a name="see-also"></a>참고 항목  
 [함수](../c-language/functions-c.md)