---
title: "컴파일러 오류 C2572 | Microsoft Docs"
ms.custom: 
ms.date: 11/04/2016
ms.reviewer: 
ms.suite: 
ms.technology: cpp-tools
ms.tgt_pltfrm: 
ms.topic: error-reference
f1_keywords: C2572
dev_langs: C++
helpviewer_keywords: C2572
ms.assetid: f1a42d69-727d-4ce5-88c8-d5f55dea66ac
caps.latest.revision: "8"
author: corob-msft
ms.author: corob
manager: ghogen
ms.workload: cplusplus
ms.openlocfilehash: e1845f6f7221ef61132027f570b761b6783b21cb
ms.sourcegitcommit: 8fa8fdf0fbb4f57950f1e8f4f9b81b4d39ec7d7a
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 12/21/2017
---
# <a name="compiler-error-c2572"></a>컴파일러 오류 C2572
'class::member': 기본 매개 변수 재정의: 매개 변수 param  
  
 기본 매개 변수를 재정의할 수 없습니다. 필요 하면 다른 값의 기본 매개 변수는 매개 변수에 대 한 왼쪽을 정의 하지 않아야 합니다.  
  
 다음 샘플에서는 C2572 오류가 생성 됩니다.  
  
```  
// C2572.cpp  
// compile with: /c  
void f(int i = 1);   // function declaration  
  
// function definition  
void f(int i = 1) {}   // C2572  
  
// try the following line instead  
// void f(int i) {}  
```