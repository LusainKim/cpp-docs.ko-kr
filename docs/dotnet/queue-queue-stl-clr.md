---
title: 'queue:: queue (STL/CLR) | Microsoft Docs'
ms.custom: 
ms.date: 11/04/2016
ms.reviewer: 
ms.suite: 
ms.technology: cpp-windows
ms.tgt_pltfrm: 
ms.topic: reference
f1_keywords: cliext::queue::queue
dev_langs: C++
helpviewer_keywords: queue member [STL/CLR]
ms.assetid: 6106c07f-d5eb-4f0b-82df-ee4e2e751047
caps.latest.revision: "18"
author: mikeblome
ms.author: mblome
manager: ghogen
ms.workload:
- cplusplus
- dotnet
ms.openlocfilehash: d6c4b24ad40bf19b7a20aafcfa2d02fb6490fed1
ms.sourcegitcommit: 8fa8fdf0fbb4f57950f1e8f4f9b81b4d39ec7d7a
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 12/21/2017
---
# <a name="queuequeue-stlclr"></a>queue::queue(STL/CLR)
컨테이너 어댑터 개체를 만듭니다.  
  
## <a name="syntax"></a>구문  
  
```  
queue();  
queue(queue<Value, Container>% right);  
queue(queue<Value, Container>^ right);  
explicit queue(container_type% wrapped);  
```  
  
#### <a name="parameters"></a>매개 변수  
 오른쪽  
 복사할 개체입니다.  
  
 래핑  
 래핑된 컨테이너를 사용 합니다.  
  
## <a name="remarks"></a>설명  
 생성자:  
  
 `queue();`  
  
 빈 래핑된 컨테이너를 만듭니다. 초기는 빈 제어 시퀀스를 지정 하려면 사용 합니다.  
  
 생성자:  
  
 `queue(queue<Value, Container>% right);`  
  
 복사본 인 래핑된 컨테이너를 만들고 `right.get_container()`합니다. 큐 개체에 의해 제어 되는 시퀀스의 복사본 인는 초기 제어 시퀀스를 지정 하려면 사용할 `right`합니다.  
  
 생성자:  
  
 `queue(queue<Value, Container>^ right);`  
  
 복사본 인 래핑된 컨테이너를 만들고 `right->get_container()`합니다. 큐 개체에 의해 제어 되는 시퀀스의 복사본 인는 초기 제어 시퀀스를 지정 하려면 사용할 `*right`합니다.  
  
 생성자:  
  
 `explicit queue(container_type wrapped);`  
  
 기존 컨테이너를 사용 하 여 `wrapped` 래핑된 컨테이너로 합니다. 기존 컨테이너에서 큐를 생성 하는 데 사용할 수 있습니다.  
  
## <a name="example"></a>예  
  
```  
// cliext_queue_construct.cpp   
// compile with: /clr   
#include <cliext/queue>   
#include <cliext/list>   
  
typedef cliext::queue<wchar_t> Myqueue;   
typedef cliext::list<wchar_t> Mylist;   
typedef cliext::queue<wchar_t, Mylist> Myqueue_list;   
int main()   
    {   
// construct an empty container   
    Myqueue c1;   
    System::Console::WriteLine("size() = {0}", c1.size());   
  
// construct from an underlying container   
    Mylist v2(5, L'x');   
    Myqueue_list c2(v2);       
    for each (wchar_t elem in c2.get_container())   
        System::Console::Write(" {0}", elem);   
    System::Console::WriteLine();   
  
// construct by copying another container   
    Myqueue_list c3(c2);   
    for each (wchar_t elem in c3.get_container())   
        System::Console::Write(" {0}", elem);   
    System::Console::WriteLine();   
  
// construct by copying another container through handle   
    Myqueue_list c4(%c2);   
    for each (wchar_t elem in c4.get_container())   
        System::Console::Write(" {0}", elem);   
    System::Console::WriteLine();   
    return (0);   
    }  
  
```  
  
```Output  
size() = 0  
 x x x x x  
 x x x x x  
 x x x x x  
```  
  
## <a name="requirements"></a>요구 사항  
 **헤더:** \<cliext/queue >  
  
 **Namespace:** cliext  
  
## <a name="see-also"></a>참고 항목  
 [queue (STL/CLR)](../dotnet/queue-stl-clr.md)   
 [queue:: assign (STL/CLR)](../dotnet/queue-assign-stl-clr.md)   
 [queue:: generic_container (STL/CLR)](../dotnet/queue-generic-container-stl-clr.md)   
 [queue::operator=(STL/CLR)](../dotnet/queue-operator-assign-stl-clr.md)