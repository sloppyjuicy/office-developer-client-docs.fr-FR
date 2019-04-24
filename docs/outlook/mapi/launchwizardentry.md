---
title: LAUNCHWIZARDENTRY
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- MAPI.LAUNCHWIZARDENTRY
api_type:
- COM
ms.assetid: 5778dffa-f01b-46b3-9c19-862793740918
description: 'Derni�re modification�: lundi 9 mars 2015'
ms.openlocfilehash: c1509918eb587c17deebf95317cf57b4ab19928a
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32270188"
---
# <a name="launchwizardentry"></a><span data-ttu-id="68025-103">LAUNCHWIZARDENTRY</span><span class="sxs-lookup"><span data-stu-id="68025-103">LAUNCHWIZARDENTRY</span></span>

  
  
<span data-ttu-id="68025-104">**S’applique à** : Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="68025-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="68025-105">Définit une fonction qui démarre l'application Assistant Profil pour l'ajout d'un ou plusieurs services de messagerie à un profil.</span><span class="sxs-lookup"><span data-stu-id="68025-105">Defines a function that starts the Profile Wizard application for the purpose of adding one or more message services to a profile.</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="68025-106">Fichier d’en-tête :</span><span class="sxs-lookup"><span data-stu-id="68025-106">Header file:</span></span>  <br/> |<span data-ttu-id="68025-107">Mapiwz. h</span><span class="sxs-lookup"><span data-stu-id="68025-107">Mapiwz.h</span></span>  <br/> |
|<span data-ttu-id="68025-108">Fonction définie implémentée par:</span><span class="sxs-lookup"><span data-stu-id="68025-108">Defined function implemented by:</span></span>  <br/> |<span data-ttu-id="68025-109">MAPI</span><span class="sxs-lookup"><span data-stu-id="68025-109">MAPI</span></span>  <br/> |
|<span data-ttu-id="68025-110">Fonction définie appelée par:</span><span class="sxs-lookup"><span data-stu-id="68025-110">Defined function called by:</span></span>  <br/> |<span data-ttu-id="68025-111">Applications clientes</span><span class="sxs-lookup"><span data-stu-id="68025-111">Client applications</span></span>  <br/> |
   
```cpp
HRESULT LAUNCHWIZARDENTRY(
  HWND hParentWnd,
  ULONG ulFlags,
  LPCSTR FAR * lppszServiceNameToAdd,
  ULONG cbBufferMax,
  LPSTR lpszNewProfileName
);
```

## <a name="parameters"></a><span data-ttu-id="68025-112">Paramètres</span><span class="sxs-lookup"><span data-stu-id="68025-112">Parameters</span></span>

 <span data-ttu-id="68025-113">_hParentWnd_</span><span class="sxs-lookup"><span data-stu-id="68025-113">_hParentWnd_</span></span>
  
> <span data-ttu-id="68025-114">dans Handle de la fenêtre parente de l'appelant.</span><span class="sxs-lookup"><span data-stu-id="68025-114">[in] A handle to the caller's parent window.</span></span> <span data-ttu-id="68025-115">Si l'appelant n'a pas de fenêtre parente, le paramètre _hParentWnd_ doit être null.</span><span class="sxs-lookup"><span data-stu-id="68025-115">If the caller does not have a parent window, the  _hParentWnd_ parameter should be NULL.</span></span> 
    
 <span data-ttu-id="68025-116">_ulFlags_</span><span class="sxs-lookup"><span data-stu-id="68025-116">_ulFlags_</span></span>
  
> <span data-ttu-id="68025-117">dans Masque de réindicateur des indicateurs indiquant les options de l'Assistant Profil.</span><span class="sxs-lookup"><span data-stu-id="68025-117">[in] Bitmask of flags indicating options for the Profile Wizard.</span></span> <span data-ttu-id="68025-118">Les indicateurs suivants peuvent être définis:</span><span class="sxs-lookup"><span data-stu-id="68025-118">The following flags can be set:</span></span>
    
