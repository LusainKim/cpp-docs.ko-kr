---
title: "bad_cast 예외 | Microsoft Docs"
ms.custom: 
ms.date: 11/04/2016
ms.reviewer: 
ms.suite: 
ms.technology: cpp-language
ms.tgt_pltfrm: 
ms.topic: language-reference
f1_keywords:
- bad_cast
- bad_cast_cpp
dev_langs: C++
helpviewer_keywords:
- exceptions [C++], bad_cast
- bad_cast keyword [C++]
ms.assetid: 31eae1e7-d8d5-40a0-9fef-64a6a4fc9021
caps.latest.revision: "9"
author: mikeblome
ms.author: mblome
manager: ghogen
ms.workload: cplusplus
ms.openlocfilehash: d7880a01f247d5dc3cce5a6f247297ef65289367
ms.sourcegitcommit: 8fa8fdf0fbb4f57950f1e8f4f9b81b4d39ec7d7a
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 12/21/2017
---
# <a name="badcast-exception"></a>bad_cast 예외
`bad_cast` 예외는 참조 형식에 대한 실패한 캐스팅 결과로 `dynamic_cast` 연산자가 throw합니다.  
  
## <a name="syntax"></a>구문  
  
```  
catch (bad_cast)  
   statement  
```  
  
## <a name="remarks"></a>설명  
 `bad_cast`의 인터페이스는 다음과 같습니다.  
  
```  
class bad_cast : public exception {  
public:  
   bad_cast(const char * _Message = "bad cast");  
   bad_cast(const bad_cast &);  
   virtual ~bad_cast();  
};  
```  
  
 다음 코드에는 `dynamic_cast` 예외를 throw하는 실패한 `bad_cast`의 예제가 포함되어 있습니다.  
  
```  
// expre_bad_cast_Exception.cpp  
// compile with: /EHsc /GR  
#include <typeinfo.h>  
#include <iostream>  
  
class Shape {  
public:  
   virtual void virtualfunc() const {}  
};  
  
class Circle: public Shape {  
public:  
   virtual void virtualfunc() const {}  
};  
  
using namespace std;  
int main() {  
   Shape shape_instance;  
   Shape& ref_shape = shape_instance;  
   try {  
      Circle& ref_circle = dynamic_cast<Circle&>(ref_shape);   
   }  
   catch (bad_cast b) {  
      cout << "Caught: " << b.what();  
   }  
}  
```  
  
 캐스팅될 개체(모양)가 지정된 캐스트 형식(원)에서 파생되지 않으므로 예외가 throw됩니다. 예외를 방지하려면 `main`에 다음과 같은 선언을 추가합니다.  
  
```  
Circle circle_instance;  
Circle& ref_circle = circle_instance;  
```  
  
 그리고 나서 다음과 같이 `try` 블록의 캐스트 감각을 반전시킵니다.  
  
```  
Shape& ref_shape = dynamic_cast<Shape&>(ref_circle);  
```  
  
## <a name="see-also"></a>참고 항목  
 [dynamic_cast 연산자](../cpp/dynamic-cast-operator.md)   
 [키워드](../cpp/keywords-cpp.md)   
 [C++ 예외 처리](../cpp/cpp-exception-handling.md)