---
title: GetCLRIdentityManager 함수
ms.date: 03/30/2017
api_name:
- GetCLRIdentityManager
api_location:
- mscoree.dll
api_type:
- COM
f1_keywords:
- GetCLRIdentityManager
helpviewer_keywords:
- GetCLRIdentityManager function [.NET Framework hosting]
ms.assetid: 66eeca30-adb4-45f4-aff5-347564c95724
topic_type:
- apiref
author: rpetrusha
ms.author: ronpet
ms.openlocfilehash: e18172ecf2d4300ae42cc42ecdb1783744cac105
ms.sourcegitcommit: 155012a8a826ee8ab6aa49b1b3a3b532e7b7d9bd
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 06/04/2019
ms.locfileid: "66490424"
---
# <a name="getclridentitymanager-function"></a>GetCLRIdentityManager 함수
CLR (공용 언어 런타임) id를 관리할 수 있도록 하는 인터페이스에 대 한 포인터를 가져옵니다.  
  
 .NET Framework 4에서이 함수에 사용 되지 않습니다.  
  
## <a name="syntax"></a>구문  
  
```  
STDAPI GetCLRIdentityManager(  
    [in]  REFIID      riid,  
    [out] IUnknown  **ppManager  
);  
```  
  
## <a name="parameters"></a>매개 변수  
 `riid`  
 [in] `REFIID` 가져오려는 인터페이스를 지정 하는 (인터페이스 식별자)입니다. 이 값은 IID_ICLRAssemblyIdentityManager 또는 IID_ICLRHostBindingPolicyManager 여야 합니다.  
  
 `ppManager`  
 [out] 주소에 대 한 포인터를 [ICLRAssemblyIdentityManager](../../../../docs/framework/unmanaged-api/hosting/iclrassemblyidentitymanager-interface.md) 요소나 [ICLRHostBindingPolicyManager](../../../../docs/framework/unmanaged-api/hosting/iclrhostbindingpolicymanager-interface.md) 개체입니다.  
  
## <a name="remarks"></a>설명  
 호출 된 [GetRealProcAddress](../../../../docs/framework/unmanaged-api/hosting/getrealprocaddress-function.md) 함수에 대 한 포인터를는 `GetCLRIdentityManager` 함수입니다.  
  
## <a name="requirements"></a>요구 사항  
 **플랫폼:** [시스템 요구 사항](../../../../docs/framework/get-started/system-requirements.md)을 참조하십시오.  
  
 **헤더:** MSCorEE.h  
  
 **라이브러리:** MSCorWks.dll  
  
 **.NET Framework 버전:** [!INCLUDE[net_current_v20plus](../../../../includes/net-current-v20plus-md.md)]  
  
## <a name="see-also"></a>참고자료

- [사용되지 않는 CLR 호스팅 함수](../../../../docs/framework/unmanaged-api/hosting/deprecated-clr-hosting-functions.md)
