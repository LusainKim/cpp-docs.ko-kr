---
title: "방법: const 키워드와 함께 내부 포인터 선언 (C + + /cli CLI) | Microsoft Docs"
ms.custom: 
ms.date: 11/04/2016
ms.reviewer: 
ms.suite: 
ms.technology: cpp-windows
ms.tgt_pltfrm: 
ms.topic: language-reference
dev_langs: C++
helpviewer_keywords: pointers, interior
ms.assetid: 64e08b0e-9396-4046-ab51-8f6588f32330
caps.latest.revision: "13"
author: mikeblome
ms.author: mblome
manager: ghogen
ms.workload:
- cplusplus
- uwp
ms.openlocfilehash: aadd1573a5110960ba74eabe4fc6c696fad887ca
ms.sourcegitcommit: 8fa8fdf0fbb4f57950f1e8f4f9b81b4d39ec7d7a
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 12/21/2017
---
# <a name="how-to-declare-interior-pointers-with-the-const-keyword-ccli"></a>방법: const 키워드(C++/CLI)를 사용하여 내부 포인터 선언
다음 샘플에서는 사용 하는 방법을 보여 줍니다. `const` 내부 포인터의 선언에 있습니다.  
  
> [!IMPORTANT]
>  이 언어 기능으로 사용할 수는 **/clr** 컴파일러 옵션을 하지만 하지는 **/ZW** 컴파일러 옵션입니다.  
  
## <a name="example"></a>예  
  
```  
// interior_ptr_const.cpp  
// compile with: /clr  
using namespace System;  
value struct V {   
   int i;  
};  
  
ref struct G {  
   V v;  
   String ^ msg;  
};  
  
interior_ptr<int> f( interior_ptr<V> pv ) {   
   return &(pv->i);   
}  
  
int main() {  
   int n = -1;  
   int o = -1;  
   interior_ptr<int> pn1 = &n;  
   *pn1 = 50;  
  
   V v;  
   v.i = 101;  
   V * npV = &v;   // ok: &v yields a pointer to the native heap  
  
   interior_ptr<int> pn2 = &n;  
   interior_ptr<V> pV = &(v);  
   pn2 = f(pV);  
   *pn2 = 50;  
  
   G ^pG = gcnew G;  
   pV = &(pG->v);   // ok: pV is an interior pointer  
  
   interior_ptr<int const> pn3 = &n;  
   // *pn3 = 5;   error because pn3 cannot be dereferenced and changed  
   pn3 = &o;   // OK, can change the memory location  
  
   interior_ptr<int> const pn4 = &n;     
   *pn4 = 5;   // OK because you can dereference and change pn4  
   // pn4 = &o;   error cannot change the memory location  
  
   const interior_ptr<const int> pn5 = &n;  
   // *pn5 = 5;   error cannot dereference and change pn5  
   // pn5 = &o;   error cannot change the memory location  
  
   const G ^ h_G = gcnew G;   // object is const, cannot modify any members of h_G or call any non-const methods  
   // h_G->msg = "test";   error h_G is const  
   interior_ptr<String^ const> int_ptr_G = &(h_G->msg);  
  
   G ^ const h_G2 = gcnew G;   // interior pointers to this obejct cannot be dereferenced and changed  
   h_G2->msg = "test";  
   interior_ptr<String^ const> int_ptr_G2 = &(h_G->msg);  
};  
```  
  
## <a name="see-also"></a>참고 항목  
 [interior_ptr(C++/CLI)](../windows/interior-ptr-cpp-cli.md)