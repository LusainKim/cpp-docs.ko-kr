---
title: "컴파일러 오류 C2611 | Microsoft Docs"
ms.custom: 
ms.date: 11/04/2016
ms.reviewer: 
ms.suite: 
ms.technology: cpp-tools
ms.tgt_pltfrm: 
ms.topic: error-reference
f1_keywords: C2611
dev_langs: C++
helpviewer_keywords: C2611
ms.assetid: 3f2d5253-f24f-4724-83d0-6b2aa6a4e551
caps.latest.revision: "8"
author: corob-msft
ms.author: corob
manager: ghogen
ms.workload: cplusplus
ms.openlocfilehash: e079376bcdf77d03e4f6d3ccc2db74d0d292af2e
ms.sourcegitcommit: 8fa8fdf0fbb4f57950f1e8f4f9b81b4d39ec7d7a
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 12/21/2017
---
# <a name="compiler-error-c2611"></a>컴파일러 오류 C2611
'token': 잘못 된 다음 ' ~' (식별자가 필요)  
  
 토큰은 식별자가 아닙니다.  
  
 다음 샘플에서는 C2611 오류가 생성 됩니다.  
  
```  
// C2611.cpp  
// compile with: /c  
class C {  
   C::~operator int();   // C2611  
   ~C();   // OK  
};  
```