---
title: "컴파일러 오류 C2952 | Microsoft Docs"
ms.custom: 
ms.date: 11/04/2016
ms.reviewer: 
ms.suite: 
ms.technology: cpp-tools
ms.tgt_pltfrm: 
ms.topic: article
f1_keywords: C2952
dev_langs: C++
helpviewer_keywords: C2952
ms.assetid: a40e18a2-d02c-4511-854f-6c6fd6789a1a
caps.latest.revision: "9"
author: corob-msft
ms.author: corob
manager: ghogen
ms.workload: cplusplus
ms.openlocfilehash: f22e10659611e4a418541894aebef6e14d26dbd8
ms.sourcegitcommit: 8fa8fdf0fbb4f57950f1e8f4f9b81b4d39ec7d7a
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 12/21/2017
---
# <a name="compiler-error-c2952"></a>컴파일러 오류 C2952
'declaration': 형식 선언에 템플릿 매개 변수 목록이 없습니다.  
  
 템플릿 선언의 형식이 잘못되었습니다.  
  
 다음 샘플에서는 C2952를 생성합니다.  
  
```  
// C2952.cpp  
// compile with: /c  
template <class T>  
struct S {  
   template <class T1>  
   struct S1 {  
      void f();  
   };  
};  
  
template <class T> void S<T>::S1<T>::f() {}   // C2952  
  
// OK  
template <class T>  
template <class T1>  
void S<T>::S1<T1>::f() {}  
```  
  
 C2952는 제네릭을 사용하는 경우에도 발생할 수 있습니다.  
  
```  
// C2952b.cpp  
// compile with: /clr /c  
generic <class T>   
ref struct GC {  
   generic <class T1>   
   ref struct GC1 {  
      void f();  
   };  
};  
  
generic <class T> void GC<T>::GC1<T>::f() {}   // C2952  
  
// OK  
generic <class T>  
generic <class T1>  
void GC<T>::GC1<T1>::f() {}  
```