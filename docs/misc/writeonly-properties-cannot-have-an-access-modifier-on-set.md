---
title: "&#39;WriteOnly&#39; 속성에는 &#39;Set&#39;에 대한 액세스 한정자를 사용할 수 없습니다. | Microsoft Docs"
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
  - "bc31104"
  - "vbc31104"
helpviewer_keywords: 
  - "BC31104"
ms.assetid: d1ac04a8-e436-4f3e-8d71-fc4569b35fcd
caps.latest.revision: 8
caps.handback.revision: 8
author: "stevehoag"
ms.author: "shoag"
manager: "wpickett"
---
# &#39;WriteOnly&#39; 속성에는 &#39;Set&#39;에 대한 액세스 한정자를 사용할 수 없습니다.
`WriteOnly` 속성 선언은 [Property Statement](../Topic/Property%20Statement.md) 및 [Set Statement](../Topic/Set%20Statement%20\(Visual%20Basic\).md) 모두에서 액세스 수준을 지정합니다.  
  
 언제든지 속성에 대한 액세스 수준을 지정할 수 있습니다. 또한 속성의 액세스 수준보다 더 제한적인 경우 해당 속성 프로시저\(`Get` 또는 `Set`\) 중 최대 하나에 대해 다른 액세스 수준을 지정할 수 있습니다. 두 속성 프로시저 모두에 대해 액세스 수준을 지정할 수는 없습니다.  
  
 **오류 ID:** BC31104  
  
### 이 오류를 해결하려면  
  
-   `Set` 문에서 액세스 한정자를 제거합니다. 전체 `WriteOnly` 속성을 나타내며 속성에 대해 두 개의 액세스 수준을 사용할 수 없습니다.  
  
## 참고 항목  
 [Property 프로시저](../Topic/Property%20Procedures%20\(Visual%20Basic\).md)   
 [How to: Declare a Property with Mixed Access Levels](../Topic/How%20to:%20Declare%20a%20Property%20with%20Mixed%20Access%20Levels%20\(Visual%20Basic\).md)