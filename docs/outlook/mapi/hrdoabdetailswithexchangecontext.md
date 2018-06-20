---
title: HrDoABDetailsWithExchangeContext
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: b4e7fed2-88e4-4e14-90b6-913a1b7e338a
description: 'Derni�re modification�: lundi 9 mars 2015'
ms.openlocfilehash: cb6138072cd5dedc528168d4056041661c40fd06
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19783544"
---
# <a name="hrdoabdetailswithexchangecontext"></a><span data-ttu-id="7b378-103">HrDoABDetailsWithExchangeContext</span><span class="sxs-lookup"><span data-stu-id="7b378-103">HrDoABDetailsWithExchangeContext</span></span>

  
  
<span data-ttu-id="7b378-104">**S’applique à**: Outlook</span><span class="sxs-lookup"><span data-stu-id="7b378-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="7b378-105">Garantit que la méthode **OpenEntry** est ouvert par le fournisseur de carnet d’adresses Exchange attendu.</span><span class="sxs-lookup"><span data-stu-id="7b378-105">Ensures that the **OpenEntry** method is opened by the expected Exchange address book provider.</span></span> <span data-ttu-id="7b378-106">Cette fonction fonctionne comme [IAddrBook::Details](iaddrbook-details.md), mais s’ouvre **entryID** à l’aide du carnet d’adresses Exchange identifié par le paramètre _pEmsmdbUID_ .</span><span class="sxs-lookup"><span data-stu-id="7b378-106">This function works similarly to [IAddrBook::Details](iaddrbook-details.md), but opens the **entryID** using the Exchange address book identified by the  _pEmsmdbUID_ parameter.</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="7b378-107">Fichier d’en-tête :</span><span class="sxs-lookup"><span data-stu-id="7b378-107">Header file:</span></span>  <br/> |<span data-ttu-id="7b378-108">abhelp.h</span><span class="sxs-lookup"><span data-stu-id="7b378-108">abhelp.h</span></span>  <br/> |
|<span data-ttu-id="7b378-109">Implémentée par :</span><span class="sxs-lookup"><span data-stu-id="7b378-109">Implemented by:</span></span>  <br/> |<span data-ttu-id="7b378-110">MAPI</span><span class="sxs-lookup"><span data-stu-id="7b378-110">MAPI</span></span>  <br/> |
|<span data-ttu-id="7b378-111">Appelée par :</span><span class="sxs-lookup"><span data-stu-id="7b378-111">Called by:</span></span>  <br/> |<span data-ttu-id="7b378-112">Les applications clientes et des fournisseurs de services</span><span class="sxs-lookup"><span data-stu-id="7b378-112">Client applications and service providers</span></span>  <br/> |
   
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

## <a name="parameters"></a><span data-ttu-id="7b378-113">Paramètres</span><span class="sxs-lookup"><span data-stu-id="7b378-113">Parameters</span></span>

 <span data-ttu-id="7b378-114">_pmsess_</span><span class="sxs-lookup"><span data-stu-id="7b378-114">_pmsess_</span></span>
  
> <span data-ttu-id="7b378-115">La session **IMAPISession**.</span><span class="sxs-lookup"><span data-stu-id="7b378-115">The logged on **IMAPISession**.</span></span> <span data-ttu-id="7b378-116">Il ne peut pas être NULL.</span><span class="sxs-lookup"><span data-stu-id="7b378-116">It cannot be NULL.</span></span>
    
 <span data-ttu-id="7b378-117">_pEmsmdbUID_</span><span class="sxs-lookup"><span data-stu-id="7b378-117">_pEmsmdbUID_</span></span>
  
> <span data-ttu-id="7b378-118">Pointeur vers un **emsmdbUID** qui identifie le Service Exchange qui contient le fournisseur de carnet d’adresses Exchange qui est utilisé par la fonction pour ouvrir l’identificateur d’entrée.</span><span class="sxs-lookup"><span data-stu-id="7b378-118">A pointer to an **emsmdbUID** that identifies the Exchange Service that contains the Exchange address book provider that is used by the function to open the entry identifier.</span></span> <span data-ttu-id="7b378-119">Si l’identificateur d’entrée entrant n’est pas un identificateur d’entrée Exchange adresse livre fournisseur, ce paramètre est ignoré et la fonction se comporte comme [IAddrBook::OpenEntry](iaddrbook-openentry.md).</span><span class="sxs-lookup"><span data-stu-id="7b378-119">If the incoming entry identifier is not an Exchange address book provider entry identifier, this parameter is ignored and the function behaves like [IAddrBook::OpenEntry](iaddrbook-openentry.md).</span></span> <span data-ttu-id="7b378-120">Si ce paramètre est NULL ou un zéro **MAPIUID**, cette fonction comporte également exactement comme [IAddrBook::OpenEntry](iaddrbook-openentry.md).</span><span class="sxs-lookup"><span data-stu-id="7b378-120">If this parameter is NULL or a zero **MAPIUID**, this function also acts exactly like [IAddrBook::OpenEntry](iaddrbook-openentry.md).</span></span> 
    
 <span data-ttu-id="7b378-121">_pAddrBook_</span><span class="sxs-lookup"><span data-stu-id="7b378-121">_pAddrBook_</span></span>
  
