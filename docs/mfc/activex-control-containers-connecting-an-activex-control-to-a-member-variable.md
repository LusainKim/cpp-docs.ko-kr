---
title: "ActiveX 컨트롤 컨테이너: ActiveX 컨트롤을 멤버 변수에 연결 | Microsoft Docs"
ms.custom: 
ms.date: 11/04/2016
ms.reviewer: 
ms.suite: 
ms.technology: cpp-windows
ms.tgt_pltfrm: 
ms.topic: article
dev_langs: C++
helpviewer_keywords:
- ActiveX control containers [MFC], accessing ActiveX controls
- ActiveX controls [MFC], member variables of project
- connecting ActiveX controls to container member variables
- ActiveX controls [MFC], accessing
- member variables [MFC], ActiveX controls in project
- ActiveX control containers [MFC], ActiveX controls as member variables
ms.assetid: 7898a336-440d-4a60-be43-cb062b807aee
caps.latest.revision: "9"
author: mikeblome
ms.author: mblome
manager: ghogen
ms.workload: cplusplus
ms.openlocfilehash: 2248dd68b0ecc7471899552bcb7b0394f3f9f363
ms.sourcegitcommit: 8fa8fdf0fbb4f57950f1e8f4f9b81b4d39ec7d7a
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 12/21/2017
---
# <a name="activex-control-containers-connecting-an-activex-control-to-a-member-variable"></a>ActiveX 컨트롤 컨테이너: ActiveX 컨트롤을 멤버 변수에 연결
ActiveX 컨트롤의 컨트롤 컨테이너 응용 프로그램 내에서 액세스 하는 가장 쉬운 방법은 컨트롤이 포함 될 대화 상자 클래스의 멤버 변수가 있는 ActiveX 컨트롤을 연결 하는 것입니다.  
  
> [!NOTE]
>  컨테이너 클래스 내에서 포함된 된 컨트롤에 액세스 하는 유일한 방법은 아닙니다. 하지만이 문서의 목적에 대 한 것으로 충분 합니다.  
  
### <a name="adding-a-member-variable-to-the-dialog-class"></a>대화 상자 클래스에 멤버 변수 추가  
  
1.  클래스 뷰에서 바로 가기 메뉴를 열고 주 대화 상자 클래스를 마우스 오른쪽 단추로 클릭 합니다. 예를 들어, `CContainerDlg`을 입력합니다.  
  
2.  바로 가기 메뉴에서 클릭 **추가** 차례로 **변수 추가**합니다.  
  
3.  멤버 변수 추가 마법사에서 클릭 **제어 변수**합니다.  
  
4.  에 **컨트롤 ID** 목록 상자에서 포함 된 ActiveX 컨트롤의 컨트롤 ID를 선택 합니다. 예를 들어, `IDC_CIRCCTRL1`을 입력합니다.  
  
5.  에 **변수 이름** 상자에 이름을 입력 합니다.  
  
     예를 들어, `m_circctl`을 입력합니다.  
  
6.  클릭 **마침** 하 여 변경 내용을 적용 하 고 멤버 변수 추가 마법사를 종료 합니다.  
  
## <a name="see-also"></a>참고 항목  
 [ActiveX 컨트롤 컨테이너](../mfc/activex-control-containers.md)

