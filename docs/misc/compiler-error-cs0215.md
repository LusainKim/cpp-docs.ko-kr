---
title: "컴파일러 오류 CS0215 | Microsoft Docs"
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
  - "CS0215"
dev_langs: 
  - "CSharp"
helpviewer_keywords: 
  - "CS0215"
ms.assetid: 2060440d-be22-4c10-8b26-43b08b615447
caps.latest.revision: 8
caps.handback.revision: 8
author: "BillWagner"
ms.author: "wiwagn"
manager: "wpickett"
---
# 컴파일러 오류 CS0215
True 또는 False 연산자의 반환 형식은 bool이어야 합니다.  
  
 사용자 정의 [true](../Topic/true%20\(C%23%20Reference\).md) 및 [false](../Topic/false%20\(C%23%20Reference\).md) 연산자에 [bool](../Topic/bool%20\(C%23%20Reference\).md)의 반환 형식이 있어야 합니다. 자세한 내용은 [오버로드할 수 있는 연산자](../Topic/Overloadable%20Operators%20\(C%23%20Programming%20Guide\).md)을 참조하세요.  
  
 다음 샘플에서는 CS0215를 생성합니다.  
  
```  
// CS0215.cs class MyClass { public static int operator true (MyClass MyInt)   // CS0215 // try the following line instead // public static bool operator true (MyClass MyInt) { return true; } public static int operator false (MyClass MyInt)   // CS0215 // try the following line instead // public static bool operator false (MyClass MyInt) { return true; } public static void Main() { } }  
```