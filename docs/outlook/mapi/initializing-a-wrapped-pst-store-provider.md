---
title: L’initialisation d’un fournisseur de magasins PST encapsulé
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
ms.assetid: 07633717-ba4c-b146-ad65-60b37ab98ab6
description: 'Dernière modification : 05 octobre 2012'
ms.openlocfilehash: a332c63814163579d5fe8ab365145e9583fa6c97
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19784326"
---
# <a name="initializing-a-wrapped-pst-store-provider"></a><span data-ttu-id="1bea1-103">L’initialisation d’un fournisseur de magasins PST encapsulé</span><span class="sxs-lookup"><span data-stu-id="1bea1-103">Initializing a wrapped PST store provider</span></span>

<span data-ttu-id="1bea1-104">**S’applique à**: Outlook</span><span class="sxs-lookup"><span data-stu-id="1bea1-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="1bea1-105">Pour implémenter un fournisseur de magasin de dossiers personnels (PST) de fichier encapsulé, vous devez initialiser le fournisseur de banque PST encapsulé à l’aide de la fonction **[MSProviderInit](msproviderinit.md)** comme point d’entrée.</span><span class="sxs-lookup"><span data-stu-id="1bea1-105">To implement a wrapped Personal Folders file (PST) store provider, you must initialize the wrapped PST store provider by using the **[MSProviderInit](msproviderinit.md)** function as an entry point.</span></span> <span data-ttu-id="1bea1-106">Une fois que la DLL du fournisseur est initialisée, la fonction **[MSGSERVICEENTRY](msgserviceentry.md)** configure le fournisseur de banque PST justifié.</span><span class="sxs-lookup"><span data-stu-id="1bea1-106">After the provider's DLL is initialized, the **[MSGSERVICEENTRY](msgserviceentry.md)** function configures the wrapped PST store provider.</span></span> 
  
<span data-ttu-id="1bea1-107">Dans cette rubrique, la fonction **MSProviderInit** et la fonction **MSGSERVICEENTRY** sont illustrées à l’aide des exemples de code à partir du fournisseur de magasin exemple encapsulé PST.</span><span class="sxs-lookup"><span data-stu-id="1bea1-107">In this topic, the **MSProviderInit** function and the **MSGSERVICEENTRY** function are demonstrated by using code examples from the Sample Wrapped PST Store Provider.</span></span> <span data-ttu-id="1bea1-108">L’exemple implémente un fournisseur PST renvoyé à la ligne qui est destiné à être utilisé conjointement avec l’API de réplication.</span><span class="sxs-lookup"><span data-stu-id="1bea1-108">The sample implements a wrapped PST provider that is intended to be used in conjunction with the Replication API.</span></span> <span data-ttu-id="1bea1-109">Pour plus d’informations sur le téléchargement et l’installation du fournisseur de magasin exemple encapsulé PST, voir [installer le fournisseur de banque exemple encapsulé PST](installing-the-sample-wrapped-pst-store-provider.md).</span><span class="sxs-lookup"><span data-stu-id="1bea1-109">For more information about downloading and installing the Sample Wrapped PST Store Provider, see [Installing the Sample Wrapped PST Store Provider](installing-the-sample-wrapped-pst-store-provider.md).</span></span> <span data-ttu-id="1bea1-110">Pour plus d’informations sur l’API de réplication, consultez la rubrique [Sur l’API de réplication](about-the-replication-api.md).</span><span class="sxs-lookup"><span data-stu-id="1bea1-110">For more information about the Replication API, see [About the Replication API](about-the-replication-api.md).</span></span>
  
<span data-ttu-id="1bea1-111">Une fois que vous avez initialisé un fournisseur de magasins PST encapsulé, vous devez implémenter les fonctions afin que MAPI et le spouleur MAPI peuvent ouvrir une session sur le fournisseur de banque de messages.</span><span class="sxs-lookup"><span data-stu-id="1bea1-111">After you have initialized a wrapped PST store provider, you must implement functions so that MAPI and the MAPI spooler can log onto the message store provider.</span></span> <span data-ttu-id="1bea1-112">Pour plus d’informations, consultez [Ouverture de session à un fournisseur de magasin PST encapsulé](logging-on-to-a-wrapped-pst-store-provider.md).</span><span class="sxs-lookup"><span data-stu-id="1bea1-112">For more information, see [Logging On to a Wrapped PST Store Provider](logging-on-to-a-wrapped-pst-store-provider.md).</span></span>
  
