---
title: "컴파일러 오류 C2883 | Microsoft Docs"
ms.custom: 
ms.date: 11/04/2016
ms.reviewer: 
ms.suite: 
ms.technology: cpp-tools
ms.tgt_pltfrm: 
ms.topic: error-reference
f1_keywords: C2883
dev_langs: C++
helpviewer_keywords: C2883
ms.assetid: 5c6d689d-ed42-41ad-b5c0-e9c2e0b8c356
caps.latest.revision: "7"
author: corob-msft
ms.author: corob
manager: ghogen
ms.workload: cplusplus
ms.openlocfilehash: b2a52236d3c017307ad44c6103f1770422239881
ms.sourcegitcommit: 8fa8fdf0fbb4f57950f1e8f4f9b81b4d39ec7d7a
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 12/21/2017
---
# <a name="compiler-error-c2883"></a>컴파일러 오류 C2883
'name': 함수 선언이 using 선언으로 인해 'identifier'와 충돌  
  
 함수를 두 번 이상 정의 하려고 했습니다. 첫 번째 정의 네임 스페이스가에서 만들어진는 `using` 선언 합니다. 두 번째 로컬 정의 했습니다.  
  
 다음 샘플에서는 C2883 오류가 생성 됩니다.  
  
```  
// C2883.cpp  
namespace A {  
   void z(int);  
}  
  
int main() {  
   using A::z;  
   void z(int);   // C2883  z is already defined  
}  
```