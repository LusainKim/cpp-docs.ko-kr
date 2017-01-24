---
title: "인터페이스에 선언된 이벤트에는 &#39;Custom&#39; 한정자를 사용할 수 없습니다. | Microsoft Docs"
ms.custom: ""
ms.date: "11/17/2016"
ms.prod: "visual-studio-dev14"
ms.reviewer: ""
ms.suite: ""
ms.technology: 
  - "devlang-visual-basic"
ms.tgt_pltfrm: ""
ms.topic: "article"
f1_keywords: 
  - "bc31121"
  - "vbc31121"
helpviewer_keywords: 
  - "BC31121"
ms.assetid: b5687034-a2b2-4961-88b7-0ba73023573e
caps.latest.revision: 8
caps.handback.revision: 8
author: "stevehoag"
ms.author: "shoag"
manager: "wpickett"
---
# 인터페이스에 선언된 이벤트에는 &#39;Custom&#39; 한정자를 사용할 수 없습니다.
사용자 지정 이벤트는 `AddHandler`, `RemoverHandler` 및 `RaiseEvent` 메서드의 구현을 제공해야 하므로 인터페이스에서 선언할 수 없습니다.  
  
 이벤트를 구현하는 파생 클래스에서 `Custom` 키워드를 사용할 수 있습니다.  
  
 **오류 ID:** BC31121  
  
### 이 오류를 해결하려면  
  
-   인터페이스의 이벤트 선언에서 `Custom` 키워드를 제거합니다.  
  
## 예제  
 이 예제에서는 인터페이스에서 선언된 이벤트를 사용자 지정 이벤트로 구현하는 방법을 보여 줍니다.  
  
 [!code-vb[VbVbalrEventError#3](../misc/codesnippet/VisualBasic/custom-modifier-is-not-valid-on-events-declared-in-interfaces_1.vb)]  
  
## 참고 항목  
 [Custom \- 삭제](http://msdn.microsoft.com/ko-kr/dc62be07-c896-4866-a533-982a661d143f)   
 [Event Statement](../Topic/Event%20Statement.md)   
 [Delegate Statement](../Topic/Delegate%20Statement.md)   
 [Class Statement](../Topic/Class%20Statement%20\(Visual%20Basic\).md)   
 [Interface Statement](../Topic/Interface%20Statement%20\(Visual%20Basic\).md)   
 [Events](../Topic/Events%20\(Visual%20Basic\).md)