## <a name="initialization-routine"></a><span data-ttu-id="1bea1-113">Routine d’initialisation</span><span class="sxs-lookup"><span data-stu-id="1bea1-113">Initialization routine</span></span>

<span data-ttu-id="1bea1-114">Tous les fournisseurs de magasins PST encapsulés doivent implémenter la fonction **[MSProviderInit](msproviderinit.md)** en tant que point d’entrée pour initialiser la DLL du fournisseur.</span><span class="sxs-lookup"><span data-stu-id="1bea1-114">All wrapped PST store providers must implement the **[MSProviderInit](msproviderinit.md)** function as an entry point to initialize the provider's DLL.</span></span> <span data-ttu-id="1bea1-115">**MSProviderInit** vérifie si le numéro de version de l’interface de fournisseur de service, `ulMAPIVer`, est compatible avec le numéro de version actuelle, `CURRENT_SPI_VERSION`.</span><span class="sxs-lookup"><span data-stu-id="1bea1-115">**MSProviderInit** checks to see if the version number of the service provider interface,  `ulMAPIVer`, is compatible with the current version number,  `CURRENT_SPI_VERSION`.</span></span> <span data-ttu-id="1bea1-116">La fonction enregistre la mémoire MAPI routines de gestion dans le `g_lpAllocateBuffer`, `g_lpAllocateMore`, et `g_lpFreeBuffer` paramètres.</span><span class="sxs-lookup"><span data-stu-id="1bea1-116">The function saves the MAPI memory management routines into the  `g_lpAllocateBuffer`,  `g_lpAllocateMore`, and  `g_lpFreeBuffer` parameters.</span></span> <span data-ttu-id="1bea1-117">Ces routines de gestion de mémoire doivent être utilisées dans l’implémentation du stockage PST encapsulée pour libération et l’allocation de mémoire.</span><span class="sxs-lookup"><span data-stu-id="1bea1-117">These memory management routines should be used throughout the wrapped PST store implementation for memory allocation and deallocation.</span></span> 
  
### <a name="msproviderinit-example"></a><span data-ttu-id="1bea1-118">Exemple MSProviderInit()</span><span class="sxs-lookup"><span data-stu-id="1bea1-118">MSProviderInit() example</span></span>

```cpp
STDINITMETHODIMP MSProviderInit ( 
    HINSTANCE /*hInstance*/, 
    LPMALLOC lpMalloc, 
    LPALLOCATEBUFFER lpAllocateBuffer, 
    LPALLOCATEMORE lpAllocateMore, 
    LPFREEBUFFER lpFreeBuffer, 
    ULONG ulFlags, 
    ULONG ulMAPIVer, 
    ULONG FAR * lpulProviderVer, 
    LPMSPROVIDER FAR * lppMSProvider) 
{ 
    Log(true,"MSProviderInit function called\n"); 
    if (!lppMSProvider || !lpulProviderVer) return MAPI_E_INVALID_PARAMETER; 
    HRESULT hRes = S_OK; 
 
    *lppMSProvider = NULL; 
    *lpulProviderVer = CURRENT_SPI_VERSION; 
    if (ulMAPIVer < CURRENT_SPI_VERSION) 
    { 
        Log(true,"MSProviderInit: The version of the subsystem cannot handle this" 
            + "version of the provider\n"); 
        return MAPI_E_VERSION; 
    } 
 
    Log(true,"MSProviderInit: saving off memory management routines\n"); 
    g_lpAllocateBuffer = lpAllocateBuffer; 
    g_lpAllocateMore = lpAllocateMore; 
    g_lpFreeBuffer = lpFreeBuffer; 
    HMODULE hm = LoadLibrary("C:\\Program Files\\Common Files\\System" + 
        "\\MSMAPI\\1033\\MSPST32.dll" ); 
    if (!hm) hm = LoadLibrary("C:\\Program Files\\Microsoft Office\\Office12" + 
        "\\MSPST32.dll" ); 
    Log(true,"LoadLibrary returned 0x%08X\n", hm); 
 
    LPMSPROVIDERINIT pMsProviderInit = NULL; 
    if (hm) 
    { 
        pMsProviderInit = (LPMSPROVIDERINIT)GetProcAddress(hm, "MSProviderInit"); 
        Log(true,"GetProcAddress returned 0x%08X\n", pMsProviderInit); 
    } 
    else hRes = E_OUTOFMEMORY; 
    if (pMsProviderInit) 
    { 
        Log(true,"Calling pMsProviderInit\n"); 
        CMSProvider* pWrappedProvider = NULL; 
        LPMSPROVIDER pSyncProviderObj = NULL; 
        hRes = pMsProviderInit( 
            hm,// not hInstance: first param is handle of module in which the function lives 
            lpMalloc, 
            lpAllocateBuffer, 
            lpAllocateMore, 
            lpFreeBuffer, 
            ulFlags, 
            ulMAPIVer, 
            lpulProviderVer, 
            &pSyncProviderObj                         
            ); 
        Log(true,"pMsProviderInit returned 0x%08X\n", hRes); 
        if (SUCCEEDED(hRes)) 
        { 
            pWrappedProvider = new CMSProvider (pSyncProviderObj); 
            if (NULL == pWrappedProvider) 
            { 
                Log(true,"MSProviderInit: Failed to allocate new CMSProvider object\n"); 
                hRes = E_OUTOFMEMORY; 
            } 
            // Copy pointer to the allocated object back into the  
            //return IMSProvider object pointer 
            *lppMSProvider = pWrappedProvider; 
        } 
    } 
    else hRes = E_OUTOFMEMORY; 
    return hRes; 
}
```

