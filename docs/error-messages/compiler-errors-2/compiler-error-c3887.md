---
title: "컴파일러 오류 C3887 | Microsoft Docs"
ms.custom: 
ms.date: 11/04/2016
ms.reviewer: 
ms.suite: 
ms.technology: cpp-tools
ms.tgt_pltfrm: 
ms.topic: error-reference
f1_keywords: C3887
dev_langs: C++
helpviewer_keywords: C3887
ms.assetid: a7e82426-ef99-437b-9562-2822004e18fe
caps.latest.revision: "7"
author: corob-msft
ms.author: corob
manager: ghogen
ms.workload: cplusplus
ms.openlocfilehash: 6ffa92a9984f982c1a71f1417f0f17c8ee36d4c4
ms.sourcegitcommit: 8fa8fdf0fbb4f57950f1e8f4f9b81b4d39ec7d7a
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 12/21/2017
---
# <a name="compiler-error-c3887"></a>컴파일러 오류 C3887
'var': 리터럴 데이터 멤버에 대 한 이니셜라이저는 상수 식 이어야 합니다.  
  
 A [리터럴](../../windows/literal-cpp-component-extensions.md) 데이터 멤버는 상수 식만 초기화 될 수 있습니다.  
  
 다음 샘플에서는 C3887 오류가 생성 됩니다.  
  
```  
// C3887.cpp  
// compile with: /clr  
ref struct Y1 {  
   static int i = 9;  
   literal  
   int staticConst = i;   // C3887  
};  
```  
  
 해결 방법:  
  
```  
// C3887b.cpp  
// compile with: /clr /c  
ref struct Y1 {  
   literal  
   int staticConst = 9;  
};  
```