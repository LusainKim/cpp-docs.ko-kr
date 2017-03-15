---
title: "OLE 끌어서 놓기 및 데이터 전송 클래스 | Microsoft Docs"
ms.custom: ""
ms.date: "11/04/2016"
ms.reviewer: ""
ms.suite: ""
ms.technology: 
  - "devlang-cpp"
ms.tgt_pltfrm: ""
ms.topic: "article"
f1_keywords: 
  - "vc.classes.ole"
dev_langs: 
  - "C++"
helpviewer_keywords: 
  - "ActiveX 클래스[C++]"
  - "데이터 전송[C++], OLE"
  - "데이터 전송 클래스[C++]"
  - "끌어서 놓기[C++], 클래스"
  - "OLE 끌어서 놓기[C++], 및 데이터 전송 클래스"
ms.assetid: c8ab2825-ed69-4b88-8ae6-f368b94726b8
caps.latest.revision: 9
author: "mikeblome"
ms.author: "mblome"
manager: "ghogen"
caps.handback.revision: 5
---
# OLE 끌어서 놓기 및 데이터 전송 클래스
[!INCLUDE[vs2017banner](../assembler/inline/includes/vs2017banner.md)]

These classes are used in OLE data transfers.  They allow data to be transferred between applications by using the Clipboard or through drag and drop.  
  
 [COleDropSource](../mfc/reference/coledropsource-class.md)  
 Controls the drag\-and\-drop operation from start to finish.  This class determines when the drag operation starts and when it ends.  It also displays cursor feedback during the drag\-and\-drop operation.  
  
 [COleDataSource](../mfc/reference/coledatasource-class.md)  
 Used when an application provides data for a data transfer.  `COleDataSource` could be viewed as an object\-oriented Clipboard object.  
  
 [COleDropTarget](../mfc/reference/coledroptarget-class.md)  
 Represents the target of a drag\-and\-drop operation.  A `COleDropTarget` object corresponds to a window on screen.  It determines whether to accept any data dropped onto it and implements the actual drop operation.  
  
 [COleDataObject](../mfc/reference/coledataobject-class.md)  
 Used as the receiver side to `COleDataSource`.  `COleDataObject` objects provide access to the data stored by a `COleDataSource` object.  
  
## 참고 항목  
 [클래스 개요](../mfc/class-library-overview.md)