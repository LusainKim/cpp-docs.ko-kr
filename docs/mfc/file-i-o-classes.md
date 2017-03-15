---
title: "파일 I/O 클래스 | Microsoft Docs"
ms.custom: ""
ms.date: "11/04/2016"
ms.reviewer: ""
ms.suite: ""
ms.technology: 
  - "devlang-cpp"
ms.tgt_pltfrm: ""
ms.topic: "article"
f1_keywords: 
  - "vc.classes.file"
dev_langs: 
  - "C++"
helpviewer_keywords: 
  - "디스크 파일 클래스"
  - "파일 I/O 클래스[C++]"
  - "I/O[C++], MFC 클래스"
  - "I/O[MFC], 클래스"
  - "메모리 파일 클래스"
  - "OLE 스트림"
  - "소켓 클래스"
  - "stdio 클래스"
  - "스트림 클래스"
  - "변환된 스트림 클래스"
ms.assetid: 92821c3f-d9e1-47f6-98c9-3b632d86e811
caps.latest.revision: 10
author: "mikeblome"
ms.author: "mblome"
manager: "ghogen"
caps.handback.revision: 6
---
# 파일 I/O 클래스
[!INCLUDE[vs2017banner](../assembler/inline/includes/vs2017banner.md)]

These classes provide an interface to traditional disk files, in\-memory files, Active streams, and Windows sockets.  All of the classes derived from `CFile` can be used with a `CArchive` object to perform serialization.  
  
 Use the following classes, particularly `CArchive` and `CFile`, if you write your own input\/output processing.  Normally you do not need to derive from these classes.  If you use the application framework, the default implementations of the **Open** and **Save** commands on the **File** menu will handle file I\/O \(using class `CArchive`\), as long as you override your document's `Serialize` function to supply details about how a document serializes its contents.  For more information about the file classes and serialization, see the article [Files in MFC](../mfc/files-in-mfc.md) and the article [Serialization](../mfc/serialization-in-mfc.md).  
  
 [CFile](../mfc/reference/cfile-class.md)  
 Provides a file interface to binary disk files.  
  
 [CStdioFile](../mfc/reference/cstdiofile-class.md)  
 Provides a `CFile` interface to buffered stream disk files, usually in text mode.  
  
 [CMemFile](../mfc/reference/cmemfile-class.md)  
 Provides a `CFile` interface to in\-memory files.  
  
 [CSharedFile](../mfc/reference/csharedfile-class.md)  
 Provides a `CFile` interface to shared in\-memory files.  
  
 [COleStreamFile](../mfc/reference/colestreamfile-class.md)  
 Uses the COM `IStream` interface to provide `CFile` access to compound files.  
  
 [CSocketFile](../mfc/reference/csocketfile-class.md)  
 Provides a `CFile` interface to a Windows Socket.  
  
## Related Classes  
 [CArchive](../mfc/reference/carchive-class.md)  
 Cooperates with a `CFile` object to implement persistent storage for objects through serialization \(see [CObject::Serialize](../Topic/CObject::Serialize.md)\).  
  
 [CArchiveException](../mfc/reference/carchiveexception-class.md)  
 An archive exception.  
  
 [CFileException](../mfc/reference/cfileexception-class.md)  
 A file\-oriented exception.  
  
 [CFileDialog](../mfc/reference/cfiledialog-class.md)  
 Provides a standard dialog box for opening or saving a file.  
  
 [CRecentFileList](../mfc/reference/crecentfilelist-class.md)  
 Maintains the most recently used \(MRU\) file list.  
  
## 참고 항목  
 [클래스 개요](../mfc/class-library-overview.md)