---
title: "인수 없이 고유 조작자 작성 | Microsoft Docs"
ms.custom: ""
ms.date: "11/04/2016"
ms.reviewer: ""
ms.suite: ""
ms.technology: 
  - "devlang-cpp"
ms.tgt_pltfrm: ""
ms.topic: "article"
dev_langs: 
  - "C++"
helpviewer_keywords: 
  - "조작자"
ms.assetid: 2dc62d09-45b7-454d-bd9d-55f3c72c206d
caps.latest.revision: 8
author: "corob-msft"
ms.author: "corob"
manager: "ghogen"
caps.handback.revision: 7
---
# 인수 없이 고유 조작자 작성
[!INCLUDE[vs2017banner](../assembler/inline/includes/vs2017banner.md)]

Writing manipulators that do not use arguments requires neither class derivation nor use of complex macros.  Suppose your printer requires the pair \<ESC\>\[ to enter bold mode.  You can insert this pair directly into the stream:  
  
```  
cout << "regular " << '\033' << '[' << "boldface" << endl;  
```  
  
 Or you can define the `bold` manipulator, which inserts the characters:  
  
```  
ostream& bold( ostream& os ) {  
    return os << '\033' << '[';  
}  
cout << "regular " << bold << "boldface" << endl;  
```  
  
 The globally defined `bold` function takes an `ostream` reference argument and returns the `ostream` reference.  It is not a member function or a friend because it does not need access to any private class elements.  The `bold` function connects to the stream because the stream's `<<` operator is overloaded to accept that type of function, using a declaration that looks something like this:  
  
```  
_Myt& operator<<(ios_base& (__cdecl *_Pfn)(ios_base&))  
{     
   // call ios_base manipulator  
   (*_Pfn)(*(ios_base *)this);  
   return (*this);  
}  
```  
  
 You can use this feature to extend other overloaded operators.  In this case, it is incidental that `bold` inserts characters into the stream.  The function is called when it is inserted into the stream, not necessarily when the adjacent characters are printed.  Thus, printing could be delayed because of the stream's buffering.  
  
## 참고 항목  
 [Output Streams](../standard-library/output-streams.md)