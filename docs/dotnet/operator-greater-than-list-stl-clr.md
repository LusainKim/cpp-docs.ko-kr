---
title: "연산자&gt; (list) (STL/CLR) | Microsoft Docs"
ms.custom: 
ms.date: 11/04/2016
ms.reviewer: 
ms.suite: 
ms.technology: cpp-windows
ms.tgt_pltfrm: 
ms.topic: reference
f1_keywords: cliext::list::operator>
dev_langs: C++
helpviewer_keywords: operator> member [STL/CLR]
ms.assetid: 58584708-1fa6-4908-84f6-790d53f46d9a
caps.latest.revision: "17"
author: mikeblome
ms.author: mblome
manager: ghogen
ms.workload:
- cplusplus
- dotnet
ms.openlocfilehash: 0a50137d309c5913d627a065455061123c0e6146
ms.sourcegitcommit: 8fa8fdf0fbb4f57950f1e8f4f9b81b4d39ec7d7a
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 12/21/2017
---
# <a name="operatorgt-list-stlclr"></a>연산자&gt; (list) (STL/CLR)
목록 비교 보다 큽니다.  
  
## <a name="syntax"></a>구문  
  
```  
template<typename Value>  
    bool operator>(list<Value>% left,  
        list<Value>% right);  
```  
  
#### <a name="parameters"></a>매개 변수  
 왼쪽  
 비교할 왼쪽 컨테이너입니다.  
  
 오른쪽  
 비교할 오른쪽 컨테이너입니다.  
  
## <a name="remarks"></a>설명  
 연산자 함수 반환 `right` `<` `left`합니다. 테스트를 사용 하는지 여부를 `left` 후 정렬 `right` 두 목록의 요소 별로 비교를 하는 경우.  
  
## <a name="example"></a>예  
  
```  
// cliext_list_operator_gt.cpp   
// compile with: /clr   
#include <cliext/list>   
  
int main()   
    {   
    cliext::list<wchar_t> c1;   
    c1.push_back(L'a');   
    c1.push_back(L'b');   
    c1.push_back(L'c');   
  
// display contents " a b c"   
    for each (wchar_t elem in c1)   
        System::Console::Write(" {0}", elem);   
    System::Console::WriteLine();   
  
// assign to a new container   
    cliext::list<wchar_t> c2;   
    c2.push_back(L'a');   
    c2.push_back(L'b');   
    c2.push_back(L'd');   
  
// display contents " a b d"   
    for each (wchar_t elem in c2)   
        System::Console::Write(" {0}", elem);   
    System::Console::WriteLine();   
  
    System::Console::WriteLine("[a b c] > [a b c] is {0}",   
        c1 > c1);   
    System::Console::WriteLine("[a b d] > [a b c] is {0}",   
        c2 > c1);   
    return (0);   
    }  
  
```  
  
```Output  
 a b c  
 a b d  
[a b c] > [a b c] is False  
[a b d] > [a b c] is True  
```  
  
## <a name="requirements"></a>요구 사항  
 **헤더:** \<cliext/목록 >  
  
 **Namespace:** cliext  
  
## <a name="see-also"></a>참고 항목  
 [list (STL/CLR)](../dotnet/list-stl-clr.md)   
 [연산자 = = (list) (STL/CLR)](../dotnet/operator-equality-list-stl-clr.md)   
 [operator! = (list) (STL/CLR)](../dotnet/operator-inequality-list-stl-clr.md)   
 [연산자\< (list) (STL/CLR)](../dotnet/operator-less-than-list-stl-clr.md)   
 [연산자 > = (list) (STL/CLR)](../dotnet/operator-greater-or-equal-list-stl-clr.md)   
 [operator<= (list)(STL/CLR)](../dotnet/operator-less-or-equal-list-stl-clr.md)