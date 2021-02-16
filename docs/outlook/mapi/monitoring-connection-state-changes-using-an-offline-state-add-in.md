---
title: Surveillance des changements d’état de connexion à l’aide d’un add-in d’état hors connexion
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
ms.assetid: c482ddce-f2b6-222b-aa30-824b1c6f3b14
description: 'Derniére modification : samedi 23 juillet 2011'
ms.openlocfilehash: d24a6d93943883a5503b57ef223d9be777af13d8
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/28/2019
ms.locfileid: "33431301"
---
# <a name="monitoring-connection-state-changes-using-an-offline-state-add-in"></a><span data-ttu-id="d224e-103">Surveillance des changements d’état de connexion à l’aide d’un add-in d’état hors connexion</span><span class="sxs-lookup"><span data-stu-id="d224e-103">Monitoring connection state changes using an offline state add-in</span></span>

<span data-ttu-id="d224e-104">**S’applique à** : Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="d224e-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="d224e-105">Avant de pouvoir utiliser un add-in d’état hors connexion pour surveiller les changements d’état de connexion, vous devez implémenter des fonctions pour configurer et initialiser le module.</span><span class="sxs-lookup"><span data-stu-id="d224e-105">Before you can use an offline state add-in to monitor connection state changes, you must implement functions to set up and initialize the add-in.</span></span> <span data-ttu-id="d224e-106">Pour plus d’informations, voir [Setting Up an Offline State Add-in](setting-up-an-offline-state-add-in.md).</span><span class="sxs-lookup"><span data-stu-id="d224e-106">For more information, see [Setting Up an Offline State Add-in](setting-up-an-offline-state-add-in.md).</span></span>
  
<span data-ttu-id="d224e-107">Après avoir installé le add-in d’état hors connexion, vous devez utiliser la fonction **[HrOpenOfflineObj](hropenofflineobj.md)** pour obtenir un objet hors connexion.</span><span class="sxs-lookup"><span data-stu-id="d224e-107">After you set up the offline state add-in, you must use the **[HrOpenOfflineObj](hropenofflineobj.md)** function to obtain an offline object.</span></span> <span data-ttu-id="d224e-108">À l’aide de cet objet hors connexion, vous pouvez initialiser votre moniteur d’état, puis obtenir et définir l’état actuel.</span><span class="sxs-lookup"><span data-stu-id="d224e-108">Using this offline object, you can initialize your state monitor, and then get and set the current state.</span></span> 
  
<span data-ttu-id="d224e-109">Dans cette rubrique, ces fonctions d’analyse d’état sont démontrées à l’aide d’exemples de code de l’exemple de add-in d’état hors connexion.</span><span class="sxs-lookup"><span data-stu-id="d224e-109">In this topic, these state monitoring functions are demonstrated by using code examples from the Sample Offline State Add-in.</span></span> <span data-ttu-id="d224e-110">L’exemple de compl?ment d’état hors connexion est un compl?ment COM qui ajoute un **menu** d’état hors connexion dans Outlook et utilise l’API d' ment hors ligne.</span><span class="sxs-lookup"><span data-stu-id="d224e-110">The Sample Offline State Add-in is a COM add-in that adds an **Offline State** menu to Outlook and utilizes the Offline State API.</span></span> <span data-ttu-id="d224e-111">Dans le menu **État** hors connexion, vous pouvez activer ou désactiver la surveillance de l’état, vérifier l’état actuel et modifier l’état actuel.</span><span class="sxs-lookup"><span data-stu-id="d224e-111">Through the **Offline State** menu, you can enable or disable state monitoring, check the current state, and change the current state.</span></span> <span data-ttu-id="d224e-112">Pour plus d’informations sur le téléchargement et l’installation de l’exemple de complément d’état hors connexion, reportez-vous à l’article [Installation de l’exemple de complément d’état hors connexion](installing-the-sample-offline-state-add-in.md).</span><span class="sxs-lookup"><span data-stu-id="d224e-112">For more information about downloading and installing the Sample Offline State Add-in, see [Installing the Sample Offline State Add-in](installing-the-sample-offline-state-add-in.md).</span></span> <span data-ttu-id="d224e-113">Pour plus d’informations sur l’API d’état hors connexion, reportez-vous à l’article [À propos de l’API d’état hors connexion](about-the-offline-state-api.md).</span><span class="sxs-lookup"><span data-stu-id="d224e-113">For more information about the Offline State API, see [About the Offline State API](about-the-offline-state-api.md).</span></span>
  
