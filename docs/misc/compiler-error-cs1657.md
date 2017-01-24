---
title: "컴파일러 오류 CS1657 | Microsoft Docs"
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
  - "CS1657"
dev_langs: 
  - "CSharp"
helpviewer_keywords: 
  - "CS1657"
ms.assetid: 6f0aeebe-5c90-4d5b-981c-1795d2e8fbb9
caps.latest.revision: 9
caps.handback.revision: 9
author: "BillWagner"
ms.author: "wiwagn"
manager: "wpickett"
---
# 컴파일러 오류 CS1657
'parameter'는 'reason'이므로 ref 또는 out 인수로 전달할 수 없습니다.  
  
 이 오류는 변수가 읽기 전용인 컨텍스트에서 [ref](../Topic/ref%20\(C%23%20Reference\).md) 또는 [out](../Topic/out%20\(C%23%20Reference\).md) 인수로 전달되는 경우에 발생합니다. 읽기 전용 컨텍스트에는 [foreach](../Topic/foreach,%20in%20\(C%23%20Reference\).md) 반복 변수, [using](../Topic/using%20Statement%20\(C%23%20Reference\).md) 변수 및 `fixed` 변수가 포함됩니다. 이 오류를 해결하려면 `using` 블록, `foreach` 문 및 `fixed` 문에서 `foreach`, `using` 또는 `fixed` 변수를 `ref` 또는 `out` 매개 변수로 사용하는 함수를 호출하지 마세요.  
  
## 예제  
 다음 샘플에서는 CS1657을 생성합니다.  
  
```  
// CS1657.cs using System; class C : IDisposable { public int i; public void Dispose() {} } class CMain { static void f(ref C c) { } static void Main() { using (C c = new C()) { f(ref c);  // CS1657 } } }  
```  
  
## 예제  
 다음 코드에서는 `fixed` 문의 동일한 문제를 보여 줍니다.  
  
```  
// CS1657b.cs // compile with: /unsafe unsafe class C { static void F(ref int* p) { } static void Main() { int[] a = new int[5]; fixed(int* p = a) F(ref p); // CS1657 } }  
```