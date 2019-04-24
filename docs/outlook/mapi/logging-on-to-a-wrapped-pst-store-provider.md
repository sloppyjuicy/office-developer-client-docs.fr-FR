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
# <a name="logging-on-to-a-wrapped-pst-store-provider"></a>Connexion à un fournisseur d’archive PST encapsulée

**S’applique à** : Outlook 2013 | Outlook 2016 
  
Avant de pouvoir ouvrir une session MAPI sur un fournisseur de magasins PST encapsulé, vous devez initialiser et configurer le fournisseur de magasins de fichiers de dossiers personnels (PST). Pour plus d'informations, consultez [la rubrique initialisation d'un fournisseur de magasins de fichiers PST encapsulés](initializing-a-wrapped-pst-store-provider.md).
  
Une fois que vous avez initialisé et configuré un fournisseur de magasins PST encapsulé, vous devez implémenter deux routines d'ouverture de session. La fonction **[IMSProvider:: Logon](imsprovider-logon.md)** ouvre une session MAPI sur le fournisseur de magasins PST encapsulé. La fonction **[IMSProvider:: SpoolerLogon](imsprovider-spoolerlogon.md)** enregistre le spouleur MAPI sur le fournisseur de banque de fichiers PST encapsulé. 
  
Dans cette rubrique, la fonction **IMSProvider:: Logon** et la fonction **IMSProvider:: SpoolerLogon** sont démontrées à l'aide d'exemples de code issus de l'exemple de fournisseur de magasins PST encapsulé. L'exemple implémente un fournisseur PST encapsulé destiné à être utilisé conjointement avec l'API de réPlication. Pour plus d'informations sur le téléchargement et l'installation de l'exemple de fournisseur de magasins PST encapsulé, consultez [la rubrique installation de l'exemple de fournisseur de magasins PST encapsulé](installing-the-sample-wrapped-pst-store-provider.md). Pour plus d'informations sur l'API de réPlication, voir [à propos de l'API](about-the-replication-api.md)de réplication.
  
Une fois que MAPI et le spouleur MAPI sont connectés au fournisseur de magasins PST encapsulé, il est prêt à être utilisé. Pour plus d'informations, consultez [la rubrique utilisation d'un fournisseur de magasins PST encapsulé](using-a-wrapped-pst-store-provider.md).
  
## <a name="mapi-logon-routine"></a>Routine de connexion MAPI

Une fois le fournisseur de banque de fichiers PST encapsulé initialisé, vous devez implémenter la fonction **[IMSProvider:: Logon](imsprovider-logon.md)** pour vous connecter à la Banque de fichiers PST encapsulée via MAPI. Cette fonction valide les informations d'identification de l'utilisateur et obtient les propriétés de configuration pour le fournisseur. Vous devez également implémenter `SetOLFIInOST` la fonction pour définir les informations de fichier hors connexion (**[OLFI](olfi.md)** ). **OLFI** est une file d'attente de structures d'ID à long terme utilisée par le fournisseur de magasins PST encapsulé pour affecter un ID d'entrée pour un nouveau message ou dossier en mode hors connexion. Enfin, la fonction **IMSProvider:: Logon** renvoie un objet de banque de messages auquel le spouleur MAPI et les applications clientes peuvent `ppMDB` se connecter dans le paramètre. 
  
### <a name="cmsproviderlogon-example"></a>CMSProvider:: Logon () exemple

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

## <a name="mapi-spooler-logon-routine"></a>Routine de connexion du spouleur MAPI

De la même manière que pour **IMSProvider:: Logon**, vous devez implémenter la fonction **[IMSProvider:: SpoolerLogon](imsprovider-spoolerlogon.md)** pour enregistrer le spouleur MAPI sur la Banque de fichiers PST encapsulée. Un objet de banque de messages auquel le spouleur MAPI et les applications clientes peuvent se connecter `ppMDB` est renvoyé dans le paramètre. 
  
### <a name="cmsproviderspoolerlogon-example"></a>CMSProvider:: SpoolerLogon () exemple

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

- [À propos de l'exemple de fournisseur de banque d'informations PST encapsulé](about-the-sample-wrapped-pst-store-provider.md) 
- [Installation de l'exemple de fournisseur de magasins PST encapsulé](installing-the-sample-wrapped-pst-store-provider.md) 
- [Initialisation d'un fournisseur de magasins PST encapsulé](initializing-a-wrapped-pst-store-provider.md)
- [Utilisation d'un fournisseur de magasins PST encapsulé](using-a-wrapped-pst-store-provider.md)
- [Arrêt d'un fournisseur de magasins PST encapsulé](shutting-down-a-wrapped-pst-store-provider.md)

