---
title: "컴파일러 오류 C2805 | Microsoft Docs"
ms.custom: 
ms.date: 11/04/2016
ms.reviewer: 
ms.suite: 
ms.technology:
- cpp-tools
ms.tgt_pltfrm: 
ms.topic: error-reference
f1_keywords:
- C2805
dev_langs:
- C++
helpviewer_keywords:
- C2805
ms.assetid: c997dc56-e199-442f-b94e-ac551ec9b015
caps.latest.revision: 8
author: corob-msft
ms.author: corob
manager: ghogen
ms.translationtype: MT
ms.sourcegitcommit: 35b46e23aeb5f4dbfd2a0dd44b906389dd5bfc88
ms.openlocfilehash: 6c314f93f9933fa20051aad91442a2d1ac00b9da
ms.contentlocale: ko-kr
ms.lasthandoff: 10/10/2017

---
# <a name="compiler-error-c2805"></a>컴파일러 오류 C2805
이진 파일 '연산자'에 매개 변수가 너무 적습니다.  
  
 이항 연산자에 매개 변수가 없습니다.  
  
 다음 샘플에서는 C2805 오류가 생성 됩니다.  
  
```  
// C2805.cpp  
// compile with: /c  
class X {  
public:  
   X operator< ( void );   // C2805 must take one parameter  
   X operator< ( X );   // OK  
};  
```