<span data-ttu-id="d224e-114">Lorsque le complément d’état hors connexion est déconnecté, vous devez implémenter des fonctions pour l’arrêter et le nettoyer correctement.</span><span class="sxs-lookup"><span data-stu-id="d224e-114">When the offline state add-in is disconnected, you must implement functions to properly terminate and clean up the add-in.</span></span> <span data-ttu-id="d224e-115">Pour plus d’informations, voir [Disconnecting an Offline State Add-in](disconnecting-an-offline-state-add-in.md).</span><span class="sxs-lookup"><span data-stu-id="d224e-115">For more information, see [Disconnecting an Offline State Add-in](disconnecting-an-offline-state-add-in.md).</span></span>
  
## <a name="open-offline-object-routine"></a><span data-ttu-id="d224e-116">Routine Ouvrir l’objet hors connexion</span><span class="sxs-lookup"><span data-stu-id="d224e-116">Open Offline Object routine</span></span>

<span data-ttu-id="d224e-117">Pour que le client soit averti en cas de changement d’état de connexion, vous devez appeler la fonction **[HrOpenOfflineObj.](hropenofflineobj.md)**</span><span class="sxs-lookup"><span data-stu-id="d224e-117">For the client to be notified when a connection state change occurs, you must call the **[HrOpenOfflineObj](hropenofflineobj.md)** function.</span></span> <span data-ttu-id="d224e-118">Cette fonction ouvre un objet hors connexion qui prend en charge **[IMAPIOfflineMgr](imapiofflinemgrimapioffline.md)**.</span><span class="sxs-lookup"><span data-stu-id="d224e-118">This function opens an offline object that supports **[IMAPIOfflineMgr](imapiofflinemgrimapioffline.md)**.</span></span> <span data-ttu-id="d224e-119">La **fonction HrOpenOfflineObj** est définie dans le fichier d’en-tête ConnectionState.h.</span><span class="sxs-lookup"><span data-stu-id="d224e-119">The **HrOpenOfflineObj** function is defined in the ConnectionState.h header file.</span></span> 
  
> [!NOTE]
> <span data-ttu-id="d224e-120">La **fonction HrOpenOfflineObj** est déclarée dans le fichier d’en-tête ImportProcs.h comme suit  `extern HROPENOFFLINEOBJ* pfnHrOpenOfflineObj;` :</span><span class="sxs-lookup"><span data-stu-id="d224e-120">The **HrOpenOfflineObj** function is declared in the ImportProcs.h header file as follows:  `extern HROPENOFFLINEOBJ* pfnHrOpenOfflineObj;`.</span></span> 
  
### <a name="hropenofflineobj-example"></a><span data-ttu-id="d224e-121">Exemple HrOpenOfflineObj</span><span class="sxs-lookup"><span data-stu-id="d224e-121">HrOpenOfflineObj example</span></span>

```cpp
typedef HRESULT (STDMETHODCALLTYPE HROPENOFFLINEOBJ)( 
    ULONG ulFlags, 
    LPCWSTR pwszProfileName, 
    const GUID* pGUID, 
    const GUID* pInstance, 
    IMAPIOfflineMgr** ppOffline 
);
```

## <a name="initialize-monitor-routine"></a><span data-ttu-id="d224e-122">Routine Initialize Monitor</span><span class="sxs-lookup"><span data-stu-id="d224e-122">Initialize Monitor routine</span></span>

<span data-ttu-id="d224e-123">La `InitMonitor` fonction appelle la fonction **HrOpenOfflineObj.**</span><span class="sxs-lookup"><span data-stu-id="d224e-123">The  `InitMonitor` function calls the **HrOpenOfflineObj** function.</span></span> <span data-ttu-id="d224e-124">La `InitMonitor` fonction appelle **CMyOfflineNotify** afin qu’Outlook puisse envoyer des notifications de rappel au client et enregistre le rappel via la variable **[MAPIOFFLINE_ADVISEINFO.](mapioffline_adviseinfo.md)** `AdviseInfo`</span><span class="sxs-lookup"><span data-stu-id="d224e-124">The  `InitMonitor` function calls **CMyOfflineNotify** so that Outlook can send callback notifications to the client, and registers the callback through the **[MAPIOFFLINE_ADVISEINFO](mapioffline_adviseinfo.md)** variable  `AdviseInfo`.</span></span>
  
### <a name="initmonitor-example"></a><span data-ttu-id="d224e-125">Exemple InitMonitor()</span><span class="sxs-lookup"><span data-stu-id="d224e-125">InitMonitor() example</span></span>

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

## <a name="get-current-state-routine"></a><span data-ttu-id="d224e-126">Obtenir la routine d’état actuel</span><span class="sxs-lookup"><span data-stu-id="d224e-126">Get Current State routine</span></span>