<span data-ttu-id="68025-119">MAPI_PW_ADD_SERVICE_ONLY</span><span class="sxs-lookup"><span data-stu-id="68025-119">MAPI_PW_ADD_SERVICE_ONLY</span></span> 
  
> <span data-ttu-id="68025-120">L'Assistant Profil est d'ajouter uniquement les services de messagerie à l'aide du paramètre _lppszServiceNameToAdd_ et de ne pas afficher sa page de sélection des services de messagerie.</span><span class="sxs-lookup"><span data-stu-id="68025-120">The Profile Wizard is to add only the message services listed through the  _lppszServiceNameToAdd_ parameter, and not display its page for selecting message services.</span></span> 
    
<span data-ttu-id="68025-121">MAPI_PW_FIRST_PROFILE</span><span class="sxs-lookup"><span data-stu-id="68025-121">MAPI_PW_FIRST_PROFILE</span></span> 
  
> <span data-ttu-id="68025-122">Le profil à créer est le premier de cette station de travail.</span><span class="sxs-lookup"><span data-stu-id="68025-122">The profile to be created is the first one for this workstation.</span></span> 
    
<span data-ttu-id="68025-123">MAPI_PW_HIDE_SERVICES_LIST</span><span class="sxs-lookup"><span data-stu-id="68025-123">MAPI_PW_HIDE_SERVICES_LIST</span></span> 
  
> <span data-ttu-id="68025-124">La page de l'Assistant Profil pour la sélection des services de message ne doit pas être affichée.</span><span class="sxs-lookup"><span data-stu-id="68025-124">The Profile Wizard's page for selecting message services should not be displayed.</span></span> 
    
<span data-ttu-id="68025-125">MAPI_PW_LAUNCHED_BY_CONFIG</span><span class="sxs-lookup"><span data-stu-id="68025-125">MAPI_PW_LAUNCHED_BY_CONFIG</span></span> 
  
> <span data-ttu-id="68025-126">L'Assistant Profil a été lancé par l'application de configuration du panneau de configuration.</span><span class="sxs-lookup"><span data-stu-id="68025-126">The Profile Wizard was launched by the Control Panel configuration application.</span></span> 
    
<span data-ttu-id="68025-127">MAPI_PW_PROVIDER_UI_ONLY</span><span class="sxs-lookup"><span data-stu-id="68025-127">MAPI_PW_PROVIDER_UI_ONLY</span></span> 
  
> <span data-ttu-id="68025-128">Seuls les boîtes de dialogue de configuration des fournisseurs de services doivent s'afficher et les pages de l'Assistant Profil ne doivent pas apparaître.</span><span class="sxs-lookup"><span data-stu-id="68025-128">Only the service providers's configuration dialog boxes should be displayed and the Profile Wizard's pages should not appear.</span></span> <span data-ttu-id="68025-129">Cet indicateur ne peut être défini que si l'indicateur MAPI_PW_ADD_SERVICE_ONLY est défini.</span><span class="sxs-lookup"><span data-stu-id="68025-129">This flag can only be set if the MAPI_PW_ADD_SERVICE_ONLY flag is set.</span></span> 
    
 <span data-ttu-id="68025-130">_lppszServiceNameToAdd_</span><span class="sxs-lookup"><span data-stu-id="68025-130">_lppszServiceNameToAdd_</span></span>
  
> <span data-ttu-id="68025-131">dans Pointeur vers un tableau de chaînes contenant les noms des services de message à ajouter au profil.</span><span class="sxs-lookup"><span data-stu-id="68025-131">[in] Pointer to an array of strings that contains the names of the message services to be added to the profile.</span></span> <span data-ttu-id="68025-132">Le tableau doit se terminer par une valeur NULL.</span><span class="sxs-lookup"><span data-stu-id="68025-132">The array must terminate with a NULL value.</span></span> 
    
 <span data-ttu-id="68025-133">_cbBufferMax_</span><span class="sxs-lookup"><span data-stu-id="68025-133">_cbBufferMax_</span></span>
  
