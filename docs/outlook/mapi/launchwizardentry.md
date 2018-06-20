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
ms.openlocfilehash: d80671331c2760c574ab32d79115a352ee4bcf25
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19784534"
---
# <a name="launchwizardentry"></a><span data-ttu-id="4e095-103">LAUNCHWIZARDENTRY</span><span class="sxs-lookup"><span data-stu-id="4e095-103">LAUNCHWIZARDENTRY</span></span>

  
  
<span data-ttu-id="4e095-104">**S’applique à**: Outlook</span><span class="sxs-lookup"><span data-stu-id="4e095-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="4e095-105">Définit une fonction qui démarre l’application Assistant profil en vue d’ajouter un ou plusieurs services de messagerie à un profil.</span><span class="sxs-lookup"><span data-stu-id="4e095-105">Defines a function that starts the Profile Wizard application for the purpose of adding one or more message services to a profile.</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="4e095-106">Fichier d’en-tête :</span><span class="sxs-lookup"><span data-stu-id="4e095-106">Header file:</span></span>  <br/> |<span data-ttu-id="4e095-107">Mapiwz.h</span><span class="sxs-lookup"><span data-stu-id="4e095-107">Mapiwz.h</span></span>  <br/> |
|<span data-ttu-id="4e095-108">Fonction implémentée par :</span><span class="sxs-lookup"><span data-stu-id="4e095-108">Defined function implemented by:</span></span>  <br/> |<span data-ttu-id="4e095-109">MAPI</span><span class="sxs-lookup"><span data-stu-id="4e095-109">MAPI</span></span>  <br/> |
|<span data-ttu-id="4e095-110">Fonction appelée par :</span><span class="sxs-lookup"><span data-stu-id="4e095-110">Defined function called by:</span></span>  <br/> |<span data-ttu-id="4e095-111">Applications clientes</span><span class="sxs-lookup"><span data-stu-id="4e095-111">Client applications</span></span>  <br/> |
   
```cpp
HRESULT LAUNCHWIZARDENTRY(
  HWND hParentWnd,
  ULONG ulFlags,
  LPCSTR FAR * lppszServiceNameToAdd,
  ULONG cbBufferMax,
  LPSTR lpszNewProfileName
);
```

## <a name="parameters"></a><span data-ttu-id="4e095-112">Paramètres</span><span class="sxs-lookup"><span data-stu-id="4e095-112">Parameters</span></span>

 <span data-ttu-id="4e095-113">_hParentWnd_</span><span class="sxs-lookup"><span data-stu-id="4e095-113">_hParentWnd_</span></span>
  
> <span data-ttu-id="4e095-114">[in] Handle de fenêtre parent de l’appelant.</span><span class="sxs-lookup"><span data-stu-id="4e095-114">[in] A handle to the caller's parent window.</span></span> <span data-ttu-id="4e095-115">Si l’appelant ne dispose pas d’une fenêtre parent, le paramètre _hParentWnd_ doit être NULL.</span><span class="sxs-lookup"><span data-stu-id="4e095-115">If the caller does not have a parent window, the  _hParentWnd_ parameter should be NULL.</span></span> 
    
 <span data-ttu-id="4e095-116">_ulFlags_</span><span class="sxs-lookup"><span data-stu-id="4e095-116">_ulFlags_</span></span>
  
> <span data-ttu-id="4e095-117">[in] Masque de bits d’indicateurs indiquant les options de l’Assistant profil.</span><span class="sxs-lookup"><span data-stu-id="4e095-117">[in] Bitmask of flags indicating options for the Profile Wizard.</span></span> <span data-ttu-id="4e095-118">Les indicateurs suivants peuvent être définis :</span><span class="sxs-lookup"><span data-stu-id="4e095-118">The following flags can be set:</span></span>
    
