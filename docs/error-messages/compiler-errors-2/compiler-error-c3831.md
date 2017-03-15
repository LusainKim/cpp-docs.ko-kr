---
title: "컴파일러 오류 C3831 | Microsoft 문서"
ms.custom: 
ms.date: 11/04/2016
ms.reviewer: 
ms.suite: 
ms.technology:
- devlang-cpp
ms.tgt_pltfrm: 
ms.topic: error-reference
f1_keywords:
- C3831
dev_langs:
- C++
helpviewer_keywords:
- C3831
ms.assetid: a125d8dc-b75a-4ea0-b6c7-fe7b119dba25
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
ms.openlocfilehash: 9b0dc2a5da701c94408e79053df721af38cada62
ms.lasthandoff: 02/24/2017

---
# <a name="compiler-error-c3831"></a>컴파일러 오류 C3831
'member': 'class'는 고정 된 데이터 멤버 또는 고정 포인터를 반환 하는 멤버 함수 여야 합니다.  
  
 [pin_ptr (C + + /cli CLI)](../../windows/pin-ptr-cpp-cli.md) 잘못 사용 했습니다.  
  
## <a name="example"></a>예제  
 다음 샘플에서는 C3831 오류가 생성 됩니다.  
  
```  
// C3831a.cpp  
// compile with: /clr  
ref class Y  
{  
public:  
   int i;  
};  
  
ref class X  
{  
   pin_ptr<int> mbr_Y;   // C3831  
   int^ mbr_Y2;   // OK  
};  
  
int main() {  
   Y y;  
   pin_ptr<int> p = &y.i;  
}  
```  

