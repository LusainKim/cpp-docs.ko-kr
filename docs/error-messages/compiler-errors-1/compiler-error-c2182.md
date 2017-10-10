---
title: "컴파일러 오류 C2182 | Microsoft Docs"
ms.custom: 
ms.date: 11/04/2016
ms.reviewer: 
ms.suite: 
ms.technology:
- cpp-tools
ms.tgt_pltfrm: 
ms.topic: article
f1_keywords:
- C2182
dev_langs:
- C++
helpviewer_keywords:
- C2182
ms.assetid: dfd8d47d-9606-496e-bd96-4bf41ba1f857
caps.latest.revision: 8
author: corob-msft
ms.author: corob
manager: ghogen
ms.translationtype: MT
ms.sourcegitcommit: 35b46e23aeb5f4dbfd2a0dd44b906389dd5bfc88
ms.openlocfilehash: d5dc323cd1efd5ad96ee77a741414f8bfbcc12de
ms.contentlocale: ko-kr
ms.lasthandoff: 10/09/2017

---
# <a name="compiler-error-c2182"></a>컴파일러 오류 C2182
'identifier': 'void' 형식을 잘못 사용했습니다.  
  
 변수가 선언된 형식 `void`입니다.  
  
 다음 샘플에서는 C2182를 생성합니다.  
  
```  
// C2182.cpp  
// compile with: /c  
int main() {  
   int i = 10;  
   void &ir = i;   // C2182 cannot have a reference to type void  
   int &ir = i;   // OK  
}  
```
