---
title: "컴파일러 오류 C3212 | Microsoft Docs"
ms.custom: 
ms.date: 11/04/2016
ms.reviewer: 
ms.suite: 
ms.technology:
- cpp-tools
ms.tgt_pltfrm: 
ms.topic: article
f1_keywords:
- C3212
dev_langs:
- C++
helpviewer_keywords:
- C3212
ms.assetid: 9e271bb6-a51f-4b96-b26b-9f4ca28fca0a
caps.latest.revision: 6
author: corob-msft
ms.author: corob
manager: ghogen
ms.translationtype: MT
ms.sourcegitcommit: 35b46e23aeb5f4dbfd2a0dd44b906389dd5bfc88
ms.openlocfilehash: e7534a3a05366eb866c67c500ed946d838732e95
ms.contentlocale: ko-kr
ms.lasthandoff: 10/10/2017

---
# <a name="compiler-error-c3212"></a>컴파일러 오류 C3212
'specialization': 템플릿 멤버의 명시적 특수화는 명시적 특수화의 멤버여야 합니다.  
  
 명시적 특수화의 형식이 잘못되었습니다.  
  
 다음 샘플에서는 C3212를 생성합니다.  
  
```  
// C3212.cpp  
// compile with: /LD  
template <class T>  
struct S {  
   template <class T1>  
   struct S1;  
};  
  
template <class T>   // C3212  
template <>  
struct S<T>::S1<int> {};  
  
/*  
// try the following instead  
template <>  
template <>  
struct S<int>::S1<int> {};  
*/  
  
/*  
// or, the following  
template <>  
struct S<int> {  
   template <class T1>  
   struct S1;  
};  
  
template <>  
struct S<int>::S1<int> {  
};  
*/  
```
