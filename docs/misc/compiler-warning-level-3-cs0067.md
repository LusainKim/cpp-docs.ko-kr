---
title: "컴파일러 경고(수준 3) CS0067 | Microsoft Docs"
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
  - "CS0067"
dev_langs: 
  - "CSharp"
helpviewer_keywords: 
  - "CS0067"
ms.assetid: df75220b-0b93-45ec-8655-98d9333b0bb7
caps.latest.revision: 7
caps.handback.revision: 7
author: "BillWagner"
ms.author: "wiwagn"
manager: "wpickett"
---
# 컴파일러 경고(수준 3) CS0067
'event' 이벤트는 사용되지 않습니다.  
  
 [event](../Topic/event%20\(C%23%20Reference\).md)가 선언되었지만 선언된 클래스에서 사용되지 않았습니다.  
  
 다음 샘플에서는 CS0067을 생성합니다.  
  
```  
// CS0067.cs // compile with: /W:3 using System; delegate void MyDelegate(); class MyClass { public event MyDelegate evt;   // CS0067 // uncomment TestMethod to resolve this CS0067 /* private void TestMethod() { if (evt != null) evt(); } */ public static void Main() { } }  
```