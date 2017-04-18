---
title: "컴파일러 오류 C3211 | Microsoft Docs"
ms.custom: 
ms.date: 11/04/2016
ms.reviewer: 
ms.suite: 
ms.technology:
- devlang-cpp
ms.tgt_pltfrm: 
ms.topic: article
f1_keywords:
- C3211
dev_langs:
- C++
helpviewer_keywords:
- C3211
ms.assetid: 85e33fed-3b59-4315-97e6-20d31c6a985a
caps.latest.revision: 6
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
translationtype: Machine Translation
ms.sourcegitcommit: 0d9cbb01d1ad0f2ea65d59334cb88140ef18fce0
ms.openlocfilehash: bba7dc1f5001b199d0789d681a9f9ad01cdabee2
ms.lasthandoff: 04/12/2017

---
# <a name="compiler-error-c3211"></a>컴파일러 오류 C3211
'explicit specialization': 명시적 특수화에 부분 특수화 구문이 사용되고 있습니다. template <>을 사용하세요.  
  
 명시적 특수화의 형식이 잘못되었습니다.  
  
 다음 샘플에서는 C3211을 생성합니다.  
  
```  
// C3211.cpp  
// compile with: /LD  
template<class T>  
struct s;  
  
template<class T>  
// use the following line instead  
// template<>  
struct s<int>{};   // C3211  
```
