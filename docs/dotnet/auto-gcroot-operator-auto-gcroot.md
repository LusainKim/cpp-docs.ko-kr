---
title: "auto_gcroot::operator auto_gcroot | Microsoft Docs"
ms.custom: ""
ms.date: "12/03/2016"
ms.prod: "visual-studio-dev14"
ms.reviewer: ""
ms.suite: ""
ms.technology: 
  - "devlang-cpp"
ms.tgt_pltfrm: ""
ms.topic: "reference"
f1_keywords: 
  - "auto_gcroot.operator auto_gcroot"
  - "auto_gcroot::operator auto_gcroot"
  - "msclr.auto_gcroot.operator auto_gcroot"
  - "msclr::auto_gcroot::operator auto_gcroot"
dev_langs: 
  - "C++"
helpviewer_keywords: 
  - "auto_gcroot 연산자"
ms.assetid: 43e3f27a-9f68-444f-9149-a9282a9b935a
caps.latest.revision: 12
caps.handback.revision: 10
author: "mikeblome"
ms.author: "mblome"
manager: "ghogen"
---
# auto_gcroot::operator auto_gcroot
[!INCLUDE[vs2017banner](../assembler/inline/includes/vs2017banner.md)]

Type\-cast operator between `auto_gcroot` and compatible types.  
  
## 구문  
  
```  
template<typename _other_type>  
operator auto_gcroot<_other_type>();  
```  
  
## 반환 값  
 The current `auto_gcroot` cast to `auto_gcroot<_other_type>`.  
  
## 예제  
  
```  
// msl_auto_gcroot_op_auto_gcroot.cpp  
// compile with: /clr  
#include <msclr\auto_gcroot.h>  
  
using namespace System;  
using namespace msclr;  
  
ref class ClassA {  
protected:     
   String^ m_s;  
public:  
   ClassA( String^ s ) : m_s( s ) {}  
  
   virtual void PrintHello() {  
      Console::WriteLine( "Hello from {0} A!", m_s );  
   }  
};  
  
ref class ClassB : ClassA {  
public:  
   ClassB( String ^ s) : ClassA( s ) {}  
   virtual void PrintHello() new {  
      Console::WriteLine( "Hello from {0} B!", m_s );  
   }  
};  
  
int main() {  
   auto_gcroot<ClassB^> b = gcnew ClassB("first");  
   b->PrintHello();  
   auto_gcroot<ClassA^> a = (auto_gcroot<ClassA^>)b;  
   a->PrintHello();  
}  
```  
  
  **Hello from first B\!**  
**Hello from first A\!**   
## 요구 사항  
 **Header file** \<msclr\\auto\_gcroot.h\>  
  
 **Namespace** msclr  
  
## 참고 항목  
 [auto\_gcroot 멤버](../dotnet/auto-gcroot-members.md)