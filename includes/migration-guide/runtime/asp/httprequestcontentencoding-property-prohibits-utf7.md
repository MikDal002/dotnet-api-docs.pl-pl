### <a name="httprequestcontentencoding-property-prohibits-utf7"></a><span data-ttu-id="67ed0-101">Właściwość HttpRequest.ContentEncoding zabrania UTF7</span><span class="sxs-lookup"><span data-stu-id="67ed0-101">HttpRequest.ContentEncoding property prohibits UTF7</span></span>

|   |   |
|---|---|
|<span data-ttu-id="67ed0-102">Szczegóły</span><span class="sxs-lookup"><span data-stu-id="67ed0-102">Details</span></span>|<span data-ttu-id="67ed0-103">Począwszy od programu .NET Framework 4.5, kodowania UTF-7 jest zabronione w <xref:System.Web.HttpRequest?displayProperty=name>s "treści.</span><span class="sxs-lookup"><span data-stu-id="67ed0-103">Beginning in .NET Framework 4.5, UTF-7 encoding is prohibited in <xref:System.Web.HttpRequest?displayProperty=name>s' bodies.</span></span> <span data-ttu-id="67ed0-104">Dane dla aplikacji, które zależą od danych przychodzących w formacie UTF-7, nie będą poprawnie dekodowane w niektórych przypadkach.</span><span class="sxs-lookup"><span data-stu-id="67ed0-104">Data for applications that depend on incoming UTF-7 data will not decode properly in some cases.</span></span>|
|<span data-ttu-id="67ed0-105">Sugestia</span><span class="sxs-lookup"><span data-stu-id="67ed0-105">Suggestion</span></span>|<span data-ttu-id="67ed0-106">Najlepiej, jeśli aplikacje powinien zostać zaktualizowany w taki sposób, aby nie używać UTF-7 kodowanie w <xref:System.Web.HttpRequest?displayProperty=name>s.</span><span class="sxs-lookup"><span data-stu-id="67ed0-106">Ideally, applications should be updated to not use UTF-7 encoding in <xref:System.Web.HttpRequest?displayProperty=name>s.</span></span> <span data-ttu-id="67ed0-107">Alternatywnie można przywracać starsze zachowanie przy użyciu <code>aspnet:AllowUtf7RequestContentEncoding</code> atrybutu [appSettings](https://msdn.microsoft.com/library/hh975440(v=vs.110).aspx) elementu.</span><span class="sxs-lookup"><span data-stu-id="67ed0-107">Alternatively, legacy behavior can be restored by using the <code>aspnet:AllowUtf7RequestContentEncoding</code> attribute of the [appSettings](https://msdn.microsoft.com/library/hh975440(v=vs.110).aspx) element.</span></span>|
|<span data-ttu-id="67ed0-108">Zakres</span><span class="sxs-lookup"><span data-stu-id="67ed0-108">Scope</span></span>|<span data-ttu-id="67ed0-109">Krawędź</span><span class="sxs-lookup"><span data-stu-id="67ed0-109">Edge</span></span>|
|<span data-ttu-id="67ed0-110">Wersja</span><span class="sxs-lookup"><span data-stu-id="67ed0-110">Version</span></span>|<span data-ttu-id="67ed0-111">4.5</span><span class="sxs-lookup"><span data-stu-id="67ed0-111">4.5</span></span>|
|<span data-ttu-id="67ed0-112">Typ</span><span class="sxs-lookup"><span data-stu-id="67ed0-112">Type</span></span>|<span data-ttu-id="67ed0-113">Środowisko uruchomieniowe</span><span class="sxs-lookup"><span data-stu-id="67ed0-113">Runtime</span></span>|
|<span data-ttu-id="67ed0-114">Dotyczy interfejsów API</span><span class="sxs-lookup"><span data-stu-id="67ed0-114">Affected APIs</span></span>|<ul><li><xref:System.Web.HttpRequest.ContentEncoding?displayProperty=nameWithType></li></ul>|
