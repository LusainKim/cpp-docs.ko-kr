---
title: 'pair:: second_type (STL/CLR) | Microsoft Docs'
ms.custom: 
ms.date: 11/04/2016
ms.reviewer: 
ms.suite: 
ms.technology: cpp-windows
ms.tgt_pltfrm: 
ms.topic: reference
f1_keywords: cliext::pair::second_type
dev_langs: C++
helpviewer_keywords: second_type member [STL/CLR]
ms.assetid: 555f0216-186b-4dac-babc-1499f69e5c1b
caps.latest.revision: "9"
author: mikeblome
ms.author: mblome
manager: ghogen
ms.workload:
- cplusplus
- dotnet
ms.openlocfilehash: 684b233eeb77093e686cfb0af7d2fd6fc1ae80e2
ms.sourcegitcommit: 8fa8fdf0fbb4f57950f1e8f4f9b81b4d39ec7d7a
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 12/21/2017
---
# <a name="pairsecondtype-stlclr"></a>pair::second_type(STL/CLR)
두 번째 래핑된 값의 형식입니다.  
  
## <a name="syntax"></a>구문  
  
```  
typedef Value2 second_type;  
```  
  
## <a name="remarks"></a>설명  
 이 형식은 템플릿 매개 변수 `Value2`의 동의어입니다.  
  
## <a name="example"></a>예  
  
```  
// cliext_pair_second_type.cpp   
// compile with: /clr   
#include <cliext/utility>   
  
int main()   
    {   
    cliext::pair<wchar_t, int> c1(L'x', 3);   
    System::Console::WriteLine("[{0}, {1}]", c1.first, c1.second);   
  
    cliext::pair<wchar_t, int>::first_type first_val = c1.first;   
    cliext::pair<wchar_t, int>::second_type second_val = c1.second;   
    System::Console::WriteLine("[{0}, {1}]", first_val, second_val);   
    return (0);   
    }  
  
```  
  
```Output  
[x, 3]  
```  
  
## <a name="requirements"></a>요구 사항  
 **헤더:** \<cliext/유틸리티 >  
  
 **Namespace:** cliext  
  
## <a name="see-also"></a>참고 항목  
 [pair (STL/CLR)](../dotnet/pair-stl-clr.md)   
 [pair:: first (STL/CLR)](../dotnet/pair-first-stl-clr.md)   
 [pair:: first_type (STL/CLR)](../dotnet/pair-first-type-stl-clr.md)   
 [pair::second(STL/CLR)](../dotnet/pair-second-stl-clr.md)