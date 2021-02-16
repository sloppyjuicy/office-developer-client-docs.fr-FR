---
title: Connexion à un fournisseur d’archive PST encapsulée
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
ms.assetid: 364bc5fd-2199-0bb2-142b-9b3b686b2268
description: 'Last modified: July 02, 2012'
ms.openlocfilehash: 96f472d67f144a451046ff61a3ed6c6ff2ff9acf
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/28/2019
ms.locfileid: "33408985"
---
# <a name="logging-on-to-a-wrapped-pst-store-provider"></a><span data-ttu-id="2103c-103">Connexion à un fournisseur d’archive PST encapsulée</span><span class="sxs-lookup"><span data-stu-id="2103c-103">Logging on to a wrapped PST store provider</span></span>

<span data-ttu-id="2103c-104">**S’applique à** : Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="2103c-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="2103c-105">Avant de pouvoir vous connecter à MAPI auprès d’un fournisseur de magasins PST wrapped, vous devez initialiser et configurer le fournisseur de magasin de dossiers personnels wrapped (PST).</span><span class="sxs-lookup"><span data-stu-id="2103c-105">Before you can log on MAPI to a wrapped PST store provider, you must initialize and configure the wrapped Personal Folders file (PST) store provider.</span></span> <span data-ttu-id="2103c-106">Pour plus d’informations, [voir Initializing a Wrapped PST Store Provider](initializing-a-wrapped-pst-store-provider.md).</span><span class="sxs-lookup"><span data-stu-id="2103c-106">For more information, see [Initializing a Wrapped PST Store Provider](initializing-a-wrapped-pst-store-provider.md).</span></span>
  
<span data-ttu-id="2103c-107">Après avoir initialisé et configuré un fournisseur de magasin PST wrapped, vous devez implémenter deux routines d’ouverture de contrat.</span><span class="sxs-lookup"><span data-stu-id="2103c-107">After you have initialized and configured a wrapped PST store provider, you must implement two logon routines.</span></span> <span data-ttu-id="2103c-108">La **[fonction IMSProvider::Logon](imsprovider-logon.md)** se connecte sur MAPI au fournisseur de magasin PST wrapped.</span><span class="sxs-lookup"><span data-stu-id="2103c-108">The **[IMSProvider::Logon](imsprovider-logon.md)** function logs on MAPI to the wrapped PST store provider.</span></span> <span data-ttu-id="2103c-109">La **[fonction IMSProvider::SpoolerLogon](imsprovider-spoolerlogon.md)** enregistre lepooler MAPI sur le fournisseur de magasin PST wrapped.</span><span class="sxs-lookup"><span data-stu-id="2103c-109">The **[IMSProvider::SpoolerLogon](imsprovider-spoolerlogon.md)** function logs on the MAPI spooler to the wrapped PST store provider.</span></span> 
  
<span data-ttu-id="2103c-110">Dans cette rubrique, les fonctions **IMSProvider::Logon** et **IMSProvider::SpoolerLogon** sont démontrées à l’aide d’exemples de code du fournisseur de magasin PST Wrapped sample.</span><span class="sxs-lookup"><span data-stu-id="2103c-110">In this topic, the **IMSProvider::Logon** function and the **IMSProvider::SpoolerLogon** function are demonstrated by using code examples from the Sample Wrapped PST Store Provider.</span></span> <span data-ttu-id="2103c-111">L’exemple implémente un fournisseur PST wrapped qui est destiné à être utilisé conjointement avec l’API de réplication.</span><span class="sxs-lookup"><span data-stu-id="2103c-111">The sample implements a wrapped PST provider that is intended to be used in conjunction with the Replication API.</span></span> <span data-ttu-id="2103c-112">Pour plus d’informations sur le téléchargement et l’installation de l’exemple de fournisseur de magasin PST [Wrapped, voir Installing the Sample Wrapped PST Store Provider](installing-the-sample-wrapped-pst-store-provider.md).</span><span class="sxs-lookup"><span data-stu-id="2103c-112">For more information about downloading and installing the Sample Wrapped PST Store Provider, see [Installing the Sample Wrapped PST Store Provider](installing-the-sample-wrapped-pst-store-provider.md).</span></span> <span data-ttu-id="2103c-113">Pour plus d’informations sur l’API de réplication, voir [à propos de l’API de réplication.](about-the-replication-api.md)</span><span class="sxs-lookup"><span data-stu-id="2103c-113">For more information about the Replication API, see [About the Replication API](about-the-replication-api.md).</span></span>
  
<span data-ttu-id="2103c-114">Une fois que MAPI et lepooler MAPI sont connectés au fournisseur de magasin PST wrapped, il est prêt à être utilisé.</span><span class="sxs-lookup"><span data-stu-id="2103c-114">After MAPI and the MAPI spooler are logged on to the wrapped PST store provider, it is ready to be used.</span></span> <span data-ttu-id="2103c-115">Pour plus d’informations, voir [Using a Wrapped PST Store Provider](using-a-wrapped-pst-store-provider.md).</span><span class="sxs-lookup"><span data-stu-id="2103c-115">For more information, see [Using a Wrapped PST Store Provider](using-a-wrapped-pst-store-provider.md).</span></span>
  
## <a name="mapi-logon-routine"></a><span data-ttu-id="2103c-116">Routine d’logo MAPI</span><span class="sxs-lookup"><span data-stu-id="2103c-116">MAPI Logon routine</span></span>

