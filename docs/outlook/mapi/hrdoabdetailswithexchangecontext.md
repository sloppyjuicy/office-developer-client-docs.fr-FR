---
title: HrDoABDetailsWithExchangeContext
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: b4e7fed2-88e4-4e14-90b6-913a1b7e338a
description: Dernière modification le 9 mars 2015
ms.openlocfilehash: 353a663071a9f23f0d2330169d3ac7747e047c2b
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/28/2019
ms.locfileid: "33421367"
---
# <a name="hrdoabdetailswithexchangecontext"></a><span data-ttu-id="bc888-103">HrDoABDetailsWithExchangeContext</span><span class="sxs-lookup"><span data-stu-id="bc888-103">HrDoABDetailsWithExchangeContext</span></span>

  
  
<span data-ttu-id="bc888-104">**S’applique à** : Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="bc888-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="bc888-105">Garantit que la **méthode OpenEntry** est ouverte par le fournisseur de carnet d’adresses Exchange attendu.</span><span class="sxs-lookup"><span data-stu-id="bc888-105">Ensures that the **OpenEntry** method is opened by the expected Exchange address book provider.</span></span> <span data-ttu-id="bc888-106">Cette fonction fonctionne de la même manière que [IAddrBook::D etails,](iaddrbook-details.md)mais ouvre **l’entryID** à l’aide du carnet d’adresses Exchange identifié par le paramètre _pEmsmdbUID._</span><span class="sxs-lookup"><span data-stu-id="bc888-106">This function works similarly to [IAddrBook::Details](iaddrbook-details.md), but opens the **entryID** using the Exchange address book identified by the  _pEmsmdbUID_ parameter.</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="bc888-107">Fichier d’en-tête :</span><span class="sxs-lookup"><span data-stu-id="bc888-107">Header file:</span></span>  <br/> |<span data-ttu-id="bc888-108">abhelp.h</span><span class="sxs-lookup"><span data-stu-id="bc888-108">abhelp.h</span></span>  <br/> |
|<span data-ttu-id="bc888-109">Implémenté par :</span><span class="sxs-lookup"><span data-stu-id="bc888-109">Implemented by:</span></span>  <br/> |<span data-ttu-id="bc888-110">MAPI</span><span class="sxs-lookup"><span data-stu-id="bc888-110">MAPI</span></span>  <br/> |
|<span data-ttu-id="bc888-111">Appelé par :</span><span class="sxs-lookup"><span data-stu-id="bc888-111">Called by:</span></span>  <br/> |<span data-ttu-id="bc888-112">Applications clientes et fournisseurs de services</span><span class="sxs-lookup"><span data-stu-id="bc888-112">Client applications and service providers</span></span>  <br/> |
   
```cpp
HRESULT HrOpenABEntryWithExchangeContext(
  LPMAPISESSION   pmsess,
  const MAPIUID  *pEmsmdbUID,
  LPADRBOOK pAddrBook,
  ULONG_PTR FAR * lpulUIParam,
  LPFNDISMISS lpfnDismiss,
  LPVOID lpvDismissContext,
  ULONG cbEntryID,
  LPENTRYID lpEntryID,
  LPENTRYID lpEntryID,
  LPFNBUTTON lpfButtonCallback,
  LPVOID lpvButtonContext,
  LPSTR lpszButtonText,
  ULONG ulFlags,
);
```

## <a name="parameters"></a><span data-ttu-id="bc888-113">Parameters</span><span class="sxs-lookup"><span data-stu-id="bc888-113">Parameters</span></span>

 <span data-ttu-id="bc888-114">_pmsess_</span><span class="sxs-lookup"><span data-stu-id="bc888-114">_pmsess_</span></span>
  
