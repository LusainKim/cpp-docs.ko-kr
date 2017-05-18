---
title: "컴파일러 오류 C2344 | Microsoft Docs"
ms.custom: 
ms.date: 11/04/2016
ms.reviewer: 
ms.suite: 
ms.technology:
- cpp-tools
ms.tgt_pltfrm: 
ms.topic: article
f1_keywords:
- C2344
dev_langs:
- C++
helpviewer_keywords:
- C2344
ms.assetid: a84c7b37-c84e-4345-8691-c23abb2dc193
caps.latest.revision: 9
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
ms.openlocfilehash: 175d379fe1c74cc9696a965de559eeef39884d74
ms.contentlocale: ko-kr
ms.lasthandoff: 04/12/2017

---
# <a name="compiler-error-c2344"></a>컴파일러 오류 C2344
align(#): 맞춤은 2의 거듭제곱이어야 합니다.  
  
 사용 하는 경우는 [맞춤](../../cpp/align-cpp.md) 키워드에 전달 하는 값 2의 거듭제곱 이어야 합니다.  
  
 예를 들어 3은 2의 거듭제곱이 아니므로 다음 코드는 C2344를 생성합니다.  
  
```  
// C2344.cpp  
// compile with: /c  
__declspec(align(3)) int a;   // C2344  
__declspec(align(4)) int b;   // OK  
```
