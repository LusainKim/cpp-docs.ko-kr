---
title: "컴파일러 오류 C2932 | Microsoft Docs"
ms.custom: 
ms.date: 11/04/2016
ms.reviewer: 
ms.suite: 
ms.technology:
- cpp-tools
ms.tgt_pltfrm: 
ms.topic: article
f1_keywords:
- C2932
dev_langs:
- C++
helpviewer_keywords:
- C2932
ms.assetid: c28e88d9-e654-4367-bfb4-13c780bca9bd
caps.latest.revision: 9
author: corob-msft
ms.author: corob
manager: ghogen
ms.translationtype: MT
ms.sourcegitcommit: 35b46e23aeb5f4dbfd2a0dd44b906389dd5bfc88
ms.openlocfilehash: 49565a60a6623e80b1d367bf3d341cfe60b639af
ms.contentlocale: ko-kr
ms.lasthandoff: 10/10/2017

---
# <a name="compiler-error-c2932"></a>컴파일러 오류 C2932
'class': type-class-id가 'identifier'의 데이터 멤버로 재정의되었습니다.  
  
 제네릭 또는 템플릿 클래스를 데이터 멤버로 사용할 수 없습니다.  
  
 다음 샘플에서는 C2932를 생성합니다.  
  
```  
// C2932.cpp  
// compile with: /c  
template<class T>   
struct TC {};   
  
struct MyStruct {  
   int TC<int>;   // C2932  
   int TC;   // OK  
};  
```  
  
 C2932는 제네릭을 사용하는 경우에도 발생할 수 있습니다.  
  
```  
// C2932b.cpp  
// compile with: /clr /c  
generic<class T>  
ref struct GC {};  
  
struct MyStruct {  
   int GC<int>;   // C2932  
   int GC;   // OK  
};  
```
