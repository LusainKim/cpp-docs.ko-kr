---
title: "-Og (전역 최적화) | Microsoft Docs"
ms.custom: 
ms.date: 09/22/2017
ms.reviewer: 
ms.suite: 
ms.technology: cpp-tools
ms.tgt_pltfrm: 
ms.topic: article
f1_keywords:
- VC.Project.VCCLCompilerTool.GlobalOptimizations
- /og
dev_langs: C++
helpviewer_keywords:
- -Og compiler option [C++]
- global optimizations compiler option [C++]
- automatic register allocation
- /Og compiler option [C++]
- loop structures, optimizing
- common subexpression elimination
- Og compiler option [C++]
ms.assetid: d10630cc-b9cf-4e97-bde3-8d7ee79e9435
caps.latest.revision: "17"
author: corob-msft
ms.author: corob
manager: ghogen
ms.workload: cplusplus
ms.openlocfilehash: 196e89a958ce49bf5e0087d98d2f40ada210cc87
ms.sourcegitcommit: 8fa8fdf0fbb4f57950f1e8f4f9b81b4d39ec7d7a
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 12/21/2017
---
# <a name="og-global-optimizations"></a>/Og(전역 최적화)

더 이상 사용되지 않습니다. 로컬 및 전역 최적화를 제공 자동 레지스터 할당 및 루프 최적화 합니다. 하나를 사용 하는 것이 좋습니다 [/O1 (크기 최소화)](../../build/reference/o1-o2-minimize-size-maximize-speed.md) 또는 [/O2 (속도 최대화)](../../build/reference/o1-o2-minimize-size-maximize-speed.md) 대신 합니다.

## <a name="syntax"></a>구문

> /Og

## <a name="remarks"></a>설명

**/Og** 는 사용 되지 않습니다. 이제 이러한 최적화는 기본적으로 일반적으로 사용 됩니다. 최적화에 대 한 자세한 내용은 참조 하십시오. [/O1, /O2 (크기 최소화, 속도 최대화)](../../build/reference/o1-o2-minimize-size-maximize-speed.md) 또는 [/Ox (활성화 가장 속도 최적화)](../../build/reference/ox-full-optimization.md)합니다.

사용 가능한 최적화는 **/Og**:

- 로컬 및 전역 공통 하위 식 제거

     이러한 최적화는 공통 하위 식의 값 한 번 계산 됩니다. 다음 예에서 경우의 값 `b` 및 `c` 세 식 사이 변경 되지 않으면, 컴파일러에 대 한 계산을 할당할 수 `b + c` 임시 변수에 대 한 변수를 대체 `b + c`:

    ```C
    a = b + c;
    d = b + c;
    e = b + c;
    ```

     로컬 공통 하위 식 최적화 컴파일러 공통 하위 식에 대 한 코드의 짧은 섹션을 검사합니다. 전역 공통 하위 식 최적화 컴파일러는 공통 하위 식에 대 한 전체 함수를 검색 합니다.

- 자동 레지스터 할당

     이 최적화 레지스터;에 저장소 자주 사용 되는 변수 및 하위 식에 컴파일러가 수 있습니다. `register` 키워드는 무시 됩니다.

- 루프 최적화

     이 최적화는 루프의 본문에서 고정 부분식을 제거합니다. 최적 루프에 루프의 각 실행을 통해 해당 값을 변경 하는 식만 포함 합니다. 다음 예제에서는 식에서에서 `x + y` 루프 본문에서 변경 되지 않습니다.

    ```C
    i = -100;
    while( i < 0 ) {
        i += x + y;
    }
    ```

     최적화 후 `x + y` 루프가 실행 될 때마다 하는 대신에 한 번 계산 됩니다.

    ```C
    i = -100;
    t = x + y;
    while( i < 0 ) {
        i += t;
    }
    ```

     컴파일러가 수 없는 경우, 사용 설정 루프 최적화는 훨씬 더 효율적 [__restrict](../../cpp/extension-restrict.md), [noalias](../../cpp/noalias.md), 또는 [제한](../../cpp/restrict.md)합니다.

    > [!NOTE]
    > 사용 하 여 함수에서 함수 별로 전역 최적화를 사용 하지 않도록 설정 하거나 설정할 수 있습니다는 `optimize` 와 함께 pragma는 `g` 옵션입니다.

 관련된 정보를 참조 하십시오. [/Oi (내장 함수 생성)](../../build/reference/oi-generate-intrinsic-functions.md) 및 [/Ox (활성화 가장 속도 최적화)](../../build/reference/ox-full-optimization.md)합니다.

### <a name="to-set-this-compiler-option-in-the-visual-studio-development-environment"></a>Visual Studio 개발 환경에서 이 컴파일러 옵션을 설정하려면

1. 프로젝트의 **속성 페이지** 대화 상자를 엽니다. 자세한 내용은 참조 [프로젝트 속성 작업](../../ide/working-with-project-properties.md)합니다.

1. **C/C++** 폴더를 클릭합니다.

1. **명령줄** 속성 페이지를 클릭합니다.

1. 입력에 컴파일러 옵션은 **추가 옵션** 상자입니다.

### <a name="to-set-this-compiler-option-programmatically"></a>프로그래밍 방식으로 이 컴파일러 옵션을 설정하려면

- <xref:Microsoft.VisualStudio.VCProjectEngine.VCCLCompilerTool.AdditionalOptions%2A>을 참조하세요.

## <a name="see-also"></a>참고 항목

[/O 옵션 (코드 최적화)](../../build/reference/o-options-optimize-code.md)

[컴파일러 옵션](../../build/reference/compiler-options.md)

[컴파일러 옵션 설정](../../build/reference/setting-compiler-options.md)