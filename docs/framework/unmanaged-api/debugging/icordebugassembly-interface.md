---
title: ICorDebugAssembly インターフェイス
ms.date: 03/30/2017
api_name:
- ICorDebugAssembly
api_location:
- mscordbi.dll
api_type:
- COM
f1_keywords:
- ICorDebugAssembly
helpviewer_keywords:
- ICorDebugAssembly interface [.NET Framework debugging]
ms.assetid: 9d657a28-6984-4c5e-8a54-89d20080baff
topic_type:
- apiref
author: rpetrusha
ms.author: ronpet
ms.openlocfilehash: a2b802845e36e818a962484c1fea09cbcc1ceefd
ms.sourcegitcommit: 40364ded04fa6cdcb2b6beca7f68412e2e12f633
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 02/28/2019
ms.locfileid: "56974576"
---
# <a name="icordebugassembly-interface"></a>ICorDebugAssembly インターフェイス

アセンブリを表します。  
  
## <a name="methods"></a>メソッド  
  
|メソッド|説明|  
|------------|-----------------|  
|[EnumerateModules メソッド](../../../../docs/framework/unmanaged-api/debugging/icordebugassembly-enumeratemodules-method.md)|アセンブリに含まれるモジュールの列挙子を取得します。|  
|[GetAppDomain メソッド](../../../../docs/framework/unmanaged-api/debugging/icordebugassembly-getappdomain-method.md)|これを含むアプリケーション ドメインへのインターフェイス ポインターを取得`ICorDebugAssembly`インスタンス。|  
|[GetCodeBase メソッド](../../../../docs/framework/unmanaged-api/debugging/icordebugassembly-getcodebase-method.md)|.NET Framework の現在のバージョンでは実装されていません。|  
|[GetName メソッド](../../../../docs/framework/unmanaged-api/debugging/icordebugassembly-getname-method.md)|アセンブリの名前を取得します。|  
|[GetProcess メソッド](../../../../docs/framework/unmanaged-api/debugging/icordebugassembly-getprocess-method.md)|アセンブリが実行されている ICorDebugProcess インスタンスを取得します。|  
  
## <a name="remarks"></a>Remarks  
  
> [!NOTE]
>  このインターフェイスは、コンピューター間またはプロセス間でのリモート呼び出しをサポートしていません。  
  
## <a name="requirements"></a>必要条件  
 **プラットフォーム:**[システム要件](../../../../docs/framework/get-started/system-requirements.md)に関するページを参照してください。  
  
 **ヘッダー:** CorDebug.idl、CorDebug.h  
  
 **ライブラリ:** CorGuids.lib  
  
 **.NET Framework のバージョン:** [!INCLUDE[net_current_v10plus](../../../../includes/net-current-v10plus-md.md)]  
  
## <a name="see-also"></a>関連項目
- [デバッグ インターフェイス](../../../../docs/framework/unmanaged-api/debugging/debugging-interfaces.md)
