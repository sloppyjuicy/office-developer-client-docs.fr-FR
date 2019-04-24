---
title: Connexion à un fournisseur d’archive PST encapsulée
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
ms.assetid: 364bc5fd-2199-0bb2-142b-9b3b686b2268
description: 'Dernière modification le: 02 juillet 2012'
ms.openlocfilehash: 96f472d67f144a451046ff61a3ed6c6ff2ff9acf
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32307818"
---
# <a name="logging-on-to-a-wrapped-pst-store-provider"></a><span data-ttu-id="a639e-103">Connexion à un fournisseur d’archive PST encapsulée</span><span class="sxs-lookup"><span data-stu-id="a639e-103">Logging on to a wrapped PST store provider</span></span>

<span data-ttu-id="a639e-104">**S’applique à** : Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="a639e-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="a639e-105">Avant de pouvoir ouvrir une session MAPI sur un fournisseur de magasins PST encapsulé, vous devez initialiser et configurer le fournisseur de magasins de fichiers de dossiers personnels (PST).</span><span class="sxs-lookup"><span data-stu-id="a639e-105">Before you can log on MAPI to a wrapped PST store provider, you must initialize and configure the wrapped Personal Folders file (PST) store provider.</span></span> <span data-ttu-id="a639e-106">Pour plus d'informations, consultez [la rubrique initialisation d'un fournisseur de magasins de fichiers PST encapsulés](initializing-a-wrapped-pst-store-provider.md).</span><span class="sxs-lookup"><span data-stu-id="a639e-106">For more information, see [Initializing a Wrapped PST Store Provider](initializing-a-wrapped-pst-store-provider.md).</span></span>
  
<span data-ttu-id="a639e-107">Une fois que vous avez initialisé et configuré un fournisseur de magasins PST encapsulé, vous devez implémenter deux routines d'ouverture de session.</span><span class="sxs-lookup"><span data-stu-id="a639e-107">After you have initialized and configured a wrapped PST store provider, you must implement two logon routines.</span></span> <span data-ttu-id="a639e-108">La fonction **[IMSProvider:: Logon](imsprovider-logon.md)** ouvre une session MAPI sur le fournisseur de magasins PST encapsulé.</span><span class="sxs-lookup"><span data-stu-id="a639e-108">The **[IMSProvider::Logon](imsprovider-logon.md)** function logs on MAPI to the wrapped PST store provider.</span></span> <span data-ttu-id="a639e-109">La fonction **[IMSProvider:: SpoolerLogon](imsprovider-spoolerlogon.md)** enregistre le spouleur MAPI sur le fournisseur de banque de fichiers PST encapsulé.</span><span class="sxs-lookup"><span data-stu-id="a639e-109">The **[IMSProvider::SpoolerLogon](imsprovider-spoolerlogon.md)** function logs on the MAPI spooler to the wrapped PST store provider.</span></span> 
  
<span data-ttu-id="a639e-110">Dans cette rubrique, la fonction **IMSProvider:: Logon** et la fonction **IMSProvider:: SpoolerLogon** sont démontrées à l'aide d'exemples de code issus de l'exemple de fournisseur de magasins PST encapsulé.</span><span class="sxs-lookup"><span data-stu-id="a639e-110">In this topic, the **IMSProvider::Logon** function and the **IMSProvider::SpoolerLogon** function are demonstrated by using code examples from the Sample Wrapped PST Store Provider.</span></span> <span data-ttu-id="a639e-111">L'exemple implémente un fournisseur PST encapsulé destiné à être utilisé conjointement avec l'API de réPlication.</span><span class="sxs-lookup"><span data-stu-id="a639e-111">The sample implements a wrapped PST provider that is intended to be used in conjunction with the Replication API.</span></span> <span data-ttu-id="a639e-112">Pour plus d'informations sur le téléchargement et l'installation de l'exemple de fournisseur de magasins PST encapsulé, consultez [la rubrique installation de l'exemple de fournisseur de magasins PST encapsulé](installing-the-sample-wrapped-pst-store-provider.md).</span><span class="sxs-lookup"><span data-stu-id="a639e-112">For more information about downloading and installing the Sample Wrapped PST Store Provider, see [Installing the Sample Wrapped PST Store Provider](installing-the-sample-wrapped-pst-store-provider.md).</span></span> <span data-ttu-id="a639e-113">Pour plus d'informations sur l'API de réPlication, voir [à propos de l'API](about-the-replication-api.md)de réplication.</span><span class="sxs-lookup"><span data-stu-id="a639e-113">For more information about the Replication API, see [About the Replication API](about-the-replication-api.md).</span></span>
  
<span data-ttu-id="a639e-114">Une fois que MAPI et le spouleur MAPI sont connectés au fournisseur de magasins PST encapsulé, il est prêt à être utilisé.</span><span class="sxs-lookup"><span data-stu-id="a639e-114">After MAPI and the MAPI spooler are logged on to the wrapped PST store provider, it is ready to be used.</span></span> <span data-ttu-id="a639e-115">Pour plus d'informations, consultez [la rubrique utilisation d'un fournisseur de magasins PST encapsulé](using-a-wrapped-pst-store-provider.md).</span><span class="sxs-lookup"><span data-stu-id="a639e-115">For more information, see [Using a Wrapped PST Store Provider](using-a-wrapped-pst-store-provider.md).</span></span>
  
## <a name="mapi-logon-routine"></a><span data-ttu-id="a639e-116">Routine de connexion MAPI</span><span class="sxs-lookup"><span data-stu-id="a639e-116">MAPI Logon routine</span></span>

