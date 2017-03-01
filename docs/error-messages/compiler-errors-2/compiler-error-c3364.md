---
title: "컴파일러 오류 C3364 | Microsoft 문서"
ms.custom: 
ms.date: 11/04/2016
ms.reviewer: 
ms.suite: 
ms.technology:
- devlang-cpp
ms.tgt_pltfrm: 
ms.topic: error-reference
f1_keywords:
- C3364
dev_langs:
- C++
helpviewer_keywords:
- C3364
ms.assetid: 98654741-60fe-4472-a6af-e580f8c0a6e1
caps.latest.revision: 8
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
ms.openlocfilehash: 783e05439168a63c21a3900c993813dd973a642a
ms.lasthandoff: 02/24/2017

---
# <a name="compiler-error-c3364"></a>컴파일러 오류 C3364
'delegate': 대리자 생성자: 인수는 관리 되는 클래스의 멤버 함수 또는 전역 함수에 대 한 포인터 여야 합니다.  
  
 대리자 생성자의 두 번째 매개 변수 멤버 함수의 주소 또는 모든 클래스의 정적 멤버 함수의 주소를 사용 합니다. 둘 다 단순 주소로 처리 됩니다.  
  
 다음 샘플에서는 C3364 오류가 생성 됩니다.  
  
```  
// C3364_2.cpp  
// compile with: /clr  
  
delegate int D( int, int );  
  
ref class C {  
public:  
   int mf( int, int ) {  
      return 1;  
   }  
};  
  
int main() {  
   C^ pC = gcnew C;  
   System::Delegate^ pD = gcnew D( pC,pC->mf( 1, 2 ) ); // C3364  
  
   // try the following line instead  
   // System::Delegate^ pD = gcnew D(pC, &C::mf);  
}  
```  

