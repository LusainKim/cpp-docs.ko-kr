---
title: "컴파일러 경고 (수준 4) C4515 | Microsoft Docs"
ms.custom: 
ms.date: 11/04/2016
ms.reviewer: 
ms.suite: 
ms.technology: cpp-tools
ms.tgt_pltfrm: 
ms.topic: error-reference
f1_keywords: C4515
dev_langs: C++
helpviewer_keywords: C4515
ms.assetid: 167b5177-3f89-418b-b6c8-7de634f6b28f
caps.latest.revision: "6"
author: corob-msft
ms.author: corob
manager: ghogen
ms.workload: cplusplus
ms.openlocfilehash: 53fbb6ad008ab004d689dcd8dbb0a1e3341256d5
ms.sourcegitcommit: 8fa8fdf0fbb4f57950f1e8f4f9b81b4d39ec7d7a
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 12/21/2017
---
# <a name="compiler-warning-level-4-c4515"></a>컴파일러 경고(수준 4) C4515
'namespace': 네임 스페이스 자체를 사용 합니다.  
  
 네임 스페이스를 재귀적으로 사용된 합니다.  
  
 다음 샘플에서는 C4515 오류가 생성 됩니다.  
  
```  
// C4515.cpp  
// compile with: /W4  
namespace A  
{  
   using namespace A; // C4515  
}  
  
int main()  
{  
}  
```