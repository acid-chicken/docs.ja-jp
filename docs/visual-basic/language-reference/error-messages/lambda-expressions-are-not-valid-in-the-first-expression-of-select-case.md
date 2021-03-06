---
title: ラムダ式は、'Select Case' ステートメントの最初の式では有効ではありません
ms.date: 07/20/2015
f1_keywords:
- bc36635
- vbc36635
helpviewer_keywords:
- BC36635
ms.assetid: 74609979-9c03-4864-bbce-f588aa2e0917
ms.openlocfilehash: d56515093020a4c987d132491957ce6db9e21683
ms.sourcegitcommit: 14355b4b2fe5bcf874cac96d0a9e6376b567e4c7
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 01/30/2019
ms.locfileid: "55287795"
---
# <a name="lambda-expressions-are-not-valid-in-the-first-expression-of-a-select-case-statement"></a>ラムダ式は、'Select Case' ステートメントの最初の式では有効ではありません
テスト式でのラムダ式を使用することはできません、`Select Case`ステートメント。 ラムダ式の定義は、関数、およびのテスト式を返す、`Select Case`ステートメントは、基本データ型である必要があります。  
  
 次のコードでは、このエラーが発生します。  
  
```vb  
' Select Case (Function(arg) arg Is Nothing)  
    ' List of the cases.  
' End Select  
```  
  
 **エラー ID:** BC36635  
  
## <a name="to-correct-this-error"></a>このエラーを解決するには  
  
-   コードを調べて、 `If...Then...Else` ステートメントなどの別の条件構造を使用できないかをご確認ください。  
  
-   指定した、関数を呼び出す次のコードに示すように。  
  
```vb  
Dim num? As Integer  
Select Case ((Function(arg? As Integer) arg Is Nothing)(num))  
    ' List of the cases  
End Select  
```  
  
## <a name="see-also"></a>関連項目
- [ラムダ式](../../../visual-basic/programming-guide/language-features/procedures/lambda-expressions.md)
- [If...Then...Else ステートメント](../../../visual-basic/language-reference/statements/if-then-else-statement.md)
- [Select...Case ステートメント](../../../visual-basic/language-reference/statements/select-case-statement.md)
