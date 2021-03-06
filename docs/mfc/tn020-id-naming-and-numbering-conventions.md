---
title: "TN020: ID 명명 및 번호 매기기 규칙 | Microsoft Docs"
ms.custom: 
ms.date: 11/04/2016
ms.reviewer: 
ms.suite: 
ms.technology: cpp-windows
ms.tgt_pltfrm: 
ms.topic: article
f1_keywords: vc.id
dev_langs: C++
helpviewer_keywords:
- TN020
- resource identifiers, naming and numbering
- resource identifiers
ms.assetid: aecbd2cf-68b3-47f6-ae21-b1f507917245
caps.latest.revision: "17"
author: mikeblome
ms.author: mblome
manager: ghogen
ms.workload: cplusplus
ms.openlocfilehash: a666c2183276b95a9405400de8acc0117c7134e1
ms.sourcegitcommit: 8fa8fdf0fbb4f57950f1e8f4f9b81b4d39ec7d7a
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 12/21/2017
---
# <a name="tn020-id-naming-and-numbering-conventions"></a>TN020: ID 명명 및 번호 매기기 규칙
이 노트 ID 명명 및 리소스, 명령, 문자열, 컨트롤 및 자식 창에 대 한 MFC 2.0을 사용 하는 번호 매기기 규칙을 설명 합니다.  
  
 MFC ID 명명 및 번호 매기기 규칙 다음 요구 사항을 충족 하도록 되어 있습니다.  
  
-   MFC 라이브러리 및 Visual c + + 리소스 편집기에서 지원 되는 MFC 응용 프로그램에서 사용 되는 일관 ID 명명 표준을 제공 합니다. 이렇게 하면 형식 및 ID에서 리소스의 출처를 해석 하는 프로그래머에 대해 쉽게  
  
-   특정 유형의 Id 간의 강력한 1-1 관계를 강조 합니다.  
  
-   이미 널리 사용 되는 표준 windows에서 Id 명명에 대 한 준수 합니다.  
  
-   파티션 ID 번호 매기기 공간입니다. ID 번호 프로그래머, MFC, Windows 및 Visual c + + 편집할 리소스가 할당 될 수 있습니다. 적절 한 분할 ID 번호 중복을 방지 하는 데 도움이 됩니다.  
  
## <a name="the-id-prefix-naming-convention"></a>ID 접두사 명명 규칙  
 여러 유형의 Id는 응용 프로그램에서 발생할 수 있습니다. MFC ID 명명 규칙 여러 리소스 종류에 대 한 서로 다른 접두사를 정의합니다.  
  
 MFC "IDR_" 접두사를 사용 하 여 여러 리소스 종류에 적용 되는 리소스 ID를 나타냅니다. 예를 들어 특정된 프레임 창에 대 한 MFC를 사용 하 여 동일한 "IDR_" 접두사 메뉴, 액셀러레이터 키, 문자열 및 아이콘 리소스를 나타냅니다. 다음 표에서 다양 한 접두사와 그 사용 방법을 보여 줍니다.  
  
|접두사|기능|  
|------------|---------|  
|IDR_|에 대 한 여러 리소스 종류를 (메뉴, 가속기 및 리본에 주로 사용).|  
|IDD_|대화 상자 템플릿 리소스 (예를 들어 IDD_DIALOG1).|  
|IDC_|커서 리소스의 경우.|  
|IDI_|아이콘 리소스의 경우.|  
|IDB_|비트맵 리소스의 경우.|  
|IDS_|에 대 한 리소스는 문자열입니다.|  
  
 MFC 대화 상자 리소스 내에서 이러한 규칙을 따릅니다.  
  
|접두사 또는 레이블|사용|  
|---------------------|---------|  
|IDOK, IDCANCEL|에 대 한 표준 누름 단추 Id입니다.|  
|IDC_|다른 대화 상자 컨트롤입니다.|  
  
 "IDC_" 접두사는 커서에도 사용 됩니다. 이 이름 충돌 문제가 되지 않습니다 일반적으로 몇 가지 커서 및 여러 대화 상자 컨트롤을 더 일반적인 응용 프로그램입니다.  
  
 메뉴 리소스 내에서 MFC는 이러한 규칙을 따릅니다.  
  
