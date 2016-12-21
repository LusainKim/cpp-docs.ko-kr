---
title: "컴파일러 경고(수준 3) CS0665 | Microsoft Docs"
ms.custom: ""
ms.date: "11/17/2016"
ms.prod: "visual-studio-dev14"
ms.reviewer: ""
ms.suite: ""
ms.technology: 
  - "devlang-csharp"
ms.tgt_pltfrm: ""
ms.topic: "article"
f1_keywords: 
  - "CS0665"
dev_langs: 
  - "CSharp"
helpviewer_keywords: 
  - "CS0665"
ms.assetid: bddff69b-e74e-45ce-8472-16ee53ae4609
caps.latest.revision: 7
caps.handback.revision: 7
author: "BillWagner"
ms.author: "wiwagn"
manager: "wpickett"
---
# 컴파일러 경고(수준 3) CS0665
조건식에 할당을 사용하면 항상 상수가 됩니다. \= 대신 \=\=을 사용하세요.  
  
 조건식에서 [\=\= 연산자](../Topic/==%20Operator%20\(C%23%20Reference\).md)가 아닌 [\= 연산자](../Topic/=%20Operator%20\(C%23%20Reference\).md)를 사용했습니다.  
  
 다음 샘플에서는 CS0665를 생성합니다.  
  
```  
// CS0665.cs // compile with: /W:3 class Test { public static void Main() { bool i = false; if (i = true)   // CS0665 // try the following line instead // if (i == true) { } System.Console.WriteLine(i); } }  
```