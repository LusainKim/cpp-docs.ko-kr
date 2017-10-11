---
title: "컴파일러 오류 C3651 | Microsoft Docs"
ms.custom: 
ms.date: 11/04/2016
ms.reviewer: 
ms.suite: 
ms.technology:
- cpp-tools
ms.tgt_pltfrm: 
ms.topic: error-reference
f1_keywords:
- C3651
dev_langs:
- C++
helpviewer_keywords:
- C3651
ms.assetid: a03e692e-c219-4654-9827-8415cfa5a22d
caps.latest.revision: 10
author: corob-msft
ms.author: corob
manager: ghogen
ms.translationtype: MT
ms.sourcegitcommit: 35b46e23aeb5f4dbfd2a0dd44b906389dd5bfc88
ms.openlocfilehash: 74188570b1a049b6945c183ab950aebbc4ca30a7
ms.contentlocale: ko-kr
ms.lasthandoff: 10/10/2017

---
# <a name="compiler-error-c3651"></a>컴파일러 오류 C3651
'member': 명시적 재정의로 사용할 수 없습니다, 기본 클래스의 멤버 여야 합니다  
  
 명시적 재정의 지정 하지만 기본 형식이 아닌 형식에 재정의 되는 함수입니다.  
  
 자세한 내용은 참조 [명시적으로 재정의](../../windows/explicit-overrides-cpp-component-extensions.md)합니다.  
  
 다음 샘플에서는 C3651 오류가 생성 됩니다.  
  
```  
// C3651.cpp  
// compile with: /clr /c  
ref class C {  
public:  
   virtual void func2();  
};  
  
ref class Other {  
public:  
   virtual void func();  
};  
  
ref class D : public C {  
public:  
   virtual void func() new sealed = Other::func;   // C3651  
   virtual void func2() new sealed = C::func2;   // OK  
};  
```
