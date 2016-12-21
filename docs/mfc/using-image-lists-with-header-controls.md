---
title: "이미지 목록과 헤더 컨트롤 함께 사용 | Microsoft Docs"
ms.custom: ""
ms.date: "12/03/2016"
ms.prod: "visual-studio-dev14"
ms.reviewer: ""
ms.suite: ""
ms.technology: 
  - "devlang-cpp"
ms.tgt_pltfrm: ""
ms.topic: "article"
dev_langs: 
  - "C++"
helpviewer_keywords: 
  - "CHeaderCtrl 클래스, 이미지 목록"
  - "헤더 컨트롤, 이미지 목록"
  - "이미지 목록[C++], 헤더 컨트롤"
ms.assetid: d5e9b310-6278-406c-909c-eefa09549a47
caps.latest.revision: 10
caps.handback.revision: 6
author: "mikeblome"
ms.author: "mblome"
manager: "ghogen"
---
# 이미지 목록과 헤더 컨트롤 함께 사용
[!INCLUDE[vs2017banner](../assembler/inline/includes/vs2017banner.md)]

Header items have the ability to display an image within a header item.  This image, stored in an associated image list, is 16 x 16 pixels and has the same characteristics as the icon images used in a list view control.  In order to implement this behavior successfully, you must first create and initialize the image list, associate the list with the header control, and then modify the attributes of the header item that will display the image.  
  
 The following procedure illustrates the details, using a pointer to a header control \(`m_pHdrCtrl`\) and a pointer to an image list \(`m_pHdrImages`\).  
  
### To display an image in a header item  
  
1.  Construct a new image list \(or use an existing image list object\) using the [CImageList](../mfc/reference/cimagelist-class.md) constructor, storing the resultant pointer.  
  
2.  Initialize the new image list object by calling [CImageList::Create](../Topic/CImageList::Create.md).  The following code is one example of this call.  
  
     [!code-cpp[NVC_MFCControlLadenDialog#15](../mfc/codesnippet/CPP/using-image-lists-with-header-controls_1.cpp)]  
  
3.  Add the images for each header item.  The following code adds two predefined images.  
  
     [!code-cpp[NVC_MFCControlLadenDialog#16](../mfc/codesnippet/CPP/using-image-lists-with-header-controls_2.cpp)]  
  
4.  Associate the image list with the header control with a call to [CHeaderCtrl::SetImageList](../Topic/CHeaderCtrl::SetImageList.md).  
  
5.  Modify the header item to display an image from the associated image list.  The following example assigns the first image, from `m_phdrImages`, to the first header item, `m_pHdrCtrl`.  
  
     [!code-cpp[NVC_MFCControlLadenDialog#17](../mfc/codesnippet/CPP/using-image-lists-with-header-controls_3.cpp)]  
  
 For detailed information on the parameter values used, consult the pertinent [CHeaderCtrl](../mfc/reference/cheaderctrl-class.md).  
  
> [!NOTE]
>  It is possible to have multiple controls using the same image list.  For instance, in a standard list view control, there could be an image list \(of 16 x 16 pixel images\) used by both the small icon view of a list view control and the header items of the list view control.  
  
## 참고 항목  
 [CHeaderCtrl 사용](../mfc/using-cheaderctrl.md)