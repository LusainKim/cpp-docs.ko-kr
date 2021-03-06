---
title: "기본적으로 해제 되어 있는 컴파일러 경고 | Microsoft Docs"
ms.date: 11/04/2016
ms.technology: cpp-tools
ms.topic: article
dev_langs: C++
helpviewer_keywords:
- warnings, compiler
- cl.exe compiler, setting options
ms.assetid: 69809cfb-a38a-4035-b154-283a61938df8
author: corob-msft
ms.author: corob
manager: ghogen
ms.workload: cplusplus
ms.openlocfilehash: 48afd89f4b795a4f582d8b9506c527a602a1d2b4
ms.sourcegitcommit: 8fa8fdf0fbb4f57950f1e8f4f9b81b4d39ec7d7a
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 12/21/2017
---
# <a name="compiler-warnings-that-are-off-by-default"></a>기본적으로 해제되어 있는 컴파일러 경고

컴파일러는 대부분의 사용자에게 표시되면 안 되기 때문에 기본적으로 해제되어 있는 경고를 포함합니다. 그러나 다음 옵션 중 하나를 사용하여 이러한 경고를 사용할 수 있습니다.

`#pragma warning(default : warning_number )`  
지정된 경고(`warning_number`)가 기본 수준에서 사용됩니다. 경고 설명서에 경고의 기본 수준이 포함되어 있습니다.

`#pragma warning( warning_level : warning_number )`  
지정된 경고(`warning_number`)가 지정된 수준(`warning_level`)에서 사용됩니다.

[/Wall](../build/reference/compiler-option-warning-level.md)  
**/ 벽** 기본적으로 해제 되어 있는 모든 경고를 활성화 합니다.

다음 경고는 기본적으로 해제되어 있습니다.

