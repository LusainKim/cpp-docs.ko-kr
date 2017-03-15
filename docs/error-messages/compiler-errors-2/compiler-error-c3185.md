---
title: "컴파일러 오류 C3185 | Microsoft 문서"
ms.custom: 
ms.date: 11/04/2016
ms.reviewer: 
ms.suite: 
ms.technology:
- devlang-cpp
ms.tgt_pltfrm: 
ms.topic: error-reference
f1_keywords:
- C3185
dev_langs:
- C++
helpviewer_keywords:
- C3185
ms.assetid: 5bf96279-043c-4981-9d02-b4550071b192
caps.latest.revision: 13
author: corob-msft
ms.author: corob
manager: ghogen
translation.priority.ht:
- cs-cz
- de-de
- es-es
- fr-fr
- it-it
- ja-jp
- ko-kr
- pl-pl
- pt-br
- ru-ru
- tr-tr
- zh-cn
- zh-tw
translationtype: Machine Translation
ms.sourcegitcommit: c243063a9770542f137d5950e8a269f771960f74
ms.openlocfilehash: 8772b939def79269dd46375c1e8db5d5dacc5f74
ms.lasthandoff: 02/24/2017

---
# <a name="compiler-error-c3185"></a>컴파일러 오류 C3185
'typeid' : 관리되는 형식 또는 WinRT 형식 'type'에 사용되었습니다. 대신 'operator'를 사용하세요.  
  
 적용할 수 없습니다는 [typeid](../../cpp/typeid-operator.md) 를 관리 되는 연산자 또는 WinRT 이때 입력 하 고 사용 하 여 [typeid](../../windows/typeid-cpp-component-extensions.md) 대신 합니다.  
  
 다음 샘플에서는 C3185 오류가 발생하는 경우 및 이를 해결하는 방법을 보여 줍니다.  
  
```  
// C3185a.cpp  
// compile with: /clr  
ref class Base {};  
ref class Derived : public Base {};  
  
int main() {  
   Derived ^ pd = gcnew Derived;  
   Base ^pb = pd;  
   const type_info & t1 = typeid(pb);   // C3185  
   System::Type ^ MyType = Base::typeid;   // OK  
};  
```  

