---
title: "컴파일러 오류 C3345 | Microsoft Docs"
ms.custom: 
ms.date: 11/04/2016
ms.reviewer: 
ms.suite: 
ms.technology: cpp-tools
ms.tgt_pltfrm: 
ms.topic: article
f1_keywords: C3345
dev_langs: C++
helpviewer_keywords: C3345
ms.assetid: 1dda4c79-73bb-441b-b939-746154c3afba
caps.latest.revision: "4"
author: corob-msft
ms.author: corob
manager: ghogen
ms.workload: cplusplus
ms.openlocfilehash: ca51e90d8c0cbb1806cc0b042d9c3ae2480a9729
ms.sourcegitcommit: 8fa8fdf0fbb4f57950f1e8f4f9b81b4d39ec7d7a
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 12/21/2017
---
# <a name="compiler-error-c3345"></a>컴파일러 오류 C3345
'identifier': 모듈 이름의 식별자가 잘못되었습니다.  
  
 모듈의 *식별자* 에 하나 이상의 허용되지 않는 문자가 포함되어 있습니다. 첫 번째 문자가 영문자, 밑줄 또는 높은 ANSI(0x80 FF) 문자이고 뒤에 나오는 문자가 영숫자, 밑줄 또는 높은 ANSI 문자이면 식별자가 유효합니다.  
  
### <a name="to-correct-this-error"></a>이 오류를 해결하려면  
  
1.  *식별자* 에 공백이나 기타 허용되지 않는 문자가 없는지 확인합니다.  
  
## <a name="example"></a>예  
 `name` 특성의 `module` 매개 변수에 공백이 있기 때문에 다음 코드 예제에서 오류 메시지 C3345가 발생합니다.  
  
```  
// cpp_attr_name_module.cpp  
// compile with: /LD /link /OPT:NOREF  
#include <atlbase.h>  
#include <atlcom.h>  
#include <atlwin.h>  
#include <atltypes.h>  
#include <atlctl.h>  
#include <atlhost.h>  
#include <atlplus.h>  
  
// C3345 expected  
[module(dll, name="My Library", version="1.2", helpfile="MyHelpFile")]   
// Try the following line instead  
//[module(dll, name="MyLibrary", version="1.2", helpfile="MyHelpFile")]   
// Module attribute now applies to this class  
class CMyClass {  
public:  
BOOL WINAPI DllMain(DWORD dwReason, LPVOID lpReserved) {  
   // add your own code here  
   return __super::DllMain(dwReason, lpReserved);  
   }  
};  
```  
  
## <a name="see-also"></a>참고 항목  
 [__iscsym](../../c-runtime-library/reference/iscsym-functions.md)   
 [문자 분류](../../c-runtime-library/character-classification.md)   
 [모듈](../../windows/module-cpp.md)