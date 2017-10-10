---
title: "컴파일러 오류 C2246 | Microsoft Docs"
ms.custom: 
ms.date: 11/04/2016
ms.reviewer: 
ms.suite: 
ms.technology:
- cpp-tools
ms.tgt_pltfrm: 
ms.topic: article
f1_keywords:
- C2246
dev_langs:
- C++
helpviewer_keywords:
- C2246
ms.assetid: 4f3e4f83-21f3-4256-af96-43e0bb060311
caps.latest.revision: 9
author: corob-msft
ms.author: corob
manager: ghogen
ms.translationtype: MT
ms.sourcegitcommit: 35b46e23aeb5f4dbfd2a0dd44b906389dd5bfc88
ms.openlocfilehash: ce194e9f08655e0acc7d1dab53f2a2392cceb4f4
ms.contentlocale: ko-kr
ms.lasthandoff: 10/09/2017

---
# <a name="compiler-error-c2246"></a>컴파일러 오류 C2246
'identifier': 지역으로 정의된 클래스에 잘못된 정적 데이터 멤버가 있습니다.  
  
 로컬 범위를 가진 클래스, 구조체 또는 공용 구조체의 멤버가 `static`으로 선언되었습니다.  
  
 다음 샘플에서는 C2246을 생성합니다.  
  
```  
// C2246.cpp  
// compile with: /c  
void func( void ) {  
   class A { static int i; };   // C2246  i is local to func  
   static int j;   // OK  
};  
```
