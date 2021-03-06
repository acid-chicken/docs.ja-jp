---
title: '方法: オブジェクトを回転させる'
ms.date: 03/30/2017
dev_langs:
- csharp
- vb
helpviewer_keywords:
- graphics [WPF], rotating objects [WPF]
- rotating objects [WPF]
ms.assetid: ee3466cd-e66f-4e8f-8a5a-71d77bc1e390
ms.openlocfilehash: b44ce71f91962806704eb05a9cbec53638856b3e
ms.sourcegitcommit: 6b308cf6d627d78ee36dbbae8972a310ac7fd6c8
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 01/23/2019
ms.locfileid: "54525431"
---
# <a name="how-to-rotate-an-object"></a>方法: オブジェクトを回転させる
次の例では、オブジェクトを回転させる方法を示します。 例では、最初に作成、<xref:System.Windows.Media.RotateTransform>を指定してその<xref:System.Windows.Media.RotateTransform.Angle%2A>(度単位)。  
  
 次の例では、回転、 <xref:System.Windows.Shapes.Polyline> 45 度の左上隅のオブジェクトします。  
  
## <a name="example"></a>例  
 [!code-xaml[Transforms_snip#RotatePolylineAboutTopLeft](../../../../samples/snippets/csharp/VS_Snippets_Wpf/Transforms_snip/CS/RotateTransformExample.xaml#rotatepolylineabouttopleft)]  
  
 [!code-csharp[Transforms_Procedural_snip#RotatePolylineAboutTopLeft](../../../../samples/snippets/csharp/VS_Snippets_Wpf/Transforms_Procedural_snip/CSharp/RotateTransformExample.cs#rotatepolylineabouttopleft)]
 [!code-vb[Transforms_Procedural_snip#RotatePolylineAboutTopLeft](../../../../samples/snippets/visualbasic/VS_Snippets_Wpf/Transforms_Procedural_snip/VisualBasic/RotateTransformExample.vb#rotatepolylineabouttopleft)]  
  
 <xref:System.Windows.Media.RotateTransform.CenterX%2A>と<xref:System.Windows.Media.RotateTransform.CenterY%2A>のプロパティ、<xref:System.Windows.Media.RotateTransform>ポイント オブジェクトが回転を指定します。 この中心点は、変換する要素の座標空間で表します。 既定では、回転は (0,0) に適用されます。これは変換対象のオブジェクトの左上隅です。  
  
 次の例では、回転、 <xref:System.Windows.Shapes.Polyline> (25, 50) にした、時計回りに 45 度のオブジェクトします。  
  
 [!code-xaml[Transforms_snip#RotatePolylineAboutCenter](../../../../samples/snippets/csharp/VS_Snippets_Wpf/Transforms_snip/CS/RotateTransformExample.xaml#rotatepolylineaboutcenter)]  
  
 [!code-csharp[Transforms_Procedural_snip#RotatePolylineAboutCenter](../../../../samples/snippets/csharp/VS_Snippets_Wpf/Transforms_Procedural_snip/CSharp/RotateTransformExample.cs#rotatepolylineaboutcenter)]
 [!code-vb[Transforms_Procedural_snip#RotatePolylineAboutCenter](../../../../samples/snippets/visualbasic/VS_Snippets_Wpf/Transforms_Procedural_snip/VisualBasic/RotateTransformExample.vb#rotatepolylineaboutcenter)]  
  
 次の図は、適用した結果、<xref:System.Windows.Media.Transform>に 2 つのオブジェクト。  
  
 ![中心点が異なる 45 度の回転](../../../../docs/framework/wpf/graphics-multimedia/media/wcpsdk-graphicsmm-rotatetransform45degrees.gif "wcpsdk_graphicsmm_rotatetransform45degrees")  
異なる中心点を軸に 45 度回転させた 2 つのオブジェクト  
  
 <xref:System.Windows.Shapes.Polyline>前の例では、<xref:System.Windows.UIElement>します。 適用すると、<xref:System.Windows.Media.Transform>を<xref:System.Windows.UIElement.RenderTransform%2A>のプロパティを<xref:System.Windows.UIElement>、使用することができます、<xref:System.Windows.UIElement.RenderTransformOrigin%2A>の原点を指定するプロパティすべて<xref:System.Windows.Media.Transform>要素に適用します。 <xref:System.Windows.UIElement.RenderTransformOrigin%2A>プロパティは、相対座標を使用して、そのサイズがわからない場合でも、要素の中央に変換を適用することができます。 詳細については、および例についてを参照してください。[を相対値での変換の原点を指定する](../../../../docs/framework/wpf/graphics-multimedia/how-to-specify-the-origin-of-a-transform-by-using-relative-values.md)します。  
  
 完全なサンプルについては、「[2-D 変換のサンプル](https://go.microsoft.com/fwlink/?LinkID=158252)」をご覧ください。  
  
## <a name="see-also"></a>関連項目
- <xref:System.Windows.Media.Transform>
- [変換の概要](../../../../docs/framework/wpf/graphics-multimedia/transforms-overview.md)
- [方法トピック](../../../../docs/framework/wpf/graphics-multimedia/transformations-how-to-topics.md)
