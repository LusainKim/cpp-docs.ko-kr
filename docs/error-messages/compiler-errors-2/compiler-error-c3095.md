---
title: "컴파일러 오류 C3095 | Microsoft Docs"
ms.custom: 
ms.date: 11/04/2016
ms.reviewer: 
ms.suite: 
ms.technology:
- cpp-tools
ms.tgt_pltfrm: 
ms.topic: article
f1_keywords:
- C3095
dev_langs:
- C++
helpviewer_keywords:
- C3095
ms.assetid: cde725be-0936-40f6-9e57-e1d7d0710f83
caps.latest.revision: 5
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
ms.translationtype: Machine Translation
ms.sourcegitcommit: 0d9cbb01d1ad0f2ea65d59334cb88140ef18fce0
ms.openlocfilehash: 18b971fb51a6b11763eef0e83ade411f7abf9a97
ms.contentlocale: ko-kr
ms.lasthandoff: 04/12/2017

---
# <a name="compiler-error-c3095"></a>컴파일러 오류 C3095
'attribute': 특성을 반복할 수 없습니다.  
  
 일부 특성이 대상에 특성을 여러 번 적용할 수 없도록 선언되었습니다.  
  
 자세한 내용은 참조 [사용자 정의 특성](../../windows/user-defined-attributes-cpp-component-extensions.md)합니다.  
  
## <a name="example"></a>예제  
 다음 샘플에서는 C3095를 생성합니다.  
  
```  
// C3095.cpp  
// compile with: /clr /c  
using namespace System;  
  
[AttributeUsage(AttributeTargets::All, AllowMultiple=false)]  
public ref class Attr : public Attribute {  
public:  
   Attr(int t) : m_t(t) {}  
   const int m_t;  
};  
  
[AttributeUsage(AttributeTargets::All, AllowMultiple=true)]  
public ref class Attr2 : public Attribute {  
public:  
   Attr2(int t) : m_t(t) {}  
   const int m_t;  
};  
  
[Attr(10)]   // C3095  
[Attr(11)]  
ref class A {};  
  
[Attr2(10)]   // OK  
[Attr2(11)]  
ref class B {};  
```
