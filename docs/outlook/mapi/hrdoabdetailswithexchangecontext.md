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
ms.openlocfilehash: 353a663071a9f23f0d2330169d3ac7747e047c2b
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32347851"
---
# <a name="hrdoabdetailswithexchangecontext"></a><span data-ttu-id="d936c-103">HrDoABDetailsWithExchangeContext</span><span class="sxs-lookup"><span data-stu-id="d936c-103">HrDoABDetailsWithExchangeContext</span></span>

  
  
<span data-ttu-id="d936c-104">**S’applique à** : Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="d936c-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="d936c-105">Garantit que la méthode **OpenEntry** est ouverte par le fournisseur de carnet d'adresses Exchange attendu.</span><span class="sxs-lookup"><span data-stu-id="d936c-105">Ensures that the **OpenEntry** method is opened by the expected Exchange address book provider.</span></span> <span data-ttu-id="d936c-106">Cette fonction fonctionne de la même manière que [IAddrBook::D etails](iaddrbook-details.md), mais il ouvre la propriété **entryID** à l'aide du carnet d'adresses Exchange identifié par le paramètre _pEmsmdbUID_ .</span><span class="sxs-lookup"><span data-stu-id="d936c-106">This function works similarly to [IAddrBook::Details](iaddrbook-details.md), but opens the **entryID** using the Exchange address book identified by the  _pEmsmdbUID_ parameter.</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="d936c-107">Fichier d’en-tête :</span><span class="sxs-lookup"><span data-stu-id="d936c-107">Header file:</span></span>  <br/> |<span data-ttu-id="d936c-108">abhelp. h</span><span class="sxs-lookup"><span data-stu-id="d936c-108">abhelp.h</span></span>  <br/> |
|<span data-ttu-id="d936c-109">Implémenté par :</span><span class="sxs-lookup"><span data-stu-id="d936c-109">Implemented by:</span></span>  <br/> |<span data-ttu-id="d936c-110">MAPI</span><span class="sxs-lookup"><span data-stu-id="d936c-110">MAPI</span></span>  <br/> |
|<span data-ttu-id="d936c-111">Appelé par :</span><span class="sxs-lookup"><span data-stu-id="d936c-111">Called by:</span></span>  <br/> |<span data-ttu-id="d936c-112">Applications clientes et fournisseurs de services</span><span class="sxs-lookup"><span data-stu-id="d936c-112">Client applications and service providers</span></span>  <br/> |
   
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

## <a name="parameters"></a><span data-ttu-id="d936c-113">Paramètres</span><span class="sxs-lookup"><span data-stu-id="d936c-113">Parameters</span></span>

 <span data-ttu-id="d936c-114">_pmsess_</span><span class="sxs-lookup"><span data-stu-id="d936c-114">_pmsess_</span></span>
  
> <span data-ttu-id="d936c-115">Le **IMAPISession**connecté.</span><span class="sxs-lookup"><span data-stu-id="d936c-115">The logged on **IMAPISession**.</span></span> <span data-ttu-id="d936c-116">Il ne peut pas être NULL.</span><span class="sxs-lookup"><span data-stu-id="d936c-116">It cannot be NULL.</span></span>
    
 <span data-ttu-id="d936c-117">_pEmsmdbUID_</span><span class="sxs-lookup"><span data-stu-id="d936c-117">_pEmsmdbUID_</span></span>
  
> <span data-ttu-id="d936c-118">Pointeur vers un **emsmdbUID** qui identifie le service Exchange qui contient le fournisseur de carnets d'adresses Exchange utilisé par la fonction pour ouvrir l'identificateur d'entrée.</span><span class="sxs-lookup"><span data-stu-id="d936c-118">A pointer to an **emsmdbUID** that identifies the Exchange Service that contains the Exchange address book provider that is used by the function to open the entry identifier.</span></span> <span data-ttu-id="d936c-119">Si l'identificateur d'entrée entrante n'est pas un identificateur d'entrée de fournisseur de carnet d'adresses Exchange, ce paramètre est ignoré et la fonction se comporte comme [IAddrBook:: OpenEntry](iaddrbook-openentry.md).</span><span class="sxs-lookup"><span data-stu-id="d936c-119">If the incoming entry identifier is not an Exchange address book provider entry identifier, this parameter is ignored and the function behaves like [IAddrBook::OpenEntry](iaddrbook-openentry.md).</span></span> <span data-ttu-id="d936c-120">Si ce paramètre a la valeur NULL ou a la valeur zéro **MAPIUID**, cette fonction agit également exactement comme [IAddrBook:: OpenEntry](iaddrbook-openentry.md).</span><span class="sxs-lookup"><span data-stu-id="d936c-120">If this parameter is NULL or a zero **MAPIUID**, this function also acts exactly like [IAddrBook::OpenEntry](iaddrbook-openentry.md).</span></span> 
    
 <span data-ttu-id="d936c-121">_pAddrBook_</span><span class="sxs-lookup"><span data-stu-id="d936c-121">_pAddrBook_</span></span>
  
