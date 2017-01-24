---
title: "슬라이더 컨트롤 스타일 | Microsoft Docs"
ms.custom: ""
ms.date: "12/03/2016"
ms.prod: "visual-studio-dev14"
ms.reviewer: ""
ms.suite: ""
ms.technology: 
  - "devlang-cpp"
ms.tgt_pltfrm: ""
ms.topic: "article"
dev_langs: 
  - "C++"
helpviewer_keywords: 
  - "CSliderCtrl 클래스, 스타일"
  - "슬라이더 컨트롤, 스타일"
  - "스타일, CSliderCtrl"
  - "스타일, 슬라이더 컨트롤"
ms.assetid: 64c491fc-5af1-4f97-ae30-854071b3dc02
caps.latest.revision: 10
caps.handback.revision: 6
author: "mikeblome"
ms.author: "mblome"
manager: "ghogen"
---
# 슬라이더 컨트롤 스타일
[!INCLUDE[vs2017banner](../assembler/inline/includes/vs2017banner.md)]

Slider controls \([CSliderCtrl](../mfc/reference/csliderctrl-class.md)\) can have either a vertical or horizontal orientation.  They can have tick marks on either side, both sides, or neither.  They can also be used to specify a range of consecutive values.  These properties are controlled by using slider control styles, which you specify when you create the slider control.  
  
 The `TBS_HORZ` and `TBS_VERT` styles determine the orientation of the slider control.  If you do not specify an orientation, the slider control is oriented horizontally.  
  
 The `TBS_AUTOTICKS` style creates a slider control that has a tick mark for each increment in its range of values.  These tick marks are added automatically when you call the [SetRange](../Topic/CSliderCtrl::SetRange.md) member function.  If you do not specify `TBS_AUTOTICKS`, you can use member functions, such as [SetTic](../Topic/CSliderCtrl::SetTic.md) and [SetTicFreq](../Topic/CSliderCtrl::SetTicFreq.md), to specify the positions of the tick marks.  To create a slider control that does not display tick marks, you can use the `TBS_NOTICKS` style.  
  
 You can display tick marks on either or both sides of the slider control.  For horizontal slider controls, you can specify the `TBS_BOTTOM` or `TBS_TOP` style.  For vertical slider controls, you can specify the `TBS_RIGHT` or `TBS_LEFT` style. \(`TBS_BOTTOM` and `TBS_RIGHT` are the default settings.\) For tick marks on both sides of the slider control in any orientation, specify the `TBS_BOTH` style.  
  
 A slider control can display a selection range only if you specify the `TBS_ENABLESELRANGE` style when you create it.  When a slider control has this style, the tick marks at the starting and ending positions of a selection range are displayed as triangles \(instead of vertical dashes\) and the selection range is highlighted.  For example, selection ranges might be useful in a simple scheduling application.  The user could select a range of tick marks corresponding to hours in a day to identify a scheduled meeting time.  
  
 By default, the length of a slider control's slider varies as the selection range changes.  If the slider control has the **TBS\_FIXEDLENGTH** style, the length of the slider remains the same even if the selection range changes.  A slider control that has the **TBS\_NOTHUMB** style does not include a slider.  
  
## 참고 항목  
 [CSliderCtrl 사용](../mfc/using-csliderctrl.md)   
 [컨트롤](../mfc/controls-mfc.md)