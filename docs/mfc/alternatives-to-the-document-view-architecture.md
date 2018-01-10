---
title: "문서 뷰 아키텍처의 대체 | Microsoft Docs"
ms.custom: 
ms.date: 11/04/2016
ms.reviewer: 
ms.suite: 
ms.technology: cpp-windows
ms.tgt_pltfrm: 
ms.topic: article
dev_langs: C++
helpviewer_keywords:
- documents [MFC], applications without
- CDocument class [MFC], space requirements
- views [MFC], applications without
ms.assetid: 2c22f352-a137-45ce-9971-c142173496fb
caps.latest.revision: "9"
author: mikeblome
ms.author: mblome
manager: ghogen
ms.workload: cplusplus
ms.openlocfilehash: 459383474c9ffed9a7ad6cefe01ea21626cb23b1
ms.sourcegitcommit: 8fa8fdf0fbb4f57950f1e8f4f9b81b4d39ec7d7a
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 12/21/2017
---
# <a name="alternatives-to-the-documentview-architecture"></a>문서/뷰 아키텍처의 대체
MFC 응용 프로그램은 일반적으로 문서/뷰 아키텍처를 사용하여 정보, 파일 형식 및 사용자 데이터의 시각적 표현을 관리합니다. 대부분의 데스크톱 응용 프로그램에 대해 문서/뷰 아키텍처는 적절하고 효율적인 응용 프로그램 아키텍처입니다. 이 아키텍처는 뷰에서 데이터를 구분하고, 대부분의 경우 응용 프로그램을 단순화하고 코드 중복을 줄입니다.  
  
 그러나 문서/뷰 아키텍처는 일부 상황에 적절하지 않습니다. 이 예제를 참조하십시오.  
  
-   Windows용 C로 작성된 응용 프로그램을 이식하는 경우 응용 프로그램에 문서/뷰 지원을 추가하기 전에 이식을 완료하는 것이 좋습니다.  
  
-   간단한 유틸리티를 작성하는 경우 문서/뷰 아키텍처 없이 작성할 수 있음을 알 수 있습니다.  
  
-   원본 코드가 이미 데이터 뷰와 데이터 관리를 혼합한 경우 두 가지를 구분해야 하므로 문서/뷰 모델에 코드를 이동할 필요가 없습니다. 코드를 현재 상태로 둘 수 있습니다.  
  
 문서/뷰 아키텍처를 사용 하지 않는 응용 프로그램을 만들려면의 선택을 취소는 **문서/뷰 아키텍처 지원** MFC 응용 프로그램 마법사의 1 단계에서 확인란 합니다. 참조 [MFC 응용 프로그램 마법사](../mfc/reference/mfc-application-wizard.md) 대 한 자세한 내용은 합니다.  
  
> [!NOTE]
>  MFC 응용 프로그램 마법사에서 생성 된 대화 상자 기반 응용 프로그램 문서/뷰 아키텍처를 사용 하지 마십시오 하므로 **문서/뷰 아키텍처 지원** 대화 응용 프로그램 종류를 선택 하는 경우 확인란은 사용할 수 없습니다.  
  
 Visual C++ 마법사와 소스 및 대화 상자 편집기는 다른 마법사에서 생성된 응용 프로그램과 같이 생성된 응용 프로그램으로 작업합니다. 응용 프로그램 도구 모음, 스크롤 막대 및 상태 표시줄을 지원할 수 있으며이 **에 대 한** 상자입니다. 응용 프로그램에는 문서 템플릿이 등록되지 않고 문서 클래스가 포함되지 않습니다.  
  
 생성 된 응용 프로그램 뷰 클래스에 참고 **CChildView**에서 파생 된 `CWnd`합니다. MFC는 응용 프로그램에서 만든 프레임 창 내에서 뷰 클래스의 인스턴스 하나를 만들고 배치합니다. MFC에서 응용 프로그램 콘텐츠의 배치 및 관리를 단순화하므로 MFC는 뷰 창의 사용을 강제로 적용합니다. 이 클래스의 `OnPaint` 멤버에 그리기 코드를 추가할 수 있습니다. 코드에서는 프레임 대신 뷰에 스크롤 막대를 추가해야 합니다.  
  
 MFC에서 제공하는 문서/뷰 아키텍처는 응용 프로그램의 많은 기본 기능을 구현하므로 프로젝트에서 해당 아키텍처가 없는 경우에는 사용자가 응용 프로그램의 많은 중요한 기능을 구현해야 한다는 의미입니다.  
  
