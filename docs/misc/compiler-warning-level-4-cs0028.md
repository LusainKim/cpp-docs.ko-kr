---
title: "컴파일러 경고(수준 4) CS0028 | Microsoft Docs"
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
  - "CS0028"
dev_langs: 
  - "CSharp"
helpviewer_keywords: 
  - "CS0028"
ms.assetid: 47df919f-01fa-45ae-a4b7-912445e679e2
caps.latest.revision: 15
caps.handback.revision: 15
author: "BillWagner"
ms.author: "wiwagn"
manager: "wpickett"
---
# 컴파일러 경고(수준 4) CS0028
'function declaration'의 서명이 잘못되어 진입점이 될 수 없습니다.  
  
 `Main`에 대한 메서드 선언이 잘못되었습니다. 잘못된 서명으로 선언되었습니다.`Main`을 정적으로 선언해야 하며, [int](../Topic/int%20\(C%23%20Reference\).md) 또는 [void](../Topic/void%20\(C%23%20Reference\).md)를 반환해야 합니다. 자세한 내용은 [Main\(\)과 명령줄 인수](../Topic/Main\(\)%20and%20Command-Line%20Arguments%20\(C%23%20Programming%20Guide\).md)을 참조하세요.  
  
 다음 샘플에서는 CS0028을 생성합니다.  
  
```  
// CS0028.cs // compile with: /W:4 /warnaserror public class a { public static double Main(int i)   // CS0028 // Try the following line instead: // public static void Main() { } }  
```