> <span data-ttu-id="bc888-115">**L’IMAPISession** connecté.</span><span class="sxs-lookup"><span data-stu-id="bc888-115">The logged on **IMAPISession**.</span></span> <span data-ttu-id="bc888-116">Elle ne peut pas être NULL.</span><span class="sxs-lookup"><span data-stu-id="bc888-116">It cannot be NULL.</span></span>
    
 <span data-ttu-id="bc888-117">_pEmsmdbUID_</span><span class="sxs-lookup"><span data-stu-id="bc888-117">_pEmsmdbUID_</span></span>
  
> <span data-ttu-id="bc888-118">Pointeur vers **un élément emsmdbUID** qui identifie le service Exchange qui contient le fournisseur de carnet d’adresses Exchange utilisé par la fonction pour ouvrir l’identificateur d’entrée.</span><span class="sxs-lookup"><span data-stu-id="bc888-118">A pointer to an **emsmdbUID** that identifies the Exchange Service that contains the Exchange address book provider that is used by the function to open the entry identifier.</span></span> <span data-ttu-id="bc888-119">Si l’identificateur d’entrée entrante n’est pas un identificateur d’entrée de fournisseur de carnet d’adresses Exchange, ce paramètre est ignoré et la fonction se comporte comme [IAddrBook::OpenEntry](iaddrbook-openentry.md).</span><span class="sxs-lookup"><span data-stu-id="bc888-119">If the incoming entry identifier is not an Exchange address book provider entry identifier, this parameter is ignored and the function behaves like [IAddrBook::OpenEntry](iaddrbook-openentry.md).</span></span> <span data-ttu-id="bc888-120">Si ce paramètre est NULL ou un **MAPIUID** zéro, cette fonction agit également exactement comme [IAddrBook::OpenEntry](iaddrbook-openentry.md).</span><span class="sxs-lookup"><span data-stu-id="bc888-120">If this parameter is NULL or a zero **MAPIUID**, this function also acts exactly like [IAddrBook::OpenEntry](iaddrbook-openentry.md).</span></span> 
    
 <span data-ttu-id="bc888-121">_pAddrBook_</span><span class="sxs-lookup"><span data-stu-id="bc888-121">_pAddrBook_</span></span>
  
> <span data-ttu-id="bc888-122">[in] Carnet d’adresses utilisé pour ouvrir l’identificateur d’entrée.</span><span class="sxs-lookup"><span data-stu-id="bc888-122">[in] The address book used to open the entry identifier.</span></span> <span data-ttu-id="bc888-123">Elle ne peut pas être NULL.</span><span class="sxs-lookup"><span data-stu-id="bc888-123">It cannot be NULL.</span></span>
    
 <span data-ttu-id="bc888-124">_lpulUIParam_</span><span class="sxs-lookup"><span data-stu-id="bc888-124">_lpulUIParam_</span></span>
  
> <span data-ttu-id="bc888-125">[out] Poignée vers la fenêtre parente de la boîte de dialogue.</span><span class="sxs-lookup"><span data-stu-id="bc888-125">[out] A handle to the parent window for the dialog box.</span></span>
    
 <span data-ttu-id="bc888-126">_lpfnDismiss_</span><span class="sxs-lookup"><span data-stu-id="bc888-126">_lpfnDismiss_</span></span>
  
> <span data-ttu-id="bc888-127">[in] Pointeur vers une fonction basée sur le prototype **DISMISSMODELESS** ou NULL.</span><span class="sxs-lookup"><span data-stu-id="bc888-127">[in] A pointer to a function based on the **DISMISSMODELESS** prototype, or NULL.</span></span> <span data-ttu-id="bc888-128">Ce membre s’applique uniquement à la version sans mode de la boîte de dialogue, comme indiqué par l’indicateur DIALOG_SDI en cours de mise en place.</span><span class="sxs-lookup"><span data-stu-id="bc888-128">This member applies only to the modeless version of the dialog box, as indicated by the DIALOG_SDI flag being set.</span></span> <span data-ttu-id="bc888-129">MAPI appelle la **fonction DISMISSMODELESS** lorsque l’utilisateur fait disparaître la boîte de dialogue d’adresses sans mode, informant un client qui appelle Details que la boîte de dialogue n’est plus active.</span><span class="sxs-lookup"><span data-stu-id="bc888-129">MAPI calls the **DISMISSMODELESS** function when the user dismisses the modeless address dialog box, informing a client that is calling Details that the dialog box is no longer active.</span></span> 
    
 <span data-ttu-id="bc888-130">_lpvDismissContext_</span><span class="sxs-lookup"><span data-stu-id="bc888-130">_lpvDismissContext_</span></span>
  
