---
title: "컴파일러 경고 (수준 1) C4076 | Microsoft Docs"
ms.custom: 
ms.date: 11/04/2016
ms.reviewer: 
ms.suite: 
ms.technology:
- cpp-tools
ms.tgt_pltfrm: 
ms.topic: article
f1_keywords:
- C4076
dev_langs:
- C++
helpviewer_keywords:
- C4076
ms.assetid: 04581066-313a-4a11-bb60-721e6d038d75
caps.latest.revision: 7
author: corob-msft
ms.author: corob
manager: ghogen
translation.priority.ht:
- de-de
- es-es
- fr-fr
- it-it
- ja-jp
- ko-kr
- ru-ru
- zh-cn
- zh-tw
translation.priority.mt:
- cs-cz
- pl-pl
- pt-br
- tr-tr
ms.translationtype: Machine Translation
ms.sourcegitcommit: 0d9cbb01d1ad0f2ea65d59334cb88140ef18fce0
ms.openlocfilehash: 2ab3c4160dfe920073c54854311bd58a5db422bb
ms.contentlocale: ko-kr
ms.lasthandoff: 04/12/2017

---
# <a name="compiler-warning-level-1-c4076"></a>컴파일러 경고(수준 1) C4076
'typemod': 'typename' 형식과 함께 사용할 수 없습니다.  
  
 **signed** 또는 `unsigned`인지에 관계없이 형식 한정자는 정수가 아닌 형식과 함께 사용할 수 없습니다. ***typemod*** 는 무시됩니다.  
  
## <a name="example"></a>예제  
 다음 샘플에서는 C4076을 생성합니다.  
  
```  
// C4076.cpp  
// compile with: /W1 /LD  
unsigned double x;   // C4076  
```
