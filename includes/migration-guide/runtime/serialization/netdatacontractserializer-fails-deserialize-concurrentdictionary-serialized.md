### <a name="netdatacontractserializer-fails-to-deserialize-a-concurrentdictionary-serialized-with-a-different-net-version"></a><span data-ttu-id="784d3-101">NetDataContractSerializer nie powiedzie się do deserializacji obiekt ConcurrentDictionary serializacji przy użyciu różnych wersji platformy .NET</span><span class="sxs-lookup"><span data-stu-id="784d3-101">NetDataContractSerializer fails to deserialize a ConcurrentDictionary serialized with a different .NET version</span></span>

|   |   |
|---|---|
|<span data-ttu-id="784d3-102">Szczegóły</span><span class="sxs-lookup"><span data-stu-id="784d3-102">Details</span></span>|<span data-ttu-id="784d3-103">Zgodnie z projektem <xref:System.Runtime.Serialization.NetDataContractSerializer?displayProperty=name> mogą być używane tylko w przypadku, gdy zarówno serializację i deserializację kończy się udostępnianie tych samych typów CLR.</span><span class="sxs-lookup"><span data-stu-id="784d3-103">By design, the <xref:System.Runtime.Serialization.NetDataContractSerializer?displayProperty=name> can be used only if both the serializing and deserializing ends share the same CLR types.</span></span> <span data-ttu-id="784d3-104">W związku z tym nie ma żadnej gwarancji czy obiekt serializowany z jednej wersji programu .NET Framework może być zdeserializowany przy użyciu innej wersji.<xref:System.Collections.Concurrent.ConcurrentDictionary%602?displayProperty=name></span><span class="sxs-lookup"><span data-stu-id="784d3-104">Therefore, it is not guaranteed that an object serialized with one version of the .NET Framework can be deserialized by a different version.<xref:System.Collections.Concurrent.ConcurrentDictionary%602?displayProperty=name></span></span> <span data-ttu-id="784d3-105">jest typem wiadomo, że nie można deserializować poprawnie, jeśli serializacji przy użyciu programu .NET Framework 4.5 lub starszego, a następnie deserializowany za pomocą programu .NET Framework 4.5.1 lub nowszej.</span><span class="sxs-lookup"><span data-stu-id="784d3-105">is a type that is known to not to deserialize correctly if serialized with the .NET Framework 4.5 or earlier and deserialized with the .NET Framework 4.5.1 or later.</span></span>|
|<span data-ttu-id="784d3-106">Sugestia</span><span class="sxs-lookup"><span data-stu-id="784d3-106">Suggestion</span></span>|<span data-ttu-id="784d3-107">Istnieje kilka możliwych obejścia tego problemu:</span><span class="sxs-lookup"><span data-stu-id="784d3-107">There are a number of possible work-arounds for this issue:</span></span><ul><li><span data-ttu-id="784d3-108">Uaktualnienie serializacji do użycia w programie .NET Framework 4.5.1, jak również.</span><span class="sxs-lookup"><span data-stu-id="784d3-108">Upgrade the serializing computer to use the .NET Framework 4.5.1, as well.</span></span></li><li><span data-ttu-id="784d3-109">Użyj <xref:System.Runtime.Serialization.DataContractSerializer?displayProperty=name> zamiast <xref:System.Runtime.Serialization.NetDataContractSerializer?displayProperty=name> jako nie oczekuje dokładnie takie same typy CLR zarówno serializacji i deserializacji kończy się.</span><span class="sxs-lookup"><span data-stu-id="784d3-109">Use <xref:System.Runtime.Serialization.DataContractSerializer?displayProperty=name> instead of <xref:System.Runtime.Serialization.NetDataContractSerializer?displayProperty=name> as this does not expect the exact same CLR types at both serializing and deserializing ends.</span></span></li><li><span data-ttu-id="784d3-110">Użyj <xref:System.Collections.Generic.Dictionary%602?displayProperty=name> zamiast <xref:System.Collections.Concurrent.ConcurrentDictionary%602?displayProperty=name> od czasu nie występuje tego konkretnego 4.5 -&gt;Podziel 4.5.1.</span><span class="sxs-lookup"><span data-stu-id="784d3-110">Use <xref:System.Collections.Generic.Dictionary%602?displayProperty=name> instead of <xref:System.Collections.Concurrent.ConcurrentDictionary%602?displayProperty=name> since it does not exhibit this particular 4.5-&gt;4.5.1 break.</span></span></li></ul>|
|<span data-ttu-id="784d3-111">Zakres</span><span class="sxs-lookup"><span data-stu-id="784d3-111">Scope</span></span>|<span data-ttu-id="784d3-112">Pomocnicza</span><span class="sxs-lookup"><span data-stu-id="784d3-112">Minor</span></span>|
|<span data-ttu-id="784d3-113">Wersja</span><span class="sxs-lookup"><span data-stu-id="784d3-113">Version</span></span>|<span data-ttu-id="784d3-114">4.5.1</span><span class="sxs-lookup"><span data-stu-id="784d3-114">4.5.1</span></span>|
|<span data-ttu-id="784d3-115">Typ</span><span class="sxs-lookup"><span data-stu-id="784d3-115">Type</span></span>|<span data-ttu-id="784d3-116">Środowisko uruchomieniowe</span><span class="sxs-lookup"><span data-stu-id="784d3-116">Runtime</span></span>|
|<span data-ttu-id="784d3-117">Dotyczy interfejsów API</span><span class="sxs-lookup"><span data-stu-id="784d3-117">Affected APIs</span></span>|<ul><li><xref:System.Runtime.Serialization.NetDataContractSerializer.Deserialize(System.IO.Stream)?displayProperty=nameWithType></li></ul>|
