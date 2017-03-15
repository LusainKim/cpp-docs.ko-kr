---
title: "헤더 컨트롤 사용 | Microsoft Docs"
ms.custom: ""
ms.date: "11/04/2016"
ms.reviewer: ""
ms.suite: ""
ms.technology: 
  - "devlang-cpp"
ms.tgt_pltfrm: ""
ms.topic: "article"
dev_langs: 
  - "C++"
helpviewer_keywords: 
  - "헤더 컨트롤"
  - "헤더 컨트롤, 작업"
ms.assetid: af3afb5c-bf97-451b-8fee-3adcb8257210
caps.latest.revision: 10
author: "mikeblome"
ms.author: "mblome"
manager: "ghogen"
caps.handback.revision: 6
---
# 헤더 컨트롤 사용
[!INCLUDE[vs2017banner](../assembler/inline/includes/vs2017banner.md)]

The easy way to use a header control \([CHeaderCtrl](../mfc/reference/cheaderctrl-class.md)\) is in conjunction with a list control; see [Using CListCtrl](../mfc/using-clistctrl.md) later in this topic family.  You can also use a header control by itself.  MFC calls **InitCommonControls** for you.  The key tasks are as follows:  
  
-   [Creating the header control](../mfc/creating-the-header-control.md)  
  
-   [Adding items to the header control](../mfc/adding-items-to-the-header-control.md)  
  
-   [Ordering items in the header control](../mfc/ordering-items-in-the-header-control.md)  
  
-   [Processing header\-control notifications](../mfc/processing-header-control-notifications.md)  
  
 If the header control object is embedded in a parent view or dialog class, the control is destroyed when the parent is destroyed.  
  
## 참고 항목  
 [CHeaderCtrl 사용](../mfc/using-cheaderctrl.md)   
 [컨트롤](../mfc/controls-mfc.md)