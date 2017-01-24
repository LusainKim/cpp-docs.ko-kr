---
title: "unary_negate(STL/CLR) | Microsoft Docs"
ms.custom: ""
ms.date: "12/03/2016"
ms.prod: "visual-studio-dev14"
ms.reviewer: ""
ms.suite: ""
ms.technology: 
  - "devlang-cpp"
ms.tgt_pltfrm: ""
ms.topic: "reference"
f1_keywords: 
  - "cliext::unary_negate"
dev_langs: 
  - "C++"
helpviewer_keywords: 
  - "unary_negate 함수[STL/CLR]"
ms.assetid: 83bbdd86-199c-4451-9f70-72f9ade2264a
caps.latest.revision: 17
caps.handback.revision: 15
author: "mikeblome"
ms.author: "mblome"
manager: "ghogen"
---
# unary_negate(STL/CLR)
[!INCLUDE[vs2017banner](../assembler/inline/includes/vs2017banner.md)]

The template class describes a functor that, when called, returns the logical NOT of its stored one\-argument functor.  You use it specify a function object in terms of its stored functor.  
  
## 구문  
  
```  
template<typename Fun>  
    ref class unary_negate  
    { // wrap operator()  
public:  
    typedef Fun stored_function_type;  
    typedef typename Fun::argument_type argument_type;  
    typedef bool result_type;  
    typedef Microsoft::VisualC::StlClr::UnaryDelegate<  
        argument_type, result_type>  
        delegate_type;  
  
    unary_negate(Fun% functor);  
    unary_negate(unary_negate<Fun>% right);  
  
    result_type operator()(argument_type left);  
    operator delegate_type^();  
    };  
```  
  
#### 매개 변수  
 Fun  
 The type of the stored functor.  
  
## 멤버 함수  
  
|Type Definition|설명|  
|---------------------|--------|  
|argument\_type|The type of the functor argument.|  
|delegate\_type|The type of the generic delegate.|  
|result\_type|The type of the functor result.|  
  
|멤버|설명|  
|--------|--------|  
|unary\_negate|Constructs the functor.|  
  
|연산자|설명|  
|---------|--------|  
|operator\(\)|Computes the desired function.|  
|delegate\_type^|Casts the functor to a delegate.|  
  
## 설명  
 The template class describes a one\-argument functor that stores another one\-argument functor.  It defines the member operator `operator()` so that, when the object is called as a function, it returns the logical NOT of the stored functor called with the argument.  
  
 You can also pass the object as a function argument whose type is `delegate_type^` and it will be converted appropriately.  
  
## 예제  
  
```  
// cliext_unary_negate.cpp   
// compile with: /clr   
#include <cliext/algorithm>   
#include <cliext/functional>   
#include <cliext/vector>   
  
typedef cliext::vector<int> Myvector;   
int main()   
    {   
    Myvector c1;   
    c1.push_back(4);   
    c1.push_back(0);   
    Myvector c3(2, 0);   
  
// display initial contents " 4 0"   
    for each (int elem in c1)   
        System::Console::Write(" {0}", elem);   
    System::Console::WriteLine();   
  
// transform and display   
    cliext::logical_not<int> not_op;   
  
    cliext::transform(c1.begin(), c1.begin() + 2, c3.begin(),   
        cliext::unary_negate<cliext::logical_not<int> >(not_op));   
    for each (int elem in c3)   
        System::Console::Write(" {0}", elem);   
    System::Console::WriteLine();   
  
// transform and display with function   
    cliext::transform(c1.begin(), c1.begin() + 2, c3.begin(),   
        cliext::not1(not_op));   
    for each (int elem in c3)   
        System::Console::Write(" {0}", elem);   
    System::Console::WriteLine();   
    return (0);   
    }  
  
```  
  
  **4 0**  
 **1 0**  
 **1 0**   
## 요구 사항  
 **Header:** \<cliext\/functional\>  
  
 **Namespace:** cliext  
  
## 참고 항목  
 [not1](../dotnet/not1-stl-clr.md)