### <a name="workflowdesignerload-doesnt-remove-symbol-property"></a><span data-ttu-id="83e14-101">WorkflowDesigner.Load nie powoduje usunięcia właściwość symbol</span><span class="sxs-lookup"><span data-stu-id="83e14-101">WorkflowDesigner.Load doesn't remove symbol property</span></span>

|   |   |
|---|---|
|<span data-ttu-id="83e14-102">Szczegóły</span><span class="sxs-lookup"><span data-stu-id="83e14-102">Details</span></span>|<span data-ttu-id="83e14-103">Podczas określania wartości docelowej platformy .NET Framework 4.5 w Projektancie przepływów pracy i ładowanie ponownie hostowanej 3,5 przepływu pracy z <xref:System.Activities.Presentation.WorkflowDesigner.Load> metody <xref:System.Xaml.XamlDuplicateMemberException?displayProperty=name> jest generowany podczas zapisywania przepływ pracy.</span><span class="sxs-lookup"><span data-stu-id="83e14-103">When targeting the .NET Framework 4.5 in the workflow designer, and loading a re-hosted 3.5 workflow with the <xref:System.Activities.Presentation.WorkflowDesigner.Load> method, a <xref:System.Xaml.XamlDuplicateMemberException?displayProperty=name> is thrown while saving the workflow.</span></span>|
|<span data-ttu-id="83e14-104">Sugestia</span><span class="sxs-lookup"><span data-stu-id="83e14-104">Suggestion</span></span>|<span data-ttu-id="83e14-105">Ta usterka tylko w sytuacji, gdy przeznaczonych dla platformy .NET Framework 4.5 w Projektancie przepływów pracy, dlatego może być działał wokół przez ustawienie <code>WorkflowDesigner.Context.Services.GetService&lt;DesignerConfigurationService&gt;().TargetFrameworkName</code> do 4.0 .NET Framework.Alternatively, można uniknąć problemu, przy użyciu <xref:System.Activities.Presentation.WorkflowDesigner.Load(System.String)> metody w celu załadowania przepływu pracy, zamiast <xref:System.Activities.Presentation.WorkflowDesigner.Load>.</span><span class="sxs-lookup"><span data-stu-id="83e14-105">This bug only manifests when targeting .NET Framework 4.5 in the workflow designer, so it can be worked around by setting the <code>WorkflowDesigner.Context.Services.GetService&lt;DesignerConfigurationService&gt;().TargetFrameworkName</code> to the 4.0 .NET Framework.Alternatively, the issue may be avoided by using the <xref:System.Activities.Presentation.WorkflowDesigner.Load(System.String)> method to load the workflow, instead of <xref:System.Activities.Presentation.WorkflowDesigner.Load>.</span></span>|
|<span data-ttu-id="83e14-106">Zakres</span><span class="sxs-lookup"><span data-stu-id="83e14-106">Scope</span></span>|<span data-ttu-id="83e14-107">Główne</span><span class="sxs-lookup"><span data-stu-id="83e14-107">Major</span></span>|
|<span data-ttu-id="83e14-108">Wersja</span><span class="sxs-lookup"><span data-stu-id="83e14-108">Version</span></span>|<span data-ttu-id="83e14-109">4.5</span><span class="sxs-lookup"><span data-stu-id="83e14-109">4.5</span></span>|
|<span data-ttu-id="83e14-110">Typ</span><span class="sxs-lookup"><span data-stu-id="83e14-110">Type</span></span>|<span data-ttu-id="83e14-111">Przekierowania</span><span class="sxs-lookup"><span data-stu-id="83e14-111">Retargeting</span></span>|
|<span data-ttu-id="83e14-112">Dotyczy interfejsów API</span><span class="sxs-lookup"><span data-stu-id="83e14-112">Affected APIs</span></span>|<ul><li><xref:System.Activities.Presentation.WorkflowDesigner.Load?displayProperty=nameWithType></li></ul>|
