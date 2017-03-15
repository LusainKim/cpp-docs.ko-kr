---
title: "CDataConnection 클래스 | Microsoft Docs"
ms.custom: ""
ms.date: "11/04/2016"
ms.reviewer: ""
ms.suite: ""
ms.technology: 
  - "devlang-cpp"
ms.tgt_pltfrm: ""
ms.topic: "article"
f1_keywords: 
  - "ATL::CDataConnection"
  - "ATL.CDataConnection"
  - "CDataConnection"
dev_langs: 
  - "C++"
helpviewer_keywords: 
  - "CDataConnection 클래스"
ms.assetid: 77432d85-4e20-49ec-a0b0-142137828471
caps.latest.revision: 13
author: "mikeblome"
ms.author: "mblome"
manager: "ghogen"
caps.handback.revision: 13
---
# CDataConnection 클래스
[!INCLUDE[vs2017banner](../../assembler/inline/includes/vs2017banner.md)]

Manages the connection with the data source.  
  
## 구문  
  
```  
class CDataConnection  
```  
  
## 멤버  
  
### 메서드  
  
|||  
|-|-|  
|[CDataConnection](../../data/oledb/cdataconnection-cdataconnection.md)|생성자입니다.  Instantiates and initializes a `CDataConnection` object.|  
|[복사](../../data/oledb/cdataconnection-copy.md)|Creates a copy of an existing data connection.|  
|[를 엽니다.](../../data/oledb/cdataconnection-open.md)|Opens a connection to a data source using an initialization string.|  
|[OpenNewSession](../../data/oledb/cdataconnection-opennewsession.md)|Opens a new session on the current connection.|  
  
### 연산자  
  
|||  
|-|-|  
|[operator BOOL](../../data/oledb/cdataconnection-operator-bool.md)|Determines whether the current session is open or not.|  
|[operator bool](../../data/oledb/cdataconnection-operator-bool-ole-db.md)|Determines whether the current session is open or not.|  
|[operator CDataSource&](../../data/oledb/cdataconnection-operator-cdatasource-amp.md)|Returns a reference to the contained `CDataSource` object.|  
|[operator CDataSource\*](../../data/oledb/cdataconnection-operator-cdatasource-star.md)|Returns a pointer to the contained `CDataSource` object.|  
|[operator CSession&](../../data/oledb/cdataconnection-operator-csession-amp.md)|Returns a reference to the contained `CSession` object.|  
|[operator CSession\*](../../data/oledb/cdataconnection-operator-csession-star.md)|Returns a pointer to the contained `CSession` object.|  
  
## 설명  
 `CDataConnection` is a useful class for creating clients because it encapsulates necessary objects \(data source and session\) and some of the work you need to do when connecting to a data source  
  
 Without `CDataConnection`, you have to create a `CDataSource` object, call its [OpenFromInitializationString](../../data/oledb/cdatasource-openfrominitializationstring.md) method, then create an instance of a [CSession](../../data/oledb/csession-class.md) object, call its [Open](../../data/oledb/csession-open.md) method, then create a [CCommand](../../data/oledb/ccommand-class.md) object and call its **Open**\* methods.  
  
 With `CDataConnection`, you only need to create a connection object, pass it an initialization string, then use that connection to open commands.  If you plan on using your connection to the database repeatedly, it is a good idea to keep the connection open, and `CDataConnection` provides a convenient way to do that.  
  
> [!NOTE]
>  If you are creating a database application that needs to handle multiple sessions, you will need to use [OpenNewSession](../../data/oledb/cdataconnection-opennewsession.md).  
  
## 요구 사항  
 **헤더:** atldbcli.h  
  
## 참고 항목  
 [OLE DB 소비자 템플릿](../../data/oledb/ole-db-consumer-templates-cpp.md)   
 [OLE DB 소비자 템플릿 참조](../../data/oledb/ole-db-consumer-templates-reference.md)