### <a name="wrapped-pst-and-unicode-paths"></a><span data-ttu-id="1bea1-119">Chemins d’accès des fichiers PST et Unicode encapsulés</span><span class="sxs-lookup"><span data-stu-id="1bea1-119">Wrapped PST and Unicode paths</span></span>

<span data-ttu-id="1bea1-120">Pour adapter l’exemple d’origine préparé dans Microsoft Visual Studio 2008 à utiliser des chemins d’accès Unicode NST pour prenant en charge Unicode Microsoft Outlook 2010 et Outlook 2013, utilisez la routine **CreateStoreEntryID** , ce qui génère l’identificateur d’entrée, un format pour les chemins d’accès ASCII et l’autre pour les chemins d’accès Unicode.</span><span class="sxs-lookup"><span data-stu-id="1bea1-120">To retrofit the original sample prepared in Microsoft Visual Studio 2008 to use Unicode paths to the NST for use in Unicode-enabled Microsoft Outlook 2010 and Outlook 2013, the **CreateStoreEntryID** routine, which produces the entry identifier, should use one format for ASCII paths, and another for Unicode paths.</span></span> <span data-ttu-id="1bea1-121">Ils sont représentés sous forme de structures dans l’exemple suivant.</span><span class="sxs-lookup"><span data-stu-id="1bea1-121">These are represented as structures in the following example.</span></span> 
  
```cpp
typedef struct                              // short format
{
         BYTE             rgbFlags[4];     // MAPI-defined flags
         MAPIUID          uid;             // PST provider MUID
         BYTE             bReserved;       // Reserved (must be zero)
         CHAR             szPath[1];       // Full path to store (ASCII)
 } EIDMS;
// Unicode version of EIDMSW is an extension of EIDMS
// and szPath is always NULL
typedef struct                              // Long format to support Unicode path and name
{
         BYTE             rgbFlags[4];     // MAPI-defined flags
         MAPIUID          uid;             // PST provider MUID
         BYTE             bReserved;       // Reserved (must be zero)
         CHAR             szPath[1];       // ASCII path to store is always NULL
         WCHAR            wzPath[1];       // Full path to store (Unicode)
} EIDMSW;
```

