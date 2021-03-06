---
title: "sample container 클래스 | Microsoft Docs"
ms.custom: 
ms.date: 11/04/2016
ms.reviewer: 
ms.suite: 
ms.technology: cpp-standard-libraries
ms.tgt_pltfrm: 
ms.topic: article
dev_langs: C++
helpviewer_keywords: container classes [C++]
ms.assetid: 5b1451f2-c708-45da-bbf0-9e42fd687a1a
caps.latest.revision: "10"
author: corob-msft
ms.author: corob
manager: ghogen
ms.workload: cplusplus
ms.openlocfilehash: 3666bf4ee03149a9c00ec93d9fc1dc536ce2d080
ms.sourcegitcommit: 8fa8fdf0fbb4f57950f1e8f4f9b81b4d39ec7d7a
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 12/21/2017
---
# <a name="sample-container-class"></a>Sample Container 클래스
> [!NOTE]
>  이 항목은 C++ 표준 라이브러리에서 사용되는 작동하지 않는 컨테이너 예제로 Visual C++ 설명서에 포함되어 있습니다. 자세한 내용은 [C++ 표준 라이브러리 컨테이너](../standard-library/stl-containers.md)를 참조하세요.  
  
 다양한 길이의 요소 시퀀스를 제어하는 개체(대개 **Ty** 형식)를 설명합니다. 시퀀스는 실제 컨테이너에 따라 다른 방식으로 저장됩니다.  
  
 컨테이너 생성자 또는 구성원 함수는 생성자 **Ty**(**const Ty&**) 또는 함수 **Ty::operator=**(**const Ty&**)를 호출할 수 있습니다. 이러한 호출에서 예외가 throw되면 container 개체는 무결성을 유지하고 catch하는 예외를 다시 throw해야 합니다. container 개체가 이러한 예외 중 하나를 throw한 후에도 해당 개체를 안전하게 교환, 할당, 제거하거나 지울 수 있습니다. 그러나 일반적으로는 container 개체가 제어하는 시퀀스의 상태를 예측할 수 없습니다.  
  
 이와 관련한 몇 가지 추가 주의 사항은 다음과 같습니다.  
  
-   **~Ty** 식이 예외를 throw하면 container 개체의 결과 상태는 정의되지 않습니다.  
  
-   컨테이너가 allocator 개체 *al*을 정의하는 경우 *al*이 *al***.allocate** 호출의 결과를 제외한 예외를 throw하면 container 개체의 결과 상태는 정의되지 않습니다.  
  
-   컨테이너가 제어되는 시퀀스의 순서를 지정할 방법을 결정하기 위해 function 개체 *comp*를 저장하는 경우 *comp*가 종류와 관계없이 예외를 throw하면 container 개체의 결과 상태는 정의되지 않습니다.  
  
 다음 단락에서 설명하는 것처럼, C++ 표준 라이브러리를 통해 정의되는 container 클래스는 여러 가지 추가 요구 사항을 충족합니다.  
  
 컨테이너 템플릿 클래스 [list](../standard-library/list-class.md)는 위에서 설명한 예외가 발생하더라도 명확하게 정의되는 유용한 동작을 제공합니다. 예를 들어 요소 하나 이상을 삽입하는 동안 예외가 throw되어도 컨테이너는 변경되지 않고 그대로 유지되며 예외가 다시 throw됩니다.  
  
 C++ 표준 라이브러리를 통해 정의되는 *모든* 컨테이너 클래스에 대해 다음 구성원 함수를 호출하는 중에 예외가 throw되는 경우  
  
```  
<A NAME="vclrfcontainerinsert"></A>insert // single element inserted  
<A NAME="vclrfcontainerpushback"></A>push_back  
<A NAME="vclrfcontainerpushfront"></A>push_front  
```  
  
 컨테이너는 변경되지 않고 그대로 유지되며 예외가 다시 throw됩니다.  
  
 C++ 표준 라이브러리를 통해 정의되는 *모든* 컨테이너 클래스에 대해 다음 구성원 함수를 호출하는 중에 예외가 throw되지 않는 경우  
  
```  
<A NAME="vclrfcontainerpopback"></A>pop_back  
<A NAME="vclrfcontainerpopfront"></A>pop_front  
```  
  
 구성원 함수 [erase](../standard-library/container-class-erase.md)는 복사 작업(할당 또는 복사본 생성)에서 예외가 throw되는 경우에만 예외를 throw합니다.  
  
 또한 구성원 함수가 반환하는 반복기를 복사하는 동안에는 예외가 throw되지 않습니다.  
  
 구성원 함수 [swap](../standard-library/container-class-swap.md)은 C++ 표준 라이브러리를 통해 정의되는 *모든* 컨테이너 클래스에 대해 다음과 같은 사항을 추가로 보장합니다.  
  
-   구성원 함수는 컨테이너가 allocator 개체 al을 저장하며 복사 시에 `al`이 예외를 throw하는 경우에만 예외를 throw합니다.  
  
-   교환 중에 제어되는 시퀀스의 요소를 지정하는 참조, 포인터 및 반복기는 유효한 상태로 유지됩니다.  
  
 C++ 표준 라이브러리를 통해 정의되는 컨테이너 클래스의 개체는 `Alloc` 형식의 저장된 개체(대개 템플릿 매개 변수)를 통해 제어하는 시퀀스용 저장소를 할당하고 확보합니다. 그러한 allocator 개체에는 클래스 **allocator\<Ty>**의 개체와 같은 외부 인터페이스가 있어야 합니다. 특히 `Alloc`는 **Alloc::rebind<value_type>::other**와 같은 형식이어야 합니다.  
  
 C++ 표준 라이브러리를 통해 정의되는 *모든* 컨테이너 클래스에 대해 구성원 함수 **Alloc get_allocator const;**는 저장된 allocator 개체의 복사본을 반환합니다. container 개체를 할당하는 경우 저장된 allocator 개체는 복사되지 *않습니다*. 모든 생성자는 allocator 매개 변수를 포함하지 않는 경우 **allocator**에 저장된 값을 `Alloc`로 초기화합니다.  
  
 C++ 표준에 따라 C++ 표준 라이브러리를 통해 정의되는 컨테이너 클래스에 대해서는 다음 사항을 가정할 수 있습니다.  
  
-   `Alloc` 클래스의 모든 개체는 비교 시 동일합니다.  
  
-   **Alloc::const_pointer** 형식은 **const Ty \***와 동일합니다.  
  
-   **Alloc::const_reference** 형식은 **const Ty&**와 동일합니다.  
  
-   **Alloc::pointer** 형식은 **Ty \***와 동일합니다.  
  
-   **Alloc::reference** 형식은 **Ty&**와 동일합니다.  
  
 그러나 이 구현에서 컨테이너는 이와 같이 단순한 가정을 하지 않습니다. 따라서 보다 복잡한 allocator 개체와도 적절하게 연동됩니다.  
  
-   클래스 `Alloc`의 모든 개체는 비교 시 같을 필요가 없습니다. 여러 저장소 풀을 유지 관리하면 되기 때문입니다.  
  
-   **Alloc::const_pointer** 형식은 **const Ty \***와 동일하지 않아도 됩니다. const 포인터는 클래스일 수도 있습니다.  
  
-   **Alloc::pointer** 형식은 **Ty \***와 동일하지 않아도 됩니다. 포인터는 클래스일 수도 있습니다.  
  
## <a name="requirements"></a>요구 사항  
 **헤더**: \<sample container>  
  
## <a name="see-also"></a>참고 항목  
 [\<sample container>](../standard-library/sample-container.md)

