### <a name="x509certificateclaimsetfindclaims-considers-all-claimtypes"></a><span data-ttu-id="62ae1-101">Traktuje wszystkie claimTypes X509CertificateClaimSet.FindClaims</span><span class="sxs-lookup"><span data-stu-id="62ae1-101">X509CertificateClaimSet.FindClaims Considers All claimTypes</span></span>

|   |   |
|---|---|
|<span data-ttu-id="62ae1-102">Szczegóły</span><span class="sxs-lookup"><span data-stu-id="62ae1-102">Details</span></span>|<span data-ttu-id="62ae1-103">W aplikacjach przeznaczonych dla platformy .NET Framework 4.6.1, jeśli X509 zestaw oświadczeń jest zainicjowany z certyfikatu, który ma wiele wpisów DNS w polu sieci SAN <xref:System.IdentityModel.Claims.X509CertificateClaimSet.FindClaims(System.String,System.String)?displayProperty=name> metoda próbuje dopasować argumentu typu oświadczenia z wszystkie wpisy DNS. W przypadku aplikacji, które odnoszą się do poprzednich wersji programu .NET Framework <xref:System.IdentityModel.Claims.X509CertificateClaimSet.FindClaims(System.String,System.String)?displayProperty=name> metoda próbuje dopasować argumentu typu oświadczenia tylko w przypadku ostatni wpis DNS.</span><span class="sxs-lookup"><span data-stu-id="62ae1-103">In apps that target the .NET Framework 4.6.1, if an X509 claim set is initialized from a certificate that has multiple DNS entries in its SAN field, the <xref:System.IdentityModel.Claims.X509CertificateClaimSet.FindClaims(System.String,System.String)?displayProperty=name> method attempts to match the claimType argument with all the DNS entries.For apps that target previous versions of the .NET Framework, the <xref:System.IdentityModel.Claims.X509CertificateClaimSet.FindClaims(System.String,System.String)?displayProperty=name> method attempts to match the claimType argument only with the last DNS entry.</span></span>|
|<span data-ttu-id="62ae1-104">Sugestia</span><span class="sxs-lookup"><span data-stu-id="62ae1-104">Suggestion</span></span>|<span data-ttu-id="62ae1-105">Ta zmiana wpływa tylko na aplikacji przeznaczonych dla platformy .NET Framework 4.6.1.</span><span class="sxs-lookup"><span data-stu-id="62ae1-105">This change only affects applications targeting the .NET Framework 4.6.1.</span></span> <span data-ttu-id="62ae1-106">Ta zmiana może być wyłączone (lub nie jest włączone, jeśli dotyczących wersji pre-4.6.1) z [DisableMultipleDNSEntries](~/docs/framework/migration-guide/mitigation-x509certificateclaimset-findclaims-method.md#mitigation) zgodności przełącznika.</span><span class="sxs-lookup"><span data-stu-id="62ae1-106">This change may be disabled (or enabled if targetting pre-4.6.1) with the [DisableMultipleDNSEntries](~/docs/framework/migration-guide/mitigation-x509certificateclaimset-findclaims-method.md#mitigation) compatibility switch.</span></span>|
|<span data-ttu-id="62ae1-107">Zakres</span><span class="sxs-lookup"><span data-stu-id="62ae1-107">Scope</span></span>|<span data-ttu-id="62ae1-108">Pomocnicza</span><span class="sxs-lookup"><span data-stu-id="62ae1-108">Minor</span></span>|
|<span data-ttu-id="62ae1-109">Wersja</span><span class="sxs-lookup"><span data-stu-id="62ae1-109">Version</span></span>|<span data-ttu-id="62ae1-110">4.6.1</span><span class="sxs-lookup"><span data-stu-id="62ae1-110">4.6.1</span></span>|
|<span data-ttu-id="62ae1-111">Typ</span><span class="sxs-lookup"><span data-stu-id="62ae1-111">Type</span></span>|<span data-ttu-id="62ae1-112">Przekierowania</span><span class="sxs-lookup"><span data-stu-id="62ae1-112">Retargeting</span></span>|
|<span data-ttu-id="62ae1-113">Dotyczy interfejsów API</span><span class="sxs-lookup"><span data-stu-id="62ae1-113">Affected APIs</span></span>|<ul><li><xref:System.IdentityModel.Claims.X509CertificateClaimSet.FindClaims(System.String,System.String)?displayProperty=nameWithType></li></ul>|
