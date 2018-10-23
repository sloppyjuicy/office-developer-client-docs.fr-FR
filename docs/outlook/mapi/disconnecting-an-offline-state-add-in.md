---
title: Déconnexion d’un complément d’état hors connexion
manager: soliver
ms.date: 12/07/2015
ms.audience: Developer
localization_priority: Normal
ms.assetid: 6922cb38-a9e3-e4a9-d4a3-e11b81fc77e2
description: 'Dernière modification : 07 décembre 2015'
ms.openlocfilehash: ce25c6777c8a71da0fe11e0bbf34eefafe2ca50d
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: HT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/23/2018
ms.locfileid: "22564135"
---
# <a name="disconnecting-an-offline-state-add-in"></a>Déconnexion d’un complément d’état hors connexion

**S’applique à** : Outlook 2013 | Outlook 2016 
  
Lorsque le complément d’état hors connexion est déconnecté, vous devez implémenter des fonctions pour l’arrêter et le nettoyer correctement. Pour plus d’informations sur la manière de configurer et d'utiliser le complément d’état hors connexion pour surveiller les modifications de l’état de connexion, reportez-vous aux articles [Configuration d’un complément d’état hors connexion](setting-up-an-offline-state-add-in.md) et [Surveillance des modifications de l’état de connexion à l’aide d’un complément d’état hors connexion](monitoring-connection-state-changes-using-an-offline-state-add-in.md).
  
Dans cette rubrique, ces fonctions de déconnexion, d’arrêt et de nettoyage sont illustrées à l’aide d’exemples de code provenant de l’exemple de complément d’état hors connexion. L’exemple de complément d’état hors connexion est un complément COM qui ajoute un menu **État hors connexion** à Outlook et qui utilise l’API d’état hors connexion. Dans le menu État hors connexion, vous pouvez activer ou désactiver la surveillance de l’état, vérifier l’état actuel ainsi que le modifier. Pour plus d’informations sur le téléchargement et l’installation de l’exemple de complément d’état hors connexion, reportez-vous à l’article [Installation de l’exemple de complément d’état hors connexion](installing-the-sample-offline-state-add-in.md). Pour plus d’informations sur l’API d’état hors connexion, reportez-vous à l’article [À propos de l’API d’état hors connexion](about-the-offline-state-api.md).
  
## <a name="on-disconnection-routine"></a>Routine à la déconnexion (OnDisconnection)

La méthode **IIDTExtensibility2.OnDisconnection** est appelée lorsque le complément d’état hors connexion est déchargé. Vous devez implémenter un code de nettoyage dans cette fonction. Dans l’exemple suivant, la fonction **IDTExtensibility2.OnDisconnection** appelle la fonction `HrTermAddin`. 
  
### <a name="cmyaddinondisconnection-example"></a>Exemple CMyAddin::OnDisconnection()

```cpp
STDMETHODIMP CMyAddin::OnDisconnection(ext_DisconnectMode /*RemoveMode*/, SAFEARRAY * * /*custom*/) 
{ 
    Log(true,"OnDisconnection\n"); 
    HRESULT hRes = S_OK; 
    hRes = HrTermAddin(); 
     return hRes; 
}
```

## <a name="terminate-add-in-function"></a>Fonction d’arrêt du complément (TermAddin)

La fonction `HrTermAddin` appelle les fonctions `inDeInitMonitor`, `HrRemoveMenuItems` et `UnloadLibraries` pour terminer le nettoyage du complément d’état hors connexion. 
  
### <a name="cmyaddinhrtermaddin-example"></a>Exemple CMyAddin::HrTermAddin()

```cpp
HRESULT CMyAddin::HrTermAddin() 
{ 
    HRESULT hRes = S_OK; 
    DeInitMonitor(); 
    hRes =  HrRemoveMenuItems(); 
    UnloadLibraries(); 
    return hRes; 
}
```

## <a name="deinitialize-monitor-routine"></a>Routine de désinitialisation du moniteur (DeInitMonitor)