<span data-ttu-id="d224e-127">La  `GetCurrentState` fonction appelle la fonction **HrOpenOfflineObj,** puis utilise l’objet hors connexion pour obtenir l’état de connexion actuel.</span><span class="sxs-lookup"><span data-stu-id="d224e-127">The  `GetCurrentState` function calls the **HrOpenOfflineObj** function, and then uses the offline object to get the current connection state.</span></span> <span data-ttu-id="d224e-128">L’état actuel est renvoyé dans la variable, qui est utilisée dans la fonction pour afficher  `ulCurState`  `CButtonEventHandler::Click` l’état actuel à l’utilisateur.</span><span class="sxs-lookup"><span data-stu-id="d224e-128">The current state is returned in the  `ulCurState` variable, which is used in the  `CButtonEventHandler::Click` function to display the current state to the user.</span></span> 
  
### <a name="getcurrentstate-example"></a><span data-ttu-id="d224e-129">Exemple GetCurrentState()</span><span class="sxs-lookup"><span data-stu-id="d224e-129">GetCurrentState() example</span></span>

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

## <a name="set-current-state-routine"></a><span data-ttu-id="d224e-130">Définir la routine d’état actuel</span><span class="sxs-lookup"><span data-stu-id="d224e-130">Set Current State routine</span></span>

<span data-ttu-id="d224e-131">La  `SetCurrentState` fonction appelle la fonction **HrOpenOfflineObj,** puis utilise l’objet hors connexion pour définir l’état de connexion actuel.</span><span class="sxs-lookup"><span data-stu-id="d224e-131">The  `SetCurrentState` function calls the **HrOpenOfflineObj** function, and then uses the offline object to set the current connection state.</span></span> <span data-ttu-id="d224e-132">La  `CButtonEventHandler::Click` fonction appelle la fonction et le nouvel état est transmis par le biais de la  `SetCurrentState`  `ulState` variable.</span><span class="sxs-lookup"><span data-stu-id="d224e-132">The  `CButtonEventHandler::Click` function calls the  `SetCurrentState` function and the new state is passed in through the  `ulState` variable.</span></span> 
  
### <a name="setcurrentstate-example"></a><span data-ttu-id="d224e-133">Exemple SetCurrentState()</span><span class="sxs-lookup"><span data-stu-id="d224e-133">SetCurrentState() example</span></span>

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

## <a name="notification-routine"></a><span data-ttu-id="d224e-134">Routine de notification</span><span class="sxs-lookup"><span data-stu-id="d224e-134">Notification routine</span></span>

<span data-ttu-id="d224e-135">La **[fonction IMAPIOfflineNotify::Notify](imapiofflinenotify-notify.md)** est utilisée par Outlook pour envoyer des notifications à un client en cas de modifications de l’état de connexion.</span><span class="sxs-lookup"><span data-stu-id="d224e-135">The **[IMAPIOfflineNotify::Notify](imapiofflinenotify-notify.md)** function is used by Outlook to send notifications to a client when there are changes in the connection state.</span></span> 
  
### <a name="cmyofflinenotifynotify-example"></a><span data-ttu-id="d224e-136">Exemple CMyOfflineNotify::Notify()</span><span class="sxs-lookup"><span data-stu-id="d224e-136">CMyOfflineNotify::Notify() example</span></span>

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

## <a name="see-also"></a><span data-ttu-id="d224e-137">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="d224e-137">See also</span></span>

- [<span data-ttu-id="d224e-138">À propos de l’API d’état hors connexion</span><span class="sxs-lookup"><span data-stu-id="d224e-138">About the Offline State API</span></span>](about-the-offline-state-api.md)
- [<span data-ttu-id="d224e-139">Installation de l’exemple de complément d’état hors connexion</span><span class="sxs-lookup"><span data-stu-id="d224e-139">Installing the Sample Offline State Add-in</span></span>](installing-the-sample-offline-state-add-in.md)
- [<span data-ttu-id="d224e-140">À propos de l’exemple de complément d’état hors connexion</span><span class="sxs-lookup"><span data-stu-id="d224e-140">About the Sample Offline State Add-in</span></span>](about-the-sample-offline-state-add-in.md)
- [<span data-ttu-id="d224e-141">Configuration d’un complément d’état hors connexion</span><span class="sxs-lookup"><span data-stu-id="d224e-141">Setting Up an Offline State Add-in</span></span>](setting-up-an-offline-state-add-in.md)
- [<span data-ttu-id="d224e-142">Déconnexion d’un add-in d’état hors connexion</span><span class="sxs-lookup"><span data-stu-id="d224e-142">Disconnecting an Offline State Add-in</span></span>](disconnecting-an-offline-state-add-in.md)

