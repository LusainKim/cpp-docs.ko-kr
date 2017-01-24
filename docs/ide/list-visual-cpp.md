---
title: "&lt;list&gt;(Visual C++) | Microsoft Docs"
ms.custom: ""
ms.date: "12/03/2016"
ms.prod: "visual-studio-dev14"
ms.reviewer: ""
ms.suite: ""
ms.technology: 
  - "devlang-cpp"
ms.tgt_pltfrm: ""
ms.topic: "article"
f1_keywords: 
  - "list"
  - "<list>"
dev_langs: 
  - "C++"
helpviewer_keywords: 
  - "<list> C++ XML 태그"
  - "list C++ XML 태그"
ms.assetid: c792a10b-0451-422c-9aa0-604116e69d64
caps.latest.revision: 8
caps.handback.revision: 8
author: "mikeblome"
ms.author: "mblome"
manager: "ghogen"
---
# &lt;list&gt;(Visual C++)
[!INCLUDE[vs2017banner](../assembler/inline/includes/vs2017banner.md)]

\<listheader\> 블록은 테이블이나 정의 목록의 머리글 행을 정의하는 데 사용됩니다.  테이블을 정의할 때는 머리글의 term에 대한 엔트리만 제공하면 됩니다.  
  
## 구문  
  
```  
<list type="bullet" | "number" | "table">  
   <listheader>  
      <term>term</term>  
      <description>description</description>  
   </listheader>  
   <item>  
      <term>term</term>  
      <description>description</description>  
   </item>  
</list>  
```  
  
#### 매개 변수  
 `term`  
 `description`에서 정의할 용어입니다.  
  
 `description`  
 글머리 기호 목록이나 번호 매기기의 항목 또는 `term`의 정의입니다.  
  
## 설명  
 목록의 각 항목은 \<item\> 블록으로 지정합니다.  정의 목록을 만들 때는 `term`과 `description`을 모두 지정해야 합니다.  그러나 테이블, 글머리 기호 목록 또는 번호 매기기 목록의 경우에는 `description`에 대한 입력만 제공하면 됩니다.  
  
 목록이나 테이블에 사용할 수 있는 \<item\> 블록의 수에는 제한이 없습니다.  
  
 [\/doc](../build/reference/doc-process-documentation-comments-c-cpp.md)로 컴파일하여 문서 주석을 파일로 저장합니다.  
  
## 예제  
  
```  
// xml_list_tag.cpp  
// compile with: /doc /LD  
// post-build command: xdcmake xml_list_tag.dll  
/// <remarks>Here is an example of a bulleted list:  
/// <list type="bullet">  
/// <item>  
/// <description>Item 1.</description>  
/// </item>  
/// <item>  
/// <description>Item 2.</description>  
/// </item>  
/// </list>  
/// </remarks>  
class MyClass {};  
```  
  
## 참고 항목  
 [XML 문서](../ide/xml-documentation-visual-cpp.md)