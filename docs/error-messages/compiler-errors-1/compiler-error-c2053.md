---
title: "컴파일러 오류 C2053 | Microsoft Docs"
ms.custom: ""
ms.date: "12/03/2016"
ms.prod: "visual-studio-dev14"
ms.reviewer: ""
ms.suite: ""
ms.technology: 
  - "devlang-cpp"
ms.tgt_pltfrm: ""
ms.topic: "error-reference"
f1_keywords: 
  - "C2053"
dev_langs: 
  - "C++"
helpviewer_keywords: 
  - "C2053"
ms.assetid: 13324c85-13a8-4996-bd42-a31bfe7ff80f
caps.latest.revision: 7
caps.handback.revision: 7
author: "corob-msft"
ms.author: "corob"
manager: "ghogen"
---
# 컴파일러 오류 C2053
[!INCLUDE[vs2017banner](../../assembler/inline/includes/vs2017banner.md)]

'identifier' : 와이드 문자열이 일치하지 않습니다.  
  
 와이드 문자열이 호환되지 않는 형식에 할당되었습니다.  
  
 다음 샘플에서는 C2053 오류가 발생하는 경우를 보여 줍니다.  
  
```  
// C2053.c  
int main() {  
   char array[] = L"Rika";   // C2053  
}  
```