|||
|-|-|
|[C4061](../error-messages/compiler-warnings/compiler-warning-level-4-c4061.md) (수준 4)|열거형 'enumeration'의 switch에 있는 'identifier' 열거자는 case 레이블에 의해 명시적으로 처리되지 않습니다.|
|[C4062](../error-messages/compiler-warnings/compiler-warning-level-4-c4062.md) (수준 4)|열거형 'enumeration'의 switch에 있는 'identifier' 열거자가 처리되지 않습니다.|
|C4191(수준 3)|'operator/operation': '식 형식'에서 '필요한 형식'(으)로의 변환이 안전하지 않습니다.|
|[C4242](../error-messages/compiler-warnings/compiler-warning-level-4-c4242.md) (수준 4)|'identifier': 'type1'에서 'type2'(으)로 변환하면서 데이터가 손실될 수 있습니다.|
|[C4254](../error-messages/compiler-warnings/compiler-warning-level-4-c4254.md) (수준 4)|'operator': 'type1'에서 'type2'(으)로 변환하면서 데이터가 손실될 수 있습니다.|
|[C4255](../error-messages/compiler-warnings/compiler-warning-level-4-c4255.md) (수준 4)|'function': 함수 프로토타입을 입력하지 않았습니다. '()'에서 '(void)'로 변환됩니다.|
|[C4263](../error-messages/compiler-warnings/compiler-warning-level-4-c4263.md) (수준 4)|'function': 멤버 함수가 기본 클래스 가상 멤버 함수를 재정의하지 않습니다.|
|[C4264](../error-messages/compiler-warnings/compiler-warning-level-1-c4264.md) (수준 1)|'virtual_function': 기본 'class'의 가상 멤버 함수에 대해 재정의를 사용할 수 없습니다. 함수가 숨겨집니다.|
|[C4265](../error-messages/compiler-warnings/compiler-warning-level-3-c4265.md) (수준 3)|'class': 클래스에 가상 함수가 있지만 소멸자는 가상이 아닙니다.|
|[C4266](../error-messages/compiler-warnings/compiler-warning-level-4-c4266.md) (수준 4)|'function': 기본 'type'의 가상 멤버 함수에 대해 재정의를 사용할 수 없습니다. 함수가 숨겨집니다.|
|[C4287](../error-messages/compiler-warnings/compiler-warning-level-3-c4287.md) (수준 3)|'operator': 부호 없는 상수 또는 음의 상수가 일치하지 않습니다.|
|[C4289](../error-messages/compiler-warnings/compiler-warning-level-4-c4289.md) (수준 4)|비표준 확장이 사용됨 : 'var' : for 루프에서 선언된 루프 제어 변수가 for 루프 범위 외부에서 사용되었습니다.|
|[C4296](../error-messages/compiler-warnings/compiler-warning-level-4-c4296.md) (수준 4)|'operator': 식이 항상 false입니다.|
|[C4339](../error-messages/compiler-warnings/compiler-warning-level-4-c4339.md) (수준 4)|'type' : CLR 메타데이터에 정의되지 않은 형식이 사용되었습니다. 이 형식을 사용하면 런타임 예외가 발생할 수 있습니다.|
|[C4342](../error-messages/compiler-warnings/compiler-warning-level-1-c4342.md) (수준 1)|동작 변경: 'function'이(가) 호출되었지만 이전 버전에서는 멤버 연산자가 호출되었습니다.|
|[C4350](../error-messages/compiler-warnings/compiler-warning-level-1-c4350.md) (수준 1)|동작 변경: 'member1'이(가) 'member2' 대신 호출됩니다.|
|[C4355](../error-messages/compiler-warnings/compiler-warning-c4355.md)|'this' : 기본 멤버 이니셜라이저 목록에서 사용되었습니다.|
|[C4365](../error-messages/compiler-warnings/compiler-warning-level-4-c4365.md) (수준 4)|'action': 'type_1'에서 'type_2'(으)로의 변환입니다. signed 또는 unsigned가 일치하지 않습니다.|
|C4370 (수준 3)|압축 기능이 향상되어 이전 버전의 컴파일러에서 클래스 레이아웃이 변경되었습니다.|
|C4371 (수준 3)|'member' 멤버를 잘 압축했기 때문에 이전 버전의 컴파일러에서 클래스 레이아웃이 변경되었을 수 있습니다.|
|C4388 (수준 4)|signed 또는 unsigned가 일치하지 않습니다.|
|[C4412](../error-messages/compiler-warnings/compiler-warning-level-2-c4412.md) (수준 2)|'function': 함수 시그니처에 'type' 형식이 있습니다. 순수형 코드와 혼합형/네이티브 코드 간에 C++ 개체를 전달하는 것은 안전하지 않습니다.|
|C4426 (수준 1)|헤더를 포함 한 후 변경 된 최적화 플래그 #pragma optimize() 되었기 때문일 수 있습니다.|
|[C4435](../error-messages/compiler-warnings/compiler-warning-level-4-c4435.md) (수준 4)|'class1': 가상 기본 'class2'(으)로 인해 /vd2의 개체 레이아웃이 변경됩니다.|
|[C4437](../error-messages/compiler-warnings/compiler-warning-level-4-c4437.md) (수준 4)|가상 기본 'class1'에서 'class2' 사이의 dynamic_cast가 일부 컨텍스트에서 실패할 수 있습니다.|
|C4444 (수준 3)|이 컨텍스트에서는 최상위 '__unaligned'가 구현되지 않았습니다.|
|C4464 (수준 4)|include에 상대 경로 포함 '..'|
|C 4472 (수준 1)|'identifier'가 네이티브 열거형입니다. 관리되는 열거형을 선언하려면 액세스 지정자(전용/공용)를 추가합니다.|
|[C4514](../error-messages/compiler-warnings/compiler-warning-level-4-c4514.md) (수준 4)|'function': 참조되지 않은 인라인 함수를 제거했습니다.|
|[C4536](../error-messages/compiler-warnings/compiler-warning-level-4-c4536.md) (수준 4)|'type name': 형식-이름이 메타데이터 한계인 '한계'자를 초과합니다.|
|[C4545](../error-messages/compiler-warnings/compiler-warning-level-1-c4545.md) (수준 1)|쉼표 앞의 식이 인수 목록이 없는 함수로 계산됩니다.|
|[C4546](../error-messages/compiler-warnings/compiler-warning-level-1-c4546.md) (수준 1)|쉼표 앞의 함수에 인수 목록이 없습니다.|
|[C4547](../error-messages/compiler-warnings/compiler-warning-level-1-c4547.md) (수준 1)|'operator': 쉼표 앞의 연산자는 의미가 없습니다. 파생 작업이 있는 연산자여야 합니다.|
|[C4548](../error-messages/compiler-warnings/compiler-warning-level-1-c4548.md) (수준 1)|쉼표 앞의 식은 의미 없는 식입니다. 파생 작업이 있는 식이어야 합니다.|
|[C4549](../error-messages/compiler-warnings/compiler-warning-level-1-c4549.md) (수준 1)|'operator': 쉼표 앞의 연산자는 의미가 없습니다. 'operator'을(를) 사용하려고 했습니까?|
|[C4555](../error-messages/compiler-warnings/compiler-warning-level-1-c4555.md) (수준 1)|식이 효과가 없습니다. 파생 작업이 있는 식이어야 합니다.|
|[C4557](../error-messages/compiler-warnings/compiler-warning-level-3-c4557.md) (수준 3)|'__assume'에 'effect' 효과가 있습니다.|
|[C4571](../error-messages/compiler-warnings/compiler-warning-level-4-c4571.md) (수준 4)|변경; Visual c + + 7.1부터 catch (...) 의미 체계를 알림: 구조적된 예외 (SEH) 변경 되었습니다.|
|C4574 (수준 4)|'식별자'가 '0'이 되도록 정의되어 있습니다. '#if 식별자'를 사용한 것은 아닌지 확인하십시오.|
|C4582 (수준 4)|'*형식*': 생성자가 암시적으로 호출 되지 않습니다|
|C4583 (수준 4)|'*형식*': 소멸자가 암시적으로 호출|
|C4587 (수준 1)|'*anonymous_structure*': 동작 변경: 생성자가 더 이상 암시적으로 호출|
|C4588 (수준 1)|'*anonymous_structure*': 동작 변경: 소멸자가 더 이상 암시적으로 호출 되 고 없습니다.|
|C4598 (수준 1 및 수준 3)|' #include "*헤더*"': 헤더 번호 *번호* 미리 컴파일된 헤더의 해당 위치에서 현재 컴파일의 일치 하지 않습니다|
|C4599 (수준 3)|'*옵션* *경로*': 명령줄 인수 번호 *번호* 미리 컴파일된 헤더와 일치 하지 않습니다|
|C4605 (수준 1)|' /D*매크로*' 현재 명령줄에 지정 되었지만 미리 컴파일된 헤더 빌드 했을 때 지정 되지 않았습니다|
|[C4619](../error-messages/compiler-warnings/compiler-warning-level-3-c4619.md) (수준 3)|#pragma warning: 경고 번호 '번호'이(가) 없습니다.|
|[C4623](../error-messages/compiler-warnings/compiler-warning-level-4-c4623.md) (수준 4)|'derived class': 기본 클래스의 기본 생성자에 액세스할 수 없으므로 기본 생성자를 생성할 수 없습니다.|
|[C4625](../error-messages/compiler-warnings/compiler-warning-level-4-c4625.md) (수준 4)|'derived class': 기본 클래스의 복사 생성자에 액세스할 수 없으므로 복사 생성자를 생성할 수 없습니다.|
|[C4626](../error-messages/compiler-warnings/compiler-warning-level-4-c4626.md) (수준 4)|'derived class': 기본 클래스의 대입 연산자에 액세스할 수 없으므로 대입 연산자를 생성할 수 없습니다.|
|[C4628](../error-messages/compiler-warnings/compiler-warning-level-1-c4628.md) (수준 1)|-Ze에는 digraph가 지원되지 않습니다. 문자 시퀀스 'digraph'은(는) 'char'에 대한 대체 토큰으로 해석되지 않습니다.|
|[C4640](../error-messages/compiler-warnings/compiler-warning-level-3-c4640.md) (수준 3)|'instance': 지역 정적 개체를 생성할 때 스레드로부터 안전하게 보호되지 않습니다.|
|C4647 (수준 3)|동작 변경: __is_pod (*형식*) 이전 버전에 서로 다른 값|
|C4654 (수준 4)|미리 컴파일된 헤더의 앞에 배치 하는 코드는 무시 됩니다. 미리 컴파일된 헤더에 코드를 추가 합니다.|
|[C4668](../error-messages/compiler-warnings/compiler-warning-level-4-c4668.md) (수준 4)|'*기호*'에 '0'으로 바뀝니다. 전처리기 매크로로 정의 되지 않은'*지시문*'|
|[C4682](../error-messages/compiler-warnings/compiler-warning-level-4-c4682.md) (수준 4)|'*기호*': 방향 매개 변수 특성을 지정 하지 [in]를 기본값으로 설정|
|[C4686](../error-messages/compiler-warnings/compiler-warning-level-3-c4686.md) (수준 3)|'*사용자 정의 형식*': 동작 변경 되었을 수, udt 반환 호출 규칙이|
|[C4692](../error-messages/compiler-warnings/compiler-warning-level-1-c4692.md) (수준 1)|'*함수*': 전용이 아닌 멤버의 시그니처에 어셈블리 전용 네이티브 형식 'native_type'|
|[C4710](../error-messages/compiler-warnings/compiler-warning-level-4-c4710.md) (수준 4)|'*함수*': 함수를 인라이닝 하지 못했습니다.|
|[C4738](../error-messages/compiler-warnings/compiler-warning-level-3-c4738.md) (수준 3)|32비트 float 결과를 메모리에 저장하면 성능이 저하될 수 있습니다.|
|[C4746](../error-messages/compiler-warnings/compiler-warning-c4746.md)|volatile 액세스 '*식*' /volatile:\<iso &#124; ms > __iso_volatile_load/store 내장 함수를 사용 하 여 고려 설정;|
|C4749 (수준 4)|조건에 따라 지원: non standard-레이아웃 형식에 적용 된 offsetof '*형식*'|
|C4767 (수준 4)|섹션 이름 '*기호*' 8 자 보다 긺 및 링커에서 잘립니다|
|C4768 (수준 3)|링크 사양이 이전 __declspec 특성이 무시 됩니다.|
|C4774 (수준 4)|'*문자열*': 서식 문자열 인수에 필요한 *번호* 이 문자열 리터럴|
|C4786 (수준 3)|'*기호*': 개체 이름이 디버그 정보의 'number' 자로 잘렸습니다.|
|[C4820](../error-messages/compiler-warnings/compiler-warning-level-4-c4820.md) (수준 4)|'bytes'바이트 채움 문자가 construct 'member_name' 뒤에 추가되었습니다.|
|C4826 (수준 2)|변환에서 '*type1*'to'*type2*' 부호가 확장 됩니다. 이렇게 하면 예기치 않은 런타임 동작이 발생할 수 있습니다.|
|C4837 (수준 4)|발견 된 삼중 자: '?? *문자*'교체'*문자*'|
|C4841 (수준 4)|비표준 확장이 사용 됨: offsetof에 사용 되는 복합 멤버 지정자|
|C4842 (수준 4)|다중 상속을 사용 하 여 형식에 적용 하는 'offsetof'의 결과 컴파일러 버전 간에 일관 되도록 보장 되지|
|[C4868](../error-messages/compiler-warnings/compiler-warning-c4868.md) (수준 4)|'_파일_(*line_number*)' 컴파일러는 중괄호로 묶인된 초기화 목록에서 왼쪽에서 오른쪽 평가 순서를 적용할 수 없습니다.|
|[C4905](../error-messages/compiler-warnings/compiler-warning-level-1-c4905.md) (수준 1)|와이드 문자열 리터럴을 'LPSTR'로 캐스팅했습니다.|
|[C4906](../error-messages/compiler-warnings/compiler-warning-level-1-c4906.md) (수준 1)|문자열 리터럴을 'LPWSTR'로 캐스팅했습니다.|
|[C4917](../error-messages/compiler-warnings/compiler-warning-level-1-c4917.md) (수준 1)|'declarator': GUID는 클래스, 인터페이스 또는 네임스페이스와만 연결할 수 있습니다.|
|[C4928](../error-messages/compiler-warnings/compiler-warning-level-1-c4928.md) (수준 1)|복사 초기화가 잘못되었습니다. 사용자 정의 변환이 암시적으로 두 번 이상 적용되었습니다.|
|[C4931](../error-messages/compiler-warnings/compiler-warning-level-4-c4931.md) (수준 4)|number비트 포인터에 대한 형식 라이브러리를 빌드했다고 간주합니다.|
|[C4946](../error-messages/compiler-warnings/compiler-warning-level-1-c4946.md) (수준 1)|관련 클래스 'class1'과(와) 'class2' 사이에 reinterpret_cast가 사용되었습니다.|
|C4962|'function': 최적화를 하면 프로필 데이터가 일관성이 없어지므로 프로필 기반 최적화를 사용하지 않습니다.|
|[C4986](../error-messages/compiler-warnings/compiler-warning-c4986.md) (수준 4)|'*기호*': 예외 사양이 이전 선언과 일치 하지 않습니다|
|C4987 (수준 4)|비표준 확장 사용: 'throw (...)'|
|C4988 (수준 4)|'*기호*': 변수가 클래스/함수 범위 외부 선언|
|C5022|'*형식*': 지정 된 여러 명의 이동 생성자|
|C5023|'*형식*': 지정 된 여러 명의 이동 할당 연산자|
|C5024 (수준 4)|'*형식*': 이동 생성자가 암시적으로 삭제 된 것으로 정의 됩니다|
|C5025 (수준 4)|'*형식*': 이동 할당 연산자가 암시적으로 삭제 된 것으로 정의 됩니다|
|C5026 (수준 1 및 수준 4)|'*형식*': 이동 생성자가 암시적으로 삭제 된 것으로 정의 됩니다|
|C5027 (수준 1 및 수준 4)|'*형식*': 이동 할당 연산자가 암시적으로 삭제 된 것으로 정의 됩니다|
|C5029 (수준 4)|비표준 확장이 사용 됨: 변수, 데이터 멤버 및 태그 형식에만에 c + +의 맞춤 특성 적용|
|C5031 (수준 4)|#pragma warning(pop): 일치 하지 않을 수, 다른 파일에서 푸시된 경고 상태를 팝 합니다.|
|C 5032가 발생 (수준 4)|없는 해당 #pragma warning(pop) #pragma warning (push)를 발견 했습니다.|
|C5035|기능을 사용 하 여 '*기능*' 하면 함수 *함수* 게스트 코드로 컴파일할 수를|
|C5036 (수준 1)|/hybrid:x86arm64로 컴파일할 때 varargs 함수 포인터 변환이 있습니다. '*type1*'to'*type2*'|

