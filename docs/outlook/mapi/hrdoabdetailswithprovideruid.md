---
title: HrDoABDetailsWithProviderUID
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: 27741887-8405-49ed-b080-613613faf91b
description: Dernière modification le 9 mars 2015
ms.openlocfilehash: 47cf87fce0af3b866018bf03a34a05ea42cef82c
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/28/2019
ms.locfileid: "33426680"
---
# <a name="hrdoabdetailswithprovideruid"></a><span data-ttu-id="32c00-103">HrDoABDetailsWithProviderUID</span><span class="sxs-lookup"><span data-stu-id="32c00-103">HrDoABDetailsWithProviderUID</span></span>

  
  
<span data-ttu-id="32c00-104">**S’applique à** : Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="32c00-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="32c00-105">Garantit que la **méthode OpenEntry** est ouverte par le fournisseur de carnet d’adresses Exchange attendu.</span><span class="sxs-lookup"><span data-stu-id="32c00-105">Ensures that the **OpenEntry** method is opened by the expected Exchange address book provider.</span></span> <span data-ttu-id="32c00-106">Cette fonction fonctionne de la même manière que [IAddrBook::D etails,](iaddrbook-details.md) mais ouvre **entryID** à l’aide du carnet d’adresses Exchange identifié par _pEmsabpUID_.</span><span class="sxs-lookup"><span data-stu-id="32c00-106">This function works similarly to [IAddrBook::Details](iaddrbook-details.md) but opens **entryID** using the Exchange address book identified by  _pEmsabpUID_.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="32c00-107">Fichier d’en-tête :</span><span class="sxs-lookup"><span data-stu-id="32c00-107">Header file:</span></span>  <br/> |<span data-ttu-id="32c00-108">abhelp.h</span><span class="sxs-lookup"><span data-stu-id="32c00-108">abhelp.h</span></span>  <br/> |
|<span data-ttu-id="32c00-109">Implémenté par :</span><span class="sxs-lookup"><span data-stu-id="32c00-109">Implemented by:</span></span>  <br/> |<span data-ttu-id="32c00-110">MAPI</span><span class="sxs-lookup"><span data-stu-id="32c00-110">MAPI</span></span>  <br/> |
|<span data-ttu-id="32c00-111">Appelé par :</span><span class="sxs-lookup"><span data-stu-id="32c00-111">Called by:</span></span>  <br/> |<span data-ttu-id="32c00-112">Applications clientes et fournisseurs de services</span><span class="sxs-lookup"><span data-stu-id="32c00-112">Client applications and service providers</span></span>  <br/> |
   
```cpp
HRESULT HrDoABDetailsWithProviderUID(
  const MAPIUID   *pEmsabpUID,
  LPADRBOOK        pAddrBook,
  ULONG_PTR FAR *  lpulUIParam,
  LPFNDISMISS      lpfnDismiss,
  LPVOID           lpvDismissContext,
  ULONG            cbEntryID,
  LPENTRYID        lpEntryID,
  LPFNBUTTON       lpfButtonCallback,
  LPVOID           lpvButtonContext,
  LPSTR           lpszButtonText,
  ULONG            ulFlags
);
```

## <a name="parameters"></a><span data-ttu-id="32c00-113">Parameters</span><span class="sxs-lookup"><span data-stu-id="32c00-113">Parameters</span></span>

 <span data-ttu-id="32c00-114">_pEmsabpUID_</span><span class="sxs-lookup"><span data-stu-id="32c00-114">_pEmsabpUID_</span></span>
  
> <span data-ttu-id="32c00-115">[in] Pointeur vers _un emsabpUID_ qui identifie le fournisseur de carnet d’adresses Exchange que cette fonction doit utiliser pour afficher des détails sur l’identificateur d’entrée.</span><span class="sxs-lookup"><span data-stu-id="32c00-115">[in] A pointer to an  _emsabpUID_ that identifies the Exchange address book provider this function should use to display details on the entry identifier.</span></span> <span data-ttu-id="32c00-116">Si l’identificateur d’entrée entrante n’est pas un identificateur d’entrée de fournisseur de carnet d’adresses Exchange, ce paramètre est ignoré et l’appel de fonction agit exactement comme [IAddrBook::D etails](iaddrbook-details.md).</span><span class="sxs-lookup"><span data-stu-id="32c00-116">If the incoming entry identifier is not an Exchange address book provider entry identifier, this parameter is ignored and the function call acts exactly like [IAddrBook::Details](iaddrbook-details.md).</span></span> <span data-ttu-id="32c00-117">Si ce paramètre est NULL ou un MAPIUID zéro, cette fonction agit également exactement comme [IAddrBook::D etails](iaddrbook-details.md).</span><span class="sxs-lookup"><span data-stu-id="32c00-117">If this parameter is NULL or a zero MAPIUID, this function also acts exactly like [IAddrBook::Details](iaddrbook-details.md).</span></span>
    
 <span data-ttu-id="32c00-118">_pAddrBook_</span><span class="sxs-lookup"><span data-stu-id="32c00-118">_pAddrBook_</span></span>
  
