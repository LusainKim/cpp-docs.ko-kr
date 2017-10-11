---
title: "컴파일러 오류 C2437 | Microsoft Docs"
ms.custom: 
ms.date: 11/04/2016
ms.reviewer: 
ms.suite: 
ms.technology:
- cpp-tools
ms.tgt_pltfrm: 
ms.topic: error-reference
f1_keywords:
- C2437
dev_langs:
- C++
helpviewer_keywords:
- C2437
ms.assetid: 2d2b3c6c-856a-4b27-ae10-64813b3e5483
caps.latest.revision: 8
author: corob-msft
ms.author: corob
manager: ghogen
ms.translationtype: MT
ms.sourcegitcommit: 35b46e23aeb5f4dbfd2a0dd44b906389dd5bfc88
ms.openlocfilehash: 41e2ff34ef15b6000cb91c87838938f5863eabdf
ms.contentlocale: ko-kr
ms.lasthandoff: 10/09/2017

---
# <a name="compiler-error-c2437"></a>컴파일러 오류 C2437
'identifier': 이미 초기화 되었습니다.  
  
 개체는 한 번만 초기화할 수 있습니다.  
  
 다음 샘플에서는 C2437 오류가 생성 됩니다.  
  
```  
// C2437.cpp  
// compile with: /c  
class A {  
public:  
   A(int i) {}  
};  
  
class B : A {  
   B() : A(1), A(2) {}   // C2437  
   B() : A(1) {}   // OK  
};  
```
