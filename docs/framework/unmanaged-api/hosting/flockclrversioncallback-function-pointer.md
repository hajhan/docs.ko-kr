---
title: FLockClrVersionCallback 함수 포인터
ms.date: 03/30/2017
api_name:
- FLockClrVersionCallback
api_location:
- mscoree.dll
api_type:
- COM
f1_keywords:
- FLockClrVersionCallback
helpviewer_keywords:
- FLockClrVersionCallback function pointer [.NET Framework hosting]
ms.assetid: 98a4762d-9ad2-45bd-9d03-39064a028b44
topic_type:
- apiref
author: rpetrusha
ms.author: ronpet
ms.openlocfilehash: ef308b624525c3a139c892e6118a24d6adb6e14a
ms.sourcegitcommit: 155012a8a826ee8ab6aa49b1b3a3b532e7b7d9bd
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 06/04/2019
ms.locfileid: "66490455"
---
# <a name="flockclrversioncallback-function-pointer"></a>FLockClrVersionCallback 함수 포인터
해당 초기화를 나타내기 위해 공용 언어 런타임 (CLR) 호출 시작 또는 완료 하는 함수를 가리킵니다.  
  
 .NET Framework 4에서이 함수 포인터에 사용 되지 않습니다.  
  
## <a name="syntax"></a>구문  
  
```  
typedef HRESULT (__stdcall *FLockClrVersionCallback) ( );  
```  
  
## <a name="remarks"></a>설명  
 이 함수는 호스트에서 구현 됩니다.  
  
## <a name="requirements"></a>요구 사항  
 **플랫폼:** [시스템 요구 사항](../../../../docs/framework/get-started/system-requirements.md)을 참조하십시오.  
  
 **헤더:** MSCorEE.h  
  
 **라이브러리:** MSCorWks.dll  
  
 **.NET Framework 버전:** [!INCLUDE[net_current_v20plus](../../../../includes/net-current-v20plus-md.md)]  
  
## <a name="see-also"></a>참고자료

- [LockClrVersion 함수](../../../../docs/framework/unmanaged-api/hosting/lockclrversion-function.md)
- [사용되지 않는 CLR 호스팅 함수](../../../../docs/framework/unmanaged-api/hosting/deprecated-clr-hosting-functions.md)
