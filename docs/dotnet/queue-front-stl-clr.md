---
title: "queue::front(STL/CLR) | Microsoft Docs"
ms.custom: ""
ms.date: "11/04/2016"
ms.reviewer: ""
ms.suite: ""
ms.technology: 
  - "devlang-cpp"
ms.tgt_pltfrm: ""
ms.topic: "reference"
f1_keywords: 
  - "cliext::queue::front"
dev_langs: 
  - "C++"
helpviewer_keywords: 
  - "front 멤버[STL/CLR]"
ms.assetid: 9d7bb95f-5896-42f7-86fa-004a7a65cc94
caps.latest.revision: 17
author: "mikeblome"
ms.author: "mblome"
manager: "ghogen"
caps.handback.revision: 15
---
# queue::front(STL/CLR)
[!INCLUDE[vs2017banner](../assembler/inline/includes/vs2017banner.md)]

Accesses the first element.  
  
## 구문  
  
```  
reference front();  
```  
  
## 설명  
 The member function returns a reference to the first element of the controlled sequence, which must be non\-empty.  You use it to access the first element, when you know it exists.  
  
## 예제  
  
```  
// cliext_queue_front.cpp   
// compile with: /clr   
#include <cliext/queue>   
  
typedef cliext::queue<wchar_t> Myqueue;   
int main()   
    {   
    Myqueue c1;   
    c1.push(L'a');   
    c1.push(L'b');   
    c1.push(L'c');   
  
// display initial contents " a b c"   
    for each (wchar_t elem in c1.get_container())   
        System::Console::Write(" {0}", elem);   
    System::Console::WriteLine();   
  
// inspect first item   
    System::Console::WriteLine("front() = {0}", c1.front());   
  
// alter first item and reinspect   
    c1.front() = L'x';   
    for each (wchar_t elem in c1.get_container())   
        System::Console::Write(" {0}", elem);   
    System::Console::WriteLine();   
    return (0);   
    }  
  
```  
  
  **a b c**  
**front\(\) \= a**  
 **x b c**   
## 요구 사항  
 **Header:** \<cliext\/queue\>  
  
 **Namespace:** cliext  
  
## 참고 항목  
 [queue](../dotnet/queue-stl-clr.md)   
 [queue::back](../dotnet/queue-back-stl-clr.md)   
 [queue::back\_item](../dotnet/queue-back-item-stl-clr.md)   
 [queue::front\_item](../dotnet/queue-front-item-stl-clr.md)