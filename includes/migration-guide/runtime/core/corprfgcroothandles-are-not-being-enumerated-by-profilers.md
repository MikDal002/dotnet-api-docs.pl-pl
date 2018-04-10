### <a name="corprfgcroothandles-are-not-being-enumerated-by-profilers"></a><span data-ttu-id="f5ab3-101">COR_PRF_GC_ROOT_HANDLEs nie są wyliczenia przez profilowania</span><span class="sxs-lookup"><span data-stu-id="f5ab3-101">COR_PRF_GC_ROOT_HANDLEs are not being enumerated by profilers</span></span>

|   |   |
|---|---|
|<span data-ttu-id="f5ab3-102">Szczegóły</span><span class="sxs-lookup"><span data-stu-id="f5ab3-102">Details</span></span>|<span data-ttu-id="f5ab3-103">W v4.5.1 .NET Framework, interfejsu API profilowania <code>RootReferences2()</code> niepoprawnie nigdy nie zwraca <code>COR_PRF_GC_ROOT_HANDLE</code> (są one zwracane jako <code>COR_PRF_GC_ROOT_OTHER</code> zamiast niego).</span><span class="sxs-lookup"><span data-stu-id="f5ab3-103">In the .NET Framework v4.5.1, the profiling API <code>RootReferences2()</code> is incorrectly never returning <code>COR_PRF_GC_ROOT_HANDLE</code> (they are returned as <code>COR_PRF_GC_ROOT_OTHER</code> instead).</span></span> <span data-ttu-id="f5ab3-104">Tego problemu w programie .NET Framework 4.6.</span><span class="sxs-lookup"><span data-stu-id="f5ab3-104">This issue is fixed beginning in the .NET Framework 4.6.</span></span>|
|<span data-ttu-id="f5ab3-105">Sugestia</span><span class="sxs-lookup"><span data-stu-id="f5ab3-105">Suggestion</span></span>|<span data-ttu-id="f5ab3-106">Ten problem został rozwiązany w .NET Framework 4.6 i mogą być kierowane przez uaktualnienie do tej wersji programu .NET Framework.</span><span class="sxs-lookup"><span data-stu-id="f5ab3-106">This issue has been fixed in the .NET Framework 4.6 and may be addressed by upgrading to that version of the .NET Framework.</span></span>|
|<span data-ttu-id="f5ab3-107">Zakres</span><span class="sxs-lookup"><span data-stu-id="f5ab3-107">Scope</span></span>|<span data-ttu-id="f5ab3-108">Pomocnicza</span><span class="sxs-lookup"><span data-stu-id="f5ab3-108">Minor</span></span>|
|<span data-ttu-id="f5ab3-109">Wersja</span><span class="sxs-lookup"><span data-stu-id="f5ab3-109">Version</span></span>|<span data-ttu-id="f5ab3-110">4.5.1</span><span class="sxs-lookup"><span data-stu-id="f5ab3-110">4.5.1</span></span>|
|<span data-ttu-id="f5ab3-111">Typ</span><span class="sxs-lookup"><span data-stu-id="f5ab3-111">Type</span></span>|<span data-ttu-id="f5ab3-112">Środowisko uruchomieniowe</span><span class="sxs-lookup"><span data-stu-id="f5ab3-112">Runtime</span></span>|
