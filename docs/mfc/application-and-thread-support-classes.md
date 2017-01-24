---
title: "응용 프로그램 및 스레드 지원 클래스 | Microsoft Docs"
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
  - "vc.classes.support"
dev_langs: 
  - "C++"
helpviewer_keywords: 
  - "응용 프로그램 개체[C++], 스레드 지원 클래스"
  - "응용 프로그램 지원 클래스[C++]"
  - "잠금 클래스"
  - "동기화 클래스, 다중 스레딩"
  - "스레드 지원 클래스[C++]"
  - "스레딩[MFC]"
ms.assetid: 3c1d14fd-c35c-48f1-86ce-1e0f9a32c36d
caps.latest.revision: 10
caps.handback.revision: 6
author: "mikeblome"
ms.author: "mblome"
manager: "ghogen"
---
# 응용 프로그램 및 스레드 지원 클래스
[!INCLUDE[vs2017banner](../assembler/inline/includes/vs2017banner.md)]

Each application has one and only one application object; this object coordinates other objects in the running program and is derived from `CWinApp`.  
  
 The Microsoft Foundation Class \(MFC\) Library supports multiple threads of execution within an application.  All applications must have at least one thread; the thread used by your `CWinApp` object is this primary thread.  
  
 `CWinThread` encapsulates a portion of the operating system's threading capabilities.  To make using multiple threads easier, MFC also provides synchronization object classes to provide a C\+\+ interface to Win32 synchronization objects.  
  
## Application and Thread Classes  
 [CWinApp](../mfc/reference/cwinapp-class.md)  
 Encapsulates the code to initialize, run, and terminate the application.  You will derive your application object from this class.  
  
 [CWinThread](../mfc/reference/cwinthread-class.md)  
 The base class for all threads.  Use directly, or derive a class from `CWinThread` if your thread performs user\-interface functions.  `CWinApp`는 `CWinThread`에서 파생됩니다.  
  
## Synchronization Object Classes  
 [CSyncObject](../mfc/reference/csyncobject-class.md)  
 Base class of the synchronization object classes.  
  
 [CCriticalSection](../mfc/reference/ccriticalsection-class.md)  
 A synchronization class that allows only one thread within a single process to access an object.  
  
 [CSemaphore](../mfc/reference/csemaphore-class.md)  
 A synchronization class that allows between one and a specified maximum number of simultaneous accesses to an object.  
  
 [CMutex](../mfc/reference/cmutex-class.md)  
 A synchronization class that allows only one thread within any number of processes to access an object.  
  
 [CEvent](../mfc/reference/cevent-class.md)  
 A synchronization class that notifies an application when an event has occurred.  
  
 [CSingleLock](../mfc/reference/csinglelock-class.md)  
 Used in member functions of thread\-safe classes to lock on one synchronization object.  
  
 [CMultiLock](../mfc/reference/cmultilock-class.md)  
 Used in member functions of thread\-safe classes to lock on one or more synchronization objects from an array of synchronization objects.  
  
## Related Classes  
 [CCommandLineInfo](../mfc/reference/ccommandlineinfo-class.md)  
 Parses the command line with which your program was started.  
  
 [CWaitCursor](../mfc/reference/cwaitcursor-class.md)  
 Puts a wait cursor on the screen.  Used during lengthy operations.  
  
 [CDockState](../mfc/reference/cdockstate-class.md)  
 Handles persistent storage of docking state data for control bars.  
  
 [CRecentFileList](../mfc/reference/crecentfilelist-class.md)  
 Maintains the most recently used \(MRU\) file list.  
  
## 참고 항목  
 [클래스 개요](../mfc/class-library-overview.md)