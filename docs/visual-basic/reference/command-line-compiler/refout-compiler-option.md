---
title: refout (Visual Basic)
ms.date: 03/16/2018
ms.prod: .net
ms.technology:
- devlang-visual-basic
ms.topic: article
f1_keywords:
- /refout
helpviewer_keywords:
- refout compiler option [Visual Basic]
- /refout compiler option [Visual Basic]
- -refout compiler option [Visual Basic]
author: rpetrusha
ms.author: ronpet
ms.openlocfilehash: d6075b92efd1eec9797fca248e97a325bd5df4bb
ms.sourcegitcommit: c883637b41ee028786edceece4fa872939d2e64c
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 03/23/2018
---
# <a name="-refout-visual-basic"></a><span data-ttu-id="79df9-102">refout (Visual Basic)</span><span class="sxs-lookup"><span data-stu-id="79df9-102">-refout (Visual Basic)</span></span>

<span data-ttu-id="79df9-103">**-refout** オプションは、参照アセンブリを出力するファイル パスを指定します。</span><span class="sxs-lookup"><span data-stu-id="79df9-103">The **-refout** option specifies a file path where the reference assembly should be output.</span></span>

[!INCLUDE[compiler-options](~/includes/compiler-options.md)]

## <a name="syntax"></a><span data-ttu-id="79df9-104">構文</span><span class="sxs-lookup"><span data-stu-id="79df9-104">Syntax</span></span>

```console
-refout:filepath
```

## <a name="arguments"></a><span data-ttu-id="79df9-105">引数</span><span class="sxs-lookup"><span data-stu-id="79df9-105">Arguments</span></span>

 <span data-ttu-id="79df9-106">`filepath` パスと、参照アセンブリのファイル名。</span><span class="sxs-lookup"><span data-stu-id="79df9-106">`filepath` The path and filename of the reference assembly.</span></span> <span data-ttu-id="79df9-107">プライマリのアセンブリのサブ フォルダーで一般的になります。</span><span class="sxs-lookup"><span data-stu-id="79df9-107">It should generally be in a sub-folder of the primary assembly.</span></span> <span data-ttu-id="79df9-108">(MSBuild で使用される) 推奨規則は、プライマリ アセンブリに相対する "ref/" サブ フォルダー内に参照アセンブリを配置することです。</span><span class="sxs-lookup"><span data-stu-id="79df9-108">The recommended convention (used by MSBuild) is to place the reference assembly in a "ref/" sub-folder relative to the primary assembly.</span></span> <span data-ttu-id="79df9-109">すべてのフォルダー`filepath`が存在する必要があります。 コンパイラは作成されません。</span><span class="sxs-lookup"><span data-stu-id="79df9-109">All folders in `filepath` must exist; the compiler does not create them.</span></span> 

## <a name="remarks"></a><span data-ttu-id="79df9-110">コメント</span><span class="sxs-lookup"><span data-stu-id="79df9-110">Remarks</span></span>

<span data-ttu-id="79df9-111">Visual Basic のサポート、`-refout`バージョン 15.3 と開始を切り替えます。</span><span class="sxs-lookup"><span data-stu-id="79df9-111">Visual Basic supports the `-refout` switch starting with version 15.3.</span></span>

<span data-ttu-id="79df9-112">参照アセンブリはメタデータ コードではなく実装が含まれているメタデータのみのアセンブリです。</span><span class="sxs-lookup"><span data-stu-id="79df9-112">Reference assemblies are metadata-only assemblies that contain metadata but no implementation code.</span></span> <span data-ttu-id="79df9-113">匿名型を除くすべての型およびメンバーの情報が含まれます。</span><span class="sxs-lookup"><span data-stu-id="79df9-113">They include type and member information for everything except anonymous types.</span></span> <span data-ttu-id="79df9-114">メソッドの本体は、1 つに置き換えられます`throw null`ステートメントです。</span><span class="sxs-lookup"><span data-stu-id="79df9-114">Their method bodies are replaced with a single `throw null` statement.</span></span> <span data-ttu-id="79df9-115">使用する理由`throw null`(本文のない) ではなく、メソッド本体が PEVerify を実行して (したがって、メタデータの完全性を検証する) を通過できるようにします。</span><span class="sxs-lookup"><span data-stu-id="79df9-115">The reason for using `throw null` method bodies (as opposed to no bodies) is so that PEVerify can run and pass (thus validating the completeness of the metadata).</span></span>

<span data-ttu-id="79df9-116">参照アセンブリは、アセンブリ レベル[ReferenceAssembly](xref:System.Runtime.CompilerServices.ReferenceAssemblyAttribute)属性。</span><span class="sxs-lookup"><span data-stu-id="79df9-116">Reference assemblies include an assembly-level [ReferenceAssembly](xref:System.Runtime.CompilerServices.ReferenceAssemblyAttribute) attribute.</span></span> <span data-ttu-id="79df9-117">この属性は、ソースで指定できます (指定すると、コンパイラではこれを合成する必要がなくなります)。</span><span class="sxs-lookup"><span data-stu-id="79df9-117">This attribute may be specified in source (then the compiler won't need to synthesize it).</span></span> <span data-ttu-id="79df9-118">この属性のためのランタイムを実行するための参照アセンブリを読み込む拒否する (ただしリフレクション専用コンテキストに読み込まれていることができます)。</span><span class="sxs-lookup"><span data-stu-id="79df9-118">Because of this attribute, runtimes refuse to load reference assemblies for execution (but they can still be loaded in a reflection-only context).</span></span> <span data-ttu-id="79df9-119">アセンブリに反映するためのツールは、リフレクション専用として参照アセンブリが読み込まれることを確認する必要があります。それ以外の場合、ランタイム、<xref:System.BadImageFormatException>です。</span><span class="sxs-lookup"><span data-stu-id="79df9-119">Tools that reflect on assemblies need to ensure they load reference assemblies as reflection-only; otherwise, the runtime throws a <xref:System.BadImageFormatException>.</span></span>

<span data-ttu-id="79df9-120">`-refout` オプションと [`-refonly`](refonly-compiler-option.md) オプションは同時に指定できません。</span><span class="sxs-lookup"><span data-stu-id="79df9-120">The `-refout` and [`-refonly`](refonly-compiler-option.md) options are mutually exclusive.</span></span>

## <a name="see-also"></a><span data-ttu-id="79df9-121">関連項目</span><span class="sxs-lookup"><span data-stu-id="79df9-121">See Also</span></span>
<span data-ttu-id="79df9-122">[-refonly](refonly-compiler-option.md) </span><span class="sxs-lookup"><span data-stu-id="79df9-122">[-refonly](refonly-compiler-option.md) </span></span>  
[<span data-ttu-id="79df9-123">Visual Basic のコマンド ライン コンパイラ</span><span class="sxs-lookup"><span data-stu-id="79df9-123">Visual Basic Command-Line Compiler</span></span>](index.md)  
[<span data-ttu-id="79df9-124">コンパイル コマンド ラインのサンプル</span><span class="sxs-lookup"><span data-stu-id="79df9-124">Sample Compilation Command Lines</span></span>](sample-compilation-command-lines.md)  
