---
title: "트리 컨트롤 부모 및 자식 항목 | Microsoft Docs"
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
  - "트리 컨트롤의 자식 항목"
  - "CTreeCtrl 클래스, 부모 및 자식 항목"
  - "CTreeCtrl의 부모 항목"
  - "트리 컨트롤, 부모 및 자식 항목"
ms.assetid: abcea1e4-fe9b-40d9-86dc-1db235f8f103
caps.latest.revision: 10
author: "mikeblome"
ms.author: "mblome"
manager: "ghogen"
caps.handback.revision: 6
---
# 트리 컨트롤 부모 및 자식 항목
[!INCLUDE[vs2017banner](../assembler/inline/includes/vs2017banner.md)]

Any item in a tree control \([CTreeCtrl](../mfc/reference/ctreectrl-class.md)\) can have a list of subitems, which are called child items, associated with it.  An item that has one or more child items is called a parent item.  A child item is displayed below its parent item and is indented to indicate it is subordinate to the parent.  An item that has no parent is at the top of the hierarchy and is called a root item.  
  
 At any given time, the state of a parent item's list of child items can be either expanded or collapsed.  When the state is expanded, the child items are displayed below the parent item.  When it is collapsed, the child items are not displayed.  The list automatically toggles between the expanded and collapsed states when the user double\-clicks the parent item or, if the parent has the **TVS\_HASBUTTONS** style, when the user clicks the button associated with the parent item.  An application can expand or collapse the child items by using the [Expand](../Topic/CTreeCtrl::Expand.md) member function.  
  
 You add an item to a tree control by calling the [InsertItem](../Topic/CTreeCtrl::InsertItem.md) member function.  This function returns a handle of the **HTREEITEM** type, which uniquely identifies the item.  When adding an item, you must specify the handle of the new item's parent item.  If you specify **NULL** or the **TVI\_ROOT** value instead of a parent item handle in the [TVINSERTSTRUCT](http://msdn.microsoft.com/library/windows/desktop/bb773452) structure or `hParent` parameter, the item is added as a root item.  
  
 A tree control sends a [TVN\_ITEMEXPANDING](http://msdn.microsoft.com/library/windows/desktop/bb773537) notification message when a parent item's list of child items is about to be expanded or collapsed.  The notification gives you the opportunity to prevent the change or to set any attributes of the parent item that depend on the state of the list of child items.  After changing the state of the list, the tree control sends a [TVN\_ITEMEXPANDED](http://msdn.microsoft.com/library/windows/desktop/bb773533) notification message.  
  
 When a list of child items is expanded, it is indented relative to the parent item.  You can set the amount of indentation by using the [SetIndent](../Topic/CTreeCtrl::SetIndent.md) member function or retrieve the current amount by using the [GetIndent](../Topic/CTreeCtrl::GetIndent.md) member function.  
  
## 참고 항목  
 [CTreeCtrl 사용](../mfc/using-ctreectrl.md)   
 [컨트롤](../mfc/controls-mfc.md)