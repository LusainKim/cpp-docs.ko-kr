---
title: "컴파일러 오류 C3358 | Microsoft Docs"
ms.custom: 
ms.date: 11/04/2016
ms.reviewer: 
ms.suite: 
ms.technology:
- cpp-tools
ms.tgt_pltfrm: 
ms.topic: article
f1_keywords:
- C3358
dev_langs:
- C++
helpviewer_keywords:
- C3358
ms.assetid: 180b93df-e78f-441a-91fb-1594c681f7f0
caps.latest.revision: 6
author: corob-msft
ms.author: corob
manager: ghogen
ms.translationtype: MT
ms.sourcegitcommit: 35b46e23aeb5f4dbfd2a0dd44b906389dd5bfc88
ms.openlocfilehash: 0a4e062fd21577836ae1b56d2d0e277b162d9451
ms.contentlocale: ko-kr
ms.lasthandoff: 10/10/2017

---
# <a name="compiler-error-c3358"></a>컴파일러 오류 C3358
'symbol': 기호를 찾을 수 없습니다.  
  
 필요한 기호를 찾을 수 없습니다.  
  
 다음 샘플에서는 C3358을 생성합니다.  
  
```  
// C3358.cpp  
#define __ATLEVENT_H__ 1   // remove this line to resolve the error  
#define _ATL_ATTRIBUTES 1  
#include "atlbase.h"  
#include "atlcom.h"  
  
[event_receiver(com)]  
struct A   // C3358  
{  
   void func();  
};  
  
int main()  
{  
}  
```