<span data-ttu-id="2103c-117">Une fois le fournisseur de magasin PST wrapped initialisé, vous devez implémenter la fonction **[IMSProvider::Logon](imsprovider-logon.md)** pour vous connecter à MAPI dans le magasin PST wrapped.</span><span class="sxs-lookup"><span data-stu-id="2103c-117">After the wrapped PST store provider is initialized, you must implement the **[IMSProvider::Logon](imsprovider-logon.md)** function to log on MAPI to the wrapped PST store.</span></span> <span data-ttu-id="2103c-118">Cette fonction valide les informations d’identification de l’utilisateur et obtient les propriétés de configuration du fournisseur.</span><span class="sxs-lookup"><span data-stu-id="2103c-118">This function validates user credentials and gets the configuration properties for the provider.</span></span> <span data-ttu-id="2103c-119">Vous devez également implémenter la fonction pour définir les informations de fichier hors  `SetOLFIInOST` connexion (**[OLFI](olfi.md)** ).</span><span class="sxs-lookup"><span data-stu-id="2103c-119">You must also implement the  `SetOLFIInOST` function to set the Offline File Info (**[OLFI](olfi.md)** ).</span></span> <span data-ttu-id="2103c-120">**OLFI** est une file d’attente de structures d’ID à long terme qui est utilisée par le fournisseur de magasin PST wrapped pour affecter un ID d’entrée pour un nouveau message ou dossier en mode hors connexion.</span><span class="sxs-lookup"><span data-stu-id="2103c-120">**OLFI** is a queue of long-term ID structures that is used by the wrapped PST store provider to assign an Entry ID for a new message or folder in offline mode.</span></span> <span data-ttu-id="2103c-121">Enfin, la **fonction IMSProvider::Logon** renvoie un objet de magasin de messages sur qui lepooler MAPI et les applications clientes peuvent se connecter dans le  `ppMDB` paramètre.</span><span class="sxs-lookup"><span data-stu-id="2103c-121">Finally, the **IMSProvider::Logon** function returns a message store object that the MAPI spooler and client applications can log on to in the  `ppMDB` parameter.</span></span> 
  
### <a name="cmsproviderlogon-example"></a><span data-ttu-id="2103c-122">Exemple CMSProvider::Logon()</span><span class="sxs-lookup"><span data-stu-id="2103c-122">CMSProvider::Logon() example</span></span>

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

## <a name="mapi-spooler-logon-routine"></a><span data-ttu-id="2103c-123">Routine d’logo mapi Spooler</span><span class="sxs-lookup"><span data-stu-id="2103c-123">MAPI Spooler Logon routine</span></span>

<span data-ttu-id="2103c-124">Similaire à **IMSProvider::Logon**, vous devez implémenter la fonction **[IMSProvider::SpoolerLogon](imsprovider-spoolerlogon.md)** pour connecter lepooler MAPI au magasin PST wrapped.</span><span class="sxs-lookup"><span data-stu-id="2103c-124">Similar to **IMSProvider::Logon**, you must implement the **[IMSProvider::SpoolerLogon](imsprovider-spoolerlogon.md)** function to log the MAPI spooler on to the wrapped PST store.</span></span> <span data-ttu-id="2103c-125">Un objet de magasin de messages à qui lepooler MAPI et les applications clientes peuvent se connecter est renvoyé dans le  `ppMDB` paramètre.</span><span class="sxs-lookup"><span data-stu-id="2103c-125">A message store object that the MAPI spooler and client applications can log on to is returned in the  `ppMDB` parameter.</span></span> 
  
### <a name="cmsproviderspoolerlogon-example"></a><span data-ttu-id="2103c-126">Exemple CMSProvider::SpoolerLogon()</span><span class="sxs-lookup"><span data-stu-id="2103c-126">CMSProvider::SpoolerLogon() example</span></span>

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

## <a name="see-also"></a><span data-ttu-id="2103c-127">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="2103c-127">See also</span></span>

- [<span data-ttu-id="2103c-128">À propos de l’exemple de fournisseur de magasin PST wrapped</span><span class="sxs-lookup"><span data-stu-id="2103c-128">About the Sample Wrapped PST Store Provider</span></span>](about-the-sample-wrapped-pst-store-provider.md) 
- [<span data-ttu-id="2103c-129">Installation de l’exemple de fournisseur de magasin PST Wrapped</span><span class="sxs-lookup"><span data-stu-id="2103c-129">Installing the Sample Wrapped PST Store Provider</span></span>](installing-the-sample-wrapped-pst-store-provider.md) 
- [<span data-ttu-id="2103c-130">Initialisation d’un fournisseur de magasin PST wrapped</span><span class="sxs-lookup"><span data-stu-id="2103c-130">Initializing a Wrapped PST Store Provider</span></span>](initializing-a-wrapped-pst-store-provider.md)
- [<span data-ttu-id="2103c-131">Utilisation d’un fournisseur de magasin PST wrapped</span><span class="sxs-lookup"><span data-stu-id="2103c-131">Using a Wrapped PST Store Provider</span></span>](using-a-wrapped-pst-store-provider.md)
- [<span data-ttu-id="2103c-132">Arrêt d’un fournisseur de magasin PST wrapped</span><span class="sxs-lookup"><span data-stu-id="2103c-132">Shutting Down a Wrapped PST Store Provider</span></span>](shutting-down-a-wrapped-pst-store-provider.md)

