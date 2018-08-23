---
title: L’initialisation d’un fournisseur de magasins PST encapsulé
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
ms.assetid: 07633717-ba4c-b146-ad65-60b37ab98ab6
description: 'Dernière modification : 05 octobre 2012'
ms.openlocfilehash: c39f66917ecc080785b3a3e91506d3994427ca62
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/23/2018
ms.locfileid: "22569077"
---
# <a name="initializing-a-wrapped-pst-store-provider"></a>L’initialisation d’un fournisseur de magasins PST encapsulé

**S’applique à**: Outlook 2013 | Outlook 2016 
  
Pour implémenter un fournisseur de magasin de dossiers personnels (PST) de fichier encapsulé, vous devez initialiser le fournisseur de banque PST encapsulé à l’aide de la fonction **[MSProviderInit](msproviderinit.md)** comme point d’entrée. Une fois que la DLL du fournisseur est initialisée, la fonction **[MSGSERVICEENTRY](msgserviceentry.md)** configure le fournisseur de banque PST justifié. 
  
Dans cette rubrique, la fonction **MSProviderInit** et la fonction **MSGSERVICEENTRY** sont illustrées à l’aide des exemples de code à partir du fournisseur de magasin exemple encapsulé PST. L’exemple implémente un fournisseur PST renvoyé à la ligne qui est destiné à être utilisé conjointement avec l’API de réplication. Pour plus d’informations sur le téléchargement et l’installation du fournisseur de magasin exemple encapsulé PST, voir [installer le fournisseur de banque exemple encapsulé PST](installing-the-sample-wrapped-pst-store-provider.md). Pour plus d’informations sur l’API de réplication, consultez la rubrique [Sur l’API de réplication](about-the-replication-api.md).
  
Une fois que vous avez initialisé un fournisseur de magasins PST encapsulé, vous devez implémenter les fonctions afin que MAPI et le spouleur MAPI peuvent ouvrir une session sur le fournisseur de banque de messages. Pour plus d’informations, consultez [Ouverture de session à un fournisseur de magasin PST encapsulé](logging-on-to-a-wrapped-pst-store-provider.md).
  
## <a name="initialization-routine"></a>Routine d’initialisation

Tous les fournisseurs de magasins PST encapsulés doivent implémenter la fonction **[MSProviderInit](msproviderinit.md)** en tant que point d’entrée pour initialiser la DLL du fournisseur. **MSProviderInit** vérifie si le numéro de version de l’interface de fournisseur de service, `ulMAPIVer`, est compatible avec le numéro de version actuelle, `CURRENT_SPI_VERSION`. La fonction enregistre la mémoire MAPI routines de gestion dans le `g_lpAllocateBuffer`, `g_lpAllocateMore`, et `g_lpFreeBuffer` paramètres. Ces routines de gestion de mémoire doivent être utilisées dans l’implémentation du stockage PST encapsulée pour libération et l’allocation de mémoire. 
  
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

### <a name="wrapped-pst-and-unicode-paths"></a>Chemins d’accès des fichiers PST et Unicode encapsulés

Pour adapter l’exemple d’origine préparé dans Microsoft Visual Studio 2008 à utiliser des chemins d’accès Unicode NST pour prenant en charge Unicode Microsoft Outlook 2010 et Outlook 2013, utilisez la routine **CreateStoreEntryID** , ce qui génère l’identificateur d’entrée, un format pour les chemins d’accès ASCII et l’autre pour les chemins d’accès Unicode. Ils sont représentés sous forme de structures dans l’exemple suivant. 
  
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
> Les différences entre ces structures sont deux octets NULL avant un chemin d’accès Unicode. Si vous devez interpréter l’identificateur d’entrée dans le « Service entrée Routine » qui suit, pour déterminer si tel est le cas ou non serait d’effectuer un cast comme EIDMS tout d’abord, puis vérifiez si le szPath [0] est NULL. S’il s’agit, convertissez-le en tant que EIDMSW à la place. 
  
## <a name="service-entry-routine"></a>Routine d’entrée de service

La fonction **[MSGSERVICEENTRY](msgserviceentry.md)** est le point d’entrée de service message où le fournisseur de banque PST encapsulé est configuré. Les appels de fonction `GetMemAllocRoutines()` pour obtenir des routines de gestion de la mémoire MAPI. La fonction utilise le `lpProviderAdmin` paramètre pour rechercher la section profil pour le fournisseur et définit les propriétés du profil. 
  
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

- [À propos de l’exemple de fournisseur d’archive PST encapsulée](about-the-sample-wrapped-pst-store-provider.md)
- [Installation de l’exemple de fournisseur d’archive PST encapsulée](installing-the-sample-wrapped-pst-store-provider.md)
- [Connexion à un fournisseur d’archive PST encapsulée](logging-on-to-a-wrapped-pst-store-provider.md)
- [Utilisation d’un fournisseur d’archive PST encapsulée](using-a-wrapped-pst-store-provider.md)
- [Arrêt d’un fournisseur d’archive PST encapsulée](shutting-down-a-wrapped-pst-store-provider.md)

