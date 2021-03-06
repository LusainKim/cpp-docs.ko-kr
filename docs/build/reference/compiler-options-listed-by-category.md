---
title: "컴파일러 옵션 범주별 목록 | Microsoft Docs"
ms.custom: 
ms.date: 11/04/2016
ms.reviewer: 
ms.suite: 
ms.technology: cpp-tools
ms.tgt_pltfrm: 
ms.topic: article
dev_langs: C++
helpviewer_keywords: compiler options, C++
ms.assetid: c4750dcf-dba0-4229-99b6-45cdecc11729
caps.latest.revision: "64"
author: corob-msft
ms.author: corob
manager: ghogen
ms.workload: cplusplus
ms.openlocfilehash: ec2b8f0f05da535fd6a4f212a08af847c997a860
ms.sourcegitcommit: 8fa8fdf0fbb4f57950f1e8f4f9b81b4d39ec7d7a
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 12/21/2017
---
# <a name="compiler-options-listed-by-category"></a>컴파일러 옵션 범주별 목록
이 문서에는 컴파일러 옵션의 범주별 목록이 포함되어 있습니다. 사전순으로 나열된 목록을 보려면 [Compiler Options Listed Alphabetically](../../build/reference/compiler-options-listed-alphabetically.md)을 참조하세요.  
  
### <a name="optimization"></a>최적화  
  
|옵션|용도|  
|------------|-------------|  
|[/O1](../../build/reference/o1-o2-minimize-size-maximize-speed.md)|작은 코드를 만듭니다.|  
|[/O2](../../build/reference/o1-o2-minimize-size-maximize-speed.md)|빠른 코드를 만듭니다.|  
|[/Ob](../../build/reference/ob-inline-function-expansion.md)|인라인 확장을 제어합니다.|  
|[/Od](../../build/reference/od-disable-debug.md)|최적화를 사용하지 않습니다.|  
|[/Og](../../build/reference/og-global-optimizations.md)|더 이상 사용되지 않습니다. 전역 최적화를 사용합니다.|  
|[/Oi](../../build/reference/oi-generate-intrinsic-functions.md)|내장 함수를 생성합니다.|  
|[/Os](../../build/reference/os-ot-favor-small-code-favor-fast-code.md)|코드 크기를 우선으로 합니다.|  
|[/Ot](../../build/reference/os-ot-favor-small-code-favor-fast-code.md)|코드 속도를 우선으로 합니다.|  
|[/Ox](../../build/reference/ox-full-optimization.md)|최대 최적화(/Ob1gity /Gs)를 사용합니다.|  
|[/Oy](../../build/reference/oy-frame-pointer-omission.md)|프레임 포인터를 생략합니다. (x86 전용)|  
|[/favor](../../build/reference/favor-optimize-for-architecture-specifics.md)|지정된 아키텍처나 아키텍처 범주에 최적화된 코드를 생성합니다.|  
  
### <a name="code-generation"></a>코드 생성  
  
