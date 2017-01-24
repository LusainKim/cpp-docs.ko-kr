---
title: "추출 연산자 사용 | Microsoft Docs"
ms.custom: ""
ms.date: "12/03/2016"
ms.prod: "visual-studio-dev14"
ms.reviewer: ""
ms.suite: ""
ms.technology: 
  - "devlang-cpp"
ms.tgt_pltfrm: ""
ms.topic: "article"
dev_langs: 
  - "C++"
helpviewer_keywords: 
  - ">> 연산자, 추출 연산자"
  - "추출 연산자"
  - "연산자[C++], 추출"
ms.assetid: a961e1a9-4897-41de-b210-89d5b2d051ae
caps.latest.revision: 8
caps.handback.revision: 7
author: "corob-msft"
ms.author: "corob"
manager: "ghogen"
---
# 추출 연산자 사용
[!INCLUDE[vs2017banner](../assembler/inline/includes/vs2017banner.md)]

The extraction operator \(`>>`\), which is preprogrammed for all standard C\+\+ data types, is the easiest way to get bytes from an input stream object.  
  
 Formatted text input extraction operators depend on white space to separate incoming data values.  This is inconvenient when a text field contains multiple words or when commas separate numbers.  In such a case, one alternative is to use the unformatted input member function [istream::getline](../Topic/basic_istream::getline.md) to read a block of text with white space included, then parse the block with special functions.  Another method is to derive an input stream class with a member function such as `GetNextToken`, which can call istream members to extract and format character data.  
  
## 참고 항목  
 [Input Streams](../standard-library/input-streams.md)