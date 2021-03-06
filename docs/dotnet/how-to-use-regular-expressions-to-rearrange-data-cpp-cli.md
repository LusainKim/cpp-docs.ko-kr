---
title: "방법: 정규식을 사용 하 여 데이터를 다시 정렬 하려면 (C + + /cli CLI) | Microsoft Docs"
ms.custom: 
ms.date: 11/04/2016
ms.reviewer: 
ms.suite: 
ms.technology: cpp-windows
ms.tgt_pltfrm: 
ms.topic: article
dev_langs: C++
helpviewer_keywords:
- regular expressions [C++], rearranging data
- data [C++], rearranging
ms.assetid: 5f91e777-9471-424e-ba75-dca3d1b49e42
caps.latest.revision: "9"
author: mikeblome
ms.author: mblome
manager: ghogen
ms.workload:
- cplusplus
- dotnet
ms.openlocfilehash: bf60fff6c15313a6f7df1104f67c1f043f885eac
ms.sourcegitcommit: 8fa8fdf0fbb4f57950f1e8f4f9b81b4d39ec7d7a
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 12/21/2017
---
# <a name="how-to-use-regular-expressions-to-rearrange-data-ccli"></a>방법: 정규식을 사용하여 데이터 다시 정렬(C++/CLI)
다음 코드 예제를 다시 정렬 하거나 데이터를 다시.NET Framework 정규식 지원을 사용할 수 있는 방법을 보여 줍니다. 다음 코드 예제에서는 <xref:System.Text.RegularExpressions.Regex> 및 <xref:System.Text.RegularExpressions.Match> 문자열에서 성과 이름을 추출 하 고 다음 이러한 이름 요소를 반대 순서로 표시 하는 클래스입니다.  
  
 <xref:System.Text.RegularExpressions.Regex> 클래스는 현재 데이터 형식을 설명 하는 정규식을 생성 하는 데 사용 합니다. 두 이름이 쉼표로 구분 하는 양의 쉼표 앞뒤에 공백을 사용할 수 있습니다. <xref:System.Text.RegularExpressions.Match> 메서드는 다음 각 문자열을 분석 하는 데 사용 됩니다. ְ ּ ¸에서 검색 됩니다 성공적으로 실행 되는 <xref:System.Text.RegularExpressions.Match> 개체를 표시 합니다.  
  
## <a name="example"></a>예  
  
```  
// regex_reorder.cpp  
// compile with: /clr  
#using <System.dll>  
using namespace System;  
using namespace Text::RegularExpressions;  
  
int main()  
{  
   array<String^>^ name =   
   {  
      "Abolrous, Sam",   
      "Berg,Matt",   
      "Berry , Jo",  
      "www.contoso.com"  
   };  
  
   Regex^ reg = gcnew Regex("(?<last>\\w*)\\s*,\\s*(?<first>\\w*)");  
  
   for ( int i=0; i < name->Length; i++ )  
   {  
      Console::Write( "{0,-20}", name[i] );  
      Match^ m = reg->Match( name[i] );  
      if ( m->Success )  
      {  
         String^ first = m->Groups["first"]->Value;  
         String^ last = m->Groups["last"]->Value;  
         Console::WriteLine("{0} {1}", first, last);  
      }  
      else  
         Console::WriteLine("(invalid)");  
   }  
   return 0;  
}  
```  
  
## <a name="see-also"></a>참고 항목  
 [.NET Framework 정규식](/dotnet/standard/base-types/regular-expressions)   
 [C++/CLI를 사용한 .NET 프로그래밍(Visual C++)](../dotnet/dotnet-programming-with-cpp-cli-visual-cpp.md)