> <span data-ttu-id="68025-134">dans Taille de la mémoire tampon vers laquelle pointe le paramètre _lpszNewProfileName_ .</span><span class="sxs-lookup"><span data-stu-id="68025-134">[in] Size of the buffer pointed to by the  _lpszNewProfileName_ parameter.</span></span> 
    
 <span data-ttu-id="68025-135">_lpszNewProfileName_</span><span class="sxs-lookup"><span data-stu-id="68025-135">_lpszNewProfileName_</span></span>
  
> <span data-ttu-id="68025-136">remarquer Pointeur vers une mémoire tampon de chaîne où la fonction basée sur **LAUNCHWIZARDENTRY** renvoie le nom du profil créé.</span><span class="sxs-lookup"><span data-stu-id="68025-136">[out] Pointer to a string buffer where the function based on **LAUNCHWIZARDENTRY** returns the name of the created profile.</span></span> 
    
## <a name="return-value"></a><span data-ttu-id="68025-137">Valeur renvoyée</span><span class="sxs-lookup"><span data-stu-id="68025-137">Return value</span></span>

<span data-ttu-id="68025-138">S_OK</span><span class="sxs-lookup"><span data-stu-id="68025-138">S_OK</span></span> 
  
> <span data-ttu-id="68025-139">L'appel a r�ussi et a renvoy� la valeur attendue ou les valeurs.</span><span class="sxs-lookup"><span data-stu-id="68025-139">The call succeeded and has returned the expected value or values.</span></span> 
    
<span data-ttu-id="68025-140">MAPI_E_CALL_FAILED</span><span class="sxs-lookup"><span data-stu-id="68025-140">MAPI_E_CALL_FAILED</span></span> 
  
> <span data-ttu-id="68025-141">Une erreur d'origine inattendue ou inconnue a empêché l'opération de s'exécuter.</span><span class="sxs-lookup"><span data-stu-id="68025-141">An error of unexpected or unknown origin prevented the operation from completing.</span></span> <span data-ttu-id="68025-142">Les possibilités incluent l'échec de l'initialisation du sous-système MAPI pour l'Assistant Profil, l'impossibilité d'accéder au profil par défaut et une erreur de retour dans la boîte de dialogue.</span><span class="sxs-lookup"><span data-stu-id="68025-142">Possibilities include failure to initialize the MAPI subsystem for the Profile Wizard, inability to access the default profile, and an error return from the dialog box.</span></span>
    
## <a name="remarks"></a><span data-ttu-id="68025-143">Remarques</span><span class="sxs-lookup"><span data-stu-id="68025-143">Remarks</span></span>

<span data-ttu-id="68025-144">L'implémentation MAPI du prototype de fonction **LAUNCHWIZARDENTRY** est le point d'entrée dans l'application Assistant Profil MAPI.</span><span class="sxs-lookup"><span data-stu-id="68025-144">The MAPI implementation of the **LAUNCHWIZARDENTRY** function prototype is the entry point into the MAPI Profile Wizard application.</span></span> <span data-ttu-id="68025-145">MAPI nomme ce point d'entrée **LaunchWizard**.</span><span class="sxs-lookup"><span data-stu-id="68025-145">MAPI names this entry point **LaunchWizard**.</span></span> 
  
<span data-ttu-id="68025-146">Lorsque l'indicateur MAPI_PW_ADD_SERVICE_ONLY est défini dans le paramètre _ulFlags_ , les règles suivantes s'appliquent:</span><span class="sxs-lookup"><span data-stu-id="68025-146">When the MAPI_PW_ADD_SERVICE_ONLY flag is set in the  _ulFlags_ parameter, the following rules apply:</span></span> 
  
