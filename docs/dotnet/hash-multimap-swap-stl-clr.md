---
title: "hash_multimap::swap(STL/CLR) | Microsoft Docs"
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
  - "cliext::hash_multimap::swap"
dev_langs: 
  - "C++"
helpviewer_keywords: 
  - "swap 멤버[STL/CLR]"
ms.assetid: 4baa60c2-865a-4e17-acd5-01b7c3c5cd44
caps.latest.revision: 14
caps.handback.revision: 12
author: "mikeblome"
ms.author: "mblome"
manager: "ghogen"
---
# hash_multimap::swap(STL/CLR)
[!INCLUDE[vs2017banner](../assembler/inline/includes/vs2017banner.md)]

두 컨테이너의 내용을 바꿉니다.  
  
## 구문  
  
```  
void swap(hash_multimap<Key, Mapped>% right);  
```  
  
#### 매개 변수  
 right  
 내용을 바꿀 컨테이너입니다.  
  
## 설명  
 The member function swaps the controlled sequences between `this` and `right`.  It does so in constant time and it throws no exceptions.  You use it as a quick way to exchange the contents of two containers.  
  
## 예제  
  
```  
// cliext_hash_multimap_swap.cpp   
// compile with: /clr   
#include <cliext/hash_map>   
  
typedef cliext::hash_multimap<wchar_t, int> Myhash_multimap;   
int main()   
    {   
    Myhash_multimap c1;   
    c1.insert(Myhash_multimap::make_value(L'a', 1));   
    c1.insert(Myhash_multimap::make_value(L'b', 2));   
    c1.insert(Myhash_multimap::make_value(L'c', 3));   
  
// display contents " [a 1] [b 2] [c 3]"   
    for each (Myhash_multimap::value_type elem in c1)   
        System::Console::Write(" [{0} {1}]", elem->first, elem->second);   
    System::Console::WriteLine();   
  
// construct another container with repetition of values   
    Myhash_multimap c2;   
    c2.insert(Myhash_multimap::make_value(L'd', 4));   
    c2.insert(Myhash_multimap::make_value(L'e', 5));   
    c2.insert(Myhash_multimap::make_value(L'f', 6));   
    for each (Myhash_multimap::value_type elem in c2)   
        System::Console::Write(" [{0} {1}]", elem->first, elem->second);   
    System::Console::WriteLine();   
  
// swap and redisplay   
    c1.swap(c2);   
    for each (Myhash_multimap::value_type elem in c1)   
        System::Console::Write(" [{0} {1}]", elem->first, elem->second);   
    System::Console::WriteLine();   
  
    for each (Myhash_multimap::value_type elem in c2)   
        System::Console::Write(" [{0} {1}]", elem->first, elem->second);   
    System::Console::WriteLine();   
    return (0);   
    }  
  
```  
  
  **\[a 1\] \[b 2\] \[c 3\]**  
 **\[d 4\] \[e 5\] \[f 6\]**  
 **\[d 4\] \[e 5\] \[f 6\]**  
 **\[a 1\] \[b 2\] \[c 3\]**   
## 요구 사항  
 **Header:** \<cliext\/hash\_map\>  
  
 **Namespace:** cliext  
  
## 참고 항목  
 [hash\_multimap](../dotnet/hash-multimap-stl-clr.md)   
 [hash\_multimap::operator\=](../dotnet/hash-multimap-operator-assign-stl-clr.md)