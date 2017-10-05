---
title: "함수 템플릿의 명시적 특수화 | Microsoft Docs"
ms.custom: 
ms.date: 11/04/2016
ms.reviewer: 
ms.suite: 
ms.technology:
- cpp-language
ms.tgt_pltfrm: 
ms.topic: language-reference
dev_langs:
- C++
helpviewer_keywords:
- overriding, functions
- function templates, specialization
- explicit specialization of function templates
- declaring functions, specialization of function template
- specialization of function templates
ms.assetid: eb0fcb73-eaed-42a1-9b83-14b055a34bf8
caps.latest.revision: 7
author: mikeblome
ms.author: mblome
manager: ghogen
translation.priority.ht:
- cs-cz
- de-de
- es-es
- fr-fr
- it-it
- ja-jp
- ko-kr
- pl-pl
- pt-br
- ru-ru
- tr-tr
- zh-cn
- zh-tw
ms.translationtype: HT
ms.sourcegitcommit: f460497071445cff87308fa9bf6e0d43c6f13a3e
ms.openlocfilehash: c5caabae41383edbdc92806249026ce8a0daa5d5
ms.contentlocale: ko-kr
ms.lasthandoff: 09/25/2017

---
# <a name="explicit-specialization-of-function-templates"></a>함수 템플릿의 명시적 특수화
함수 템플릿을 사용하면 특정 형식에 대한 함수 템플릿의 명시적 특수화(재정의)를 제공하여 해당 형식에 대한 특별한 동작을 정의할 수 있습니다. 예:  
  
```cpp
template<> void MySwap(double a, double b);  
```  
  
 이 선언에 대 한 다른 함수를 정의할 수 있습니다를 사용 하면 **double** 변수입니다. 표준 형식 변환, 비템플릿 함수와 마찬가지로 (형식의 변수 승격 등 **float** 를 **double**) 적용 됩니다.  
  
## <a name="example"></a>예제  
  
```cpp
// explicit_specialization.cpp  
template<class T> void f(T t)  
{  
};  
  
// Explicit specialization of f with 'char' with the  
// template argument explicitly specified:  
//  
template<> void f<char>(char c)  
{  
}  
  
// Explicit specialization of f with 'double' with the  
// template argument deduced:  
//  
template<> void f(double d)  
{  
}  
int main()  
{  
}  
```  
  
## <a name="see-also"></a>참고 항목  
 [함수 템플릿](../cpp/function-templates.md)

