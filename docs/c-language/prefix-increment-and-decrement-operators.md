---
title: "접두사 증가 및 감소 연산자 | Microsoft Docs"
ms.custom: 
ms.date: 11/04/2016
ms.reviewer: 
ms.suite: 
ms.technology: cpp-language
ms.tgt_pltfrm: 
ms.topic: article
dev_langs: C++
helpviewer_keywords:
- increment operators, types of
- decrement operators, syntax
- decrement operators
ms.assetid: 9a441bb9-d94a-4b6a-9db2-0d0d76bc480d
caps.latest.revision: "6"
author: mikeblome
ms.author: mblome
manager: ghogen
ms.workload: cplusplus
ms.openlocfilehash: 84d8c3f5a1b43fdec5554003e32db4f23b4f0406
ms.sourcegitcommit: 8fa8fdf0fbb4f57950f1e8f4f9b81b4d39ec7d7a
ms.translationtype: HT
ms.contentlocale: ko-KR
ms.lasthandoff: 12/21/2017
---
# <a name="prefix-increment-and-decrement-operators"></a>접두사 증가 및 감소 연산자
증가 또는 감소 연산자가 피연산자 앞에 올 때 단항 연산자(`++` 및 **--**)를 "접두사" 증가 또는 감소 연산자라고 합니다. 후위 증가 및 감소는 전위 증가 및 감소보다 우선 순위가 높습니다. 피연산자는 정수, 부동 및 포인터 형식이어야 하며 수정할 수 있는 l-value 식(**const** 특성이 없는 식)이어야 합니다. 결과는 l-value입니다.  
  
 연산자가 피연산자 앞에 오면 피연산자가 증가하거나 감소하고 새 값이 식의 결과가 됩니다.  
  
 정수 계열 또는 부동 형식의 피연산자는 정수 값 1만큼 증가하거나 감소합니다. 결과 형식은 피연산자 형식과 동일합니다. 포인터 형식의 피연산자는 자신이 처리하는 개체의 크기만큼 증가하거나 감소합니다. 증가한 포인터는 다음 개체를 가리키고, 감소한 포인터는 이전 개체를 가리킵니다.  
  
## <a name="example"></a>예  
 이 예제에서는 단항 전위 감소 연산자를 보여 줍니다.  
  
```  
if( line[--i] != '\n' )  
    return;  
```  
  
 이 예제에서 `i` 변수가 `line`의 첨자로 사용되기 전에 감소합니다.  
  
## <a name="see-also"></a>참고 항목  
 [C 단항 연산자](../c-language/c-unary-operators.md)