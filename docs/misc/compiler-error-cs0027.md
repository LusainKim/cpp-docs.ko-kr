---
title: "컴파일러 오류 CS0027 | Microsoft Docs"
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
  - "CS0027"
dev_langs: 
  - "CSharp"
helpviewer_keywords: 
  - "CS0027"
ms.assetid: 3a599876-9643-4c68-9457-3306858a73e9
caps.latest.revision: 12
caps.handback.revision: 12
author: "BillWagner"
ms.author: "wiwagn"
manager: "wpickett"
---
# 컴파일러 오류 CS0027
현재 컨텍스트에서는 'this' 키워드를 사용할 수 없습니다.  
  
 속성, 메서드 또는 생성자 외부에서 [this](../Topic/this%20\(C%23%20Reference\).md) 키워드를 발견했습니다.  
  
 이 오류를 해결하려면 `this` 키워드 사용을 제거하도록 문을 수정하거나 일부 또는 전체 문을 속성, 메서드 또는 생성자 내부로 이동합니다.  
  
 다음 예제에서는 CS0027을 생성합니다.  
  
```  
using System; using System.Collections.Generic; using System.Text; namespace ConsoleApplication3 { class MyClass { int err1 = this.Fun() + 1;  // CS0027 public int Fun() { return 10; } public void Test() { // valid use of this int err = this.Fun() + 1; Console.WriteLine(err); } public static void Main() { MyClass c = new MyClass(); c.Test(); } } }  
```