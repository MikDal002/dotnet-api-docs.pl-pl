### <a name="some-workflow-drag-and-drop-apis-are-obsolete"></a><span data-ttu-id="c0cdc-101">Niektórych interfejsów API przeciągania i upuszczania przepływu pracy są nieaktualne</span><span class="sxs-lookup"><span data-stu-id="c0cdc-101">Some WorkFlow drag-and-drop APIs are obsolete</span></span>

|   |   |
|---|---|
|<span data-ttu-id="c0cdc-102">Szczegóły</span><span class="sxs-lookup"><span data-stu-id="c0cdc-102">Details</span></span>|<span data-ttu-id="c0cdc-103">Ten interfejs API przeciągania i upuszczania przepływu pracy jest przestarzały i jeśli aplikacja zostanie odtworzony przed 4.5 spowoduje ostrzeżeń kompilatora.</span><span class="sxs-lookup"><span data-stu-id="c0cdc-103">This WorkFlow drag-and-drop API is obsolete and will cause compiler warnings if the app is rebuilt against 4.5.</span></span>|
|<span data-ttu-id="c0cdc-104">Sugestia</span><span class="sxs-lookup"><span data-stu-id="c0cdc-104">Suggestion</span></span>|<span data-ttu-id="c0cdc-105">Nowe <xref:System.Activities.Presentation.DragDropHelper?displayProperty=name> interfejsów API, która obsługuje operacje z wielu obiektów należy użyć.</span><span class="sxs-lookup"><span data-stu-id="c0cdc-105">New <xref:System.Activities.Presentation.DragDropHelper?displayProperty=name> APIs that support operations with multiple objects should be used instead.</span></span> <span data-ttu-id="c0cdc-106">Alternatywnie można pominąć ostrzeżenia kompilacji lub można uniknąć za pomocą starszego kompilatora.</span><span class="sxs-lookup"><span data-stu-id="c0cdc-106">Alternatively, the build warnings can be suppressed or they can be avoided by using an older compiler.</span></span> <span data-ttu-id="c0cdc-107">Interfejsy API są wciąż obsługiwane.</span><span class="sxs-lookup"><span data-stu-id="c0cdc-107">The APIs are still supported.</span></span>|
|<span data-ttu-id="c0cdc-108">Zakres</span><span class="sxs-lookup"><span data-stu-id="c0cdc-108">Scope</span></span>|<span data-ttu-id="c0cdc-109">Pomocnicza</span><span class="sxs-lookup"><span data-stu-id="c0cdc-109">Minor</span></span>|
|<span data-ttu-id="c0cdc-110">Wersja</span><span class="sxs-lookup"><span data-stu-id="c0cdc-110">Version</span></span>|<span data-ttu-id="c0cdc-111">4.5</span><span class="sxs-lookup"><span data-stu-id="c0cdc-111">4.5</span></span>|
|<span data-ttu-id="c0cdc-112">Typ</span><span class="sxs-lookup"><span data-stu-id="c0cdc-112">Type</span></span>|<span data-ttu-id="c0cdc-113">Przekierowania</span><span class="sxs-lookup"><span data-stu-id="c0cdc-113">Retargeting</span></span>|
|<span data-ttu-id="c0cdc-114">Dotyczy interfejsów API</span><span class="sxs-lookup"><span data-stu-id="c0cdc-114">Affected APIs</span></span>|<ul><li><xref:System.Activities.Presentation.DragDropHelper.DoDragMove(System.Activities.Presentation.WorkflowViewElement,System.Windows.Point)?displayProperty=nameWithType></li><li><xref:System.Activities.Presentation.DragDropHelper.GetCompositeView(System.Windows.DragEventArgs)?displayProperty=nameWithType></li><li><xref:System.Activities.Presentation.DragDropHelper.GetDraggedModelItem(System.Windows.DragEventArgs)?displayProperty=nameWithType></li><li><xref:System.Activities.Presentation.DragDropHelper.GetDroppedObject(System.Windows.DependencyObject,System.Windows.DragEventArgs,System.Activities.Presentation.EditingContext)?displayProperty=nameWithType></li></ul>|
