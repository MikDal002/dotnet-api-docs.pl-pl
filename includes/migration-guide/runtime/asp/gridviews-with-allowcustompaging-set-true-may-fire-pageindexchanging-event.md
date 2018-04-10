### <a name="gridviews-with-allowcustompaging-set-to-true-may-fire-the-pageindexchanging-event-when-leaving-the-final-page-of-the-view"></a><span data-ttu-id="c5904-101">GridViews z Wartość AllowCustomPaging o wartości true może wyzwalać zdarzeń PageIndexChanging podczas opuszczania ostatnia strona widoku</span><span class="sxs-lookup"><span data-stu-id="c5904-101">GridViews with AllowCustomPaging set to true may fire the PageIndexChanging event when leaving the final page of the view</span></span>

|   |   |
|---|---|
|<span data-ttu-id="c5904-102">Szczegóły</span><span class="sxs-lookup"><span data-stu-id="c5904-102">Details</span></span>|<span data-ttu-id="c5904-103">Powoduje usterki w programie .NET Framework 4.5 <xref:System.Web.UI.WebControls.GridView.PageIndexChanging?displayProperty=name> czasami nie uruchomienie dla <xref:System.Web.UI.WebControls.GridView?displayProperty=name>, które mają włączone <xref:System.Web.UI.WebControls.GridView.AllowCustomPaging?displayProperty=name>.</span><span class="sxs-lookup"><span data-stu-id="c5904-103">A bug in the .NET Framework 4.5 causes <xref:System.Web.UI.WebControls.GridView.PageIndexChanging?displayProperty=name> to sometimes not fire for <xref:System.Web.UI.WebControls.GridView?displayProperty=name>s that have enabled <xref:System.Web.UI.WebControls.GridView.AllowCustomPaging?displayProperty=name>.</span></span>|
|<span data-ttu-id="c5904-104">Sugestia</span><span class="sxs-lookup"><span data-stu-id="c5904-104">Suggestion</span></span>|<span data-ttu-id="c5904-105">Ten problem został rozwiązany w .NET Framework 4.6 i mogą być kierowane przez uaktualnienie do tej wersji programu .NET Framework.</span><span class="sxs-lookup"><span data-stu-id="c5904-105">This issue has been fixed in the .NET Framework 4.6 and may be addressed by upgrading to that version of the .NET Framework.</span></span> <span data-ttu-id="c5904-106">Jako obejście, aplikację można wykonać jawne BindGrid na dowolnym <code>Page_Load</code> który czy trafień tych warunków ( <xref:System.Web.UI.WebControls.GridView?displayProperty=name> jest na ostatniej stronie i ostatnich<xref:System.Web.UI.WebControls.GridView.PageSize?displayProperty=name> różni się od <xref:System.Web.UI.WebControls.GridView.PageSize?displayProperty=name>).</span><span class="sxs-lookup"><span data-stu-id="c5904-106">As a work-around, the app can do an explicit BindGrid on any <code>Page_Load</code> that would hit these conditions (the <xref:System.Web.UI.WebControls.GridView?displayProperty=name> is on the last page and Last<xref:System.Web.UI.WebControls.GridView.PageSize?displayProperty=name> is different from <xref:System.Web.UI.WebControls.GridView.PageSize?displayProperty=name>).</span></span> <span data-ttu-id="c5904-107">Alternatywnie aplikacji można zmodyfikować umożliwia stronicowania (zamiast stronicowania niestandardowego), w tym scenariuszu nie przedstawiać problemu.</span><span class="sxs-lookup"><span data-stu-id="c5904-107">Alternatively, the app can be modified to allow paging (instead of custom paging), as that scenario does not demonstrate the problem.</span></span>|
|<span data-ttu-id="c5904-108">Zakres</span><span class="sxs-lookup"><span data-stu-id="c5904-108">Scope</span></span>|<span data-ttu-id="c5904-109">Pomocnicza</span><span class="sxs-lookup"><span data-stu-id="c5904-109">Minor</span></span>|
|<span data-ttu-id="c5904-110">Wersja</span><span class="sxs-lookup"><span data-stu-id="c5904-110">Version</span></span>|<span data-ttu-id="c5904-111">4.5</span><span class="sxs-lookup"><span data-stu-id="c5904-111">4.5</span></span>|
|<span data-ttu-id="c5904-112">Typ</span><span class="sxs-lookup"><span data-stu-id="c5904-112">Type</span></span>|<span data-ttu-id="c5904-113">Środowisko uruchomieniowe</span><span class="sxs-lookup"><span data-stu-id="c5904-113">Runtime</span></span>|
|<span data-ttu-id="c5904-114">Dotyczy interfejsów API</span><span class="sxs-lookup"><span data-stu-id="c5904-114">Affected APIs</span></span>|<ul><li><xref:System.Web.UI.WebControls.GridView.AllowCustomPaging?displayProperty=nameWithType></li></ul>|
