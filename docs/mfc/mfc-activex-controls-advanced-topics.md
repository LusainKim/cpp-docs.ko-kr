---
title: "MFC ActiveX 컨트롤: 고급 항목 | Microsoft Docs"
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
  - "FireError 메서드"
  - "MFC ActiveX 컨트롤, 보이지 않는 대화 상자 컨트롤 액세스"
  - "MFC ActiveX 컨트롤, 고급 항목"
  - "MFC ActiveX 컨트롤, 데이터베이스 클래스"
  - "MFC ActiveX 컨트롤, 오류 코드"
  - "MFC ActiveX 컨트롤, 매개 변수가 있는 속성"
  - "MFC ActiveX 컨트롤, 특수 키"
  - "PreTranslateMessage 메서드"
  - "ThrowError 메서드"
ms.assetid: e9e34abb-8e2d-461e-bb9c-a1aec5dcecbd
caps.latest.revision: 13
author: "mikeblome"
ms.author: "mblome"
manager: "ghogen"
caps.handback.revision: 9
---
# MFC ActiveX 컨트롤: 고급 항목
[!INCLUDE[vs2017banner](../assembler/inline/includes/vs2017banner.md)]

This article covers advanced topics related to developing ActiveX controls.  제공합니다.  
  
-   [Using Database Classes in ActiveX Controls](#_core_using_database_classes_in_activex_controls)  
  
-   [Implementing a Parameterized Property](#_core_implementing_a_parameterized_property)  
  
-   [Handling Errors in Your ActiveX Control](#_core_handling_errors_in_your_activex_control)  
  
-   [Handling Special Keys in the Control](#_core_handling_special_keys_in_your_control)  
  
-   [Accessing Dialog Controls That Are Invisible at Run Time](#_core_accessing_dialog_controls_that_are_invisible_at_run_time)  
  
##  <a name="_core_using_database_classes_in_activex_controls"></a> Using Database Classes in ActiveX Controls  
 Because the ActiveX control classes are part of the class library, you can apply the same procedures and rules for using database classes in a standard MFC application to developing ActiveX controls that use the MFC database classes.  
  
 For a general overview of the MFC database classes, see [MFC Database Classes \(DAO and ODBC\)](../data/mfc-database-classes-odbc-and-dao.md).  The article introduces both the MFC ODBC classes and the MFC DAO classes and directs you to more details on either.  
  
> [!NOTE]
>  Visual C\+\+ .NET에서는 포함된 DAO 클래스를 아직 사용할 수 있지만 Visual C\+\+ 환경 및 마법사가 더 이상 DAO를 지원하지 않습니다.  Microsoft recommends that you use [OLE DB Templates](../data/oledb/ole-db-programming.md) or [ODBC and MFC](../data/odbc/odbc-and-mfc.md) for new projects.  DAO는 기존 응용 프로그램을 유지 관리하는 데만 사용할 수 있습니다.  
  
##  <a name="_core_implementing_a_parameterized_property"></a> Implementing a Parameterized Property  
 A parameterized property \(sometimes called a property array\) is a method for exposing a homogeneous collection of values as a single property of the control.  For example, you can use a parameterized property to expose an array or a dictionary as a property.  In Visual Basic, such a property is accessed using array notation:  
  
 [!code-vb[NVC_MFC_AxVb#1](../mfc/codesnippet/VisualBasic/mfc-activex-controls-advanced-topics_1.vb)]  
  
 Use the Add Property Wizard to implement a parameterized property.  The Add Property Wizard implements the property by adding a pair of Get\/Set functions that allow the control user to access the property using the above notation or in the standard fashion.  
  
 Similar to methods and properties, parameterized properties also have a limit to the number of parameters allowed.  In the case of parameterized properties, the limit is 15 parameters \(with one parameter reserved for storing the property value\).  
  
 The following procedure adds a parameterized property, called Array, which can be accessed as a two\-dimensional array of integers.  
  
#### To add a parameterized property using the Add Property Wizard  
  
1.  Load your control's project.  
  
2.  In Class View, expand the library node of your control.  
  
3.  Right\-click the interface node for your control \(the second node of the library node\) to open the shortcut menu.  
  
4.  From the shortcut menu, click **Add** and then click **Add Property**.  
  
5.  In the **Property Name** box, type `Array`.  
  
6.  In the **Property Type** box, select **short**.  
  
7.  For **Implementation** Type, click **Get\/Set Methods**.  
  
8.  In the **Get Function** and **Set Function** boxes, type unique names for your Get and Set Functions or accept the default names.  
  
9. Add a parameter, called `row` \(type `short`\), using the **Parameter Name** and **Parameter Type** controls.  
  
10. Add a second parameter called `column` \(type `short`\).  
  
11. **마침**을 클릭합니다.  
  
### Changes Made by the Add Property Wizard  
 When you add a custom property, the Add Property Wizard makes changes to the control class header \(.H\) and the implementation \(.CPP\) files.  
  
 The following lines are added to the control class .H file:  
  
 [!code-cpp[NVC_MFC_AxUI#35](../mfc/codesnippet/CPP/mfc-activex-controls-advanced-topics_2.h)]  
  
 This code declares two functions called `GetArray` and `SetArray` that allow the user to request a specific row and column when accessing the property.  
  
 In addition, the Add Property Wizard adds the following lines to the control dispatch map, located in the control class implementation \(.CPP\) file:  
  
 [!code-cpp[NVC_MFC_AxUI#36](../mfc/codesnippet/CPP/mfc-activex-controls-advanced-topics_3.cpp)]  
  
 Finally, the implementations of the `GetArray` and `SetArray` functions are added to the end of the .CPP file.  In most cases, you will modify the Get function to return the value of the property.  The Set function will usually contain code that should execute, either before or after the property changes.  
  
 For this property to be useful, you could declare a two\-dimensional array member variable in the control class, of type **short**, to store values for the parameterized property.  You could then modify the Get function to return the value stored at the proper row and column, as indicated by the parameters, and modify the Set function to update the value referenced by the row and column parameters.  
  
##  <a name="_core_handling_errors_in_your_activex_control"></a> Handling Errors in Your ActiveX Control  
 If error conditions occur in the control, you may need to report the error to the control container.  There are two methods for reporting errors, depending on the situation in which the error occurs.  If the error occurs within a property's Get or Set function, or within the implementation of an OLE Automation method, the control should call [COleControl::ThrowError](../Topic/COleControl::ThrowError.md), which signals to the control user that an error has occurred.  If the error occurs at any other time, the control should call [COleControl::FireError](../Topic/COleControl::FireError.md), which fires a stock Error event.  
  
 To indicate the kind of error that has occurred, the control must pass an error code to `ThrowError` or `FireError`.  An error code is an OLE status code, which has a 32\-bit value.  When possible, choose an error code from the standard set of codes defined in the OLECTL.H header file.  The following table summarizes these codes.  
  
### ActiveX Control Error Codes  
  
|오류|설명|  
|--------|--------|  
|**CTL\_E\_ILLEGALFUNCTIONCALL**|Illegal function call|  
|**CTL\_E\_OVERFLOW**|오버플로가 발생했습니다.|  
|**CTL\_E\_OUTOFMEMORY**|메모리가 부족합니다.|  
|**CTL\_E\_DIVISIONBYZERO**|Division by zero|  
|**CTL\_E\_OUTOFSTRINGSPACE**|Out of string space|  
|**CTL\_E\_OUTOFSTACKSPACE**|Out of stack space|  
|**CTL\_E\_BADFILENAMEORNUMBER**|Bad file name or number|  
|**CTL\_E\_FILENOTFOUND**|File not found|  
|**CTL\_E\_BADFILEMODE**|Bad file mode|  
|**CTL\_E\_FILEALREADYOPEN**|File already open|  
|**CTL\_E\_DEVICEIOERROR**|Device I\/O error|  
|**CTL\_E\_FILEALREADYEXISTS**|File already exists|  
|**CTL\_E\_BADRECORDLENGTH**|Bad record length|  
|**CTL\_E\_DISKFULL**|디스크가 꽉 찼습니다.|  
|**CTL\_E\_BADRECORDNUMBER**|Bad record number|  
|**CTL\_E\_BADFILENAME**|Bad file name|  
|**CTL\_E\_TOOMANYFILES**|Too many files|  
|**CTL\_E\_DEVICEUNAVAILABLE**|Device unavailable|  
|**CTL\_E\_PERMISSIONDENIED**|Permission denied|  
|**CTL\_E\_DISKNOTREADY**|Disk not ready|  
|**CTL\_E\_PATHFILEACCESSERROR**|Path\/file access error|  
|**CTL\_E\_PATHNOTFOUND**|Path not found|  
|**CTL\_E\_INVALIDPATTERNSTRING**|Invalid pattern string|  
|**CTL\_E\_INVALIDUSEOFNULL**|Invalid use of NULL|  
|**CTL\_E\_INVALIDFILEFORMAT**|Invalid file format|  
|**CTL\_E\_INVALIDPROPERTYVALUE**|Invalid property value|  
|**CTL\_E\_INVALIDPROPERTYARRAYINDEX**|Invalid property array index|  
|**CTL\_E\_SETNOTSUPPORTEDATRUNTIME**|Set not supported at run time|  
|**CTL\_E\_SETNOTSUPPORTED**|Set not supported \(read\-only property\)|  
|**CTL\_E\_NEEDPROPERTYARRAYINDEX**|Need property array index|  
|**CTL\_E\_SETNOTPERMITTED**|Set not permitted|  
|**CTL\_E\_GETNOTSUPPORTEDATRUNTIME**|Get not supported at run time|  
|**CTL\_E\_GETNOTSUPPORTED**|Get not supported \(write\-only property\)|  
|**CTL\_E\_PROPERTYNOTFOUND**|Property not found|  
|**CTL\_E\_INVALIDCLIPBOARDFORMAT**|Invalid clipboard format|  
|**CTL\_E\_INVALIDPICTURE**|Invalid picture|  
|**CTL\_E\_PRINTERERROR**|Printer error|  
|**CTL\_E\_CANTSAVEFILETOTEMP**|Can't save file to TEMP|  
|**CTL\_E\_SEARCHTEXTNOTFOUND**|Search text not found|  
|**CTL\_E\_REPLACEMENTSTOOLONG**|Replacements too long|  
  
 If necessary, use the **CUSTOM\_CTL\_SCODE** macro to define a custom error code for a condition that is not covered by one of the standard codes.  The parameter for this macro should be an integer between 1000 and 32767, inclusive.  예를 들면 다음과 같습니다.  
  
 [!code-cpp[NVC_MFC_AxUI#37](../mfc/codesnippet/CPP/mfc-activex-controls-advanced-topics_4.cpp)]  
  
 If you are creating an ActiveX control to replace an existing VBX control, define your ActiveX control error codes with the same numeric values the VBX control uses to ensure that the error codes are compatible.  
  
##  <a name="_core_handling_special_keys_in_your_control"></a> Handling Special Keys in the Control  
 In some cases you may want to handle certain keystroke combinations in a special way; for example, insert a new line when the ENTER key is pressed in a multiline text box control or move between a group of edit controls when a directional key ID pressed.  
  
 If the base class of your ActiveX control is `COleControl`, you can override [CWnd::PreTranslateMessage](../Topic/CWnd::PreTranslateMessage.md) to handle messages before the container processes them.  When using this technique, always return **TRUE** if you handle the message in your override of `PreTranslateMessage`.  
  
 The following code example demonstrates a possible way of handling any messages related to the directional keys.  
  
 [!code-cpp[NVC_MFC_AxUI#38](../mfc/codesnippet/CPP/mfc-activex-controls-advanced-topics_5.cpp)]  
  
 For more information on handling keyboard interfaces for an ActiveX control, see the ActiveX SDK documentation.  
  
##  <a name="_core_accessing_dialog_controls_that_are_invisible_at_run_time"></a> Accessing Dialog Controls that Are Invisible at Run Time  
 You can create dialog controls that have no user interface and are invisible at run time.  If you add an invisible at run time ActiveX control to a dialog box and use [CWnd::GetDlgItem](../Topic/CWnd::GetDlgItem.md) to access the control, the control will not work correctly.  Instead, you should use one of the following techniques to obtain an object that represents the control:  
  
-   Using the Add Member Variable Wizard, select **Control Variable** and then select the control's ID.  Enter a member variable name and select the control's wrapper class as the **Control Type**.  
  
     또는  
  
-   Declare a local variable and subclass as the dialog item.  Insert code that resembles the following \(`CMyCtrl` is the wrapper class, `IDC_MYCTRL1` is the control's ID\):  
  
     [!code-cpp[NVC_MFC_AxCont#19](../mfc/codesnippet/CPP/mfc-activex-controls-advanced-topics_6.cpp)]  
  
## 참고 항목  
 [MFC ActiveX 컨트롤](../mfc/mfc-activex-controls.md)