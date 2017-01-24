---
title: "map::equal_range(STL/CLR) | Microsoft Docs"
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
  - "cliext::map::equal_range"
dev_langs: 
  - "C++"
helpviewer_keywords: 
  - "equal_range 멤버[STL/CLR]"
ms.assetid: c0d7409c-344d-4102-99c4-aeab8643a073
caps.latest.revision: 17
caps.handback.revision: 15
author: "mikeblome"
ms.author: "mblome"
manager: "ghogen"
---
# map::equal_range(STL/CLR)
[!INCLUDE[vs2017banner](../assembler/inline/includes/vs2017banner.md)]

Finds range that matches a specified key.  
  
## 구문  
  
```  
cliext::pair<iterator, iterator> equal_range(key_type key);  
```  
  
#### 매개 변수  
 key  
 Key value to search for.  
  
## 설명  
 The member function returns a pair of iterators `cliext::pair<iterator, iterator>(` [map::lower\_bound](../dotnet/map-lower-bound-stl-clr.md)`(``key``),` [map::upper\_bound](../dotnet/map-upper-bound-stl-clr.md)`(``key``))`.  You use it to determine the range of elements currently in the controlled sequence that match a specified key.  
  
## 예제  
  
```  
// cliext_map_equal_range.cpp   
// compile with: /clr   
#include <cliext/map>   
  
typedef cliext::map<wchar_t, int> Mymap;   
typedef Mymap::pair_iter_iter Pairii;   
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
  
// display results of failed search   
    Pairii pair1 = c1.equal_range(L'x');   
    System::Console::WriteLine("equal_range(L'x') empty = {0}",   
        pair1.first == pair1.second);   
  
// display results of successful search   
    pair1 = c1.equal_range(L'b');   
    for (; pair1.first != pair1.second; ++pair1.first)   
        System::Console::Write(" [{0} {1}]",   
            pair1.first->first, pair1.first->second);   
    System::Console::WriteLine();   
    return (0);   
    }  
  
```  
  
  **\[a 1\] \[b 2\] \[c 3\]**  
**equal\_range\(L'x'\) empty \= True**  
 **\[b 2\]**   
## 요구 사항  
 **Header:** \<cliext\/map\>  
  
 **Namespace:** cliext  
  
## 참고 항목  
 [map](../dotnet/map-stl-clr.md)   
 [map::count](../dotnet/map-count-stl-clr.md)   
 [map::find](../dotnet/map-find-stl-clr.md)   
 [map::lower\_bound](../dotnet/map-lower-bound-stl-clr.md)   
 [map::upper\_bound](../dotnet/map-upper-bound-stl-clr.md)