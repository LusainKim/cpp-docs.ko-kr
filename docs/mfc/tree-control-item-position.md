---
title: "트리 컨트롤 항목 위치 | Microsoft Docs"
ms.custom: 
ms.date: 11/04/2016
ms.reviewer: 
ms.suite: 
ms.technology: cpp-windows
ms.tgt_pltfrm: 
ms.topic: article
dev_langs: C++
helpviewer_keywords:
- CTreeCtrl class [MFC], item position
- item position in tree controls
- tree controls [MFC], item position
- position, CTreeCtrl items
ms.assetid: cd264344-2cf9-4d90-9ea8-c6900b6f60e7
caps.latest.revision: "10"
author: mikeblome
ms.author: mblome
manager: ghogen
ms.workload: cplusplus
ms.openlocfilehash: db47e27ad0b556e08f51685bf84b6bd998722239
ms.sourcegitcommit: 8fa8fdf0fbb4f57950f1e8f4f9b81b4d39ec7d7a
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 12/21/2017
---
# <a name="tree-control-item-position"></a>트리 컨트롤 항목 위치
항목의 초기 위치는 트리 컨트롤에 항목을 추가할 때 설정 됩니다 ([CTreeCtrl](../mfc/reference/ctreectrl-class.md))를 사용 하 여는 `InsertItem` 멤버 함수입니다. 멤버 함수 호출 이후에 새 항목을 삽입할 수는 항목의 핸들과 부모 항목의 핸들을 지정 합니다. 이러한 값 중 하나 또는 두 번째 핸들로 지정 된 부모의 자식 항목을 식별 해야 합니다: `TVI_FIRST`, `TVI_LAST`, 또는 `TVI_SORT`합니다.  
  
 때 `TVI_FIRST` 또는 `TVI_LAST` 지정, 트리 컨트롤 나 하위 항목의 목록 지정 된 부모 항목의 끝 부분에 새 항목을 배치 합니다. 때 `TVI_SORT` 지정, 트리 컨트롤 항목 레이블 텍스트에 따라 알파벳 순서로 자식 항목의 목록에 새 항목을 삽입 합니다.  
  
 호출 하 여 자식 항목의 부모 항목의 목록이 사전순에 넣을 수 있습니다는 [SortChildren](../mfc/reference/ctreectrl-class.md#sortchildren) 멤버 함수입니다. 이 함수는 모든 수준의 하위 항목을 지정 된 부모 항목 으로부터 내림차순으로 사전순으로 정렬 되는지 여부를 지정 하는 매개 변수를 포함 합니다.  
  
 [SortChildrenCB](../mfc/reference/ctreectrl-class.md#sortchildrencb) 멤버 함수를 사용 하면 정의 된 기준에 따라 자식 항목을 정렬할 수 있습니다. 이 함수를 호출할 때 두 개의 자식 항목의 상대 순서 결정 해야 때마다 트리 컨트롤 호출할 수 있는 응용 프로그램에서 정의 된 콜백 함수를 지정 합니다. 비교 하 고 항목에 대 한 두 개의 32 비트 응용 프로그램 정의 값 및를 호출할 때 지정 하는 세 번째 32 비트 값을 수신 하는 콜백 함수 `SortChildrenCB`합니다.  
  
## <a name="see-also"></a>참고 항목  
 [CTreeCtrl 사용](../mfc/using-ctreectrl.md)   
 [컨트롤](../mfc/controls-mfc.md)

