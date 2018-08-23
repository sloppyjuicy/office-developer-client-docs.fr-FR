---
title: Se connecter à un fournisseur de magasin PST encapsulé
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
ms.assetid: 364bc5fd-2199-0bb2-142b-9b3b686b2268
description: 'Dernière modification : 02 juillet 2012'
ms.openlocfilehash: 0716017788239c22f31007438089118d109010a3
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/23/2018
ms.locfileid: "22570477"
---
# <a name="logging-on-to-a-wrapped-pst-store-provider"></a><span data-ttu-id="27415-103">Se connecter à un fournisseur de magasin PST encapsulé</span><span class="sxs-lookup"><span data-stu-id="27415-103">Logging on to a wrapped PST store provider</span></span>

<span data-ttu-id="27415-104">**S’applique à**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="27415-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="27415-105">Avant de session MAPI à un fournisseur de magasin PST encapsulé, vous devez initialiser et configurer le fournisseur de banque encapsulé dossiers personnels (PST) de fichier.</span><span class="sxs-lookup"><span data-stu-id="27415-105">Before you can log on MAPI to a wrapped PST store provider, you must initialize and configure the wrapped Personal Folders file (PST) store provider.</span></span> <span data-ttu-id="27415-106">Pour plus d’informations, voir [l’initialisation d’un fournisseur de magasins encapsulé PST](initializing-a-wrapped-pst-store-provider.md).</span><span class="sxs-lookup"><span data-stu-id="27415-106">For more information, see [Initializing a Wrapped PST Store Provider](initializing-a-wrapped-pst-store-provider.md).</span></span>
  
<span data-ttu-id="27415-107">Après avoir initialisé et configuré un fournisseur de magasins PST encapsulé, vous devez implémenter deux routines d’ouverture de session.</span><span class="sxs-lookup"><span data-stu-id="27415-107">After you have initialized and configured a wrapped PST store provider, you must implement two logon routines.</span></span> <span data-ttu-id="27415-108">La fonction **[IMSProvider::Logon](imsprovider-logon.md)** ouvre une session MAPI pour le fournisseur de banque PST justifié.</span><span class="sxs-lookup"><span data-stu-id="27415-108">The **[IMSProvider::Logon](imsprovider-logon.md)** function logs on MAPI to the wrapped PST store provider.</span></span> <span data-ttu-id="27415-109">La fonction **[IMSProvider::SpoolerLogon](imsprovider-spoolerlogon.md)** se connecte le spouleur MAPI pour le fournisseur de banque PST justifié.</span><span class="sxs-lookup"><span data-stu-id="27415-109">The **[IMSProvider::SpoolerLogon](imsprovider-spoolerlogon.md)** function logs on the MAPI spooler to the wrapped PST store provider.</span></span> 
  
<span data-ttu-id="27415-110">Dans cette rubrique, la fonction **IMSProvider::Logon** et la fonction **IMSProvider::SpoolerLogon** sont illustrées à l’aide des exemples de code à partir du fournisseur de magasin exemple encapsulé PST.</span><span class="sxs-lookup"><span data-stu-id="27415-110">In this topic, the **IMSProvider::Logon** function and the **IMSProvider::SpoolerLogon** function are demonstrated by using code examples from the Sample Wrapped PST Store Provider.</span></span> <span data-ttu-id="27415-111">L’exemple implémente un fournisseur PST renvoyé à la ligne qui est destiné à être utilisé conjointement avec l’API de réplication.</span><span class="sxs-lookup"><span data-stu-id="27415-111">The sample implements a wrapped PST provider that is intended to be used in conjunction with the Replication API.</span></span> <span data-ttu-id="27415-112">Pour plus d’informations sur le téléchargement et l’installation du fournisseur de magasin exemple encapsulé PST, voir [installer le fournisseur de banque exemple encapsulé PST](installing-the-sample-wrapped-pst-store-provider.md).</span><span class="sxs-lookup"><span data-stu-id="27415-112">For more information about downloading and installing the Sample Wrapped PST Store Provider, see [Installing the Sample Wrapped PST Store Provider](installing-the-sample-wrapped-pst-store-provider.md).</span></span> <span data-ttu-id="27415-113">Pour plus d’informations sur l’API de réplication, consultez la rubrique [Sur l’API de réplication](about-the-replication-api.md).</span><span class="sxs-lookup"><span data-stu-id="27415-113">For more information about the Replication API, see [About the Replication API](about-the-replication-api.md).</span></span>
  
<span data-ttu-id="27415-114">Une fois que MAPI et le spouleur MAPI sont enregistrés sur le fichier PST renvoyé à la ligne fournisseur de magasins, il est prêt à être utilisé.</span><span class="sxs-lookup"><span data-stu-id="27415-114">After MAPI and the MAPI spooler are logged on to the wrapped PST store provider, it is ready to be used.</span></span> <span data-ttu-id="27415-115">Pour plus d’informations, voir [utilisation d’un fournisseur de magasin PST encapsulé](using-a-wrapped-pst-store-provider.md).</span><span class="sxs-lookup"><span data-stu-id="27415-115">For more information, see [Using a Wrapped PST Store Provider](using-a-wrapped-pst-store-provider.md).</span></span>
  
