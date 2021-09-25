---
title: Initialisation d’un fournisseur d’archive PST encapsulée
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.localizationpriority: medium
ms.assetid: 07633717-ba4c-b146-ad65-60b37ab98ab6
description: 'Last modified: October 05, 2012'
ms.openlocfilehash: 3601e359eef6d798170d10e2debcb3613245f30c
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/24/2021
ms.locfileid: "59571653"
---
# <a name="initializing-a-wrapped-pst-store-provider"></a>Initialisation d’un fournisseur d’archive PST encapsulée

**S’applique à** : Outlook 2013 | Outlook 2016 
  
Pour implémenter un fournisseur de magasins de dossiers personnels wrapped (PST), vous devez initialiser le fournisseur de magasin PST wrapped en utilisant la fonction **[MSProviderInit](msproviderinit.md)** comme point d’entrée. Une fois la DLL du fournisseur initialisée, la fonction **[MSGSERVICEENTRY](msgserviceentry.md)** configure le fournisseur de magasins PST wrapped. 
  
Dans cette rubrique, les fonctions **MSProviderInit** et **MSGSERVICEENTRY** sont démontrées à l’aide d’exemples de code provenant du fournisseur de magasin PST Wrapped sample. L’exemple implémente un fournisseur PST wrapped qui est destiné à être utilisé conjointement avec l’API de réplication. Pour plus d’informations sur le téléchargement et l’installation de l’exemple de fournisseur de magasin PST [Wrapped, voir Installing the Sample Wrapped PST Store Provider](installing-the-sample-wrapped-pst-store-provider.md). Pour plus d’informations sur l’API de réplication, voir [à propos de l’API de réplication.](about-the-replication-api.md)
  
Après avoir initialisé un fournisseur de magasins PST wrapped, vous devez implémenter des fonctions afin que MAPI et lepooler MAPI se connectent au fournisseur de la boutique de messages. Pour plus d’informations, voir Connexion à un fournisseur de magasin [PST Wrapped.](logging-on-to-a-wrapped-pst-store-provider.md)
  
## <a name="initialization-routine"></a>Routine d’initialisation

Tous les fournisseurs de magasins PST wrapped doivent implémenter la fonction **[MSProviderInit](msproviderinit.md)** comme point d’entrée pour initialiser la DLL du fournisseur. **MSProviderInit vérifie** si le numéro de version de l’interface du fournisseur de services, est compatible avec le `ulMAPIVer` numéro de version actuel. `CURRENT_SPI_VERSION` La fonction enregistre les routines de gestion de la mémoire MAPI dans  `g_lpAllocateBuffer`  `g_lpAllocateMore` les paramètres et les  `g_lpFreeBuffer` paramètres. Ces routines de gestion de mémoire doivent être utilisées tout au long de l’implémentation du magasin PST wrapped pour l’allocation et la déallocation de la mémoire. 
  
### <a name="msproviderinit-example"></a>Exemple MSProviderInit()

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

### <a name="wrapped-pst-and-unicode-paths"></a>Chemins PST et Unicode wrapped

Pour moderniser l’exemple d’origine préparé dans Microsoft Visual Studio 2008 afin d’utiliser des chemins Unicode vers le NST pour une utilisation dans les Microsoft Outlook 2010 et Outlook 2013, la routine **CreateStoreEntryID,** qui produit l’identificateur d’entrée, doit utiliser un format pour les chemins ASCII et un autre pour les chemins Unicode. Ils sont représentés en tant que structures dans l’exemple suivant. 
  
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
> Les différences entre ces structures sont de deux octets NULL avant un chemin Unicode. Si vous avez besoin d’interpréter l’identificateur d’entrée dans la « Routine d’entrée de service » qui suit, une façon de déterminer si c’est le cas ou non serait d’abord d’être casté en tant que EIDMS, puis vérifiez si le szPath[0] est NULL. Si c’est le cas, castez-le en tant que EIDMSW à la place. 
  
## <a name="service-entry-routine"></a>Routine d’entrée de service

La **[fonction MSGSERVICEENTRY](msgserviceentry.md)** est le point d’entrée du service de messagerie où le fournisseur de magasins PST wrapped est configuré. La fonction appelle pour obtenir les routines de gestion de mémoire  `GetMemAllocRoutines()` MAPI. La fonction utilise le paramètre pour localiser la section de profil pour le fournisseur et  `lpProviderAdmin` définit les propriétés dans le profil. 
  
### <a name="serviceentry-example"></a>Exemple ServiceEntry()

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

## <a name="see-also"></a>Voir aussi

- [À propos de l’exemple de fournisseur de magasins PST wrapped](about-the-sample-wrapped-pst-store-provider.md)
- [Installation de l’exemple de fournisseur de magasin PST Wrapped](installing-the-sample-wrapped-pst-store-provider.md)
- [Connexion à un fournisseur de magasin PST wrapped](logging-on-to-a-wrapped-pst-store-provider.md)
- [Utilisation d’un fournisseur de magasin PST wrapped](using-a-wrapped-pst-store-provider.md)
- [Arrêt d’un fournisseur de magasin PST wrapped](shutting-down-a-wrapped-pst-store-provider.md)

