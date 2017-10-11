---
title: "컴파일러 오류 C2835 | Microsoft Docs"
ms.custom: 
ms.date: 11/04/2016
ms.reviewer: 
ms.suite: 
ms.technology:
- cpp-tools
ms.tgt_pltfrm: 
ms.topic: error-reference
f1_keywords:
- C2835
dev_langs:
- C++
helpviewer_keywords:
- C2835
ms.assetid: 41c70630-983f-4da2-8342-513cf48b0519
caps.latest.revision: 7
author: corob-msft
ms.author: corob
manager: ghogen
ms.translationtype: MT
ms.sourcegitcommit: 35b46e23aeb5f4dbfd2a0dd44b906389dd5bfc88
ms.openlocfilehash: 08a09c0ea495fcaff01527b0c4af720f2a831db5
ms.contentlocale: ko-kr
ms.lasthandoff: 10/10/2017

---
# <a name="compiler-error-c2835"></a>컴파일러 오류 C2835
사용자 정의 변환 'type' 형식 매개 변수를 사용합니다.  
  
 사용자 정의 형식 변환 정식 매개 변수를 사용할 수 없습니다.  
  
 다음 샘플에서는 C2835 오류가 생성 됩니다.  
  
```  
// C2835.cpp  
class A {  
public:  
   char v_char;  
  
   A() {   
      v_char = 'A';   
   };  
   operator char(char a) {   // C2835  
   // try the following line instead  
   // operator char() {     
      return v_char + 1;   
   };  
};  
  
int main() {  
   A a;  
}  
```
