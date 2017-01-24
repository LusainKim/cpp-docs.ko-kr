---
title: "&lt;filesystem&gt; 함수 | Microsoft Docs"
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
  - "FILESYSTEM/std::experimental::filesystem::v1::absolute"
  - "std::experimental::filesystem::v1::absolute"
  - "FILESYSTEM/std::experimental::filesystem::v1::canonical"
  - "std::experimental::filesystem::v1::canonical"
  - "FILESYSTEM/std::experimental::filesystem::v1::copy"
  - "std::experimental::filesystem::v1::copy"
  - "FILESYSTEM/std::experimental::filesystem::v1::copy_file"
  - "std::experimental::filesystem::v1::copy_file"
  - "FILESYSTEM/std::experimental::filesystem::v1::copy_symlink"
  - "std::experimental::filesystem::v1::copy_symlink"
  - "FILESYSTEM/std::experimental::filesystem::v1::create_directories"
  - "std::experimental::filesystem::v1::create_directories"
  - "FILESYSTEM/std::experimental::filesystem::v1::create_directory"
  - "std::experimental::filesystem::v1::create_directory"
  - "FILESYSTEM/std::experimental::filesystem::v1::create_directory_symlink"
  - "std::experimental::filesystem::v1::create_directory_symlink"
  - "FILESYSTEM/std::experimental::filesystem::v1::create_hard_link"
  - "std::experimental::filesystem::v1::create_hard_link"
  - "FILESYSTEM/std::experimental::filesystem::v1::create_symlink"
  - "std::experimental::filesystem::v1::create_symlink"
  - "FILESYSTEM/std::experimental::filesystem::v1::current_path"
  - "std::experimental::filesystem::v1::current_path"
  - "FILESYSTEM/std::experimental::filesystem::v1::equivalent"
  - "std::experimental::filesystem::v1::equivalent"
  - "FILESYSTEM/std::experimental::filesystem::v1::exists"
  - "std::experimental::filesystem::v1::exists"
  - "FILESYSTEM/std::experimental::filesystem::v1::file_size"
  - "std::experimental::filesystem::v1::file_size"
  - "FILESYSTEM/std::experimental::filesystem::v1::hard_link_count"
  - "std::experimental::filesystem::v1::hard_link_count"
  - "FILESYSTEM/std::experimental::filesystem::v1::hash_value"
  - "std::experimental::filesystem::v1::hash_value"
  - "FILESYSTEM/std::experimental::filesystem::v1::is_block_file"
  - "std::experimental::filesystem::v1::is_block_file"
  - "FILESYSTEM/std::experimental::filesystem::v1::is_character_file"
  - "std::experimental::filesystem::v1::is_character_file"
  - "FILESYSTEM/std::experimental::filesystem::v1::is_directory"
  - "std::experimental::filesystem::v1::is_directory"
  - "FILESYSTEM/std::experimental::filesystem::v1::is_empty"
  - "std::experimental::filesystem::v1::is_empty"
  - "FILESYSTEM/std::experimental::filesystem::v1::is_fifo"
  - "std::experimental::filesystem::v1::is_fifo"
  - "FILESYSTEM/std::experimental::filesystem::v1::is_other"
  - "std::experimental::filesystem::v1::is_other"
  - "FILESYSTEM/std::experimental::filesystem::v1::is_regular_file"
  - "std::experimental::filesystem::v1::is_regular_file"
  - "FILESYSTEM/std::experimental::filesystem::v1::is_socket"
  - "std::experimental::filesystem::v1::is_socket"
  - "FILESYSTEM/std::experimental::filesystem::v1::is_symlink"
  - "std::experimental::filesystem::v1::is_symlink"
  - "FILESYSTEM/std::experimental::filesystem::v1::last_write_time"
  - "std::experimental::filesystem::v1::last_write_time"
  - "FILESYSTEM/std::experimental::filesystem::v1::permissions"
  - "std::experimental::filesystem::v1::permissions"
  - "FILESYSTEM/std::experimental::filesystem::v1::read_symlink"
  - "std::experimental::filesystem::v1::read_symlink"
  - "FILESYSTEM/std::experimental::filesystem::v1::remove"
  - "std::experimental::filesystem::v1::remove"
  - "FILESYSTEM/std::experimental::filesystem::v1::remove_all"
  - "std::experimental::filesystem::v1::remove_all"
  - "FILESYSTEM/std::experimental::filesystem::v1::rename"
  - "std::experimental::filesystem::v1::rename"
  - "FILESYSTEM/std::experimental::filesystem::v1::resize_file"
  - "std::experimental::filesystem::v1::resize_file"
  - "FILESYSTEM/std::experimental::filesystem::v1::space"
  - "std::experimental::filesystem::v1::space"
  - "FILESYSTEM/std::experimental::filesystem::v1::status"
  - "std::experimental::filesystem::v1::status"
  - "FILESYSTEM/std::experimental::filesystem::v1::status_known"
  - "std::experimental::filesystem::v1::status_known"
  - "FILESYSTEM/std::experimental::filesystem::v1::swap"
  - "std::experimental::filesystem::v1::swap"
  - "FILESYSTEM/std::experimental::filesystem::v1::symlink_status"
  - "std::experimental::filesystem::v1::symlink_status"
  - "FILESYSTEM/std::experimental::filesystem::v1::system_complete"
  - "std::experimental::filesystem::v1::system_complete"
  - "FILESYSTEM/std::experimental::filesystem::v1::temp_directory_path"
  - "std::experimental::filesystem::v1::temp_directory_path"
  - "FILESYSTEM/std::experimental::filesystem::v1::u8path"
  - "std::experimental::filesystem::v1::u8path"
