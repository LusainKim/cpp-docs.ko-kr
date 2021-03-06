---
title: "CWinApp: 응용 프로그램 클래스 | Microsoft Docs"
ms.custom: 
ms.date: 11/04/2016
ms.reviewer: 
ms.suite: 
ms.technology: cpp-windows
ms.tgt_pltfrm: 
ms.topic: article
f1_keywords: CWinApp
dev_langs: C++
helpviewer_keywords:
- application class [MFC]
- CWinApp class [MFC], CWinThread
- MFC, WinMain and
- CWinApp class [MFC], multithreading
- CWinThread class [MFC], and CWinApp
- InitApplication method [MFC]
- WinMain method [MFC]
- WinMain method [MFC], in MFC
- CWinApp class [MFC], WinMain
ms.assetid: 935822bb-d463-481b-a5f6-9719d68ed1d5
caps.latest.revision: "13"
author: mikeblome
ms.author: mblome
manager: ghogen
ms.workload: cplusplus
ms.openlocfilehash: c1f146df2dd4f97affdaf1c3107d1b00bfd86876
ms.sourcegitcommit: 8fa8fdf0fbb4f57950f1e8f4f9b81b4d39ec7d7a
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 12/21/2017
---
# <a name="cwinapp-the-application-class"></a>CWinApp: 응용 프로그램 클래스
MFC의 기본 응용 프로그램 클래스 초기화, 실행 중, 및 Windows 운영 체제에 대 한 응용 프로그램의 종료를 캡슐화합니다. 프레임 워크에서 빌드된 응용 프로그램을 하나 있어야 하며에서 파생 된 클래스의 개체를 하나만 [CWinApp](../mfc/reference/cwinapp-class.md)합니다. 이 개체는 창을 만들기 전에 만들어집니다.  
  
 `CWinApp`파생 된 `CWinThread`, 하나 이상의 스레드를 가질 수 있는 사용자 응용 프로그램에 대 한 실행의 주 스레드에 나타냅니다. MFC의 최신 버전에는 `InitInstance`, **실행**, `ExitInstance`, 및 `OnIdle` 멤버 함수는 클래스에서 실제로 `CWinThread`합니다. 이러한 함수 여기에 설명 되어 큐브인 것 처럼 `CWinApp` 멤버 대신 초점은 주 스레드가 아닌 응용 프로그램 개체와 개체의 역할 때문에 있습니다.  
  
> [!NOTE]
>  응용 프로그램 클래스는 응용 프로그램의 주 스레드 실행을 구성합니다. Win32 API 함수를 사용 하 여 보조 실행 스레드를 만들 수도 있습니다. 이러한 스레드는 MFC 라이브러리를 사용할 수 있습니다. 자세한 내용은 참조 [다중 스레딩](../parallel/multithreading-support-for-older-code-visual-cpp.md)합니다.  
  
 Windows 운영 체제에 대 한 다른 프로그램과 마찬가지로 응용 프로그램 프레임 워크에는 `WinMain` 함수입니다. 그러나 프레임 워크 응용 프로그램에서 작성 하지 않으면 `WinMain`합니다. 클래스 라이브러리에서 제공 하 고 응용 프로그램이 시작 될 때 호출 됩니다. `WinMain`창 클래스 등록 등의 표준 서비스를 수행 합니다. 멤버 함수는 응용 프로그램 개체를 초기화 하 고 응용 프로그램을 실행의 다음 호출 합니다. (사용자 지정할 수 있습니다 `WinMain` 재정의 하 여는 `CWinApp` 멤버 함수를 `WinMain` 호출 합니다.)  
  
 응용 프로그램을 초기화 하려면 `WinMain` 호출 응용 프로그램 개체 `InitApplication` 및 `InitInstance` 멤버 함수입니다. 응용 프로그램의 메시지 루프를 실행 하려면 `WinMain` 호출은 **실행** 멤버 함수입니다. 종료 `WinMain` application 개체의 호출 `ExitInstance` 멤버 함수입니다.  
  
> [!NOTE]
>  에 나와 있는 이름은 **굵게** 이 설명서에서는 Microsoft Foundation Class 라이브러리 및 Visual c + +에서 제공 하는 요소를 나타냅니다. 에 나와 있는 이름은 `monospaced` 형식을 만들거나 재정의 된 요소를 나타냅니다.  
  
## <a name="see-also"></a>참고 항목  
 [일반 MFC 항목](../mfc/general-mfc-topics.md)   
 [CWinApp 및 MFC 응용 프로그램 마법사](../mfc/cwinapp-and-the-mfc-application-wizard.md)   
 [재정의 가능 CWinApp 멤버 함수](../mfc/overridable-cwinapp-member-functions.md)   
 [특수 CWinApp 서비스](../mfc/special-cwinapp-services.md)