> <span data-ttu-id="7b378-122">[in] Le carnet d’adresses utilisée pour ouvrir l’identificateur d’entrée.</span><span class="sxs-lookup"><span data-stu-id="7b378-122">[in] The address book used to open the entry identifier.</span></span> <span data-ttu-id="7b378-123">Il ne peut pas être NULL.</span><span class="sxs-lookup"><span data-stu-id="7b378-123">It cannot be NULL.</span></span>
    
 <span data-ttu-id="7b378-124">_lpulUIParam_</span><span class="sxs-lookup"><span data-stu-id="7b378-124">_lpulUIParam_</span></span>
  
> <span data-ttu-id="7b378-125">[out] Handle vers la fenêtre parente de la boîte de dialogue.</span><span class="sxs-lookup"><span data-stu-id="7b378-125">[out] A handle to the parent window for the dialog box.</span></span>
    
 <span data-ttu-id="7b378-126">_lpfnDismiss_</span><span class="sxs-lookup"><span data-stu-id="7b378-126">_lpfnDismiss_</span></span>
  
> <span data-ttu-id="7b378-127">[in] Pointeur vers une fonction basée sur le prototype **DISMISSMODELESS** ou NULL.</span><span class="sxs-lookup"><span data-stu-id="7b378-127">[in] A pointer to a function based on the **DISMISSMODELESS** prototype, or NULL.</span></span> <span data-ttu-id="7b378-128">Ce membre s’applique uniquement à la version de la boîte de dialogue non modale, telle qu’indiquée par l’indicateur DIALOG_SDI en cours.</span><span class="sxs-lookup"><span data-stu-id="7b378-128">This member applies only to the modeless version of the dialog box, as indicated by the DIALOG_SDI flag being set.</span></span> <span data-ttu-id="7b378-129">MAPI appelle la fonction **DISMISSMODELESS** lorsque l’utilisateur ferme la boîte de dialogue non modale adresse informant le client qui appelle plus d’informations que la boîte de dialogue n’est plus active.</span><span class="sxs-lookup"><span data-stu-id="7b378-129">MAPI calls the **DISMISSMODELESS** function when the user dismisses the modeless address dialog box, informing a client that is calling Details that the dialog box is no longer active.</span></span> 
    
 <span data-ttu-id="7b378-130">_lpvDismissContext_</span><span class="sxs-lookup"><span data-stu-id="7b378-130">_lpvDismissContext_</span></span>
  
> <span data-ttu-id="7b378-131">[in] Un pointeur vers les informations de contexte à transmettre à la fonction **DISMISSMODELESS** indiqué par le paramètre _lpfnDismiss_ .</span><span class="sxs-lookup"><span data-stu-id="7b378-131">[in] A pointer to context information to pass to the **DISMISSMODELESS** function pointed to by the  _lpfnDismiss_ parameter.</span></span> <span data-ttu-id="7b378-132">Ce paramètre s’applique uniquement à la version de la boîte de dialogue non modale en incluant l’indicateur **DIALOG_SDI** dans le paramètre _ulFlags_ .</span><span class="sxs-lookup"><span data-stu-id="7b378-132">This parameter applies only to the modeless version of the dialog box by including the **DIALOG_SDI** flag in the  _ulFlags_ parameter.</span></span> 
    
 <span data-ttu-id="7b378-133">_cbEntryID_</span><span class="sxs-lookup"><span data-stu-id="7b378-133">_cbEntryID_</span></span>
  
> <span data-ttu-id="7b378-134">[in] Nombre d’octets de l’identificateur d’entrée spécifié par le paramètre _lpEntryID_ .</span><span class="sxs-lookup"><span data-stu-id="7b378-134">[in] The byte count of the entry identifier specified by the  _lpEntryID_ parameter.</span></span> 
    
 <span data-ttu-id="7b378-135">_lpEntryID_</span><span class="sxs-lookup"><span data-stu-id="7b378-135">_lpEntryID_</span></span>
  
> <span data-ttu-id="7b378-136">[in] Pointeur vers l’identificateur d’entrée qui représente l’entrée du carnet d’adresses à ouvrir.</span><span class="sxs-lookup"><span data-stu-id="7b378-136">[in] A pointer to the entry identifier that represents the address book entry to open.</span></span>
    
 <span data-ttu-id="7b378-137">_lpfButtonCallback_</span><span class="sxs-lookup"><span data-stu-id="7b378-137">_lpfButtonCallback_</span></span>
  
