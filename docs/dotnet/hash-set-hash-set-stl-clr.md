---
title: 'hash_set:: hash_set (STL/CLR) | Microsoft Docs'
ms.custom: 
ms.date: 11/04/2016
ms.reviewer: 
ms.suite: 
ms.technology: cpp-windows
ms.tgt_pltfrm: 
ms.topic: reference
f1_keywords: cliext::hash_set::hash_set
dev_langs: C++
helpviewer_keywords: hash_set member [STL/CLR]
ms.assetid: 006414ed-db5a-4c08-ac81-4a8ae57d0aad
caps.latest.revision: "18"
author: mikeblome
ms.author: mblome
manager: ghogen
ms.workload:
- cplusplus
- dotnet
ms.openlocfilehash: a01d8dcfda1bbb7f05db9fde7b16aa5094fba2bc
ms.sourcegitcommit: 8fa8fdf0fbb4f57950f1e8f4f9b81b4d39ec7d7a
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 12/21/2017
---
# <a name="hashsethashset-stlclr"></a>hash_set::hash_set(STL/CLR)
컨테이너 개체를 만듭니다.  
  
## <a name="syntax"></a>구문  
  
```  
hash_set();  
explicit hash_set(key_compare^ pred);  
hash_set(key_compare^ pred, hasher^ hashfn);  
hash_set(hash_set<Key>% right);  
hash_set(hash_set<Key>^ right);  
template<typename InIter>  
    hash_sethash_set(InIter first, InIter last);  
template<typename InIter>  
    hash_set(InIter first, InIter last,  
        key_compare^ pred);  
template<typename InIter>  
    hash_set(InIter first, InIter last,  
        key_compare^ pred, hasher^ hashfn);  
hash_set(System::Collections::Generic::IEnumerable<GValue>^ right);  
hash_set(System::Collections::Generic::IEnumerable<GValue>^ right,  
    key_compare^ pred);  
hash_set(System::Collections::Generic::IEnumerable<GValue>^ right,  
    key_compare^ pred, hasher^ hashfn);  
```  
  
#### <a name="parameters"></a>매개 변수  
 첫 번째  
 삽입할 범위의의 시작입니다.  
  
 hashfn  
 해시 버킷에 매핑 키에 대 한 함수입니다.  
  
 last  
 삽입할 범위의 끝입니다.  
  
 pred  
 제어 되는 시퀀스에 대 한 조건자를 정렬 합니다.  
  
 오른쪽  
 삽입할 개체 또는 범위입니다.  
  
