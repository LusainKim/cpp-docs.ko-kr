---
title: "컴파일러 오류 CS1593 | Microsoft Docs"
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
  - "CS1593"
dev_langs: 
  - "CSharp"
helpviewer_keywords: 
  - "CS1593"
ms.assetid: 7476e799-8a8d-457d-b4e7-2d5e073799d8
caps.latest.revision: 7
caps.handback.revision: 7
author: "BillWagner"
ms.author: "wiwagn"
manager: "wpickett"
---
# 컴파일러 오류 CS1593
'del' 대리자는 인수를 'number'개 사용하지 않습니다.  
  
 [delegate](../Topic/delegate%20\(C%23%20Reference\).md) 호출에 전달된 인수 개수가 대리자 선언의 매개 변수 개수에 맞지 않습니다.  
  
 다음 샘플에서는 CS1593을 생성합니다.  
  
```  
// CS1593.cs using System; delegate string func(int i);   // declare delegate class a { public static void Main() { func dt = new func(z); x(dt); } public static string z(int j) { Console.WriteLine(j); return j.ToString(); } public static void x(func hello) { hello(8, 9);   // CS1593 // try the following line instead // hello(8); } }  
```