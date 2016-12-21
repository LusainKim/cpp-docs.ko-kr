---
title: "컴파일러 오류 CS0159 | Microsoft Docs"
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
  - "CS0159"
dev_langs: 
  - "CSharp"
helpviewer_keywords: 
  - "CS0159"
ms.assetid: 9fde7ffa-aed7-4a9d-8f47-ea67bc9df9e4
caps.latest.revision: 8
caps.handback.revision: 8
author: "BillWagner"
ms.author: "wiwagn"
manager: "wpickett"
---
# 컴파일러 오류 CS0159
goto 문의 범위 내에 'label' 레이블이 없습니다.  
  
 [goto](../Topic/goto%20\(C%23%20Reference\).md) 문에서 참조하는 레이블을 `goto` 문의 범위 내에서 찾을 수 없습니다.  
  
 다음 샘플에서는 CS0159를 생성합니다.  
  
```  
// CS0159.cs public class Class1 { public static void Main() { int i = 0; switch (i) { case 1: goto case 3;   // CS0159, case 3 label does not exist case 2: break; } goto NOWHERE;   // CS0159, NOWHERE label does not exist } }  
```