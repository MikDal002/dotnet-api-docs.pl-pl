### <a name="new-64-bit-jit-compiler-in-the-net-framework-46"></a><span data-ttu-id="d9e4f-101">Nowy kompilator JIT 64-bitowe w .NET Framework 4.6</span><span class="sxs-lookup"><span data-stu-id="d9e4f-101">New 64-bit JIT compiler in the .NET Framework 4.6</span></span>

|   |   |
|---|---|
|<span data-ttu-id="d9e4f-102">Szczegóły</span><span class="sxs-lookup"><span data-stu-id="d9e4f-102">Details</span></span>|<span data-ttu-id="d9e4f-103">Począwszy od programu .NET Framework 4.6, nowy kompilator JIT 64-bitowy jest używany w czasie kompilacji.</span><span class="sxs-lookup"><span data-stu-id="d9e4f-103">Starting with the .NET Framework 4.6, a new 64-bit JIT compiler is used for just-in-time compilation.</span></span> <span data-ttu-id="d9e4f-104">W niektórych przypadkach jest nieoczekiwany wyjątek lub zaobserwowano inaczej niż Jeśli aplikacja jest uruchamiana za pomocą kompilatora 32-bitowej lub starszego kompilatora JIT 64-bitowych.</span><span class="sxs-lookup"><span data-stu-id="d9e4f-104">In some cases, an unexpected exception is thrown or a different behavior is observed than if an app is run using the 32-bit compiler or the older 64-bit JIT compiler.</span></span> <span data-ttu-id="d9e4f-105">Ta zmiana nie wpływa na 32-bitowej przy użyciu kompilatora JIT. Znane różnice są następujące:</span><span class="sxs-lookup"><span data-stu-id="d9e4f-105">This change does not affect the 32-bit JIT compiler.The known differences include the following:</span></span><ul><li><span data-ttu-id="d9e4f-106">W niektórych warunkach może zgłaszać rozpakowującej operacji <xref:System.NullReferenceException> w kompilacjach wydania z optymalizacją włączona.</span><span class="sxs-lookup"><span data-stu-id="d9e4f-106">Under certain conditions, an unboxing operation may throw a <xref:System.NullReferenceException> in Release builds with optimization turned on.</span></span></li><li><span data-ttu-id="d9e4f-107">W niektórych przypadkach może zgłaszać wykonywanie kodu produkcyjnego w treści metody dużych <xref:System.StackOverflowException>.</span><span class="sxs-lookup"><span data-stu-id="d9e4f-107">In some cases, execution of production code in a large method body may throw a <xref:System.StackOverflowException>.</span></span></li><li><span data-ttu-id="d9e4f-108">W niektórych warunkach struktury przekazana do metody są traktowane jako typów referencyjnych, a nie jako wartość typów w wersji kompilacji.</span><span class="sxs-lookup"><span data-stu-id="d9e4f-108">Under certain conditions, structures passed to a method are treated as reference types rather than as value types in Release builds.</span></span> <span data-ttu-id="d9e4f-109">Jednym z przejawy tego problemu jest czy poszczególnych elementów w kolekcji są wyświetlane w kolejności nieoczekiwany.</span><span class="sxs-lookup"><span data-stu-id="d9e4f-109">One of the manifestations of this issue is that the individual items in a collection appear in an unexpected order.</span></span></li><li><span data-ttu-id="d9e4f-110">W niektórych warunkach porównanie <xref:System.UInt16> wartości z ich wysokobitowe zestawu jest nieprawidłowa, gdy Optymalizacja jest włączona.</span><span class="sxs-lookup"><span data-stu-id="d9e4f-110">Under certain conditions, the comparison of <xref:System.UInt16> values with their high bit set is incorrect if optimization is enabled.</span></span></li><li><span data-ttu-id="d9e4f-111">W niektórych warunkach, szczególnie gdy inicjowanie tablicy wartości, inicjowania pamięci przez <xref:System.Reflection.Emit.OpCodes.Initblk?displayProperty=nameWithType> instrukcji IL może zainicjować pamięci z niepoprawną wartość.</span><span class="sxs-lookup"><span data-stu-id="d9e4f-111">Under certain conditions, particularly when initializing array values, memory initialization by the <xref:System.Reflection.Emit.OpCodes.Initblk?displayProperty=nameWithType> IL instruction may initialize memory with an incorrect value.</span></span> <span data-ttu-id="d9e4f-112">Dzięki temu można w nieobsługiwany wyjątek lub nieprawidłowych danych wyjściowych.</span><span class="sxs-lookup"><span data-stu-id="d9e4f-112">This can result either in an unhandled exception or incorrect output.</span></span></li><li><span data-ttu-id="d9e4f-113">W niektórych warunkach rzadkich test warunkowy bit może zwrócić nieprawidłowym <xref:System.Boolean> wartość lub zgłosić wyjątek, jeśli jest włączona Optymalizacja kompilatora.</span><span class="sxs-lookup"><span data-stu-id="d9e4f-113">Under certain rare conditions, a conditional bit test can return the incorrect <xref:System.Boolean> value or throw an exception if compiler optimizations are enabled.</span></span></li><li><span data-ttu-id="d9e4f-114">W niektórych warunkach Jeśli <code>if</code> testować warunek przed wprowadzeniem używana jest instrukcja <code>try</code> bloku i wyjście z <code>try</code> bloku, a tym samym stanie, które są oceniane w <code>catch</code> lub <code>finally</code> bloku, nowy Kompilator JIT 64-bitowy usuwa <code>if</code> warunku z <code>catch</code> lub <code>finally</code> zablokować, jeśli optymalizuje kod.</span><span class="sxs-lookup"><span data-stu-id="d9e4f-114">Under certain conditions, if an <code>if</code> statement is used to test for a condition before entering  a <code>try</code> block and in the exit from the <code>try</code> block, and the same condition is evaluated in the <code>catch</code> or <code>finally</code> block, the new 64-bit JIT compiler removes the <code>if</code> condition from the <code>catch</code> or <code>finally</code> block when it optimizes code.</span></span> <span data-ttu-id="d9e4f-115">W związku z tym kodu wewnątrz <code>if</code> instrukcji w <code>catch</code> lub <code>finally</code> bezwarunkowo wykonaniu bloku.</span><span class="sxs-lookup"><span data-stu-id="d9e4f-115">As a result, code inside the <code>if</code> statement in the <code>catch</code> or <code>finally</code> block is executed unconditionally.</span></span></li></ul>|
|<span data-ttu-id="d9e4f-116">Sugestia</span><span class="sxs-lookup"><span data-stu-id="d9e4f-116">Suggestion</span></span>|<span data-ttu-id="d9e4f-117"><strong>Środki zaradcze znanych problemów</strong> Jeśli wystąpią problemy z wymienionych powyżej, można rozwiązać je, wykonując jedną z następujących czynności:</span><span class="sxs-lookup"><span data-stu-id="d9e4f-117"><strong>Mitigation of known issues</strong> If you encounter the issues listed above, you can address them by doing any of the following:</span></span><ul><li><span data-ttu-id="d9e4f-118">Uaktualnianie do programu .NET Framework 4.6.2.</span><span class="sxs-lookup"><span data-stu-id="d9e4f-118">Upgrade to the .NET Framework 4.6.2.</span></span> <span data-ttu-id="d9e4f-119">Kompilator 64-bitowych uwzględnionych w programie .NET Framework 4.6.2 adresów każdego z tych znanych problemów.</span><span class="sxs-lookup"><span data-stu-id="d9e4f-119">The new 64-bit compiler included with the .NET Framework 4.6.2 addresses each of these known issues.</span></span></li><li><span data-ttu-id="d9e4f-120">Upewnij się, że danej wersji systemu Windows jest aktualny, uruchamiając usługi Windows Update.</span><span class="sxs-lookup"><span data-stu-id="d9e4f-120">Ensure that your version of Windows is up to date by running Windows Update.</span></span> <span data-ttu-id="d9e4f-121">Usługi aktualizacji programu .NET Framework 4.6 i 4.6.1 dotyczą każdego z tych problemów, z wyjątkiem <xref:System.NullReferenceException> w rozpakowującej operacji.</span><span class="sxs-lookup"><span data-stu-id="d9e4f-121">Service updates to the .NET Framework 4.6 and 4.6.1 address each of these issues except the <xref:System.NullReferenceException> in an unboxing operation.</span></span></li><li><span data-ttu-id="d9e4f-122">Kompiluj z użyciem starszego kompilatora JIT 64-bitowych.</span><span class="sxs-lookup"><span data-stu-id="d9e4f-122">Compile with the older 64-bit JIT compiler.</span></span> <span data-ttu-id="d9e4f-123">Zobacz <strong>ograniczenie inne problemy</strong> sekcji, aby uzyskać więcej informacji na temat sposobu wykonania tego zadania.</span><span class="sxs-lookup"><span data-stu-id="d9e4f-123">See the <strong>Mitigation of other issues</strong> section for more information on how to do this.</span></span></li></ul><span data-ttu-id="d9e4f-124"><strong>Środki zaradcze innych problemów</strong> wystąpią wszelkie inne różnice w zachowaniu kodu skompilowanego za pomocą starszego kompilatora 64-bitowe i kompilator JIT 64-bitowych, czy między wersjami debug i release aplikacji znajdujących się zarówno skompilowana z nowym Kompilator JIT 64-bitowy, można wykonać następujące polecenie, aby skompilować aplikacji za pomocą starszego kompilatora JIT 64-bitowe:</span><span class="sxs-lookup"><span data-stu-id="d9e4f-124"><strong>Mitigation of other issues</strong> If you encounter any other difference in behavior between code compiled with the older 64-bit compiler and the new 64-bit JIT compiler, or between the debug and release versions of your app that are both compiled with the new 64-bit JIT compiler, you can do the following to compile your app with the older 64-bit JIT compiler:</span></span><ul><li><span data-ttu-id="d9e4f-125">Na poszczególnych aplikacji, co można dodać [ \<useLegacyJit >](~/docs/framework/configure-apps/file-schema/runtime/uselegacyjit-element.md) elementu do pliku konfiguracji aplikacji.</span><span class="sxs-lookup"><span data-stu-id="d9e4f-125">On a per-application basis, you can add the [\<useLegacyJit>](~/docs/framework/configure-apps/file-schema/runtime/uselegacyjit-element.md) element to your application's configuration file.</span></span> <span data-ttu-id="d9e4f-126">Następujące wyłącza kompilacji przez kompilator JIT 64-bitowe i zamiast tego używa starszej wersji kompilatora JIT 64-bitowych.</span><span class="sxs-lookup"><span data-stu-id="d9e4f-126">The following disables compilation with the new 64-bit JIT compiler and instead uses the legacy 64-bit JIT compiler.</span></span></li></ul><pre><code class="language-xml">&lt;?xml version =&quot;1.0&quot;?&gt;&#13;&#10;&lt;configuration&gt;&#13;&#10;&lt;runtime&gt;&#13;&#10;&lt;useLegacyJit enabled=&quot;1&quot; /&gt;&#13;&#10;&lt;/runtime&gt;&#13;&#10;&lt;/configuration&gt;&#13;&#10;</code></pre><ul><li><span data-ttu-id="d9e4f-127">Na podstawie użytkownika, można dodać <code>REG_DWORD</code> wartość o nazwie <code>useLegacyJit</code> do <code>HKEY_CURRENT_USER\SOFTWARE\Microsoft\.NETFramework</code> klucza rejestru.</span><span class="sxs-lookup"><span data-stu-id="d9e4f-127">On a per-user basis, you can add a <code>REG_DWORD</code> value named <code>useLegacyJit</code> to the <code>HKEY_CURRENT_USER\SOFTWARE\Microsoft\.NETFramework</code> key of the registry.</span></span> <span data-ttu-id="d9e4f-128">Wartość 1 powoduje włączenie starszej wersji 64-bitowej przy użyciu kompilatora JIT; wartość 0 powoduje wyłączenie go i włącza kompilator JIT 64-bitowych.</span><span class="sxs-lookup"><span data-stu-id="d9e4f-128">A value of 1 enables the legacy 64-bit JIT compiler; a value of 0 disables it and enables the new 64-bit JIT compiler.</span></span></li><li><span data-ttu-id="d9e4f-129">Na poszczególnych komputerach, można dodać <code>REG_DWORD</code> wartość o nazwie <code>useLegacyJit</code> do <code>HKEY_LOCAL_MACHINE\SOFTWARE\Microsoft\.NETFramework</code> klucza rejestru.</span><span class="sxs-lookup"><span data-stu-id="d9e4f-129">On a per-machine basis, you can add a <code>REG_DWORD</code> value named <code>useLegacyJit</code> to the <code>HKEY_LOCAL_MACHINE\SOFTWARE\Microsoft\.NETFramework</code> key of the registry.</span></span> <span data-ttu-id="d9e4f-130">Wartość <code>1</code> kompilatora JIT umożliwia starszej wersji 64-bitowy; wartość <code>0</code> powoduje wyłączenie go i włącza kompilator JIT 64-bitowych.</span><span class="sxs-lookup"><span data-stu-id="d9e4f-130">A value of <code>1</code> enables the legacy 64-bit JIT compiler; a value of <code>0</code> disables it and enables the new 64-bit JIT compiler.</span></span></li></ul><span data-ttu-id="d9e4f-131">Można również Daj nam wiedzę na temat problemu przez raportowanie błędów na [Microsoft Connect](https://connect.microsoft.com/VisualStudio).</span><span class="sxs-lookup"><span data-stu-id="d9e4f-131">You can also let us know about the problem by reporting a bug on [Microsoft Connect](https://connect.microsoft.com/VisualStudio).</span></span>|
|<span data-ttu-id="d9e4f-132">Zakres</span><span class="sxs-lookup"><span data-stu-id="d9e4f-132">Scope</span></span>|<span data-ttu-id="d9e4f-133">Krawędź</span><span class="sxs-lookup"><span data-stu-id="d9e4f-133">Edge</span></span>|
|<span data-ttu-id="d9e4f-134">Wersja</span><span class="sxs-lookup"><span data-stu-id="d9e4f-134">Version</span></span>|<span data-ttu-id="d9e4f-135">4.6</span><span class="sxs-lookup"><span data-stu-id="d9e4f-135">4.6</span></span>|
|<span data-ttu-id="d9e4f-136">Typ</span><span class="sxs-lookup"><span data-stu-id="d9e4f-136">Type</span></span>|<span data-ttu-id="d9e4f-137">Przekierowania</span><span class="sxs-lookup"><span data-stu-id="d9e4f-137">Retargeting</span></span>|
