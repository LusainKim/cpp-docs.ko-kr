---
title: "컴파일러 오류 C2332 | Microsoft Docs"
ms.custom: 
ms.date: 11/04/2016
ms.reviewer: 
ms.suite: 
ms.technology:
- cpp-tools
ms.tgt_pltfrm: 
ms.topic: error-reference
f1_keywords:
- C2332
dev_langs:
- C++
helpviewer_keywords:
- C2332
ms.assetid: fb05cd68-e271-4bea-9fb7-ef4edb0a26ac
caps.latest.revision: 8
author: corob-msft
ms.author: corob
manager: ghogen
ms.translationtype: MT
ms.sourcegitcommit: 35b46e23aeb5f4dbfd2a0dd44b906389dd5bfc88
ms.openlocfilehash: 5dc5e520f64a7f16b2cd142346232cfc712175c1
ms.contentlocale: ko-kr
ms.lasthandoff: 10/09/2017

---
# <a name="compiler-error-c2332"></a>컴파일러 오류 C2332
'typedef': 태그 이름이 없습니다.  
  
 컴파일러는 불완전 한 형식 정을 찾았습니다.  
  
 다음 샘플에서는 C2332 오류가 생성 됩니다.  
  
```  
// C2332.cpp  
// compile with: /c  
struct S {  
   int i;  
};  
  
typedef struct * pS;   // C2332  
typedef struct S* pS;   // OK  
  
int get_S_i(pS p) {  
   return p->i;  
}  
```
