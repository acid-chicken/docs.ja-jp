---
title: '方法: ScrollBar のつまみのサイズをカスタマイズする'
ms.date: 03/30/2017
helpviewer_keywords:
- ScrollBar control [WPF]
- customizing thumb size [WPF]
- thumb size [WPF]
ms.assetid: fa32b866-5ca1-4e73-85e7-2ac64b80d194
ms.openlocfilehash: 2c77eb23c1a42051a7c2d81f3454eb51425fa034
ms.sourcegitcommit: 6b308cf6d627d78ee36dbbae8972a310ac7fd6c8
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 01/23/2019
ms.locfileid: "54590865"
---
# <a name="how-to-customize-the-thumb-size-on-a-scrollbar"></a>方法: ScrollBar のつまみのサイズをカスタマイズする
このトピックでは、設定する方法を説明します、<xref:System.Windows.Controls.Primitives.Thumb>の<xref:System.Windows.Controls.Primitives.ScrollBar>固定サイズの最小サイズを指定する方法を<xref:System.Windows.Controls.Primitives.Thumb>の<xref:System.Windows.Controls.Primitives.ScrollBar>します。  
  
## <a name="example"></a>例  
  
## <a name="description"></a>説明  
 次の例では、作成、<xref:System.Windows.Controls.Primitives.ScrollBar>を持つ、<xref:System.Windows.Controls.Primitives.Thumb>固定サイズです。 例のセット、<xref:System.Windows.Controls.Primitives.Track.ViewportSize%2A>のプロパティ、<xref:System.Windows.Controls.Primitives.Thumb>に<xref:System.Double.NaN>の高さを設定し、<xref:System.Windows.Controls.Primitives.Thumb>します。  水平方向を作成する<xref:System.Windows.Controls.Primitives.ScrollBar>で、<xref:System.Windows.Controls.Primitives.Thumb>固定幅を持つの幅を設定、<xref:System.Windows.Controls.Primitives.Thumb>します。  
  
## <a name="code"></a>コード  
 [!code-xaml[ScrollBarCustomThumbSize#1](../../../../samples/snippets/csharp/VS_Snippets_Wpf/ScrollBarCustomThumbSize/CS/Window1.xaml#1)]  
  
## <a name="description"></a>説明  
 次の例では、作成、<xref:System.Windows.Controls.Primitives.ScrollBar>を持つ、<xref:System.Windows.Controls.Primitives.Thumb>最小サイズ。 値を設定する例では、<xref:System.Windows.SystemParameters.VerticalScrollBarButtonHeightKey%2A>します。 水平方向を作成する<xref:System.Windows.Controls.Primitives.ScrollBar>で、<xref:System.Windows.Controls.Primitives.Thumb>幅の最小値を持つ、設定、<xref:System.Windows.SystemParameters.HorizontalScrollBarButtonWidthKey%2A>します。  
  
## <a name="code"></a>コード  
 [!code-xaml[ScrollBarCustomThumbSize#2](../../../../samples/snippets/csharp/VS_Snippets_Wpf/ScrollBarCustomThumbSize/CS/Window1.xaml#2)]  
  
## <a name="see-also"></a>関連項目
- [ScrollBar のスタイルとテンプレート](../../../../docs/framework/wpf/controls/scrollbar-styles-and-templates.md)
