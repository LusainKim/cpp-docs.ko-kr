---
title: "컴파일러 오류 CS1575 | Microsoft Docs"
ms.custom: ""
ms.date: "11/16/2016"
ms.prod: "visual-studio-dev14"
ms.reviewer: ""
ms.suite: ""
ms.technology: 
  - "devlang-csharp"
ms.tgt_pltfrm: ""
ms.topic: "article"
f1_keywords: 
  - "CS1575"
dev_langs: 
  - "CSharp"
helpviewer_keywords: 
  - "CS1575"
ms.assetid: 76a9c57c-8f79-482e-9ae8-c70e8f199dd7
caps.latest.revision: 7
caps.handback.revision: 7
author: "BillWagner"
ms.author: "wiwagn"
manager: "wpickett"
---
# 컴파일러 오류 CS1575
stackalloc 식에서 형식 뒤에는 \[\]가 있어야 합니다.  
  
 [stackalloc](../Topic/stackalloc%20\(C%23%20Reference\).md)를 사용하여 요청된 할당의 크기를 대괄호 안에 지정해야 합니다.  
  
 다음 샘플에서는 CS1575를 생성합니다.  
  
```  
// CS1575.cs // compile with: /unsafe public class MyClass { unsafe public static void Main() { int *p = stackalloc int (30);   // CS1575 // try the following line instead // int *p = stackalloc int [30]; } }  
```