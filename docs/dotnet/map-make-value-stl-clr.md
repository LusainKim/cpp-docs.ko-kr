---
title: "map::make_value(STL/CLR) | Microsoft Docs"
ms.custom: ""
ms.date: "11/04/2016"
ms.reviewer: ""
ms.suite: ""
ms.technology: 
  - "devlang-cpp"
ms.tgt_pltfrm: ""
ms.topic: "reference"
f1_keywords: 
  - "cliext::map::make_value"
dev_langs: 
  - "C++"
helpviewer_keywords: 
  - "make_value 멤버[STL/CLR]"
ms.assetid: a0bc4081-b8b7-450e-b041-a49ac42b279f
caps.latest.revision: 15
author: "mikeblome"
ms.author: "mblome"
manager: "ghogen"
caps.handback.revision: 13
---
# map::make_value(STL/CLR)
[!INCLUDE[vs2017banner](../assembler/inline/includes/vs2017banner.md)]

Constructs a value object.  
  
## 구문  
  
```  
static value_type make_value(key_type key, mapped_type mapped);  
```  
  
#### 매개 변수  
 key  
 Key value to use.  
  
 mapped  
 Mapped value to search for.  
  
## 설명  
 The member function returns a `value_type` object whose key is `key` and whose mapped value is `mapped`.  You use it to compose an object suitable for use with several other member functions.  
  
## 예제  
  
```  
// cliext_map_make_value.cpp   
// compile with: /clr   
#include <cliext/map>   
  
typedef cliext::map<wchar_t, int> Mymap;   
int main()   
    {   
    Mymap c1;   
    c1.insert(Mymap::make_value(L'a', 1));   
    c1.insert(Mymap::make_value(L'b', 2));   
    c1.insert(Mymap::make_value(L'c', 3));   
  
// display contents " [a 1] [b 2] [c 3]"   
    for each (Mymap::value_type elem in c1)   
        System::Console::Write(" [{0} {1}]", elem->first, elem->second);   
    System::Console::WriteLine();   
    return (0);   
    }  
  
```  
  
  **\[a 1\] \[b 2\] \[c 3\]**   
## 요구 사항  
 **Header:** \<cliext\/map\>  
  
 **Namespace:** cliext  
  
## 참고 항목  
 [map](../dotnet/map-stl-clr.md)   
 [map::key\_type](../dotnet/map-key-type-stl-clr.md)   
 [map::mapped\_type](../dotnet/map-mapped-type-stl-clr.md)   
 [map::value\_type](../dotnet/map-value-type-stl-clr.md)