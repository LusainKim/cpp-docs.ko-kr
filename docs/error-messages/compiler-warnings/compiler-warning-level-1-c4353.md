---
title: "컴파일러 경고 (수준 1) C4353 | Microsoft Docs"
ms.custom: 
ms.date: 11/04/2016
ms.reviewer: 
ms.suite: 
ms.technology: cpp-tools
ms.tgt_pltfrm: 
ms.topic: error-reference
f1_keywords: C4353
dev_langs: C++
helpviewer_keywords: C4353
ms.assetid: 6e79f186-ed82-4c95-9923-0ad5bb9c4db1
caps.latest.revision: "7"
author: corob-msft
ms.author: corob
manager: ghogen
ms.workload: cplusplus
ms.openlocfilehash: 8dd3ec65dac6720509b9c918f272d2eb6ff2720c
ms.sourcegitcommit: 8fa8fdf0fbb4f57950f1e8f4f9b81b4d39ec7d7a
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 12/21/2017
---
# <a name="compiler-warning-level-1-c4353"></a>컴파일러 경고(수준 1) C4353
비표준 확장이 사용 됨: 함수 식으로 상수 0입니다. 내장 '__noop' 함수를 사용  
  
 함수 식으로 상수 영 (0)를 사용할 수 없습니다. 자세한 내용은 참조 [__noop](../../intrinsics/noop.md)합니다.  
  
 다음 샘플에서는 C4353 오류가 생성 됩니다.  
  
```  
// C4353.cpp  
// compile with: /W1  
void MyPrintf(void){};  
#define X 0  
#if X  
   #define DBPRINT MyPrint  
#else  
   #define DBPRINT 0   // C4353 expected  
#endif  
int main(){  
DBPRINT();  
}  
```