> <span data-ttu-id="d936c-122">dans Carnet d'adresses utilisé pour ouvrir l'identificateur d'entrée.</span><span class="sxs-lookup"><span data-stu-id="d936c-122">[in] The address book used to open the entry identifier.</span></span> <span data-ttu-id="d936c-123">Il ne peut pas être NULL.</span><span class="sxs-lookup"><span data-stu-id="d936c-123">It cannot be NULL.</span></span>
    
 <span data-ttu-id="d936c-124">_lpulUIParam_</span><span class="sxs-lookup"><span data-stu-id="d936c-124">_lpulUIParam_</span></span>
  
> <span data-ttu-id="d936c-125">remarquer Handle de la fenêtre parente de la boîte de dialogue.</span><span class="sxs-lookup"><span data-stu-id="d936c-125">[out] A handle to the parent window for the dialog box.</span></span>
    
 <span data-ttu-id="d936c-126">_lpfnDismiss_</span><span class="sxs-lookup"><span data-stu-id="d936c-126">_lpfnDismiss_</span></span>
  
> <span data-ttu-id="d936c-127">dans Pointeur vers une fonction basée sur le prototype **DISMISSMODELESS** , ou valeur null.</span><span class="sxs-lookup"><span data-stu-id="d936c-127">[in] A pointer to a function based on the **DISMISSMODELESS** prototype, or NULL.</span></span> <span data-ttu-id="d936c-128">Ce membre s'applique uniquement à la version non modale de la boîte de dialogue, comme indiqué par l'indicateur DIALOG_SDI défini.</span><span class="sxs-lookup"><span data-stu-id="d936c-128">This member applies only to the modeless version of the dialog box, as indicated by the DIALOG_SDI flag being set.</span></span> <span data-ttu-id="d936c-129">MAPI appelle la fonction **DISMISSMODELESS** lorsque l'utilisateur fait disparaître la boîte de dialogue d'adresses non modale, en informant un client qui appelle les détails que la boîte de dialogue n'est plus active.</span><span class="sxs-lookup"><span data-stu-id="d936c-129">MAPI calls the **DISMISSMODELESS** function when the user dismisses the modeless address dialog box, informing a client that is calling Details that the dialog box is no longer active.</span></span> 
    
 <span data-ttu-id="d936c-130">_lpvDismissContext_</span><span class="sxs-lookup"><span data-stu-id="d936c-130">_lpvDismissContext_</span></span>
  
> <span data-ttu-id="d936c-131">dans Pointeur vers les informations de contexte à transmettre à la fonction **DISMISSMODELESS** vers laquelle pointe le paramètre _lpfnDismiss_ .</span><span class="sxs-lookup"><span data-stu-id="d936c-131">[in] A pointer to context information to pass to the **DISMISSMODELESS** function pointed to by the  _lpfnDismiss_ parameter.</span></span> <span data-ttu-id="d936c-132">Ce paramètre s'applique uniquement à la version non modale de la boîte de dialogue en incluant l'indicateur **DIALOG_SDI** dans le paramètre _ulFlags_ .</span><span class="sxs-lookup"><span data-stu-id="d936c-132">This parameter applies only to the modeless version of the dialog box by including the **DIALOG_SDI** flag in the  _ulFlags_ parameter.</span></span> 
    
 <span data-ttu-id="d936c-133">_cbEntryID_</span><span class="sxs-lookup"><span data-stu-id="d936c-133">_cbEntryID_</span></span>
  
> <span data-ttu-id="d936c-134">dans Nombre d'octets de l'identificateur d'entrée spécifié par le paramètre _lpEntryID_ .</span><span class="sxs-lookup"><span data-stu-id="d936c-134">[in] The byte count of the entry identifier specified by the  _lpEntryID_ parameter.</span></span> 
    
 <span data-ttu-id="d936c-135">_lpEntryID_</span><span class="sxs-lookup"><span data-stu-id="d936c-135">_lpEntryID_</span></span>
  
> <span data-ttu-id="d936c-136">dans Pointeur vers l'identificateur d'entrée qui représente l'entrée de carnet d'adresses à ouvrir.</span><span class="sxs-lookup"><span data-stu-id="d936c-136">[in] A pointer to the entry identifier that represents the address book entry to open.</span></span>
    
 <span data-ttu-id="d936c-137">_lpfButtonCallback_</span><span class="sxs-lookup"><span data-stu-id="d936c-137">_lpfButtonCallback_</span></span>
  
> <span data-ttu-id="d936c-138">dans Pointeur vers une fonction basée sur le prototype de fonction **LPFNBUTTON** .</span><span class="sxs-lookup"><span data-stu-id="d936c-138">[in] A pointer to a function based on the **LPFNBUTTON** function prototype.</span></span> <span data-ttu-id="d936c-139">Une fonction **LPFNBUTTON** ajoute un bouton à la boîte de dialogue détails.</span><span class="sxs-lookup"><span data-stu-id="d936c-139">An **LPFNBUTTON** function adds a button to the details dialog box.</span></span> 
    
 <span data-ttu-id="d936c-140">_lpvButtonContext_</span><span class="sxs-lookup"><span data-stu-id="d936c-140">_lpvButtonContext_</span></span>
  
