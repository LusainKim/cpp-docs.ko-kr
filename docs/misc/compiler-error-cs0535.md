---
title: "컴파일러 오류 CS0535 | Microsoft Docs"
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
  - "CS0535"
dev_langs: 
  - "CSharp"
helpviewer_keywords: 
  - "CS0535"
ms.assetid: 282ed5d6-acb7-445b-999f-27a973ccc0b5
caps.latest.revision: 9
caps.handback.revision: 9
author: "BillWagner"
ms.author: "wiwagn"
manager: "wpickett"
---
# 컴파일러 오류 CS0535
'class'는 'member' 인터페이스 멤버를 구현하지 않습니다.  
  
 [클래스](../Topic/class%20\(C%23%20Reference\).md)가 [인터페이스](../Topic/interface%20\(C%23%20Reference\).md)에서 파생되었지만 해당 클래스가 인터페이스 멤버를 하나 이상 구현하지 않았습니다. 클래스는 클래스가 파생된 인터페이스의 모든 멤버를 구현하거나 `abstract`로 선언되어야 합니다.  
  
## 예제  
 다음 샘플에서는 CS0535를 생성합니다.  
  
```  
// CS0535.cs public interface A { void F(); } public class B : A {}   // CS0535 A::F is not implemented // OK public class C : A { public void F() {} public static void Main() {} }  
```  
  
## 예제  
 다음 샘플에서는 CS0535를 생성합니다.  
  
```  
// CS0535_b.cs using System; class C : IDisposable {}   // CS0535 // OK class D : IDisposable { void IDisposable.Dispose() {} public void Dispose() {} static void Main() { using (D d = new D()) {} } }  
```