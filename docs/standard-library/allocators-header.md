---
title: "&lt;allocators&gt; | Microsoft Docs"
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
  - "stdext::<allocators>"
  - "allocators/stdext::allocators"
  - "<allocators>"
  - "stdext.<allocators>"
dev_langs: 
  - "C++"
helpviewer_keywords: 
  - "allocators 헤더"
ms.assetid: 4393a607-4df8-4278-bbb2-c8ec52e60b83
caps.latest.revision: 19
caps.handback.revision: 9
author: "corob-msft"
ms.author: "corob"
manager: "ghogen"
---
# &lt;allocators&gt;
[!INCLUDE[vs2017banner](../assembler/inline/includes/vs2017banner.md)]

Defines several templates that help allocate and free memory blocks for node\-based containers.  
  
## 구문  
  
```  
#include <allocators>  
```  
  
## 설명  
 The \<allocators\> header provides six allocator templates that can be used to select memory\-management strategies for node\-based containers.  For use with these templates, it also provides several different synchronization filters to tailor the memory\-management strategy to a variety of different multithreading schemes \(including none\).  Matching a memory management strategy to the known memory usage patterns, and synchronization requirements, of a particular application can often increase the speed or reduce the overall memory requirements of an application.  
  
 The allocator templates are implemented with reusable components that can be customized or replaced to provide additional memory\-management strategies.  
  
 The node\-based containers in the Standard C\+\+ library \(std::list, std::set, std::multiset, std::map and std::multimap\) store their elements in individual nodes.  All the nodes for a particular container type are the same size, so the flexibility of a general\-purpose memory manager is not needed.  Because the size of each memory block is known at compile time, the memory manager can be much simpler and faster.  
  
 When used with containers that are not node\-based \(such as the Standard C\+\+ library containers std::vector std::deque, and std::basic\_string\), the alllocator templates will work correctly, but are not likely to provide any performance improvement over the default allocator.  
  
 An allocator is a template class that describes an object that manages storage allocation and freeing for objects and arrays of objects of a designated type.  Allocator objects are used by several container template classes in the Standard C\+\+ library.  
  
 The allocators are all templates of this type:  
  
 `template<class`  `Type` `>`  
  
 `class allocator;`  
  
 where the template argument `Type` is the type managed by the allocator instance.  The Standard C\+\+ library provides a default allocator, template class [allocator](../standard-library/allocator-class.md), which is defined in [\<memory\>](../standard-library/memory.md).  The \<allocators\> header provides the following allocators:  
  
-   [allocator\_newdel](../standard-library/allocator-newdel-class.md)  
  
-   [allocator\_unbounded](../standard-library/allocator-unbounded-class.md)  
  
-   [allocator\_fixed\_size](../standard-library/allocator-fixed-size-class.md)  
  
-   [allocator\_variable\_size](../standard-library/allocator-variable-size-class.md)  
  
-   [allocator\_suballoc](../standard-library/allocator-suballoc-class.md)  
  
-   [allocator\_chunklist](../standard-library/allocator-chunklist-class.md)  
  
 Use an appropriate instantiation of an allocator as the second type argument when creating a container, such as the following code example.  
  
 `#include <list>`  
  
 `#include <allocators>`  
  
 `std::list<int, stdext::allocators::allocator_chunklist<int> > _List0;`  
  
 \_List0 allocates nodes with `allocator_chunklist` and the default synchronization filter.  
  
 Use the macro [ALLOCATOR\_DECL](../Topic/ALLOCATOR_DECL%20\(%3Callocators%3E\).md) to create allocator templates with synchronization filters other than the default:  
  
 `#include <list>`  
  
 `#include <allocators>`  
  
 `ALLOCATOR_DECL(CACHE_CHUNKLIST, stdext::allocators::sync_per_thread, Alloc);`  
  
 `std::list<int, alloc<int> > _List1;`  
  
 \_Lst1 allocates nodes with `allocator_chunklist` and the [sync\_per\_thread](../standard-library/sync-per-thread-class.md) synchronization filter.  
  
 A block allocator is a cache or a filter.  A cache is a template class that takes one argument of type std::size\_t.  It defines a block allocator that allocates and deallocates memory blocks of a single size.  It must obtain memory using operator `new`, but it need not make a separate call to operator `new` for each block.  It may, for example, suballocate from a larger block or cache deallocated blocks for subsequent reallocation.  
  
 With a compiler that cannot compile rebind the value of the std::size\_t argument used when the template was instantiated is not necessarily the value of the argument \_Sz passed to a cache's member functions allocate and deallocate.  
  
 \<allocators\> provides the following cache templates:  
  
