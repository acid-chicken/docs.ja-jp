---
title: '方法: バインディングをクリアする'
ms.date: 03/30/2017
dev_langs:
- csharp
- vb
helpviewer_keywords:
- bindings [WPF], clearing
- clearing bindings [WPF]
- data binding [WPF], clearing bindings
ms.assetid: 73962a93-32a9-4bcd-9240-bcfbb239093a
ms.openlocfilehash: bd0f42b868c316cb9a6344134d4aaf01930519ac
ms.sourcegitcommit: 6b308cf6d627d78ee36dbbae8972a310ac7fd6c8
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 01/23/2019
ms.locfileid: "54508432"
---
# <a name="how-to-clear-bindings"></a>方法: バインディングをクリアする
この例では、オブジェクトからバインディングをクリアする方法を示します。  
  
## <a name="example"></a>例  
 オブジェクトの個々 のプロパティからバインディングをクリアするには、呼び出す<xref:System.Windows.Data.BindingOperations.ClearBinding%2A>次の例に示すようにします。 次の例からのバインドを削除する、<xref:System.Windows.Controls.TextBlock.TextProperty>の*mytext*、<xref:System.Windows.Controls.TextBlock>オブジェクト。  
  
 [!code-csharp[CodeOnlyBinding#ClearBinding](../../../../samples/snippets/csharp/VS_Snippets_Wpf/CodeOnlyBinding/CSharp/binding.cs#clearbinding)]
 [!code-vb[CodeOnlyBinding#ClearBinding](../../../../samples/snippets/visualbasic/VS_Snippets_Wpf/CodeOnlyBinding/VisualBasic/App.vb#clearbinding)]  
  
 バインディングをクリアすると、バイディングが削除され、依存関係プロパティの値は、バインディングが存在していなかったときの値に変更されます。 この値は、既定値、継承された値、データ テンプレート バインディングの値などです。  
  
 オブジェクトのすべてのプロパティからバインディングをクリアする<xref:System.Windows.Data.BindingOperations.ClearAllBindings%2A>します。  
  
## <a name="see-also"></a>関連項目
- <xref:System.Windows.Data.BindingOperations>
- [データ バインディングの概要](../../../../docs/framework/wpf/data/data-binding-overview.md)
- [方法トピック](../../../../docs/framework/wpf/data/data-binding-how-to-topics.md)
