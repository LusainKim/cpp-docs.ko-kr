---
title: "Platform:: classnotregisteredexception 클래스 | Microsoft Docs"
ms.custom: 
ms.date: 12/30/2016
ms.technology: cpp-windows
ms.reviewer: 
ms.suite: 
ms.tgt_pltfrm: 
ms.topic: language-reference
f1_keywords:
- VCCORLIB/Platform::ClassNotRegisteredException::ClassNotRegisteredException
- VCCORLIB/Platform::ClassNotRegisteredException
dev_langs: C++
helpviewer_keywords: Platform::ClassNotRegisteredException
ms.assetid: 8f8871d8-51b9-46e8-902e-ae023c9f1de9
caps.latest.revision: "3"
author: ghogen
ms.author: ghogen
manager: ghogen
ms.workload: cplusplus
ms.openlocfilehash: 9f5576a21d5080a248d063673d29d3a2d8bd7f32
ms.sourcegitcommit: 8fa8fdf0fbb4f57950f1e8f4f9b81b4d39ec7d7a
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 12/21/2017
---
# <a name="platformclassnotregisteredexception-class"></a>Platform::ClassNotRegisteredException 클래스
COM 클래스가 등록되지 않은 경우 throw됩니다.  
  
## <a name="syntax"></a>구문  
  
```cpp  
public ref class ClassNotRegisteredException : COMException,    IException,    IPrintable,    IEquatable  
```  
  
### <a name="remarks"></a>설명  
 자세한 내용은 [COMException](../cppcx/platform-comexception-class.md) 클래스를 참조하세요.  
  
### <a name="requirements"></a>요구 사항  
 **지원 되는 최소 클라이언트:** Windows 8  
  
 **지원 되는 최소 서버:** Windows Server 2012  
  
 **네임스페이스:** Platform  
  
 **메타데이터:** platform.winmd  
  
## <a name="see-also"></a>참고 항목  
 [Platform::COMException 클래스](../cppcx/platform-comexception-class.md)