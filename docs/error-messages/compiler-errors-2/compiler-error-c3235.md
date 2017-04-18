---
title: "컴파일러 오류 C3235 | Microsoft Docs"
ms.custom: 
ms.date: 11/04/2016
ms.reviewer: 
ms.suite: 
ms.technology:
- devlang-cpp
ms.tgt_pltfrm: 
ms.topic: article
f1_keywords:
- C3235
dev_langs:
- C++
helpviewer_keywords:
- C3235
ms.assetid: 0554d6c7-e1dc-4c99-8934-cbcf491c8203
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
translationtype: Machine Translation
ms.sourcegitcommit: 0d9cbb01d1ad0f2ea65d59334cb88140ef18fce0
ms.openlocfilehash: 80266394412670630be665f43b86dea611b4a463
ms.lasthandoff: 04/12/2017

---
# <a name="compiler-error-c3235"></a>컴파일러 오류 C3235
'specialization': 제네릭 클래스의 명시적 특수화 또는 부분 특수화는 허용되지 않습니다.  
  
 명시적 특수화 또는 부분 특수화에 제네릭 클래스를 사용할 수 없습니다.  
  
## <a name="example"></a>예제  
 다음 샘플에서는 C3235를 생성합니다.  
  
```  
// C3235.cpp  
// compile with: /clr  
generic<class T>  
public ref class C {};  
  
generic<>  
public ref class C<int> {};   // C3235 Remove this specialization to resolve this error.  
```
