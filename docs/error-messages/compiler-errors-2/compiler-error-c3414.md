---
title: "컴파일러 오류 C3414 | Microsoft Docs"
ms.custom: 
ms.date: 11/04/2016
ms.reviewer: 
ms.suite: 
ms.technology: cpp-tools
ms.tgt_pltfrm: 
ms.topic: error-reference
f1_keywords: C3414
dev_langs: C++
helpviewer_keywords: C3414
ms.assetid: 715f5432-b509-4f8f-84f5-e1463bac490f
caps.latest.revision: "8"
author: corob-msft
ms.author: corob
manager: ghogen
ms.workload: cplusplus
ms.openlocfilehash: 7bc2ded1e32d68a14f8cc34ce12beb290757e81e
ms.sourcegitcommit: 8fa8fdf0fbb4f57950f1e8f4f9b81b4d39ec7d7a
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 12/21/2017
---
# <a name="compiler-error-c3414"></a>컴파일러 오류 C3414
'member': 가져온된 멤버 함수를 정의할 수 없습니다.  
  
 멤버는 참조 된 어셈블리에 정의 된 코드에 정의 되었습니다.  
  
 다음 샘플에서는 C3414 오류가 생성 됩니다.  
  
```  
// C3414a2.cpp  
// compile with: /clr /LD  
public ref class MyClass {  
public:  
   void Test(){}  
};  
```  
  
 그리고  
  
```  
// C3414b2.cpp  
// compile with: /clr  
#using <C3414a2.dll>  
  
void MyClass::Test() {    // C3414  
}  
  
System::Object::Object() {    // C3414  
}  
```  
