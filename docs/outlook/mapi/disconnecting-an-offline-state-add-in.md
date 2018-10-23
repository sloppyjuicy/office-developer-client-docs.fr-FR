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
# <a name="disconnecting-an-offline-state-add-in"></a><span data-ttu-id="28155-103">Déconnexion d’un complément d’état hors connexion</span><span class="sxs-lookup"><span data-stu-id="28155-103">Disconnecting an Offline State Add-in</span></span>

<span data-ttu-id="28155-104">**S’applique à** : Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="28155-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="28155-105">Lorsque le complément d’état hors connexion est déconnecté, vous devez implémenter des fonctions pour l’arrêter et le nettoyer correctement.</span><span class="sxs-lookup"><span data-stu-id="28155-105">When the offline state add-in is disconnected, you must implement functions to properly terminate and clean up the add-in.</span></span> <span data-ttu-id="28155-106">Pour plus d’informations sur la manière de configurer et d'utiliser le complément d’état hors connexion pour surveiller les modifications de l’état de connexion, reportez-vous aux articles [Configuration d’un complément d’état hors connexion](setting-up-an-offline-state-add-in.md) et [Surveillance des modifications de l’état de connexion à l’aide d’un complément d’état hors connexion](monitoring-connection-state-changes-using-an-offline-state-add-in.md).</span><span class="sxs-lookup"><span data-stu-id="28155-106">For more information on setting up and using the offline state add-in to monitor connection state changes, see [Setting Up an Offline State Add-in](setting-up-an-offline-state-add-in.md) and [Monitoring Connection State Changes Using an Offline State Add-in](monitoring-connection-state-changes-using-an-offline-state-add-in.md).</span></span>
  
<span data-ttu-id="28155-107">Dans cette rubrique, ces fonctions de déconnexion, d’arrêt et de nettoyage sont illustrées à l’aide d’exemples de code provenant de l’exemple de complément d’état hors connexion.</span><span class="sxs-lookup"><span data-stu-id="28155-107">In this topic, these disconnection, terminate, and clean-up functions are demonstrated by using code examples from the Sample Offline State Add-in.</span></span> <span data-ttu-id="28155-108">L’exemple de complément d’état hors connexion est un complément COM qui ajoute un menu **État hors connexion** à Outlook et qui utilise l’API d’état hors connexion.</span><span class="sxs-lookup"><span data-stu-id="28155-108">The Sample Offline State Add-in is a COM add-in that adds an **Offline State** menu to Outlook and uses the Offline State API.</span></span> <span data-ttu-id="28155-109">Dans le menu État hors connexion, vous pouvez activer ou désactiver la surveillance de l’état, vérifier l’état actuel ainsi que le modifier.</span><span class="sxs-lookup"><span data-stu-id="28155-109">Through the Offline State menu, you can enable or disable state monitoring, check the current state, and change the current state.</span></span> <span data-ttu-id="28155-110">Pour plus d’informations sur le téléchargement et l’installation de l’exemple de complément d’état hors connexion, reportez-vous à l’article [Installation de l’exemple de complément d’état hors connexion](installing-the-sample-offline-state-add-in.md).</span><span class="sxs-lookup"><span data-stu-id="28155-110">For more information about downloading and installing the Sample Offline State Add-in, see [Installing the Sample Offline State Add-in](installing-the-sample-offline-state-add-in.md).</span></span> <span data-ttu-id="28155-111">Pour plus d’informations sur l’API d’état hors connexion, reportez-vous à l’article [À propos de l’API d’état hors connexion](about-the-offline-state-api.md).</span><span class="sxs-lookup"><span data-stu-id="28155-111">For more information about the Offline State API, see [About the Offline State API](about-the-offline-state-api.md).</span></span>
  
## <a name="on-disconnection-routine"></a><span data-ttu-id="28155-112">Routine à la déconnexion (OnDisconnection)</span><span class="sxs-lookup"><span data-stu-id="28155-112">On Disconnection Routine</span></span>

<span data-ttu-id="28155-113">La méthode **IIDTExtensibility2.OnDisconnection** est appelée lorsque le complément d’état hors connexion est déchargé.</span><span class="sxs-lookup"><span data-stu-id="28155-113">The **IDTExtensibility2.OnDisconnection** method is called when the Offline State Add-in is unloaded.</span></span> <span data-ttu-id="28155-114">Vous devez implémenter un code de nettoyage dans cette fonction.</span><span class="sxs-lookup"><span data-stu-id="28155-114">You should implement clean up code in this function.</span></span> <span data-ttu-id="28155-115">Dans l’exemple suivant, la fonction **IDTExtensibility2.OnDisconnection** appelle la fonction `HrTermAddin`.</span><span class="sxs-lookup"><span data-stu-id="28155-115">In the following example, the **IDTExtensibility2.OnDisconnection** function calls the  `HrTermAddin` function.</span></span> 
  
### <a name="cmyaddinondisconnection-example"></a><span data-ttu-id="28155-116">Exemple CMyAddin::OnDisconnection()</span><span class="sxs-lookup"><span data-stu-id="28155-116">CMyAddin::OnDisconnection() example</span></span>

```cpp
STDMETHODIMP CMyAddin::OnDisconnection(ext_DisconnectMode /*RemoveMode*/, SAFEARRAY * * /*custom*/) 
{ 
    Log(true,"OnDisconnection\n"); 
    HRESULT hRes = S_OK; 
    hRes = HrTermAddin(); 
     return hRes; 
}
```

