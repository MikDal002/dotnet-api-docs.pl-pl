### <a name="improved-accessibility-for-some-net-sdk-tools"></a><span data-ttu-id="96dd9-101">Ulepszone ułatwień dostępu dla niektórych narzędzi zestawu .NET SDK</span><span class="sxs-lookup"><span data-stu-id="96dd9-101">Improved accessibility for some .NET SDK tools</span></span>

|   |   |
|---|---|
|<span data-ttu-id="96dd9-102">Szczegóły</span><span class="sxs-lookup"><span data-stu-id="96dd9-102">Details</span></span>|<span data-ttu-id="96dd9-103">W zestawie SDK 4.7.1 Framework .NET ulepszono narzędzia svcconfigedit.exe i svctraceviewer.exe napraw problemy z dostępem zróżnicowane.</span><span class="sxs-lookup"><span data-stu-id="96dd9-103">In the .NET Framework SDK 4.7.1, the svcconfigedit.exe and svctraceviewer.exe tools have been improved by fixing varied accessibility issues.</span></span> <span data-ttu-id="96dd9-104">Większość tych były niewielkie problemy, jak nazwa nie jest zdefiniowany lub niektórych wzorce automatyzacji interfejsu użytkownika nie jest zaimplementowana poprawnie.</span><span class="sxs-lookup"><span data-stu-id="96dd9-104">Most of these were small issues like a name not being defined or certain UI automation patterns not being implemented correctly.</span></span> <span data-ttu-id="96dd9-105">Gdy wielu użytkowników nie byłoby znać te nieprawidłowe wartości, klienci korzystający z ułatwieniami technologii, takich jak czytniki znajdzie te narzędzia zestawu SDK dostęp.</span><span class="sxs-lookup"><span data-stu-id="96dd9-105">While many users wouldn’t be aware of these incorrect values, customers who use assistive technologies like screen readers will find these SDK tools more accessible.</span></span> <span data-ttu-id="96dd9-106">Oczywiście te poprawki zmienić niektóre zachowania poprzedniej, takich jak kolejność fokus klawiatury. Aby pobrać wszystkie, dostępność naprawia w tych narzędzi, można następujące do pliku app.config:</span><span class="sxs-lookup"><span data-stu-id="96dd9-106">Certainly, these fixes change some previous behaviors, like keyboard focus order.In order to get all the accessibility fixes in these tools, you can the following to your app.config file:</span></span><pre><code class="language-xml">&lt;runtime&gt;&#13;&#10;&lt;AppContextSwitchOverrides value=&quot;Switch.UseLegacyAccessibilityFeatures=false&quot;/&gt;&#13;&#10;&lt;/runtime&gt;&#13;&#10;</code></pre>|
|<span data-ttu-id="96dd9-107">Zakres</span><span class="sxs-lookup"><span data-stu-id="96dd9-107">Scope</span></span>|<span data-ttu-id="96dd9-108">Krawędź</span><span class="sxs-lookup"><span data-stu-id="96dd9-108">Edge</span></span>|
|<span data-ttu-id="96dd9-109">Wersja</span><span class="sxs-lookup"><span data-stu-id="96dd9-109">Version</span></span>|<span data-ttu-id="96dd9-110">4.7.1</span><span class="sxs-lookup"><span data-stu-id="96dd9-110">4.7.1</span></span>|
|<span data-ttu-id="96dd9-111">Typ</span><span class="sxs-lookup"><span data-stu-id="96dd9-111">Type</span></span>|<span data-ttu-id="96dd9-112">Przekierowania</span><span class="sxs-lookup"><span data-stu-id="96dd9-112">Retargeting</span></span>|
