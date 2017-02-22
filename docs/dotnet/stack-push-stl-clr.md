---
title: "stack::push(STL/CLR) | Microsoft Docs"
ms.custom: ""
ms.date: "11/04/2016"
ms.reviewer: ""
ms.suite: ""
ms.technology: 
  - "devlang-cpp"
ms.tgt_pltfrm: ""
ms.topic: "reference"
f1_keywords: 
  - "cliext::stack::push"
dev_langs: 
  - "C++"
helpviewer_keywords: 
  - "push 멤버[STL/CLR]"
ms.assetid: 60e5b076-c80f-4af0-a018-62cda7e081db
caps.latest.revision: 15
author: "mikeblome"
ms.author: "mblome"
manager: "ghogen"
caps.handback.revision: 13
---
# stack::push(STL/CLR)
[!INCLUDE[vs2017banner](../assembler/inline/includes/vs2017banner.md)]

Adds a new last element.  
  
## 구문  
  
```  
void push(value_type val);  
```  
  
## 설명  
 The member function inserts an element with value `val` at the end of the controlled sequence.  You use it to append another element to the stack.  
  
## 예제  
  
```  
// cliext_stack_push.cpp   
// compile with: /clr   
#include <cliext/stack>   
  
typedef cliext::stack<wchar_t> Mystack;   
int main()   
    {   
    Mystack c1;   
    c1.push(L'a');   
    c1.push(L'b');   
    c1.push(L'c');   
  
// display contents " a b c"   
    for each (wchar_t elem in c1.get_container())   
        System::Console::Write(" {0}", elem);   
    System::Console::WriteLine();   
    return (0);   
    }  
  
```  
  
  **a b c**   
## 요구 사항  
 **Header:** \<cliext\/stack\>  
  
 **Namespace:** cliext  
  
## 참고 항목  
 [stack](../dotnet/stack-stl-clr.md)   
 [stack::pop](../dotnet/stack-pop-stl-clr.md)