> [!IMPORTANT]
> <span data-ttu-id="1bea1-122">Les différences entre ces structures sont deux octets NULL avant un chemin d’accès Unicode.</span><span class="sxs-lookup"><span data-stu-id="1bea1-122">The differences in these structures are two NULL bytes prior to a Unicode path.</span></span> <span data-ttu-id="1bea1-123">Si vous devez interpréter l’identificateur d’entrée dans le « Service entrée Routine » qui suit, pour déterminer si tel est le cas ou non serait d’effectuer un cast comme EIDMS tout d’abord, puis vérifiez si le szPath [0] est NULL.</span><span class="sxs-lookup"><span data-stu-id="1bea1-123">If you need to interpret the entry identifier in the "Service Entry Routine" that follows, one way to determine whether that is the case or not would be to cast as EIDMS first, then check whether the szPath[0] is NULL.</span></span> <span data-ttu-id="1bea1-124">S’il s’agit, convertissez-le en tant que EIDMSW à la place.</span><span class="sxs-lookup"><span data-stu-id="1bea1-124">If it is, cast it as EIDMSW instead.</span></span> 
  
## <a name="service-entry-routine"></a><span data-ttu-id="1bea1-125">Routine d’entrée de service</span><span class="sxs-lookup"><span data-stu-id="1bea1-125">Service Entry routine</span></span>

<span data-ttu-id="1bea1-126">La fonction **[MSGSERVICEENTRY](msgserviceentry.md)** est le point d’entrée de service message où le fournisseur de banque PST encapsulé est configuré.</span><span class="sxs-lookup"><span data-stu-id="1bea1-126">The **[MSGSERVICEENTRY](msgserviceentry.md)** function is the message service entry point where the wrapped PST store provider is configured.</span></span> <span data-ttu-id="1bea1-127">Les appels de fonction `GetMemAllocRoutines()` pour obtenir des routines de gestion de la mémoire MAPI.</span><span class="sxs-lookup"><span data-stu-id="1bea1-127">The function calls  `GetMemAllocRoutines()` to get the MAPI memory management routines.</span></span> <span data-ttu-id="1bea1-128">La fonction utilise le `lpProviderAdmin` paramètre pour rechercher la section profil pour le fournisseur et définit les propriétés du profil.</span><span class="sxs-lookup"><span data-stu-id="1bea1-128">The function uses the  `lpProviderAdmin` parameter to locate the profile section for the provider and sets the properties in the profile.</span></span> 
  
### <a name="serviceentry-example"></a><span data-ttu-id="1bea1-129">Exemple ServiceEntry()</span><span class="sxs-lookup"><span data-stu-id="1bea1-129">ServiceEntry() example</span></span>

