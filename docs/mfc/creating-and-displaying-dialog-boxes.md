---
title: "대화 상자 만들기 및 표시 | Microsoft Docs"
ms.custom: 
ms.date: 11/04/2016
ms.reviewer: 
ms.suite: 
ms.technology: cpp-windows
ms.tgt_pltfrm: 
ms.topic: article
dev_langs: C++
helpviewer_keywords:
- modal dialog boxes [MFC], creating
- opening dialog boxes
- modeless dialog boxes [MFC], creating
- MFC dialog boxes [MFC], creating
- MFC dialog boxes [MFC], displaying
ms.assetid: 1c5219ee-8b46-44bc-9708-83705d4f248b
caps.latest.revision: "9"
author: mikeblome
ms.author: mblome
manager: ghogen
ms.workload: cplusplus
ms.openlocfilehash: d436301a979dbba2bc4a922f8427f355a398f654
ms.sourcegitcommit: 8fa8fdf0fbb4f57950f1e8f4f9b81b4d39ec7d7a
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 12/21/2017
---
# <a name="creating-and-displaying-dialog-boxes"></a>대화 상자 만들기 및 표시
대화 상자 개체 만들기는 2단계 작업입니다. 먼저, 대화 상자 개체를 생성한 다음 대화 상자 창을 만듭니다. 모달 및 모덜리스 대화 상자는 만들고 표시하는 과정에서 차이가 있습니다. 다음 표는 모달 및 모덜리스 대화 상자가 일반적으로 생성되고 표시되는 방법을 보여 줍니다.  
  
### <a name="dialog-creation"></a>대화 상자 만들기  
  
|대화 상자 형식|대화 상자를 만드는 방법|  
|-----------------|----------------------|  
|[모덜리스](../mfc/creating-modeless-dialog-boxes.md)|생성 `CDialog`, 호출 **만들기** 멤버 함수입니다.|  
|[모달](../mfc/creating-modal-dialog-boxes.md)|`CDialog`를 구성한 다음 `DoModal` 멤버 함수를 호출합니다.|  
  
 만들 수 있습니다를에서 대화 상자는 [메모리 내 대화 상자 템플릿을](../mfc/using-a-dialog-template-in-memory.md) 를 생성 한 대화 상자 템플릿 리소스에서 읽지 못하고 있습니다. 그러나 이는 고급 항목입니다.  
  
## <a name="see-also"></a>참고 항목  
 [대화 상자의 수명 주기](../mfc/life-cycle-of-a-dialog-box.md)