|접두사|사용|  
|------------|---------|  
|IDM_|MFC 명령 아키텍처를 사용 하지 않는 메뉴 항목에 대 한|  
|ID_|MFC를 사용 하는 메뉴 명령에 대 한 아키텍처를 명령입니다.|  
  
 MFC 명령 아키텍처 뒤에 나오는 명령은 있어야는 `ON_COMMAND` 명령 처리기 있고 사용할 수 있습니다는 `ON_UPDATE_COMMAND_UI` 처리기입니다. 이러한 명령 처리기에서 MFC 명령 아키텍처를 따르는 경우 프로그램이 제대로 작동지 것입니다 메뉴 명령, 도구 모음 단추 또는 대화 상자 막대 단추에 바인딩되어 있는지 여부. 동일한 "ID_" 접두사는 프로그램의 메시지 표시줄에 표시 되는 메뉴 프롬프트 문자열에도 사용 됩니다. 대부분 응용 프로그램에서 메뉴 항목의 MFC 명령 규칙을 따라야 합니다. 모든 표준 명령 Id (예를 들어 `ID_FILE_NEW`)이이 규칙을 따릅니다.  
  
 또한 MFC는 특수 한 형태의 문자열 ("형식이 사용") 하는 대신으로 "IDP_"를 사용합니다. "IDP_" 접두사가 포함 된 문자열에는 표시 되는 메시지, 즉, 메시지 상자에 사용 되는 문자열입니다. 문자열 "IDP_"는 프로그램에 의해 결정 되는 문자열의 자리 표시자로 "%1" 및 "%2"를 포함할 수 있습니다. 일반적으로 "IDP_" 문자열 그와 관련 된 도움말 항목이 있고 "형식이 사용" 문자열은 그렇지 않습니다. "IDP_" 문자열이 지역화 항상 됩니다 및 "형식이 사용" 문자열을 지역화할 수 있습니다.  
  
 또한 MFC 라이브러리는 특수 한 형태의 컨트롤 Id (대신 "IDC_")으로 "IDW_" 접두사를 사용합니다. 이러한 Id는 뷰 및 분할 창을 같이 자식 창에 프레임 워크 클래스에 의해 할당 됩니다. MFC 구현 Id "AFX_" 접두사로 추가 됩니다.  
  
## <a name="the-id-numbering-convention"></a>ID 번호 매기기 규칙  
 다음 표에서 특정 유형의 Id에 대 한 유효한 범위를 나열합니다. 기술 구현 제한 한도 중 일부는 고, 나머지는 미리 정의 된 Windows Id 또는 MFC 기본 구현 충돌 여 Id를 방지 하기 위해 설계 된 규칙입니다.  
  
 권장된 범위 내 모든 Id를 정의 하는 것이 좋습니다. 0이 사용 되지 않으므로 이러한 범위의 하 한은 1입니다. 일반적인 규칙을 사용 하 여 첫 번째 ID로 100 또는 101를 사용 하는 것이 좋습니다.  
  
|접두사|리소스 종류|유효 범위|  
|------------|-------------------|-----------------|  
|IDR_|여러 가지|1 ~ 0x6FFF|  
|IDD_|대화 상자 템플릿|1 ~ 0x6FFF|  
|IDC_, IDI_, IDB_|비트맵, 아이콘, 커서|1 ~ 0x6FFF|  
|형식이 사용, IDP_|일반 문자열|1 ~ 0x7FFF|  
|ID_|명령|0x8000 0xDFFF까지|  
|IDC_|컨트롤|8 ~ 0xDFFF|  
  
 이러한 범위 제한에 대 한 이유:  
  
-   규칙에 따라 0의 ID 값 사용 되지 않습니다.  
  
-   Windows 구현 제한으로 인해 제한 실제 리소스 Id를 0x7FFF 보다 작거나 같아야 합니다.  
  
-   MFC의 내부 프레임 워크는 이러한 범위를 예약 합니다.  
  
    -   0x7FFF 통해 0x7000 (afxres.h 참조)  
  
    -   0xEFFF 통해 0xE000 (afxres.h 참조)  
  
    -   16000 18000 (afxribbonres.h 참조)를 통해  
  
     MFC 구현에서는 이러한 범위 나중에 변경할 수 있습니다.  
  
-   0xf000 0xFFFF의 범위를 사용 하는 몇 가지 Windows 시스템 명령입니다.  
  
-   1-7의 컨트롤 Id IDOK IDCANCEL 등의 표준 컨트롤에 대 한 예약 되어 있습니다.  
  
-   0x8000 문자열에 대 한 0xFFFF까지 범위의 메뉴 프롬프트 명령에 대 한 예약 되어 있습니다.  
  
## <a name="see-also"></a>참고 항목  
 [번호별 기술 참고 사항](../mfc/technical-notes-by-number.md)   
 [범주별 기술 참고 사항](../mfc/technical-notes-by-category.md)

