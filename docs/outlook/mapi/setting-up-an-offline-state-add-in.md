---
title: Configuration d’un add-in d’état hors connexion
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
ms.assetid: 2a326e93-fe8c-e3a5-1e92-30b75b6cb1d2
description: 'Derni�re modification�: jeudi 5 juillet 2012'
ms.openlocfilehash: fa3cee9e6b25a9bcb951fbcbfa4435890341a872
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32339290"
---
# <a name="setting-up-an-offline-state-add-in"></a><span data-ttu-id="e3988-103">Configuration d’un add-in d’état hors connexion</span><span class="sxs-lookup"><span data-stu-id="e3988-103">Setting up an offline state add-in</span></span>

<span data-ttu-id="e3988-104">**S’applique à** : Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="e3988-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="e3988-105">Pour implémenter un add-in d’état hors connexion, vous devez implémenter la connexion, l’initialisation et d’autres fonctions d’installation.</span><span class="sxs-lookup"><span data-stu-id="e3988-105">To implement an offline state add-in, you must implement connection, initialization, and other setup functions.</span></span> <span data-ttu-id="e3988-106">Dans cette rubrique, ces fonctions de connexion, d’initialisation et d’installation sont démontrées à l’aide d’exemples de code de l’exemple de add-in d’état hors connexion.</span><span class="sxs-lookup"><span data-stu-id="e3988-106">In this topic, these connection, initialization, and setup functions are demonstrated by using code examples from the Sample Offline State Add-in.</span></span> <span data-ttu-id="e3988-107">L’exemple de complément d’état hors connexion est un complément COM qui ajoute un menu **État hors connexion** à Outlook et qui utilise l’API d’état hors connexion.</span><span class="sxs-lookup"><span data-stu-id="e3988-107">The Sample Offline State Add-in is a COM add-in that adds an **Offline State** menu to Outlook and uses the Offline State API.</span></span> <span data-ttu-id="e3988-108">Dans le menu **État** hors connexion, vous pouvez activer ou désactiver la surveillance de l’état, vérifier l’état actuel et modifier l’état actuel.</span><span class="sxs-lookup"><span data-stu-id="e3988-108">Through the **Offline State** menu, you can enable or disable state monitoring, check the current state, and change the current state.</span></span> <span data-ttu-id="e3988-109">Pour plus d’informations sur le téléchargement et l’installation de l’exemple de complément d’état hors connexion, reportez-vous à l’article [Installation de l’exemple de complément d’état hors connexion](installing-the-sample-offline-state-add-in.md).</span><span class="sxs-lookup"><span data-stu-id="e3988-109">For more information about downloading and installing the Sample Offline State Add-in, see [Installing the Sample Offline State Add-in](installing-the-sample-offline-state-add-in.md).</span></span> <span data-ttu-id="e3988-110">Pour plus d’informations sur l’API d’état hors connexion, reportez-vous à l’article [À propos de l’API d’état hors connexion](about-the-offline-state-api.md).</span><span class="sxs-lookup"><span data-stu-id="e3988-110">For more information about the Offline State API, see [About the Offline State API](about-the-offline-state-api.md).</span></span>
  
<span data-ttu-id="e3988-111">Après avoir installé un add-in d’état hors connexion, vous devez implémenter des fonctions pour surveiller et modifier les changements d’état de connexion.</span><span class="sxs-lookup"><span data-stu-id="e3988-111">After you set up an offline state add-in, you must implement functions to monitor and modify connection state changes.</span></span> <span data-ttu-id="e3988-112">Pour plus d’informations, voir [Monitoring Connection State Changes Using an Offline State Add-in](monitoring-connection-state-changes-using-an-offline-state-add-in.md).</span><span class="sxs-lookup"><span data-stu-id="e3988-112">For more information, see [Monitoring Connection State Changes Using an Offline State Add-in](monitoring-connection-state-changes-using-an-offline-state-add-in.md).</span></span>
  
## <a name="on-connection-routine"></a><span data-ttu-id="e3988-113">Routine de connexion</span><span class="sxs-lookup"><span data-stu-id="e3988-113">On Connection routine</span></span>

