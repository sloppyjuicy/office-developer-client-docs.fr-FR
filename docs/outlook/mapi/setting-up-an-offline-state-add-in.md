---
title: Configuration d’un complément hors connexion
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
ms.assetid: 2a326e93-fe8c-e3a5-1e92-30b75b6cb1d2
description: 'Derni�re modification�: jeudi 5 juillet 2012'
ms.openlocfilehash: 7b3d0eed6039552813798d4ceb30158444902b36
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19787145"
---
# <a name="setting-up-an-offline-state-add-in"></a><span data-ttu-id="fd69a-103">Configuration d’un complément hors connexion</span><span class="sxs-lookup"><span data-stu-id="fd69a-103">Setting up an offline state add-in</span></span>

<span data-ttu-id="fd69a-104">**S’applique à**: Outlook</span><span class="sxs-lookup"><span data-stu-id="fd69a-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="fd69a-105">Pour implémenter un complément hors connexion, vous devez implémenter la connexion, d’initialisation et d’autres fonctions du programme d’installation.</span><span class="sxs-lookup"><span data-stu-id="fd69a-105">To implement an offline state add-in, you must implement connection, initialization, and other setup functions.</span></span> <span data-ttu-id="fd69a-106">Dans cette rubrique, ces connexions, l’initialisation et le programme d’installation des fonctions sont illustrées à l’aide des exemples de code à partir de la macro complémentaire exemple hors connexion état.</span><span class="sxs-lookup"><span data-stu-id="fd69a-106">In this topic, these connection, initialization, and setup functions are demonstrated by using code examples from the Sample Offline State Add-in.</span></span> <span data-ttu-id="fd69a-107">Le complément exemple hors connexion état est un complément COM qui ajoute un menu **État hors connexion** dans Outlook et utilise l’API de l’état en mode hors connexion.</span><span class="sxs-lookup"><span data-stu-id="fd69a-107">The Sample Offline State Add-in is a COM add-in that adds an **Offline State** menu to Outlook and uses the Offline State API.</span></span> <span data-ttu-id="fd69a-108">Via le menu **État hors connexion** , vous pouvez activer ou désactiver l’analyse de l’état, vérifiez l’état en cours et modifier l’état actuel.</span><span class="sxs-lookup"><span data-stu-id="fd69a-108">Through the **Offline State** menu, you can enable or disable state monitoring, check the current state, and change the current state.</span></span> <span data-ttu-id="fd69a-109">Pour plus d’informations sur le téléchargement et l’installation du complément exemple hors connexion état, consultez [installation du complément exemple hors connexion état](installing-the-sample-offline-state-add-in.md).</span><span class="sxs-lookup"><span data-stu-id="fd69a-109">For more information about downloading and installing the Sample Offline State Add-in, see [Installing the Sample Offline State Add-in](installing-the-sample-offline-state-add-in.md).</span></span> <span data-ttu-id="fd69a-110">Pour plus d’informations sur l’API de l’état en mode hors connexion, voir [à propos en mode hors connexion état API](about-the-offline-state-api.md).</span><span class="sxs-lookup"><span data-stu-id="fd69a-110">For more information about the Offline State API, see [About the Offline State API](about-the-offline-state-api.md).</span></span>
  
<span data-ttu-id="fd69a-111">Après avoir configuré un complément hors connexion, vous devez implémenter les fonctions pour surveiller et modifier des changements d’état de connexion.</span><span class="sxs-lookup"><span data-stu-id="fd69a-111">After you set up an offline state add-in, you must implement functions to monitor and modify connection state changes.</span></span> <span data-ttu-id="fd69a-112">Pour plus d’informations, voir [Surveillance connexion état modifications à l’aide de complément état hors connexion](monitoring-connection-state-changes-using-an-offline-state-add-in.md).</span><span class="sxs-lookup"><span data-stu-id="fd69a-112">For more information, see [Monitoring Connection State Changes Using an Offline State Add-in](monitoring-connection-state-changes-using-an-offline-state-add-in.md).</span></span>
  
## <a name="on-connection-routine"></a><span data-ttu-id="fd69a-113">Dans la routine de connexion</span><span class="sxs-lookup"><span data-stu-id="fd69a-113">On Connection routine</span></span>