## <a name="remarks"></a>설명  
 생성자:  
  
 `hash_set();`  
  
 기본 조건자를 정렬 된 요소가 없는 제어 되는 시퀀스를 초기화 `key_compare()`, 및 기본 해시 함수가 있습니다. 기본 조건자 및 해시 함수를 정렬 된 빈 초기 제어 시퀀스를 지정 하려면 사용 합니다.  
  
 생성자:  
  
 `explicit hash_set(key_compare^ pred);`  
  
 정렬 조건자가 있는 요소가 없는 제어 되는 시퀀스를 초기화 `pred`, 및 기본 해시 함수로 합니다. 지정된 된 정렬 조건자와 기본 해시 함수는 빈 초기 제어 시퀀스를 지정 하려면 사용 합니다.  
  
 생성자:  
  
 `hash_set(key_compare^ pred, hasher^ hashfn);`  
  
 정렬 조건자가 있는 요소가 없는 제어 되는 시퀀스를 초기화 `pred`, 및 해시 함수가 `hashfn`합니다. 지정 된 정렬 조건자 및 해시 함수는 빈 초기 제어 시퀀스를 지정 하려면 사용 합니다.  
  
 생성자:  
  
 `hash_set(hash_set<Key>% right);`  
  
 순서와 제어 된 시퀀스를 초기화 합니다. [`right.begin()`, `right.end()`), 기본 조건자를 정렬 및 기본 해시 함수입니다. Hash_set 개체에 의해 제어 되는 시퀀스의 복사본 인는 초기 제어 시퀀스를 지정 하려면 사용할 `right`된 기본 정렬 조건자 및 해시 함수입니다.  
  
 생성자:  
  
 `hash_set(hash_set<Key>^ right);`  
  
 순서와 제어 된 시퀀스를 초기화 합니다. [`right->begin()`, `right->end()`), 기본 조건자를 정렬 및 기본 해시 함수입니다. Hash_set 개체에 의해 제어 되는 시퀀스의 복사본 인는 초기 제어 시퀀스를 지정 하려면 사용할 `right`된 기본 정렬 조건자 및 해시 함수입니다.  
  
 생성자:  
  
 `template<typename InIter> hash_set(InIter first, InIter last);`  
  
 순서와 제어 된 시퀀스를 초기화 합니다. [`first`, `last`), 기본 조건자를 정렬 및 기본 해시 함수입니다. 기본 조건자 및 해시 함수를 정렬 된 제어 되는 다른 시퀀스의 복사본을 확인을 사용 합니다.  
  
 생성자:  
  
 `template<typename InIter> hash_set(InIter first, InIter last, key_compare^ pred);`  
  
 순서와 제어 된 시퀀스를 초기화 합니다. [`first`, `last`), 정렬 조건부와 함께 `pred`, 및 기본 해시 함수로 합니다. 제어 되는 시퀀스의 사본이 지정된 된 정렬 조건자 및 기본 해시 함수와 다른 시퀀스를 사용 합니다.  
  
 생성자:  
  
 `template<typename InIter> hash_set(InIter first, InIter last, key_compare^ pred, hasher^ hashfn);`  
  
 순서와 제어 된 시퀀스를 초기화 합니다. [`first`, `last`), 정렬 조건부와 함께 `pred`, 및 해시 함수가 `hashfn`합니다. 제어 되는 시퀀스의 사본을 지정한 정렬 조건자 및 해시 함수가 있는 다른 시퀀스를 사용 합니다.  
  
 생성자:  
  
 `hash_set(System::Collections::Generic::IEnumerable<Key>^ right);`  
  
 열거자에 지정 된 시퀀스와 제어 된 시퀀스를 초기화 `right`, 기본 조건자를 정렬 및 기본 해시 함수입니다. 제어 되는 시퀀스의 사본을 설명 하는 열거자에 따라 기본 조건자 및 해시 함수를 정렬 하는 다른 시퀀스를 사용 합니다.  
  
 생성자:  
  
 `hash_set(System::Collections::Generic::IEnumerable<Key>^ right, key_compare^ pred);`  
  
 열거자에 지정 된 시퀀스와 제어 된 시퀀스를 초기화 `right`, 정렬 조건부와 함께 `pred`, 및 기본 해시 함수로 합니다. 제어 되는 시퀀스에서 지정 된 정렬 조건자 및 기본 해시 함수가 열거자를 설명 하는 다른 시퀀스의 복사본을 확인 하려면 사용 합니다.  
  
 생성자:  
  
 `hash_set(System::Collections::Generic::IEnumerable<Key>^ right, key_compare^ pred, hasher^ hashfn);`  
  
 열거자에 지정 된 시퀀스와 제어 된 시퀀스를 초기화 `right`, 정렬 조건부와 함께 `pred`, 및 해시 함수가 `hashfn`합니다. 제어 되는 시퀀스의 사본을 열거자를 지정한 순서 지정 조건자 및 해시 함수가 있는 설명 하는 다른 시퀀스를 사용 합니다.  
  
## <a name="example"></a>예  
  
