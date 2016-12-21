---
title: "schedule | Microsoft Docs"
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
  - "schedule"
dev_langs: 
  - "C++"
helpviewer_keywords: 
  - "schedule OpenMP clause"
ms.assetid: 286f1fc3-6598-4837-b4c8-8b1fa3193965
caps.latest.revision: 12
caps.handback.revision: 10
author: "mikeblome"
ms.author: "mblome"
manager: "ghogen"
---
# schedule
[!INCLUDE[vs2017banner](../../../assembler/inline/includes/vs2017banner.md)]

적용 되는 [for](../../../parallel/openmp/reference/for-openmp.md) 지시문입니다.  
  
## 구문  
  
```  
schedule(type[,size])  
```  
  
#### 매개 변수  
 `type`  
 일정 관리의 종류:  
  
-   `dynamic`  
  
-   `guided`  
  
-   `runtime`  
  
-   `static`  
  
 `size`\(선택적 요소\)  
 반복의 크기를 지정합니다.  `size`정수 여야 합니다.  Not valid when `type` is `runtime`.  
  
## 설명  
 자세한 내용은 [2.4.1 for Construct](../../../parallel/openmp/2-4-1-for-construct.md)를 참조하십시오.  
  
## 예제  
  
```  
// omp_schedule.cpp  
// compile with: /openmp   
#include <windows.h>  
#include <stdio.h>  
#include <omp.h>  
  
#define NUM_THREADS 4  
#define STATIC_CHUNK 5  
#define DYNAMIC_CHUNK 5  
#define NUM_LOOPS 20  
#define SLEEP_EVERY_N 3  
  
int main( )   
{  
    int nStatic1[NUM_LOOPS],   
        nStaticN[NUM_LOOPS];  
    int nDynamic1[NUM_LOOPS],   
        nDynamicN[NUM_LOOPS];  
    int nGuided[NUM_LOOPS];  
  
    omp_set_num_threads(NUM_THREADS);  
  
    #pragma omp parallel  
    {  
        #pragma omp for schedule(static, 1)  
        for (int i = 0 ; i < NUM_LOOPS ; ++i)   
        {  
            if ((i % SLEEP_EVERY_N) == 0)   
                Sleep(0);  
            nStatic1[i] = omp_get_thread_num( );  
        }  
  
        #pragma omp for schedule(static, STATIC_CHUNK)  
        for (int i = 0 ; i < NUM_LOOPS ; ++i)   
        {  
            if ((i % SLEEP_EVERY_N) == 0)   
                Sleep(0);  
            nStaticN[i] = omp_get_thread_num( );  
        }  
  
        #pragma omp for schedule(dynamic, 1)  
        for (int i = 0 ; i < NUM_LOOPS ; ++i)   
        {  
            if ((i % SLEEP_EVERY_N) == 0)   
                Sleep(0);  
            nDynamic1[i] = omp_get_thread_num( );  
        }  
  
        #pragma omp for schedule(dynamic, DYNAMIC_CHUNK)  
        for (int i = 0 ; i < NUM_LOOPS ; ++i)   
        {  
            if ((i % SLEEP_EVERY_N) == 0)   
                Sleep(0);  
            nDynamicN[i] = omp_get_thread_num( );  
        }  
  
        #pragma omp for schedule(guided)  
        for (int i = 0 ; i < NUM_LOOPS ; ++i)   
        {  
            if ((i % SLEEP_EVERY_N) == 0)   
                Sleep(0);  
            nGuided[i] = omp_get_thread_num( );  
        }  
    }  
  
    printf_s("------------------------------------------------\n");  
    printf_s("| static | static | dynamic | dynamic | guided |\n");  
    printf_s("|    1   |    %d   |    1    |    %d    |        |\n",  
             STATIC_CHUNK, DYNAMIC_CHUNK);  
    printf_s("------------------------------------------------\n");  
  
    for (int i=0; i<NUM_LOOPS; ++i)   
    {  
        printf_s("|    %d   |    %d   |    %d    |    %d    |"  
                 "    %d   |\n",  
                 nStatic1[i], nStaticN[i],  
                 nDynamic1[i], nDynamicN[i], nGuided[i]);  
    }  
  
    printf_s("------------------------------------------------\n");  
}  
```  
  
  **\-\-\-\-\-\-\-\-\-\-\-\-\-\-\-\-\-\-\-\-\-\-\-\-\-\-\-\-\-\-\-\-\-\-\-\-\-\-\-\-\-\-\-\-\-\-\-\-**  
**&#124; 정적 &#124; 정적 &#124; 동적 &#124; 동적 &#124; 안내 &#124;**  
**&#124;    1   &#124;    5   &#124;    1    &#124;    5    &#124;        &#124;**  
**\-\-\-\-\-\-\-\-\-\-\-\-\-\-\-\-\-\-\-\-\-\-\-\-\-\-\-\-\-\-\-\-\-\-\-\-\-\-\-\-\-\-\-\-\-\-\-\-**  
**&#124;    0   &#124;    0   &#124;    0    &#124;    2    &#124;    1   &#124;**  
**&#124;    1   &#124;    0   &#124;    3    &#124;    2    &#124;    1   &#124;**  
**&#124;    2   &#124;    0   &#124;    3    &#124;    2    &#124;    1   &#124;**  
**&#124;    3   &#124;    0   &#124;    3    &#124;    2    &#124;    1   &#124;**  
**&#124;    0   &#124;    0   &#124;    2    &#124;    2    &#124;    1   &#124;**  
**&#124;    1   &#124;    1   &#124;    2    &#124;    3    &#124;    3   &#124;**  
**&#124;    2   &#124;    1   &#124;    2    &#124;    3    &#124;    3   &#124;**  
**&#124;    3   &#124;    1   &#124;    0    &#124;    3    &#124;    3   &#124;**  
**&#124;    0   &#124;    1   &#124;    0    &#124;    3    &#124;    3   &#124;**  
**&#124;    1   &#124;    1   &#124;    0    &#124;    3    &#124;    2   &#124;**  
**&#124;    2   &#124;    2   &#124;    1    &#124;    0    &#124;    2   &#124;**  
**&#124;    3   &#124;    2   &#124;    1    &#124;    0    &#124;    2   &#124;**  
**&#124;    0   &#124;    2   &#124;    1    &#124;    0    &#124;    3   &#124;**  
**&#124;    1   &#124;    2   &#124;    2    &#124;    0    &#124;    3   &#124;**  
**&#124;    2   &#124;    2   &#124;    2    &#124;    0    &#124;    0   &#124;**  
**&#124;    3   &#124;    3   &#124;    2    &#124;    1    &#124;    0   &#124;**  
**&#124;    0   &#124;    3   &#124;    3    &#124;    1    &#124;    1   &#124;**  
**&#124;    1   &#124;    3   &#124;    3    &#124;    1    &#124;    1   &#124;**  
**&#124;    2   &#124;    3   &#124;    3    &#124;    1    &#124;    1   &#124;**  
**&#124;    3   &#124;    3   &#124;    0    &#124;    1    &#124;    3   &#124;**  
**\-\-\-\-\-\-\-\-\-\-\-\-\-\-\-\-\-\-\-\-\-\-\-\-\-\-\-\-\-\-\-\-\-\-\-\-\-\-\-\-\-\-\-\-\-\-\-\-**   
## 참고 항목  
 [Clauses](../../../parallel/openmp/reference/openmp-clauses.md)