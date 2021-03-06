---
title: '方法: Windows フォームのボタン クリックに応答するには'
ms.date: 03/30/2017
dev_langs:
- csharp
- vb
- cpp
helpviewer_keywords:
- buttons [Windows Forms], responding to Click events
- events [Windows Forms], Click events
- Click event [Windows Forms], Button control
- MouseDown event
- Button control [Windows Forms], click response
- double-clicks
- examples [Windows Forms], controls
- Click event [Windows Forms], responding to
ms.assetid: 7a4951bd-369c-4662-b246-28ad83eda484
ms.openlocfilehash: 98b52e914a891baec0b52dcc7b38d4f9f2198c90
ms.sourcegitcommit: 6b308cf6d627d78ee36dbbae8972a310ac7fd6c8
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 01/23/2019
ms.locfileid: "54539552"
---
# <a name="how-to-respond-to-windows-forms-button-clicks"></a>方法: Windows フォームのボタン クリックに応答するには
Windows フォームの最も基本的な使用<xref:System.Windows.Forms.Button>コントロールのボタンがクリックされたときに、いくつかのコードを実行します。  
  
 クリックすると、<xref:System.Windows.Forms.Button>コントロールもなどが生成されるその他のイベント数、 <xref:System.Windows.Forms.Control.MouseEnter>、 <xref:System.Windows.Forms.Control.MouseDown>、および<xref:System.Windows.Forms.Control.MouseUp>イベント。 これらの関連イベントのイベント ハンドラーをアタッチする場合は、そのアクションが競合しないことを確認します。 たとえば場合、ユーザーがテキスト ボックスに入力した情報をクリア ボタンをクリックして、ボタンの上にマウス ポインターを置く必要があります表示されません現時点で存在しない情報をツール ヒント。  
  
 ユーザーをダブルクリックする場合、<xref:System.Windows.Forms.Button>コントロール、1 回のクリックを個別に処理されます。 これは、コントロールがダブルクリック イベントをサポートしません。  
  
### <a name="to-respond-to-a-button-click"></a>ボタンのクリックに応答するには  
  
-   ボタンの`Click`<xref:System.EventHandler>を実行するコードを記述します。 `Button1_Click` コントロールにバインドする必要があります。 詳細については、「[方法 :Windows フォームの実行時にイベント ハンドラーを作成](../../../../docs/framework/winforms/how-to-create-event-handlers-at-run-time-for-windows-forms.md)です。  
  
    ```vb  
    Private Sub Button1_Click(ByVal sender As System.Object, ByVal e As System.EventArgs) Handles Button1.Click  
       MessageBox.Show("Button1 was clicked")  
    End Sub  
    ```  
  
    ```csharp  
    private void button1_Click(object sender, System.EventArgs e)  
    {  
       MessageBox.Show("button1 was clicked");  
    }  
    ```  
  
    ```cpp  
    private:  
       void button1_Click(System::Object ^ sender,  
          System::EventArgs ^ e)  
       {  
          MessageBox::Show("button1 was clicked");  
       }  
    ```  
  
## <a name="see-also"></a>関連項目
- [Button コントロールの概要](../../../../docs/framework/winforms/controls/button-control-overview-windows-forms.md)
- [Windows フォームの Button コントロールを選択する方法](../../../../docs/framework/winforms/controls/ways-to-select-a-windows-forms-button-control.md)
- [Button コントロール](../../../../docs/framework/winforms/controls/button-control-windows-forms.md)