<span data-ttu-id="4e095-119">MAPI_PW_ADD_SERVICE_ONLY</span><span class="sxs-lookup"><span data-stu-id="4e095-119">MAPI_PW_ADD_SERVICE_ONLY</span></span> 
  
> <span data-ttu-id="4e095-120">L’Assistant profil consiste à ajouter uniquement les services de message répertoriés via le paramètre _lppszServiceNameToAdd_ et n’affiche pas la page de sélection de services de messagerie.</span><span class="sxs-lookup"><span data-stu-id="4e095-120">The Profile Wizard is to add only the message services listed through the  _lppszServiceNameToAdd_ parameter, and not display its page for selecting message services.</span></span> 
    
<span data-ttu-id="4e095-121">MAPI_PW_FIRST_PROFILE</span><span class="sxs-lookup"><span data-stu-id="4e095-121">MAPI_PW_FIRST_PROFILE</span></span> 
  
> <span data-ttu-id="4e095-122">Le profil doit être créé est la première pour cette station de travail.</span><span class="sxs-lookup"><span data-stu-id="4e095-122">The profile to be created is the first one for this workstation.</span></span> 
    
<span data-ttu-id="4e095-123">MAPI_PW_HIDE_SERVICES_LIST</span><span class="sxs-lookup"><span data-stu-id="4e095-123">MAPI_PW_HIDE_SERVICES_LIST</span></span> 
  
> <span data-ttu-id="4e095-124">Page de l’Assistant profil de sélection de services de messagerie ne doit pas être affichée.</span><span class="sxs-lookup"><span data-stu-id="4e095-124">The Profile Wizard's page for selecting message services should not be displayed.</span></span> 
    
<span data-ttu-id="4e095-125">MAPI_PW_LAUNCHED_BY_CONFIG</span><span class="sxs-lookup"><span data-stu-id="4e095-125">MAPI_PW_LAUNCHED_BY_CONFIG</span></span> 
  
> <span data-ttu-id="4e095-126">L’Assistant profil a été lancé par l’application de panneau de configuration.</span><span class="sxs-lookup"><span data-stu-id="4e095-126">The Profile Wizard was launched by the Control Panel configuration application.</span></span> 
    
<span data-ttu-id="4e095-127">MAPI_PW_PROVIDER_UI_ONLY</span><span class="sxs-lookup"><span data-stu-id="4e095-127">MAPI_PW_PROVIDER_UI_ONLY</span></span> 
  
> <span data-ttu-id="4e095-128">Seules les boîtes de dialogue de configuration des fournisseurs de services doivent être affichés et pages de l’Assistant profil ne doivent pas apparaître.</span><span class="sxs-lookup"><span data-stu-id="4e095-128">Only the service providers's configuration dialog boxes should be displayed and the Profile Wizard's pages should not appear.</span></span> <span data-ttu-id="4e095-129">Cet indicateur peut être défini uniquement si l’indicateur MAPI_PW_ADD_SERVICE_ONLY est défini.</span><span class="sxs-lookup"><span data-stu-id="4e095-129">This flag can only be set if the MAPI_PW_ADD_SERVICE_ONLY flag is set.</span></span> 
    
 <span data-ttu-id="4e095-130">_lppszServiceNameToAdd_</span><span class="sxs-lookup"><span data-stu-id="4e095-130">_lppszServiceNameToAdd_</span></span>
  
> <span data-ttu-id="4e095-131">[in] Pointeur vers un tableau de chaînes contenant les noms des services de message à ajouter au profil.</span><span class="sxs-lookup"><span data-stu-id="4e095-131">[in] Pointer to an array of strings that contains the names of the message services to be added to the profile.</span></span> <span data-ttu-id="4e095-132">Le tableau doit se terminer par une valeur NULL.</span><span class="sxs-lookup"><span data-stu-id="4e095-132">The array must terminate with a NULL value.</span></span> 
    
 <span data-ttu-id="4e095-133">_cbBufferMax_</span><span class="sxs-lookup"><span data-stu-id="4e095-133">_cbBufferMax_</span></span>
  