-   [cache\_freelist](../standard-library/cache-freelist-class.md)  
  
-   [cache\_suballoc](../standard-library/cache-suballoc-class.md)  
  
-   [cache\_chunklist](../standard-library/cache-chunklist-class.md)  
  
 A filter is a block allocator that implements its member functions using another block allocator which is passed to it as a template argument.  The most common form of filter is a synchronization filter, which applies a synchronization policy to control access to the member functions of an instance of another block allocator. \<allocators\> provides the following synchronization filters:  
  
-   [sync\_none](../standard-library/sync-none-class.md)  
  
-   [sync\_per\_container](../standard-library/sync-per-container-class.md)  
  
-   [sync\_per\_thread](../standard-library/sync-per-thread-class.md)  
  
-   [sync\_shared](../standard-library/sync-shared-class.md)  
  
 \<allocators\> also provides the filter [rts\_alloc](../standard-library/rts-alloc-class.md), which holds multiple block allocator instances and determines which instance to use for allocation or deallocation at runtime instead of at compile time.  It is used with compilers that cannot compile rebind.  
  
 A synchronization policy determines how an allocator instance handles simultaneous allocation and deallocation requests from multiple threads.  The simplest policy is to pass all requests directly through to the underlying cache object, leaving synchronization management to the user.  A more complex policy could be to use a mutex to serialize access to the underlying cache object.  
  
 If a compiler supports compiling both single\-threaded and multi\-threaded applications, the default synchronization filter for single\-threaded applications is `sync_none`; for all other cases it is `sync_shared`.  
  
 The cache template `cache_freelist` takes a max class argument which determines the maximum number of elements to be stored in the free list.  
  
 \<allocators\> provides the following max classes:  
  
-   [max\_none](../standard-library/max-none-class.md)  
  
-   [max\_unbounded](../standard-library/max-unbounded-class.md)  
  
-   [max\_fixed\_size](../standard-library/max-fixed-size-class.md)  
  
-   [max\_variable\_size](../standard-library/max-variable-size-class.md)  
  
### 매크로  
  
|||  
|-|-|  
|[ALLOCATOR\_DECL](../Topic/ALLOCATOR_DECL%20\(%3Callocators%3E\).md)|Yields an allocator template class.|  
|[CACHE\_CHUNKLIST](../Topic/CACHE_CHUNKLIST%20\(%3Callocators%3E\).md)|Yields `stdext::allocators::cache_chunklist<sizeof(Type)>`.|  
|[CACHE\_FREELIST](../Topic/CACHE_FREELIST%20\(%3Callocators%3E\).md)|Yields `stdext::allocators::cache_freelist<sizeof(Type), max>`.|  
|[CACHE\_SUBALLOC](../Topic/CACHE_SUBALLOC%20\(%3Callocators%3E\).md)|Yields `stdext::allocators::cache_suballoc<sizeof(Type)>`.|  
|[SYNC\_DEFAULT](../Topic/SYNC_DEFAULT%20\(%3Callocators%3E\).md)|Yields a synchronization filter.|  
  
### 연산자  
  
|||  
|-|-|  
|[operator\!\=](../Topic/operator!=%20\(%3Callocators%3E\).md)|지정된 클래스의 할당자 개체가 다른지 테스트합니다.|  
|[operator\=\=](../Topic/operator==%20\(%3Callocators%3E\).md)|지정된 클래스의 할당자 개체가 같은지 테스트합니다.|  
  
### 클래스  
  