<span data-ttu-id="a639e-117">Une fois le fournisseur de banque de fichiers PST encapsulé initialisé, vous devez implémenter la fonction **[IMSProvider:: Logon](imsprovider-logon.md)** pour vous connecter à la Banque de fichiers PST encapsulée via MAPI.</span><span class="sxs-lookup"><span data-stu-id="a639e-117">After the wrapped PST store provider is initialized, you must implement the **[IMSProvider::Logon](imsprovider-logon.md)** function to log on MAPI to the wrapped PST store.</span></span> <span data-ttu-id="a639e-118">Cette fonction valide les informations d'identification de l'utilisateur et obtient les propriétés de configuration pour le fournisseur.</span><span class="sxs-lookup"><span data-stu-id="a639e-118">This function validates user credentials and gets the configuration properties for the provider.</span></span> <span data-ttu-id="a639e-119">Vous devez également implémenter `SetOLFIInOST` la fonction pour définir les informations de fichier hors connexion (**[OLFI](olfi.md)** ).</span><span class="sxs-lookup"><span data-stu-id="a639e-119">You must also implement the  `SetOLFIInOST` function to set the Offline File Info (**[OLFI](olfi.md)** ).</span></span> <span data-ttu-id="a639e-120">**OLFI** est une file d'attente de structures d'ID à long terme utilisée par le fournisseur de magasins PST encapsulé pour affecter un ID d'entrée pour un nouveau message ou dossier en mode hors connexion.</span><span class="sxs-lookup"><span data-stu-id="a639e-120">**OLFI** is a queue of long-term ID structures that is used by the wrapped PST store provider to assign an Entry ID for a new message or folder in offline mode.</span></span> <span data-ttu-id="a639e-121">Enfin, la fonction **IMSProvider:: Logon** renvoie un objet de banque de messages auquel le spouleur MAPI et les applications clientes peuvent `ppMDB` se connecter dans le paramètre.</span><span class="sxs-lookup"><span data-stu-id="a639e-121">Finally, the **IMSProvider::Logon** function returns a message store object that the MAPI spooler and client applications can log on to in the  `ppMDB` parameter.</span></span> 
  
### <a name="cmsproviderlogon-example"></a><span data-ttu-id="a639e-122">CMSProvider:: Logon () exemple</span><span class="sxs-lookup"><span data-stu-id="a639e-122">CMSProvider::Logon() example</span></span>

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

## <a name="mapi-spooler-logon-routine"></a><span data-ttu-id="a639e-123">Routine de connexion du spouleur MAPI</span><span class="sxs-lookup"><span data-stu-id="a639e-123">MAPI Spooler Logon routine</span></span>

<span data-ttu-id="a639e-124">De la même manière que pour **IMSProvider:: Logon**, vous devez implémenter la fonction **[IMSProvider:: SpoolerLogon](imsprovider-spoolerlogon.md)** pour enregistrer le spouleur MAPI sur la Banque de fichiers PST encapsulée.</span><span class="sxs-lookup"><span data-stu-id="a639e-124">Similar to **IMSProvider::Logon**, you must implement the **[IMSProvider::SpoolerLogon](imsprovider-spoolerlogon.md)** function to log the MAPI spooler on to the wrapped PST store.</span></span> <span data-ttu-id="a639e-125">Un objet de banque de messages auquel le spouleur MAPI et les applications clientes peuvent se connecter `ppMDB` est renvoyé dans le paramètre.</span><span class="sxs-lookup"><span data-stu-id="a639e-125">A message store object that the MAPI spooler and client applications can log on to is returned in the  `ppMDB` parameter.</span></span> 
  
### <a name="cmsproviderspoolerlogon-example"></a><span data-ttu-id="a639e-126">CMSProvider:: SpoolerLogon () exemple</span><span class="sxs-lookup"><span data-stu-id="a639e-126">CMSProvider::SpoolerLogon() example</span></span>

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

## <a name="see-also"></a><span data-ttu-id="a639e-127">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="a639e-127">See also</span></span>

- [<span data-ttu-id="a639e-128">À propos de l'exemple de fournisseur de banque d'informations PST encapsulé</span><span class="sxs-lookup"><span data-stu-id="a639e-128">About the Sample Wrapped PST Store Provider</span></span>](about-the-sample-wrapped-pst-store-provider.md) 
- [<span data-ttu-id="a639e-129">Installation de l'exemple de fournisseur de magasins PST encapsulé</span><span class="sxs-lookup"><span data-stu-id="a639e-129">Installing the Sample Wrapped PST Store Provider</span></span>](installing-the-sample-wrapped-pst-store-provider.md) 
- [<span data-ttu-id="a639e-130">Initialisation d'un fournisseur de magasins PST encapsulé</span><span class="sxs-lookup"><span data-stu-id="a639e-130">Initializing a Wrapped PST Store Provider</span></span>](initializing-a-wrapped-pst-store-provider.md)
- [<span data-ttu-id="a639e-131">Utilisation d'un fournisseur de magasins PST encapsulé</span><span class="sxs-lookup"><span data-stu-id="a639e-131">Using a Wrapped PST Store Provider</span></span>](using-a-wrapped-pst-store-provider.md)
- [<span data-ttu-id="a639e-132">Arrêt d'un fournisseur de magasins PST encapsulé</span><span class="sxs-lookup"><span data-stu-id="a639e-132">Shutting Down a Wrapped PST Store Provider</span></span>](shutting-down-a-wrapped-pst-store-provider.md)

