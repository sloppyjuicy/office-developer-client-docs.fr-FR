---
title: Surveillance des changements d’état de connexion à l’aide de complément hors connexion
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
ms.assetid: c482ddce-f2b6-222b-aa30-824b1c6f3b14
description: 'Derniére modification : samedi 23 juillet 2011'
ms.openlocfilehash: d8385b2379f2fde8689ae2c7fc5d177af696f22e
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/23/2018
ms.locfileid: "22579878"
---
# <a name="monitoring-connection-state-changes-using-an-offline-state-add-in"></a>Surveillance des changements d’état de connexion à l’aide de complément hors connexion

**S’applique à**: Outlook 2013 | Outlook 2016 
  
Avant de pouvoir utiliser un complément hors connexion pour surveiller les changements d’état de connexion, vous devez implémenter les fonctions pour configurer et initialiser le complément. Pour plus d’informations, voir [définition d’une en mode hors connexion de l’état Add-in](setting-up-an-offline-state-add-in.md).
  
Après avoir configuré le complément hors connexion, vous devez utiliser la fonction **[HrOpenOfflineObj](hropenofflineobj.md)** pour obtenir un objet en mode hors connexion. À l’aide de cet objet en mode hors connexion, vous pouvez initialiser votre moniteur d’état et puis obtenir et définir l’état actuel. 
  
Dans cette rubrique, les fonctions de surveillance d’état sont illustrées à l’aide des exemples de code à partir de la macro complémentaire exemple hors connexion état. Le complément exemple hors connexion état est un complément COM qui ajoute un menu **État hors connexion** dans Outlook et utilise l’API de l’état en mode hors connexion. Via le menu **État hors connexion** , vous pouvez activer ou désactiver l’analyse de l’état, vérifiez l’état en cours et modifier l’état actuel. Pour plus d’informations sur le téléchargement et l’installation du complément exemple hors connexion état, consultez [installation du complément exemple hors connexion état](installing-the-sample-offline-state-add-in.md). Pour plus d’informations sur l’API de l’état en mode hors connexion, voir [à propos en mode hors connexion état API](about-the-offline-state-api.md).
  
Lorsque le complément hors connexion est déconnecté, vous devez implémenter les fonctions pour terminer correctement et de nettoyer le complément. Pour plus d’informations, voir [déconnexion d’une macro complémentaire état hors connexion](disconnecting-an-offline-state-add-in.md).
  
## <a name="open-offline-object-routine"></a>Routine Open objet en mode hors connexion

Pour le client être averti lorsque cet événement se produit un changement d’état de connexion, vous devez appeler la fonction **[HrOpenOfflineObj](hropenofflineobj.md)** . Cette fonction ouvre un objet en mode hors connexion qui prend en charge **[IMAPIOfflineMgr](imapiofflinemgrimapioffline.md)**. La fonction **HrOpenOfflineObj** est définie dans le fichier d’en-tête ConnectionState.h. 
  
> [!NOTE]
> La fonction **HrOpenOfflineObj** est déclarée comme suit dans le fichier d’en-tête ImportProcs.h : `extern HROPENOFFLINEOBJ* pfnHrOpenOfflineObj;`. 
  
### <a name="hropenofflineobj-example"></a>Exemple HrOpenOfflineObj

```cpp
typedef HRESULT (STDMETHODCALLTYPE HROPENOFFLINEOBJ)( 
    ULONG ulFlags, 
    LPCWSTR pwszProfileName, 
    const GUID* pGUID, 
    const GUID* pInstance, 
    IMAPIOfflineMgr** ppOffline 
);
```

## <a name="initialize-monitor-routine"></a>Initialiser la routine moniteur

Le `InitMonitor` fonction appelle la fonction **HrOpenOfflineObj** . Le `InitMonitor` fonction appelle **CMyOfflineNotify** afin qu’Outlook peut envoyer des notifications de rappel pour le client et enregistre le rappel par le biais de la variable **[MAPIOFFLINE_ADVISEINFO](mapioffline_adviseinfo.md)** `AdviseInfo`.
  
### <a name="initmonitor-example"></a>Exemple InitMonitor()

