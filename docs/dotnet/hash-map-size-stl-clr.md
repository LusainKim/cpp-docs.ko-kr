---
title: "hash_map::size(STL/CLR) | Microsoft Docs"
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
  - "cliext::hash_map::size"
dev_langs: 
  - "C++"
helpviewer_keywords: 
  - "size 멤버[STL/CLR]"
ms.assetid: 5eb91502-1b11-4703-b473-eb609c181b74
caps.latest.revision: 16
caps.handback.revision: 14
author: "mikeblome"
ms.author: "mblome"
manager: "ghogen"
---
# hash_map::size(STL/CLR)
[!INCLUDE[vs2017banner](../assembler/inline/includes/vs2017banner.md)]

요소의 수를 셉니다.  
  
## 구문  
  
```  
size_type size();  
```  
  
## 설명  
 The member function returns the length of the controlled sequence.  You use it to determine the number of elements currently in the controlled sequence.  If all you care about is whether the sequence has nonzero size, see [hash\_map::empty](../dotnet/hash-map-empty-stl-clr.md)`()`.  
  
## 예제  
  
```  
// cliext_hash_map_size.cpp   
// compile with: /clr   
#include <cliext/hash_map>   
  
typedef cliext::hash_map<wchar_t, int> Myhash_map;   
int main()   
    {   
    Myhash_map c1;   
    c1.insert(Myhash_map::make_value(L'a', 1));   
    c1.insert(Myhash_map::make_value(L'b', 2));   
    c1.insert(Myhash_map::make_value(L'c', 3));   
  
// display contents " [a 1] [b 2] [c 3]"   
    for each (Myhash_map::value_type elem in c1)   
        System::Console::Write(" [{0} {1}]", elem->first, elem->second);   
    System::Console::WriteLine();   
  
// clear the container and reinspect   
    c1.clear();   
    System::Console::WriteLine("size() = {0} after clearing", c1.size());   
  
// add elements and clear again   
    c1.insert(Myhash_map::make_value(L'd', 4));   
    c1.insert(Myhash_map::make_value(L'e', 5));   
    System::Console::WriteLine("size() = {0} after adding 2", c1.size());   
    return (0);   
    }  
  
```  
  
  **\[a 1\] \[b 2\] \[c 3\]**  
**size\(\) \= 0 after clearing**  
**size\(\) \= 2 after adding 2**   
## 요구 사항  
 **Header:** \<cliext\/hash\_map\>  
  
 **Namespace:** cliext  
  
## 참고 항목  
 [hash\_map](../dotnet/hash-map-stl-clr.md)   
 [hash\_map::empty](../dotnet/hash-map-empty-stl-clr.md)