> <span data-ttu-id="32c00-119">[in] Carnet d’adresses utilisé pour ouvrir l’identificateur d’entrée.</span><span class="sxs-lookup"><span data-stu-id="32c00-119">[in] The address book used to open the entry identifier.</span></span> <span data-ttu-id="32c00-120">Elle ne peut pas être NULL.</span><span class="sxs-lookup"><span data-stu-id="32c00-120">It cannot be NULL.</span></span>
    
 <span data-ttu-id="32c00-121">_lpulUIParam_</span><span class="sxs-lookup"><span data-stu-id="32c00-121">_lpulUIParam_</span></span>
  
> <span data-ttu-id="32c00-122">[out] Poignée vers la fenêtre parente de la boîte de dialogue.</span><span class="sxs-lookup"><span data-stu-id="32c00-122">[out] A handle to the parent window for the dialog box.</span></span>
    
 <span data-ttu-id="32c00-123">_lpfnDismiss_</span><span class="sxs-lookup"><span data-stu-id="32c00-123">_lpfnDismiss_</span></span>
  
> <span data-ttu-id="32c00-124">[in] Pointeur vers une fonction basée sur le prototype **DISMISSMODELESS** ou NULL.</span><span class="sxs-lookup"><span data-stu-id="32c00-124">[in] A pointer to a function based on the **DISMISSMODELESS** prototype, or NULL.</span></span> <span data-ttu-id="32c00-125">Ce membre s’applique uniquement à la version sans mode de la boîte de dialogue, comme indiqué par l’indicateur DIALOG_SDI en cours de mise en place.</span><span class="sxs-lookup"><span data-stu-id="32c00-125">This member applies only to the modeless version of the dialog box, as indicated by the DIALOG_SDI flag being set.</span></span> <span data-ttu-id="32c00-126">MAPI appelle la **fonction DISMISSMODELESS** lorsque l’utilisateur fait disparaître la boîte de dialogue d’adresses sans mode, informant un client qui appelle Details que la boîte de dialogue n’est plus active.</span><span class="sxs-lookup"><span data-stu-id="32c00-126">MAPI calls the **DISMISSMODELESS** function when the user dismisses the modeless address dialog box, informing a client that is calling Details that the dialog box is no longer active.</span></span> 
    
 <span data-ttu-id="32c00-127">_lpvDismissContext_</span><span class="sxs-lookup"><span data-stu-id="32c00-127">_lpvDismissContext_</span></span>
  
> <span data-ttu-id="32c00-128">[in] Pointeur vers les informations de contexte à transmettre à la **fonction DISMISSMODELESS** pointée par le paramètre _lpfnDismiss._</span><span class="sxs-lookup"><span data-stu-id="32c00-128">[in] A pointer to context information to pass to the **DISMISSMODELESS** function pointed to by the  _lpfnDismiss_ parameter.</span></span> <span data-ttu-id="32c00-129">Ce paramètre s’applique uniquement à la version sans mode de la boîte de dialogue en incluant **l’indicateur DIALOG_SDI** dans le _paramètre ulFlags._</span><span class="sxs-lookup"><span data-stu-id="32c00-129">This parameter applies only to the modeless version of the dialog box by including the **DIALOG_SDI** flag in the  _ulFlags_ parameter.</span></span> 
    
 <span data-ttu-id="32c00-130">_cbEntryID_</span><span class="sxs-lookup"><span data-stu-id="32c00-130">_cbEntryID_</span></span>
  
> <span data-ttu-id="32c00-131">[in] Nombre d’bytes de l’identificateur d’entrée spécifié par _le paramètre lpEntryID._</span><span class="sxs-lookup"><span data-stu-id="32c00-131">[in] The byte count of the entry identifier specified by the  _lpEntryID_ parameter.</span></span> 
    
 <span data-ttu-id="32c00-132">_lpEntryID_</span><span class="sxs-lookup"><span data-stu-id="32c00-132">_lpEntryID_</span></span>
  
> <span data-ttu-id="32c00-133">[in] Pointeur vers l’identificateur d’entrée qui représente l’entrée de carnet d’adresses à ouvrir.</span><span class="sxs-lookup"><span data-stu-id="32c00-133">[in] A pointer to the entry identifier that represents the address book entry to open.</span></span>
    
 <span data-ttu-id="32c00-134">_lpfButtonCallback_</span><span class="sxs-lookup"><span data-stu-id="32c00-134">_lpfButtonCallback_</span></span>
  
