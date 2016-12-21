---
title: "SafeInt 함수 | Microsoft Docs"
ms.custom: ""
ms.date: "12/03/2016"
ms.prod: "visual-studio-dev14"
ms.reviewer: ""
ms.suite: ""
ms.technology: 
  - "devlang-cpp"
ms.tgt_pltfrm: ""
ms.topic: "language-reference"
dev_langs: 
  - "C++"
helpviewer_keywords: 
  - "함수, SafeInt"
ms.assetid: fdc208e5-5d8a-41a9-8271-567fd438958d
caps.latest.revision: 13
caps.handback.revision: 13
author: "ghogen"
ms.author: "ghogen"
manager: "ghogen"
---
# SafeInt 함수
[!INCLUDE[vs2017banner](../assembler/inline/includes/vs2017banner.md)]

The SafeInt library provides several functions that you can use without creating an instance of the [SafeInt 클래스](../windows/safeint-class.md).  If you want to protect a single mathematical operation from integer overflow, you can use these functions.  If you want to protect multiple mathematical operations, you should create `SafeInt` objects.  It is more efficient to create `SafeInt` objects than to use these functions multiple times.  
  
 These functions enable you to compare or perform mathematical operations on two different types of parameters without having to convert them to the same type first.  
  
 Each of these functions has two template types: `T` and `U`.  Each of these types can be a Boolean, character, or integral type.  Integral types can be signed or unsigned and any size from 8 bits to 64 bits.  
  
## 단원 내용  
  
|Function|설명|  
|--------------|--------|  
|[SafeAdd](../windows/safeadd.md)|Adds two numbers and protects against overflow.|  
|[SafeCast](../windows/safecast.md)|Casts one type of parameter to another type.|  
|[SafeDivide](../windows/safedivide.md)|Divides two numbers and protects against dividing by zero.|  
|[SafeEquals](../windows/safeequals.md), [SafeGreaterThan](../windows/safegreaterthan.md), [SafeGreaterThanEquals](../windows/safegreaterthanequals.md), [SafeLessThan](../windows/safelessthan.md), [SafeLessThanEquals](../windows/safelessthanequals.md), [SafeNotEquals](../windows/safenotequals.md)|Compares two numbers.  These functions enable you to compare two different types of numbers without changing their types.|  
|[SafeModulus](../windows/safemodulus.md)|Performs the modulus operation on two numbers.|  
|[SafeMultiply](../windows/safemultiply.md)|Multiplies two numbers together and protects against overflow.|  
|[SafeSubtract](../windows/safesubtract.md)|Subtracts two numbers and protects against overflow.|  
  
## 관련 단원  
  
|단원|설명|  
|--------|--------|  
|[SafeInt 클래스](../windows/safeint-class.md)|`SafeInt` 클래스입니다.|  
|[SafeIntException 클래스](../windows/safeintexception-class.md)|The exception class specific to the SafeInt library.|