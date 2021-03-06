---
title: 構造体メンバーとして宣言された配列を初期サイズで宣言することはできません。
ms.date: 07/20/2015
f1_keywords:
- vbc31043
- bc31043
helpviewer_keywords:
- BC31043
ms.assetid: 5bd90c71-1b78-444b-91e1-4789451ef085
ms.openlocfilehash: 06e5e36f3e0522e0449c0ef9698f3a1b01b9cb5f
ms.sourcegitcommit: 6b308cf6d627d78ee36dbbae8972a310ac7fd6c8
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 01/23/2019
ms.locfileid: "54549068"
---
# <a name="arrays-declared-as-structure-members-cannot-be-declared-with-an-initial-size"></a>構造体メンバーとして宣言された配列を初期サイズで宣言することはできません。
構造体の配列は、初期サイズで宣言されます。 構造体の要素を初期化することはできませんし、初期化の 1 つの形式は、配列のサイズを宣言します。  
  
 **エラー ID:** BC31043  
  
## <a name="to-correct-this-error"></a>このエラーを解決するには  
  
1.  動的 (初期サイズはありません)、構造体の配列を定義します。  
  
2.  動的配列のディメンションを変更できる配列の特定のサイズを必要とする場合、 [ReDim ステートメント](../../../visual-basic/language-reference/statements/redim-statement.md)コードが実行されています。 次に例を示します。  
  
    ```  
    Structure demoStruct  
        Public demoArray() As Integer  
    End Structure  
    Sub useStruct()  
        Dim struct As demoStruct  
        ReDim struct.demoArray(9)  
        Struct.demoArray(2) = 777  
    End Sub  
    ```  
  
## <a name="see-also"></a>関連項目
- [配列](../../../visual-basic/programming-guide/language-features/arrays/index.md)
- [方法: 構造体を宣言する](../../../visual-basic/programming-guide/language-features/data-types/how-to-declare-a-structure.md)
