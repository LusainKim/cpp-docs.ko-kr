---
title: "컴파일러 오류 C2766 | Microsoft Docs"
ms.custom: 
ms.date: 11/04/2016
ms.reviewer: 
ms.suite: 
ms.technology: cpp-tools
ms.tgt_pltfrm: 
ms.topic: error-reference
f1_keywords: C2766
dev_langs: C++
helpviewer_keywords: C2766
ms.assetid: 8032f4ca-6827-4f04-9c61-c44643c85cc4
caps.latest.revision: "9"
author: corob-msft
ms.author: corob
manager: ghogen
ms.workload: cplusplus
ms.openlocfilehash: 795e2fe63a9252a5d6ab4b05f3666e975c997ebc
ms.sourcegitcommit: 8fa8fdf0fbb4f57950f1e8f4f9b81b4d39ec7d7a
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 12/21/2017
---
# <a name="compiler-error-c2766"></a>컴파일러 오류 C2766
명시적 특수화. 'specialization'가 이미 정의 되어  
  
 중복 된 명시적 특수화는 허용 되지 않습니다. 자세한 내용은 참조 [명시적 함수 템플릿의 특수화](../../cpp/explicit-specialization-of-function-templates.md)합니다.  
  
 다음 샘플에서는 C2766 오류가 생성 됩니다.  
  
```  
// C2766.cpp  
// compile with: /c  
template<class T>   
struct A {};  
  
template<>   
struct A<int> {};  
  
template<>   
struct A<int> {};   // C2766  
// try the following line instead  
// struct A<char> {};  
```