dev_langs: 
  - "C++"
ms.assetid: be3cb821-4728-4d47-ab78-858fa8aa5045
caps.latest.revision: 13
caps.handback.revision: 4
author: "corob-msft"
ms.author: "corob"
manager: "ghogen"
---
# &lt;filesystem&gt; 함수
[!INCLUDE[vs2017banner](../assembler/inline/includes/vs2017banner.md)]

[\<filesystem\>](../standard-library/filesystem.md) 헤더의 이러한 사용 가능한 함수는 경로, 파일, symlink, 디렉터리 및 볼륨에서 수정 및 쿼리 작업을 수행합니다. 자세한 내용 및 코드 예제를 보려면 [파일 시스템 탐색\(C\+\+\)](../standard-library/file-system-navigation.md)를 참조하세요.  
  
## absolute  
  
```  
path absolute(const path& pval, const path& base = current_path());  
  
```  
  
 이 함수는 경로 이름 기준에 상대적인 pval에 해당하는 절대 경로 이름을 반환합니다.  
  
1.  pval.has\_root\_name\(\) && pval.has\_root\_directory\(\)인 경우 함수는 pval을 반환합니다.  
  
2.  pval.has\_root\_name\(\) && \!pval.has\_root\_directory\(\)인 경우 함수는 pval.root\_name\(\) \/ absolute\(base\).root\_directory\(\) \/ absolute\(base\).relative\_path\(\) \/ pval.relative\_path\(\)를 반환합니다.  
  
3.  \!pval.has\_root\_name\(\) && pval.has\_root\_directory\(\)인 경우 함수는 absolute\(base\).root\_name\(\) \/ pval을 반환합니다.  
  
4.  \!pval.has\_root\_name\(\) && \!pval.has\_root\_directory\(\)인 경우 함수는 absolute\(base\) \/ pval을 반환합니다.  
  
5.  
  
## begin  
  
```  
const directory_iterator& begin(const directory_iterator& iter) noexcept;  
const recursive_directory_iterator&  
    begin(const recursive_directory_iterator& iter) noexcept;  
  
```  
  
 두 함수 모두 iter를 반환합니다.  
  
## canonical  
  
```  
path canonical(const path& pval, const path& base = current_path());  
path canonical(const path& pval,  
    error_code& ec);  
path canonical(const path& pval, const path& base,  
    error_code& ec);  
```  
  
 모든 함수에서 절대 경로 이름 pabs \= absolute\(pval, base\)\(또는 기준 매개 변수가 없는 오버로드의 경우 pabs \= absolute\(pval\)\)를 구성한 후 다음 순서에 따라 정규 형식으로 줄입니다.  
  
