---
title: ICorPublishProcess::GetProcessID メソッド
ms.date: 03/30/2017
api_name:
- ICorPublishProcess.GetProcessID
api_location:
- mscordbi.dll
api_type:
- COM
f1_keywords:
- ICorPublishProcess::GetProcessID
helpviewer_keywords:
- ICorPublishProcess::GetProcessID method [.NET Framework debugging]
- GetProcessID method [.NET Framework debugging]
ms.assetid: f31185e0-f01d-463a-b392-42163e39bfe9
topic_type:
- apiref
author: rpetrusha
ms.author: ronpet
ms.openlocfilehash: 39382b73a0fcd73282dbc69508b15dbfff240463
ms.sourcegitcommit: 6b308cf6d627d78ee36dbbae8972a310ac7fd6c8
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 01/23/2019
ms.locfileid: "54669708"
---
# <a name="icorpublishprocessgetprocessid-method"></a>ICorPublishProcess::GetProcessID メソッド
このプロセスには、オペレーティング システムの識別子を取得します。  
  
## <a name="syntax"></a>構文  
  
```  
HRESULT GetProcessID (  
    [out] unsigned   *pid  
);  
```  
  
#### <a name="parameters"></a>パラメーター  
 `pid`  
 [out]これで表されるプロセスの id へのポインター [ICorPublishProcess](../../../../docs/framework/unmanaged-api/debugging/icorpublishprocess-interface.md)オブジェクト。  
  
## <a name="requirements"></a>必要条件  
 **プラットフォーム:**[システム要件](../../../../docs/framework/get-started/system-requirements.md)に関するページを参照してください。  
  
 **ヘッダー:** CorPub.idl, CorPub.h  
  
 **ライブラリ:** CorGuids.lib  
  
 **.NET Framework のバージョン:** [!INCLUDE[net_current_v10plus](../../../../includes/net-current-v10plus-md.md)]  
  
## <a name="see-also"></a>関連項目
- [ICorPublishProcess インターフェイス](../../../../docs/framework/unmanaged-api/debugging/icorpublishprocess-interface.md)
