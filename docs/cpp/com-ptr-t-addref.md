---
title: _com_ptr_t::AddRef | Microsoft Docs
ms.custom: 
ms.date: 11/04/2016
ms.reviewer: 
ms.suite: 
ms.technology:
- cpp-language
ms.tgt_pltfrm: 
ms.topic: language-reference
f1_keywords:
- _com_ptr_t::AddRef
- _com_ptr_t.AddRef
- AddRef
dev_langs:
- C++
helpviewer_keywords:
- AddRef method [C++], interface pointers
ms.assetid: c104dac3-aad3-40bb-a298-75c6cd0e63a2
caps.latest.revision: 6
author: mikeblome
ms.author: mblome
manager: ghogen
translation.priority.ht:
- cs-cz
- de-de
- es-es
- fr-fr
- it-it
- ja-jp
- ko-kr
- pl-pl
- pt-br
- ru-ru
- tr-tr
- zh-cn
- zh-tw
ms.translationtype: HT
ms.sourcegitcommit: 6ffef5f51e57cf36d5984bfc43d023abc8bc5c62
ms.openlocfilehash: d873d91192dc13f7b1277cbe8ef26b24421b6904
ms.contentlocale: ko-kr
ms.lasthandoff: 09/25/2017

---
# <a name="comptrtaddref"></a>_com_ptr_t::AddRef
**Microsoft 전용**  
  
 호출의 `AddRef` 의 멤버 함수 **IUnknown** 캡슐화 된 인터페이스 포인터입니다.  
  
## <a name="syntax"></a>구문  
  
```  
  
void AddRef( );  
  
```  
  
## <a name="remarks"></a>설명  
 호출 `IUnknown::AddRef` 캡슐화 된 인터페이스 포인터에 발생 한 `E_POINTER` 포인터가 있는 경우 오류 **NULL**합니다.  
  
 **Microsoft 전용 종료**  
  
## <a name="see-also"></a>참고 항목  
 [_com_ptr_t 클래스](../cpp/com-ptr-t-class.md)
