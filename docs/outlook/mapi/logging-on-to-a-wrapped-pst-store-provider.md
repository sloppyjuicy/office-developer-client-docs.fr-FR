---
title: Connexion à un fournisseur d’archive PST encapsulée
description: La fonction d’ouverture de session IMSProvider et la fonction IMSProvider SpoolerLogon sont illustrées à l’aide d’exemples de code provenant de l’exemple de fournisseur de magasin PST encapsulé.
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.localizationpriority: medium
ms.assetid: 364bc5fd-2199-0bb2-142b-9b3b686b2268
ms.openlocfilehash: 9a5fc33759e8e80e1b4832a4d2c186a6cfda9b29
ms.sourcegitcommit: e2b79cc4469013a4b3705620a93aa70b88e6c996
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/02/2022
ms.locfileid: "65828009"
---
# <a name="logging-on-to-a-wrapped-pst-store-provider"></a>Connexion à un fournisseur d’archive PST encapsulée

**S’applique à** : Outlook 2013 | Outlook 2016 
  
Avant de pouvoir vous connecter à MAPI à un fournisseur de magasin PST encapsulé, vous devez initialiser et configurer le fournisseur de magasinS PST (Personal Folders File). Pour plus d’informations, consultez [Initialisation d’un fournisseur de magasin PST encapsulé](initializing-a-wrapped-pst-store-provider.md).
  
Une fois que vous avez initialisé et configuré un fournisseur de magasin PST encapsulé, vous devez implémenter deux routines d’ouverture de session. La fonction **[IMSProvider::Logon](imsprovider-logon.md)** se connecte sur MAPI au fournisseur de magasin PST encapsulé. La fonction **[IMSProvider::SpoolerLogon](imsprovider-spoolerlogon.md)** se connecte sur le spouleur MAPI au fournisseur de magasin PST encapsulé. 
  
Dans cette rubrique, la fonction **IMSProvider::Logon** et la fonction **IMSProvider::SpoolerLogon** sont illustrées à l’aide d’exemples de code de l’exemple de fournisseur de magasin PST encapsulé. L’exemple implémente un fournisseur PST encapsulé qui est destiné à être utilisé conjointement avec l’API de réplication. Pour plus d’informations sur le téléchargement et l’installation de l’exemple de fournisseur de magasin PST encapsulé, consultez [l’installation de l’exemple de fournisseur de magasin PST encapsulé](installing-the-sample-wrapped-pst-store-provider.md). Pour plus d’informations sur l’API de réplication, consultez [À propos de l’API de réplication](about-the-replication-api.md).
  
Une fois mapi et le spouleur MAPI connectés au fournisseur de magasin PST encapsulé, il est prêt à être utilisé. Pour plus d’informations, consultez [Utilisation d’un fournisseur de magasin PST encapsulé](using-a-wrapped-pst-store-provider.md).
  
## <a name="mapi-logon-routine"></a>Routine d’ouverture de session MAPI

Une fois que le fournisseur du magasin PST encapsulé est initialisé, vous devez implémenter la fonction **[IMSProvider::Logon](imsprovider-logon.md)** pour vous connecter à MAPI dans le magasin PST encapsulé. Cette fonction valide les informations d’identification de l’utilisateur et obtient les propriétés de configuration du fournisseur. Vous devez également implémenter la  `SetOLFIInOST` fonction pour définir les informations de fichier hors connexion (**[OLFI](olfi.md)** ). **OLFI** est une file d’attente de structures d’ID à long terme utilisée par le fournisseur du magasin PST encapsulé pour affecter un ID d’entrée pour un nouveau message ou dossier en mode hors connexion. Enfin, la fonction **IMSProvider::Logon** renvoie un objet de magasin de messages auquel le spouleur MAPI et les applications clientes peuvent se connecter dans le  `ppMDB` paramètre. 
  
### <a name="cmsproviderlogon-example"></a>EXEMPLE CMSProvider::Logon()

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

## <a name="mapi-spooler-logon-routine"></a>Routine d’ouverture de session du spouleur MAPI

À l’instar **d’IMSProvider::Logon**, vous devez implémenter la fonction **[IMSProvider::SpoolerLogon](imsprovider-spoolerlogon.md)** pour journaliser le spouleur MAPI dans le magasin PST encapsulé. Un objet de magasin de messages auquel le spouleur MAPI et les applications clientes peuvent se connecter sont retournés dans le  `ppMDB` paramètre. 
  
### <a name="cmsproviderspoolerlogon-example"></a>EXEMPLE CMSProvider::SpoolerLogon()

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

- [À propos de l’exemple de fournisseur de magasin PST encapsulé](about-the-sample-wrapped-pst-store-provider.md) 
- [Installation de l’exemple de fournisseur de magasin PST encapsulé](installing-the-sample-wrapped-pst-store-provider.md) 
- [Initialisation d’un fournisseur de magasin PST encapsulé](initializing-a-wrapped-pst-store-provider.md)
- [Utilisation d’un fournisseur de magasin PST encapsulé](using-a-wrapped-pst-store-provider.md)
- [Arrêt d’un fournisseur de magasin PST encapsulé](shutting-down-a-wrapped-pst-store-provider.md)

