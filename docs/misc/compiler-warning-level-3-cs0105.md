---
title: "컴파일러 경고(수준 3) CS0105 | Microsoft Docs"
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
  - "CS0105"
dev_langs: 
  - "CSharp"
helpviewer_keywords: 
  - "CS0105"
ms.assetid: 96d1d5d7-79e9-424f-bbde-f87e88b70003
caps.latest.revision: 7
caps.handback.revision: 7
author: "BillWagner"
ms.author: "wiwagn"
manager: "wpickett"
---
# 컴파일러 경고(수준 3) CS0105
'namespace'에 대한 using 지시문을 이미 이 네임스페이스에서 사용했습니다.  
  
 한 번만 선언해야 하는 [네임스페이스](../Topic/namespace%20\(C%23%20Reference\).md)가 두 번 이상 선언되었습니다. 중복된 네임스페이스 선언을 모두 제거합니다.  
  
 다음 샘플에서는 CS0105를 생성합니다.  
  
```  
// CS0105.cs // compile with: /W:3 using System; using System;   // CS0105 public class a { public static void Main() { } }  
```