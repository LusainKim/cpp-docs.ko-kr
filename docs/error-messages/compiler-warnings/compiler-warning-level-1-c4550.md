---
title: "컴파일러 경고 (수준 1) C4550 | Microsoft Docs"
ms.custom: 
ms.date: 11/04/2016
ms.reviewer: 
ms.suite: 
ms.technology: cpp-tools
ms.tgt_pltfrm: 
ms.topic: error-reference
f1_keywords: C4550
dev_langs: C++
helpviewer_keywords: C4550
ms.assetid: f902b4ed-5f17-48ea-b693-92f4fb8c8054
caps.latest.revision: "6"
author: corob-msft
ms.author: corob
manager: ghogen
ms.workload: cplusplus
ms.openlocfilehash: 08b0e586500b4de2ed0005d118f6302e67ecc7d1
ms.sourcegitcommit: 8fa8fdf0fbb4f57950f1e8f4f9b81b4d39ec7d7a
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 12/21/2017
---
# <a name="compiler-warning-level-1-c4550"></a>컴파일러 경고(수준 1) C4550
식이 인수 목록이 없는 함수로 계산  
  
 함수에 대 한 역참조 포인터에 인수 목록이 없습니다.  
  
## <a name="example"></a>예  
  
```  
// C4550.cpp  
// compile with: /W1  
bool f()  
{  
   return true;  
}  
  
typedef bool (*pf_t)();  
  
int main()  
{  
   pf_t pf = f;  
   if (*pf) {}  // C4550  
   return 0;  
}  
```