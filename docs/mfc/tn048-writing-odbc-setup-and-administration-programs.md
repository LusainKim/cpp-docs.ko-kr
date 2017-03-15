---
title: "TN048: MFC 데이터베이스 응용 프로그램에 대한 ODBC 설정 및 관리 프로그램 작성 | Microsoft Docs"
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
  - "vc.mfc.odbc"
dev_langs: 
  - "C++"
helpviewer_keywords: 
  - "ODBC 설치"
  - "MFC, 데이터베이스 응용 프로그램"
  - "ODBC, 및 MFC"
  - "ODBC, 설치"
  - "설치, ODBC 설치 프로그램"
  - "TN048"
ms.assetid: d456cdd4-0513-4a51-80c0-9132b66115ce
caps.latest.revision: 9
caps.handback.revision: 5
author: "mikeblome"
ms.author: "mblome"
manager: "ghogen"
---
# TN048: MFC 데이터베이스 응용 프로그램에 대한 ODBC 설정 및 관리 프로그램 작성
[!INCLUDE[vs2017banner](../assembler/inline/includes/vs2017banner.md)]

> [!NOTE]
>  다음 기술 노트는 온라인 설명서에 먼저 포함되어 있었으므로 업데이트되지 않았습니다.  따라서 일부 절차 및 항목은 만료되거나 올바르지 않을 수 있습니다.  최신 정보를 보려면 온라인 설명서 색인에서 관심 있는 항목을 검색하는 것이 좋습니다.  
  
 Applications using MFC database classes will need a setup program that installs ODBC components.  They may also need an ODBC Administration program that will retrieve information about the available drivers, to specify default drivers and to configure data sources.  This note describes the use of the ODBC Installer API to write these programs.  
  
##  <a name="_mfcnotes_writing_an_odbc_setup_program"></a> Writing an ODBC Setup Program  
 An MFC database application requires the ODBC Driver Manager \(ODBC.DLL\) and ODBC drivers to be able to get to data sources.  Many ODBC drivers also require additional network and communication DLLs.  Most ODBC drivers ship with a setup program that will install the required ODBC components.  Application developers using MFC database classes can:  
  
-   Rely on the driver\-specific setup programs for installing ODBC components.  This will require no further work on the developer's part — you can just redistribute the driver's setup program.  
  
-   Alternatively, you can write your own setup program, which will install the driver manager and the driver.  
  
 The ODBC installer API can be used to write application\-specific setup programs.  The functions in the installer API are implemented by the ODBC installer DLL — ODBCINST.DLL on 16\-bit Windows and ODBCCP32.DLL on Win32.  An application can call **SQLInstallODBC** in the installer DLL, which will install the ODBC driver manager, ODBC drivers, and any required translators.  It then records the installed drivers and translators in the ODBCINST.INI file \(or the registry, on NT\).  **SQLInstallODBC** requires the full path to the ODBC.INF file, which contains the list of drivers to be installed and describes the files that comprise each driver.  It also contains similar information about the driver manager and translators.  ODBC.INF files are typically supplied by driver developers.  
  
 A program can also install individual ODBC components.  To install the Driver Manager, a program first calls **SQLInstallDriverManager** in the installer DLL to get the target directory for the Driver Manager.  This is usually the directory in which Windows DLLs reside.  The program then uses the information in the \[ODBC Driver Manager\] section of the ODBC.INF file to copy the Driver Manager and related files from the installation disk to this directory.  To install an individual driver, a program first calls **SQLInstallDriver** in the installer DLL to add the driver specification to the ODBCINST.INI file \(or the registry, on NT\).  **SQLInstallDriver** returns the driver's target directory — usually the directory in which Windows DLLs reside.  The program then uses the information in the driver's section of the ODBC.INF file to copy the driver DLL and related files from the installation disk to this directory.  
  
 For more information on ODBC.INF, ODBCINST.INI and using the installer API, see ODBC SDK *Programmer's Reference,* Chapter 19, Installing ODBC Software.  
  
##  <a name="_mfcnotes_writing_an_odbc_administrator"></a> Writing an ODBC Administrator  
 An MFC database application can set up and configure ODBC data sources in one of two ways, as follows:  
  
-   Use the ODBC Administrator \(available as a program or as a Control Panel item\).  
  
-   Create your own program to configure data sources.  
  
 A program that configures data sources makes function calls to the installer DLL.  The installer DLL calls a setup DLL to configure a data source.  There is one setup DLL for each driver; it may be the driver DLL itself, or a separate DLL.  The setup DLL prompts the user for information that the driver needs to connect to the data source and the default translator, if supported.  It then calls the installer DLL and Windows APIs to record this information in the ODBC.INI file \(or registry\).  
  
 To display a dialog box with which a user can add, modify, and delete data sources, a program calls **SQLManageDataSources** in the installer DLL.  This function is invoked when the installer DLL is called from the Control Panel.  To add, modify, or delete a data source, **SQLManageDataSources** calls **ConfigDSN** in the setup DLL for the driver associated with that data source.  To directly add, modify, or delete data sources, a program calls **SQLConfigDataSource** in the installer DLL.  The program passes the name of the data source and an option that specifies the action to take.  **SQLConfigDataSource** calls **ConfigDSN** in the setup DLL and passes it the arguments from **SQLConfigDataSource**.  
  
 For more information, see ODBC SDK *Programmer's Reference,* Chapter 23, Setup DLL Function Reference, and Chapter 24, Installer DLL Function Reference.  
  
## 참고 항목  
 [번호별 기술 참고 사항](../mfc/technical-notes-by-number.md)   
 [범주별 기술 참고 사항](../mfc/technical-notes-by-category.md)