---
title: Déconnexion d’un complément en mode hors connexion d’état
manager: soliver
ms.date: 12/07/2015
ms.audience: Developer
localization_priority: Normal
ms.assetid: 6922cb38-a9e3-e4a9-d4a3-e11b81fc77e2
description: 'Derni�re modification�: lundi 7 d�cembre 2015'
ms.openlocfilehash: 82f529f58a62f412ed8b25d1ceaf508463491612
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/15/2018
ms.locfileid: "19783165"
---
# <a name="disconnecting-an-offline-state-add-in"></a>Déconnexion d’un complément en mode hors connexion d’état

**S’applique à**: Outlook 
  
Lorsque le complément hors connexion est déconnecté, vous devez implémenter les fonctions pour terminer correctement et de nettoyer le complément. Pour plus d’informations sur la configuration et l’utilisation hors connexion d’état de complément pour surveiller les changements d’état de connexion, voir le [complément de paramètre d’un état en mode hors connexion](setting-up-an-offline-state-add-in.md) et [Surveillance connexion état modifications en utilisant un complément état hors connexion](monitoring-connection-state-changes-using-an-offline-state-add-in.md).
  
Dans cette rubrique, ces de déconnexion, terminer et le nettoyage des fonctions sont illustrées à l’aide des exemples de code à partir de la macro complémentaire exemple hors connexion état. Le complément exemple hors connexion état est un complément COM qui ajoute un menu **État hors connexion** dans Outlook et utilise l’API de l’état en mode hors connexion. Via le menu état hors connexion, vous pouvez activer ou désactiver l’analyse de l’état, vérifiez l’état en cours et modifier l’état actuel. Pour plus d’informations sur le téléchargement et l’installation du complément exemple hors connexion état, consultez [installation du complément exemple hors connexion état](installing-the-sample-offline-state-add-in.md). Pour plus d’informations sur l’API de l’état en mode hors connexion, voir [à propos en mode hors connexion état API](about-the-offline-state-api.md).
  
## <a name="on-disconnection-routine"></a>Dans la Routine de déconnexion

La méthode **IDTExtensibility2.OnDisconnection** est appelée lorsque l’état hors connexion est déchargé. Vous devez implémenter nettoyer le code de cette fonction. Dans l’exemple suivant, la fonction **IDTExtensibility2.OnDisconnection** appelle le `HrTermAddin` fonction. 
  
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

## <a name="terminate-add-in-function"></a>Mettre fin à la fonction complémentaire

Les `HrTermAddin` les appels de fonction la `inDeInitMonitor`, `HrRemoveMenuItems`, et `UnloadLibraries` fonctions pour terminer le nettoyage de la macro complémentaire état hors connexion. 
  
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

## <a name="deinitialize-monitor-routine"></a>Désinitialiser Routine moniteur

Le `inDeInitMonitor` fonction appelle la fonction [IMAPIOfflineMgr::Unadvise](imapiofflinemgr-unadvise.md) pour annuler des rappels pour l’objet en mode hors connexion. 
  
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

## <a name="remove-menu-items-routine"></a>Supprimer la Routine d’éléments de Menu

Les `HrRemoveMenuItems` les appels de fonction `DispEventUnadvise` pour chaque élément de menu dans le menu **État hors connexion** , puis supprime le menu **d’État hors connexion** . 
  
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

## <a name="unload-libraries-routine"></a>Déchargement d’une Routine de bibliothèques

Lorsque le complément est déchargé à partir d’Outlook, le `UnloadLibraries` fonction décharge les bibliothèques de liens dynamiques (DLL) nécessitant la macro complémentaire. 
  
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

- [À propos de l’API d’état en mode hors connexion](about-the-offline-state-api.md)
- [L’installation de l’exemple en mode hors connexion d’état complément](installing-the-sample-offline-state-add-in.md)
- [À propos de l’exemple en mode hors connexion-dans l’état](about-the-sample-offline-state-add-in.md)
- [Configuration d’un complément en mode hors connexion d’état](setting-up-an-offline-state-add-in.md)
- [Analyse l’état de connexion change utilisant un complément en mode hors connexion d’état](monitoring-connection-state-changes-using-an-offline-state-add-in.md)

