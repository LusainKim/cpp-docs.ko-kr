---
title: "컴파일러 오류 C2931 | Microsoft Docs"
ms.custom: 
ms.date: 11/04/2016
ms.reviewer: 
ms.suite: 
ms.technology: cpp-tools
ms.tgt_pltfrm: 
ms.topic: article
f1_keywords: C2931
dev_langs: C++
helpviewer_keywords: C2931
ms.assetid: 33430407-b149-4ba3-baf8-b0dae1ea3a5d
caps.latest.revision: "9"
author: corob-msft
ms.author: corob
manager: ghogen
ms.openlocfilehash: 8b8289508c84b24a5077be2160a7915900d3619a
ms.sourcegitcommit: ebec1d449f2bd98aa851667c2bfeb7e27ce657b2
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 10/24/2017
---
# <a name="compiler-error-c2931"></a>컴파일러 오류 C2931
'class': type-class-id가 'identifier'의 멤버 함수로 다시 정의되었습니다.  
  
 제네릭 또는 템플릿 클래스를 다른 클래스의 멤버 함수로 사용할 수 없습니다.  
  
 중괄호가 짝이 맞지 않는 경우 이 오류가 발생할 수 있습니다.  
  
 다음 샘플에서는 C2931을 생성합니다.  
  
```  
// C2931.cpp  
// compile with: /c  
template<class T>   
struct TC { };   
struct MyStruct {  
   void TC<int>();   // C2931  
};  
  
struct TC2 { };   
struct MyStruct2 {  
   void TC2();  
};  
```  
  
 C2931은 제네릭을 사용하는 경우에도 발생할 수 있습니다.  
  
```  
// C2931b.cpp  
// compile with: /clr /c  
generic<class T> ref struct GC {};  
struct MyStruct {  
   void GC<int>();   // C2931  
   void GC2();   // OK  
};  
```