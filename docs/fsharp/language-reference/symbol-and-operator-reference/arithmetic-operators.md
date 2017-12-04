---
title: "算術演算子 (F#)"
description: "F# のプログラミング言語で使用可能な算術演算子について説明します。"
keywords: "visual f#, f#, 関数型プログラミング"
author: cartermp
ms.author: phcart
ms.date: 05/16/2016
ms.topic: language-reference
ms.prod: .net
ms.technology: devlang-fsharp
ms.devlang: fsharp
ms.assetid: 75ddcfa3-564e-4382-80a3-f9da73d0f0ea
ms.openlocfilehash: 237b97c24f207b3a9b4661d66f029f1b18b8fec7
ms.sourcegitcommit: bd1ef61f4bb794b25383d3d72e71041a5ced172e
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 10/18/2017
---
# <a name="arithmetic-operators"></a>算術演算子

このトピックでは、f# 言語で使用可能な算術演算子について説明します。

## <a name="summary-of-binary-arithmetic-operators"></a>二項算術演算子の概要
次の表は、ボックス化解除された整数型および浮動小数点型で利用可能なバイナリの算術演算子をまとめたものです。

|二項演算子|ノート|
|---------------|-----|
|`+`(さらに、プラス)|オンになっていません。 数値が一緒に追加するときに、オーバーフローが発生し、合計型によってサポートされている最大の絶対値を超えています。|
|`-`(減算、マイナス記号)|オンになっていません。 アンダー フローの条件の型によって表される浮動小数点値が小さすぎる場合または符号なしの型を減算します。|
|`*`(乗算, 時間)|オンになっていません。 番号が乗算されるときに、オーバーフローが発生し、製品の種類でサポート絶対値の最大値を超えています。|
|`/`(除算、)|ゼロ原因による除算、<xref:System.DivideByZeroException>整数型。 浮動小数点型は、0 による除算は、提供する特殊な浮動小数点値`+Infinity`または`-Infinity`です。 アンダー フロー条件の型によって表される浮動小数点数が小さすぎる場合にあります。|
|`%`(剰余、mod)|除算の剰余を返します。 結果の符号は、最初のオペランドの符号と同じです。|
|`**`(のべき乗に累乗)|結果を型の絶対値の最大値を超えた場合に、オーバーフローが発生します。<br /><br />指数演算子は、浮動小数点型でのみ動作します。|

## <a name="summary-of-unary-arithmetic-operators"></a>単項算術演算子の概要
次の表は、整数および浮動小数点型で利用可能な単項算術演算子をまとめたものです。


|単項演算子|ノート|
|--------------|-----|
|`+`(正)|算術式に適用できます。 値の符号は変更されません。|
|`-`(マイナス符号、負の値)|算術式に適用できます。 値の符号を変更します。|
オーバーフローまたはアンダー フローに整数型での動作は、ラップします。 これにより、不適切な結果です。 整数オーバーフローは、ソフトウェアはそのアカウントに書き込まれないときにセキュリティの問題に影響することが可能性がある重大な問題です。 アプリケーションにとって問題になる場合は、チェックの演算子の使用を検討`Microsoft.FSharp.Core.Operators.Checked`です。


## <a name="summary-of-binary-comparison-operators"></a>バイナリの比較演算子の概要
次の表は、整数および浮動小数点型で利用可能な 2 項比較演算子を示します。 これらの演算子は、型の値を返す`bool`です。

浮動小数点数必要がありますしない直接比較されます、等しい IEEE 浮動小数点表現が正確な等価演算をサポートしていないためです。 簡単に、コードを調べることによって同等であることを確認できます 2 つの数値は、別のビット表現を実際にがあります。



|演算子|ノート|
|--------|-----|
|`=`(等値を代入)|これは、代入演算子ではありません。 比較のためにのみ使用されます。 これは、一般的な演算子です。|
|`>`(より大きい)|これは、一般的な演算子です。|
|`<`(より小さい)|これは、一般的な演算子です。|
|`>=`(より大きいまたは等しい)|これは、一般的な演算子です。|
|`<=`(より小さいまたは等しい)|これは、一般的な演算子です。|
|`<>`(等しくない)|これは、一般的な演算子です。|

## <a name="overloaded-and-generic-operators"></a>演算子のオーバー ロードされたとジェネリック
このトピックで説明した演算子のすべてで定義されて、 **Microsoft.FSharp.Core.Operators**名前空間。 一部の操作は、静的に解決される型パラメーターを使用して定義されます。 これは、演算子で使用する特定の種類ごとに個別の定義があることを意味します。 このカテゴリのすべての単項および二項算術演算子とビットごとの演算子です。 比較演算子は、汎用し、したがっていないだけプリミティブ数値型、任意の型を処理します。 判別共用体およびレコード型、f# コンパイラによって生成される、独自のカスタム実装があります。 クラス型、メソッドを使用して<xref:System.Object.Equals%2A>です。

ジェネリックの演算子は、カスタマイズできます。 比較関数をカスタマイズする上書き<xref:System.Object.Equals%2A>独自のカスタムの等値比較を提供し、実装に<xref:System.IComparable>です。 <xref:System.IComparable?displayProperty=nameWithType>インターフェイスが 1 つのメソッドには、<xref:System.IComparable.CompareTo%2A>メソッドです。


## <a name="operators-and-type-inference"></a>演算子と型の推論
式の中で演算子の使用は、その演算子に型の推論を制約します。 また、演算子の使用は、演算子の使用は数値型を意味するため、自動汎化を防止します。 その他の情報がない場合は、f# コンパイラが推論`int`算術式の型として。 この動作をオーバーライドするには、別の型を指定します。 したがって、引数の型と戻り値の型`function1`次のコードと推論されます`int`の型にも`function2`と推論されます`float`です。

[!code-fsharp[Main](../../../../samples/snippets/fsharp/lang-ref-1/snippet3501.fs)]
    
## <a name="see-also"></a>関連項目
[シンボルと演算子のリファレンス](index.md)

[演算子のオーバーロード](../operator-overloading.md)

[ビット処理演算子](bitwise-operators.md)

[ブール演算子](boolean-operators.md)