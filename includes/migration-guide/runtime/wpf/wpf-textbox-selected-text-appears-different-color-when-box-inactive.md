### <a name="wpf-textbox-selected-text-appears-a-different-color-when-the-text-box-is-inactive"></a><span data-ttu-id="19f47-101">WPF TextBox で選択されているテキストが、テキスト ボックスがアクティブでないときに異なる色で表示される</span><span class="sxs-lookup"><span data-stu-id="19f47-101">WPF TextBox selected text appears a different color when the text box is inactive</span></span>

|   |   |
|---|---|
|<span data-ttu-id="19f47-102">説明</span><span class="sxs-lookup"><span data-stu-id="19f47-102">Details</span></span>|<span data-ttu-id="19f47-103">.NET 4.5 では、WPF テキスト ボックス コントロールがアクティブでないとき (フォーカスがないとき)、ボックス内で選択されているテキストは、コントロールがアクティブなときとは別の色で表示されます。</span><span class="sxs-lookup"><span data-stu-id="19f47-103">In .NET 4.5, when a WPF text box control is inactive (it doesn't have focus), the selected text inside the box will appear a different color than when the control is active.</span></span>|
|<span data-ttu-id="19f47-104">提案される解決策</span><span class="sxs-lookup"><span data-stu-id="19f47-104">Suggestion</span></span>|<span data-ttu-id="19f47-105"><xref:System.Windows.FrameworkCompatibilityPreferences.AreInactiveSelectionHighlightBrushKeysSupported> プロパティを <code>false</code> に設定することで、以前 (.NET 4.0) の動作が復元される可能性があります。</span><span class="sxs-lookup"><span data-stu-id="19f47-105">Previous (.NET 4.0) behavior may be restored by setting the <xref:System.Windows.FrameworkCompatibilityPreferences.AreInactiveSelectionHighlightBrushKeysSupported> property to <code>false</code>.</span></span>|
|<span data-ttu-id="19f47-106">スコープ</span><span class="sxs-lookup"><span data-stu-id="19f47-106">Scope</span></span>|<span data-ttu-id="19f47-107">エッジ</span><span class="sxs-lookup"><span data-stu-id="19f47-107">Edge</span></span>|
|<span data-ttu-id="19f47-108">Version</span><span class="sxs-lookup"><span data-stu-id="19f47-108">Version</span></span>|<span data-ttu-id="19f47-109">4.5</span><span class="sxs-lookup"><span data-stu-id="19f47-109">4.5</span></span>|
|<span data-ttu-id="19f47-110">型</span><span class="sxs-lookup"><span data-stu-id="19f47-110">Type</span></span>|<span data-ttu-id="19f47-111">ランタイム</span><span class="sxs-lookup"><span data-stu-id="19f47-111">Runtime</span></span>|
|<span data-ttu-id="19f47-112">影響を受ける API</span><span class="sxs-lookup"><span data-stu-id="19f47-112">Affected APIs</span></span>|<ul><li><xref:System.Windows.Controls.TextBox?displayProperty=nameWithType></li></ul>|
