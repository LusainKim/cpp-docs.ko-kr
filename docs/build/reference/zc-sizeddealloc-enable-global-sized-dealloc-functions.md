---
title: "/Zc:sizedDealloc (전역 크기의 할당 해제 함수 사용) | Microsoft Docs"
ms.custom: 
ms.date: 12/13/2016
ms.reviewer: 
ms.suite: 
ms.technology: cpp-tools
ms.tgt_pltfrm: 
ms.topic: article
f1_keywords:
- sizedDealloc
- /Zc:sizedDealloc
dev_langs: C++
helpviewer_keywords:
- -Zc compiler options (C++)
- sizedDealloc
- Enable Global Sized Deallocation Functions
- /Zc compiler options (C++)
- Zc compiler options (C++)
ms.assetid: 3a73ace0-4d36-420a-b699-0ca6fc0dd134
caps.latest.revision: "1"
author: corob-msft
ms.author: corob
manager: ghogen
ms.workload: cplusplus
ms.openlocfilehash: 1343c037f87aee609de2b082cb87f7f1f2832221
ms.sourcegitcommit: 8fa8fdf0fbb4f57950f1e8f4f9b81b4d39ec7d7a
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 12/21/2017
---
# <a name="zcsizeddealloc-enable-global-sized-deallocation-functions"></a>/Zc:sizedDealloc (전역 크기의 할당 해제 함수 사용)  
`/Zc:sizedDealloc` 컴파일러 옵션 우선적으로 글로벌를 호출 하는 컴파일러가 `operator delete` 또는 `operator delete[]` 형식의 두 번째 매개 변수는 함수를 `size_t` 개체의 크기를 사용할 수 있습니다. 이러한 함수를 사용할 수는 `size_t` 비 할당자 성능을 최적화 하기 위해 매개 변수입니다.   
  
## <a name="syntax"></a>구문  
`/Zc:sizedDealloc`[`-`\]  
  
## <a name="remarks"></a>설명  
  
표준 C + + 11에서 정적 멤버 함수를 정의할 수 있습니다 `operator delete` 및 `operator delete[]` 는 두 번째 인수로 `size_t` 매개 변수입니다. 일반적으로 함께에서 사용 됩니다 이러한 [new 연산자](../../cpp/new-operator-cpp.md) 보다 효율적인 allocator 및 비 할당자 개체를 구현 하는 함수입니다. 그러나 C + + 11은 전역 범위에서 할당 해제 함수의 이와 동등한 집합이 정의 되지 않았습니다. C + + 11, 글로벌 할당 해제가 있는 함수에 두 번째 형식 매개 변수가 `size_t` placement delete 함수 것으로 간주 됩니다. 이러한 함수는 크기 인수를 전달 하 여 명시적으로 호출 해야 합니다.  
  
표준 C + + 14 컴파일러의 동작을 변경합니다. 정의 하는 경우 전역 `operator delete` 및 `operator delete[]` 형식의 두 번째 매개 변수를 사용 하는 `size_t`, 멤버 범위 버전이 호출 되지 하 고 개체의 크기는 사용할 수 있는 이러한 함수를 호출 하는 컴파일러에서 선호 합니다. 컴파일러는 암시적으로 크기 인수를 전달합니다. 단일 인수 버전은 컴파일러에서 할당 취소 되 고 개체의 크기를 확인할 수 없을 때 호출 됩니다. 그렇지 않으면 호출 하는 할당 해제 함수의 버전을 선택 하기 위한 일반적인 규칙이 계속 적용 합니다. 전역 함수에 대 한 호출 범위 확인 연산자 앞에 추가 하 여 명시적으로 지정할 수 있습니다 (`::`)를 할당 해제 함수 호출 합니다.  
  
기본적으로 Visual Studio 2015부터 Visual c + +가 C + + 14 표준 동작을 구현 합니다. 이 설정 하 여에 명시적으로 지정할 수 있습니다는 `/Zc:sizedDealloc` 컴파일러 옵션입니다. 이 잠재적으로 중요 나타냅니다 변경 합니다. 사용 하 여는 `/Zc:sizedDealloc-` 코드 형식의 두 번째 매개 변수를 사용 하는 배치 delete 연산자를 정의 하는 경우 이전 동작이 유지 옵션 `size_t`합니다. 형식의 두 번째 매개 변수가 있는 전역 할당 해제 함수의 기본 Visual Studio 라이브러리 구현 `size_t` 단일 매개 변수 버전을 호출 합니다. 코드만 단일-매개 변수를 제공 전역 delete 연산자 및 operator delete, 전역 함수를 호출 하는 전역 크기 지정 된 할당 해제 함수의 기본 라이브러리 구현입니다.  
  
Visual C++의 규칙과 관련된 문제에 대한 자세한 내용은 [Nonstandard Behavior](../../cpp/nonstandard-behavior.md)을 참조하세요.  
  
## <a name="to-set-this-compiler-option-in-the-visual-studio-development-environment"></a>Visual Studio 개발 환경에서 이 컴파일러 옵션을 설정하려면  
1.  프로젝트의 **속성 페이지** 대화 상자를 엽니다. 자세한 내용은 참조 [프로젝트 속성 작업](../../ide/working-with-project-properties.md)합니다.  
2.  **구성을** 드롭다운 메뉴에서 선택 **모든 구성**합니다.  
3.  선택 된 **구성 속성**, **C/c + +**, **명령줄** 속성 페이지.  
4.  수정 된 **추가 옵션** 포함할 속성을 `/Zc:sizedDealloc` 또는 `/Zc:sizedDealloc-` 선택한 후 **확인**합니다.  
  
## <a name="see-also"></a>참고 항목  
[컴파일러 옵션](../../build/reference/compiler-options.md)  
[컴파일러 옵션 설정](../../build/reference/setting-compiler-options.md)  
[/Zc (규칙)](../../build/reference/zc-conformance.md)  
