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
# <a name="logging-on-to-a-wrapped-pst-store-provider"></a>Se connecter à un fournisseur de magasin PST encapsulé

**S’applique à**: Outlook 2013 | Outlook 2016 
  
Avant de session MAPI à un fournisseur de magasin PST encapsulé, vous devez initialiser et configurer le fournisseur de banque encapsulé dossiers personnels (PST) de fichier. Pour plus d’informations, voir [l’initialisation d’un fournisseur de magasins encapsulé PST](initializing-a-wrapped-pst-store-provider.md).
  
Après avoir initialisé et configuré un fournisseur de magasins PST encapsulé, vous devez implémenter deux routines d’ouverture de session. La fonction **[IMSProvider::Logon](imsprovider-logon.md)** ouvre une session MAPI pour le fournisseur de banque PST justifié. La fonction **[IMSProvider::SpoolerLogon](imsprovider-spoolerlogon.md)** se connecte le spouleur MAPI pour le fournisseur de banque PST justifié. 
  
Dans cette rubrique, la fonction **IMSProvider::Logon** et la fonction **IMSProvider::SpoolerLogon** sont illustrées à l’aide des exemples de code à partir du fournisseur de magasin exemple encapsulé PST. L’exemple implémente un fournisseur PST renvoyé à la ligne qui est destiné à être utilisé conjointement avec l’API de réplication. Pour plus d’informations sur le téléchargement et l’installation du fournisseur de magasin exemple encapsulé PST, voir [installer le fournisseur de banque exemple encapsulé PST](installing-the-sample-wrapped-pst-store-provider.md). Pour plus d’informations sur l’API de réplication, consultez la rubrique [Sur l’API de réplication](about-the-replication-api.md).
  
Une fois que MAPI et le spouleur MAPI sont enregistrés sur le fichier PST renvoyé à la ligne fournisseur de magasins, il est prêt à être utilisé. Pour plus d’informations, voir [utilisation d’un fournisseur de magasin PST encapsulé](using-a-wrapped-pst-store-provider.md).
  
## <a name="mapi-logon-routine"></a>Routine d’ouverture de session MAPI

Une fois que le fournisseur de banque PST encapsulé est initialisé, vous devez implémenter la fonction **[IMSProvider::Logon](imsprovider-logon.md)** pour ouvrir une session MAPI sur le magasin de fichiers PST justifié. Cette fonction valide les informations d’identification utilisateur et obtient les propriétés de configuration pour le fournisseur. Vous devez également implémenter la `SetOLFIInOST` fonction pour définir les informations de fichier en mode hors connexion (**[OLFI](olfi.md)** ). **OLFI** est une file d’attente des structures d’ID à long terme qui est utilisée par le fournisseur de banque PST encapsulé pour attribuer un ID d’entrée pour un nouveau message ou un dossier en mode hors connexion. Enfin, la fonction **IMSProvider::Logon** renvoie un objet de banque de messages qui les applications MAPI spouleur et le client peuvent se connecter à la `ppMDB` paramètre. 
  
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

## <a name="mapi-spooler-logon-routine"></a>Routine d’ouverture de session MAPI spouleur

Similaire aux **IMSProvider::Logon**, vous devez implémenter la fonction **[IMSProvider::SpoolerLogon](imsprovider-spoolerlogon.md)** pour enregistrer le spouleur MAPI sur la banque de dossiers personnels encapsulé. Un objet de banque de message peuvent ouvrir une session sur les applications de client et spouleur MAPI est retourné dans le `ppMDB` paramètre. 
  
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

- [À propos de l’exemple de fournisseur d’archive PST encapsulée](about-the-sample-wrapped-pst-store-provider.md) 
- [Installation de l’exemple de fournisseur d’archive PST encapsulée](installing-the-sample-wrapped-pst-store-provider.md) 
- [Initialisation d’un fournisseur d’archive PST encapsulée](initializing-a-wrapped-pst-store-provider.md)
- [Utilisation d’un fournisseur d’archive PST encapsulée](using-a-wrapped-pst-store-provider.md)
- [Arrêt d’un fournisseur d’archive PST encapsulée](shutting-down-a-wrapped-pst-store-provider.md)

