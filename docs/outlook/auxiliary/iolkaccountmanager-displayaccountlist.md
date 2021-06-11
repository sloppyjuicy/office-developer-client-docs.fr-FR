---
title: IOlkAccountManagerDisplayAccountList
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: a637dcab-81e0-4195-a1d5-61d9957fcf10
description: Affiche la boîte de dialogue Paramètres compte ou Ajouter un nouveau compte.
ms.openlocfilehash: ecf5242fa4f224516e12e667ab66fd0adfe4a25d
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/28/2019
ms.locfileid: "33415032"
---
# <a name="iolkaccountmanagerdisplayaccountlist"></a><span data-ttu-id="e8321-103">IOlkAccountManager::DisplayAccountList</span><span class="sxs-lookup"><span data-stu-id="e8321-103">IOlkAccountManager::DisplayAccountList</span></span>

<span data-ttu-id="e8321-104">Affiche la boîte de **dialogue Paramètres** compte ou Ajouter **un** nouveau compte.</span><span class="sxs-lookup"><span data-stu-id="e8321-104">Displays either the **Account Settings** or **Add New Account** dialog box.</span></span> 
  
## <a name="quick-info"></a><span data-ttu-id="e8321-105">Informations rapides</span><span class="sxs-lookup"><span data-stu-id="e8321-105">Quick info</span></span>

<span data-ttu-id="e8321-106">See [IOlkAccountManager](iolkaccountmanager.md).</span><span class="sxs-lookup"><span data-stu-id="e8321-106">See [IOlkAccountManager](iolkaccountmanager.md).</span></span>
  
```cpp
HRESULT IOlkAccountManager::DisplayAccountList ( 
    HWND hwnd,
    DWORD dwFlags,
    LPCWSTR wszTitle,
    DWORD cCategories,
    const CLSID * rgclsidCategories,
    const CLSID * pclsidType
);

```

## <a name="parameters"></a><span data-ttu-id="e8321-107">Parameters</span><span class="sxs-lookup"><span data-stu-id="e8321-107">Parameters</span></span>

<span data-ttu-id="e8321-108">_hwnd_</span><span class="sxs-lookup"><span data-stu-id="e8321-108">_hwnd_</span></span>
  
> <span data-ttu-id="e8321-109">[in] Poignée de la fenêtre dans laquelle la boîte de dialogue affichée est modale.</span><span class="sxs-lookup"><span data-stu-id="e8321-109">[in] The handle to the window to which the displayed dialog box is modal.</span></span> <span data-ttu-id="e8321-110">Peut être zéro.</span><span class="sxs-lookup"><span data-stu-id="e8321-110">May be zero.</span></span>
    
<span data-ttu-id="e8321-111">_dwFlags_</span><span class="sxs-lookup"><span data-stu-id="e8321-111">_dwFlags_</span></span>
  
> <span data-ttu-id="e8321-112">[in] Indicateurs pour modifier le comportement de l’affichage.</span><span class="sxs-lookup"><span data-stu-id="e8321-112">[in] Flags to modify the behavior of the display.</span></span> 
    
   - <span data-ttu-id="e8321-113">**ACCTUI_NO_WARNING**: n’affichez pas l’avertissement signalant que les modifications ne prennent effet qu’une fois Outlook redémarrage.</span><span class="sxs-lookup"><span data-stu-id="e8321-113">**ACCTUI_NO_WARNING**—Do not display the warning that changes will not take effect until Outlook is restarted.</span></span> <span data-ttu-id="e8321-114">S’applique uniquement si l’application est en cours d’exécution in-process avec Outlook.exe.</span><span class="sxs-lookup"><span data-stu-id="e8321-114">Applies only if the application is running in-process with Outlook.exe.</span></span>
    
   - <span data-ttu-id="e8321-115">**ACCTUI_SHOW_DATA_TAB**:afficher la boîte de **dialogue Paramètres** compte avec **l’onglet** Données sélectionné.</span><span class="sxs-lookup"><span data-stu-id="e8321-115">**ACCTUI_SHOW_DATA_TAB**—Show the **Account Settings** dialog box with the **Data** tab selected.</span></span> <span data-ttu-id="e8321-116">Valide uniquement si **ACCTUI_SHOW_ACCTWIZARD** n’est pas définie.</span><span class="sxs-lookup"><span data-stu-id="e8321-116">Valid only if **ACCTUI_SHOW_ACCTWIZARD** is not set.</span></span> 
    
   - <span data-ttu-id="e8321-117">**ACCTUI_SHOW_ACCTWIZARD**: affiche la boîte de dialogue Ajouter **un nouveau** compte.</span><span class="sxs-lookup"><span data-stu-id="e8321-117">**ACCTUI_SHOW_ACCTWIZARD**—Display the **Add New Account** dialog box.</span></span> 
    
<span data-ttu-id="e8321-118">_wszTitle_</span><span class="sxs-lookup"><span data-stu-id="e8321-118">_wszTitle_</span></span>
  
> <span data-ttu-id="e8321-119">[in] Ce paramètre n’est pas utilisé et doit être NULL.</span><span class="sxs-lookup"><span data-stu-id="e8321-119">[in] This parameter is not used and should be NULL.</span></span>
    
