---
title: ICorDebugNativeFrame2::IsMatchingParentFrame メソッド
ms.date: 03/30/2017
api_name:
- ICorDebugNativeFrame2.IsMatchingParentFrame Method
api_location:
- mscordbi.dll
api_type:
- COM
f1_keywords:
- ICorDebugNativeFrame2::IsMatchingParentFrame
helpviewer_keywords:
- IsMatchingParentFrame method [.NET Framework debugging]
- ICorDebugNativeFrame2::IsMatchingParentFrame method [.NET Framework debugging]
ms.assetid: d2ca20db-df22-4528-a0dd-a09ea62c8998
topic_type:
- apiref
author: rpetrusha
ms.author: ronpet
ms.openlocfilehash: 6e8baa73594823c6b2f19b2af87e6a681ad71e3b
ms.sourcegitcommit: 6b308cf6d627d78ee36dbbae8972a310ac7fd6c8
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 01/23/2019
ms.locfileid: "54713302"
---
# <a name="icordebugnativeframe2ismatchingparentframe-method"></a>ICorDebugNativeFrame2::IsMatchingParentFrame メソッド
指定したフレームの現在のフレームの親であるかどうかを判断します。  
  
## <a name="syntax"></a>構文  
  
```  
HRESULT IsMatchingParentFrame([in] ICorDebugNativeFrame2  
                                      *pPotentialParentFrame,  
                              [out] BOOL *pIsParent);  
```  
  
#### <a name="parameters"></a>パラメーター  
 `pPotentialParentFrame`  
 [in]親のステータスを評価するフレーム オブジェクトへのポインター。  
  
 `pIsParent`  
 [out]`true`場合`pPotentialParentFrame`現在のフレームの親が、それ以外の`false`します。  
  
## <a name="return-value"></a>戻り値  
 このメソッドは、次の特定の HRESULT と、メソッドの失敗を示す HRESULT エラーも返します。  
  
|HRESULT|説明|  
|-------------|-----------------|  
|S_OK|親のステータスは正常に返されました。|  
|E_FAIL|親のステータスが返されませんでした。|  
|E_INVALIDARG|`pPotentialParentFrame` または `pIsParent` が null です。|  
  
## <a name="exceptions"></a>例外  
  
## <a name="remarks"></a>Remarks  
 `IsMatchingParentFrame` 返します`true`フレーム オブジェクトをメソッドに渡すメソッドが呼び出されたフレーム オブジェクトの親であるかどうか。 指定したフレームの子ではない特定のフレーム、メソッドを呼び出す場合は、エラーを返します。  
  
## <a name="requirements"></a>必要条件  
 **プラットフォーム:**[システム要件](../../../../docs/framework/get-started/system-requirements.md)に関するページを参照してください。  
  
 **ヘッダー:** CorDebug.idl、CorDebug.h  
  
 **ライブラリ:** CorGuids.lib  
  
 **.NET Framework のバージョン:** [!INCLUDE[net_current_v40plus](../../../../includes/net-current-v40plus-md.md)]  
  
## <a name="see-also"></a>関連項目
- [ICorDebugNativeFrame2 インターフェイス](../../../../docs/framework/unmanaged-api/debugging/icordebugnativeframe2-interface.md)
- [デバッグ インターフェイス](../../../../docs/framework/unmanaged-api/debugging/debugging-interfaces.md)
- [デバッグ](../../../../docs/framework/unmanaged-api/debugging/index.md)