```cpp
void InitMonitor(LPCWSTR szProfile) 
{ 
    if (!szProfile) return; 
    Log(true,_T("Initializing Outlook Offline State Monitor\n")); 
    HRESULT hRes = S_OK; 
 
    if (g_lpOfflineMgr) 
    { 
        Log(true,_T("Already initialized\n")); 
        return; 
    } 
     
    if (pfnHrOpenOfflineObj) 
    { 
        if (g_lpOfflineMgr) DeInitMonitor(); 
        Log(true,_T("Calling HrOpenOfflineObj for \"%ws\"\n"),szProfile); 
        hRes = pfnHrOpenOfflineObj( 
            NULL, 
            szProfile, 
            &GUID_GlobalState, 
            NULL, 
            &g_lpOfflineMgr); 
        if (FAILED(hRes))  
        { 
            Log(true,_T("HrOpenOfflineObj failed: 0x%08X\n"),hRes); 
        } 
        if (g_lpOfflineMgr) 
        { 
            IMAPIOffline* lpOffline = NULL; 
            hRes = g_lpOfflineMgr->QueryInterface(IID_IMAPIOffline,(LPVOID*)&lpOffline); 
             
            if (lpOffline) 
            { 
                ULONG ulCap = NULL; 
                hRes = lpOffline->GetCapabilities(&ulCap); 
                 
                if (ulCap & MAPIOFFLINE_CAPABILITY_OFFLINE) Log(true,_T("MAPIOFFLINE_CAPABILITY_OFFLINE supported\n")); 
                if (ulCap & MAPIOFFLINE_CAPABILITY_ONLINE) Log(true,_T("MAPIOFFLINE_CAPABILITY_ONLINE supported\n")); 
                 
                if (ulCap & (MAPIOFFLINE_CAPABILITY_OFFLINE | MAPIOFFLINE_CAPABILITY_ONLINE)) 
                { 
                    CMyOfflineNotify* lpImplNotify = new CMyOfflineNotify(); 
                     
                    if (lpImplNotify) 
                    { 
                        MAPIOFFLINE_ADVISEINFO AdviseInfo = {0}; 
                        AdviseInfo.ulSize = sizeof(MAPIOFFLINE_ADVISEINFO); 
                        AdviseInfo.ulClientToken = 0;// something you want to get handed back when you get the notification 
                        AdviseInfo.CallbackType = MAPIOFFLINE_CALLBACK_TYPE_NOTIFY; 
                        AdviseInfo.pCallback = lpImplNotify; 
                        AdviseInfo.ulAdviseTypes = MAPIOFFLINE_ADVISE_TYPE_STATECHANGE; 
                        AdviseInfo.ulStateMask = MAPIOFFLINE_STATE_ALL; 
                         
                        hRes = g_lpOfflineMgr->Advise(MAPIOFFLINE_ADVISE_DEFAULT, &AdviseInfo, &g_ulAdviseToken); 
                        Log(true,"ulAdviseToken = 0x%08X\n",g_ulAdviseToken); 
                    } 
                } 
                lpOffline->Release(); 
            }                 
        } 
    } 
}
```

## <a name="get-current-state-routine"></a>Routine d’obtenir l’état actuel

Le `GetCurrentState` fonction appelle la fonction **HrOpenOfflineObj** , puis utilise l’objet en mode hors connexion pour obtenir l’état actuel de la connexion. L’état actuel est retournée dans le `ulCurState` variable, qui est utilisé dans les `CButtonEventHandler::Click` fonction pour afficher l’état en cours à l’utilisateur. 
  
### <a name="getcurrentstate-example"></a>Exemple GetCurrentState()