```  
// cliext_hash_set_construct.cpp   
// compile with: /clr   
#include <cliext/hash_set>   
  
int myfun(wchar_t key)   
    { // hash a key   
    return (key ^ 0xdeadbeef);   
    }   
  
typedef cliext::hash_set<wchar_t> Myhash_set;   
int main()   
    {   
// construct an empty container   
    Myhash_set c1;   
    System::Console::WriteLine("size() = {0}", c1.size());   
  
    c1.insert(L'a');   
    c1.insert(L'b');   
    c1.insert(L'c');   
    for each (wchar_t elem in c1)   
        System::Console::Write(" {0}", elem);   
    System::Console::WriteLine();   
  
// construct with an ordering rule   
    Myhash_set c2 = cliext::greater_equal<wchar_t>();   
    System::Console::WriteLine("size() = {0}", c2.size());   
  
    c2.insert(c1.begin(), c1.end());   
    for each (wchar_t elem in c2)   
        System::Console::Write(" {0}", elem);   
    System::Console::WriteLine();   
  
// construct with an ordering rule and hash function   
    Myhash_set c2h(cliext::greater_equal<wchar_t>(),   
        gcnew Myhash_set::hasher(&myfun));   
    System::Console::WriteLine("size() = {0}", c2h.size());   
  
    c2h.insert(c1.begin(), c1.end());   
    for each (wchar_t elem in c2h)   
        System::Console::Write(" {0}", elem);   
    System::Console::WriteLine();   
    System::Console::WriteLine();   
  
// construct with an iterator range   
    Myhash_set c3(c1.begin(), c1.end());   
    for each (wchar_t elem in c3)   
        System::Console::Write(" {0}", elem);   
    System::Console::WriteLine();   
  
// construct with an iterator range and an ordering rule   
    Myhash_set c4(c1.begin(), c1.end(),   
        cliext::greater_equal<wchar_t>());   
    for each (wchar_t elem in c4)   
        System::Console::Write(" {0}", elem);   
    System::Console::WriteLine();   
  
// construct with an iterator range and an ordering rule and hash function   
    Myhash_set c4h(c1.begin(), c1.end(),   
        cliext::greater_equal<wchar_t>(),   
        gcnew Myhash_set::hasher(&myfun));   
    for each (wchar_t elem in c4h)   
        System::Console::Write(" {0}", elem);   
    System::Console::WriteLine();   
    System::Console::WriteLine();   
  
// construct with an enumeration   
    Myhash_set c5(   // NOTE: cast is not needed   
        (System::Collections::Generic::IEnumerable<wchar_t>^)%c3);   
    for each (wchar_t elem in c5)   
        System::Console::Write(" {0}", elem);   
    System::Console::WriteLine();   
  
// construct with an enumeration and an ordering rule   
    Myhash_set c6(   // NOTE: cast is not needed   
        (System::Collections::Generic::IEnumerable<wchar_t>^)%c3,   
            cliext::greater_equal<wchar_t>());   
    for each (wchar_t elem in c6)   
        System::Console::Write(" {0}", elem);   
    System::Console::WriteLine();   
  
// construct with an enumeration and an ordering rule and hash function   
    Myhash_set c6h(   // NOTE: cast is not needed   
        (System::Collections::Generic::IEnumerable<wchar_t>^)%c3,   
            cliext::greater_equal<wchar_t>(),   
                gcnew Myhash_set::hasher(&myfun));   
    for each (wchar_t elem in c6h)   
        System::Console::Write(" {0}", elem);   
    System::Console::WriteLine();   
    System::Console::WriteLine();   
  
// construct from a generic container   
    Myhash_set c7(c4);   
    for each (wchar_t elem in c7)   
        System::Console::Write(" {0}", elem);   
    System::Console::WriteLine();   
  
// construct by copying another container   
    Myhash_set c8(%c3);   
    for each (wchar_t elem in c8)   
        System::Console::Write(" {0}", elem);   
    System::Console::WriteLine();   
    return (0);   
    }  
  
```  
  
```Output  
size() = 0  
 a b c  
size() = 0  
 a b c  
size() = 0  
 c b a  
  
 a b c  
 a b c  
 c b a  
  
 a b c  
 a b c  
 c b a  
  
 a b c  
 a b c  
```  
  
## <a name="requirements"></a>요구 사항  
 **헤더:** \<cliext/hash_set >  
  
 **Namespace:** cliext  
  
## <a name="see-also"></a>참고 항목  
 [hash_set (STL/CLR)](../dotnet/hash-set-stl-clr.md)   
 [hash_set:: generic_container (STL/CLR)](../dotnet/hash-set-generic-container-stl-clr.md)   
 [hash_set::operator=(STL/CLR)](../dotnet/hash-set-operator-assign-stl-clr.md)