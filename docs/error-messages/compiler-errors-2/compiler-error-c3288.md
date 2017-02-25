---
title: "컴파일러 오류 C3288 | Microsoft Docs"
ms.custom: ""
ms.date: "11/04/2016"
ms.reviewer: ""
ms.suite: ""
ms.technology: 
  - "devlang-cpp"
ms.tgt_pltfrm: ""
ms.topic: "error-reference"
f1_keywords: 
  - "C3288"
dev_langs: 
  - "C++"
helpviewer_keywords: 
  - "C3288"
ms.assetid: ed08a540-9751-46e1-9cbe-c51d6a49ffab
caps.latest.revision: 5
author: "corob-msft"
ms.author: "corob"
manager: "ghogen"
caps.handback.revision: 5
---
# 컴파일러 오류 C3288
[!INCLUDE[vs2017banner](../../assembler/inline/includes/vs2017banner.md)]

'type' : 핸들 형식에 대한 역참조가 잘못되었습니다.  
  
 컴파일러가 핸들 형식에 대한 잘못된 역참조를 발견했습니다.  핸들 형식을 역참조하고 이를 참조에 할당할 수 있습니다.  자세한 내용은 [Tracking Reference Operator](../../windows/tracking-reference-operator-cpp-component-extensions.md)을 참조하십시오.  
  
## 예제  
 다음 샘플에서는 C3288 오류가 발생하는 경우를 보여 줍니다.  
  
```  
// C3288.cpp  
// compile with: /clr  
ref class R {};  
int main() {  
   *(System::Object^) nullptr;   // C3288  
  
// OK  
   (System::Object^) nullptr;   // OK  
   R^ r;  
   R% pr = *r;  
}  
```