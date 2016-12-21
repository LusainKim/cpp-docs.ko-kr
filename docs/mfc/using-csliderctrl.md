---
title: "CSliderCtrl 사용 | Microsoft Docs"
ms.custom: ""
ms.date: "12/03/2016"
ms.prod: "visual-studio-dev14"
ms.reviewer: ""
ms.suite: ""
ms.technology: 
  - "devlang-cpp"
ms.tgt_pltfrm: ""
ms.topic: "article"
f1_keywords: 
  - "CSliderCtrl"
dev_langs: 
  - "C++"
helpviewer_keywords: 
  - "CSliderCtrl 클래스, using"
  - "슬라이더 컨트롤, using"
ms.assetid: 242c7bcd-126e-4b9b-8f76-8082ad06fe73
caps.latest.revision: 10
caps.handback.revision: 6
author: "mikeblome"
ms.author: "mblome"
manager: "ghogen"
---
# CSliderCtrl 사용
[!INCLUDE[vs2017banner](../assembler/inline/includes/vs2017banner.md)]

The [CSliderCtrl](../mfc/reference/csliderctrl-class.md) class represents a slider control, which is also called a trackbar.  A "slider control" is a window that contains a slider and optional tick marks.  When the user moves the slider, using either the mouse or the arrow keys, the slider control sends notification messages to indicate the change.  
  
 Slider controls are useful when you want the user to select a discrete value or a set of consecutive values in a range.  For example, you might use a slider control to allow the user to set the repeat rate of the keyboard by moving the slider to a given tick mark.  
  
 The slider in a slider control moves in increments that you specify when you create it.  For example, if you specify that the slider control should have a range of five, the slider can only occupy six positions: a position at the left side of the slider control and one position for each increment in the range.  Typically, each of these positions is identified by a tick mark.  
  
## 추가 정보  
  
-   [Using Slider Controls](../mfc/using-slider-controls.md)  
  
-   [Slider Control Styles](../mfc/slider-control-styles.md)  
  
-   [Slider Control Member Functions](../mfc/slider-control-member-functions.md)  
  
-   [Slider Notification Messages](../mfc/slider-notification-messages.md)  
  
## 참고 항목  
 [컨트롤](../mfc/controls-mfc.md)