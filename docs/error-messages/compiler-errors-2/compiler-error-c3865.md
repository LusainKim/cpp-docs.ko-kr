---
title: "컴파일러 오류 C3865 | Microsoft Docs"
ms.custom: 
ms.date: 11/04/2016
ms.reviewer: 
ms.suite: 
ms.technology: cpp-tools
ms.tgt_pltfrm: 
ms.topic: error-reference
f1_keywords: C3865
dev_langs: C++
helpviewer_keywords: C3865
ms.assetid: 9bc62bb0-4fb8-4856-a5cf-c7cb4029a596
caps.latest.revision: "9"
author: corob-msft
ms.author: corob
manager: ghogen
ms.workload: cplusplus
ms.openlocfilehash: cec5eabe6f4fa62648e9d3787d8ef2d2133f7736
ms.sourcegitcommit: 8fa8fdf0fbb4f57950f1e8f4f9b81b4d39ec7d7a
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 12/21/2017
---
# <a name="compiler-error-c3865"></a>컴파일러 오류 C3865
'calling_convention': 네이티브 멤버 함수에만 사용할 수  
  
 호출 규칙은 관리 되는 멤버 함수 또는 함수를 전역 함수에 사용 되었습니다. 호출 규칙 (관리 되지 않음) 네이티브 멤버 함수에만 사용할 수 있습니다.  
  
 자세한 내용은 참조 [호출 규칙](../../cpp/calling-conventions.md)합니다.  
  
 다음 샘플에서는 C3865 오류가 생성 됩니다.  
  
```  
// C3865.cpp  
// compile with: /clr  
// processor: x86  
void __thiscall Func(){}   // C3865  
  
// OK  
struct MyType {  
   void __thiscall Func(){}  
};  
```