- <span data-ttu-id="68025-147">L'indicateur MAPI_PW_LAUNCHED_BY_CONFIG empêche l'affichage de la page d'accueil.</span><span class="sxs-lookup"><span data-stu-id="68025-147">The MAPI_PW_LAUNCHED_BY_CONFIG flag inhibits the welcome page from being displayed.</span></span> 
    
- <span data-ttu-id="68025-148">Les indicateurs MAPI_PW_HIDE_SERVICES_LIST et MAPI_PW_PROVIDER_UI_ONLY ne sont utiles que s'il n'y a pas de profil par défaut.</span><span class="sxs-lookup"><span data-stu-id="68025-148">The MAPI_PW_HIDE_SERVICES_LIST and MAPI_PW_PROVIDER_UI_ONLY flags are useful only when there is no default profile.</span></span> <span data-ttu-id="68025-149">Dans ce cas, ces indicateurs déterminent la page de l'Assistant Profil qui doit être affichée.</span><span class="sxs-lookup"><span data-stu-id="68025-149">In this case these flags determine which Profile Wizard page is to be displayed.</span></span> 
    
- <span data-ttu-id="68025-150">Si un profil par défaut existe, aucune des pages de l'Assistant Profil n'est affichée.</span><span class="sxs-lookup"><span data-stu-id="68025-150">If a default profile exists, none of the Profile Wizard pages are to be displayed.</span></span> 
    
- <span data-ttu-id="68025-151">S'il existe un profil par défaut, un seul service de messagerie est répertorié via le paramètre _lppszServiceNameToAdd_ , et ce service de messagerie se trouve déjà dans le profil par défaut, l'Assistant Profil renvoie S_OK sans rien ajouter au profil.</span><span class="sxs-lookup"><span data-stu-id="68025-151">If a default profile exists, only one message service is listed through the  _lppszServiceNameToAdd_ parameter, and that message service is already in the default profile, the Profile Wizard returns S_OK without adding anything to the profile.</span></span> 
    
<span data-ttu-id="68025-152">Pour que chaque service de messagerie soit ajouté au profil, l'Assistant Profil appelle la fonction de point d'entrée du service en fonction du prototype [MSGSERVICEENTRY](msgserviceentry.md) .</span><span class="sxs-lookup"><span data-stu-id="68025-152">For every message service to be added to the profile, the Profile Wizard calls the service's entry point function based on the [MSGSERVICEENTRY](msgserviceentry.md) prototype.</span></span> <span data-ttu-id="68025-153">Pour chaque fournisseur de services sélectionné dans un service de messagerie à ajouter au profil, l'Assistant Profil appelle la fonction de point d'entrée du fournisseur en fonction du prototype [WIZARDENTRY](wizardentry.md) .</span><span class="sxs-lookup"><span data-stu-id="68025-153">For each service provider selected from a message service to be added to the profile, the Profile Wizard calls the provider's entry point function based on the [WIZARDENTRY](wizardentry.md) prototype.</span></span> <span data-ttu-id="68025-154">Lors de la configuration interactive, chaque événement utilisateur dans les pages de propriétés fait en sorte que l'Assistant Profil appelle la fonction de rappel du fournisseur en fonction du prototype [SERVICEWIZARDDLGPROC](servicewizarddlgproc.md) .</span><span class="sxs-lookup"><span data-stu-id="68025-154">During interactive configuration, every user event in the property pages causes the Profile Wizard to call the provider's callback function based on the [SERVICEWIZARDDLGPROC](servicewizarddlgproc.md) prototype.</span></span> 
  
<span data-ttu-id="68025-155">Si un fournisseur de services ajouté au profil prend en charge les pages de l'Assistant Profil, il doit autoriser la configuration par programme du profil.</span><span class="sxs-lookup"><span data-stu-id="68025-155">If a service provider being added to the profile supports the Profile Wizard pages, it must allow programmatic configuration of the profile.</span></span>
  