## <a name="mapi-logon-routine"></a><span data-ttu-id="27415-116">Routine d’ouverture de session MAPI</span><span class="sxs-lookup"><span data-stu-id="27415-116">MAPI Logon routine</span></span>

<span data-ttu-id="27415-117">Une fois que le fournisseur de banque PST encapsulé est initialisé, vous devez implémenter la fonction **[IMSProvider::Logon](imsprovider-logon.md)** pour ouvrir une session MAPI sur le magasin de fichiers PST justifié.</span><span class="sxs-lookup"><span data-stu-id="27415-117">After the wrapped PST store provider is initialized, you must implement the **[IMSProvider::Logon](imsprovider-logon.md)** function to log on MAPI to the wrapped PST store.</span></span> <span data-ttu-id="27415-118">Cette fonction valide les informations d’identification utilisateur et obtient les propriétés de configuration pour le fournisseur.</span><span class="sxs-lookup"><span data-stu-id="27415-118">This function validates user credentials and gets the configuration properties for the provider.</span></span> <span data-ttu-id="27415-119">Vous devez également implémenter la `SetOLFIInOST` fonction pour définir les informations de fichier en mode hors connexion (**[OLFI](olfi.md)** ).</span><span class="sxs-lookup"><span data-stu-id="27415-119">You must also implement the  `SetOLFIInOST` function to set the Offline File Info (**[OLFI](olfi.md)** ).</span></span> <span data-ttu-id="27415-120">**OLFI** est une file d’attente des structures d’ID à long terme qui est utilisée par le fournisseur de banque PST encapsulé pour attribuer un ID d’entrée pour un nouveau message ou un dossier en mode hors connexion.</span><span class="sxs-lookup"><span data-stu-id="27415-120">**OLFI** is a queue of long-term ID structures that is used by the wrapped PST store provider to assign an Entry ID for a new message or folder in offline mode.</span></span> <span data-ttu-id="27415-121">Enfin, la fonction **IMSProvider::Logon** renvoie un objet de banque de messages qui les applications MAPI spouleur et le client peuvent se connecter à la `ppMDB` paramètre.</span><span class="sxs-lookup"><span data-stu-id="27415-121">Finally, the **IMSProvider::Logon** function returns a message store object that the MAPI spooler and client applications can log on to in the  `ppMDB` parameter.</span></span> 
  
### <a name="cmsproviderlogon-example"></a><span data-ttu-id="27415-122">Exemple CMSProvider::Logon()</span><span class="sxs-lookup"><span data-stu-id="27415-122">CMSProvider::Logon() example</span></span>

```cpp
STDMETHODIMP CMSProvider::Logon( 
    LPMAPISUP pSupObj, 
    ULONG ulUIParam, 
    LPTSTR pszProfileName, 
    ULONG cbEntryID, 
    LPENTRYID pEntryID, 
    ULONG ulFlags, 
    LPCIID pInterface, 
    ULONG * pcbSpoolSecurity, 
    LPBYTE * ppbSpoolSecurity, 
    LPMAPIERROR * ppMAPIError, 
    LPMSLOGON * ppMSLogon, 
    LPMDB * ppMDB) 
{ 
    HRESULT hRes = S_OK; 
    LPMDB lpPSTMDB = NULL; 
    CMsgStore* pWrappedMDB = NULL; 
 
    Log(true,"CMSProvider::Logon Pst logon Called\n"); 
 
    LPPROFSECT lpProfSect = NULL; 
    CSupport * pMySup = NULL; 
    hRes = GetGlobalProfileObject(pSupObj,&lpProfSect); 
    pMySup = new CSupport(pSupObj, lpProfSect); 
    if (!pMySup) 
    { 
        Log(true,"CMSProvider::Logon: Failed to allocate new CSupport object\n"); 
        hRes = E_OUTOFMEMORY; 
    } 
    if (SUCCEEDED(hRes)) 
    { 
        ulFlags = (ulFlags & ~MDB_OST_LOGON_ANSI) | MDB_OST_LOGON_UNICODE; 
        hRes = m_pPSTMS->Logon( 
            pMySup, 
            ulUIParam,  
            pszProfileName,  
            cbEntryID, 
            pEntryID,  
            ulFlags,  
            pInterface,  
            pcbSpoolSecurity, 
            ppbSpoolSecurity,  
            ppMAPIError,  
            ppMSLogon,  
            &lpPSTMDB); 
    } 
    Log(true,"CMSProvider::Logon returned 0x%08X\n", hRes); 
 
    // Set up the MDB to allow synchronization 
    if (SUCCEEDED(hRes)) 
    { 
        hRes = SetOLFIInOST(lpPSTMDB); 
        Log(true,"SetOLFIInOST returned 0x%08X\n", hRes); 
    } 
    // Wrap the outgoing MDB 
    pWrappedMDB = new CMsgStore (lpPSTMDB); 
    if (NULL == pWrappedMDB) 
    { 
        Log(true,"CMSProvider::Logon: Failed to allocate new CMsgStore object\n"); 
        hRes = E_OUTOFMEMORY; 
    } 
    // Copy pointer to the allocated object back into the return LPMDB object pointer 
    *ppMDB = pWrappedMDB; 
    if (lpProfSect) lpProfSect->Release(); 
 
    return hRes; 
}
```

