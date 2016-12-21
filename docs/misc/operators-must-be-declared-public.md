---
title: "연산자를 &#39;Public&#39;으로 선언해야 합니다. | Microsoft Docs"
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
  - "vbc33011"
  - "bc33011"
helpviewer_keywords: 
  - "BC33011"
ms.assetid: 67fc0dee-4ef5-4afc-a63a-f7d20bce7954
caps.latest.revision: 8
caps.handback.revision: 8
author: "stevehoag"
ms.author: "shoag"
manager: "wpickett"
---
# 연산자를 &#39;Public&#39;으로 선언해야 합니다.
[Operator Statement](../Topic/Operator%20Statement.md)에 [Public](../Topic/Public%20\(Visual%20Basic\).md) 키워드가 없습니다.  
  
 `Operator` 프로시저에는 `Public` 및 [Shared](../Topic/Shared%20\(Visual%20Basic\).md) 키워드가 둘 다 필요하며, 변환 연산자에도 [Widening](../Topic/Widening%20\(Visual%20Basic\).md) 또는 [Narrowing](../Topic/Narrowing%20\(Visual%20Basic\).md) 키워드가 필요합니다.  
  
 **오류 ID:** BC33011  
  
### 이 오류를 해결하려면  
  
-   `Operator` 문에 `Public` 키워드를 추가합니다.  
  
## 참고 항목  
 [Operator Procedures](../Topic/Operator%20Procedures%20\(Visual%20Basic\).md)   
 [Operator Statement](../Topic/Operator%20Statement.md)   
 [How to: Define an Operator](../Topic/How%20to:%20Define%20an%20Operator%20\(Visual%20Basic\).md)   
 [How to: Define a Conversion Operator](../Topic/How%20to:%20Define%20a%20Conversion%20Operator%20\(Visual%20Basic\).md)