---
title: "속성이 &#39;Private&#39; 접근자를 포함하므로 &#39;&lt;propertymodifier&gt;&#39;로 선언할 수 없습니다. | Microsoft Docs"
ms.custom: ""
ms.date: "11/24/2016"
ms.prod: "visual-studio-dev14"
ms.reviewer: ""
ms.suite: ""
ms.technology: 
  - "devlang-visual-basic"
ms.tgt_pltfrm: ""
ms.topic: "article"
f1_keywords: 
  - "vbc31108"
  - "bc31108"
helpviewer_keywords: 
  - "BC31108"
ms.assetid: 74fb36f4-54cd-4fda-bcc6-e965b5c7c37b
caps.latest.revision: 9
caps.handback.revision: 9
author: "stevehoag"
ms.author: "shoag"
manager: "wpickett"
---
# 속성이 &#39;Private&#39; 접근자를 포함하므로 &#39;&lt;propertymodifier&gt;&#39;로 선언할 수 없습니다.
`Private` 속성 프로시저\(`Get` 또는 `Set`\)를 포함하는 속성이 [Overridable](../Topic/Overridable%20\(Visual%20Basic\).md)로 표시되었습니다.  
  
 기본 클래스 속성 또는 프로시저가 [Private](../Topic/Private%20\(Visual%20Basic\).md)로 선언된 경우 액세스할 수 없으므로 파생 클래스에서 해당 속성이나 프로시저를 재정의할 수 없습니다. 그러므로 `Private`를 `Overridable`과 함께 사용할 수 없습니다. 이는 속성 자체뿐 아니라 개별 속성 프로시저에도 적용됩니다.  
  
 **오류 ID:** BC31108  
  
### 이 오류를 해결하려면  
  
-   [Property Statement](../Topic/Property%20Statement.md)에서 `Overridable` 키워드를 제거하거나 [Get Statement](../Topic/Get%20Statement.md) 또는 [Set Statement](../Topic/Set%20Statement%20\(Visual%20Basic\).md)에서 `Private` 키워드를 제거합니다.  
  
## 참고 항목  
 [Property 프로시저](../Topic/Property%20Procedures%20\(Visual%20Basic\).md)   
 [How to: Declare a Property with Mixed Access Levels](../Topic/How%20to:%20Declare%20a%20Property%20with%20Mixed%20Access%20Levels%20\(Visual%20Basic\).md)