1.  is\_symlink\(X\)가 true인 모든 경로 구성 요소 X가 read\_symlink\(X\)로 대체됩니다.  
  
2.  모든 경로 구성 요소 . \(점은 이전 경로 구성 요소에서 설정한 현재 디렉터리임\)이 제거됩니다.  
  
3.  모든 경로 구성 요소 X\/.. 쌍 \(점\-점은 이전 경로 구성 요소에서 설정한 부모 디렉터리임\)이 제거됩니다.  
  
 그런 다음 함수는 pabs를 반환합니다.  
  
## copy  
  
```  
void copy(const path& from, const path& to);  
void copy(const path& from, const path& to,  
    error_code& ec) noexcept;  
void copy(const path& from, const path& to, copy_options opts);  
void copy(const path& from, const path& to, copy_options opts,  
    error_code& ec) noexcept;  
```  
  
 모든 함수는 opts가 제어하는 from과 to 사이에서 하나 이상의 파일을 복사하거나 연결할 수 있으며, opts 매개 변수가 없는 오버로드의 경우에는 copy\_options::none으로 간주됩니다. opts에는 다음 중 하나만 포함되어야 합니다.  
  
-   skip\_existing, overwrite\_existing 또는 update\_existing  
  
-   copy\_symlinks 또는 skip\_symlinks  
  
-   directories\_only, create\_symlinks 또는 create\_hard\_links  
  
 함수는 먼저 다음과 같이 file\_status 값을 from에 대해서는 f를, to에 대해서는 t를 결정합니다.  
  