> <span data-ttu-id="7b378-138">[in] Pointeur vers une fonction basée sur le prototype de fonction **LPFNBUTTON** .</span><span class="sxs-lookup"><span data-stu-id="7b378-138">[in] A pointer to a function based on the **LPFNBUTTON** function prototype.</span></span> <span data-ttu-id="7b378-139">Une fonction **LPFNBUTTON** ajoute un bouton à la boîte de dialogue Détails.</span><span class="sxs-lookup"><span data-stu-id="7b378-139">An **LPFNBUTTON** function adds a button to the details dialog box.</span></span> 
    
 <span data-ttu-id="7b378-140">_lpvButtonContext_</span><span class="sxs-lookup"><span data-stu-id="7b378-140">_lpvButtonContext_</span></span>
  
> <span data-ttu-id="7b378-141">[in] Pointeur vers les données qui a été utilisés en tant que paramètre pour la fonction spécifiée par le paramètre _lpfButtonCallback_ .</span><span class="sxs-lookup"><span data-stu-id="7b378-141">[in] A pointer to data that was used as a parameter for the function specified by the  _lpfButtonCallback_ parameter.</span></span> 
    
 <span data-ttu-id="7b378-142">_lpszButtonText_</span><span class="sxs-lookup"><span data-stu-id="7b378-142">_lpszButtonText_</span></span>
  
> <span data-ttu-id="7b378-143">[in] Pointeur vers une chaîne qui contient du texte à appliquer au bouton ajouté, si ce bouton est extensible.</span><span class="sxs-lookup"><span data-stu-id="7b378-143">[in] A pointer to a string that contains text to be applied to the added button, if that button is extensible.</span></span> <span data-ttu-id="7b378-144">Le paramètre _lpszButtonText_ doit être NULL lorsqu’un bouton extensible n’est pas nécessaire.</span><span class="sxs-lookup"><span data-stu-id="7b378-144">The  _lpszButtonText_ parameter should be NULL when an extensible button is not needed.</span></span> 
    
 <span data-ttu-id="7b378-145">_ulFlags_</span><span class="sxs-lookup"><span data-stu-id="7b378-145">_ulFlags_</span></span>
  
> <span data-ttu-id="7b378-146">[in] Masque de bits d’indicateurs qui contrôle le type du texte pour le paramètre _lpszButtonText_ .</span><span class="sxs-lookup"><span data-stu-id="7b378-146">[in] A bitmask of flags that controls the type of the text for the  _lpszButtonText_ parameter.</span></span> <span data-ttu-id="7b378-147">Les indicateurs suivants peuvent être définis :</span><span class="sxs-lookup"><span data-stu-id="7b378-147">The following flags can be set:</span></span> 
    
<span data-ttu-id="7b378-148">AB_TELL_DETAILS_CHANGE</span><span class="sxs-lookup"><span data-stu-id="7b378-148">AB_TELL_DETAILS_CHANGE</span></span>
  
> <span data-ttu-id="7b378-149">Indique que les détails renvoie la valeur TRUE si les modifications sont réellement apportées à l’adresse ; plus d’informations dans le cas contraire, renvoie la valeur FALSE.</span><span class="sxs-lookup"><span data-stu-id="7b378-149">Indicates that Details returns TRUE if changes are actually made to the address; otherwise, Details returns FALSE.</span></span>
    
<span data-ttu-id="7b378-150">DIALOG_MODAL</span><span class="sxs-lookup"><span data-stu-id="7b378-150">DIALOG_MODAL</span></span>
  
> <span data-ttu-id="7b378-151">Affiche la version de la boîte de dialogue adresse modale.</span><span class="sxs-lookup"><span data-stu-id="7b378-151">Displays the modal version of the common address dialog box.</span></span> <span data-ttu-id="7b378-152">Cet indicateur est mutuellement exclusif avec DIALOG_SDI.</span><span class="sxs-lookup"><span data-stu-id="7b378-152">This flag is mutually exclusive with DIALOG_SDI.</span></span>
    
<span data-ttu-id="7b378-153">DIALOG_SDI</span><span class="sxs-lookup"><span data-stu-id="7b378-153">DIALOG_SDI</span></span>
  
> <span data-ttu-id="7b378-154">Affiche la version de la boîte de dialogue adresse non modale.</span><span class="sxs-lookup"><span data-stu-id="7b378-154">Displays the modeless version of the common address dialog box.</span></span> <span data-ttu-id="7b378-155">Cet indicateur est mutuellement exclusif avec DIALOG_MODAL.</span><span class="sxs-lookup"><span data-stu-id="7b378-155">This flag is mutually exclusive with DIALOG_MODAL.</span></span>
    
<span data-ttu-id="7b378-156">MAPI_UNICODE</span><span class="sxs-lookup"><span data-stu-id="7b378-156">MAPI_UNICODE</span></span>
  
> <span data-ttu-id="7b378-157">Les chaînes passée sont au format Unicode.</span><span class="sxs-lookup"><span data-stu-id="7b378-157">The passed-in strings are in Unicode format.</span></span> <span data-ttu-id="7b378-158">Si l’indicateur MAPI_UNICODE n’est pas définie, les chaînes sont au format ANSI.</span><span class="sxs-lookup"><span data-stu-id="7b378-158">If the MAPI_UNICODE flag is not set, the strings are in ANSI format.</span></span>
    