> <span data-ttu-id="32c00-135">[in] Pointeur vers une fonction basée sur le prototype de fonction **LPFNBUTTON.**</span><span class="sxs-lookup"><span data-stu-id="32c00-135">[in] A pointer to a function based on the **LPFNBUTTON** function prototype.</span></span> <span data-ttu-id="32c00-136">Une **fonction LPFNBUTTON** ajoute un bouton à la boîte de dialogue Détails.</span><span class="sxs-lookup"><span data-stu-id="32c00-136">An **LPFNBUTTON** function adds a button to the details dialog box.</span></span> 
    
 <span data-ttu-id="32c00-137">_lpvButtonContext_</span><span class="sxs-lookup"><span data-stu-id="32c00-137">_lpvButtonContext_</span></span>
  
> <span data-ttu-id="32c00-138">[in] Pointeur vers des données qui a été utilisé comme paramètre pour la fonction spécifiée par le _paramètre lpfButtonCallback._</span><span class="sxs-lookup"><span data-stu-id="32c00-138">[in] A pointer to data that was used as a parameter for the function specified by the  _lpfButtonCallback_ parameter.</span></span> 
    
 <span data-ttu-id="32c00-139">_lpszButtonText_</span><span class="sxs-lookup"><span data-stu-id="32c00-139">_lpszButtonText_</span></span>
  
> <span data-ttu-id="32c00-140">[in] Pointeur vers une chaîne qui contient du texte à appliquer au bouton ajouté, si ce bouton est extensible.</span><span class="sxs-lookup"><span data-stu-id="32c00-140">[in] A pointer to a string that contains text to be applied to the added button, if that button is extensible.</span></span> <span data-ttu-id="32c00-141">Le  _paramètre lpszButtonText_ doit être NULL lorsqu’un bouton extensible n’est pas nécessaire.</span><span class="sxs-lookup"><span data-stu-id="32c00-141">The  _lpszButtonText_ parameter should be NULL when an extensible button is not needed.</span></span> 
    
 <span data-ttu-id="32c00-142">_ulFlags_</span><span class="sxs-lookup"><span data-stu-id="32c00-142">_ulFlags_</span></span>
  
> <span data-ttu-id="32c00-143">[in] Masque de bits d’indicateurs qui contrôle le type du texte pour le _paramètre lpszButtonText._</span><span class="sxs-lookup"><span data-stu-id="32c00-143">[in] A bitmask of flags that controls the type of the text for the  _lpszButtonText_ parameter.</span></span> <span data-ttu-id="32c00-144">Les indicateurs suivants peuvent être définies :</span><span class="sxs-lookup"><span data-stu-id="32c00-144">The following flags can be set:</span></span> 
    
<span data-ttu-id="32c00-145">AB_TELL_DETAILS_CHANGE</span><span class="sxs-lookup"><span data-stu-id="32c00-145">AB_TELL_DETAILS_CHANGE</span></span>
  
> <span data-ttu-id="32c00-146">Indique que details renvoie TRUE si des modifications sont réellement apportées à l’adresse ; Dans le cas contraire, Details renvoie FALSE.</span><span class="sxs-lookup"><span data-stu-id="32c00-146">Indicates that Details returns TRUE if changes are actually made to the address; otherwise, Details returns FALSE.</span></span>
    
<span data-ttu-id="32c00-147">DIALOG_MODAL</span><span class="sxs-lookup"><span data-stu-id="32c00-147">DIALOG_MODAL</span></span>
  
> <span data-ttu-id="32c00-148">Affiche la version modale de la boîte de dialogue d’adresse commune.</span><span class="sxs-lookup"><span data-stu-id="32c00-148">Displays the modal version of the common address dialog box.</span></span> <span data-ttu-id="32c00-149">Cet indicateur s’exclue mutuellement avec DIALOG_SDI.</span><span class="sxs-lookup"><span data-stu-id="32c00-149">This flag is mutually exclusive with DIALOG_SDI.</span></span>
    
<span data-ttu-id="32c00-150">DIALOG_SDI</span><span class="sxs-lookup"><span data-stu-id="32c00-150">DIALOG_SDI</span></span>
  
> <span data-ttu-id="32c00-151">Affiche la version non modée de la boîte de dialogue d’adresse commune.</span><span class="sxs-lookup"><span data-stu-id="32c00-151">Displays the modeless version of the common address dialog box.</span></span> <span data-ttu-id="32c00-152">Cet indicateur s’exclue mutuellement avec DIALOG_MODAL.</span><span class="sxs-lookup"><span data-stu-id="32c00-152">This flag is mutually exclusive with DIALOG_MODAL.</span></span>
    
<span data-ttu-id="32c00-153">MAPI_UNICODE</span><span class="sxs-lookup"><span data-stu-id="32c00-153">MAPI_UNICODE</span></span>
  
> <span data-ttu-id="32c00-154">Les chaînes transmises sont au format Unicode.</span><span class="sxs-lookup"><span data-stu-id="32c00-154">The passed-in strings are in Unicode format.</span></span> <span data-ttu-id="32c00-155">Si l’MAPI_UNICODE n’est pas définie, les chaînes sont au format ANSI.</span><span class="sxs-lookup"><span data-stu-id="32c00-155">If the MAPI_UNICODE flag is not set, the strings are in ANSI format.</span></span>
    