|||  
|-|-|  
|[allocator\_base](../standard-library/allocator-base-class.md)|Defines the base class and common functions needed to create a user\-defined allocator from a synchronization filter.|  
|[allocator\_chunklist](../standard-library/allocator-chunklist-class.md)|Describes an object that manages storage allocation and freeing for objects using a cache of type [cache\_chunklist](../standard-library/cache-chunklist-class.md).|  
|[allocator\_fixed\_size](../standard-library/allocator-fixed-size-class.md)|Describes an object that manages storage allocation and freeing for objects of type `Type` using a cache of type [cache\_freelist](../standard-library/cache-freelist-class.md) with a length managed by [max\_fixed\_size](../standard-library/max-fixed-size-class.md).|  
|[allocator\_newdel](../standard-library/allocator-newdel-class.md)|Implements an allocator that uses `operator delete` to deallocate a memory block and `operator new` to allocate a memory block.|  
|[allocator\_suballoc](../standard-library/allocator-suballoc-class.md)|Describes an object that manages storage allocation and freeing for objects of type `Type` using a cache of type [cache\_suballoc](../standard-library/cache-suballoc-class.md).|  
|[allocator\_unbounded](../standard-library/allocator-unbounded-class.md)|Describes an object that manages storage allocation and freeing for objects of type `Type` using a cache of type [cache\_freelist](../standard-library/cache-freelist-class.md) with a length managed by [max\_unbounded](../standard-library/max-unbounded-class.md).|  
|[allocator\_variable\_size](../standard-library/allocator-variable-size-class.md)|Describes an object that manages storage allocation and freeing for objects of type `Type` using a cache of type [cache\_freelist](../standard-library/cache-freelist-class.md) with a length managed by [max\_variable\_size](../standard-library/max-variable-size-class.md).|  
|[cache\_chunklist](../standard-library/cache-chunklist-class.md)|Defines a block allocator that allocates and deallocates memory blocks of a single size.|  
|[cache\_freelist](../standard-library/cache-freelist-class.md)|Defines a block allocator that allocates and deallocates memory blocks of a single size.|  
|[cache\_suballoc](../standard-library/cache-suballoc-class.md)|Defines a block allocator that allocates and deallocates memory blocks of a single size.|  
|[freelist](../standard-library/freelist-class.md)|Manages a list of memory blocks.|  
|[max\_fixed\_size](../standard-library/max-fixed-size-class.md)|Describes a max class object that limits a [freelist](../standard-library/freelist-class.md) object to a fixed maximum length.|  
|[max\_none](../standard-library/max-none-class.md)|Describes a max class object that limits a [freelist](../standard-library/freelist-class.md) object to a maximum length of zero.|  
|[max\_unbounded](../standard-library/max-unbounded-class.md)|Describes a max class object that does not limit the maximum length of a [freelist](../standard-library/freelist-class.md) object.|  
|[max\_variable\_size](../standard-library/max-variable-size-class.md)|Describes a max class object that limits a [freelist](../standard-library/freelist-class.md) object to a maximum length that is roughly proportional to the number of allocated memory blocks.|  
|[rts\_alloc](../standard-library/rts-alloc-class.md)|The rts\_alloc template class describes a [filter](../standard-library/allocators-header.md) that holds an array of cache instances and determines which instance to use for allocation and deallocation at runtime instead of at compile time.|  
|[sync\_none](../standard-library/sync-none-class.md)|Describes a synchronization filter that provides no synchronization.|  
|[sync\_per\_container](../standard-library/sync-per-container-class.md)|Describes a synchronization filter that provides a separate cache object for each allocator object.|  
|[sync\_per\_thread](../standard-library/sync-per-thread-class.md)|Describes a synchronization filter that provides a separate cache object for each thread.|  
|[sync\_shared](../standard-library/sync-shared-class.md)|Describes a synchronization filter that uses a mutex to control access to a cache object that is shared by all allocators.|  
  
## 요구 사항  
 **Header:** \<allocators\>  
  
 **네임스페이스:** stdext  
  
## 참고 항목  
 [헤더 파일 참조](../standard-library/cpp-standard-library-header-files.md)