---
title: "약한 참조 및 순환 끊기 (C + + /cli CX) | Microsoft Docs"
ms.custom: 
ms.date: 01/22/2017
ms.technology: cpp-windows
ms.reviewer: 
ms.suite: 
ms.tgt_pltfrm: 
ms.topic: article
ms.assetid: 1acb6402-05f0-4951-af94-0e9dab41c53e
caps.latest.revision: "12"
author: ghogen
ms.author: ghogen
manager: ghogen
ms.workload: cplusplus
ms.openlocfilehash: 5adb4f2376213d2c297b40f82382261fcf961349
ms.sourcegitcommit: 8fa8fdf0fbb4f57950f1e8f4f9b81b4d39ec7d7a
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 12/21/2017
---
# <a name="weak-references-and-breaking-cycles-ccx"></a>약한 참조 및 순환 중단(C++/CX)
참조 횟수를 기반으로 하는 모든 형식 시스템에서는 형식 참조가 *순환*을 형성할 수 있는 문제가 있습니다. 즉, 하나의 개체가 두 번째 개체를 참조하고, 두 번째 개체가 세 번째 개체를 참조하는 식으로 최종 개체가 첫 번째 개체를 다시 참조할 때까지 진행됩니다. 이러한 순환에서는 한 개체의 참조 횟수가 0인 경우 개체를 올바르게 삭제할 수 없습니다. C +이 문제 해결을 돕기 위해 + CX 제공는 [platform:: weakreference 클래스](../cppcx/platform-weakreference-class.md) 클래스입니다. `WeakReference` 개체는 [Resolve](../cppcx/platform-weakreference-class.md#resolve) 메서드를 지원하며, 이 메서드는 개체가 더 이상 존재하지 않는 경우 null을 반환하고 개체가 활성 상태이지만 [형식이 아닌 경우](../cppcx/platform-invalidcastexception-class.md) Platform::InvalidCastException `T`을 throw합니다.  
  
 `WeakReference` 를 사용해야 하는 한 가지 시나리오는 `this` 포인터가 이벤트 처리기를 정의하는 데 사용되는 람다 식에서 캡처되는 경우입니다. 이벤트 처리기를 정의할 때 명명된 메서드를 사용하는 것이 좋지만 이벤트 처리기에 람다를 사용하려는 경우나 다른 상황에서 참조 횟수 순환을 끊어야 하는 경우에는 `WeakReference`를 사용하세요. 예를 들면 다음과 같습니다.  
  
```  
  
using namespace Platform::Details;  
using namespace Windows::UI::Xaml;  
using namespace Windows::UI::Xaml::Input;  
using namespace Windows::UI::Xaml::Controls;  
  
Class1::Class1()  
{  
    // Class1 has a reference to m_Page  
    m_Page = ref new Page();  
  
    // m_Page will have a reference to this Class1  
    // so create a weak reference to this  
    WeakReference wr(this);  
    m_Page->DoubleTapped += ref new DoubleTappedEventHandler(   
        [wr](Object^ sender, DoubleTappedRoutedEventArgs^ args)  
    {  
       // Use the weak reference to get the object  
       Class1^ c = wr.Resolve<Class1>();  
       if (c != nullptr)  
       {  
           c->m_eventFired = true;  
       }  
       else  
       {  
           // Inform the event that this handler should be removed  
           // from the subscriber list  
           throw ref new DisconnectedException();  
       }  
    });   
}  
  
}  
```  
  
 이벤트 처리기가 `DisconnectedException`을 throw하면 이벤트가 구독자 목록에서 처리기를 제거합니다.  
  
## <a name="see-also"></a>참고 항목  


