---
title: '方法: Windows フォーム DataGridView コントロールでデータを検証します。'
ms.date: 03/30/2017
dev_langs:
- csharp
- vb
helpviewer_keywords:
- data [Windows Forms], validation
- DataGridView control [Windows Forms], data validation
- data grids [Windows Forms], validating data
- data validation [Windows Forms], Windows Forms
ms.assetid: d10aef35-701e-4a3c-a684-2a2ed1aeaca6
ms.openlocfilehash: 10cd8a0bd2bed7c55be9540d5ee68b13dcd5f90d
ms.sourcegitcommit: af0a22a4eb11bbcd33baec49150d551955b50a16
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 02/14/2019
ms.locfileid: "56261727"
---
# <a name="how-to-validate-data-in-the-windows-forms-datagridview-control"></a>方法: Windows フォーム DataGridView コントロールでデータを検証します。
ユーザーによって <xref:System.Windows.Forms.DataGridView> コントロールに入力されたデータを検証する方法を次のコード例に示します。 この例では、<xref:System.Windows.Forms.DataGridView> には、Northwind サンプル データベースの `Customers` テーブルの行が読み込まれます。 ユーザーが `CompanyName` 列内のセルを編集すると、値の有効性をテストするために、空ではないことが確認されます。 
  <xref:System.Windows.Forms.DataGridView.CellValidating> イベントのイベント ハンドラーによって値が空の文字列であることが検出されると、<xref:System.Windows.Forms.DataGridView> では、ユーザーが空ではない文字列を入力するまでそのセルから移動できなくなります。  
  
 このコード例の詳細については、次を参照してください。[チュートリアル。フォームの DataGridView コントロールを Windows のデータの検証](../../../../docs/framework/winforms/controls/walkthrough-validating-data-in-the-windows-forms-datagridview-control.md)です。  
  
## <a name="example"></a>例  
 [!code-csharp[System.Windows.Forms.DataGridViewDataValidation#00](../../../../samples/snippets/csharp/VS_Snippets_Winforms/System.Windows.Forms.DataGridViewDataValidation/CS/datavalidation.cs#00)]
 [!code-vb[System.Windows.Forms.DataGridViewDataValidation#00](../../../../samples/snippets/visualbasic/VS_Snippets_Winforms/System.Windows.Forms.DataGridViewDataValidation/VB/datavalidation.vb#00)]  
  
## <a name="compiling-the-code"></a>コードのコンパイル  
 この例で必要な要素は次のとおりです。  
  
-   System、System.Data、System.Windows.Forms、および System.XML の各アセンブリへの参照。  
  
 コマンドラインからこの例を Visual Basic または Visual c# の構築方法の詳細については、次を参照してください。 [、コマンドラインからビルドする](../../../visual-basic/reference/command-line-compiler/building-from-the-command-line.md)または[コマンド ライン ビルドで csc.exe](../../../csharp/language-reference/compiler-options/command-line-building-with-csc-exe.md)します。 新しいプロジェクトにコードを貼り付けることによって、この例では、Visual Studio を構築することもできます。  
  
## <a name="net-framework-security"></a>.NET Framework セキュリティ  
 接続文字列内に機密情報 (パスワードなど) を格納すると、アプリケーションのセキュリティに影響を及ぼすことがあります。 データベースへのアクセスを制御する方法としては、Windows 認証 (統合セキュリティとも呼ばれます) を使用する方が安全です。 詳細については、「[接続情報の保護](../../../../docs/framework/data/adonet/protecting-connection-information.md)」を参照してください。  
  
## <a name="see-also"></a>関連項目
- <xref:System.Windows.Forms.DataGridView>
- <xref:System.Windows.Forms.BindingSource>
- [チュートリアル: Windows フォームの DataGridView コントロールのデータの検証](../../../../docs/framework/winforms/controls/walkthrough-validating-data-in-the-windows-forms-datagridview-control.md)
- [Windows フォーム DataGridView コントロールでのデータ入力](../../../../docs/framework/winforms/controls/data-entry-in-the-windows-forms-datagridview-control.md)
- [チュートリアル: Windows フォームの DataGridView コントロールでのデータ入力中に発生したエラーの処理](../../../../docs/framework/winforms/controls/handling-errors-that-occur-during-data-entry-in-the-datagrid.md)
- [接続情報の保護](../../../../docs/framework/data/adonet/protecting-connection-information.md)
