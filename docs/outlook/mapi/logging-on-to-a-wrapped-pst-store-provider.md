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
# <a name="logging-on-to-a-wrapped-pst-store-provider"></a>Connexion à un fournisseur d’archive PST encapsulée

**S’applique à** : Outlook 2013 | Outlook 2016 
  
Avant de pouvoir vous connecter à MAPI auprès d’un fournisseur de magasins PST wrapped, vous devez initialiser et configurer le fournisseur de magasin de dossiers personnels wrapped (PST). Pour plus d’informations, [voir Initializing a Wrapped PST Store Provider](initializing-a-wrapped-pst-store-provider.md).
  
Après avoir initialisé et configuré un fournisseur de magasin PST wrapped, vous devez implémenter deux routines d’ouverture de contrat. La **[fonction IMSProvider::Logon](imsprovider-logon.md)** se connecte sur MAPI au fournisseur de magasin PST wrapped. La **[fonction IMSProvider::SpoolerLogon](imsprovider-spoolerlogon.md)** enregistre lepooler MAPI sur le fournisseur de magasin PST wrapped. 
  
Dans cette rubrique, les fonctions **IMSProvider::Logon** et **IMSProvider::SpoolerLogon** sont démontrées à l’aide d’exemples de code du fournisseur de magasin PST Wrapped sample. L’exemple implémente un fournisseur PST wrapped qui est destiné à être utilisé conjointement avec l’API de réplication. Pour plus d’informations sur le téléchargement et l’installation de l’exemple de fournisseur de magasin PST [Wrapped, voir Installing the Sample Wrapped PST Store Provider](installing-the-sample-wrapped-pst-store-provider.md). Pour plus d’informations sur l’API de réplication, voir [à propos de l’API de réplication.](about-the-replication-api.md)
  
Une fois que MAPI et lepooler MAPI sont connectés au fournisseur de magasin PST wrapped, il est prêt à être utilisé. Pour plus d’informations, voir [Using a Wrapped PST Store Provider](using-a-wrapped-pst-store-provider.md).
  
## <a name="mapi-logon-routine"></a>Routine d’logo MAPI

Une fois le fournisseur de magasin PST wrapped initialisé, vous devez implémenter la fonction **[IMSProvider::Logon](imsprovider-logon.md)** pour vous connecter à MAPI dans le magasin PST wrapped. Cette fonction valide les informations d’identification de l’utilisateur et obtient les propriétés de configuration du fournisseur. Vous devez également implémenter la fonction pour définir les informations de fichier hors  `SetOLFIInOST` connexion (**[OLFI](olfi.md)** ). **OLFI** est une file d’attente de structures d’ID à long terme qui est utilisée par le fournisseur de magasin PST wrapped pour affecter un ID d’entrée pour un nouveau message ou dossier en mode hors connexion. Enfin, la **fonction IMSProvider::Logon** renvoie un objet de magasin de messages sur qui lepooler MAPI et les applications clientes peuvent se connecter dans le  `ppMDB` paramètre. 
  
### <a name="cmsproviderlogon-example"></a>Exemple CMSProvider::Logon()

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

## <a name="mapi-spooler-logon-routine"></a>Routine d’logo mapi Spooler

Similaire à **IMSProvider::Logon**, vous devez implémenter la fonction **[IMSProvider::SpoolerLogon](imsprovider-spoolerlogon.md)** pour connecter lepooler MAPI au magasin PST wrapped. Un objet de magasin de messages à qui lepooler MAPI et les applications clientes peuvent se connecter est renvoyé dans le  `ppMDB` paramètre. 
  
### <a name="cmsproviderspoolerlogon-example"></a>Exemple CMSProvider::SpoolerLogon()

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

## <a name="see-also"></a>Voir aussi

- [À propos de l’exemple de fournisseur de magasin PST wrapped](about-the-sample-wrapped-pst-store-provider.md) 
- [Installation de l’exemple de fournisseur de magasin PST Wrapped](installing-the-sample-wrapped-pst-store-provider.md) 
- [Initialisation d’un fournisseur de magasin PST wrapped](initializing-a-wrapped-pst-store-provider.md)
- [Utilisation d’un fournisseur de magasin PST wrapped](using-a-wrapped-pst-store-provider.md)
- [Arrêt d’un fournisseur de magasin PST wrapped](shutting-down-a-wrapped-pst-store-provider.md)

