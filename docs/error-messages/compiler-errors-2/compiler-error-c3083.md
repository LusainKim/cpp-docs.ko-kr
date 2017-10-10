---
title: "컴파일러 오류 C3083 | Microsoft Docs"
ms.custom: 
ms.date: 11/04/2016
ms.reviewer: 
ms.suite: 
ms.technology:
- cpp-tools
ms.tgt_pltfrm: 
ms.topic: error-reference
f1_keywords:
- C3083
dev_langs:
- C++
helpviewer_keywords:
- C3083
ms.assetid: 05ff791d-52bb-41eb-9511-3ef89d7f4710
caps.latest.revision: 5
author: corob-msft
ms.author: corob
manager: ghogen
ms.translationtype: MT
ms.sourcegitcommit: 35b46e23aeb5f4dbfd2a0dd44b906389dd5bfc88
ms.openlocfilehash: 8aa8296d117105b91a66bc134a1510519c17deff
ms.contentlocale: ko-kr
ms.lasthandoff: 10/10/2017

---
# <a name="compiler-error-c3083"></a>컴파일러 오류 C3083
'function': 왼쪽의 기호는 ':: ' 형식 이어야 합니다  
  
 함수를 잘못 호출 했습니다.  
  
## <a name="example"></a>예제  
 다음 샘플에서는 C3083 오류가 발생 합니다.  
  
```  
// C3083.cpp  
// compile with: /c  
struct N {  
   ~N();  
};  
  
struct N1 {  
   ~N1();  
};  
  
N::N::~N() {}   // C3083  
N1::~N1() {}   // OK  
```
