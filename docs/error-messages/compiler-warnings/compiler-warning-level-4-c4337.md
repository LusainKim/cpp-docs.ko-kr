---
title: "컴파일러 경고 (수준 4) C4337 | Microsoft Docs"
ms.custom: 
ms.date: 11/04/2016
ms.reviewer: 
ms.suite: 
ms.technology: cpp-tools
ms.tgt_pltfrm: 
ms.topic: error-reference
f1_keywords: C4337
dev_langs: C++
helpviewer_keywords: C4337
ms.assetid: 70bc72d9-aac5-45cd-abd3-ebe42a05897b
caps.latest.revision: "7"
author: corob-msft
ms.author: corob
manager: ghogen
ms.workload: cplusplus
ms.openlocfilehash: b620d43e595ca959622cd8fca1396a96718e80df
ms.sourcegitcommit: 8fa8fdf0fbb4f57950f1e8f4f9b81b4d39ec7d7a
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 12/21/2017
---
# <a name="compiler-warning-level-4-c4337"></a>컴파일러 경고(수준 4) C4337
'typelib2'에서 'typelib1' 상호 참조 형식 라이브러리는 자동으로 가져옵니다.  
  
 Auto_search 특성의 [#import 지시문](../../preprocessor/hash-import-directive-cpp.md) 암시적으로 가져올 형식 라이브러리를 발생 합니다.  
  
 다음 두 파일 (midl.exe를 사용 하 여 컴파일된)에서 만든 디스크에 지정 된 두 개의 형식 라이브러리:  
  
```  
// C4337a.idl  
[  
  uuid(F87070BA-C6D9-405C-A8E4-8CD9CA25C12B)  
]  
library C4337aLib  
{  
   [uuid(F87070BA-C6D9-405C-A8E4-8CD9CA25C12C)]  
   enum E_C4337a  
   {  
      one = 0,  
      two = 1,  
      three = 2  
    };  
};  
```  
  
 및 다음의 두 번째.idl 파일  
  
```  
// C4337b.idl  
[  
   uuid(F87070BA-C6D9-405C-A8E4-8CD9CA25C12D)  
]  
  
library C4337bLib  
{  
   importlib("c4337a.tlb");  
  
   [uuid(F87070BA-C6D9-405C-A8E4-8CD9CA25C12E)]  
   struct S_C4337b  
   {  
      enum E_C4337a e;  
   };  
};  
```  
  
 다음 샘플에서는 C4337 오류가 생성 됩니다.  
  
```  
// C4337.cpp  
// compile with: /W4 /LD  
#import "c4337b.tlb" auto_search   // C4337  
// explicitly #import all type libraries to resolve  
// #import "C4337a.tlb"  
// #import "C4337b.tlb"  
```