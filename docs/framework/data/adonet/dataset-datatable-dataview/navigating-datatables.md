---
title: DataTable の移動
ms.date: 03/30/2017
dev_langs:
- csharp
- vb
ms.assetid: 202026a1-ec79-435e-b507-12a77f5011b2
ms.openlocfilehash: 710e4bdaeafc483510c4102dc9ac0f6ffaaafce9
ms.sourcegitcommit: 6b308cf6d627d78ee36dbbae8972a310ac7fd6c8
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 01/23/2019
ms.locfileid: "54528083"
---
# <a name="navigating-datatables"></a>DataTable の移動
<xref:System.Data.DataTableReader> は、1 つ以上の <xref:System.Data.DataTable> オブジェクトの内容を、読み取り専用、前方参照専用の 1 つ以上の結果セットとして取得します。  
  
 <xref:System.Data.DataTableReader> メソッドの呼び出しにより DataTableReader を作成した場合、<xref:System.Data.DataSet.CreateDataReader%2A> に複数の結果セットが含まれる場合があります。 結果セットが複数ある場合、<xref:System.Data.DataTableReader.NextResult%2A> メソッドは、カーソルを次の結果セットに移動します。 これは前方参照専用です。 前の結果セットに戻ることはできません。  
  
## <a name="example"></a>例  
 次の例では、`TestConstructor`メソッドでは、2 つ作成されます<xref:System.Data.DataTable>インスタンス。 このコンス トラクターを示すために、<xref:System.Data.DataTableReader>クラス、サンプルを作成する新しい**DataTableReader** 、2 つを格納する配列に基づく**Datatable**、し、単純な操作を実行します。最初のいくつかの列から、コンソール ウィンドウに内容を印刷します。  
  
 [!code-csharp[DataWorks DataTableReader.NextResult#1](../../../../../samples/snippets/csharp/VS_Snippets_ADO.NET/DataWorks DataTableReader.NextResult/CS/source.cs#1)]
 [!code-vb[DataWorks DataTableReader.NextResult#1](../../../../../samples/snippets/visualbasic/VS_Snippets_ADO.NET/DataWorks DataTableReader.NextResult/VB/source.vb#1)]  
  
## <a name="see-also"></a>関連項目
- [DataTableReaders](../../../../../docs/framework/data/adonet/dataset-datatable-dataview/datatablereaders.md)
- [ADO.NET のマネージド プロバイダーと DataSet デベロッパー センター](https://go.microsoft.com/fwlink/?LinkId=217917)
