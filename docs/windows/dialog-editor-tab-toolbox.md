---
title: "대화 상자 편집기 탭, 도구 상자 | Microsoft Docs"
ms.custom: 
ms.date: 11/04/2016
ms.reviewer: 
ms.suite: 
ms.technology: cpp-windows
ms.tgt_pltfrm: 
ms.topic: article
dev_langs: C++
helpviewer_keywords:
- Toolbox [C++], Dialog Editor tab
- controls [C++], types
- syslink controls ino dialog boxes
- custom controls [Visual Studio], dialog boxes
- controls [C++], standard
- Dialog editor, creating controls
- controls [C++], adding to dialog boxes
ms.assetid: 253885c2-dcb9-4d8e-ac9b-805ea31cbf5e
caps.latest.revision: "12"
author: mikeblome
ms.author: mblome
manager: ghogen
ms.workload:
- cplusplus
- uwp
ms.openlocfilehash: 9db31d6e152be10f2c4934b7b1f239d1e08387f5
ms.sourcegitcommit: 8fa8fdf0fbb4f57950f1e8f4f9b81b4d39ec7d7a
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 12/21/2017
---
# <a name="dialog-editor-tab-toolbox"></a>도구 상자, 대화 상자 편집기 탭
대화 상자 편집기 탭이 표시는 [도구 상자 창](/visualstudio/ide/reference/toolbox) 대화 상자 편집기에서 작업 하는 경우. 새 대화 상자에 컨트롤을 추가 하려면 컨트롤 도구 상자에서 만들려는 대화 상자로 끌어 (자세한 내용은 참조 [대화 상자에 컨트롤 추가](adding-a-control-to-a-dialog-box.md)). 그런 다음 컨트롤을 주변으로 이동하거나 크기와 모양을 변경할 수 있습니다.  
  
 도구 상자에서 사용할 수 있는 표준 컨트롤은 다음과 같습니다.  
  
-   [Button 컨트롤](../mfc/reference/cbutton-class.md)  
  
-   [확인란 컨트롤](../mfc/reference/styles-used-by-mfc.md#button-styles)  
  
-   [콤보 상자 컨트롤](../mfc/reference/ccombobox-class.md)  
  
-   [편집 컨트롤](../mfc/reference/cedit-class.md)  
  
-   그룹 상자  
  
-   [목록 상자 컨트롤](../mfc/reference/clistbox-class.md)  
  
-   [라디오 단추 컨트롤](../mfc/reference/styles-used-by-mfc.md#button-styles)  
  
-   [정적 텍스트 컨트롤](../mfc/reference/cstatic-class.md)  
  
-   [그림 컨트롤](../mfc/reference/cpictureholder-class.md)  
  
-   [Rich Edit 2.0 컨트롤](../mfc/using-cricheditctrl.md)  
  
-   [스크롤 막대 컨트롤](../mfc/reference/cscrollbar-class.md)  
  
 [Windows 공용 컨트롤](../mfc/controls-mfc.md) 도구 상자에서 사용할 수 있는 응용 프로그램에 더 많은 기능을 제공 합니다. 다음과 같은 변경 내용이 해당됩니다.  
  
-   [슬라이더 컨트롤](../mfc/slider-control-styles.md)  
  
-   [Spin 컨트롤](../mfc/using-cspinbuttonctrl.md)  
  
-   [진행률 컨트롤](../mfc/styles-for-the-progress-control.md)  
  
-   [Hot Key 컨트롤](../mfc/using-a-hot-key-control.md)  
  
-   [목록 컨트롤](../mfc/list-control-and-list-view.md)  
  
-   [트리 컨트롤](../mfc/tree-control-styles.md)  
  
-   [탭 컨트롤](../mfc/tab-controls-and-property-sheets.md)  
  
-   [애니메이션 컨트롤](../mfc/using-an-animation-control.md)  
  
-   [날짜 시간 선택 컨트롤](../mfc/creating-the-date-and-time-picker-control.md)  
  
-   [Monthcalendar 컨트롤](../mfc/month-calendar-control-examples.md)  
  
-   [IP 주소 컨트롤](../mfc/reference/cipaddressctrl-class.md)  
  
-   [확장 된 콤보 상자 컨트롤](../mfc/creating-an-extended-combo-box-control.md)  
  
-   [사용자 지정 컨트롤](custom-controls-in-the-dialog-editor.md)  
  
 선택 하 여 대화 상자에 사용자 지정 컨트롤을 추가할 수 있습니다는 **사용자 지정 컨트롤** 도구 상자에 끌어서 놓아 대화 상자에서 아이콘입니다. Syslink 컨트롤을 추가 하려면 사용자 지정 컨트롤을 추가한 후 컨트롤의 변경 **클래스** 속성을 **Syslink**합니다. 이렇게 하면 속성이 새로 고쳐지고 Syslink 컨트롤 속성이 표시됩니다. MFC 래퍼 클래스에 대 한 자세한 내용은 참조 [CLinkCtrl](../mfc/reference/clinkctrl-class.md)합니다.  
  
 수도 있습니다 [대화 상자에 ActiveX 컨트롤 추가](../windows/viewing-and-adding-activex-controls-to-a-dialog-box.md)합니다.  
  
 더욱 쉽게 사용하기 위해 도구 상자 창을 사용자 지정할 수도 있습니다. 자세한 내용은 [도구 상자 사용](/visualstudio/ide/using-the-toolbox)을 참조하세요.  

 MFC에 RichEdit 1.0 컨트롤 사용에 대 한 자세한 내용은 참조 하세요. [MFC에 RichEdit 1.0 컨트롤 사용](../windows/using-the-richedit-1-0-control-with-mfc.md)  
  
 관리 되는 프로젝트에 리소스를 추가 정보를 참조 하십시오 [데스크톱 응용 프로그램의 리소스](/dotnet/framework/resources/index) 에 *.NET Framework 개발자 가이드입니다.* 수동으로 관리 되는 프로젝트에 리소스 파일을 추가, 리소스 액세스, 정적 리소스 표시 및 속성에 리소스 문자열 할당에 대 한 정보를 참조 하십시오. [데스크톱 앱에 대 한 리소스 파일 만들기](/dotnet/framework/resources/creating-resource-files-for-desktop-apps)합니다. 전역화 및 지역화의 관리 되는 응용 프로그램의 리소스에 대 한 정보를 참조 하십시오. [전역화 및 지역화.NET Framework 응용 프로그램](/dotnet/standard/globalization-localization/index)합니다.  
  
## <a name="requirements"></a>요구 사항  
 Win32  
  
## <a name="see-also"></a>참고 항목  
 [컨트롤](../mfc/controls-mfc.md)   
 [컨트롤 클래스](../mfc/control-classes.md)   
 [대화 상자 클래스](../mfc/dialog-box-classes.md)   
 [스크롤 막대 스타일](../mfc/reference/styles-used-by-mfc.md#scroll-bar-styles)   
 [Rich Edit 컨트롤 예](../mfc/rich-edit-control-examples.md)   
 [대화 상자 컨트롤에 대 한 이벤트 처리기를 추가합니다.](../windows/adding-event-handlers-for-dialog-box-controls.md)   
 [대화 상자 컨트롤 및 변수 형식](../ide/dialog-box-controls-and-variable-types.md)

