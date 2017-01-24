---
title: "컴파일러 오류 CS0206 | Microsoft Docs"
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
  - "CS0206"
dev_langs: 
  - "CSharp"
helpviewer_keywords: 
  - "CS0206"
ms.assetid: d2f9838a-d8ae-4342-b8bd-fa5745619a26
caps.latest.revision: 8
caps.handback.revision: 8
author: "BillWagner"
ms.author: "wiwagn"
manager: "wpickett"
---
# 컴파일러 오류 CS0206
속성 또는 인덱서는 out 또는 ref 매개 변수로 전달할 수 없습니다.  
  
 [속성](../Topic/Properties%20\(C%23%20Programming%20Guide\).md)을 [ref](../Topic/ref%20\(C%23%20Reference\).md) 또는 [out](../Topic/out%20\(C%23%20Reference\).md) 매개 변수로 전달할 수 없습니다. 자세한 내용은 [매개 변수 전달](../Topic/Passing%20Parameters%20\(C%23%20Programming%20Guide\).md)을 참조하세요.  
  
## 예제  
 다음 샘플에서는 CS0206을 생성합니다.  
  
```  
// CS0206.cs public class MyClass { public static int P { get { return 0; } set { } } public static void MyMeth(ref int i) // public static void MyMeth(int i) { } public static void Main() { MyMeth(ref P);   // CS0206 // try the following line instead // MyMeth(P);   // CS0206 } }  
```