-   MFC 응용 프로그램 마법사에서 제공 하는, 응용 프로그램에 대 한 메뉴만 포함 되어 `New` 및 `Exit` 에 있는 명령을 **파일** 메뉴. `New` 명령은 문서/뷰 지원 없이 SDI 응용 프로그램이 아닌 MDI 응용 프로그램으로만 지원됩니다. 생성된 메뉴 리소스는 MRU(가장 최근에 사용됨) 목록을 지원하지 않습니다.  
  
-   처리기 함수 및 응용 프로그램에서 지원할 포함 하는 모든 명령에 대 한 구현을 추가 해야 **열려** 및 **저장** 에 **파일** 메뉴. MFC는 일반적으로 이러한 기능을 지원하는 코드를 제공하지만 해당 기능은 문서/뷰 아키텍처에 밀접하게 바인딩되어 있습니다.  
  
-   응용 프로그램의 도구 모음은 요청하는 경우 최소로 됩니다.  
  
 마법사가 올바른 MFC 아키텍처를 보장하므로 문서/뷰 아키텍처를 사용하지 않고 MFC 응용 프로그램 마법사를 사용하여 응용 프로그램을 만드는 것이 좋습니다. 그러나 마법사를 사용하지 않도록 해야 하는 경우 코드에서 문서/뷰 아키텍처를 우회하기 위한 몇 가지 방법은 다음과 같습니다.  
  
-   문서를 사용하지 않는 부속물로 취급하고 위에서 제시한 대로 뷰 클래스에서 데이터 관리 코드를 구현합니다. 문서에 대한 오버헤드는 상대적으로 낮습니다. 단일 [CDocument](../mfc/reference/cdocument-class.md) 개체 적은 양의 단독으로 오버 헤드를 더한의 작은 오버 헤드를 발생 시킵니다. **CDocument**의 기본 클래스인 [CCmdTarget](../mfc/reference/ccmdtarget-class.md) 및 [ CObject](../mfc/reference/cobject-class.md)합니다. 후자의 클래스는 모두 작습니다.  
  
     에 선언 된 **CDocument**:  
  
    -   두 개의 `CString` 개체입니다.  
  
    -   세 가지 **BOOL**s입니다.  
  
    -   한 개의 `CDocTemplate` 포인터입니다.  
  
    -   문서 보기 목록이 포함된 한 개의 `CPtrList` 개체입니다.  
  
     또한 문서에는 문서 개체를 만드는 시간, 해당 뷰 개체, 프레임 창 및 문서 템플릿 개체가 필요합니다.  
  
-   문서와 뷰 모두 사용하지 않는 부속물로 취급합니다. 데이터 관리 및 그리기 코드를 뷰 대신 프레임 창에 넣습니다. 이 방법은 C 언어 프로그래밍 모델에 더 가깝습니다.  
  
-   MFC 프레임워크의 문서 및 뷰 만들기를 완전히 제거하기 위해 문서 및 뷰 만들기 부분을 재정의합니다. 문서 작성 프로세스는 `CWinApp::AddDocTemplate`을 호출하여 시작합니다. 응용 프로그램 클래스의 `InitInstance` 멤버 함수에서 호출을 제거하고 대신 `InitInstance`에서 직접 프레임 창을 만듭니다. 프레임 창 클래스에 데이터 관리 코드를 넣습니다. 문서/뷰 만들기 프로세스에 설명 되어 [문서/뷰 만들기](../mfc/document-view-creation.md)합니다. 이 방법은 작업량이 많고 프레임워크에 대한 깊은 이해가 필요하지만 문서/뷰 오버헤드를 완전히 해제합니다.  
  
 문서 [MFC: 문서 데이터베이스 클래스를 사용 하 여 뷰와](../data/mfc-using-database-classes-without-documents-and-views.md) 데이터베이스 응용 프로그램의 컨텍스트에서 문서/뷰 대안의 구체적인 예제를 제공 합니다.  
  
## <a name="see-also"></a>참고 항목  
 [문서/뷰 아키텍처](../mfc/document-view-architecture.md)
