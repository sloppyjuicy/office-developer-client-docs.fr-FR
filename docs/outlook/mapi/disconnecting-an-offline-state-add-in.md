---
title: Déconnexion d’un complément d’état hors connexion
manager: soliver
ms.date: 12/07/2015
ms.audience: Developer
localization_priority: Normal
ms.assetid: 6922cb38-a9e3-e4a9-d4a3-e11b81fc77e2
description: 'Derni�re modification�: lundi 7 d�cembre 2015'
ms.openlocfilehash: ce25c6777c8a71da0fe11e0bbf34eefafe2ca50d
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/23/2018
ms.locfileid: "22564135"
---
# <a name="disconnecting-an-offline-state-add-in"></a><span data-ttu-id="20f9e-103">Déconnexion d’un complément d’état hors connexion</span><span class="sxs-lookup"><span data-stu-id="20f9e-103">Disconnecting an Offline State Add-in</span></span>

<span data-ttu-id="20f9e-104">**S’applique à**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="20f9e-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="20f9e-105">Lorsque le complément hors connexion est déconnecté, vous devez implémenter les fonctions pour terminer correctement et de nettoyer le complément.</span><span class="sxs-lookup"><span data-stu-id="20f9e-105">When the offline state add-in is disconnected, you must implement functions to properly terminate and clean up the add-in.</span></span> <span data-ttu-id="20f9e-106">Pour plus d’informations sur la configuration et l’utilisation hors connexion d’état de complément pour surveiller les changements d’état de connexion, voir le [complément de paramètre d’un état en mode hors connexion](setting-up-an-offline-state-add-in.md) et [Surveillance connexion état modifications en utilisant un complément état hors connexion](monitoring-connection-state-changes-using-an-offline-state-add-in.md).</span><span class="sxs-lookup"><span data-stu-id="20f9e-106">For more information on setting up and using the offline state add-in to monitor connection state changes, see [Setting Up an Offline State Add-in](setting-up-an-offline-state-add-in.md) and [Monitoring Connection State Changes Using an Offline State Add-in](monitoring-connection-state-changes-using-an-offline-state-add-in.md).</span></span>
  
<span data-ttu-id="20f9e-107">Dans cette rubrique, ces de déconnexion, terminer et le nettoyage des fonctions sont illustrées à l’aide des exemples de code à partir de la macro complémentaire exemple hors connexion état.</span><span class="sxs-lookup"><span data-stu-id="20f9e-107">In this topic, these disconnection, terminate, and clean-up functions are demonstrated by using code examples from the Sample Offline State Add-in.</span></span> <span data-ttu-id="20f9e-108">Le complément exemple hors connexion état est un complément COM qui ajoute un menu **État hors connexion** dans Outlook et utilise l’API de l’état en mode hors connexion.</span><span class="sxs-lookup"><span data-stu-id="20f9e-108">The Sample Offline State Add-in is a COM add-in that adds an **Offline State** menu to Outlook and uses the Offline State API.</span></span> <span data-ttu-id="20f9e-109">Via le menu état hors connexion, vous pouvez activer ou désactiver l’analyse de l’état, vérifiez l’état en cours et modifier l’état actuel.</span><span class="sxs-lookup"><span data-stu-id="20f9e-109">Through the Offline State menu, you can enable or disable state monitoring, check the current state, and change the current state.</span></span> <span data-ttu-id="20f9e-110">Pour plus d’informations sur le téléchargement et l’installation du complément exemple hors connexion état, consultez [installation du complément exemple hors connexion état](installing-the-sample-offline-state-add-in.md).</span><span class="sxs-lookup"><span data-stu-id="20f9e-110">For more information about downloading and installing the Sample Offline State Add-in, see [Installing the Sample Offline State Add-in](installing-the-sample-offline-state-add-in.md).</span></span> <span data-ttu-id="20f9e-111">Pour plus d’informations sur l’API de l’état en mode hors connexion, voir [à propos en mode hors connexion état API](about-the-offline-state-api.md).</span><span class="sxs-lookup"><span data-stu-id="20f9e-111">For more information about the Offline State API, see [About the Offline State API](about-the-offline-state-api.md).</span></span>
  
## <a name="on-disconnection-routine"></a><span data-ttu-id="20f9e-112">Dans la Routine de déconnexion</span><span class="sxs-lookup"><span data-stu-id="20f9e-112">On Disconnection Routine</span></span>

<span data-ttu-id="20f9e-113">La méthode **IDTExtensibility2.OnDisconnection** est appelée lorsque l’état hors connexion est déchargé.</span><span class="sxs-lookup"><span data-stu-id="20f9e-113">The **IDTExtensibility2.OnDisconnection** method is called when the Offline State Add-in is unloaded.</span></span> <span data-ttu-id="20f9e-114">Vous devez implémenter nettoyer le code de cette fonction.</span><span class="sxs-lookup"><span data-stu-id="20f9e-114">You should implement clean up code in this function.</span></span> <span data-ttu-id="20f9e-115">Dans l’exemple suivant, la fonction **IDTExtensibility2.OnDisconnection** appelle le `HrTermAddin` fonction.</span><span class="sxs-lookup"><span data-stu-id="20f9e-115">In the following example, the **IDTExtensibility2.OnDisconnection** function calls the  `HrTermAddin` function.</span></span> 
  
### <a name="cmyaddinondisconnection-example"></a><span data-ttu-id="20f9e-116">Exemple CMyAddin::OnDisconnection()</span><span class="sxs-lookup"><span data-stu-id="20f9e-116">CMyAddin::OnDisconnection() example</span></span>

