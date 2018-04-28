### <a name="listboxitem-isselected-binding-issue-with-observablecollectionlttgtmove"></a><span data-ttu-id="079c4-101">ObservableCollection&lt;T&gt;.Move に対する ListBoxItem IsSelected のバインディングの問題</span><span class="sxs-lookup"><span data-stu-id="079c4-101">ListBoxItem IsSelected binding issue with ObservableCollection&lt;T&gt;.Move</span></span>

|   |   |
|---|---|
|<span data-ttu-id="079c4-102">説明</span><span class="sxs-lookup"><span data-stu-id="079c4-102">Details</span></span>|<span data-ttu-id="079c4-103">項目が選択された <xref:System.Windows.Controls.ListBox?displayProperty=name> にバインドされるコレクションで <xref:System.Collections.ObjectModel.ObservableCollection%601.Move(System.Int32,System.Int32)> または <xref:System.Collections.ObjectModel.ObservableCollection%601.MoveItem(System.Int32,System.Int32)> を呼び出すと、<xref:System.Windows.Controls.ListBox?displayProperty=name> 項目の今後の選択または選択解除で不規則な動作が発生する可能性があります。</span><span class="sxs-lookup"><span data-stu-id="079c4-103">Calling <xref:System.Collections.ObjectModel.ObservableCollection%601.Move(System.Int32,System.Int32)> or <xref:System.Collections.ObjectModel.ObservableCollection%601.MoveItem(System.Int32,System.Int32)> on a collection bound to a <xref:System.Windows.Controls.ListBox?displayProperty=name> with items selected can lead to erratic behavior with future selection or unselection of <xref:System.Windows.Controls.ListBox?displayProperty=name> items.</span></span>|
|<span data-ttu-id="079c4-104">提案される解決策</span><span class="sxs-lookup"><span data-stu-id="079c4-104">Suggestion</span></span>|<span data-ttu-id="079c4-105"><xref:System.Collections.ObjectModel.ObservableCollection%601.Move(System.Int32,System.Int32)> ではなく <xref:System.Collections.ObjectModel.Collection%601.Remove(%600)?displayProperty=name> と <xref:System.Collections.ObjectModel.Collection%601.Insert(System.Int32,%600)?displayProperty=name> を呼び出すことで、この問題は解決されます。</span><span class="sxs-lookup"><span data-stu-id="079c4-105">Calling <xref:System.Collections.ObjectModel.Collection%601.Remove(%600)?displayProperty=name> and <xref:System.Collections.ObjectModel.Collection%601.Insert(System.Int32,%600)?displayProperty=name> instead of <xref:System.Collections.ObjectModel.ObservableCollection%601.Move(System.Int32,System.Int32)> will work around this issue.</span></span> <span data-ttu-id="079c4-106">または、この問題は .NET Framework 4.6 で修正されたため、このバージョンの .NET Framework にアップグレードすることによって対処できます。</span><span class="sxs-lookup"><span data-stu-id="079c4-106">Alternatively, this issue has been fixed in the .NET Framework 4.6 and may be addressed by upgrading to that version of the .NET Framework.</span></span>|
|<span data-ttu-id="079c4-107">スコープ</span><span class="sxs-lookup"><span data-stu-id="079c4-107">Scope</span></span>|<span data-ttu-id="079c4-108">マイナー</span><span class="sxs-lookup"><span data-stu-id="079c4-108">Minor</span></span>|
|<span data-ttu-id="079c4-109">Version</span><span class="sxs-lookup"><span data-stu-id="079c4-109">Version</span></span>|<span data-ttu-id="079c4-110">4.5</span><span class="sxs-lookup"><span data-stu-id="079c4-110">4.5</span></span>|
|<span data-ttu-id="079c4-111">型</span><span class="sxs-lookup"><span data-stu-id="079c4-111">Type</span></span>|<span data-ttu-id="079c4-112">ランタイム</span><span class="sxs-lookup"><span data-stu-id="079c4-112">Runtime</span></span>|
|<span data-ttu-id="079c4-113">影響を受ける API</span><span class="sxs-lookup"><span data-stu-id="079c4-113">Affected APIs</span></span>|<ul><li><xref:System.Collections.ObjectModel.ObservableCollection%601.Move(System.Int32,System.Int32)?displayProperty=nameWithType></li><li><xref:System.Collections.ObjectModel.ObservableCollection%601.MoveItem(System.Int32,System.Int32)?displayProperty=nameWithType></li></ul>|
