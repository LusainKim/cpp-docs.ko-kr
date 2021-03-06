---
title: "방법:.NET Framework로 이미지 표시 | Microsoft Docs"
ms.custom: 
ms.date: 11/04/2016
ms.reviewer: 
ms.suite: 
ms.technology: cpp-windows
ms.tgt_pltfrm: 
ms.topic: article
dev_langs: C++
helpviewer_keywords:
- GDI+ [C++], displaying images
- graphics [C++], displaying images
ms.assetid: c0eddfa1-4bd6-4af5-a533-1fa84b360325
caps.latest.revision: "16"
author: mikeblome
ms.author: mblome
manager: ghogen
ms.workload:
- cplusplus
- dotnet
ms.openlocfilehash: 7c12d6a67f6fbe73802d3b876621a2ea606af553
ms.sourcegitcommit: 54035dce0992ba5dce0323d67f86301f994ff3db
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 01/03/2018
---
# <a name="how-to-display-images-with-the-net-framework"></a>방법: .NET Framework로 이미지 표시
다음 코드 예제에서는 수정 OnPaint 이벤트 처리기에 대 한 포인터를 검색 하는 <xref:System.Drawing.Graphics> 기본 폼에 대 한 개체입니다. <xref:System.Windows.Forms.Form.OnPaint%2A> 함수는 대부분 Visual Studio 응용 프로그램 마법사를 사용 하 여 만든 Windows Forms 응용 프로그램을 위한 것입니다.  
  
 이미지가 표시 됩니다는 <xref:System.Drawing.Image> 클래스입니다. 이미지 데이터가 사용 하 여.jpg 파일에서 로드 되는 <xref:System.Drawing.Image.FromFile%2A?displayProperty=fullName> 메서드. 이미지를 폼에 그릴 전에 폼 이미지에 맞게 크기가 조정 됩니다. 이미지를 그리는 하 여 수행 됩니다는 <xref:System.Drawing.Graphics.DrawImage%2A?displayProperty=fullName> 메서드.  
  
 <xref:System.Drawing.Graphics> 및 <xref:System.Drawing.Image> 클래스는 모두는 <xref:System.Drawing?displayProperty=fullName> 네임 스페이스입니다.  
  
> [!NOTE]
>  GDI + Windows XP에 포함 되어 있으며 Windows NT 4.0 SP 6, Windows 2000, Windows 98 및 Windows me 재배포 가능 구성 요소로 제공 됩니다. 최신 재배포 가능 패키지를 다운로드 하려면 [http://go.microsoft.com/fwlink/p/?linkid=11232](http://go.microsoft.com/fwlink/p/?linkid=11232)합니다.   
  
## <a name="example"></a>예  
  
```  
#using <system.drawing.dll>  
  
using namespace System;  
using namespace System::Drawing;  
  
protected:  
virtual Void Form1::OnPaint(PaintEventArgs^ pe) override  
{  
    Graphics^ g = pe->Graphics;  
    Image^ image = Image::FromFile("SampleImage.jpg");  
    Form::ClientSize = image->Size;  
    g->DrawImage( image, 0, 0, image->Size.Width, image->Size.Height );  
}  
```  
  
## <a name="see-also"></a>참고 항목  
 <xref:System.Drawing?displayProperty=fullName>   
 [C++/CLI를 사용한 .NET 프로그래밍(Visual C++)](../dotnet/dotnet-programming-with-cpp-cli-visual-cpp.md)