```cpp
STDMETHODIMP CMyAddin::OnDisconnection(ext_DisconnectMode /*RemoveMode*/, SAFEARRAY * * /*custom*/) 
{ 
    Log(true,"OnDisconnection\n"); 
    HRESULT hRes = S_OK; 
    hRes = HrTermAddin(); 
     return hRes; 
}
```

## <a name="terminate-add-in-function"></a><span data-ttu-id="20f9e-117">Mettre fin à la fonction complémentaire</span><span class="sxs-lookup"><span data-stu-id="20f9e-117">Terminate Add-in Function</span></span>

<span data-ttu-id="20f9e-118">Les `HrTermAddin` les appels de fonction la `inDeInitMonitor`, `HrRemoveMenuItems`, et `UnloadLibraries` fonctions pour terminer le nettoyage de la macro complémentaire état hors connexion.</span><span class="sxs-lookup"><span data-stu-id="20f9e-118">The  `HrTermAddin` function calls the  `inDeInitMonitor`,  `HrRemoveMenuItems`, and  `UnloadLibraries` functions to finish cleaning up the Offline State Add-in.</span></span> 
  
### <a name="cmyaddinhrtermaddin-example"></a><span data-ttu-id="20f9e-119">Exemple CMyAddin::HrTermAddin()</span><span class="sxs-lookup"><span data-stu-id="20f9e-119">CMyAddin::HrTermAddin() example</span></span>

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

## <a name="deinitialize-monitor-routine"></a><span data-ttu-id="20f9e-120">Désinitialiser Routine moniteur</span><span class="sxs-lookup"><span data-stu-id="20f9e-120">Deinitialize Monitor Routine</span></span>

<span data-ttu-id="20f9e-121">Le `inDeInitMonitor` fonction appelle la fonction [IMAPIOfflineMgr::Unadvise](imapiofflinemgr-unadvise.md) pour annuler des rappels pour l’objet en mode hors connexion.</span><span class="sxs-lookup"><span data-stu-id="20f9e-121">The  `inDeInitMonitor` function calls the [IMAPIOfflineMgr::Unadvise](imapiofflinemgr-unadvise.md) function to cancel the callbacks for the offline object.</span></span> 
  
### <a name="deinitmonitor-example"></a><span data-ttu-id="20f9e-122">Exemple DeInitMonitor()</span><span class="sxs-lookup"><span data-stu-id="20f9e-122">DeInitMonitor() example</span></span>

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

## <a name="remove-menu-items-routine"></a><span data-ttu-id="20f9e-123">Supprimer la Routine d’éléments de Menu</span><span class="sxs-lookup"><span data-stu-id="20f9e-123">Remove Menu Items Routine</span></span>

<span data-ttu-id="20f9e-124">Les `HrRemoveMenuItems` les appels de fonction `DispEventUnadvise` pour chaque élément de menu dans le menu **État hors connexion** , puis supprime le menu **d’État hors connexion** .</span><span class="sxs-lookup"><span data-stu-id="20f9e-124">The  `HrRemoveMenuItems` function calls  `DispEventUnadvise` for each menu item under the **Offline State** menu, and then deletes the **Offline State** menu.</span></span> 
  
### <a name="cmyaddinhrremovemenuitems-example"></a><span data-ttu-id="20f9e-125">Exemple CMyAddin::HrRemoveMenuItems()</span><span class="sxs-lookup"><span data-stu-id="20f9e-125">CMyAddin::HrRemoveMenuItems() example</span></span>

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

## <a name="unload-libraries-routine"></a><span data-ttu-id="20f9e-126">Déchargement d’une Routine de bibliothèques</span><span class="sxs-lookup"><span data-stu-id="20f9e-126">Unload Libraries Routine</span></span>

<span data-ttu-id="20f9e-127">Lorsque le complément est déchargé à partir d’Outlook, le `UnloadLibraries` fonction décharge les bibliothèques de liens dynamiques (DLL) nécessitant la macro complémentaire.</span><span class="sxs-lookup"><span data-stu-id="20f9e-127">When the add-in is unloaded from Outlook, the  `UnloadLibraries` function unloads the dynamic-link libraries (DLLs) that the add-in required.</span></span> 
  
### <a name="unloadlibraries-example"></a><span data-ttu-id="20f9e-128">Exemple UnloadLibraries()</span><span class="sxs-lookup"><span data-stu-id="20f9e-128">UnloadLibraries() example</span></span>

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

## <a name="see-also"></a><span data-ttu-id="20f9e-129">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="20f9e-129">See also</span></span>

- [<span data-ttu-id="20f9e-130">À propos de l’API d’état hors connexion</span><span class="sxs-lookup"><span data-stu-id="20f9e-130">About the Offline State API</span></span>](about-the-offline-state-api.md)
- [<span data-ttu-id="20f9e-131">Installation de l’exemple de complément d’état hors connexion</span><span class="sxs-lookup"><span data-stu-id="20f9e-131">Installing the Sample Offline State Add-in</span></span>](installing-the-sample-offline-state-add-in.md)
- [<span data-ttu-id="20f9e-132">À propos de l’exemple de complément d’état hors connexion</span><span class="sxs-lookup"><span data-stu-id="20f9e-132">About the Sample Offline State Add-in</span></span>](about-the-sample-offline-state-add-in.md)
- [<span data-ttu-id="20f9e-133">Configuration d’un complément d’état hors connexion</span><span class="sxs-lookup"><span data-stu-id="20f9e-133">Setting Up an Offline State Add-in</span></span>](setting-up-an-offline-state-add-in.md)
- [<span data-ttu-id="20f9e-134">Surveillance des modifications de l’état de connexion à l’aide d’un complément d’état hors connexion</span><span class="sxs-lookup"><span data-stu-id="20f9e-134">Monitoring Connection State Changes Using an Offline State Add-in</span></span>](monitoring-connection-state-changes-using-an-offline-state-add-in.md)

