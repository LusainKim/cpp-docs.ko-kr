---
title: "컴파일러 오류 C2094 | Microsoft 문서"
ms.custom: 
ms.date: 11/04/2016
ms.reviewer: 
ms.suite: 
ms.technology:
- cpp-tools
ms.tgt_pltfrm: 
ms.topic: article
f1_keywords:
- C2094
dev_langs:
- C++
helpviewer_keywords:
- C2094
ms.assetid: 9e4f8f88-f189-46e7-91c9-481bacc7af87
caps.latest.revision: 8
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
ms.translationtype: Machine Translation
ms.sourcegitcommit: 6fe065a9cefe7a01942aa3f5411167f8a5f38985
ms.openlocfilehash: a33bc40cd39494a304652ff8b20d40a6f3fdd099
ms.contentlocale: ko-kr
ms.lasthandoff: 02/24/2017

---
# <a name="compiler-error-c2094"></a>컴파일러 오류 C2094
'identifier' 레이블이 정의되지 않았습니다.  
  
사용 하는 레이블이 [goto](../../cpp/goto-statement-cpp.md) 문 함수에 존재 하지 않습니다.  
  
## <a name="example"></a>예제  
다음 샘플에서는 C2094를 생성합니다.  
  
```cpp  
// C2094.c  
int main() {  
   goto test;  
}   // C2094  
```  
  
 해결 방법:  
  
```cpp  
// C2094b.c  
int main() {  
   goto test;  
   test:   
   {  
   }  
}  
```
