---
title: 'hash_multiset:: erase (STL/CLR) | Microsoft Docs'
ms.custom: 
ms.date: 11/04/2016
ms.reviewer: 
ms.suite: 
ms.technology: cpp-windows
ms.tgt_pltfrm: 
ms.topic: reference
f1_keywords: cliext::hash_multiset::erase
dev_langs: C++
helpviewer_keywords: erase member [STL/CLR]
ms.assetid: bddd329d-aece-4b93-8355-005351c3aa45
caps.latest.revision: "16"
author: mikeblome
ms.author: mblome
manager: ghogen
ms.workload:
- cplusplus
- dotnet
ms.openlocfilehash: 9e2e35eeecab632371922705cc95848e84a46d1d
ms.sourcegitcommit: 8fa8fdf0fbb4f57950f1e8f4f9b81b4d39ec7d7a
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 12/21/2017
---
# <a name="hashmultiseterase-stlclr"></a>hash_multiset::erase(STL/CLR)
지정된 위치에 있는 요소를 제거합니다.  
  
## <a name="syntax"></a>구문  
  
```  
iterator erase(iterator where);  
iterator erase(iterator first, iterator last);  
bool erase(key_type key)  
```  
  
#### <a name="parameters"></a>매개 변수  
 첫 번째  
 범위를 지우려면의 시작입니다.  
  
 key  
 지우기 키 값입니다.  
  
 last  
 범위를 지우려면의 끝입니다.  
  
 형식에 대한 설명  
 지울 요소입니다.  
  
## <a name="remarks"></a>설명  
 가 가리키는 제어 된 시퀀스의 요소를 제거 하는 첫 번째 멤버 함수 `where`를 제거 하는 요소 뒤에 남은 첫 번째 요소를 지정 하는 반복기를 반환 하 고 또는 [hash_multiset:: end (STL/CLR)](../dotnet/hash-multiset-end-stl-clr.md) `()` 이러한 요소가 없을 경우. 단일 요소를 제거 하려면 사용 합니다.  
  
 범위에서 제어 된 시퀀스의 요소를 제거 하는 두 번째 멤버 함수 [`first`, `last`), 제거 된 요소 뒤에 남은 첫 번째 요소를 지정 하는 반복기를 반환 하거나 `end()` 요소가 없는 경우 있습니다. 0 개 이상의 연속 요소를 제거 하려면 사용 합니다.  
  
 해당 키가 동일 하 게 정렬 된 제어 된 시퀀스의 모든 요소를 제거 하는 세 번째 멤버 함수를 `key`, 제거 된 요소의 수를 반환 합니다. 제거 하 고 계산 된 지정 된 키와 일치 하는 모든 요소를 사용 합니다.  
  
 각 요소 삭제 시간이의 요소 수 로그에 비례 제어 된 시퀀스의 됩니다.  
  
## <a name="example"></a>예  
  
```  
// cliext_hash_multiset_erase.cpp   
// compile with: /clr   
#include <cliext/hash_set>   
  
typedef cliext::hash_multiset<wchar_t> Myhash_multiset;   
int main()   
    {   
    Myhash_multiset c1;   
    c1.insert(L'a');   
    c1.insert(L'b');   
    c1.insert(L'c');   
  
// display initial contents " a b c"   
    for each (wchar_t elem in c1)   
        System::Console::Write(" {0}", elem);   
    System::Console::WriteLine();   
  
// erase an element and reinspect   
    System::Console::WriteLine("erase(begin()) = {0}",   
        *c1.erase(c1.begin()));   
  
// add elements and display " b c d e"   
    c1.insert(L'd');   
    c1.insert(L'e');   
    for each (wchar_t elem in c1)   
        System::Console::Write(" {0}", elem);   
    System::Console::WriteLine();   
  
// erase all but end   
    Myhash_multiset::iterator it = c1.end();   
    System::Console::WriteLine("erase(begin(), end()-1) = {0}",   
        *c1.erase(c1.begin(), --it));   
    System::Console::WriteLine("size() = {0}", c1.size());   
    return (0);   
    }  
  
```  
  
```Output  
 a b c  
erase(begin()) = b  
 b c d e  
erase(begin(), end()-1) = e  
size() = 1  
```  
  
## <a name="requirements"></a>요구 사항  
 **헤더:** \<cliext/hash_set >  
  
 **Namespace:** cliext  
  
## <a name="see-also"></a>참고 항목  
 [hash_multiset (STL/CLR)](../dotnet/hash-multiset-stl-clr.md)   
 [hash_multiset::clear(STL/CLR)](../dotnet/hash-multiset-clear-stl-clr.md)