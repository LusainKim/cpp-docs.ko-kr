---
title: "컴파일러 오류 C2807 | Microsoft Docs"
ms.custom: 
ms.date: 11/04/2016
ms.reviewer: 
ms.suite: 
ms.technology: cpp-tools
ms.tgt_pltfrm: 
ms.topic: error-reference
f1_keywords: C2807
dev_langs: C++
helpviewer_keywords: C2807
ms.assetid: bd7a207a-f379-4de6-8ee8-c7cab78b3480
caps.latest.revision: "7"
author: corob-msft
ms.author: corob
manager: ghogen
ms.workload: cplusplus
ms.openlocfilehash: a4d8954b74983ed790bdcf3d559cc23d6c38751c
ms.sourcegitcommit: 8fa8fdf0fbb4f57950f1e8f4f9b81b4d39ec7d7a
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 12/21/2017
---
# <a name="compiler-error-c2807"></a>컴파일러 오류 C2807
'operator 연산자' 후 위 두 번째 형식 매개 변수 'int' 여야 합니다.  
  
 후 위 연산자는 두 번째 매개 변수 형식이 잘못 되었습니다.  
  
 다음 샘플에서는 C2807 오류가 생성 됩니다.  
  
```  
// C2807.cpp  
// compile with: /c  
class X {  
public:  
   X operator++ ( X );   // C2807 nonvoid parameter  
   X operator++ ( int );   // OK, int parameter  
};  
```