> <span data-ttu-id="4e095-134">[in] Taille de la mémoire tampon vers laquelle pointe le paramètre _lpszNewProfileName_ .</span><span class="sxs-lookup"><span data-stu-id="4e095-134">[in] Size of the buffer pointed to by the  _lpszNewProfileName_ parameter.</span></span> 
    
 <span data-ttu-id="4e095-135">_lpszNewProfileName_</span><span class="sxs-lookup"><span data-stu-id="4e095-135">_lpszNewProfileName_</span></span>
  
> <span data-ttu-id="4e095-136">[out] Pointeur vers un tampon de chaîne dans laquelle la fonction **LAUNCHWIZARDENTRY** renvoie le nom du profil créé.</span><span class="sxs-lookup"><span data-stu-id="4e095-136">[out] Pointer to a string buffer where the function based on **LAUNCHWIZARDENTRY** returns the name of the created profile.</span></span> 
    
## <a name="return-value"></a><span data-ttu-id="4e095-137">Valeur renvoy�e</span><span class="sxs-lookup"><span data-stu-id="4e095-137">Return value</span></span>

<span data-ttu-id="4e095-138">S_OK</span><span class="sxs-lookup"><span data-stu-id="4e095-138">S_OK</span></span> 
  
> <span data-ttu-id="4e095-139">L'appel a r�ussi et a renvoy� la valeur attendue ou les valeurs.</span><span class="sxs-lookup"><span data-stu-id="4e095-139">The call succeeded and has returned the expected value or values.</span></span> 
    
<span data-ttu-id="4e095-140">MAPI_E_CALL_FAILED</span><span class="sxs-lookup"><span data-stu-id="4e095-140">MAPI_E_CALL_FAILED</span></span> 
  
> <span data-ttu-id="4e095-141">Une erreur d’origine inattendu ou inconnu a empêché l’opération de se terminer.</span><span class="sxs-lookup"><span data-stu-id="4e095-141">An error of unexpected or unknown origin prevented the operation from completing.</span></span> <span data-ttu-id="4e095-142">Impossibilité d’accéder au profil par défaut et une erreur possibilités : échec d’initialisation du sous-système MAPI pour l’Assistant profil, renvoyer à partir de la boîte de dialogue.</span><span class="sxs-lookup"><span data-stu-id="4e095-142">Possibilities include failure to initialize the MAPI subsystem for the Profile Wizard, inability to access the default profile, and an error return from the dialog box.</span></span>
    
## <a name="remarks"></a><span data-ttu-id="4e095-143">Remarques</span><span class="sxs-lookup"><span data-stu-id="4e095-143">Remarks</span></span>

<span data-ttu-id="4e095-144">L’implémentation MAPI du prototype de la fonction **LAUNCHWIZARDENTRY** est le point d’entrée dans l’application Assistant profil MAPI.</span><span class="sxs-lookup"><span data-stu-id="4e095-144">The MAPI implementation of the **LAUNCHWIZARDENTRY** function prototype is the entry point into the MAPI Profile Wizard application.</span></span> <span data-ttu-id="4e095-145">Ce point d’entrée **LaunchWizard**les noms MAPI.</span><span class="sxs-lookup"><span data-stu-id="4e095-145">MAPI names this entry point **LaunchWizard**.</span></span> 
  
<span data-ttu-id="4e095-146">Lorsque l’indicateur MAPI_PW_ADD_SERVICE_ONLY est défini dans le paramètre _ulFlags_ , les règles suivantes s’appliquent :</span><span class="sxs-lookup"><span data-stu-id="4e095-146">When the MAPI_PW_ADD_SERVICE_ONLY flag is set in the  _ulFlags_ parameter, the following rules apply:</span></span> 
  
