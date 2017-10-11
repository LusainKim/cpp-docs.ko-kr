---
title: "컴파일러 오류 C2599 | Microsoft Docs"
ms.custom: 
ms.date: 11/04/2016
ms.reviewer: 
ms.suite: 
ms.technology:
- cpp-tools
ms.tgt_pltfrm: 
ms.topic: error-reference
f1_keywords:
- C2599
dev_langs:
- C++
helpviewer_keywords:
- C2599
ms.assetid: 88515f36-7589-47e2-862e-0de8b18d6668
caps.latest.revision: 17
author: corob-msft
ms.author: corob
manager: ghogen
ms.translationtype: MT
ms.sourcegitcommit: 35b46e23aeb5f4dbfd2a0dd44b906389dd5bfc88
ms.openlocfilehash: e71bf7f08591ed80489b6e83590696cabdb57c03
ms.contentlocale: ko-kr
ms.lasthandoff: 10/10/2017

---
# <a name="compiler-error-c2599"></a>컴파일러 오류 C2599
'enum': 열거형 형식의 정방향 선언은 허용 되지 않습니다  
  
 컴파일러는 더 이상 관리 되는 열거형의 정방향 선언을 지원합니다.  
  
 열거형 형식의 정방향 선언은 허용 되지 않습니다 [/Za](../../build/reference/za-ze-disable-language-extensions.md)합니다.  
  
 다음 샘플에서는 c 2599를 생성합니다.  
  
```  
// C2599.cpp  
// compile with: /clr /c  
enum class Status;   // C2599  
  
enum class Status2 { stop2, hold2, go2};   
  
ref struct MyStruct {  
   // Delete the following line to resolve.  
   Status m_status;  
  
   Status2 m_status2;   // OK  
};  
  
enum class Status { stop, hold, go };  
```
