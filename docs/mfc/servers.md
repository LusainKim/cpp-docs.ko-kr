---
title: "서버 | Microsoft Docs"
ms.custom: ""
ms.date: "11/04/2016"
ms.reviewer: ""
ms.suite: ""
ms.technology: 
  - "devlang-cpp"
ms.tgt_pltfrm: ""
ms.topic: "article"
dev_langs: 
  - "C++"
helpviewer_keywords: 
  - "풀 서버"
  - "미니 서버"
  - "OLE 서버 응용 프로그램"
  - "OLE 서버 응용 프로그램, 활성화"
  - "OLE 서버 응용 프로그램, 서버 유형"
  - "서버 응용 프로그램"
  - "서버"
ms.assetid: e45172e8-eae3-400a-8139-0fa009a42fdc
caps.latest.revision: 9
author: "mikeblome"
ms.author: "mblome"
manager: "ghogen"
caps.handback.revision: 5
---
# 서버
[!INCLUDE[vs2017banner](../assembler/inline/includes/vs2017banner.md)]

A server application \(or component application\) creates OLE items \(or components\) for use by container applications.  A visual editing server application also supports visual editing or in\-place activation.  Another form of OLE server is an [automation server](../mfc/automation-servers.md).  Some server applications support only the creation of embedded items; others support the creation of both embedded and linked items.  Some support linking only, although this is rare.  All server applications must support activation by container applications when the user wants to edit an item.  An application can be both a container and a server.  In other words, it can both incorporate data into its documents, and create data that can be incorporated as items into other applications' documents.  
  
 A miniserver is a special type of server application that can only be launched by a container.  Microsoft Draw and Microsoft Graph are examples of miniservers.  A miniserver does not store documents as files on disk.  Instead, it reads its documents from and writes them to items in documents belonging to containers.  As a result, a miniserver supports embedding only, not linking.  
  
 A full server can be run either as a stand\-alone application or launched by a container application.  A full server can store documents as files on disk.  It can support embedding only, both embedding and linking, or linking only.  The user of a container application can create an embedded item by choosing the Cut or Copy command in the server and the Paste command in the container.  A linked item is created by choosing the Copy command in the server and the Paste Link command in the container.  Alternatively, the user can create an embedded or linked item using the Insert Object dialog box.  
  
 The following table summarizes characteristics of different types of servers:  
  
### Server Characteristics  
  
|Type of server|Supports multiple instances|Items per document|Documents per instance|  
|--------------------|---------------------------------|------------------------|----------------------------|  
|Miniserver|예|1|1|  
|SDI full server|예|1 \(if linking is supported, 1 or more\)|1|  
|MDI full server|No \(not required\)|1 \(if linking is supported, 1 or more\)|0 or more|  
  
 A server application should support multiple containers simultaneously, in the event that more than one container will be used to edit an embedded or linked item.  If the server is an SDI application \(or a miniserver with a dialog box interface\), multiple instances of the server must be able to run simultaneously.  This allows a separate instance of the application to handle each container request.  
  
 If the server is an MDI application, it can create a new MDI child window each time a container needs to edit an item.  In this way, a single instance of the application can support multiple containers.  
  
 Your server application must tell the OLE system DLLs what to do if one instance of the server is already running when another container requests its services: whether it should launch a new instance of the server or direct all containers' requests to one instance of the server.  
  
 For more details on servers, see:  
  
-   [서버: 서버 구현](../mfc/servers-implementing-a-server.md)  
  
-   [Servers: Implementing Server Documents](../mfc/servers-implementing-server-documents.md)  
  
-   [Servers: Implementing In\-Place Frame Windows](../mfc/servers-implementing-in-place-frame-windows.md)  
  
-   [Servers: Server Items](../mfc/servers-server-items.md)  
  
-   [Servers: User\-Interface Issues](../mfc/servers-user-interface-issues.md)  
  
## 참고 항목  
 [OLE](../mfc/ole-in-mfc.md)   
 [컨테이너](../mfc/containers.md)   
 [컨테이너: 고급 기능](../mfc/containers-advanced-features.md)   
 [메뉴 및 리소스\(OLE\)](../mfc/menus-and-resources-ole.md)   
 [등록](../mfc/registration.md)   
 [자동화 서버](../mfc/automation-servers.md)