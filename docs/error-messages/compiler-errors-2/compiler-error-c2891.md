---
title: "컴파일러 오류 C2891 | Microsoft Docs"
ms.custom: 
ms.date: 11/04/2016
ms.reviewer: 
ms.suite: 
ms.technology: cpp-tools
ms.tgt_pltfrm: 
ms.topic: error-reference
f1_keywords: C2891
dev_langs: C++
helpviewer_keywords: C2891
ms.assetid: e12cfb2d-df45-4b0d-b155-c51d17e812fa
caps.latest.revision: "7"
author: corob-msft
ms.author: corob
manager: ghogen
ms.workload: cplusplus
ms.openlocfilehash: 979d77ad5b5bd0b68dd539695d6cb1b60b099c55
ms.sourcegitcommit: 8fa8fdf0fbb4f57950f1e8f4f9b81b4d39ec7d7a
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 12/21/2017
---
# <a name="compiler-error-c2891"></a>컴파일러 오류 C2891
'parameter': 템플릿 매개 변수의 주소를 가져올 수 없습니다  
  
 Lvalue 경우가 아니라면 템플릿 매개 변수 주소를 가져올 수 없습니다. 형식 매개 변수가 주소가 없기 때문에 lvalue 않습니다. Lvalue 없는 템플릿 매개 변수 목록에 비형식 값도 주소를가지고 하지 않습니다. 이 템플릿 매개 변수로 전달 된 값에는 템플릿 인수는 컴파일러 생성 복사 이므로 컴파일러 오류 C2891 하는 코드의 예시입니다.  
  
```  
template <int i> int* f() { return &i; }  
```  
  
 템플릿 매개 변수를 lvalue 참조 형식에 같은 수의 주소는 수행 했습니다.  
  
```  
template <int& r> int* f() { return &r; }  
```  
  
 이 오류를 해결 하려면 lvalue 하지 않은 주소는 템플릿 매개 변수를 사용 하지 않습니다.