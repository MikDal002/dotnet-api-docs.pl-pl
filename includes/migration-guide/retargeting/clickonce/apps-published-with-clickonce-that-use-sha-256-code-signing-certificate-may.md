### <a name="apps-published-with-clickonce-that-use-a-sha-256-code-signing-certificate-may-fail-on-windows-2003"></a><span data-ttu-id="5625a-101">Aplikacje opublikowane za pomocą technologii ClickOnce, korzystających z algorytmu SHA-256 certyfikat podpisywania kodu może zakończyć się niepowodzeniem w systemie Windows 2003</span><span class="sxs-lookup"><span data-stu-id="5625a-101">Apps published with ClickOnce that use a SHA-256 code-signing certificate may fail on Windows 2003</span></span>

|   |   |
|---|---|
|<span data-ttu-id="5625a-102">Szczegóły</span><span class="sxs-lookup"><span data-stu-id="5625a-102">Details</span></span>|<span data-ttu-id="5625a-103">Plik wykonywalny jest podpisany za pomocą SHA256.</span><span class="sxs-lookup"><span data-stu-id="5625a-103">The executable is signed with SHA256.</span></span> <span data-ttu-id="5625a-104">Wcześniej był podpisany z SHA1 niezależnie od tego, czy certyfikat podpisywania kodu został SHA-1 lub SHA-256.</span><span class="sxs-lookup"><span data-stu-id="5625a-104">Previously, it was signed with SHA1 regardless of whether the code-signing certificate was SHA-1 or SHA-256.</span></span> <span data-ttu-id="5625a-105">Dotyczy to:</span><span class="sxs-lookup"><span data-stu-id="5625a-105">This applies to:</span></span><ul><li><span data-ttu-id="5625a-106">Wszystkie aplikacje skompilowane z programu Visual Studio 2012 lub nowszym.</span><span class="sxs-lookup"><span data-stu-id="5625a-106">All applications built with Visual Studio 2012 or later.</span></span></li><li><span data-ttu-id="5625a-107">Aplikacje opracowane za pomocą programu Visual Studio 2010 lub wcześniej w przypadku systemów z obecne środowisko .NET Framework 4.5.</span><span class="sxs-lookup"><span data-stu-id="5625a-107">Applications built with Visual Studio 2010 or earlier on systems with the .NET Framework 4.5 present.</span></span></li></ul><span data-ttu-id="5625a-108">Ponadto jeśli .NET Framework 4.5 lub nowszej, manifestu aplikacji ClickOnce są także podpisane z algorytmu SHA-256 w przypadku certyfikatów algorytmu SHA-256, niezależnie od wersji programu .NET Framework, względem którego został skompilowany.</span><span class="sxs-lookup"><span data-stu-id="5625a-108">In addition, if the .NET Framework 4.5 or later is present, the ClickOnce manifest is also signed with SHA-256 for SHA-256 certificates regardless of the .NET Framework version against which it was compiled.</span></span>|
|<span data-ttu-id="5625a-109">Sugestia</span><span class="sxs-lookup"><span data-stu-id="5625a-109">Suggestion</span></span>|<span data-ttu-id="5625a-110">W pliku wykonywalnego ClickOnce podpisywania dotyczy tylko systemów Windows Server 2003; wymagają zainstalowania KB 938397. Zmiana podpisywanie manifestu z algorytmu SHA-256, nawet wtedy, gdy aplikacja jest przeznaczony dla programu .NET Framework 4.0 i jego wcześniejsze wersje wprowadza zależności środowiska uruchomieniowego .NET Framework 4.5 lub nowszej wersji.</span><span class="sxs-lookup"><span data-stu-id="5625a-110">The change in signing the ClickOnce executable affects only Windows Server 2003 systems; they require that KB 938397 be installed.The change in signing the manifest with SHA-256 even when an app targets the .NET Framework 4.0 or earlier versions introduces a runtime dependency on the .NET Framework 4.5 or a later version.</span></span>|
|<span data-ttu-id="5625a-111">Zakres</span><span class="sxs-lookup"><span data-stu-id="5625a-111">Scope</span></span>|<span data-ttu-id="5625a-112">Krawędź</span><span class="sxs-lookup"><span data-stu-id="5625a-112">Edge</span></span>|
|<span data-ttu-id="5625a-113">Wersja</span><span class="sxs-lookup"><span data-stu-id="5625a-113">Version</span></span>|<span data-ttu-id="5625a-114">4.5</span><span class="sxs-lookup"><span data-stu-id="5625a-114">4.5</span></span>|
|<span data-ttu-id="5625a-115">Typ</span><span class="sxs-lookup"><span data-stu-id="5625a-115">Type</span></span>|<span data-ttu-id="5625a-116">Przekierowania</span><span class="sxs-lookup"><span data-stu-id="5625a-116">Retargeting</span></span>|