La fonction `inDeInitMonitor` appelle la fonction [IMAPIOfflineMgr::Unadvise](imapiofflinemgr-unadvise.md) pour annuler les rappels pour l’objet hors connexion. 
  
### <a name="deinitmonitor-example"></a>Exemple DeInitMonitor()

```cpp
void DeInitMonitor() 
{ 
Log(true,_T("Deinitializing Outlook Offline State Monitor\n")); 
HRESULT hRes = S_OK; 
if (g_lpOfflineMgr) 
{ 
hRes = g_lpOfflineMgr->Unadvise(MAPIOFFLINE_UNADVISE_DEFAULT, g_ulAdviseToken); 
g_lpOfflineMgr->Release(); 
g_lpOfflineMgr = NULL; 
g_ulAdviseToken = NULL; 
} 
}
```

## <a name="remove-menu-items-routine"></a>Routine de suppression d’éléments de menu (RemoveMenuItems)

La fonction `HrRemoveMenuItems` appelle `DispEventUnadvise` pour chaque élément de menu sous le menu **État hors connexion**, puis supprime le menu **État hors connexion**. 
  
### <a name="cmyaddinhrremovemenuitems-example"></a>Exemple CMyAddin::HrRemoveMenuItems()

```cpp
HRESULT CMyAddin::HrRemoveMenuItems() 
{     
    Log(true,"HrRemoveMenuItems\n"); 
    HRESULT hRes = S_OK; 
    if (m_fMenuItemsAdded) 
    { 
        try 
        { 
            if (m_spInitButton) 
            { 
                m_InitButtonHandler.DispEventUnadvise(m_spInitButton); 
            } 
            if (m_spDeinitButton) 
            { 
                m_DeinitButtonHandler.DispEventUnadvise(m_spDeinitButton); 
            } 
            if (m_spGetStateButton) 
            { 
                m_GetStateButtonHandler.DispEventUnadvise(m_spGetStateButton); 
            } 
            if (m_spSetStateButton) 
            { 
                m_SetStateButtonHandler.DispEventUnadvise(m_spSetStateButton); 
            } 
 
            m_spMyMenu->Delete(); 
        } 
        catch(_com_error) 
        { 
            hRes = E_FAIL; 
        } 
        if (SUCCEEDED(hRes)) 
        { 
            m_fMenuItemsAdded = false; 
        } 
    } 
    return hRes; 
}
```

## <a name="unload-libraries-routine"></a>Routine de déchargement de bibliothèques (UnloadLibraries)

Lorsque le complément est déchargé à partir d’Outlook, la fonction `UnloadLibraries` décharge les bibliothèques de liens dynamiques (DLL) requises par le complément. 
  
### <a name="unloadlibraries-example"></a>Exemple UnloadLibraries()

```cpp
void UnloadLibraries() 
{ 
    Log(true,_T("UnloadLibraries - freeing modules\n")); 
    pfnHrOpenOfflineObj = NULL; 
    pfnMAPIFreeBuffer = NULL; 
    if (hModMSMAPI) FreeLibrary(hModMSMAPI); 
    hModMSMAPI = NULL; 
    if (hModMAPI) FreeLibrary(hModMAPI); 
    hModMAPI = NULL; 
    if (hModMAPIStub) FreeLibrary(hModMAPIStub); 
    hModMAPIStub = NULL; 
}
```

## <a name="see-also"></a>Voir aussi

- [À propos de l’API d’état hors connexion](about-the-offline-state-api.md)
- [Installation de l’exemple de complément d’état hors connexion](installing-the-sample-offline-state-add-in.md)
- [À propos de l’exemple de complément d’état hors connexion](about-the-sample-offline-state-add-in.md)
- [Configuration d’un complément d’état hors connexion](setting-up-an-offline-state-add-in.md)
- [Surveillance des modifications de l’état de connexion à l’aide d’un complément d’état hors connexion](monitoring-connection-state-changes-using-an-offline-state-add-in.md)

