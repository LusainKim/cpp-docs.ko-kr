---
title: "컴파일러 오류 C2353 | Microsoft Docs"
ms.custom: 
ms.date: 11/04/2016
ms.reviewer: 
ms.suite: 
ms.technology: cpp-tools
ms.tgt_pltfrm: 
ms.topic: error-reference
f1_keywords: C2353
dev_langs: C++
helpviewer_keywords: C2353
ms.assetid: d57f8f77-d9b1-4bba-a940-87ec269ad183
caps.latest.revision: "9"
author: corob-msft
ms.author: corob
manager: ghogen
ms.workload: cplusplus
ms.openlocfilehash: 353c752c4a247a0c6b70656f23d9c4e24d9b4ea6
ms.sourcegitcommit: 8fa8fdf0fbb4f57950f1e8f4f9b81b4d39ec7d7a
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 12/21/2017
---
# <a name="compiler-error-c2353"></a>컴파일러 오류 C2353
예외 사양이 허용 되지 않습니다.  
  
 관리 되는 클래스의 멤버 함수에 예외 사양이 허용 되지 않습니다.  
  
 다음 샘플에서는 C2353 오류가 생성 됩니다.  
  
```  
// C2353.cpp  
// compile with: /clr /c  
ref class X {  
   void f() throw(int);   // C2353  
   void f();   // OK  
};  
```