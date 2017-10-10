---
title: "컴파일러 오류 C2761 | Microsoft Docs"
ms.custom: 
ms.date: 11/04/2016
ms.reviewer: 
ms.suite: 
ms.technology:
- cpp-tools
ms.tgt_pltfrm: 
ms.topic: error-reference
f1_keywords:
- C2761
dev_langs:
- C++
helpviewer_keywords:
- C2761
ms.assetid: 38c79a05-b56d-485b-820f-95e8c0cb926f
caps.latest.revision: 9
author: corob-msft
ms.author: corob
manager: ghogen
ms.translationtype: MT
ms.sourcegitcommit: 35b46e23aeb5f4dbfd2a0dd44b906389dd5bfc88
ms.openlocfilehash: 7670c3fa67579c218024dfd3f1f585ad57cf37e5
ms.contentlocale: ko-kr
ms.lasthandoff: 10/10/2017

---
# <a name="compiler-error-c2761"></a>컴파일러 오류 C2761
'function': 멤버 함수를 재선언 할 수 없습니다  
  
 멤버 함수를 다시 선언할 수 없습니다. 정의할 수 있지만 하지 다시 선언할 수 있습니다.  
  
## <a name="example"></a>예제  
 다음 샘플에서는 C2761 오류가 발생 합니다.  
  
```  
// C2761.cpp  
class a {  
   int t;  
   void test();  
};  
  
void a::a;     // C2761  
void a::test;  // C2761  
  
```  
  
## <a name="example"></a>예제  
 클래스 또는 구조체의 비정적 멤버를 정의할 수 없습니다.  다음 샘플에서는 C2761 오류가 발생 합니다.  
  
```  
// C2761_b.cpp  
// compile with: /c  
struct C {  
   int s;  
   static int t;  
};  
  
int C::s;   // C2761  
int C::t;   // OK  
```