> <span data-ttu-id="d936c-141">dans Pointeur vers les données qui ont été utilisées comme paramètre pour la fonction spécifiée par le paramètre _lpfButtonCallback_ .</span><span class="sxs-lookup"><span data-stu-id="d936c-141">[in] A pointer to data that was used as a parameter for the function specified by the  _lpfButtonCallback_ parameter.</span></span> 
    
 <span data-ttu-id="d936c-142">_lpszButtonText_</span><span class="sxs-lookup"><span data-stu-id="d936c-142">_lpszButtonText_</span></span>
  
> <span data-ttu-id="d936c-143">dans Pointeur vers une chaîne qui contient le texte à appliquer au bouton ajouté, si ce bouton est extensible.</span><span class="sxs-lookup"><span data-stu-id="d936c-143">[in] A pointer to a string that contains text to be applied to the added button, if that button is extensible.</span></span> <span data-ttu-id="d936c-144">Le paramètre _lpszButtonText_ doit être null lorsqu'un bouton extensible n'est pas nécessaire.</span><span class="sxs-lookup"><span data-stu-id="d936c-144">The  _lpszButtonText_ parameter should be NULL when an extensible button is not needed.</span></span> 
    
 <span data-ttu-id="d936c-145">_ulFlags_</span><span class="sxs-lookup"><span data-stu-id="d936c-145">_ulFlags_</span></span>
  
> <span data-ttu-id="d936c-146">dans Masque de des indicateurs qui contrôle le type de texte pour le paramètre _lpszButtonText_ .</span><span class="sxs-lookup"><span data-stu-id="d936c-146">[in] A bitmask of flags that controls the type of the text for the  _lpszButtonText_ parameter.</span></span> <span data-ttu-id="d936c-147">Les indicateurs suivants peuvent être définis:</span><span class="sxs-lookup"><span data-stu-id="d936c-147">The following flags can be set:</span></span> 
    
<span data-ttu-id="d936c-148">AB_TELL_DETAILS_CHANGE</span><span class="sxs-lookup"><span data-stu-id="d936c-148">AB_TELL_DETAILS_CHANGE</span></span>
  
> <span data-ttu-id="d936c-149">Indique que les détails renvoient la valeur TRUE si les modifications sont réellement apportées à l'adresse; dans le cas contraire, la méthode Details renvoie FALSe.</span><span class="sxs-lookup"><span data-stu-id="d936c-149">Indicates that Details returns TRUE if changes are actually made to the address; otherwise, Details returns FALSE.</span></span>
    
<span data-ttu-id="d936c-150">DIALOG_MODAL</span><span class="sxs-lookup"><span data-stu-id="d936c-150">DIALOG_MODAL</span></span>
  
> <span data-ttu-id="d936c-151">Affiche la version modale de la boîte de dialogue adresse commune.</span><span class="sxs-lookup"><span data-stu-id="d936c-151">Displays the modal version of the common address dialog box.</span></span> <span data-ttu-id="d936c-152">Cet indicateur est mutuellement exclusif avec DIALOG_SDI.</span><span class="sxs-lookup"><span data-stu-id="d936c-152">This flag is mutually exclusive with DIALOG_SDI.</span></span>
    
<span data-ttu-id="d936c-153">DIALOG_SDI</span><span class="sxs-lookup"><span data-stu-id="d936c-153">DIALOG_SDI</span></span>
  
> <span data-ttu-id="d936c-154">Affiche la version non modale de la boîte de dialogue adresse commune.</span><span class="sxs-lookup"><span data-stu-id="d936c-154">Displays the modeless version of the common address dialog box.</span></span> <span data-ttu-id="d936c-155">Cet indicateur est mutuellement exclusif avec DIALOG_MODAL.</span><span class="sxs-lookup"><span data-stu-id="d936c-155">This flag is mutually exclusive with DIALOG_MODAL.</span></span>
    
<span data-ttu-id="d936c-156">MAPI_UNICODE</span><span class="sxs-lookup"><span data-stu-id="d936c-156">MAPI_UNICODE</span></span>
  
> <span data-ttu-id="d936c-157">Les chaînes transmises sont au format Unicode.</span><span class="sxs-lookup"><span data-stu-id="d936c-157">The passed-in strings are in Unicode format.</span></span> <span data-ttu-id="d936c-158">Si l'indicateur MAPI_UNICODE n'est pas défini, les chaînes sont au format ANSI.</span><span class="sxs-lookup"><span data-stu-id="d936c-158">If the MAPI_UNICODE flag is not set, the strings are in ANSI format.</span></span>
    

