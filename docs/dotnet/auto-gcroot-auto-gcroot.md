---
title: auto_gcroot::auto_gcroot | Microsoft Docs
ms.custom: 
ms.date: 11/04/2016
ms.reviewer: 
ms.suite: 
ms.technology: cpp-windows
ms.tgt_pltfrm: 
ms.topic: reference
f1_keywords:
- msclr::auto_gcroot::auto_gcroot
- auto_gcroot::auto_gcroot
- auto_gcroot.auto_gcroot
- msclr.auto_gcroot.auto_gcroot
dev_langs: C++
helpviewer_keywords: auto_gcroot::auto_gcroot
ms.assetid: 27faa42a-64ea-4d31-836f-073a55145735
caps.latest.revision: "12"
author: mikeblome
ms.author: mblome
manager: ghogen
ms.workload:
- cplusplus
- dotnet
ms.openlocfilehash: 30503886c3a4af047226af88ee16e1132e9d0896
ms.sourcegitcommit: 8fa8fdf0fbb4f57950f1e8f4f9b81b4d39ec7d7a
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 12/21/2017
---
# <a name="autogcrootautogcroot"></a>auto_gcroot::auto_gcroot
`auto_gcroot` 생성자입니다.  
  
## <a name="syntax"></a>구문  
  
```  
auto_gcroot(  
   _element_type _ptr = nullptr  
);  
auto_gcroot(  
   auto_gcroot<_element_type> & _right  
);  
template<typename _other_type>  
auto_gcroot(  
   auto_gcroot<_other_type> & _right  
);  
```  
  
#### <a name="parameters"></a>매개 변수  
 `_ptr`  
 소유 하는 개체입니다.  
  
 `_right`  
 기존 `auto_gcroot`입니다.  
  
## <a name="remarks"></a>설명  
 생성할 때는 `auto_gcroot` 기존 `auto_gcroot`, 기존 `auto_gcroot` 를 새 개체의 소유권을 전송 하기 전에 해당 개체를 해제 `auto_gcroot`합니다.  
  
## <a name="example"></a>예  
  
```  
// msl_auto_gcroot_auto_gcroot.cpp  
// compile with: /clr  
#include <msclr\auto_gcroot.h>  
  
using namespace System;  
using namespace msclr;  
  
ref class RefClassA {  
protected:  
   String^ m_s;     
public:  
   RefClassA(String^ s) : m_s(s) {  
      Console::WriteLine( "in RefClassA constructor: " + m_s );  
   }  
   ~RefClassA() {  
      Console::WriteLine( "in RefClassA destructor: " + m_s );  
   }  
  
   virtual void PrintHello() {  
      Console::WriteLine( "Hello from {0} A!", m_s );  
   }  
};  
  
ref class RefClassB : RefClassA {  
public:     
   RefClassB( String^ s ) : RefClassA( s ) {}  
   virtual void PrintHello() new {  
      Console::WriteLine( "Hello from {0} B!", m_s );  
   }  
};  
  
class ClassA { //unmanaged class  
private:     
   auto_gcroot<RefClassA^> m_a;  
  
public:  
   ClassA() : m_a( gcnew RefClassA( "unmanaged" ) ) {}  
   ~ClassA() {} //no need to delete m_a  
  
   void DoSomething() {  
      m_a->PrintHello();  
   }  
};  
  
int main()  
{  
   {  
      ClassA a;  
      a.DoSomething();  
   } // a.m_a is automatically destroyed as a goes out of scope  
  
   {  
      auto_gcroot<RefClassA^> a(gcnew RefClassA( "first" ) );  
      a->PrintHello();  
   }  
  
   {  
      auto_gcroot<RefClassB^> b(gcnew RefClassB( "second" ) );  
      b->PrintHello();  
      auto_gcroot<RefClassA^> a(b); //construct from derived type  
      a->PrintHello();  
      auto_gcroot<RefClassA^> a2(a); //construct from same type  
      a2->PrintHello();  
   }  
  
   Console::WriteLine("done");  
}  
```  
  
```Output  
in RefClassA constructor: unmanaged  
Hello from unmanaged A!  
in RefClassA destructor: unmanaged  
in RefClassA constructor: first  
Hello from first A!  
in RefClassA destructor: first  
in RefClassA constructor: second  
Hello from second B!  
Hello from second A!  
Hello from second A!  
in RefClassA destructor: second  
done  
```  
  
## <a name="requirements"></a>요구 사항  
 **헤더 파일** \<msclr\auto_gcroot.h >  
  
 **Namespace** msclr  
  
## <a name="see-also"></a>참고 항목  
 [auto_gcroot 멤버](../dotnet/auto-gcroot-members.md)   
 [auto_gcroot::attach](../dotnet/auto-gcroot-attach.md)   
 [auto_gcroot::operator =](../dotnet/auto-gcroot-operator-assign.md)   
 [auto_gcroot::~auto_gcroot](../dotnet/auto-gcroot-tilde-auto-gcroot.md)