---
title: "컴파일러 오류 C2788 | Microsoft Docs"
ms.custom: 
ms.date: 11/04/2016
ms.reviewer: 
ms.suite: 
ms.technology: cpp-tools
ms.tgt_pltfrm: 
ms.topic: error-reference
f1_keywords: C2788
dev_langs: C++
helpviewer_keywords: C2788
ms.assetid: 8688fc5c-e652-43b4-b407-9c488c76f2db
caps.latest.revision: "9"
author: corob-msft
ms.author: corob
manager: ghogen
ms.workload: cplusplus
ms.openlocfilehash: 3629bb6d9196f8f1f24daea581f581c805d4b542
ms.sourcegitcommit: 8fa8fdf0fbb4f57950f1e8f4f9b81b4d39ec7d7a
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 12/21/2017
---
# <a name="compiler-error-c2788"></a>컴파일러 오류 C2788
'identifier':이 개체와 관련 된 둘 이상의 GUID  
  
 [__uuidof](../../cpp/uuidof-operator.md) 연산자는 연결 된 GUID 또는 사용자 정의 형식의 개체와 사용자 정의 형식을 사용 합니다. 이 오류는 인수가 개체가 여러 Guid 포함 하는 경우에 발생 합니다.  
  
 다음 샘플에서는 C2788 오류가 생성 됩니다.  
  
```  
// C2788.cpp  
#include <windows.h>  
struct __declspec(uuid("00000001-0000-0000-0000-000000000000")) A {};  
struct __declspec(uuid("{00000002-0000-0000-0000-000000000000}")) B {};  
template <class T, class U> class MyClass {};  
  
typedef MyClass<A,B> MyBadClass;  
typedef MyClass<A,A> MyGoodClass;  
  
int main() {  
   __uuidof(MyBadClass);    // C2788  
   // try the following line instead  
   __uuidof(MyGoodClass);  
}  
```