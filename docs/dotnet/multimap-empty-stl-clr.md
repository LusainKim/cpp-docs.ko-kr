---
title: "multimap::empty(STL/CLR) | Microsoft Docs"
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
  - "cliext::multimap::empty"
dev_langs: 
  - "C++"
helpviewer_keywords: 
  - "empty 멤버[STL/CLR]"
ms.assetid: 6214279b-289a-4843-a52a-2034667a2ba3
caps.latest.revision: 17
caps.handback.revision: 15
author: "mikeblome"
ms.author: "mblome"
manager: "ghogen"
---
# multimap::empty(STL/CLR)
[!INCLUDE[vs2017banner](../assembler/inline/includes/vs2017banner.md)]

Tests whether no elements are present.  
  
## 구문  
  
```  
bool empty();  
```  
  
## 설명  
 The member function returns true for an empty controlled sequence.  It is equivalent to [multimap::size](../dotnet/multimap-size-stl-clr.md)`() == 0`.  You use it to test whether the multimap is empty.  
  
## 예제  
  
```  
// cliext_multimap_empty.cpp   
// compile with: /clr   
#include <cliext/map>   
  
typedef cliext::multimap<wchar_t, int> Mymultimap;   
int main()   
    {   
    Mymultimap c1;   
    c1.insert(Mymultimap::make_value(L'a', 1));   
    c1.insert(Mymultimap::make_value(L'b', 2));   
    c1.insert(Mymultimap::make_value(L'c', 3));   
  
// display contents " [a 1] [b 2] [c 3]"   
    for each (Mymultimap::value_type elem in c1)   
        System::Console::Write(" [{0} {1}]", elem->first, elem->second);   
    System::Console::WriteLine();   
    System::Console::WriteLine("size() = {0}", c1.size());   
    System::Console::WriteLine("empty() = {0}", c1.empty());   
  
// clear the container and reinspect   
    c1.clear();   
    System::Console::WriteLine("size() = {0}", c1.size());   
    System::Console::WriteLine("empty() = {0}", c1.empty());   
    return (0);   
    }  
  
```  
  
  **\[a 1\] \[b 2\] \[c 3\]**  
**size\(\) \= 3**  
**empty\(\) \= False**  
**size\(\) \= 0**  
**empty\(\) \= True**   
## 요구 사항  
 **Header:** \<cliext\/map\>  
  
 **Namespace:** cliext  
  
## 참고 항목  
 [multimap](../dotnet/multimap-stl-clr.md)   
 [multimap::size](../dotnet/multimap-size-stl-clr.md)