```cpp
HRESULT STDAPICALLTYPE ServiceEntry ( 
    HINSTANCE /*hInstance*/, 
    LPMALLOC lpMalloc, 
    LPMAPISUP lpMAPISup, 
    ULONG ulUIParam, 
    ULONG ulFlags, 
    ULONG ulContext, 
    ULONG cValues, 
    LPSPropValue lpProps, 
    LPPROVIDERADMIN lpProviderAdmin, 
    LPMAPIERROR FAR *lppMapiError) 
{ 
    if (!lpMAPISup || !lpProviderAdmin) return MAPI_E_INVALID_PARAMETER; 
    HRESULT         hRes = S_OK; 
    Log(true,"ServiceEntry function called\n"); 
    Log(true,"About to call NSTServiceEntry\n"); 
 
    if (MSG_SERVICE_INSTALL         == ulContext || 
        MSG_SERVICE_DELETE            == ulContext || 
        MSG_SERVICE_UNINSTALL        == ulContext || 
        MSG_SERVICE_PROVIDER_CREATE == ulContext || 
        MSG_SERVICE_PROVIDER_DELETE == ulContext) 
    { 
        // These contexts are not supported 
        return MAPI_E_NO_SUPPORT; 
    } 
 
    // Get memory routines 
    hRes = lpMAPISup-> 
        GetMemAllocRoutines(&g_lpAllocateBuffer,&g_lpAllocateMore,&g_lpFreeBuffer); 
    HMODULE hm = LoadLibrary("C:\\Program Files\\Common Files\\System" + 
        "\\MSMAPI\\1033\\MSPST32.dll" ); 
    if (!hm) hm = LoadLibrary("C:\\Program Files\\Microsoft Office\\Office12" + 
        "\\MSPST32.dll" ); 
    Log(true, "Got module 0x%08X\n", hm); 
    if (!hm) return E_OUTOFMEMORY; 
    LPMSGSERVICEENTRY pNSTServiceEntry =  
        (LPMSGSERVICEENTRY)GetProcAddress(hm, "NSTServiceEntry"); 
    Log(true, "Got procaddress  0x%08X\n", pNSTServiceEntry); 
    if (!pNSTServiceEntry) return E_OUTOFMEMORY; 
 
    // Get profile section 
    LPPROFSECT lpProfSect = NULL; 
    hRes = lpProviderAdmin-> 
        OpenProfileSection((LPMAPIUID) NULL, NULL, MAPI_MODIFY, &lpProfSect); 
    // Set passed in props into the profile 
    if (lpProps && cValues) 
    { 
        hRes = lpProfSect->SetProps(cValues,lpProps,NULL); 
    } 
    // Make sure there is a store path set 
    if (SUCCEEDED(hRes)) hRes = SetOfflineStoreProps(lpProfSect,ulUIParam); 
    ULONG            ulProfProps = 0; 
    LPSPropValue    lpProfProps = NULL; 
 
    // Evaluate props 
    hRes = lpProfSect->GetProps((LPSPropTagArray)&sptClientProps, 
                                fMapiUnicode, 
                                &ulProfProps, 
                                &lpProfProps); 
    if (SUCCEEDED(hRes)) 
    { 
        CSupport * pMySup = NULL; 
        pMySup = new CSupport(lpMAPISup, lpProfSect); 
        if (!pMySup) 
        { 
            Log(true,"MSProviderInit: Failed to allocate new CSupport object\n"); 
            hRes = E_OUTOFMEMORY; 
        } 
        if (SUCCEEDED(hRes)) 
        { 
            hRes = pNSTServiceEntry( 
                hm,  
                lpMalloc, 
                pMySup, 
                ulUIParam, 
                ulFlags, 
                ulContext, 
                ulProfProps, 
                lpProfProps, 
                NULL,//pAdminProvObj, //Don't pass this when creating an NST 
                lppMapiError); 
            if (SUCCEEDED(hRes)) 
            { 
                // Finish setting up the profile 
                hRes = InitStoreProps( 
                    lpMAPISup,  
                    lpProfSect,  
                    lpProviderAdmin); 
                hRes = lpProfSect->SaveChanges(KEEP_OPEN_READWRITE); 
            } 
        } 
    } 
    Log(true, "Ran pNSTServiceEntry 0x%08X\n", hRes); 
    MyFreeBuffer(lpProfProps); 
    if (lpProfSect) lpProfSect->Release(); 
 
    return hRes; 
}
```

## <a name="see-also"></a><span data-ttu-id="1bea1-130">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="1bea1-130">See also</span></span>

- [<span data-ttu-id="1bea1-131">À propos de l’exemple de wrapper fournisseur de banque de dossiers personnels</span><span class="sxs-lookup"><span data-stu-id="1bea1-131">About the Sample Wrapped PST Store Provider</span></span>](about-the-sample-wrapped-pst-store-provider.md)
- [<span data-ttu-id="1bea1-132">Installation de l’exemple de wrapper fournisseur de banque de dossiers personnels</span><span class="sxs-lookup"><span data-stu-id="1bea1-132">Installing the Sample Wrapped PST Store Provider</span></span>](installing-the-sample-wrapped-pst-store-provider.md)
- [<span data-ttu-id="1bea1-133">Se connecter à un fournisseur de banque de dossiers personnels encapsulé</span><span class="sxs-lookup"><span data-stu-id="1bea1-133">Logging On to a Wrapped PST Store Provider</span></span>](logging-on-to-a-wrapped-pst-store-provider.md)
- [<span data-ttu-id="1bea1-134">À l’aide d’un fournisseur de banque de dossiers personnels encapsulé</span><span class="sxs-lookup"><span data-stu-id="1bea1-134">Using a Wrapped PST Store Provider</span></span>](using-a-wrapped-pst-store-provider.md)
- [<span data-ttu-id="1bea1-135">Arrêt d’un fournisseur de banque de dossiers personnels encapsulé</span><span class="sxs-lookup"><span data-stu-id="1bea1-135">Shutting Down a Wrapped PST Store Provider</span></span>](shutting-down-a-wrapped-pst-store-provider.md)

