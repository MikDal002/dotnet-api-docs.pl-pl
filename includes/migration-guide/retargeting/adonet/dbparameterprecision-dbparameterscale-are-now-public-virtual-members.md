### <a name="dbparameterprecision-and-dbparameterscale-are-now-public-virtual-members"></a><span data-ttu-id="3b046-101">DbParameter.Precision i DbParameter.Scale są teraz publicznych wirtualnych elementów członkowskich</span><span class="sxs-lookup"><span data-stu-id="3b046-101">DbParameter.Precision and DbParameter.Scale are now public virtual members</span></span>

|   |   |
|---|---|
|<span data-ttu-id="3b046-102">Szczegóły</span><span class="sxs-lookup"><span data-stu-id="3b046-102">Details</span></span>|<span data-ttu-id="3b046-103"><xref:System.Data.Common.DbParameter.Precision> i <xref:System.Data.Common.DbParameter.Scale> są zaimplementowane jako publiczny właściwości wirtualnych.</span><span class="sxs-lookup"><span data-stu-id="3b046-103"><xref:System.Data.Common.DbParameter.Precision> and <xref:System.Data.Common.DbParameter.Scale> are implemented as public virtual properties.</span></span> <span data-ttu-id="3b046-104">Zastępują one odpowiedniej implementacji interfejsu jawnego <xref:System.Data.Common.DbParameter.System%23Data%23IDbDataParameter%23Precision> i <xref:System.Data.Common.DbParameter.System%23Data%23IDbDataParameter%23Scale>.</span><span class="sxs-lookup"><span data-stu-id="3b046-104">They replace the corresponding explicit interface implementations, <xref:System.Data.Common.DbParameter.System%23Data%23IDbDataParameter%23Precision> and <xref:System.Data.Common.DbParameter.System%23Data%23IDbDataParameter%23Scale>.</span></span>|
|<span data-ttu-id="3b046-105">Sugestia</span><span class="sxs-lookup"><span data-stu-id="3b046-105">Suggestion</span></span>|<span data-ttu-id="3b046-106">Podczas ponownego tworzenia dostawcy bazy danych programu ADO.NET, te różnice wymaga słowa kluczowego "override" ma zostać zastosowany do właściwości Precision i Scale.</span><span class="sxs-lookup"><span data-stu-id="3b046-106">When re-building an ADO.NET database provider, these differences will require the 'override' keyword to be applied to the Precision and Scale properties.</span></span> <span data-ttu-id="3b046-107">Jest to potrzebne tylko wtedy, gdy ponowne utworzenie składników; istniejące pliki binarne będą nadal działać.</span><span class="sxs-lookup"><span data-stu-id="3b046-107">This is only needed when re-building the components; existing binaries will continue to work.</span></span>|
|<span data-ttu-id="3b046-108">Zakres</span><span class="sxs-lookup"><span data-stu-id="3b046-108">Scope</span></span>|<span data-ttu-id="3b046-109">Pomocnicza</span><span class="sxs-lookup"><span data-stu-id="3b046-109">Minor</span></span>|
|<span data-ttu-id="3b046-110">Wersja</span><span class="sxs-lookup"><span data-stu-id="3b046-110">Version</span></span>|<span data-ttu-id="3b046-111">4.5.1</span><span class="sxs-lookup"><span data-stu-id="3b046-111">4.5.1</span></span>|
|<span data-ttu-id="3b046-112">Typ</span><span class="sxs-lookup"><span data-stu-id="3b046-112">Type</span></span>|<span data-ttu-id="3b046-113">Przekierowania</span><span class="sxs-lookup"><span data-stu-id="3b046-113">Retargeting</span></span>|
|<span data-ttu-id="3b046-114">Dotyczy interfejsów API</span><span class="sxs-lookup"><span data-stu-id="3b046-114">Affected APIs</span></span>|<ul><li><xref:System.Data.Common.DbParameter.Precision?displayProperty=nameWithType></li><li><xref:System.Data.Common.DbParameter.Scale?displayProperty=nameWithType></li></ul>|