## <a name="terminate-add-in-function"></a><span data-ttu-id="28155-117">Fonction d’arrêt du complément (TermAddin)</span><span class="sxs-lookup"><span data-stu-id="28155-117">Terminate Add-in Function</span></span>

<span data-ttu-id="28155-118">La fonction `HrTermAddin` appelle les fonctions `inDeInitMonitor`, `HrRemoveMenuItems` et `UnloadLibraries` pour terminer le nettoyage du complément d’état hors connexion.</span><span class="sxs-lookup"><span data-stu-id="28155-118">The  `HrTermAddin` function calls the  `inDeInitMonitor`,  `HrRemoveMenuItems`, and  `UnloadLibraries` functions to finish cleaning up the Offline State Add-in.</span></span> 
  
### <a name="cmyaddinhrtermaddin-example"></a><span data-ttu-id="28155-119">Exemple CMyAddin::HrTermAddin()</span><span class="sxs-lookup"><span data-stu-id="28155-119">CMyAddin::HrTermAddin() example</span></span>

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

## <a name="deinitialize-monitor-routine"></a><span data-ttu-id="28155-120">Routine de désinitialisation du moniteur (DeInitMonitor)</span><span class="sxs-lookup"><span data-stu-id="28155-120">Deinitialize Monitor Routine</span></span>

<span data-ttu-id="28155-121">La fonction `inDeInitMonitor` appelle la fonction [IMAPIOfflineMgr::Unadvise](imapiofflinemgr-unadvise.md) pour annuler les rappels pour l’objet hors connexion.</span><span class="sxs-lookup"><span data-stu-id="28155-121">The  `inDeInitMonitor` function calls the [IMAPIOfflineMgr::Unadvise](imapiofflinemgr-unadvise.md) function to cancel the callbacks for the offline object.</span></span> 
  
### <a name="deinitmonitor-example"></a><span data-ttu-id="28155-122">Exemple DeInitMonitor()</span><span class="sxs-lookup"><span data-stu-id="28155-122">DeInitMonitor() example</span></span>

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

## <a name="remove-menu-items-routine"></a><span data-ttu-id="28155-123">Routine de suppression d’éléments de menu (RemoveMenuItems)</span><span class="sxs-lookup"><span data-stu-id="28155-123">Remove Menu Items Routine</span></span>

<span data-ttu-id="28155-124">La fonction `HrRemoveMenuItems` appelle `DispEventUnadvise` pour chaque élément de menu sous le menu **État hors connexion**, puis supprime le menu **État hors connexion**.</span><span class="sxs-lookup"><span data-stu-id="28155-124">The  `HrRemoveMenuItems` function calls  `DispEventUnadvise` for each menu item under the **Offline State** menu, and then deletes the **Offline State** menu.</span></span> 
  
### <a name="cmyaddinhrremovemenuitems-example"></a><span data-ttu-id="28155-125">Exemple CMyAddin::HrRemoveMenuItems()</span><span class="sxs-lookup"><span data-stu-id="28155-125">CMyAddin::HrRemoveMenuItems() example</span></span>

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

## <a name="unload-libraries-routine"></a><span data-ttu-id="28155-126">Routine de déchargement de bibliothèques (UnloadLibraries)</span><span class="sxs-lookup"><span data-stu-id="28155-126">Unload Libraries Routine</span></span>

<span data-ttu-id="28155-127">Lorsque le complément est déchargé à partir d’Outlook, la fonction `UnloadLibraries` décharge les bibliothèques de liens dynamiques (DLL) requises par le complément.</span><span class="sxs-lookup"><span data-stu-id="28155-127">When the add-in is unloaded from Outlook, the  `UnloadLibraries` function unloads the dynamic-link libraries (DLLs) that the add-in required.</span></span> 
  
### <a name="unloadlibraries-example"></a><span data-ttu-id="28155-128">Exemple UnloadLibraries()</span><span class="sxs-lookup"><span data-stu-id="28155-128">UnloadLibraries() example</span></span>

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

## <a name="see-also"></a><span data-ttu-id="28155-129">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="28155-129">See also</span></span>

- [<span data-ttu-id="28155-130">À propos de l’API d’état hors connexion</span><span class="sxs-lookup"><span data-stu-id="28155-130">About the Offline State API</span></span>](about-the-offline-state-api.md)
- [<span data-ttu-id="28155-131">Installation de l’exemple de complément d’état hors connexion</span><span class="sxs-lookup"><span data-stu-id="28155-131">Installing the sample Offline State add-in</span></span>](installing-the-sample-offline-state-add-in.md)
- [<span data-ttu-id="28155-132">À propos de l’exemple de complément d’état hors connexion</span><span class="sxs-lookup"><span data-stu-id="28155-132">About the sample Offline State add-in</span></span>](about-the-sample-offline-state-add-in.md)
- [<span data-ttu-id="28155-133">Configuration d’un complément d’état hors connexion</span><span class="sxs-lookup"><span data-stu-id="28155-133">Setting up an Offline State add-in</span></span>](setting-up-an-offline-state-add-in.md)
- [<span data-ttu-id="28155-134">Surveillance des modifications de l’état de connexion à l’aide d’un complément d’état hors connexion</span><span class="sxs-lookup"><span data-stu-id="28155-134">Monitoring connection state changes using an Offline State add-in</span></span>](monitoring-connection-state-changes-using-an-offline-state-add-in.md)

