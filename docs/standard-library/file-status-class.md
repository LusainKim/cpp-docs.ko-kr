---
title: "file_status 클래스 | Microsoft 문서"
ms.custom: 
ms.date: 11/04/2016
ms.reviewer: 
ms.suite: 
ms.technology:
- devlang-cpp
ms.tgt_pltfrm: 
ms.topic: article
f1_keywords:
- file_status
- std::experimental::filesystem::v1::file_status
- filesystem/std::experimental::filesystem::v1::file_status
- std::experimental::filesystem::v1::file_status::operator=
- filesystem/std::experimental::filesystem::v1::file_status::operator=
- std::experimental::filesystem::v1::file_status::type
- filesystem/std::experimental::filesystem::v1::file_status::type
- std::experimental::filesystem::v1::file_status::permissions
- filesystem/std::experimental::filesystem::v1::file_status::permissions
dev_langs:
- C++
ms.assetid: 9781840e-ad22-44dd-ad79-0fabaa94bac4
caps.latest.revision: 15
author: corob-msft
ms.author: corob
manager: ghogen
translation.priority.mt:
- cs-cz
- de-de
- es-es
- fr-fr
- it-it
- ja-jp
- ko-kr
- pl-pl
- pt-br
- ru-ru
- tr-tr
- zh-cn
- zh-tw
translationtype: Machine Translation
ms.sourcegitcommit: c7f3b346bc8abeab0c6bd913fc0b554bef4ed208
ms.openlocfilehash: 954da8df11c2382887717baa61070acc0b6070b4
ms.lasthandoff: 02/24/2017

---
# <a name="filestatus-class"></a>file_status 클래스
[file_type](../standard-library/filesystem-enumerations.md#filesystem__file_type) 및 파일 [perms](../standard-library/filesystem-enumerations.md#filesystem__perms)를 래핑합니다.  
  
## <a name="syntax"></a>구문  
  
```cpp  
class file_status;  
```  
  
## <a name="filestatusfilestatus"></a>file_status::file_status  
  
```cpp  
explicit file_status(  
   file_type ftype = file_type::none,  
   perms mask = perms::unknown) noexcept;  
  
file_status(const file_status&) noexcept = default;  
  
file_status(file_status&&) noexcept = default; 

~file_status() noexcept = default; 
```  
  
## <a name="filestatusoperator"></a>file_status::operator=  
  
```cpp  
file_status& operator=(const file_status&) noexcept = default;  
file_status& operator=(file_status&&) nexcept = default;  
```  
  
 기본 멤버 대입 연산자가 예상대로 작동합니다.  
  
## <a name="type"></a>type  
  
```cpp  
file_type type() const noexcept  
void type(file_type ftype) noexcept  
```  
  
 file_type을 가져오거나 설정합니다.  
  
## <a name="permissions"></a>permissions  
  
``cpp  
perms permissions() const noexcept  
void permissions(perms mask) noexcept   
```  
  
 Gets or sets the file permissions.  
  
 Use the setter to make a file readonly or remove the readonly attribute.  
  
## Requirements  
 **Header:** \<filesystem>  
  
 **Namespace:** std::experimental::filesystem, std::experimental::filesystem::v1  
  
## See Also  
 [Header Files Reference](../standard-library/cpp-standard-library-header-files.md)   
 [path Class](../standard-library/path-class.md)   
 [\<filesystem>](../standard-library/filesystem.md)


