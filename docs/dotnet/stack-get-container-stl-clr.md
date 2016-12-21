---
title: "stack::get_container(STL/CLR) | Microsoft Docs"
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
  - "cliext::stack::get_container"
dev_langs: 
  - "C++"
helpviewer_keywords: 
  - "get_container 멤버[STL/CLR]"
ms.assetid: ba6fc541-fc18-4d1c-8e3f-6baaed427cbb
caps.latest.revision: 15
caps.handback.revision: 13
author: "mikeblome"
ms.author: "mblome"
manager: "ghogen"
---
# stack::get_container(STL/CLR)
[!INCLUDE[vs2017banner](../assembler/inline/includes/vs2017banner.md)]

기본 컨테이너에 액세스합니다.  
  
## 구문  
  
```  
container_type^ get_container();  
```  
  
## 설명  
 The member function returns a handle for underlying container.  You use it to bypass the restrictions imposed by the container wrapper.  
  
## 예제  
  
```  
// cliext_stack_get_container.cpp   
// compile with: /clr   
#include <cliext/stack>   
  
typedef cliext::stack<wchar_t> Mystack;   
int main()   
    {   
    Mystack c1;   
    c1.push(L'a');   
    c1.push(L'b');   
    c1.push(L'c');   
  
// display contents " a b c" using container_type   
    Mystack::container_type wc1 = c1.get_container();   
    for each (wchar_t elem in wc1)   
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
 [stack::container\_type](../dotnet/stack-container-type-stl-clr.md)