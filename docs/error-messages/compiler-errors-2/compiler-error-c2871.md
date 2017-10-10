---
title: "컴파일러 오류 C2871 | Microsoft Docs"
ms.custom: 
ms.date: 11/04/2016
ms.reviewer: 
ms.suite: 
ms.technology:
- cpp-tools
ms.tgt_pltfrm: 
ms.topic: error-reference
f1_keywords:
- C2871
dev_langs:
- C++
helpviewer_keywords:
- C2871
ms.assetid: 44aeb84d-61f0-45e0-8dad-22a3cd46b7f8
caps.latest.revision: 10
author: corob-msft
ms.author: corob
manager: ghogen
ms.translationtype: MT
ms.sourcegitcommit: 35b46e23aeb5f4dbfd2a0dd44b906389dd5bfc88
ms.openlocfilehash: 0003f04a32ff017234607a90162465549092a013
ms.contentlocale: ko-kr
ms.lasthandoff: 10/10/2017

---
# <a name="compiler-error-c2871"></a>컴파일러 오류 C2871
'name':이 이름의 네임 스페이스가 없습니다.  
  
네임 스페이스를 하지 않은 식별자를 전달 하는 경우이 오류가 발생 합니다는 [를 사용 하 여](../../cpp/namespaces-cpp.md#using_directives) 지시문입니다.  
  
## <a name="example"></a>예제  
다음 샘플에서는 C2871 오류가 생성 됩니다.  
  
```cpp  
// C2871.cpp  
// compile with: /c
namespace a {
   int fn(int i) { return i; }
} 
namespace b { 
   using namespace d;   // C2871 because d is not a namespace  
   using namespace a;   // OK
}  
```
