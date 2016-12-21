---
title: "컴파일러 오류 CS0072 | Microsoft Docs"
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
  - "CS0072"
dev_langs: 
  - "CSharp"
helpviewer_keywords: 
  - "CS0072"
ms.assetid: 9153cd52-f497-4128-a11f-a2820218b0e6
caps.latest.revision: 8
caps.handback.revision: 8
author: "BillWagner"
ms.author: "wiwagn"
manager: "wpickett"
---
# 컴파일러 오류 CS0072
'event': 재정의할 수 없습니다. 'method'가 이벤트가 아닙니다.  
  
 [event](../Topic/event%20\(C%23%20Reference\).md)는 다른 이벤트만 재정의할 수 있습니다. 자세한 내용은 [이벤트](../Topic/Events%20\(C%23%20Programming%20Guide\).md)을 참조하세요.  
  
 다음 샘플에서는 CS0072를 생성합니다.  
  
```  
// CS0072.cs delegate void MyDelegate(); class Test1 { public virtual event MyDelegate MyEvent; public virtual void VMeth() { } public void FireAway() { if (MyEvent != null) MyEvent(); } } class Test2 : Test1 { public override event MyDelegate VMeth   // CS0072 // uncomment the following lines to resolve // public override event MyDelegate MyEvent { add { VMeth += value; // MyEvent += value; } remove { VMeth -= value; // MyEvent -= value; } } public static void Main() { } }  
```