<span data-ttu-id="e8321-120">_cCategories_</span><span class="sxs-lookup"><span data-stu-id="e8321-120">_cCategories_</span></span>
  
> <span data-ttu-id="e8321-121">[in] Ce paramètre n’est pas utilisé et doit être NULL.</span><span class="sxs-lookup"><span data-stu-id="e8321-121">[in] This parameter is not used and must be NULL.</span></span> 
    
<span data-ttu-id="e8321-122">_rgclsidCategories_</span><span class="sxs-lookup"><span data-stu-id="e8321-122">_rgclsidCategories_</span></span>
  
> <span data-ttu-id="e8321-123">[in] Ce paramètre n’est pas utilisé et doit être NULL.</span><span class="sxs-lookup"><span data-stu-id="e8321-123">[in] This parameter is not used and must be NULL.</span></span>
    
<span data-ttu-id="e8321-124">_pclsidType_</span><span class="sxs-lookup"><span data-stu-id="e8321-124">_pclsidType_</span></span>
  
> <span data-ttu-id="e8321-125">[in] Ce paramètre n’est pas utilisé et doit être NULL.</span><span class="sxs-lookup"><span data-stu-id="e8321-125">[in] This parameter is not used and must be NULL.</span></span>
    
## <a name="return-values"></a><span data-ttu-id="e8321-126">Valeurs de retour</span><span class="sxs-lookup"><span data-stu-id="e8321-126">Return values</span></span>

|<span data-ttu-id="e8321-127">**[HRESULT]**</span><span class="sxs-lookup"><span data-stu-id="e8321-127">**HRESULT**</span></span>|<span data-ttu-id="e8321-128">**Description**</span><span class="sxs-lookup"><span data-stu-id="e8321-128">**Description**</span></span>|
|:-----|:-----|
|<span data-ttu-id="e8321-129">S_OK</span><span class="sxs-lookup"><span data-stu-id="e8321-129">S_OK</span></span>  <br/> |<span data-ttu-id="e8321-130">L’appel a réussi.</span><span class="sxs-lookup"><span data-stu-id="e8321-130">The call was successful.</span></span>  <br/> |
|<span data-ttu-id="e8321-131">E_ACCT_UI_BUSY</span><span class="sxs-lookup"><span data-stu-id="e8321-131">E_ACCT_UI_BUSY</span></span>  <br/> |<span data-ttu-id="e8321-132">La boîte de dialogue n’a pas pu être créée.</span><span class="sxs-lookup"><span data-stu-id="e8321-132">The dialog box could not be created.</span></span>  <br/> |
|<span data-ttu-id="e8321-133">E_OLK_NOT_INITIALIZED</span><span class="sxs-lookup"><span data-stu-id="e8321-133">E_OLK_NOT_INITIALIZED</span></span>  <br/> |<span data-ttu-id="e8321-134">Le Gestionnaire de comptes n'a pas été initialisé pour une utilisation.</span><span class="sxs-lookup"><span data-stu-id="e8321-134">The account manager has not been initialized for use.</span></span>  <br/> |
|<span data-ttu-id="e8321-135">MAPI_E_CALL_FAILED</span><span class="sxs-lookup"><span data-stu-id="e8321-135">MAPI_E_CALL_FAILED</span></span>  <br/> |<span data-ttu-id="e8321-136">La **boîte de dialogue Ajouter un nouveau compte** a renvoyé une erreur.</span><span class="sxs-lookup"><span data-stu-id="e8321-136">The **Add New Account** dialog box returned an error.</span></span>  <br/> |
|<span data-ttu-id="e8321-137">MAPI_E_INVALID_PARAMETER</span><span class="sxs-lookup"><span data-stu-id="e8321-137">MAPI_E_INVALID_PARAMETER</span></span>  <br/> |<span data-ttu-id="e8321-138">Le  _paramètre cCategories_,  _rgclsidCategories_ ou  _pclsidType_ est non NULL.</span><span class="sxs-lookup"><span data-stu-id="e8321-138">The  _cCategories_,  _rgclsidCategories_, or  _pclsidType_ parameter is non-NULL.</span></span>  <br/> |
|<span data-ttu-id="e8321-139">MAPI_E_USER_CANCEL</span><span class="sxs-lookup"><span data-stu-id="e8321-139">MAPI_E_USER_CANCEL</span></span>  <br/> |<span data-ttu-id="e8321-140">La **boîte de dialogue Paramètres** compte a renvoyé une erreur.</span><span class="sxs-lookup"><span data-stu-id="e8321-140">The **Account Settings** dialog box returned an error.</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="e8321-141">Remarques</span><span class="sxs-lookup"><span data-stu-id="e8321-141">Remarks</span></span>

<span data-ttu-id="e8321-142">Les  _paramètres cCategories,_  _rgclsidCategories_ et  _pclsidType_ ne sont pas utilisés pour le moment et doivent être NULL.</span><span class="sxs-lookup"><span data-stu-id="e8321-142">The  _cCategories_,  _rgclsidCategories_, and  _pclsidType_ parameters are not used at this time and must be NULL.</span></span>  <span data-ttu-id="e8321-143">_wszTitle n’est_ pas utilisé et doit également être NULL.</span><span class="sxs-lookup"><span data-stu-id="e8321-143">_wszTitle_ is not used and should also be NULL.</span></span> 
  

