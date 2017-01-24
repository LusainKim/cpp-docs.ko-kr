---
title: "컴파일러 오류 CS0157 | Microsoft Docs"
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
  - "CS0157"
dev_langs: 
  - "CSharp"
helpviewer_keywords: 
  - "CS0157"
ms.assetid: a5d9d506-81f8-47dd-85b6-85f8170bcbef
caps.latest.revision: 8
caps.handback.revision: 8
author: "BillWagner"
ms.author: "wiwagn"
manager: "wpickett"
---
# 컴파일러 오류 CS0157
제어가 finally 절의 본문을 벗어날 수 없습니다.  
  
 [finally](../Topic/try-catch-finally%20\(C%23%20Reference\).md) 절의 모든 문을 실행해야 합니다. 자세한 내용은 [예외 처리문](../Topic/Exception%20Handling%20Statements%20\(C%23%20Reference\).md) 및 [예외 및 예외 처리](../Topic/Exceptions%20and%20Exception%20Handling%20\(C%23%20Programming%20Guide\).md)를 참조하세요.  
  
 다음 샘플에서는 CS0157을 생성합니다.  
  
```  
// CS0157.cs using System; namespace MyNamespace { public class MyClass2 : Exception { } public class MyClass { public static void Main() { try { } finally { return;   // CS0157, cannot leave finally clause } } } }  
```