### <a name="building-an-entity-framework-edmx-with-visual-studio-2013-can-fail-with-error-msb4062-if-using-the-entitydeploysplit-or-entityclean-tasks"></a><span data-ttu-id="881bd-101">Tworzenie pliku edmx Entity Framework z programu Visual Studio 2013 może zakończyć się niepowodzeniem z powodu błędu MSB4062 Jeśli za pomocą zadań EntityDeploySplit lub EntityClean</span><span class="sxs-lookup"><span data-stu-id="881bd-101">Building an Entity Framework edmx with Visual Studio 2013 can fail with error MSB4062 if using the EntityDeploySplit or EntityClean tasks</span></span>

|   |   |
|---|---|
|<span data-ttu-id="881bd-102">Szczegóły</span><span class="sxs-lookup"><span data-stu-id="881bd-102">Details</span></span>|<span data-ttu-id="881bd-103">Narzędzia MSBuild 12.0 (dołączone do programu Visual Studio 2013) zmienić MSBuild lokalizacje plików, co powoduje starsze pliki cele Entity Framework jest nieprawidłowy.</span><span class="sxs-lookup"><span data-stu-id="881bd-103">MSBuild 12.0 tools (included in Visual Studio 2013) changed MSBuild file locations, causing older Entity Framework targets files to be invalid.</span></span> <span data-ttu-id="881bd-104">W wyniku <code>EntityDeploySplit</code> i <code>EntityClean</code> zadań zakończy się niepowodzeniem, ponieważ nie można odnaleźć <code>Microsoft.Data.Entity.Build.Tasks.dll</code>.</span><span class="sxs-lookup"><span data-stu-id="881bd-104">The result is that <code>EntityDeploySplit</code> and <code>EntityClean</code> tasks fail because they are unable to find <code>Microsoft.Data.Entity.Build.Tasks.dll</code>.</span></span> <span data-ttu-id="881bd-105">Należy pamiętać, że ten podział ze względu na zmiany (MSBuild/VS) zestawu narzędzi nie ze względu na zmiany .NET Framework.</span><span class="sxs-lookup"><span data-stu-id="881bd-105">Note that this break is because of a toolset (MSBuild/VS) change, not because of a .NET Framework change.</span></span> <span data-ttu-id="881bd-106">Tylko wystąpią, gdy uaktualniania narzędzi dla deweloperów, nie w przypadku, gdy tylko uaktualniania programu .NET Framework.</span><span class="sxs-lookup"><span data-stu-id="881bd-106">It will only occur when upgrading developer tools, not when merely upgrading the .NET Framework.</span></span>|
|<span data-ttu-id="881bd-107">Sugestia</span><span class="sxs-lookup"><span data-stu-id="881bd-107">Suggestion</span></span>|<span data-ttu-id="881bd-108">Usunięto Entity Framework cele plików do pracy z nowego MSBuild układu począwszy od wersji programu .NET Framework 4.6.</span><span class="sxs-lookup"><span data-stu-id="881bd-108">Entity Framework targets files are fixed to work with the new MSBuild layout beginning in the .NET Framework 4.6.</span></span> <span data-ttu-id="881bd-109">Uaktualnianie do tej wersji platformy naprawi ten problem.</span><span class="sxs-lookup"><span data-stu-id="881bd-109">Upgrading to that version of the Framework will fix this issue.</span></span> <span data-ttu-id="881bd-110">Alternatywnie [to](http://stackoverflow.com/a/24249247/131944) obejście może służyć do bezpośrednio poprawka plików obiektów docelowych.</span><span class="sxs-lookup"><span data-stu-id="881bd-110">Alternatively, [this](http://stackoverflow.com/a/24249247/131944) workaround can be used to patch the targets files directly.</span></span>|
|<span data-ttu-id="881bd-111">Zakres</span><span class="sxs-lookup"><span data-stu-id="881bd-111">Scope</span></span>|<span data-ttu-id="881bd-112">Główne</span><span class="sxs-lookup"><span data-stu-id="881bd-112">Major</span></span>|
|<span data-ttu-id="881bd-113">Wersja</span><span class="sxs-lookup"><span data-stu-id="881bd-113">Version</span></span>|<span data-ttu-id="881bd-114">4.5.1</span><span class="sxs-lookup"><span data-stu-id="881bd-114">4.5.1</span></span>|
|<span data-ttu-id="881bd-115">Typ</span><span class="sxs-lookup"><span data-stu-id="881bd-115">Type</span></span>|<span data-ttu-id="881bd-116">Przekierowania</span><span class="sxs-lookup"><span data-stu-id="881bd-116">Retargeting</span></span>|
