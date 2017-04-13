---
title: "컴파일러 오류 C2135 | Microsoft Docs"
ms.custom: 
ms.date: 11/04/2016
ms.reviewer: 
ms.suite: 
ms.technology:
- devlang-cpp
ms.tgt_pltfrm: 
ms.topic: article
f1_keywords:
- C2135
dev_langs:
- C++
helpviewer_keywords:
- C2135
ms.assetid: aa360d22-4f79-4de1-b384-93cadd10975f
caps.latest.revision: 9
author: corob-msft
ms.author: corob
manager: ghogen
translation.priority.ht:
- de-de
- es-es
- fr-fr
- it-it
- ja-jp
- ko-kr
- ru-ru
- zh-cn
- zh-tw
translation.priority.mt:
- cs-cz
- pl-pl
- pt-br
- tr-tr
translationtype: Machine Translation
ms.sourcegitcommit: 0d9cbb01d1ad0f2ea65d59334cb88140ef18fce0
ms.openlocfilehash: 068dd861aed4a743ecf2b643b7722d4b35b929fc
ms.lasthandoff: 04/12/2017

---
# <a name="compiler-error-c2135"></a>컴파일러 오류 C2135
'비트 연산자': 비트 필드 연산이 잘못되었습니다.  
  
 address-of 연산자(`&`)는 비트 필드에 적용할 수 없습니다.  
  
 다음 샘플에서는 C2135를 생성합니다.  
  
```  
// C2135.cpp  
struct S {  
   int i : 1;  
};  
  
struct T {  
   int j;  
};  
int main() {  
   &S::i;   // C2135 address of a bit field  
   &T::j;   // OK  
}  
```