- <span data-ttu-id="4e095-147">L’indicateur MAPI_PW_LAUNCHED_BY_CONFIG empêche la page d’accueil de s’afficher.</span><span class="sxs-lookup"><span data-stu-id="4e095-147">The MAPI_PW_LAUNCHED_BY_CONFIG flag inhibits the welcome page from being displayed.</span></span> 
    
- <span data-ttu-id="4e095-148">Les indicateurs MAPI_PW_HIDE_SERVICES_LIST et MAPI_PW_PROVIDER_UI_ONLY sont utiles uniquement lorsqu’il n’existe aucun profil par défaut.</span><span class="sxs-lookup"><span data-stu-id="4e095-148">The MAPI_PW_HIDE_SERVICES_LIST and MAPI_PW_PROVIDER_UI_ONLY flags are useful only when there is no default profile.</span></span> <span data-ttu-id="4e095-149">Dans ce cas, ces indicateurs déterminent quel Assistant profil page doit s’afficher.</span><span class="sxs-lookup"><span data-stu-id="4e095-149">In this case these flags determine which Profile Wizard page is to be displayed.</span></span> 
    
- <span data-ttu-id="4e095-150">Si un profil par défaut existe, aucune des pages de l’Assistant profil doivent être affichées.</span><span class="sxs-lookup"><span data-stu-id="4e095-150">If a default profile exists, none of the Profile Wizard pages are to be displayed.</span></span> 
    
- <span data-ttu-id="4e095-151">Si un profil par défaut existe, service qu’un message est répertorié par le biais du paramètre _lppszServiceNameToAdd_ , et que le service de message est déjà dans le profil par défaut, l’Assistant profil renvoie S_OK sans rien ajouter au profil.</span><span class="sxs-lookup"><span data-stu-id="4e095-151">If a default profile exists, only one message service is listed through the  _lppszServiceNameToAdd_ parameter, and that message service is already in the default profile, the Profile Wizard returns S_OK without adding anything to the profile.</span></span> 
    
<span data-ttu-id="4e095-152">Pour chaque service de message à ajouter au profil, l’Assistant profil appelle la fonction de point d’entrée du service basée sur le prototype [MSGSERVICEENTRY](msgserviceentry.md) .</span><span class="sxs-lookup"><span data-stu-id="4e095-152">For every message service to be added to the profile, the Profile Wizard calls the service's entry point function based on the [MSGSERVICEENTRY](msgserviceentry.md) prototype.</span></span> <span data-ttu-id="4e095-153">Pour chaque fournisseur de services sélectionné à partir d’un service de message à ajouter au profil, l’Assistant profil appelle la fonction de point d’entrée du fournisseur basée sur le prototype [WIZARDENTRY](wizardentry.md) .</span><span class="sxs-lookup"><span data-stu-id="4e095-153">For each service provider selected from a message service to be added to the profile, the Profile Wizard calls the provider's entry point function based on the [WIZARDENTRY](wizardentry.md) prototype.</span></span> <span data-ttu-id="4e095-154">Lors de la configuration interactive, tous les événements dans les pages de propriétés utilisateur, l’Assistant de profil appeler la fonction de rappel du fournisseur basée sur le prototype [SERVICEWIZARDDLGPROC](servicewizarddlgproc.md) .</span><span class="sxs-lookup"><span data-stu-id="4e095-154">During interactive configuration, every user event in the property pages causes the Profile Wizard to call the provider's callback function based on the [SERVICEWIZARDDLGPROC](servicewizarddlgproc.md) prototype.</span></span> 
  
<span data-ttu-id="4e095-155">Si un fournisseur de services en cours d’ajout au profil prend en charge les pages de l’Assistant profil, il doit autoriser la configuration par programme du profil.</span><span class="sxs-lookup"><span data-stu-id="4e095-155">If a service provider being added to the profile supports the Profile Wizard pages, it must allow programmatic configuration of the profile.</span></span>
  

