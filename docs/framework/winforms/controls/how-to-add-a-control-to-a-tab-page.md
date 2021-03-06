---
title: '方法: タブ ページにコントロールを追加します。'
ms.date: 03/30/2017
dev_langs:
- csharp
- vb
- cpp
helpviewer_keywords:
- TabPage control
- tab controls [Windows Forms], tab order
- tab pages [Windows Forms], adding controls
ms.assetid: b092532e-7346-469f-b9a1-897f9bea4fb7
ms.openlocfilehash: 42f0be64a6ac050fe8873588263b1faf7e2491a6
ms.sourcegitcommit: 6b308cf6d627d78ee36dbbae8972a310ac7fd6c8
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 01/23/2019
ms.locfileid: "54710184"
---
# <a name="how-to-add-a-control-to-a-tab-page"></a>方法: タブ ページにコントロールを追加します。
Windows フォームを使用する<xref:System.Windows.Forms.TabControl>を組織的に他のコントロールを表示します。 次の手順では、最初のタブにボタンを追加する方法を示します。タブ ページのラベルの部分にアイコンを追加する方法の詳細については、次を参照してください。[方法。Windows フォーム TabControl の外観を変更する](../../../../docs/framework/winforms/controls/how-to-change-the-appearance-of-the-windows-forms-tabcontrol.md)します。  
  
### <a name="to-add-a-control-programmatically"></a>プログラムでコントロールを追加するには  
  
1.  使用して、<xref:System.Windows.Forms.Control.ControlCollection.Add%2A>メソッドによって返されるコレクションの<xref:System.Windows.Forms.Control.Controls%2A>プロパティの<xref:System.Windows.Forms.TabPage>:  
  
     [!code-cpp[TabPageControlCollectionHowToAdd#1](../../../../samples/snippets/cpp/VS_Snippets_Winforms/tabpagecontrolcollectionhowtoadd/cpp/add.cpp#1)]
     [!code-csharp[TabPageControlCollectionHowToAdd#1](../../../../samples/snippets/csharp/VS_Snippets_Winforms/tabpagecontrolcollectionhowtoadd/cs/add.cs#1)]
     [!code-vb[TabPageControlCollectionHowToAdd#1](../../../../samples/snippets/visualbasic/VS_Snippets_Winforms/tabpagecontrolcollectionhowtoadd/vb/add.vb#1)]  
  
## <a name="see-also"></a>関連項目
- [TabControl コントロール](../../../../docs/framework/winforms/controls/tabcontrol-control-windows-forms.md)
- [TabControl コントロールの概要](../../../../docs/framework/winforms/controls/tabcontrol-control-overview-windows-forms.md)
- [方法: Windows フォーム TabControl の外観を変更します。](../../../../docs/framework/winforms/controls/how-to-change-the-appearance-of-the-windows-forms-tabcontrol.md)
- [方法: タブ ページを無効にします。](../../../../docs/framework/winforms/controls/how-to-disable-tab-pages.md)
- [方法: Windows フォーム tabcontrol のタブ追加および削除](../../../../docs/framework/winforms/controls/how-to-add-and-remove-tabs-with-the-windows-forms-tabcontrol.md)
