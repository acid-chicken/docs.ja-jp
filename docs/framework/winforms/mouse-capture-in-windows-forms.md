---
title: Windows フォームにおけるマウスのキャプチャ
ms.date: 03/30/2017
helpviewer_keywords:
- mouse [Windows Forms], capture
ms.assetid: 8911d4b0-a4f8-4f93-8246-371aebd27d0c
ms.openlocfilehash: ca16d2fa2339f8d9110bb748a687f90e093598fd
ms.sourcegitcommit: 6b308cf6d627d78ee36dbbae8972a310ac7fd6c8
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 01/23/2019
ms.locfileid: "54690329"
---
# <a name="mouse-capture-in-windows-forms"></a>Windows フォームにおけるマウスのキャプチャ
*マウスのキャプチャ*コントロールのすべてのマウス入力コマンドの実行時を参照します。 コントロールは、マウスをキャプチャしたら、マウス ポインターが境界内にあるかどうかを示すマウス入力を受け取ります。  
  
## <a name="setting-mouse-capture"></a>マウスのキャプチャの設定  
 Windows フォームで、ユーザーがコントロールのマウス ボタンを押すし、ユーザーがマウス ボタンを離したときに、マウスがコントロールによってリリースされたときに、マウスはコントロールによってキャプチャされます。  
  
 <xref:System.Windows.Forms.Control.Capture%2A>のプロパティ、<xref:System.Windows.Forms.Control>クラスは、コントロールがマウスをキャプチャしたかどうかを指定します。 コントロールがマウス キャプチャを失ったときにするには、処理、<xref:System.Windows.Forms.Control.MouseCaptureChanged>イベント。  
  
 前面のウィンドウには、マウスをキャプチャできます。 背景ウィンドウがマウスをキャプチャしようとすると、ウィンドウは、ウィンドウの表示部分内にマウス ポインターがときに発生するマウス イベントにのみメッセージを受信します。 また、前面のウィンドウがマウスをキャプチャした場合でも、ユーザー クリックできます別のウィンドウへの前景色。 マウスをキャプチャしたら、ショートカット キーは機能しません。  
  
## <a name="see-also"></a>関連項目
- [Windows フォーム アプリケーションにおけるマウス入力](../../../docs/framework/winforms/mouse-input-in-a-windows-forms-application.md)
