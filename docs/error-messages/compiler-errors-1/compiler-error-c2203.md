---
title: "컴파일러 오류 C2203 | Microsoft Docs"
ms.custom: 
ms.date: 11/04/2016
ms.reviewer: 
ms.suite: 
ms.technology: cpp-tools
ms.tgt_pltfrm: 
ms.topic: error-reference
f1_keywords: C2203
dev_langs: C++
helpviewer_keywords: C2203
ms.assetid: 5497df43-86f6-43d5-b6cb-723c4c589b10
caps.latest.revision: "9"
author: corob-msft
ms.author: corob
manager: ghogen
ms.workload: cplusplus
ms.openlocfilehash: 659dfe24cb2c5181192eb4ba910d641484bcbf7e
ms.sourcegitcommit: 8fa8fdf0fbb4f57950f1e8f4f9b81b4d39ec7d7a
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 12/21/2017
---
# <a name="compiler-error-c2203"></a>컴파일러 오류 C2203
delete 연산자는 배열의 범위를 지정할 수 없습니다  
  
 와 **/Za** (ANSI) 옵션은 `delete` 운영자 배열 전체 되지만 파트 나 배열의 특정 멤버를 삭제할 수 있습니다.  
  
 다음 샘플에서는 C2203 오류가 생성 됩니다.  
  
```  
// C2203.cpp  
// compile with: /Za  
int main() {  
   int *ar = new int[10];  
   delete [4] ar;   // C2203  
   // try the following line instead  
   // delete [] ar;  
}  
```