<span data-ttu-id="e3988-114">La **[méthode IDTExtensibility2.OnConnection](https://msdn.microsoft.com/library/extensibility.idtextensibility2.onconnection%28v=VS.80%29.aspx)** est appelée chaque fois qu’un module est chargé.</span><span class="sxs-lookup"><span data-stu-id="e3988-114">The **[IDTExtensibility2.OnConnection Method](https://msdn.microsoft.com/library/extensibility.idtextensibility2.onconnection%28v=VS.80%29.aspx)** is called every time an add-in is loaded.</span></span> <span data-ttu-id="e3988-115">Il s’agit du point d’entrée du module, de sorte que le code que vous avez placé dans la fonction est appelé au démarrage  `OnConnection` du module.</span><span class="sxs-lookup"><span data-stu-id="e3988-115">It is the entry point for the add-in, so the code you put in the  `OnConnection` function will be called when the add-in starts.</span></span> <span data-ttu-id="e3988-116">Dans l’exemple suivant, la  `OnConnection` fonction appelle la  `HrInitAddin` fonction.</span><span class="sxs-lookup"><span data-stu-id="e3988-116">In the following example, the  `OnConnection` function calls the  `HrInitAddin` function.</span></span> 
  
### <a name="cmyaddinonconnection-example"></a><span data-ttu-id="e3988-117">Exemple CMyAddin::OnConnection()</span><span class="sxs-lookup"><span data-stu-id="e3988-117">CMyAddin::OnConnection() example</span></span>

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

## <a name="initialize-add-in-routine"></a><span data-ttu-id="e3988-118">Initialiser la routine de l’ajout</span><span class="sxs-lookup"><span data-stu-id="e3988-118">Initialize Add-in routine</span></span>

<span data-ttu-id="e3988-119">La fonction appelle le , et les fonctions pour terminer la configuration du  `HrInitAddin`  `LoadLibraries`  `HrCacheProfileName`  `HrAddMenuItems` add-in d’état hors connexion.</span><span class="sxs-lookup"><span data-stu-id="e3988-119">The  `HrInitAddin` function calls the  `LoadLibraries`,  `HrCacheProfileName`, and  `HrAddMenuItems` functions to finish setting up the offline state add-in.</span></span> 
  
### <a name="cmyaddinhrinitaddin-example"></a><span data-ttu-id="e3988-120">Exemple CMyAddin::HrInitAddin()</span><span class="sxs-lookup"><span data-stu-id="e3988-120">CMyAddin::HrInitAddin() example</span></span>

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

## <a name="load-libraries-routine"></a><span data-ttu-id="e3988-121">Routine Load Libraries</span><span class="sxs-lookup"><span data-stu-id="e3988-121">Load Libraries routine</span></span>

<span data-ttu-id="e3988-122">La fonction charge les fichiers de bibliothèque de liens dynamiques  `LoadLibraries` (DLL) dont le add-in a besoin.</span><span class="sxs-lookup"><span data-stu-id="e3988-122">The  `LoadLibraries` function loads the dynamic-link library (DLL) files that the add-in requires.</span></span> 
  
### <a name="loadlibraries-example"></a><span data-ttu-id="e3988-123">Exemple LoadLibraries()</span><span class="sxs-lookup"><span data-stu-id="e3988-123">LoadLibraries() example</span></span>

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

## <a name="cache-profile-name-routine"></a><span data-ttu-id="e3988-124">Routine de nom de profil de cache</span><span class="sxs-lookup"><span data-stu-id="e3988-124">Cache Profile Name routine</span></span>

<span data-ttu-id="e3988-125">La fonction appelle la fonction  `HrCacheProfileName` **[IMAPISupport::OpenProfileSection](imapisupport-openprofilesection.md)** pour ouvrir une section de profil pour la session en cours, puis définit le profil des personnes qui gèrent les boutons.</span><span class="sxs-lookup"><span data-stu-id="e3988-125">The  `HrCacheProfileName` function calls the **[IMAPISupport::OpenProfileSection](imapisupport-openprofilesection.md)** function to open a profile section for the current session, and then sets the profile for the button handlers.</span></span> 
  
### <a name="cmyaddinhrcacheprofilename-example"></a><span data-ttu-id="e3988-126">Exemple CMyAddin::HrCacheProfileName()</span><span class="sxs-lookup"><span data-stu-id="e3988-126">CMyAddin::HrCacheProfileName() example</span></span>

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

## <a name="add-menu-items-routine"></a><span data-ttu-id="e3988-127">Routine Ajouter des éléments de menu</span><span class="sxs-lookup"><span data-stu-id="e3988-127">Add Menu Items routine</span></span>

<span data-ttu-id="e3988-128">La fonction définit les options de menu qui apparaissent sous le menu État hors connexion qui est créé lorsque le module est chargé dans Outlook, puis appelle chaque `HrAddMenuItems` élément de  `DispEventAdvise` menu.</span><span class="sxs-lookup"><span data-stu-id="e3988-128">The  `HrAddMenuItems` function defines the menu options that appear under the **Offline State** menu that is created when the add-in is loaded in Outlook, and then calls  `DispEventAdvise` for each menu item.</span></span> 
  
### <a name="cmyaddinhraddmenuitems-example"></a><span data-ttu-id="e3988-129">Exemple CMyAddin::HrAddMenuItems()</span><span class="sxs-lookup"><span data-stu-id="e3988-129">CMyAddin::HrAddMenuItems() example</span></span>

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

## <a name="see-also"></a><span data-ttu-id="e3988-130">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="e3988-130">See also</span></span>

- [<span data-ttu-id="e3988-131">À propos de l’API d’état hors connexion</span><span class="sxs-lookup"><span data-stu-id="e3988-131">About the Offline State API</span></span>](about-the-offline-state-api.md) 
- [<span data-ttu-id="e3988-132">Installation de l’exemple de complément d’état hors connexion</span><span class="sxs-lookup"><span data-stu-id="e3988-132">Installing the Sample Offline State Add-in</span></span>](installing-the-sample-offline-state-add-in.md)
- [<span data-ttu-id="e3988-133">À propos de l’exemple de complément d’état hors connexion</span><span class="sxs-lookup"><span data-stu-id="e3988-133">About the Sample Offline State Add-in</span></span>](about-the-sample-offline-state-add-in.md)
- [<span data-ttu-id="e3988-134">Surveillance des modifications de l’état de connexion à l’aide d’un complément d’état hors connexion</span><span class="sxs-lookup"><span data-stu-id="e3988-134">Monitoring Connection State Changes Using an Offline State Add-in</span></span>](monitoring-connection-state-changes-using-an-offline-state-add-in.md)
- [<span data-ttu-id="e3988-135">Déconnexion d’un add-in d’état hors connexion</span><span class="sxs-lookup"><span data-stu-id="e3988-135">Disconnecting an Offline State Add-in</span></span>](disconnecting-an-offline-state-add-in.md)