> <span data-ttu-id="bc888-131">[in] Pointeur vers les informations de contexte à transmettre à la **fonction DISMISSMODELESS** pointée par le paramètre _lpfnDismiss._</span><span class="sxs-lookup"><span data-stu-id="bc888-131">[in] A pointer to context information to pass to the **DISMISSMODELESS** function pointed to by the  _lpfnDismiss_ parameter.</span></span> <span data-ttu-id="bc888-132">Ce paramètre s’applique uniquement à la version sans mode de la boîte de dialogue en incluant **l’indicateur DIALOG_SDI** dans le _paramètre ulFlags._</span><span class="sxs-lookup"><span data-stu-id="bc888-132">This parameter applies only to the modeless version of the dialog box by including the **DIALOG_SDI** flag in the  _ulFlags_ parameter.</span></span> 
    
 <span data-ttu-id="bc888-133">_cbEntryID_</span><span class="sxs-lookup"><span data-stu-id="bc888-133">_cbEntryID_</span></span>
  
> <span data-ttu-id="bc888-134">[in] Nombre d’bytes de l’identificateur d’entrée spécifié par _le paramètre lpEntryID._</span><span class="sxs-lookup"><span data-stu-id="bc888-134">[in] The byte count of the entry identifier specified by the  _lpEntryID_ parameter.</span></span> 
    
 <span data-ttu-id="bc888-135">_lpEntryID_</span><span class="sxs-lookup"><span data-stu-id="bc888-135">_lpEntryID_</span></span>
  
> <span data-ttu-id="bc888-136">[in] Pointeur vers l’identificateur d’entrée qui représente l’entrée de carnet d’adresses à ouvrir.</span><span class="sxs-lookup"><span data-stu-id="bc888-136">[in] A pointer to the entry identifier that represents the address book entry to open.</span></span>
    
 <span data-ttu-id="bc888-137">_lpfButtonCallback_</span><span class="sxs-lookup"><span data-stu-id="bc888-137">_lpfButtonCallback_</span></span>
  
> <span data-ttu-id="bc888-138">[in] Pointeur vers une fonction basée sur le prototype de fonction **LPFNBUTTON.**</span><span class="sxs-lookup"><span data-stu-id="bc888-138">[in] A pointer to a function based on the **LPFNBUTTON** function prototype.</span></span> <span data-ttu-id="bc888-139">Une **fonction LPFNBUTTON** ajoute un bouton à la boîte de dialogue Détails.</span><span class="sxs-lookup"><span data-stu-id="bc888-139">An **LPFNBUTTON** function adds a button to the details dialog box.</span></span> 
    
 <span data-ttu-id="bc888-140">_lpvButtonContext_</span><span class="sxs-lookup"><span data-stu-id="bc888-140">_lpvButtonContext_</span></span>
  
> <span data-ttu-id="bc888-141">[in] Pointeur vers des données qui a été utilisé comme paramètre pour la fonction spécifiée par le _paramètre lpfButtonCallback._</span><span class="sxs-lookup"><span data-stu-id="bc888-141">[in] A pointer to data that was used as a parameter for the function specified by the  _lpfButtonCallback_ parameter.</span></span> 
    
 <span data-ttu-id="bc888-142">_lpszButtonText_</span><span class="sxs-lookup"><span data-stu-id="bc888-142">_lpszButtonText_</span></span>
  