-   opts & \(copy\_options::create\_symlinks &#124; copy\_options::skip\_symlinks\)이면 symlink\_status를 호출합니다.  
  
-   그렇지 않으면 status를 호출합니다.  
  
-   그렇지 않으면 오류를 보고합니다.  
  
 \!exists\(f\) &#124;&#124; equivalent\(f, t\) &#124;&#124; is\_other\(f\) &#124;&#124; is\_other\(t\) &#124;&#124; is\_directory\(f\)&& is\_regular\_file\(t\)이면 오류를 보고하고 그 외에는 아무 작업도 수행하지 않습니다.  
  
 그렇지 않고 is\_symlink\(f\)이면 다음과 같습니다.  
  
-   options & copy\_options::skip\_symlinks이면 아무 작업도 수행하지 않습니다.  
  
-   그렇지 않고 \!exists\(t\)&& options & copy\_options::copy\_symlinks이면 copy\_symlink\(from, to, opts\)입니다.  
  
-   그렇지 않으면 오류를 보고합니다.  
  
 그렇지 않고 is\_regular\_file\(f\)이면 다음과 같습니다.  
  
-   opts & copy\_options::directories\_only이면 아무 작업도 수행하지 않습니다.  
  
-   그렇지 않고 opts & copy\_options::create\_symlinks이면 create\_symlink\(to, from\)입니다.  
  
-   그렇지 않고 opts & copy\_options::create\_hard\_links이면 create\_hard\_link\(to, from\)입니다.  
  
-   그렇지 않고 is\_directory\(f\)이면 copy\_file\(from, to \/ from.filename\(\), opts\)입니다.  
  
-   그렇지 않으면 copy\_file\(from, to, opts\)입니다.  
  
 그렇지 않고 is\_directory\(f\) && \(opts & copy\_options::recursive &#124;&#124; \!opts\)이면 다음과 같습니다.  
  
-   ```  
    if (!exists(t))  
        {  // copy directory contents recursively  
        create_directory(to, from, ec);  
        for (directory_iterator next(from), end;  
            ec == error_code() && next != end; ++next)  
            copy(next->path(),  
                to / next->path().filename(), opts, ec);  
        }  
<CodeContentPlaceHolder>4</CodeContentPlaceHolder>bool copy_file(const path& from, const path& to);  
bool copy_file(const path& from, const path& to,  
    error_code& ec) noexcept;  
bool copy_file(const path& from, const path& to, copy_options opts);  
bool copy_file(const path& from, const path& to, copy_options opts,  
    error_code& ec) noexcept;  
<CodeContentPlaceHolder>5</CodeContentPlaceHolder>void copy_symlink(const path& from, const path& to);  
void copy_symlink(const path& from, const path& to,  
    error_code& ec) noexcept;  
<CodeContentPlaceHolder>6</CodeContentPlaceHolder>bool create_directories(const path& pval);  
bool create_directories(const path& pval,  
    error_code& ec) noexcept;  
<CodeContentPlaceHolder>7</CodeContentPlaceHolder>bool create_directory(const path& pval);  
bool create_directory(const path& pval,  
    error_code& ec) noexcept;  
bool create_directory(const path& pval, const path& attr);  
bool create_directory(const path& pval, const path& attr,  
    error_code& ec) noexcept;  
<CodeContentPlaceHolder>8</CodeContentPlaceHolder>void create_directory_symlink(const path& to, const path& link);  
void create_directory_symlink(const path& to, const path& link),  
    error_code& ec) noexcept;  
<CodeContentPlaceHolder>9</CodeContentPlaceHolder>void create_hard_link(const path& to, const path& link);  
void create_hard_link(const path& to, const path& link),  
    error_code& ec) noexcept;  
<CodeContentPlaceHolder>10</CodeContentPlaceHolder>void create_symlink(const path& to, const path& link);  
void create_symlink(const path& to, const path& link),  
    error_code& ec) noexcept;  
<CodeContentPlaceHolder>11</CodeContentPlaceHolder>path current_path();  
path current_path(  
    error_code& ec);  
void current_path(const path& pval);  
void current_path(const path& pval,  
    error_code& ec) noexcept;  
<CodeContentPlaceHolder>12</CodeContentPlaceHolder>directory_iterator& end(const directory_iterator& iter) noexcept;  
recursive_directory_iterator&  
    end(const recursive_directory_iterator& iter) noexcept;  
<CodeContentPlaceHolder>13</CodeContentPlaceHolder>bool equivalent(const path& left, const path& right);  
bool equivalent(const path& left, const path& right,  
    error_code& ec) noexcept;  
<CodeContentPlaceHolder>14</CodeContentPlaceHolder>bool exists(file_status stat) noexcept;  
bool exists(const path& pval);  
bool exists(const path& pval,  
    error_code& ec) noexcept;  
<CodeContentPlaceHolder>15</CodeContentPlaceHolder>uintmax_t file_size(const path& pval);  
uintmax_t file_size(const path& pval,  
    error_code& ec) noexcept;  
<CodeContentPlaceHolder>16</CodeContentPlaceHolder>uintmax_t hard_link_count(const path& pval);  
uintmax_t hard_link_count(const path& pval,  
    error_code& ec) noexcept;  
<CodeContentPlaceHolder>17</CodeContentPlaceHolder>size_t hash_value(const path& pval) noexcept;  
<CodeContentPlaceHolder>18</CodeContentPlaceHolder>bool is_block_file(file_status stat) noexcept;  
bool is_block_file(const path& pval);  
bool is_block_file(const path& pval,  
    error_code& ec) noexcept;  
  
<CodeContentPlaceHolder>19</CodeContentPlaceHolder>  
bool is_character_file(file_status stat) noexcept;  
bool is_character_file(const path& pval);  
bool is_character_file(const path& pval,  
    error_code& ec) noexcept;  
  
<CodeContentPlaceHolder>20</CodeContentPlaceHolder>  
bool is_directory(file_status stat) noexcept;  
bool is_directory(const path& pval);  
bool is_directory(const path& pval,  
    error_code& ec) noexcept;  
  
<CodeContentPlaceHolder>21</CodeContentPlaceHolder>  
bool is_empty(file_status stat) noexcept;  
bool is_empty(const path& pval);  
bool is_empty(const path& pval,  
    error_code& ec) noexcept;  
  
<CodeContentPlaceHolder>22</CodeContentPlaceHolder>bool is_fifo(file_status stat) noexcept;  
bool is_fifo(const path& pval);  
bool is_fifo(const path& pval,  
    error_code& ec) noexcept;  
  
<CodeContentPlaceHolder>23</CodeContentPlaceHolder>bool is_other(file_status stat) noexcept;  
bool is_other(const path& pval);  
bool is_other(const path& pval,  
    error_code& ec) noexcept;  
  
<CodeContentPlaceHolder>24</CodeContentPlaceHolder>  
bool is_regular_file(file_status stat) noexcept;  
bool is_regular_file(const path& pval);  
bool is_regular_file(const path& pval,  
    error_code& ec) noexcept;  
  
<CodeContentPlaceHolder>25</CodeContentPlaceHolder>  
bool is_socket(file_status stat) noexcept;  
bool is_socket(const path& pval);  
bool is_socket(const path& pval,  
    error_code& ec) noexcept;  
  
<CodeContentPlaceHolder>26</CodeContentPlaceHolder>  
bool is_symlink(file_status stat) noexcept;  
bool is_symlink(const path& pval);  
bool is_symlink(const path& pval,  
    error_code& ec) noexcept;  
  
<CodeContentPlaceHolder>27</CodeContentPlaceHolder>  
file_time_type last_write_time(const path& pval);  
file_time_type last_write_time(const path& pval,  
    error_code& ec) noexcept;  
void last_write_time(const path& pval, file_time_type new_time);  
void last_write_time(const path& pval, file_time_type new_time,  
    error_code& ec) noexcept;  
  
<CodeContentPlaceHolder>28</CodeContentPlaceHolder>void permissions(const path& pval, perms mask);  
void permissions(const path& pval, perms mask,  
    error_code& ec) noexcept;  
  
<CodeContentPlaceHolder>29</CodeContentPlaceHolder>path read_symlink(const path& pval);  
path read_symlink(const path& pval.  
    error_code& ec);  
<CodeContentPlaceHolder>30</CodeContentPlaceHolder>bool remove(const path& pval);  
bool remove(const path& pval,  
    error_code& ec) noexcept;  
<CodeContentPlaceHolder>31</CodeContentPlaceHolder>uintmax_t remove_all(const path& pval);  
uintmax_t remove_all(const path& pval,  
    error_code& ec) noexcept;  
  
<CodeContentPlaceHolder>32</CodeContentPlaceHolder>void rename(const path& from, const path& to);  
void rename(const path& from, const path& to,  
    error_code& ec) noexcept;  
<CodeContentPlaceHolder>33</CodeContentPlaceHolder>void resize(const path& pval, uintmax_t size);  
void resize(const path& pval, uintmax_t size,  
    error_code& ec) noexcept;  
<CodeContentPlaceHolder>34</CodeContentPlaceHolder>space_info space(const path& pval);  
space_info space(const path& pval,  
    error_code& ec) noexcept;  
<CodeContentPlaceHolder>35</CodeContentPlaceHolder>file_status status(const path& pval);  
file_status status(const path& pval,  
    error_code& ec) noexcept;  
  
<CodeContentPlaceHolder>36</CodeContentPlaceHolder>bool status_known(file_status stat) noexcept;  
<CodeContentPlaceHolder>37</CodeContentPlaceHolder>void swap(path& left, path& right) noexcept;  
  
<CodeContentPlaceHolder>38</CodeContentPlaceHolder>file_status symlink_status(const path& pval);  
file_status symlink_status(const path& pval,  
    erroxr_code& ec) noexcept;  
  
<CodeContentPlaceHolder>39</CodeContentPlaceHolder>path system_complete(const path& pval);  
path system_complete(const path& pval,  
    error_code& ec);  
  
<CodeContentPlaceHolder>40</CodeContentPlaceHolder>path temp_directory_path();  
path temp_directory_path(  
    error_code& ec);  
  
<CodeContentPlaceHolder>41</CodeContentPlaceHolder>template<class Source>  
    path u8path(const Source& source);  
template<class InIt>  
    path u8path(InIt first, InIt last);  
  
```  
  
 각각의 경우 파일 시스템에 관계없이 지정된 소스가 UTF\-8로 인코드된 char 요소의 시퀀스로 간주된다는 점을 제외하면 첫 번째 함수는 path\(source\)와 동일하게 작동하고 두 번째 함수는 path\(first, last\)와 동일하게 작동합니다.