---
title: 'multimap:: make_value (STL/CLR) | Microsoft Docs'
ms.custom: 
ms.date: 11/04/2016
ms.reviewer: 
ms.suite: 
ms.technology: cpp-windows
ms.tgt_pltfrm: 
ms.topic: reference
f1_keywords: cliext::multimap::make_value
dev_langs: C++
helpviewer_keywords: make_value member [STL/CLR]
ms.assetid: 9ae5ace0-e529-4247-8cd6-4e96c0611a75
caps.latest.revision: "15"
author: mikeblome
ms.author: mblome
manager: ghogen
ms.workload:
- cplusplus
- dotnet
ms.openlocfilehash: 8a4b6519cc298219269ab0f35afc880449669caf
ms.sourcegitcommit: 8fa8fdf0fbb4f57950f1e8f4f9b81b4d39ec7d7a
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 12/21/2017
---
# <a name="multimapmakevalue-stlclr"></a>multimap::make_value(STL/CLR)
값 개체를 만듭니다.  
  
## <a name="syntax"></a>구문  
  
```  
static value_type make_value(key_type key, mapped_type mapped);  
```  
  
#### <a name="parameters"></a>매개 변수  
 key  
 사용할 키 값입니다.  
  
 매핑된  
 매핑된 검색할 값입니다.  
  
## <a name="remarks"></a>설명  
 멤버 함수가 반환 하는 `value_type` 개체 키가 `key` 고 매핑된 값이 `mapped`합니다. 여러 다른 멤버 함수 사용에 적합 한 개체를 작성 하려면 사용 합니다.  
  
## <a name="example"></a>예  
  
```  
// cliext_multimap_make_value.cpp   
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
    return (0);   
    }  
  
```  
  
```Output  
[a 1] [b 2] [c 3]  
```  
  
## <a name="requirements"></a>요구 사항  
 **헤더:** \<cliext/매핑 >  
  
 **Namespace:** cliext  
  
## <a name="see-also"></a>참고 항목  
 [multimap (STL/CLR)](../dotnet/multimap-stl-clr.md)   
 [multimap:: key_type (STL/CLR)](../dotnet/multimap-key-type-stl-clr.md)   
 [multimap:: mapped_type (STL/CLR)](../dotnet/multimap-mapped-type-stl-clr.md)   
 [multimap::value_type(STL/CLR)](../dotnet/multimap-value-type-stl-clr.md)