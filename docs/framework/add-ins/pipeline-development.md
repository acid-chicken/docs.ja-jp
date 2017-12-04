---
title: "パイプラインの開発"
ms.custom: 
ms.date: 03/30/2017
ms.prod: .net-framework
ms.reviewer: 
ms.suite: 
ms.technology: dotnet-clr
ms.tgt_pltfrm: 
ms.topic: article
helpviewer_keywords:
- add-in pipeline [.NET Framework], segments
- activation path for add-ins [.NET Framework]
- add-in pipeline [.NET Framework], activation path
- communication pipeline for add-ins [.NET Framework]
- add-in pipeline [.NET Framework], about
- add-ins [.NET Framework], pipeline development
ms.assetid: 932788f2-b87d-44cf-82f9-04492a8b2722
caps.latest.revision: "31"
author: rpetrusha
ms.author: ronpet
manager: wpickett
ms.openlocfilehash: 4991fc65a48d620d30d09c44f1a30c2d1839071e
ms.sourcegitcommit: 4f3fef493080a43e70e951223894768d36ce430a
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 11/21/2017
---
# <a name="pipeline-development"></a>パイプラインの開発
アドイン パイプラインは、ホスト アプリケーションとそのアドインが互いに通信するために使用する必要がありますパイプライン セグメントのパスです。  
  
 次の図は、通信パイプラインとそのセグメントを示します。  
  
 ![追加 (& a) #45; パイプライン モデル。] (../../../docs/framework/add-ins/media/addin1.png "AddIn1")  
アドイン パイプライン  
  
 ホスト アプリケーションは、パイプラインの 1 つの最後に、アドインで、もう一方の end。 各端から開始し、中央方向に移動、ホスト アプリケーションとアドインの両方がある、両方を共有するオブジェクト モデルのビューを定義する抽象基本クラスです。 これらの型 (クラス) は、ビューでは、追加のパイプライン セグメントと、アドイン パイプライン セグメントのホスト ビューを構成します。 アドイン ビュー パイプライン セグメントには多くの場合、2 つ以上の抽象クラスが含まれていますが、アドインから継承するクラスは、アドインをベースと呼ばれます。  
  
 アドイン側アダプター パイプライン セグメントと、ホスト側アダプター パイプライン セグメントのフローが変換、ビュー パイプライン セグメント、およびコントラクト パイプライン セグメントの間での型。 パイプラインの中央のセグメントがから派生したコントラクト、<xref:System.AddIn.Contract.IContract>インターフェイスです。 このコントラクトは、ホスト アプリケーションとそのアドインを両方使用するメソッドを定義します。  
  
 個別のアプリケーション ドメインにホストとアドインを読み込む場合、アドインのスコープからホスト アプリケーションのスコープを分離する分離境界が設定されます。 コントラクトは、ホストとアドインでは、アプリケーション ドメインの両方に読み込まれている唯一のアセンブリです。 ホストとアドインを各コントラクト メソッドのビューのみを参照してください。 したがって、コントラクトから抽象化レイヤーで区切られます。  
  
 パイプライン セグメントを開発するには、それらを格納するディレクトリ構造を作成する必要があります。 開発の必要条件とスコープのガイドラインの詳細については、次を参照してください。[パイプラインの開発要件](http://msdn.microsoft.com/en-us/ef9fa986-e80b-43e1-868b-247f4c1d9da5)です。  
  
 次の図は、パイプライン セグメントを構成する型を示します。 図に示す型の名前は任意ですが、ホストとホストを除くすべての種類のビューを追加で必要な属性情報ストアを構築するメソッドによって検出できるようにします。  
  
 ![追加 (& a) #45 以外の型に必要な属性をモデルにします。] (../../../docs/framework/add-ins/media/addin-model.png "AddIn_Model")  
アドイン パイプラインの種類  
  
 次の表では、アドインをアクティブ化するためのパイプライン セグメントについて説明します。 これらのセグメントの詳細については、次を参照してください。[コントラクト、ビュー、およびアダプター](http://msdn.microsoft.com/en-us/a6460173-9507-4b87-8c07-d4ee245d715c)です。  
  
|パイプライン セグメント|説明|  
|----------------------|-----------------|  
|Host|アドインのインスタンスを作成するアプリケーションのアセンブリ。|  
|アドインのホスト ビュー|オブジェクトの種類と、アドインと通信するために使用されるメソッドのホスト アプリケーションのビューを表します。 [ホスト] ビューは、抽象基本クラスまたはインターフェイスです。|  
|ホスト側アダプター|メソッドとの間のコントラクトを対応する 1 つまたは複数のクラスがアセンブリ。<br /><br /> 使用してこのパイプライン セグメントが識別される、<xref:System.AddIn.Pipeline.HostAdapterAttribute>属性。<br /><br /> マルチ モジュール アセンブリはサポートされていません。|  
|コントラクト|派生したインターフェイス、<xref:System.AddIn.Contract.IContract>インターフェイスを定義する、ホストとそのアドインの間での型との通信用プロトコルです。<br /><br /> このパイプライン セグメントが設定によって識別される、<xref:System.AddIn.Pipeline.AddInContractAttribute>属性。|  
|追加側アダプター|メソッドとの間のコントラクトを対応する 1 つまたは複数のクラスがアセンブリ。<br /><br /> 使用してこのパイプライン セグメントが識別される、<xref:System.AddIn.Pipeline.AddInAdapterAttribute>属性。<br /><br /> 各アセンブリを持つ型を含む追加側アダプターのディレクトリに、<xref:System.AddIn.Pipeline.AddInAdapterAttribute>属性がアドインのアプリケーション ドメインに読み込まれます。<br /><br /> 追加側ディレクトリの各アセンブリは、独自のアプリケーション ドメインに読み込まれます。<br /><br /> マルチ モジュール アセンブリはサポートされていません|  
|アドインでは、ビュー|アドインのビューのオブジェクトの種類と、ホストと通信するために使用されるメソッドを表すアセンブリ。 アドイン ビューは、抽象基本クラスまたはインターフェイスです。<br /><br /> 使用してこのパイプライン セグメントが識別される、<xref:System.AddIn.Pipeline.AddInBaseAttribute>属性。<br /><br /> 各アセンブリを持つ型を含む AddInViews ディレクトリに、<xref:System.AddIn.Pipeline.AddInBaseAttribute>属性がアドインのアプリケーション ドメインに読み込まれます。|  
|アドイン|ホストのサービスを実行する型のインスタンス。|  
  
## <a name="pipeline-activation-path"></a>パイプラインのアクティブ化のパス  
 次の図は、アドインがアクティブになる型のアクティブ化を示します。 オブジェクトを渡すことは、計算、またはオブジェクトのコレクションの結果などのホストも示しています。 これは、最も一般的なシナリオです。  
  
 ![追加 (& a) #45; アクティブ化パスを持つモデルをします。] (../../../docs/framework/add-ins/media/addin6.png "AddIn6")  
アドインからホストへのアクティブ化パス  
  
 パイプラインのアクティブ化のパスは次のようです。  
  
1.  ホスト アプリケーションがアドインをアクティブ化、<xref:System.AddIn.Hosting.AddInToken.Activate%2A>メソッドです。  
  
2.  アドインでは、追加、表示、追加側アダプター、およびコントラクト アセンブリは、アドインのアプリケーション ドメインに読み込まれます。  
  
3.  追加のビューを使用して追加側アダプターのインスタンスを作成 (で識別されるクラスを使用した、<xref:System.AddIn.Pipeline.AddInBaseAttribute>属性)、コンス トラクターとして。 アドイン側アダプターは、コントラクトから継承します。  
  
4.  コントラクトとして型指定された、追加側アダプターは、ホスト側アダプターのコンス トラクターには (省略可能) の分離の境界を越えて渡されます。  
  
5.  アドインで、ホスト側アダプター、およびコントラクト アセンブリのホスト ビューは、ホストのアプリケーション ドメインに読み込まれます。  
  
6.  ホスト側のアダプターのインスタンスを作成するには、コントラクトのコンス トラクターとして使用されます。 ホスト側のアダプターは、アドインのホスト ビューから継承します。  
  
7.  アドインをホストは、アドインの表示し、メソッドの呼び出しを続行できますとして型指定されているホストがあります。  
  
## <a name="walkthroughs"></a>チュートリアル  
 Visual Studio を使用してパイプラインを作成する方法を説明する 3 つのチュートリアル トピックがあります。  
  
-   [チュートリアル: 拡張性のあるアプリケーションの作成](../../../docs/framework/add-ins/walkthrough-create-extensible-app.md)  
  
     ホストの加算、減算、乗算、および除算を実行する電卓アドインについて説明します。  
  
-   [チュートリアル: ホスト変更時の旧バージョンとの互換性を有効にします。](http://msdn.microsoft.com/en-us/6fa15bb5-8f04-407d-bd7d-675dc043c848)  
  
     電卓アドイン、強化された計算の機能と、初めて電卓アドインとの互換性を維持する方法について説明します。  
  
-   [チュートリアル: アドインとホスト間でのコレクションの受け渡し](http://msdn.microsoft.com/en-us/b532c604-548e-4fab-b11c-377257dd0ee5)  
  
     書店のシナリオを使用してパイプライン経由でデータ コレクションを渡す方法について説明します。  
  
## <a name="see-also"></a>関連項目  
 [アドイン パイプラインのシナリオ](http://msdn.microsoft.com/en-us/feb70e0b-8734-494c-aeaf-b567f014043e)  
 [アドインおよび拡張機能](../../../docs/framework/add-ins/index.md)