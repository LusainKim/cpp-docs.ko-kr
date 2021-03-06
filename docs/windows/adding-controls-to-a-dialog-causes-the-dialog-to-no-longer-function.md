---
title: "대화 상자에 컨트롤 추가 대화 상자에 상자가 더 이상 작동 | Microsoft Docs"
ms.custom: 
ms.date: 11/04/2016
ms.reviewer: 
ms.suite: 
ms.technology: cpp-windows
ms.tgt_pltfrm: 
ms.topic: article
dev_langs: C++
helpviewer_keywords:
- controls [C++], troubleshooting
- common controls, troubleshooting
- troubleshooting controls
- dialog boxes, troubleshooting
- dialog box controls, troubleshooting
- InitCommonControls
ms.assetid: b2dd4574-ea59-4343-8d65-b387cead5da6
caps.latest.revision: "10"
author: mikeblome
ms.author: mblome
manager: ghogen
ms.workload:
- cplusplus
- uwp
ms.openlocfilehash: d0ec4825419c7a9d3c9bc35151b84c327a03325b
ms.sourcegitcommit: 8fa8fdf0fbb4f57950f1e8f4f9b81b4d39ec7d7a
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 12/21/2017
---
# <a name="adding-controls-to-a-dialog-causes-the-dialog-to-no-longer-function"></a>대화 상자에 컨트롤을 추가하여 대화 상자가 작동하지 않는 경우
공용 컨트롤 또는 서식 있는 편집 컨트롤을 대화 상자를 추가한 후 대화 상자를 테스트 하거나 자체 대화 상자가 나타나지는 표시 됩니다.  
  
 **문제의 예**  
  
1.  Windows 응용 프로그램 (콘솔 앱)을 만드는 응용 프로그램 설정을 수정 Win32 프로젝트를 만듭니다.  
  
2.  [리소스 뷰](../windows/resource-view-window.md),.rc 파일을 두 번 클릭 합니다.  
  
3.  대화 상자 옵션에서 두 번 클릭은 **에 대 한** 상자입니다.  
  
4.  추가 **IP 주소 컨트롤** 대화 상자.  
  
5.  저장 및 **모두 다시 빌드**합니다.  
  
6.  프로그램을 실행 합니다.  
  
7.  대화 상자에서 **도움말** 메뉴를 클릭 하 여는 **에 대 한** 명령; 없음 대화 상자가 표시 됩니다.  
  
 **원인**  
  
 현재 대화 상자 편집기가 자동으로 추가 되지 코드 프로젝트 또는 rich edit 컨트롤 대화 상자에 끌어서 다음과 같은 공용 컨트롤을 놓을 때. 또는 Visual Studio 오류 또는 경고가 발생 하면 제공이 문제가 발생 합니다. 컨트롤에 대 한 코드를 수동으로 추가 해야 합니다.  
  
||||  
|-|-|-|  
|슬라이더 컨트롤|트리 컨트롤|날짜 시간 선택|  
|Spin 컨트롤|탭 컨트롤|월 달력|  
|진행률 컨트롤|애니메이션 컨트롤|IP 주소 컨트롤|  
|바로 가기 키|Rich Edit 컨트롤|확장 된 콤보 상자|  
|목록 컨트롤|Rich Edit 2.0 컨트롤|사용자 지정 컨트롤|  
  
## <a name="the-fix-for-common-controls"></a>공용 컨트롤에 대 한 수정 프로그램  
 호출 해야 대화 상자에서 공용 컨트롤을 사용 하려면 [InitCommonControlsEx](http://msdn.microsoft.com/library/windows/desktop/bb775697) 또는 **AFXInitCommonControls** 대화 상자를 만들기 전에 합니다.  
  
## <a name="the-fix-for-richedit-controls"></a>RichEdit 컨트롤에 대 한 수정 프로그램  
 호출 해야 **LoadLibrary** rich edit 컨트롤에 대 한 합니다. 자세한 내용은 참조 [MFC에 RichEdit 1.0 컨트롤 사용](../windows/using-the-richedit-1-0-control-with-mfc.md), [Rich Edit 컨트롤](http://msdn.microsoft.com/library/windows/desktop/bb787873) 에 [!INCLUDE[winsdkshort](../atl-mfc-shared/reference/includes/winsdkshort_md.md)], 및 [서식 있는 편집 컨트롤의 개요](../mfc/overview-of-the-rich-edit-control.md)합니다.  
  
## <a name="requirements"></a>요구 사항  
 Win32  
  
## <a name="see-also"></a>참고 항목  
 [대화 상자 편집기 문제 해결](../windows/troubleshooting-the-dialog-editor.md)   
 [대화 상자 편집기](../windows/dialog-editor.md)

