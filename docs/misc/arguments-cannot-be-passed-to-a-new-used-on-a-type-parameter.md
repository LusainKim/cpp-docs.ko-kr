---
title: "형식 매개 변수에 사용된 &#39;New&#39;에 인수를 전달할 수 없습니다. | Microsoft Docs"
ms.custom: ""
ms.date: "11/16/2016"
ms.prod: "visual-studio-dev14"
ms.reviewer: ""
ms.suite: ""
ms.technology: 
  - "devlang-visual-basic"
ms.tgt_pltfrm: ""
ms.topic: "article"
f1_keywords: 
  - "BC32085"
  - "vbc32085"
helpviewer_keywords: 
  - "BC32085"
ms.assetid: a60bf62d-2b2e-4621-b8db-e67720b918fb
caps.latest.revision: 8
caps.handback.revision: 8
author: "stevehoag"
ms.author: "shoag"
manager: "wpickett"
---
# 형식 매개 변수에 사용된 &#39;New&#39;에 인수를 전달할 수 없습니다.
선언 또는 대입문은 제네릭 형식을 호출하고 [New Operator](../Topic/New%20Operator%20\(Visual%20Basic\).md) 제약 조건이 있는 형식 매개 변수에 생성자 인수를 제공합니다.  
  
 형식 매개 변수에 대한 제약 조건 목록에서 해당 형식 매개 변수로 전달된 형식 인수에서 만드는 코드가 액세스할 수 있는, 매개 변수 없는 생성자를 노출하도록 지정할 수 있습니다. 형식 매개 변수는 매개 변수를 사용하는 생성자를 요구할 수 없으며 `New` 제약 조건이 있는 형식 매개 변수에서는 이러한 생성자를 사용할 수 없습니다.  
  
 **오류 ID:** BC32085  
  
### 이 오류를 해결하려면  
  
-   제네릭 형식을 호출하는 문에서 형식 인수 뒤의 인수 목록을 제거합니다. 해당 형식 매개 변수로 생성자 인수를 전달할 수 없습니다.  
  
## 참고 항목  
 [Visual Basic의 제네릭 형식](../Topic/Generic%20Types%20in%20Visual%20Basic%20\(Visual%20Basic\).md)   
 [Value Types and Reference Types](../Topic/Value%20Types%20and%20Reference%20Types.md)