> <span data-ttu-id="bc888-143">[in] Pointeur vers une chaîne qui contient du texte à appliquer au bouton ajouté, si ce bouton est extensible.</span><span class="sxs-lookup"><span data-stu-id="bc888-143">[in] A pointer to a string that contains text to be applied to the added button, if that button is extensible.</span></span> <span data-ttu-id="bc888-144">Le  _paramètre lpszButtonText_ doit être NULL lorsqu’un bouton extensible n’est pas nécessaire.</span><span class="sxs-lookup"><span data-stu-id="bc888-144">The  _lpszButtonText_ parameter should be NULL when an extensible button is not needed.</span></span> 
    
 <span data-ttu-id="bc888-145">_ulFlags_</span><span class="sxs-lookup"><span data-stu-id="bc888-145">_ulFlags_</span></span>
  
> <span data-ttu-id="bc888-146">[in] Masque de bits d’indicateurs qui contrôle le type du texte pour le _paramètre lpszButtonText._</span><span class="sxs-lookup"><span data-stu-id="bc888-146">[in] A bitmask of flags that controls the type of the text for the  _lpszButtonText_ parameter.</span></span> <span data-ttu-id="bc888-147">Les indicateurs suivants peuvent être définies :</span><span class="sxs-lookup"><span data-stu-id="bc888-147">The following flags can be set:</span></span> 
    
<span data-ttu-id="bc888-148">AB_TELL_DETAILS_CHANGE</span><span class="sxs-lookup"><span data-stu-id="bc888-148">AB_TELL_DETAILS_CHANGE</span></span>
  
> <span data-ttu-id="bc888-149">Indique que details renvoie TRUE si des modifications sont réellement apportées à l’adresse ; Dans le cas contraire, Details renvoie FALSE.</span><span class="sxs-lookup"><span data-stu-id="bc888-149">Indicates that Details returns TRUE if changes are actually made to the address; otherwise, Details returns FALSE.</span></span>
    
<span data-ttu-id="bc888-150">DIALOG_MODAL</span><span class="sxs-lookup"><span data-stu-id="bc888-150">DIALOG_MODAL</span></span>
  
> <span data-ttu-id="bc888-151">Affiche la version modale de la boîte de dialogue d’adresse commune.</span><span class="sxs-lookup"><span data-stu-id="bc888-151">Displays the modal version of the common address dialog box.</span></span> <span data-ttu-id="bc888-152">Cet indicateur s’exclue mutuellement avec DIALOG_SDI.</span><span class="sxs-lookup"><span data-stu-id="bc888-152">This flag is mutually exclusive with DIALOG_SDI.</span></span>
    
<span data-ttu-id="bc888-153">DIALOG_SDI</span><span class="sxs-lookup"><span data-stu-id="bc888-153">DIALOG_SDI</span></span>
  
> <span data-ttu-id="bc888-154">Affiche la version non modée de la boîte de dialogue d’adresse commune.</span><span class="sxs-lookup"><span data-stu-id="bc888-154">Displays the modeless version of the common address dialog box.</span></span> <span data-ttu-id="bc888-155">Cet indicateur s’exclue mutuellement avec DIALOG_MODAL.</span><span class="sxs-lookup"><span data-stu-id="bc888-155">This flag is mutually exclusive with DIALOG_MODAL.</span></span>
    
<span data-ttu-id="bc888-156">MAPI_UNICODE</span><span class="sxs-lookup"><span data-stu-id="bc888-156">MAPI_UNICODE</span></span>
  
> <span data-ttu-id="bc888-157">Les chaînes transmises sont au format Unicode.</span><span class="sxs-lookup"><span data-stu-id="bc888-157">The passed-in strings are in Unicode format.</span></span> <span data-ttu-id="bc888-158">Si l’MAPI_UNICODE n’est pas définie, les chaînes sont au format ANSI.</span><span class="sxs-lookup"><span data-stu-id="bc888-158">If the MAPI_UNICODE flag is not set, the strings are in ANSI format.</span></span>
    

