---
title: "연습: 빌드 프로젝트 (c + +) | Microsoft Docs"
ms.custom: 
ms.date: 11/04/2016
ms.reviewer: 
ms.suite: 
ms.technology: cpp-ide
ms.tgt_pltfrm: 
ms.topic: article
dev_langs: C++
helpviewer_keywords:
- building projects [C++]
- projects [C++], building
- project building [C++]
ms.assetid: d459bc03-88ef-48d0-9f9a-82d17f0b6a4d
caps.latest.revision: "14"
author: corob-msft
ms.author: corob
manager: ghogen
ms.workload: cplusplus
ms.openlocfilehash: 65d7a4bf7e4b3fd519911a2a127ec0ac2723b630
ms.sourcegitcommit: 8fa8fdf0fbb4f57950f1e8f4f9b81b4d39ec7d7a
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 12/21/2017
---
# <a name="walkthrough-building-a-project-c"></a>연습: 프로젝트 빌드(C++)
이 연습에서는 코드에 일부러 Visual C++ 구문 오류를 포함한 다음 어떠한 컴파일 오류가 발생하는지 확인하고 이를 수정하는 방법에 대해 살펴봅니다. 프로젝트를 컴파일하면 어디에 어떠한 문제가 있는지 표시하는 오류 메시지가 나타납니다.  
  
## <a name="prerequisites"></a>필수 구성 요소  
  
-   이 연습에서는 사용자가 C++ 언어의 기본적인 사항을 알고 있는 것으로 가정합니다.  
  
-   또한 이전 관련된 연습에 나와 있는 완료 한 것으로 가정 [c + + 데스크톱 개발을 위한 Visual Studio IDE를 사용 하 여](../ide/using-the-visual-studio-ide-for-cpp-desktop-development.md)합니다.  
  
### <a name="to-fix-compilation-errors"></a>컴파일 오류를 수정하려면  
  
1.  TestGames.cpp에서 마지막 줄의 세미콜론을 삭제하여 다음과 같이 만듭니다.  
  
     `return 0`  
  
2.  메뉴 모음에서 **빌드**, **솔루션 빌드**를 선택합니다.  
  
3.  메시지는 **오류 목록** 창 프로젝트 빌드에 오류가 발생 했음을 나타냅니다. 설명을 다음과 같이 나타납니다.  
  
     `error C2143: syntax error : missing ';' before '}'`  
  
     이 오류에 대 한 도움말 정보를 보려면 강조 표시에 **오류 목록** 창 F1 키를 선택 합니다.  
  
4.  구문 오류가 발생한 줄의 끝에 세미콜론을 다시 추가합니다.  
  
     `return 0;`  
  
5.  메뉴 모음에서 **빌드**, **솔루션 빌드**를 선택합니다.  
  
     메시지는 **출력** 창은 프로젝트 성공적으로 컴파일 되었음을 나타냅니다.  
  
    ```Output  
    1>------ Build started: Project: Game, Configuration: Debug Win32 ------  
    1>  TestGames.cpp  
    1>  Game.vcxproj -> C:\Users\<username>\Documents\Visual Studio <version>\Projects\Game\Debug\Game.exe  
    ========== Build: 1 succeeded, 0 failed, 0 up-to-date, 0 skipped ==========  
    ```  
  
## <a name="next-steps"></a>다음 단계  
 **이전:** [연습: 프로젝트 및 솔루션 (c + +) 작업](../ide/walkthrough-working-with-projects-and-solutions-cpp.md) &#124; **다음:**[연습: 테스트 프로젝트 (c + +)](../ide/walkthrough-testing-a-project-cpp.md)  
  
## <a name="see-also"></a>참고 항목  
 [C + + 언어 참조](../cpp/cpp-language-reference.md)   
 [C/C++ 프로그램 빌드](../build/building-c-cpp-programs.md)