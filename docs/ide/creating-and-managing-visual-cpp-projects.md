---
title: "Visual c + + 프로젝트 만들기 및 관리 | Microsoft Docs"
ms.custom: 
ms.date: 11/04/2016
ms.reviewer: 
ms.suite: 
ms.technology: cpp-ide
ms.tgt_pltfrm: 
ms.topic: article
f1_keywords:
- vcprojects
- creatingmanagingVC
dev_langs: C++
helpviewer_keywords:
- ATL projects, creating
- Visual C++ projects, creating
- projects [C++], creating
- Visual C++ projects
- ATL projects
ms.assetid: 11003cd8-9046-4630-a189-a32bf3b88047
caps.latest.revision: "28"
author: mikeblome
ms.author: mblome
manager: ghogen
ms.workload: cplusplus
ms.openlocfilehash: 0c38f4c75a41de8b2f2b494941c6a52b1ff46fa4
ms.sourcegitcommit: 8fa8fdf0fbb4f57950f1e8f4f9b81b4d39ec7d7a
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 12/21/2017
---
# <a name="creating-and-managing-msbuild-based-visual-c-projects"></a>MSBuild 기반 Visual c + + 프로젝트 만들기 및 관리
MSBuild는 Visual c + +에 대 한 네이티브 빌드 시스템 및는 일반적으로 MFC 또는 ATL 라이브러리를 사용 하는 데스크톱 응용 프로그램 뿐만 아니라 UWP 앱에 대 한 사용 하는 시스템을 작성 하는 가장 적합 합니다. MSBuild는 Visual Studio IDE 및 프로젝트 시스템와 통합 긴밀 하 게 하지만 명령줄에서 사용할 수도 있습니다. Visual c + +에서는 Visual Studio 2017 년부터 [CMake 및 기타 MSBuild가 아닌 시스템 폴더 열기 기능을 통해](non-msbuild-projects.md)합니다.

MSBuild 기반 프로젝트에 프로젝트 파일을 개발 하 고 예제 (x 86, x64 또는 ARM) 대상 플랫폼에 대 한 다른 구성 설정 뿐만 아니라 해당 프로그램을 컴파일하는 데 필요한 모든 파일 및 리소스 지정 하는 XML 형식의 (.vcxproj)는 버전 또는 디버그 버전의 프로그램을 해제 합니다. 한 프로젝트(또는 여러 프로젝트)가 *솔루션*에 포함됩니다. 예를 들어 솔루션에는 몇 개의 Win32 DLL 프로젝트 및 이러한 DLL을 사용하는 단일 Win32 콘솔 응용 프로그램이 포함될 수 있습니다. 프로젝트를 빌드하면 MSBuild 엔진에서 프로젝트 파일을 사용하고 실행 파일 및/또는 다른 모든 사용자 지정 출력을 생성합니다.

선택 하 여 Visual c + + 프로젝트를 만들 수 **파일 &#124; 새로 만들기 &#124; 프로젝트**, 왼쪽된 창에서 Visual c + +가 선택 되어 있는지 확인 한 다음 가운데 창의 프로젝트 템플릿 목록에서 선택 합니다. 서식 파일을 클릭할 때 대부분의 경우에는 마법사가 나타납니다 하는 프로젝트를 만들기 전에 다양 한 프로젝트 속성을 설정할 수 있습니다. 보고 하 고 프로젝트의 속성 페이지를 사용 하 여 해당 속성을 나중에 수정할 수 있습니다 (**프로젝트 &#124; 속성**).  
  
 새 프로젝트를 만들 수도 있습니다.  
  
-   선택 **파일 &#124; 새로 만들기 &#124; 기존 코드의 프로젝트** 기존 소스 코드 파일을 추가 하 고 지시 합니다. 이 옵션은 예를 들어 소스 코드 파일이 25개 이하이고 복잡한 종속성이 적거나 아예 없는 상대적으로 작고 간단한 프로젝트에서 가장 잘 작동합니다.  
  
-   메이크파일을 사용하여 시작하고 일반 탭에서 메이크파일 프로젝트 템플릿을 선택합니다.  
  
-   빈 프로젝트 만들기 (아래에서 **일반** 탭) 솔루션 탐색기에서 프로젝트 노드를 마우스 오른쪽 단추로 클릭 하 고 선택 하 여 소스 코드 파일을 수동으로 추가 하 고 **추가 &#124; 기존 항목**합니다.  
  
-   using the [Win32 Application Wizard](../windows/win32-application-wizard.md)를 사용합니다.  
  
## <a name="in-this-section"></a>섹션 내용  
 [Visual C++ 프로젝트 형식](../ide/visual-cpp-project-types.md)  
 Visual c + +에서 사용할 수 있는 MSBuild 기반 프로젝트 형식을 설명 합니다.  
  
 [Visual C++ 프로젝트용 파일 형식](../ide/file-types-created-for-visual-cpp-projects.md)  
 다양 한 MSBuild 프로젝트 형식에 사용 되는 파일의 종류를 설명 합니다.  
  
 [응용 프로그램 마법사를 사용하여 데스크톱 프로젝트 만들기](../ide/creating-desktop-projects-by-using-application-wizards.md)  
 마법사를 사용하여 Visual C++로 프로젝트를 만드는 방법을 설명합니다.  
  
 [프로젝트 속성 사용](../ide/working-with-project-properties.md)  
 속성 페이지 및 속성 시트를 사용하여 프로젝트 설정을 지정하는 방법을 설명합니다.  
  
 [코드 마법사로 기능 추가](../ide/adding-functionality-with-code-wizards-cpp.md)  
 프로젝트에 기능을 추가하기 위해 클래스, 메서드, 변수 및 기타 요소를 추가하는 방법을 설명합니다.  
  
 [방법: 빌드할 프로젝트 출력 파일 구성](../ide/how-to-organize-project-output-files-for-builds.md)  
 프로젝트 출력 파일을 구성하는 방법을 설명합니다.  
  
## <a name="related-sections"></a>관련 단원  
 [C/C++ 프로그램 빌드](../build/building-c-cpp-programs.md)  
 명령줄 또는 Visual Studio의 통합 개발 환경에서 프로그램 빌드를 설명하는 항목에 대한 링크를 제공합니다.  
  
 [Visual C++ 참조](http://msdn.microsoft.com/en-us/1ba03b5c-8229-4f63-b08c-6c12141d6ab1)  
 C 및 C++ 언어 참조, Visual C++에서 제공하는 라이브러리, Visual C++ 확장성 개체 모델 및 MASM(Microsoft Macro Assembler)을 설명하는 항목에 대한 링크를 제공합니다.  
  
## <a name="see-also"></a>참고 항목  
 [Visual Studio SDK](http://msdn.microsoft.com/vstudio/extend)
