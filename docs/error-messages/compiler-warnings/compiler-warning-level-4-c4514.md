---
title: "컴파일러 경고 (수준 4) C4514 | Microsoft Docs"
ms.custom: 
ms.date: 11/04/2016
ms.reviewer: 
ms.suite: 
ms.technology: cpp-tools
ms.tgt_pltfrm: 
ms.topic: error-reference
f1_keywords: C4514
dev_langs: C++
helpviewer_keywords: C4514
ms.assetid: cdae966a-9cd4-4e31-af30-2a014e68f614
caps.latest.revision: "7"
author: corob-msft
ms.author: corob
manager: ghogen
ms.workload: cplusplus
ms.openlocfilehash: b6c9ac776c108a84c813ca814bc674dec4999e31
ms.sourcegitcommit: 8fa8fdf0fbb4f57950f1e8f4f9b81b4d39ec7d7a
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 12/21/2017
---
# <a name="compiler-warning-level-4-c4514"></a>컴파일러 경고(수준 4) C4514
'function': 참조 되지 않은 인라인 함수를 제거  
  
 최적화 프로그램 제거 인라인 함수를 호출 하지 않습니다.  
  
 기본적으로 이 경고는 해제되어 있습니다. 자세한 내용은 [기본적으로 해제되어 있는 컴파일러 경고](../../preprocessor/compiler-warnings-that-are-off-by-default.md) 를 참조하세요.  
  
 다음 샘플에서는 C4514 오류가 생성 됩니다.  
  
```  
// C4514.cpp  
// compile with: /W4  
#pragma warning(default : 4514)  
class A  
{  
   public:  
      void func()   // C4514, remove the function to resolve  
      {  
      }  
};  
  
int main()  
{  
}  
```