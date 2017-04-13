---
title: "컴파일러 경고 (수준 1) C4997 | Microsoft Docs"
ms.custom: 
ms.date: 11/04/2016
ms.reviewer: 
ms.suite: 
ms.technology:
- devlang-cpp
ms.tgt_pltfrm: 
ms.topic: article
f1_keywords:
- C4997
dev_langs:
- C++
helpviewer_keywords:
- C4997
ms.assetid: d39678fd-0c1a-4104-8a45-9e3f20de0407
caps.latest.revision: 7
author: corob-msft
ms.author: corob
manager: ghogen
translation.priority.ht:
- de-de
- es-es
- fr-fr
- it-it
- ja-jp
- ko-kr
- ru-ru
- zh-cn
- zh-tw
translation.priority.mt:
- cs-cz
- pl-pl
- pt-br
- tr-tr
translationtype: Machine Translation
ms.sourcegitcommit: 0d9cbb01d1ad0f2ea65d59334cb88140ef18fce0
ms.openlocfilehash: 5b20c93c167ca2d13e7257241c476a6680547437
ms.lasthandoff: 04/12/2017

---
# <a name="compiler-warning-level-1-c4997"></a>컴파일러 경고(수준 1) C4997
'class': coclass가 COM 인터페이스 또는 의사(pseudo) 인터페이스를 구현하지 않습니다.  
  
 클래스에 표시 된 [coclass](../../windows/coclass.md) 특성 인터페이스를 구현 하지 않았습니다.  
  
 다음 샘플에서는 C4997을 생성합니다.  
  
```  
// C4997.cpp  
// compile with: /WX  
// to resolve this C4997, uncomment all code  
#include <objbase.h>  
  
[ object ]  
__interface I {  
   HRESULT func();  
};  
  
[ coclass ]  
struct C /*: I*/ {  
   /*  
   HRESULT func() {  
      return S_OK;  
   }  
   */  
};   // C4997  
```
