---
title: 'hash_multimap:: key_type (STL/CLR) | Microsoft Docs'
ms.custom: 
ms.date: 11/04/2016
ms.reviewer: 
ms.suite: 
ms.technology: cpp-windows
ms.tgt_pltfrm: 
ms.topic: reference
f1_keywords: cliext::hash_multimap::key_type
dev_langs: C++
helpviewer_keywords: key_type member [STL/CLR]
ms.assetid: fd6ef622-6812-4574-b459-d3ee110b0382
caps.latest.revision: "14"
author: mikeblome
ms.author: mblome
manager: ghogen
ms.workload:
- cplusplus
- dotnet
ms.openlocfilehash: e317b8523fa5220168c10a9f5e345c65ff5aace7
ms.sourcegitcommit: 8fa8fdf0fbb4f57950f1e8f4f9b81b4d39ec7d7a
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 12/21/2017
---
# <a name="hashmultimapkeytype-stlclr"></a>hash_multimap::key_type(STL/CLR)
정렬 키의 형식입니다.  
  
## <a name="syntax"></a>구문  
  
```  
typedef Key key_type;  
```  
  
## <a name="remarks"></a>설명  
 이 형식은 템플릿 매개 변수 `Key`의 동의어입니다.  
  
## <a name="example"></a>예  
  
```  
// cliext_hash_multimap_key_type.cpp   
// compile with: /clr   
#include <cliext/hash_map>   
  
typedef cliext::hash_multimap<wchar_t, int> Myhash_multimap;   
int main()   
    {   
    Myhash_multimap c1;   
    c1.insert(Myhash_multimap::make_value(L'a', 1));   
    c1.insert(Myhash_multimap::make_value(L'b', 2));   
    c1.insert(Myhash_multimap::make_value(L'c', 3));   
  
// display contents " [a 1] [b 2] [c 3]" using key_type   
    for (Myhash_multimap::iterator it = c1.begin(); it != c1.end(); ++it)   
        {   // store element in key_type object   
        Myhash_multimap::key_type val = it->first;   
  
        System::Console::Write(" {0}", val);   
        }   
    System::Console::WriteLine();   
    return (0);   
    }  
  
```  
  
```Output  
a b c  
```  
  
## <a name="requirements"></a>요구 사항  
 **헤더:** \<cliext/hash_map >  
  
 **Namespace:** cliext  
  
## <a name="see-also"></a>참고 항목  
 [hash_multimap (STL/CLR)](../dotnet/hash-multimap-stl-clr.md)   
 [hash_multimap:: key_compare (STL/CLR)](../dotnet/hash-multimap-key-compare-stl-clr.md)   
 [hash_multimap:: mapped_type (STL/CLR)](../dotnet/hash-multimap-mapped-type-stl-clr.md)   
 [hash_multimap::value_type(STL/CLR)](../dotnet/hash-multimap-value-type-stl-clr.md)