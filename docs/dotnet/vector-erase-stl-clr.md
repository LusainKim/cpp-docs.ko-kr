---
title: "vector::erase(STL/CLR) | Microsoft Docs"
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
  - "cliext::vector::erase"
dev_langs: 
  - "C++"
helpviewer_keywords: 
  - "erase 멤버[STL/CLR]"
ms.assetid: 624905eb-83c0-499b-a07a-c10aebd7acc3
caps.latest.revision: 17
caps.handback.revision: 15
author: "mikeblome"
ms.author: "mblome"
manager: "ghogen"
---
# vector::erase(STL/CLR)
[!INCLUDE[vs2017banner](../assembler/inline/includes/vs2017banner.md)]

지정된 위치에 있는 요소를 제거합니다.  
  
## 구문  
  
```  
iterator erase(iterator where);  
iterator erase(iterator first, iterator last);  
```  
  
#### 매개 변수  
 first  
 Beginning of range to erase.  
  
 last  
 End of range to erase.  
  
 where  
 Element to erase.  
  
## 설명  
 The first member function removes the element of the controlled sequence pointed to by `where`.  You use it to remove a single element.  
  
 The second member function removes the elements of the controlled sequence in the range `[``first``,` `last``)`.  You use it to remove zero or more contiguous elements.  
  
 Both member functions return an iterator that designates the first element remaining beyond any elements removed, or [vector::end](../dotnet/vector-end-stl-clr.md)`()` if no such element exists.  
  
 When erasing elements, the number of element copies is linear in the number of elements between the end of the erasure and the nearer end of the sequence. \(When erasing one or more elements at either end of the sequence, no element copies occur.\)  
  
## 예제  
  
```  
// cliext_vector_erase.cpp   
// compile with: /clr   
#include <cliext/vector>   
  
int main()   
    {   
    cliext::vector<wchar_t> c1;   
    c1.push_back(L'a');   
    c1.push_back(L'b');   
    c1.push_back(L'c');   
  
// display initial contents " a b c"   
    for each (wchar_t elem in c1)   
        System::Console::Write(" {0}", elem);   
    System::Console::WriteLine();   
  
// erase an element and reinspect   
    System::Console::WriteLine("erase(begin()) = {0}",   
        *c1.erase(c1.begin()));   
  
// add elements and display " b c d e"   
    c1.push_back(L'd');   
    c1.push_back(L'e');   
    for each (wchar_t elem in c1)   
        System::Console::Write(" {0}", elem);   
    System::Console::WriteLine();   
  
// erase all but end   
    cliext::vector<wchar_t>::iterator it = c1.end();   
    System::Console::WriteLine("erase(begin(), end()-1) = {0}",   
        *c1.erase(c1.begin(), --it));   
    System::Console::WriteLine("size() = {0}", c1.size());   
    return (0);   
    }  
  
```  
  
  **a b c**  
**erase\(begin\(\)\) \= b**  
 **b c d e**  
**erase\(begin\(\), end\(\)\-1\) \= e**  
**size\(\) \= 1**   
## 요구 사항  
 **Header:** \<cliext\/vector\>  
  
 **Namespace:** cliext  
  
## 참고 항목  
 [vector](../dotnet/vector-stl-clr.md)   
 [vector::clear](../dotnet/vector-clear-stl-clr.md)