```cpp
ULONG (LPCWSTR szProfile) 
{ 
    if (!szProfile) return 0; 
    Log(true,_T("Getting Current Offline State\n")); 
    HRESULT hRes = S_OK; 
    ULONG ulCurState = NULL; 
 
    if (pfnHrOpenOfflineObj) 
    { 
        if (g_lpOfflineMgr) DeInitMonitor(); 
        Log(true,_T("Calling HrOpenOfflineObj for \"%ws\"\n"),szProfile); 
        hRes = pfnHrOpenOfflineObj( 
            NULL, 
            szProfile, 
            &GUID_GlobalState, 
            NULL, 
            &g_lpOfflineMgr); 
        if (FAILED(hRes))  
        { 
            Log(true,_T("HrOpenOfflineObj failed: 0x%08X\n"),hRes); 
        } 
        if (g_lpOfflineMgr) 
        { 
            IMAPIOffline* lpOffline = NULL; 
            hRes = g_lpOfflineMgr->QueryInterface(IID_IMAPIOffline,(LPVOID*)&lpOffline); 
             
            if (lpOffline) 
            { 
                hRes = lpOffline->GetCurrentState(&ulCurState); 
                Log(true,_T("GetCurrentState returned 0x%08X\n"),hRes); 
 
                switch(ulCurState) 
                { 
                case MAPIOFFLINE_STATE_ONLINE: 
                    Log(true,_T("Current state is MAPIOFFLINE_STATE_ONLINE\n")); 
                    break; 
                case MAPIOFFLINE_STATE_OFFLINE: 
                    Log(true,_T("Current state is MAPIOFFLINE_STATE_OFFLINE\n")); 
                    break; 
                default: 
                    Log(true,_T("Current state is 0x%0X\n"),ulCurState); 
                } 
                lpOffline->Release(); 
            } 
        } 
    } 
    return ulCurState; 
}
```

## <a name="set-current-state-routine"></a>Routine de définir l’état en cours

Le `SetCurrentState` fonction appelle la fonction **HrOpenOfflineObj** et utilise ensuite l’objet en mode hors connexion pour définir l’état actuel de la connexion. Les `CButtonEventHandler::Click` les appels de fonction la `SetCurrentState` fonction et le nouvel état est passé par le biais du `ulState` variable. 
  
### <a name="setcurrentstate-example"></a>Exemple SetCurrentState()

```cpp
HRESULT SetCurrentState(LPCWSTR szProfile, ULONG ulFlags, ULONG ulState) 
{ 
    if (!szProfile) return 0; 
    Log(true,_T("Setting Current Offline State\n")); 
    HRESULT hRes = S_OK; 
 
    if (pfnHrOpenOfflineObj) 
    { 
        if (g_lpOfflineMgr) DeInitMonitor(); 
        Log(true,_T("Calling HrOpenOfflineObj for \"%ws\"\n"),szProfile); 
        hRes = pfnHrOpenOfflineObj( 
            NULL, 
            szProfile, 
            &GUID_GlobalState, 
            NULL, 
            &g_lpOfflineMgr); 
        if (FAILED(hRes))  
        { 
            Log(true,_T("HrOpenOfflineObj failed: 0x%08X\n"),hRes); 
        } 
        if (g_lpOfflineMgr) 
        { 
            IMAPIOffline* lpOffline = NULL; 
            hRes = g_lpOfflineMgr->QueryInterface(IID_IMAPIOffline,(LPVOID*)&lpOffline); 
             
            if (lpOffline) 
            { 
                switch(ulFlags) 
                { 
                case MAPIOFFLINE_FLAG_BLOCK: 
                    Log(true,_T("Flag used: MAPIOFFLINE_FLAG_BLOCK\n")); 
                    break; 
                case MAPIOFFLINE_FLAG_DEFAULT: 
                    Log(true,_T("Flag used: MAPIOFFLINE_FLAG_DEFAULT\n")); 
                    break; 
                default: 
                    Log(true,_T("Flag used: 0x%0X\n"),ulFlags); 
                } 
                switch(ulState) 
                { 
                case MAPIOFFLINE_STATE_ONLINE: 
                    Log(true,_T("New state will be MAPIOFFLINE_STATE_ONLINE\n")); 
                    break; 
                case MAPIOFFLINE_STATE_OFFLINE: 
                    Log(true,_T("New state will be MAPIOFFLINE_STATE_OFFLINE\n")); 
                    break; 
                default: 
                    Log(true,_T("New state will be 0x%0X\n"),ulState); 
                } 
                hRes = lpOffline->SetCurrentState(ulFlags, MAPIOFFLINE_STATE_OFFLINE_MASK,ulState,NULL); 
                Log(true,_T("SetCurrentState returned 0x%08X\n"),hRes); 
                 
                lpOffline->Release(); 
            } 
        } 
    } 
    return hRes; 
}
```

## <a name="notification-routine"></a>Routine de notification

La fonction **[IMAPIOfflineNotify::Notify](imapiofflinenotify-notify.md)** est utilisée par Outlook pour envoyer des notifications à un client lorsqu’il existe des modifications dans l’état de connexion. 
  
