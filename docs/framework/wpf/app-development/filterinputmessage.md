---
title: FilterInputMessage
ms.date: 03/30/2017
helpviewer_keywords:
- raw input [WPF]
- FilterInputMessage method [WPF]
ms.assetid: 4d74c6cf-7d1d-49ff-96c1-231340ce54f5
ms.openlocfilehash: c3620e13951afddc8de25c314de17704548d2366
ms.sourcegitcommit: 8f95d3a37e591963ebbb9af6e90686fd5f3b8707
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 02/23/2019
ms.locfileid: "56746167"
---
# <a name="filterinputmessage"></a>FilterInputMessage
E_NOTIMPL が返されない限り、メッセージを受信するたびに PresentationHost.exe によって呼び出されます。  
  
## <a name="syntax"></a>構文  
  
```  
HRESULT FilterInputMessage( [in] MSG* pMsg ) ;  
```  
  
#### <a name="parameters"></a>パラメーター  
 `pMsg`  
  
 [in] 未加工入力を取得するウィンドウに送信される WM_INPUT メッセージ。  
  
## <a name="property-valuereturn-value"></a>プロパティ値/戻り値  
 HRESULT:  
  
 S_OK - フィルターはメッセージを処理せず、それ以降の処理は実行されることがあります。  
  
 S_FALSE - フィルターはこのメッセージを処理しました。それ以降の処理は実行されません。  
  
 E_NOTIMPL – この値が返された場合[FilterInputMessage](../../../../docs/framework/wpf/app-development/filterinputmessage.md)は再度呼び出されません。 この値は、カスタムの進行状況の提供のみを対象とするホスト アプリケーションから返されることがあります。PresentationHost.exe へのエラー ユーザー インターフェイスは、PresentationHost.exe からの未加工の入力メッセージの転送を対象としていません。  
  
## <a name="remarks"></a>Remarks  
 PresentationHost.exe は、キーボード、マウス、およびリモート コントロールなどのさまざまな未加工入力デバイスのターゲットになります。 場合によって、ホスト アプリケーションでの動作は PresentationHost.exe で使用される入力に依存します。 たとえば、ホスト アプリケーションは、特定のユーザー インターフェイス要素を表示するかどうかを判断するために、特定の入力メッセージの受信に依存することがあります。  
  
 ホスト アプリケーションがこれらの動作を提供するために必要な入力メッセージを受信するには、PresentationHost.exe では、呼び出すことによってホストされるアプリケーションに適切な未加工の入力メッセージを転送[FilterInputMessage](../../../../docs/framework/wpf/app-development/filterinputmessage.md)します。  
  
 ホストされるアプリケーションがによって返される未加工の入力デバイス (ヒューマン インターフェイス デバイス) のセットを登録して未加工の入力メッセージを受信[GetRawInputDevices](../../../../docs/framework/wpf/app-development/getrawinputdevices.md)します。  
  
## <a name="see-also"></a>関連項目
- [WM_INPUT メッセージ](/windows/desktop/inputdev/wm-input)