<span data-ttu-id="fd69a-114">La **[Méthode IDTExtensibility2.OnConnection](http://msdn.microsoft.com/fr-fr/library/extensibility.idtextensibility2.onconnection%28v=VS.80%29.aspx)** est appelé chaque fois qu’un complément est chargé.</span><span class="sxs-lookup"><span data-stu-id="fd69a-114">The **[IDTExtensibility2.OnConnection Method](http://msdn.microsoft.com/fr-fr/library/extensibility.idtextensibility2.onconnection%28v=VS.80%29.aspx)** is called every time an add-in is loaded.</span></span> <span data-ttu-id="fd69a-115">Il est le point d’entrée pour le complément, de sorte que le code que vous avez placé dans le `OnConnection` fonction est appelée lorsque le complément démarre.</span><span class="sxs-lookup"><span data-stu-id="fd69a-115">It is the entry point for the add-in, so the code you put in the  `OnConnection` function will be called when the add-in starts.</span></span> <span data-ttu-id="fd69a-116">Dans l’exemple suivant, la `OnConnection` les appels de fonction la `HrInitAddin` fonction.</span><span class="sxs-lookup"><span data-stu-id="fd69a-116">In the following example, the  `OnConnection` function calls the  `HrInitAddin` function.</span></span> 
  
### <a name="cmyaddinonconnection-example"></a><span data-ttu-id="fd69a-117">Exemple CMyAddin::OnConnection()</span><span class="sxs-lookup"><span data-stu-id="fd69a-117">CMyAddin::OnConnection() example</span></span>

```cpp
STDMETHODIMP CMyAddin::OnConnection( 
    IDispatch * Application,  
    ext_ConnectMode ConnectMode,  
    IDispatch * /*AddInInst*/,  
    SAFEARRAY * * /*custom*/) 
{ 
    Log(true,"OnConnection\n"); 
    HRESULT hRes = S_OK; 
    m_spApp = Application; 
    m_ConnectMode = ConnectMode; 
    if (ConnectMode == ext_cm_AfterStartup) 
        hRes = HrInitAddin(); 
    return hRes; 
}
```

## <a name="initialize-add-in-routine"></a><span data-ttu-id="fd69a-118">Initialiser le complément de routine</span><span class="sxs-lookup"><span data-stu-id="fd69a-118">Initialize Add-in routine</span></span>

<span data-ttu-id="fd69a-119">Les `HrInitAddin` les appels de fonction la `LoadLibraries`, `HrCacheProfileName`, et `HrAddMenuItems` fonctions pour terminer la configuration du complément hors connexion.</span><span class="sxs-lookup"><span data-stu-id="fd69a-119">The  `HrInitAddin` function calls the  `LoadLibraries`,  `HrCacheProfileName`, and  `HrAddMenuItems` functions to finish setting up the offline state add-in.</span></span> 
  
### <a name="cmyaddinhrinitaddin-example"></a><span data-ttu-id="fd69a-120">Exemple CMyAddin::HrInitAddin()</span><span class="sxs-lookup"><span data-stu-id="fd69a-120">CMyAddin::HrInitAddin() example</span></span>

```cpp
HRESULT CMyAddin::HrInitAddin() 
{ 
    HRESULT hRes = S_OK; 
    LoadLibraries(); 
    hRes = HrCacheProfileName(); 
    Log(true,_T("HrCacheProfileName returned 0x%08X\n"),hRes); 
    hRes = HrAddMenuItems(); 
    Log(true,_T("HrAddMenuItems returned 0x%08X\n"),hRes); 
    return hRes; 
}
```

## <a name="load-libraries-routine"></a><span data-ttu-id="fd69a-121">Charger une routine de bibliothèques</span><span class="sxs-lookup"><span data-stu-id="fd69a-121">Load Libraries routine</span></span>

<span data-ttu-id="fd69a-122">Le `LoadLibraries` fonction charge les fichiers de bibliothèque de liens dynamiques (DLL) nécessitant la macro complémentaire.</span><span class="sxs-lookup"><span data-stu-id="fd69a-122">The  `LoadLibraries` function loads the dynamic-link library (DLL) files that the add-in requires.</span></span> 
  
### <a name="loadlibraries-example"></a><span data-ttu-id="fd69a-123">Exemple LoadLibraries()</span><span class="sxs-lookup"><span data-stu-id="fd69a-123">LoadLibraries() example</span></span>

```cpp
void LoadLibraries() 
{ 
    Log(true,_T("LoadLibraries - loading exports from DLLs\n"));     
    HRESULT hRes = S_OK; 
    UINT uiRet = 0; 
    LONG lRet = 0; 
    BOOL bRet = true; 
    CHAR szSystemDir[MAX_PATH+1] = {0}; 
 
    // Get the system directory path 
    // (mapistub.dll and mapi32.dll reside here) 
    uiRet = GetSystemDirectoryA(szSystemDir, MAX_PATH); 
    if (uiRet > 0) 
    { 
        CHAR szDLLPath[MAX_PATH+1] = {0}; 
        hRes = StringCchPrintfA(szDLLPath, MAX_PATH+1, "%s\\%s",  
            szSystemDir, "mapistub.dll"); 
        if (SUCCEEDED(hRes)) 
        { 
            LPFGETCOMPONENTPATH pfnFGetComponentPath = NULL; 
            // Load mapistub.dll 
            hModMAPIStub = LoadLibraryA(szDLLPath); 
            if (hModMAPIStub) 
            {    
                // Get the address of FGetComponentPath from the mapistub 
                pfnFGetComponentPath = (LPFGETCOMPONENTPATH)GetProcAddress( 
                    hModMAPIStub, "FGetComponentPath"); 
            } 
            // If there is no address for FGetComponentPath yet 
            // try getting it from mapi32.dll 
            if (!pfnFGetComponentPath) 
            { 
                hRes = StringCchPrintfA(szDLLPath, MAX_PATH+1, "%s\\%s", 
                    szSystemDir, "mapi32.dll"); 
                if (SUCCEEDED(hRes)) 
                { 
                    // Load mapi32.dll 
                    hModMAPI = LoadLibraryA(szDLLPath); 
                    if (hModMAPI) 
                    { 
                        // Get the address of FGetComponentPath from mapi32 
                        pfnFGetComponentPath = (LPFGETCOMPONENTPATH)GetProcAddress( 
                            hModMAPI, "FGetComponentPath"); 
                    } 
                } 
            } 
            if (pfnFGetComponentPath) 
            { 
                LPSTR szAppLCID = NULL; 
                LPSTR szOfficeLCID = NULL; 
                HKEY hMicrosoftOutlook = NULL; 
                lRet = RegOpenKeyEx( 
                    HKEY_LOCAL_MACHINE, 
                    _T("Software\\Clients\\Mail\\Microsoft Outlook"), 
                    NULL, 
                    KEY_READ, 
                    &hMicrosoftOutlook); 
                if (ERROR_SUCCESS == lRet && hMicrosoftOutlook) 
                { 
                    HrGetRegMultiSZValueA(hMicrosoftOutlook, "MSIApplicationLCID", (LPVOID*) &szAppLCID); 
                    HrGetRegMultiSZValueA(hMicrosoftOutlook, "MSIOfficeLCID", (LPVOID*) &szOfficeLCID); 
                } 
                if (szAppLCID) 
                { 
                    bRet = pfnFGetComponentPath( 
                        "{FF1D0740-D227-11D1-A4B0-006008AF820E}", szAppLCID, szDLLPath, MAX_PATH, true); 
                } 
                if ((!bRet || szDLLPath[0] == _T('\0')) && szOfficeLCID) 
                { 
                    bRet = pfnFGetComponentPath( 
                        "{FF1D0740-D227-11D1-A4B0-006008AF820E}", szOfficeLCID, szDLLPath, MAX_PATH, true); 
                } 
                if (!bRet || szDLLPath[0] == _T('\0')) 
                { 
                    bRet = pfnFGetComponentPath( 
                        "{FF1D0740-D227-11D1-A4B0-006008AF820E}", NULL, szDLLPath, MAX_PATH, true); 
                } 
                delete[] szOfficeLCID; 
                delete[] szAppLCID; 
                if (hMicrosoftOutlook) RegCloseKey(hMicrosoftOutlook);       
            } 
            hModMSMAPI = LoadLibrary(szDLLPath); 
            if (hModMSMAPI) 
            { 
                pfnHrOpenOfflineObj = (HROPENOFFLINEOBJ*) GetProcAddress( 
                    hModMSMAPI, 
                    "HrOpenOfflineObj@20"); 
                pfnMAPIFreeBuffer = (LPMAPIFREEBUFFER) GetProcAddress( 
                    hModMSMAPI, 
                    "MAPIFreeBuffer"); 
            } 
        } 
    }    
}
```

## <a name="cache-profile-name-routine"></a><span data-ttu-id="fd69a-124">Routine de nom du profil de cache</span><span class="sxs-lookup"><span data-stu-id="fd69a-124">Cache Profile Name routine</span></span>

<span data-ttu-id="fd69a-125">Le `HrCacheProfileName` fonction appelle la fonction **[IMAPISupport::OpenProfileSection](imapisupport-openprofilesection.md)** pour ouvrir une section de profil pour la session active, puis définit le profil pour les gestionnaires de bouton.</span><span class="sxs-lookup"><span data-stu-id="fd69a-125">The  `HrCacheProfileName` function calls the **[IMAPISupport::OpenProfileSection](imapisupport-openprofilesection.md)** function to open a profile section for the current session, and then sets the profile for the button handlers.</span></span> 
  
### <a name="cmyaddinhrcacheprofilename-example"></a><span data-ttu-id="fd69a-126">Exemple CMyAddin::HrCacheProfileName()</span><span class="sxs-lookup"><span data-stu-id="fd69a-126">CMyAddin::HrCacheProfileName() example</span></span>

```cpp
HRESULT CMyAddin::HrCacheProfileName() 
{ 
    HRESULT hRes = S_OK;     
    _NameSpacePtr spSession = m_spApp->GetNamespace("MAPI"); 
    IUnknown* lpMAPIObject = NULL; 
    LPMAPISESSION lpMAPISession = NULL; 
    // use the raw accessor 
    hRes = spSession->get_MAPIOBJECT(&lpMAPIObject); 
    if (SUCCEEDED(hRes) && lpMAPIObject) 
    { 
        hRes = lpMAPIObject->QueryInterface(IID_IMAPISession,(LPVOID*)&lpMAPISession); 
    } 
    if (SUCCEEDED(hRes) && lpMAPISession) 
    { 
        LPPROFSECT lpPSGlobal = NULL; 
        hRes = lpMAPISession->OpenProfileSection((LPMAPIUID)pbGlobalProfileSectionGuid, NULL, 0, &lpPSGlobal); 
 
        if (SUCCEEDED(hRes) && lpPSGlobal) 
        { 
            LPSPropValue lpProfileName = NULL; 
            // Asking for PR_PROFILE_NAME_W here - this might not work with earlier versions of Outlook 
            SPropTagArray staga = {1,PR_PROFILE_NAME_W}; 
            ULONG cVal = 0; 
            hRes = lpPSGlobal->GetProps(&staga,0,&cVal,&lpProfileName); 
            if (SUCCEEDED(hRes) && 1 == cVal && lpProfileName && PR_PROFILE_NAME_W == lpProfileName->ulPropTag) 
            { 
                m_InitButtonHandler.SetProfile(lpProfileName->Value.lpszW); 
                m_GetStateButtonHandler.SetProfile(lpProfileName->Value.lpszW); 
                m_SetStateButtonHandler.SetProfile(lpProfileName->Value.lpszW); 
            } 
            if (pfnMAPIFreeBuffer) pfnMAPIFreeBuffer(lpProfileName); 
        } 
        if (lpPSGlobal) lpPSGlobal->Release(); 
    } 
    if (lpMAPISession) lpMAPISession->Release(); 
    return hRes; 
}
```

## <a name="add-menu-items-routine"></a><span data-ttu-id="fd69a-127">Ajouter des éléments de Menu routine</span><span class="sxs-lookup"><span data-stu-id="fd69a-127">Add Menu Items routine</span></span>

<span data-ttu-id="fd69a-128">Le `HrAddMenuItems` fonction définit les options de menu qui s’affichent dans le menu **État hors connexion** qui est créé lorsque le complément est chargé dans Outlook et appelle ensuite `DispEventAdvise` pour chaque élément de menu.</span><span class="sxs-lookup"><span data-stu-id="fd69a-128">The  `HrAddMenuItems` function defines the menu options that appear under the **Offline State** menu that is created when the add-in is loaded in Outlook, and then calls  `DispEventAdvise` for each menu item.</span></span> 
  
### <a name="cmyaddinhraddmenuitems-example"></a><span data-ttu-id="fd69a-129">Exemple CMyAddin::HrAddMenuItems()</span><span class="sxs-lookup"><span data-stu-id="fd69a-129">CMyAddin::HrAddMenuItems() example</span></span>

```cpp
HRESULT CMyAddin::HrAddMenuItems() 
{ 
    Log(true,"HrAddMenuItems\n"); 
    HRESULT    hRes = S_OK; 
    if (!m_fMenuItemsAdded) 
    { 
        try 
        { 
            _ExplorerPtr spExplorer = m_spApp->ActiveExplorer(); 
            _CommandBarsPtr spCmdBars = spExplorer->__CommandBars; 
            CommandBarPtr spMainBar = spCmdBars->ActiveMenuBar; 
            CommandBarControlsPtr spMainCtrls = spMainBar->Controls; 
 
            try { m_spMyMenu = spMainCtrls->GetItem("Offline State"); } catch (_com_error) {} 
            if (m_spMyMenu == NULL) 
            {             
                m_spMyMenu = spMainCtrls->Add((long)msoControlPopup,vtMissing,vtMissing,vtMissing, true); 
                m_spMyMenu->Caption = "Offline State"; 
            } 
 
            CommandBarControlsPtr spMyMenuCtrls = m_spMyMenu->Controls; 
            try { m_spInitButton = spMyMenuCtrls->GetItem("&Init Monitor"); } catch (_com_error) {} 
            if (m_spInitButton == NULL) 
            { 
                m_spInitButton = spMyMenuCtrls->Add((long)msoControlButton, vtMissing, vtMissing, vtMissing, true); 
                m_spInitButton->Caption = "&Init Monitor"; 
                m_spInitButton->FaceId = MY_INIT_BUTTON; 
            } 
            try { m_spDeinitButton = spMyMenuCtrls->GetItem("&Deinit Monitor"); } catch (_com_error) {} 
            if (m_spDeinitButton == NULL) 
            { 
                m_spDeinitButton = spMyMenuCtrls->Add((long)msoControlButton, vtMissing, vtMissing, vtMissing, true); 
                m_spDeinitButton->Caption = "&Deinit Monitor"; 
                m_spDeinitButton->FaceId = MY_DEINIT_BUTTON; 
            } 
            try { m_spGetStateButton = spMyMenuCtrls->GetItem("&GetCurrentState"); } catch (_com_error) {} 
            if (m_spGetStateButton == NULL) 
            { 
                m_spGetStateButton = spMyMenuCtrls->Add((long)msoControlButton, vtMissing, vtMissing, vtMissing, true); 
                m_spGetStateButton->Caption = "&GetCurrentState"; 
                m_spGetStateButton->FaceId = MY_GETSTATE_BUTTON; 
            } 
            try { m_spSetStateButton = spMyMenuCtrls->GetItem("&SetCurrentState"); } catch (_com_error) {} 
            if (m_spSetStateButton == NULL) 
            { 
                m_spSetStateButton = spMyMenuCtrls->Add((long)msoControlButton, vtMissing, vtMissing, vtMissing, true); 
                m_spSetStateButton->Caption = "&SetCurrentState"; 
                m_spSetStateButton->FaceId = MY_SETSTATE_BUTTON; 
            } 
            // Set up advise 
            _com_util::CheckError(m_InitButtonHandler.DispEventAdvise(m_spInitButton)); 
            _com_util::CheckError(m_DeinitButtonHandler.DispEventAdvise(m_spDeinitButton)); 
            _com_util::CheckError(m_GetStateButtonHandler.DispEventAdvise(m_spGetStateButton)); 
            _com_util::CheckError(m_SetStateButtonHandler.DispEventAdvise(m_spSetStateButton)); 
        } 
        catch (_com_error) 
        { 
            hRes = E_FAIL; 
        } 
        if (SUCCEEDED(hRes)) 
        { 
            m_fMenuItemsAdded = true; 
        } 
    } 
    return hRes;  
}
```

## <a name="see-also"></a><span data-ttu-id="fd69a-130">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="fd69a-130">See also</span></span>

- [<span data-ttu-id="fd69a-131">À propos de l’API d’état en mode hors connexion</span><span class="sxs-lookup"><span data-stu-id="fd69a-131">About the Offline State API</span></span>](about-the-offline-state-api.md) 
- [<span data-ttu-id="fd69a-132">L’installation de l’exemple en mode hors connexion d’état complément</span><span class="sxs-lookup"><span data-stu-id="fd69a-132">Installing the Sample Offline State Add-in</span></span>](installing-the-sample-offline-state-add-in.md)
- [<span data-ttu-id="fd69a-133">À propos de l’exemple en mode hors connexion-dans l’état</span><span class="sxs-lookup"><span data-stu-id="fd69a-133">About the Sample Offline State Add-in</span></span>](about-the-sample-offline-state-add-in.md)
- [<span data-ttu-id="fd69a-134">Analyse l’état de connexion change utilisant un complément en mode hors connexion d’état</span><span class="sxs-lookup"><span data-stu-id="fd69a-134">Monitoring Connection State Changes Using an Offline State Add-in</span></span>](monitoring-connection-state-changes-using-an-offline-state-add-in.md)
- [<span data-ttu-id="fd69a-135">Déconnexion d’un complément en mode hors connexion d’état</span><span class="sxs-lookup"><span data-stu-id="fd69a-135">Disconnecting an Offline State Add-in</span></span>](disconnecting-an-offline-state-add-in.md)