하지 않는 한 이러한 경고는 해제는 [관대 한 /-](../build/reference/permissive-standards-conformance.md) 컴파일러 옵션을 설정 합니다.

|||
|-|-|
|[C4471 (수준 4)](../error-messages/compiler-warnings/compiler-warning-level-4-c4471.md)|범위가 지정되지 않은 열거형의 정방향 선언에는 내부 형식이 있어야 합니다(int로 가정).|
|[C4608 (수준 3)](../error-messages/compiler-warnings/compiler-warning-level-3-c4608.md)|' union\_멤버 ' 'union_member' 이니셜라이저 목록의 다른 공용 구조체 멤버에서 이미 초기화|


이러한 경고의 Visual Studio 2015 이전 컴파일러 버전에서는 기본적으로 해제 했습니다.

|||
|-|-|
|[C4302](../error-messages/compiler-warnings/compiler-warning-level-2-c4302.md) (수준 2)|'conversion': 'type1'에서 'type2'(으)로 잘립니다.|
|[C4311](../error-messages/compiler-warnings/compiler-warning-level-1-c4311.md) (수준 1)|'variable' : 'type'에서 'type'(으)로 포인터가 잘립니다.|
|[C4312](../error-messages/compiler-warnings/compiler-warning-level-1-c4312.md) (수준 1)|'identifier' : 'type1'에서 더 큰 'type2'(으)로의 변환입니다.|
|[C4319](../error-messages/compiler-warnings/compiler-warning-level-1-c4319.md) (수준 1)|'operator': 0 확장 'type1' 더 큰 'type2'|

이러한 경고의 Visual Studio 2012 이전의 컴파일러 버전에서는 기본적으로 해제 했습니다.

|||
|-|-|
|[C4431](../error-messages/compiler-warnings/compiler-warning-level-4-c4431.md) (수준 4)|형식 지정자가 없습니다. int로 가정합니다. 참고: C에서는 더 이상 기본 int를 지원하지 않습니다.|

## <a name="see-also"></a>참고 항목

[warning](../preprocessor/warning.md)
