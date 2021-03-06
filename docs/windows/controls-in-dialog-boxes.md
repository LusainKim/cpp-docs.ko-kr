---
title: "대화 상자의 컨트롤 | Microsoft Docs"
ms.custom: 
ms.date: 11/04/2016
ms.reviewer: 
ms.suite: 
ms.technology: cpp-windows
ms.tgt_pltfrm: 
ms.topic: article
dev_langs: C++
helpviewer_keywords:
- controls [C++], dialog boxes
- dialog box controls, about dialog box controls
- dialog box controls
ms.assetid: e216c4f9-2fd4-429d-889a-8ebce7bad177
caps.latest.revision: "9"
author: mikeblome
ms.author: mblome
manager: ghogen
ms.workload:
- cplusplus
- uwp
ms.openlocfilehash: 02ca3523de9341c14d2e2a9837ba84f5625a3379
ms.sourcegitcommit: 8fa8fdf0fbb4f57950f1e8f4f9b81b4d39ec7d7a
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 12/21/2017
---
# <a name="controls-in-dialog-boxes"></a>대화 상자의 컨트롤
사용 하 여 대화 상자에 컨트롤을 추가할 수 있습니다는 [대화 상자 편집기 탭](../windows/dialog-editor-tab-toolbox.md) 에 [도구 상자 창](/visualstudio/ide/reference/toolbox), 대화 상자도 끌어와 원하는 컨트롤을 선택할 수 있습니다. 기본적으로 도구 상자 창 자동 숨기기로 설정 됩니다. 대화 상자 편집기 열릴 때 솔루션의 왼쪽된 여백에 탭으로 나타납니다. 그러나 클릭 하 여 위치를 도구 상자 창을 고정할 수는는 **자동 숨기기** 창의 상단 오른쪽 모서리에 있는 단추입니다. 이 창의 동작을 제어 하는 방법에 대 한 자세한 내용은 참조 하십시오. [창 관리](/visualstudio/ide/customizing-window-layouts-in-visual-studio)합니다.  
  
 대화 상자에 컨트롤을 추가, 기존 컨트롤의 위치를 변경 또는 다른 한 대화 상자에서 컨트롤을 이동 하는 가장 빠른 방법은-drop 메서드를 사용 하는 것입니다. 대화 상자에 놓을 때까지 점선 컨트롤의 위치가 같습니다. 끌어서 놓기 방법을 대화 상자에 컨트롤을 추가 하면 컨트롤의 형식에 맞는 표준 높이 컨트롤에 제공 됩니다.  
  
 대화 상자에 컨트롤을 추가 하거나 위치를 변경할 때의 최종 위치 확인할 수 있습니다 가이드 또는 여백, 아니면 레이아웃 모눈이 있습니다.  
  
 대화 상자에 컨트롤을 추가한 후에 캡션 등의 속성을 변경할 수 있습니다는 [속성 창](/visualstudio/ide/reference/properties-window)합니다. 여러 컨트롤을 선택할 수 있으며 해당 속성을 한 번에 변경할 수 없습니다.  
  
-   [컨트롤 추가, 편집 및 삭제](adding-editing-or-deleting-controls.md)  
  
-   [컨트롤 선택](../windows/selecting-controls.md)  
  
-   [각 컨트롤 크기 조정](../windows/sizing-individual-controls.md)  
  
-   [컨트롤의 너비, 높이, 크기를 동일하게 만들기](../windows/making-controls-the-same-width-height-or-size.md)  
  
-   [콤보 상자 및 드롭다운 목록의 크기 설정](setting-the-size-of-the-combo-box-and-its-drop-down-list.md)  
  
-   [콤보 상자 컨트롤에 값 추가](../windows/adding-values-to-a-combo-box-control.md)  
  
-   [가로 스크롤 막대 너비 설정](../windows/setting-the-width-of-a-horizontal-scroll-bar.md)  
  
-   [대화 상자에 컨트롤 배치](../windows/arrangement-of-controls-on-dialog-boxes.md)  
  
-   [대화 상자 편집기의 사용자 지정 컨트롤](custom-controls-in-the-dialog-editor.md)  
  
-   [니모닉(선택키) 정의](../windows/defining-mnemonics-access-keys.md)  
  
-   [대화 상자의 위치와 크기 지정](../windows/specifying-the-location-and-size-of-a-dialog-box.md)  
  
 관리 되는 프로젝트에 리소스를 추가 정보를 참조 하십시오 [데스크톱 응용 프로그램의 리소스](/dotnet/framework/resources/index) 에 *.NET Framework 개발자 가이드입니다.* 수동으로 관리 되는 프로젝트에 리소스 파일을 추가, 리소스 액세스, 정적 리소스 표시 및 속성에 리소스 문자열 할당에 대 한 정보를 참조 하십시오. [데스크톱 앱에 대 한 리소스 파일 만들기](/dotnet/framework/resources/creating-resource-files-for-desktop-apps)합니다. 전역화 및 지역화의 관리 되는 응용 프로그램의 리소스에 대 한 정보를 참조 하십시오. [전역화 및 지역화.NET Framework 응용 프로그램](/dotnet/standard/globalization-localization/index)합니다.  
  
## <a name="requirements"></a>요구 사항  
 Win32  
  
## <a name="see-also"></a>참고 항목  
 [대화 상자 컨트롤에 대 한 이벤트 처리기를 추가합니다.](../windows/adding-event-handlers-for-dialog-box-controls.md)   
 [대화 상자 컨트롤 및 변수 형식](../ide/dialog-box-controls-and-variable-types.md)   
 [대화 상자 편집기](../windows/dialog-editor.md)