## <a name="mapi-spooler-logon-routine"></a><span data-ttu-id="27415-123">Routine d’ouverture de session MAPI spouleur</span><span class="sxs-lookup"><span data-stu-id="27415-123">MAPI Spooler Logon routine</span></span>

<span data-ttu-id="27415-124">Similaire aux **IMSProvider::Logon**, vous devez implémenter la fonction **[IMSProvider::SpoolerLogon](imsprovider-spoolerlogon.md)** pour enregistrer le spouleur MAPI sur la banque de dossiers personnels encapsulé.</span><span class="sxs-lookup"><span data-stu-id="27415-124">Similar to **IMSProvider::Logon**, you must implement the **[IMSProvider::SpoolerLogon](imsprovider-spoolerlogon.md)** function to log the MAPI spooler on to the wrapped PST store.</span></span> <span data-ttu-id="27415-125">Un objet de banque de message peuvent ouvrir une session sur les applications de client et spouleur MAPI est retourné dans le `ppMDB` paramètre.</span><span class="sxs-lookup"><span data-stu-id="27415-125">A message store object that the MAPI spooler and client applications can log on to is returned in the  `ppMDB` parameter.</span></span> 
  
### <a name="cmsproviderspoolerlogon-example"></a><span data-ttu-id="27415-126">Exemple CMSProvider::SpoolerLogon()</span><span class="sxs-lookup"><span data-stu-id="27415-126">CMSProvider::SpoolerLogon() example</span></span>

```cpp
STDMETHODIMP CMSProvider::SpoolerLogon ( 
    LPMAPISUP pSupObj, 
    ULONG ulUIParam, 
    LPTSTR pszProfileName, 
    ULONG cbEntryID, 
    LPENTRYID pEntryID, 
    ULONG ulFlags, 
    LPCIID pInterface, 
    ULONG cbSpoolSecurity, 
    LPBYTE pbSpoolSecurity, 
    LPMAPIERROR * ppMAPIError, 
    LPMSLOGON * ppMSLogon, 
    LPMDB * ppMDB) 
{ 
    HRESULT hRes = S_OK; 
     
    Log(true,"CMSProvider::SpoolerLogon\n"); 
    LPPROFSECT lpProfSect = NULL; 
    CSupport * pMySup = NULL; 
    hRes = GetGlobalProfileObject(pSupObj,&lpProfSect); 
    pMySup = new CSupport(pSupObj, lpProfSect); 
    if (!pMySup) 
    { 
        Log(true,"CMSProvider::SpoolerLogon: " + 
            "Failed to allocate new CSupport object\n"); 
        hRes = E_OUTOFMEMORY; 
    } 
    if (SUCCEEDED(hRes)) 
    { 
        hRes = m_pPSTMS->SpoolerLogon(  
            pMySup,//pSupObj, 
            ulUIParam, 
            pszProfileName, 
            cbEntryID, 
            pEntryID, 
            ulFlags, 
            pInterface, 
            cbSpoolSecurity, 
            pbSpoolSecurity, 
            ppMAPIError, 
            ppMSLogon, 
            ppMDB); 
    } 
    Log(true,"CMSProvider::SpoolerLogon returned 0x%08X\n", hRes); 
 
    return hRes; 
}
```

## <a name="see-also"></a><span data-ttu-id="27415-127">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="27415-127">See also</span></span>

- [<span data-ttu-id="27415-128">À propos de l’exemple de fournisseur d’archive PST encapsulée</span><span class="sxs-lookup"><span data-stu-id="27415-128">About the Sample Wrapped PST Store Provider</span></span>](about-the-sample-wrapped-pst-store-provider.md) 
- [<span data-ttu-id="27415-129">Installation de l’exemple de fournisseur d’archive PST encapsulée</span><span class="sxs-lookup"><span data-stu-id="27415-129">Installing the Sample Wrapped PST Store Provider</span></span>](installing-the-sample-wrapped-pst-store-provider.md) 
- [<span data-ttu-id="27415-130">Initialisation d’un fournisseur d’archive PST encapsulée</span><span class="sxs-lookup"><span data-stu-id="27415-130">Initializing a Wrapped PST Store Provider</span></span>](initializing-a-wrapped-pst-store-provider.md)
- [<span data-ttu-id="27415-131">Utilisation d’un fournisseur d’archive PST encapsulée</span><span class="sxs-lookup"><span data-stu-id="27415-131">Using a Wrapped PST Store Provider</span></span>](using-a-wrapped-pst-store-provider.md)
- [<span data-ttu-id="27415-132">Arrêt d’un fournisseur d’archive PST encapsulée</span><span class="sxs-lookup"><span data-stu-id="27415-132">Shutting Down a Wrapped PST Store Provider</span></span>](shutting-down-a-wrapped-pst-store-provider.md)

