---
title: "서버: 내부 프레임 창 구현 | Microsoft Docs"
ms.custom: 
ms.date: 11/04/2016
ms.reviewer: 
ms.suite: 
ms.technology: cpp-windows
ms.tgt_pltfrm: 
ms.topic: article
dev_langs: C++
helpviewer_keywords:
- frame windows [MFC], implementing
- OLE server applications [MFC], frame windows
- servers, in-place frame windows
- frame windows [MFC], in-place
- in-place frame windows
ms.assetid: 09bde4d8-15e2-4fba-8d14-9b954d926b92
caps.latest.revision: "10"
author: mikeblome
ms.author: mblome
manager: ghogen
ms.workload: cplusplus
ms.openlocfilehash: 7e26cbb0099f897c65ab3e39338f3c36e77112e0
ms.sourcegitcommit: 8fa8fdf0fbb4f57950f1e8f4f9b81b4d39ec7d7a
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 12/21/2017
---
# <a name="servers-implementing-in-place-frame-windows"></a>서버: 내부 프레임 창 구현
이 문서에서는 서버 응용 프로그램을 만들 때 응용 프로그램 마법사를 사용하지 않는 경우, 시각적인 편집 서버 응용 프로그램에서 내부 프레임 창을 구현하기 위해 수행해야 하는 작업에 대해 설명합니다. 이 문서에 설명 된 절차를 수행 하는 대신 응용 프로그램 마법사에서 생성 된 응용 프로그램 또는 Visual c + +와 함께 제공 되는 샘플에서 기존에 내부 frame-window 클래스를 사용할 수 있습니다.  
  
#### <a name="to-declare-an-in-place-frame-window-class"></a>내부 frame-window 클래스를 선언하려면  
  
1.  `COleIPFrameWnd`에서 내부 frame-window 클래스를 파생합니다.  
  
    -   클래스 헤더 파일에서 `DECLARE_DYNCREATE` 매크로를 사용합니다.  
  
    -   클래스 구현(.cpp) 파일에서 `IMPLEMENT_DYNCREATE` 매크로를 사용합니다. 이렇게 하면 프레임워크가 이 클래스의 개체를 만들 수 있습니다.  
  
2.  frame-window 클래스에서 `COleResizeBar` 멤버를 선언합니다. 이 멤버는 서버 응용 프로그램의 내부 크기 조정을 지원하려는 경우에 필요합니다.  
  
     선언는 `OnCreate` 메시지 처리기 (사용 하는 **속성** 창), 호출 **만들기** 에 대 한 프로그램 `COleResizeBar` 멤버를 정의 했습니다.  
  
3.  도구 모음이 있으면 frame-window 클래스에서 `CToolBar` 멤버를 선언합니다.  
  
     서버가 내부에서 활성 상태일 때 도구 모음을 만들도록 `OnCreateControlBars` 멤버 함수를 재정의합니다. 예:  
  
     [!code-cpp[NVC_MFCOleServer#1](../mfc/codesnippet/cpp/servers-implementing-in-place-frame-windows_1.cpp)]  
  
     5단계의 코드 설명을 참조하십시오.  
  
4.  기본 .cpp 파일에서 이 내부 frame-window 클래스에 대한 헤더 파일을 포함합니다.  
  
5.  응용 프로그램 클래스에 대한 `InitInstance`에서 문서 템플릿 개체의 `SetServerInfo` 함수를 호출하여 열기 및 내부 편집에 사용할 리소스 및 내부 프레임 창을 지정합니다.  
  
 있는 일련의 함수 호출의 **경우** 문은 만듭니다 도구 모음 리소스에서 제공 되는 server입니다. 이 지점에서 도구 모음은 컨테이너의 창 계층의 일부입니다. 도구 모음이 `CToolBar`에서 파생되기 때문에 소유자를 변경하지 않는 한, 해당 메시지를 소유자 즉, 컨테이너 응용 프로그램의 프레임 창으로 전달합니다. `SetOwner` 호출이 필요한 이유는 바로 이 때문입니다. 이 호출은 명령이 서버의 내부 프레임 창에 전달되는 창을 변경해서 메시지가 서버에 전달되도록 합니다. 그러면 서버가 제공된 도구 모음에서 작업에 반응할 수 있습니다.  
  
 도구 모음 비트맵 ID는 서버 응용 프로그램에 정의된 다른 내부 리소스와 동일해야 합니다. 참조 [메뉴 및 리소스: 서버 추가](../mfc/menus-and-resources-server-additions.md) 대 한 자세한 내용은 합니다.  
  
 자세한 내용은 참조 [COleIPFrameWnd](../mfc/reference/coleipframewnd-class.md), [COleResizeBar](../mfc/reference/coleresizebar-class.md), 및 [CDocTemplate::SetServerInfo](../mfc/reference/cdoctemplate-class.md#setserverinfo) 에 *클래스 라이브러리 참조*.  
  
## <a name="see-also"></a>참고 항목  
 [서버](../mfc/servers.md)   
 [서버: 서버 구현](../mfc/servers-implementing-a-server.md)   
 [서버: 서버 문서 구현](../mfc/servers-implementing-server-documents.md)   
 [서버: 서버 항목](../mfc/servers-server-items.md)