|옵션|용도|  
|------------|-------------|  
|[/arch](../../build/reference/arch-x86.md)|코드 생성 시 SSE 또는 SSE2 명령을 사용합니다. (x86 전용)|  
|[/clr](../../build/reference/clr-common-language-runtime-compilation.md)|공용 언어 런타임에 실행할 출력 파일을 생성합니다.|  
|[/EH](../../build/reference/eh-exception-handling-model.md)|예외 처리 모델을 지정합니다.|  
|[/fp](../../build/reference/fp-specify-floating-point-behavior.md)|부동 소수점 동작을 지정합니다.|  
|[/GA](../../build/reference/ga-optimize-for-windows-application.md)|Windows 응용 프로그램에 맞게 최적화합니다.|  
|[/Gd](../../build/reference/gd-gr-gv-gz-calling-convention.md)|`__cdecl` 호출 규칙을 사용합니다(x86 (x86 전용)|  
|[/Ge](../../build/reference/ge-enable-stack-probes.md)|더 이상 사용되지 않습니다. 스택 프로브를 활성화합니다.|  
|[/GF](../../build/reference/gf-eliminate-duplicate-strings.md)|문자열 풀링을 사용합니다.|  
|[/Gh](../../build/reference/gh-enable-penter-hook-function.md)|후크 함수 `_penter`를 호출합니다.|  
|[/GH](../../build/reference/gh-enable-pexit-hook-function.md)|후크 함수 `_pexit`를 호출합니다.|  
|[/GL](../../build/reference/gl-whole-program-optimization.md)|전체 프로그램 최적화를 사용합니다.|  
|[/Gm](../../build/reference/gm-enable-minimal-rebuild.md)|최소 재빌드를 사용합니다.|  
|[/GR](../../build/reference/gr-enable-run-time-type-information.md)|RTTI(런타임 형식 정보)를 사용합니다.|  
|[/Gr](../../build/reference/gd-gr-gv-gz-calling-convention.md)|`__fastcall` 호출 규칙을 사용합니다(x86 (x86 전용)|  
|[/GS](../../build/reference/gs-buffer-security-check.md)|버퍼 보안을 검사합니다.|  
|[/Gs](../../build/reference/gs-control-stack-checking-calls.md)|스택 프로브를 제어합니다.|  
|[/GT](../../build/reference/gt-support-fiber-safe-thread-local-storage.md)|정적 스레드 로컬 저장소를 사용하여 할당한 데이터의 파이버 안전을 지원합니다.|  
|[/guard:cf](../../build/reference/guard-enable-control-flow-guard.md)|제어 흐름 가드 보안 검사를 추가합니다.|  
|[/Gv](../../build/reference/gd-gr-gv-gz-calling-convention.md)|`__vectorcall` 호출 규칙을 사용합니다(x86 및 x64에만 해당).|  
|[/Gw](../../build/reference/gw-optimize-global-data.md)|전체 프로그램 전역 데이터 최적화를 사용하도록 설정합니다.|  
|[/GX](../../build/reference/gx-enable-exception-handling.md)|더 이상 사용되지 않습니다. 동기 예외 처리를 사용합니다. 대신 [/EH](../../build/reference/eh-exception-handling-model.md) 를 사용합니다.|  
|[/Gy](../../build/reference/gy-enable-function-level-linking.md)|함수 수준 링크를 사용합니다.|  
|[/GZ](../../build/reference/gz-enable-stack-frame-run-time-error-checking.md)|더 이상 사용되지 않습니다. 빠른 검사를 사용하도록 설정합니다. [/RTC1](../../build/reference/rtc-run-time-error-checks.md)과 동일합니다.|  
|[/Gz](../../build/reference/gd-gr-gv-gz-calling-convention.md)|`__stdcall` 호출 규칙을 사용합니다(x86 (x86 전용)|  
|[/homeparams](../../build/reference/homeparams-copy-register-parameters-to-stack.md)|레지스터에 전달된 매개 변수를 함수 시작 시 스택의 해당 위치에 기록합니다. 이 컴파일러 옵션은 [!INCLUDE[vcprx64](../../assembler/inline/includes/vcprx64_md.md)] 컴파일러(네이티브 및 크로스 컴파일)에만 사용됩니다.|  
|[/hotpatch](../../build/reference/hotpatch-create-hotpatchable-image.md)|핫 패치할 수 있는 이미지를 만듭니다.|  
|[/Qfast_transcendentals](../../build/reference/qfast-transcendentals-force-fast-transcendentals.md)|빠른 초월수를 생성합니다.|  
|[QIfist](../../build/reference/qifist-suppress-ftol.md)|더 이상 사용되지 않습니다. 부동 소수점 형식에서 정수 계열 형식으로 변환해야 할 때 도우미 함수 `_ftol` 이 호출되지 않도록 합니다. (x86 전용)|  
|[/Qimprecise_fwaits](../../build/reference/qimprecise-fwaits-remove-fwaits-inside-try-blocks.md)|`fwait` 블록 내에 있는 `try` 명령을 제거합니다.|  
|[/Qpar](../../build/reference/qpar-auto-parallelizer.md)|루프 자동 병렬화를 사용하도록 설정합니다.|  
|[/Qpar-report](../../build/reference/qpar-report-auto-parallelizer-reporting-level.md)|자동 병렬화에 대한 보고 수준을 사용하도록 설정합니다.|  
|[/Qsafe_fp_loads](../../build/reference/qsafe-fp-loads.md)|부동 소수점 값에 대한 정수 이동 명령을 사용하고 특정 부동 소수점 부하 최적화를 사용하지 않도록 설정합니다.|  
|[/Qvec-report (자동 벡터화 도우미 보고 수준)](../../build/reference/qvec-report-auto-vectorizer-reporting-level.md)|자동 벡터화에 대한 보고 수준을 사용하도록 설정합니다.|  
|[/RTC](../../build/reference/rtc-run-time-error-checks.md)|런타임 오류 검사를 사용합니다.|  
|[/volatile](../../build/reference/volatile-volatile-keyword-interpretation.md)|volatile 키워드가 해석되는 방식을 선택합니다.|  
  
### <a name="output-files"></a>출력 파일  
  
|옵션|용도|  
|------------|-------------|  
|[/doc](../../build/reference/doc-process-documentation-comments-c-cpp.md)|XML 파일에 대해 문서 주석을 처리합니다.|  
|[/FA](../../build/reference/fa-fa-listing-file.md)|어셈블리 목록 파일을 구성합니다.|  
|[/Fa](../../build/reference/fa-fa-listing-file.md)|어셈블리 목록 파일을 만듭니다.|  
|[/Fd](../../build/reference/fd-program-database-file-name.md)|프로그램 데이터베이스 파일 이름을 바꿉니다.|  
|[/Fe](../../build/reference/fe-name-exe-file.md)|실행 파일 이름을 바꿉니다.|  
|[/Fi](../../build/reference/fi-preprocess-output-file-name.md)|전처리된 출력 파일 이름을 지정합니다.|  
|[/Fm](../../build/reference/fm-name-mapfile.md)|맵 파일을 만듭니다.|  
|[/Fo](../../build/reference/fo-object-file-name.md)|개체 파일을 만듭니다.|  
|[/Fp](../../build/reference/fp-name-dot-pch-file.md)|미리 컴파일된 헤더 파일 이름을 지정합니다.|  
|[/FR](../../build/reference/fr-fr-create-dot-sbr-file.md) [/Fr](../../build/reference/fr-fr-create-dot-sbr-file.md)|브라우저 파일을 생성합니다.|  
  
### <a name="preprocessor"></a>전처리기  
  
|옵션|용도|  
|------------|-------------|  
|[/AI](../../build/reference/ai-specify-metadata-directories.md)|[#using](../../preprocessor/hash-using-directive-cpp.md) 지시문에 전달된 파일 참조를 확인하기 위해 검색할 디렉터리를 지정합니다.|  
|[/C](../../build/reference/c-preserve-comments-during-preprocessing.md)|전처리하는 동안 주석을 유지합니다.|  
|[/D](../../build/reference/d-preprocessor-definitions.md)|상수와 매크로를 정의합니다.|  
|[/E](../../build/reference/e-preprocess-to-stdout.md)|전처리기 출력을 표준 출력에 복사합니다.|  
|[/EP](../../build/reference/ep-preprocess-to-stdout-without-hash-line-directives.md)|전처리기 출력을 표준 출력에 복사합니다.|  
|[/FI](../../build/reference/fi-name-forced-include-file.md)|지정된 포함 파일을 전처리합니다.|  
|[/FU](../../build/reference/fu-name-forced-hash-using-file.md)|파일 이름을 [#using](../../preprocessor/hash-using-directive-cpp.md) 지시문에 전달된 것처럼 강제 사용합니다.|  
|[/Fx](../../build/reference/fx-merge-injected-code.md)|삽입된 코드와 소스 파일을 병합합니다.|  
|[/I](../../build/reference/i-additional-include-directories.md)|포함 파일의 디렉터리를 검색합니다.|  
|[/P](../../build/reference/p-preprocess-to-a-file.md)|전처리기 출력을 파일에 씁니다.|  
|[/U](../../build/reference/u-u-undefine-symbols.md)|미리 정의된 매크로를 제거합니다.|  
|[/u](../../build/reference/u-u-undefine-symbols.md)|미리 정의된 모든 매크로를 제거합니다.|  
|[/X](../../build/reference/x-ignore-standard-include-paths.md)|표준 포함 디렉터리를 무시합니다.|  
  
### <a name="language"></a>언어  
  
|옵션|용도|  
|------------|-------------|  
|[/constexpr](constexpr-control-constexpr-evaluation.md)|컴파일 타임에 constexpr 평가 제어 합니다.|  
|[/openmp](../../build/reference/openmp-enable-openmp-2-0-support.md)|소스 코드에서 [#pragma omp](../../preprocessor/omp.md) 를 활성화합니다.|  
|[/vd](../../build/reference/vd-disable-construction-displacements.md)|숨겨진 `vtordisp` 클래스 멤버를 사용하도록 설정하거나 표시하지 않습니다.|  
|[/vmb](../../build/reference/vmb-vmg-representation-method.md)|멤버의 포인터에 best case를 사용합니다.|  
|[/vmg](../../build/reference/vmb-vmg-representation-method.md)|멤버의 포인터에 full generality를 사용합니다.|  
|[/vmm](../../build/reference/vmm-vms-vmv-general-purpose-representation.md)|다중 상속을 선언합니다.|  
|[/vms](../../build/reference/vmm-vms-vmv-general-purpose-representation.md)|단일 상속을 선언합니다.|  
|[/vmv](../../build/reference/vmm-vms-vmv-general-purpose-representation.md)|가상 상속을 선언합니다.|  
|[/Z7](../../build/reference/z7-zi-zi-debug-information-format.md)|C 7.0 호환 디버깅 정보를 생성 합니다.|  
|[/Za](../../build/reference/za-ze-disable-language-extensions.md)|언어 확장을 사용하지 않습니다.|  
|[/Zc](../../build/reference/zc-conformance.md)|[/Ze](../../build/reference/za-ze-disable-language-extensions.md)에서 표준 동작을 지정합니다.|  
|[/Ze](../../build/reference/za-ze-disable-language-extensions.md)|더 이상 사용되지 않습니다. 언어 확장을 사용합니다.|  
|[/ZI](../../build/reference/z7-zi-zi-debug-information-format.md)|편집하며 계속하기와 호환되는 프로그램 데이터베이스에 디버깅 정보를 포함합니다. (x86 전용)|  
|[/Zi](../../build/reference/z7-zi-zi-debug-information-format.md)|완전한 디버깅 정보를 생성합니다.|  
|[/Zl](../../build/reference/zl-omit-default-library-name.md)|.obj 파일에서 기본 라이브러리 이름을 제거합니다.|  
|[/Zp](../../build/reference/zp-struct-member-alignment.md) *n*|구조체 멤버를 압축합니다.|  
|[/Zs](../../build/reference/zs-syntax-check-only.md)|구문만 확인합니다.|  
|[/ZW](../../build/reference/zw-windows-runtime-compilation.md)|Windows Runtime에서 실행할 출력 파일을 생성 합니다.|  
  
### <a name="linking"></a>연결  
  
|옵션|용도|  
|------------|-------------|  
|[/F](../../build/reference/f-set-stack-size.md)|스택 크기를 설정합니다.|  
|[/LD](../../build/reference/md-mt-ld-use-run-time-library.md)|DLL(동적 연결 라이브러리)을 만듭니다.|  
|[/LDd](../../build/reference/md-mt-ld-use-run-time-library.md)|디버그 DLL(동적 연결 라이브러리)을 만듭니다.|  
|[/link](../../build/reference/link-pass-options-to-linker.md)|지정된 옵션을 LINK에 전달합니다.|  
|[/LN](../../build/reference/ln-create-msil-module.md)|MSIL 모듈을 만듭니다.|  
|[/MD](../../build/reference/md-mt-ld-use-run-time-library.md)|MSVCRT.lib을 사용하여 컴파일함으로써 다중 스레드 DLL을 만듭니다.|  
|[/MDd](../../build/reference/md-mt-ld-use-run-time-library.md)|MSVCRTD.lib로 컴파일하여 디버그 다중 스레드 DLL을 만듭니다.|  
|[/MT](../../build/reference/md-mt-ld-use-run-time-library.md)|LIBCMT.lib를 사용하여 컴파일함으로써 다중 스레드 실행 파일을 만듭니다.|  
|[/MTd](../../build/reference/md-mt-ld-use-run-time-library.md)|LIBCMTD.lib를 사용하여 컴파일함으로써 디버그 다중 스레드 실행 파일을 만듭니다.|  
  
### <a name="miscellaneous"></a>기타  
  
|옵션|용도|  
|------------|-------------|  
|[/?](../../build/reference/help-compiler-command-line-help.md)|컴파일러 옵션을 나열합니다.|  
|[@](../../build/reference/at-specify-a-compiler-response-file.md)|지시 파일을 지정합니다.|  
|[/analyze](../../build/reference/analyze-code-analysis.md)|코드 분석을 활성화합니다.|  
|[/bigobj](../../build/reference/bigobj-increase-number-of-sections-in-dot-obj-file.md)|.obj 파일에서 주소 지정 가능한 섹션의 수를 늘립니다.|  
|[/c](../../build/reference/c-compile-without-linking.md)|링크하지 않고 컴파일합니다.|  
|[/cgthreads](../../build/reference/cgthreads-code-generation-threads.md)|최적화 및 코드 생성에 사용할 cl.exe 스레드 수를 지정합니다.|  
|[/errorReport](../../build/reference/errorreport-report-internal-compiler-errors.md)|ICE(내부 컴파일러 오류) 정보를 Visual C++ 팀에 직접 제공할 수 있도록 합니다.|  
|[/FC](../../build/reference/fc-full-path-of-source-code-file-in-diagnostics.md)|진단 텍스트에서 cl.exe에 전달된 소스 코드 파일의 전체 경로를 표시합니다.|  
|[/FS](../../build/reference/fs-force-synchronous-pdb-writes.md)|MSPDBSRV.EXE를 통해 serialize될 프로그램 데이터베이스(PDB) 파일에 강제로 씁니다.|  
|[/H](../../build/reference/h-restrict-length-of-external-names.md)|더 이상 사용되지 않습니다. 외부 공개 이름의 길이를 제한합니다.|  
|[/HELP](../../build/reference/help-compiler-command-line-help.md)|컴파일러 옵션을 나열합니다.|  
|[/J](../../build/reference/j-default-char-type-is-unsigned.md)|기본 `char` 형식을 변경합니다.|  
|[/kernel](../../build/reference/kernel-create-kernel-mode-binary.md)|컴파일러와 링커는 Windows 커널에서 실행할 수 있는 이진 파일을 만듭니다.|  
|[/MP](../../build/reference/mp-build-with-multiple-processes.md)|여러 개의 소스 파일을 동시에 빌드합니다.|  
|[/nologo](../../build/reference/nologo-suppress-startup-banner-c-cpp.md)|초기 화면 배너를 표시하지 않습니다.|  
|[/sdl](../../build/reference/sdl-enable-additional-security-checks.md)|추가 보안 기능 및 경고를 사용하도록 설정합니다.|  
|[/showIncludes](../../build/reference/showincludes-list-include-files.md)|컴파일하는 동안 전체 포함 파일의 목록을 표시합니다.|  
|[/Tc](../../build/reference/tc-tp-tc-tp-specify-source-file-type.md)|C 소스 파일을 지정합니다.|  
|[/TC](../../build/reference/tc-tp-tc-tp-specify-source-file-type.md)|3. 모든 소스 파일 지정|  
|[/Tp](../../build/reference/tc-tp-tc-tp-specify-source-file-type.md)|C++ 소스 파일을 지정합니다.|  
|[/TP](../../build/reference/tc-tp-tc-tp-specify-source-file-type.md)|모든 소스 파일은 c + +를 지정 합니다.|  
|[/V](../../build/reference/v-version-number.md)|더 이상 사용되지 않습니다. 버전 문자열을 설정합니다.|  
|[/w](../../build/reference/compiler-option-warning-level.md)|모든 경고를 사용하지 않습니다.|  
|[/W0, /W1, /W2, /W3, /W4](../../build/reference/compiler-option-warning-level.md)|출력 경고 수준을 설정합니다.|  
|[/w1, /w2, /w3, /w4](../../build/reference/compiler-option-warning-level.md)|지정된 경고에 대한 경고 수준을 설정합니다.|  
|[/Wall](../../build/reference/compiler-option-warning-level.md)|기본적으로 비활성화되는 경고를 포함하여 모든 경고를 활성화합니다.|  
|[/wd](../../build/reference/compiler-option-warning-level.md)|지정된 경고를 사용하지 않습니다.|  
|[/we](../../build/reference/compiler-option-warning-level.md)|지정된 경고를 오류로 처리합니다.|  
|[/WL](../../build/reference/wl-enable-one-line-diagnostics.md)|명령줄에서 C++ 소스 코드를 컴파일할 때 오류 및 경고 메시지에 한 줄 진단을 사용합니다.|  
|[/wo](../../build/reference/compiler-option-warning-level.md)|지정된 경고를 한 번만 표시합니다.|  
|[/Wv](../../build/reference/compiler-option-warning-level.md)|이후 버전의 컴파일러에서 도입된 경고를 사용하지 않습니다.|  
|[/WX](../../build/reference/compiler-option-warning-level.md)|경고를 오류로 처리합니다.|  
|[/Yc](../../build/reference/yc-create-precompiled-header-file.md)|만듭니다. PCH 파일입니다.|  
|[/Yd](../../build/reference/yd-place-debug-information-in-object-file.md)|더 이상 사용되지 않습니다. 모든 개체 파일에 완전한 디버깅 정보를 저장합니다. 대신 [/Zi](../../build/reference/z7-zi-zi-debug-information-format.md) 를 사용합니다.|  
|[/Yl](../../build/reference/yl-inject-pch-reference-for-debug-library.md)|디버그 라이브러리를 만들 때 PCH 참조를 삽입합니다.|  
|[/Yu](../../build/reference/yu-use-precompiled-header-file.md)|빌드하는 동안 미리 컴파일된 헤더 파일을 사용합니다.|  
|[/Y-](../../build/reference/y-ignore-precompiled-header-options.md)|현재 빌드에서 미리 컴파일된 다른 모든 헤더 컴파일러 옵션을 무시합니다.|  
|[/Zm](../../build/reference/zm-specify-precompiled-header-memory-allocation-limit.md)|미리 컴파일된 헤더 메모리의 할당 제한을 지정합니다.|  
|[await /](await-enable-coroutine-support.md)|코 루틴 (다시 시작 가능한 함수) 확장을 사용 합니다.|  
|[/source-charset](source-charset-set-source-character-set.md)|소스 문자 집합을 설정 합니다.|
|[/execution-charset](execution-charset-set-execution-character-set.md)|실행 문자 집합을 설정 합니다.|
|[/utf-8](utf-8-set-source-and-executable-character-sets-to-utf-8.md)|소스 및 실행 문자 집합을 u t F-8로 설정합니다.|
|[/validate-charset](validate-charset-validate-for-compatible-characters.md)|호환 문자만 대 한 utf-8 파일의 유효성을 검사 합니다.|
|[/diagnostics](diagnostics-compiler-diagnostic-options.md)|진단 메시지의 형식을 제어합니다.|
|[관대 한 /-](permissive-standards-conformance.md)|표준 준수 모드를 설정 합니다.|
|[/std](std-specify-language-standard-version.md)|C + + 표준 버전 호환성 선택기입니다.|
  
### <a name="deprecated-and-removed-compiler-options"></a>사용되지 않는 컴파일러 옵션  
  
|옵션|용도|  
|------------|-------------|  
|[/clr:noAssembly](../../build/reference/clr-common-language-runtime-compilation.md)|더 이상 사용되지 않습니다. 대신 [/LN (Create MSIL Module)](../../build/reference/ln-create-msil-module.md) 를 사용하세요.|  
|[/Fr](../../build/reference/fr-fr-create-dot-sbr-file.md)|더 이상 사용되지 않습니다. 지역 변수 없이 찾아보기 정보 파일을 만듭니다.|  
|[/Ge](../../build/reference/ge-enable-stack-probes.md)|더 이상 사용되지 않습니다. 스택 프로브를 활성화합니다. 기본적으로 설정되어 있습니다.|  
|[/GX](../../build/reference/gx-enable-exception-handling.md)|더 이상 사용되지 않습니다. 동기 예외 처리를 사용합니다. 대신 [/EH](../../build/reference/eh-exception-handling-model.md) 를 사용합니다.|  
|[/GZ](../../build/reference/gz-enable-stack-frame-run-time-error-checking.md)|더 이상 사용되지 않습니다. 빠른 검사를 사용하도록 설정합니다. 대신 [/RTC1](../../build/reference/rtc-run-time-error-checks.md) 을 사용합니다.|  
|[/H](../../build/reference/h-restrict-length-of-external-names.md)|더 이상 사용되지 않습니다. 외부 공개 이름의 길이를 제한합니다.|  
|[/Og](../../build/reference/og-global-optimizations.md)|더 이상 사용되지 않습니다. 전역 최적화를 사용합니다.|  
|[QIfist](../../build/reference/qifist-suppress-ftol.md)|더 이상 사용되지 않습니다. 부동 소수점 형식에서 정수 계열 형식으로 변환하는 방법을 지정하는 데 사용되었습니다.|  
|[/V](../../build/reference/v-version-number.md)|더 이상 사용되지 않습니다. .obj 파일 버전 문자열을 설정합니다.|  
|[/Wp64](../../build/reference/wp64-detect-64-bit-portability-issues.md)|사용되지 않습니다. 64비트 이식성 문제를 검색합니다.|  
|[/Yd](../../build/reference/yd-place-debug-information-in-object-file.md)|더 이상 사용되지 않습니다. 모든 개체 파일에 완전한 디버깅 정보를 저장합니다. 대신 [/Zi](../../build/reference/z7-zi-zi-debug-information-format.md) 를 사용합니다.|  
|[/Zc:forScope-](../../build/reference/zc-forscope-force-conformance-in-for-loop-scope.md)|더 이상 사용되지 않습니다. for 루프 범위의 규칙을 사용하지 않도록 설정합니다.|  
|[/Ze](../../build/reference/za-ze-disable-language-extensions.md)|더 이상 사용되지 않습니다. 언어 확장을 사용합니다.|  
|[/Zg](../../build/reference/zg-generate-function-prototypes.md)|Visual C++ 2015에서 제거되었습니다. 함수 프로토타입을 생성합니다.|  
  
## <a name="see-also"></a>참고 항목  
 [C/C++ 빌드 참조](../../build/reference/c-cpp-building-reference.md)   
 [컴파일러 옵션](../../build/reference/compiler-options.md)   
 [컴파일러 옵션 설정](../../build/reference/setting-compiler-options.md)