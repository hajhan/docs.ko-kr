---
title: RunDll32ShimW 함수
ms.date: 03/30/2017
api_name:
- RunDll32ShimW
api_location:
- mscoree.dll
api_type:
- DLLExport
f1_keywords:
- RunDll32ShimW
helpviewer_keywords:
- RunDll32ShimW function [.NET Framework hosting]
ms.assetid: 9ea07b57-96e2-44df-8711-8fe6c119087f
topic_type:
- apiref
author: rpetrusha
ms.author: ronpet
ms.openlocfilehash: fa7df47ab55b8dc7ef3f55f5591b44614052bcee
ms.sourcegitcommit: 155012a8a826ee8ab6aa49b1b3a3b532e7b7d9bd
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 06/04/2019
ms.locfileid: "66490130"
---
# <a name="rundll32shimw-function"></a>RunDll32ShimW 함수
지정된 명령을 실행합니다.  
  
 .NET Framework 4에서이 함수에 사용 되지 않습니다.  
  
## <a name="syntax"></a>구문  
  
```  
HRESULT RunDll32ShimW (  
    [in] HWND        hwnd,  
    [in] HINSTANCE   hinst,  
    [in] LPCWSTR     lpszCmdLine,  
    [in] int         nCmdShow  
);  
```  
  
## <a name="parameters"></a>매개 변수  
 `hwnd`  
 [in] 명령 출력은 표시 되는 창 핸들입니다.  
  
 `hinst`  
 [in] 명령이 포함 된 라이브러리에 대 한 핸들입니다.  
  
 `lpszCmdLine`  
 [in] 실행할 명령을 지정 하는 문자열입니다.  
  
 `nCmdShow`  
 [in] 출력 창에 대 한 디스플레이 모드를 지정 하는 정수입니다.  
  
## <a name="requirements"></a>요구 사항  
 **플랫폼:** [시스템 요구 사항](../../../../docs/framework/get-started/system-requirements.md)을 참조하십시오.  
  
 **헤더:** MSCorEE.h  
  
 **라이브러리:** MSCorEE.dll  
  
 **.NET Framework 버전:** [!INCLUDE[net_current_v10plus](../../../../includes/net-current-v10plus-md.md)]  
  
## <a name="see-also"></a>참고자료

- [사용되지 않는 CLR 호스팅 함수](../../../../docs/framework/unmanaged-api/hosting/deprecated-clr-hosting-functions.md)
