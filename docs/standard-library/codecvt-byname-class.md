---
title: "codecvt_byname 클래스 | Microsoft Docs"
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
  - "std.codecvt_byname"
  - "codecvt_byname"
  - "std::codecvt_byname"
  - "xlocale/std::codecvt_byname"
dev_langs: 
  - "C++"
helpviewer_keywords: 
  - "codecvt_byname 클래스"
ms.assetid: b63b6c04-f60c-47b9-8e30-a933f24a8ffb
caps.latest.revision: 24
caps.handback.revision: 14
author: "corob-msft"
ms.author: "corob"
manager: "ghogen"
---
# codecvt_byname 클래스
[!INCLUDE[vs2017banner](../assembler/inline/includes/vs2017banner.md)]

A derived template class that describes an object that can serve as a collate facet of a given locale, enabling the retrieval of information specific to a cultural area concerning conversions.  
  
## 구문  
  
```  
template<Class CharType, class Byte, class StateType>  
    class codecvt_byname: public codecvt<CharType, Byte, StateType> {  
public:  
    explicit codecvt_byname(  
        const char* _Locname,  
        size_t _Refs = 0  
    );  
```  
  
```  
explicit codecvt_byname(  
    const string& _Locname,  
    size_t _Refs = 0  
);  
```  
  
```  
protected:  
    virtual ~codecvt_byname( );  
};  
```  
  
#### 매개 변수  
 `_Locname`  
 A named locale.  
  
 `_Refs`  
 An initial reference count.  
  
## 설명  
 Byname facets are automatically created when a named locale is constructed.  
  
 Its behavior is determined by the named locale `_Locname`.  Each constructor initializes its base object with [codecvt](../standard-library/codecvt-class.md)\<CharType, Byte, StateType\>\(`_Refs`\).  
  
## 요구 사항  
 **Header:** \<locale\>  
  
 **네임스페이스:** std  
  
## 참고 항목  
 [C\+\+ 표준 라이브러리의 스레드 보안](../standard-library/thread-safety-in-the-cpp-standard-library.md)