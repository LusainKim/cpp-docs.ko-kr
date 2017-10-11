---
title: "컴파일러 오류 C2612 | Microsoft Docs"
ms.custom: 
ms.date: 11/04/2016
ms.reviewer: 
ms.suite: 
ms.technology:
- cpp-tools
ms.tgt_pltfrm: 
ms.topic: error-reference
f1_keywords:
- C2612
dev_langs:
- C++
helpviewer_keywords:
- C2612
ms.assetid: 6faacfd6-4455-41a2-808e-0f6799f84d6d
caps.latest.revision: 7
author: corob-msft
ms.author: corob
manager: ghogen
ms.translationtype: MT
ms.sourcegitcommit: 35b46e23aeb5f4dbfd2a0dd44b906389dd5bfc88
ms.openlocfilehash: 51859278f3f1651bfa183eaaeaeae25802fd8cf7
ms.contentlocale: ko-kr
ms.lasthandoff: 10/10/2017

---
# <a name="compiler-error-c2612"></a>컴파일러 오류 C2612
'char' 기본/멤버 이니셜라이저 목록에 잘못 된 후행  
  
 마지막 기본 또는 멤버 이니셜라이저 목록에서 다음에 문자가 표시 합니다.  
  
 다음 샘플에서는 C2612 오류가 생성 됩니다.  
  
```  
// C2612.cpp  
class A {  
public:  
   int i;  
   A( int ia ) : i( ia ) + {};   // C2612  
};  
```
