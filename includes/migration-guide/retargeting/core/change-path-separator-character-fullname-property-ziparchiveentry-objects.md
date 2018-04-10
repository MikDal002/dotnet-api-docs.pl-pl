### <a name="change-in-path-separator-character-in-fullname-property-of-ziparchiveentry-objects"></a><span data-ttu-id="3e4d6-101">Zmiany w znaku separatora ścieżki we właściwości pełną nazwę obiektu klasy ZipArchiveEntry obiektów</span><span class="sxs-lookup"><span data-stu-id="3e4d6-101">Change in path separator character in FullName property of ZipArchiveEntry objects</span></span>

|   |   |
|---|---|
|<span data-ttu-id="3e4d6-102">Szczegóły</span><span class="sxs-lookup"><span data-stu-id="3e4d6-102">Details</span></span>|<span data-ttu-id="3e4d6-103">W przypadku aplikacji przeznaczonych dla platformy .NET Framework 4.6.1 i nowszych wersjach znak separatora ścieżki zmienił się z ukośnik odwrotny (&quot;&quot;) na ukośnik (&quot;/&quot;) w <xref:System.IO.Compression.ZipArchiveEntry.FullName> właściwości <xref:System.IO.Compression.ZipArchiveEntry> obiekty utworzone przez przeciążeń <xref:System.IO.Compression.ZipFile.CreateFromDirectory%2A> metody.</span><span class="sxs-lookup"><span data-stu-id="3e4d6-103">For apps that target the .NET Framework 4.6.1 and later versions, the path separator character has changed from a backslash (&quot;&quot;) to a forward slash (&quot;/&quot;) in the <xref:System.IO.Compression.ZipArchiveEntry.FullName> property of <xref:System.IO.Compression.ZipArchiveEntry>  objects created by overloads of the <xref:System.IO.Compression.ZipFile.CreateFromDirectory%2A> method.</span></span> <span data-ttu-id="3e4d6-104">Zmiana powoduje implementacji .NET do zgodności z sekcji 4.4.17.1 [. Specyfikacją formatu pliku ZIP](https://pkware.cachefly.net/webdocs/casestudies/APPNOTE.TXT) i umożliwia. Archiwa ZIP do można zdekompresować w systemach z systemem innym niż Windows. Podczas dekompresowania pliku zip utworzonego przez aplikację którego element docelowy poprzedniej wersji programu .NET Framework w systemach operacyjnych z systemem innym niż Windows, takich jak Macintosh nie powiedzie się, aby zachować struktura katalogów.</span><span class="sxs-lookup"><span data-stu-id="3e4d6-104">The change brings the .NET implementation into conformity with section 4.4.17.1 of the [.ZIP File Format Specification](https://pkware.cachefly.net/webdocs/casestudies/APPNOTE.TXT) and allows .ZIP archives to be decompressed on non-Windows systems.Decompressing a zip file created by an app that targets a previous version of the .NET Framework on non-Windows operating systems such as the Macintosh fails to preserve the directory structure.</span></span> <span data-ttu-id="3e4d6-105">Na przykład w przypadku komputerów Macintosh tworzy zestaw plików, których nazwy łączy ścieżki katalogu, wraz z dowolnym ukośnik odwrotny (&quot;&quot;) znaków, a nazwa pliku.</span><span class="sxs-lookup"><span data-stu-id="3e4d6-105">For example, on the Macintosh, it creates a set of files whose filename concatenates the directory path, along with any backslash (&quot;&quot;) characters, and the filename.</span></span> <span data-ttu-id="3e4d6-106">W związku z tym struktura katalogów zdekompresowanych plików nie są zachowywane.</span><span class="sxs-lookup"><span data-stu-id="3e4d6-106">As a result, the directory structure of decompressed files is not preserved.</span></span>|
|<span data-ttu-id="3e4d6-107">Sugestia</span><span class="sxs-lookup"><span data-stu-id="3e4d6-107">Suggestion</span></span>|<span data-ttu-id="3e4d6-108">Wpływ tej zmiany na. Pliki ZIP, które są zdekompresować w systemie operacyjnym Windows przez interfejs API programu .NET Framework <xref:System.IO?displayProperty=nameWithType> przestrzeń nazw powinna mieć minimalny, ponieważ te interfejsy API bezproblemowo może obsłużyć albo ukośnika (&quot;/&quot;) ani ukośnika odwrotnego (&quot; \&quot;) jako znaku separatora ścieżki. Jeśli ta zmiana jest niepożądane, można zrezygnować z go, dodając ustawienia konfiguracji w celu [ \<runtime >](~/docs/framework/configure-apps/file-schema/runtime/runtime-element.md) sekcji pliku konfiguracji aplikacji.</span><span class="sxs-lookup"><span data-stu-id="3e4d6-108">The impact of this change on .ZIP files that are decompressed on the Windows operating system by APIs in the .NET Framework <xref:System.IO?displayProperty=nameWithType> namespace should be minimal, since these APIs can seamlessly handle either a slash (&quot;/&quot;) or a backslash (&quot;\&quot;) as the path separator character.If this change is undesirable, you can opt out of it by adding a configuration setting to the [\<runtime>](~/docs/framework/configure-apps/file-schema/runtime/runtime-element.md) section of your application configuration file.</span></span> <span data-ttu-id="3e4d6-109">W poniższym przykładzie przedstawiono oba `<runtime>` sekcji i `Switch.System.IO.Compression.ZipFile.UseBackslash` przełącznika zrezygnować:</span><span class="sxs-lookup"><span data-stu-id="3e4d6-109">The following example shows both the `<runtime>` section and the `Switch.System.IO.Compression.ZipFile.UseBackslash` opt-out switch:</span></span><pre><code class="language-xml">&lt;runtime&gt;&#13;&#10;&lt;AppContextSwitchOverrides value=&quot;Switch.System.IO.Compression.ZipFile.UseBackslash=true&quot; /&gt;&#13;&#10;&lt;/runtime&gt;&#13;&#10;</code></pre><span data-ttu-id="3e4d6-110">Ponadto aplikacje docelowe poprzednie wersje programu .NET Framework, które są uruchomione w programie .NET Framework 4.6.1 i nowszych wersjach zgodzić się na to zachowanie przez dodanie ustawienia konfiguracji do [ \<runtime >](~/docs/framework/configure-apps/file-schema/runtime/runtime-element.md) sekcja pliku konfiguracji aplikacji.</span><span class="sxs-lookup"><span data-stu-id="3e4d6-110">In addition, apps that target previous versions of the .NET Framework but are running on the .NET Framework 4.6.1 and later versions can opt in to this behavior by adding a configuration setting to the [\<runtime>](~/docs/framework/configure-apps/file-schema/runtime/runtime-element.md) section of the application configuration file.</span></span> <span data-ttu-id="3e4d6-111">Poniżej pokazano zarówno `<runtime>` sekcji i `Switch.System.IO.Compression.ZipFile.UseBackslash` opcjonalnych przełącznika.</span><span class="sxs-lookup"><span data-stu-id="3e4d6-111">The following shows both the `<runtime>` section and the `Switch.System.IO.Compression.ZipFile.UseBackslash` opt-in switch.</span></span><pre><code class="language-xml">&lt;runtime&gt;&#13;&#10;&lt;AppContextSwitchOverrides value=&quot;Switch.System.IO.Compression.ZipFile.UseBackslash=false&quot; /&gt;&#13;&#10;&lt;/runtime&gt;&#13;&#10;</code></pre>|
|<span data-ttu-id="3e4d6-112">Zakres</span><span class="sxs-lookup"><span data-stu-id="3e4d6-112">Scope</span></span>|<span data-ttu-id="3e4d6-113">Krawędź</span><span class="sxs-lookup"><span data-stu-id="3e4d6-113">Edge</span></span>|
|<span data-ttu-id="3e4d6-114">Wersja</span><span class="sxs-lookup"><span data-stu-id="3e4d6-114">Version</span></span>|<span data-ttu-id="3e4d6-115">4.6.1</span><span class="sxs-lookup"><span data-stu-id="3e4d6-115">4.6.1</span></span>|
|<span data-ttu-id="3e4d6-116">Typ</span><span class="sxs-lookup"><span data-stu-id="3e4d6-116">Type</span></span>|<span data-ttu-id="3e4d6-117">Przekierowania</span><span class="sxs-lookup"><span data-stu-id="3e4d6-117">Retargeting</span></span>|
|<span data-ttu-id="3e4d6-118">Dotyczy interfejsów API</span><span class="sxs-lookup"><span data-stu-id="3e4d6-118">Affected APIs</span></span>|<ul><li><xref:System.IO.Compression.ZipFile.CreateFromDirectory(System.String,System.String)?displayProperty=nameWithType></li><li><xref:System.IO.Compression.ZipFile.CreateFromDirectory(System.String,System.String,System.IO.Compression.CompressionLevel,System.Boolean)?displayProperty=nameWithType></li><li><xref:System.IO.Compression.ZipFile.CreateFromDirectory(System.String,System.String,System.IO.Compression.CompressionLevel,System.Boolean,System.Text.Encoding)?displayProperty=nameWithType></li></ul>|