### <a name="cmyofflinenotifynotify-example"></a>Exemple CMyOfflineNotify::Notify()

```cpp
void CMyOfflineNotify::Notify(const MAPIOFFLINE_NOTIFY *pNotifyInfo) 
{ 
    Log(true,_T("CMyOfflineNotify::Notify\n")); 
    if    (pNotifyInfo == NULL) 
    {     
        Log(true,_T("pNotifyInfo is NULL\n")); 
    } 
    else 
    { 
        Log(true,_T("pNotifyInfo->ulSize == 0x%0X\n"),pNotifyInfo->ulSize); 
        switch(pNotifyInfo->NotifyType) 
        { 
            case    MAPIOFFLINE_NOTIFY_TYPE_STATECHANGE: 
                Log(true,_T("pNotifyInfo->NotifyType == MAPIOFFLINE_NOTIFY_TYPE_STATECHANGE\n")); 
                break; 
            case    MAPIOFFLINE_NOTIFY_TYPE_STATECHANGE_START: 
                Log(true,_T("pNotifyInfo->NotifyType == MAPIOFFLINE_NOTIFY_TYPE_STATECHANGE_START\n")); 
                break; 
            case    MAPIOFFLINE_NOTIFY_TYPE_STATECHANGE_DONE: 
                Log(true,_T("pNotifyInfo->NotifyType == MAPIOFFLINE_NOTIFY_TYPE_STATECHANGE_DONE\n")); 
                break; 
            default: 
                Log(true,_T("pNotifyInfo->NotifyType == 0x%08X\n"),pNotifyInfo->NotifyType); 
        } 
        Log(true,_T("pNotifyInfo->ulClientToken == 0x%0X\n"),pNotifyInfo->ulClientToken); 
        switch(pNotifyInfo->Info.StateChange.ulMask) 
        { 
            case    MAPIOFFLINE_STATE_OFFLINE_MASK: 
                Log(true,_T("pNotifyInfo->Info.StateChange.ulMask == MAPIOFFLINE_STATE_OFFLINE_MASK\n")); 
                break; 
            default: 
                Log(true,_T("pNotifyInfo->Info.StateChange.ulMask == 0x%0X\n"),pNotifyInfo->Info.StateChange.ulMask); 
        } 
        switch(pNotifyInfo->Info.StateChange.ulStateOld) 
        { 
            case    MAPIOFFLINE_STATE_ONLINE: 
                Log(true,_T("pNotifyInfo->Info.StateChange.ulStateOld == MAPIOFFLINE_STATE_ONLINE\n")); 
                break; 
            case    MAPIOFFLINE_STATE_OFFLINE: 
                Log(true,_T("pNotifyInfo->Info.StateChange.ulStateOld == MAPIOFFLINE_STATE_OFFLINE\n")); 
                break; 
            default: 
                Log(true,_T("pNotifyInfo->Info.StateChange.ulStateOld == 0x%0X\n"),pNotifyInfo->Info.StateChange.ulStateOld); 
        } 
        switch(pNotifyInfo->Info.StateChange.ulStateNew) 
        { 
            case    MAPIOFFLINE_STATE_ONLINE: 
                Log(true,_T("pNotifyInfo->Info.StateChange.ulStateNew == MAPIOFFLINE_STATE_ONLINE\n")); 
                break; 
            case    MAPIOFFLINE_STATE_OFFLINE: 
                Log(true,_T("pNotifyInfo->Info.StateChange.ulStateNew == MAPIOFFLINE_STATE_OFFLINE\n")); 
                break; 
            default: 
                Log(true,_T("pNotifyInfo->Info.StateChange.ulStateNew == 0x%0X\n"),pNotifyInfo->Info.StateChange.ulStateNew); 
        } 
    } 
    return; 
}
```

## <a name="see-also"></a>Voir aussi

- [À propos de l’API d’état hors connexion](about-the-offline-state-api.md)
- [Installation de l’exemple de complément d’état hors connexion](installing-the-sample-offline-state-add-in.md)
- [À propos de l’exemple de complément d’état hors connexion](about-the-sample-offline-state-add-in.md)
- [Configuration d’un complément d’état hors connexion](setting-up-an-offline-state-add-in.md)
- [Déconnexion d’un complément d’état hors connexion](disconnecting-an-offline-state-add-in.md)

