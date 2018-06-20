---
title: HrDoABDetailsWithProviderUID
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: 27741887-8405-49ed-b080-613613faf91b
description: 'Derni�re modification�: lundi 9 mars 2015'
ms.openlocfilehash: fada57c45602f0a0b07276034101fa23a7525f5b
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19783531"
---
# <a name="hrdoabdetailswithprovideruid"></a><span data-ttu-id="1c870-103">HrDoABDetailsWithProviderUID</span><span class="sxs-lookup"><span data-stu-id="1c870-103">HrDoABDetailsWithProviderUID</span></span>

  
  
<span data-ttu-id="1c870-104">**S’applique à**: Outlook</span><span class="sxs-lookup"><span data-stu-id="1c870-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="1c870-105">Garantit que la méthode **OpenEntry** est ouvert par le fournisseur de carnet d’adresses Exchange attendu.</span><span class="sxs-lookup"><span data-stu-id="1c870-105">Ensures that the **OpenEntry** method is opened by the expected Exchange address book provider.</span></span> <span data-ttu-id="1c870-106">Cette fonction fonctionne comme [IAddrBook::Details](iaddrbook-details.md) mais ouvre **entryID** à l’aide du carnet d’adresses Exchange identifié par _pEmsabpUID_.</span><span class="sxs-lookup"><span data-stu-id="1c870-106">This function works similarly to [IAddrBook::Details](iaddrbook-details.md) but opens **entryID** using the Exchange address book identified by  _pEmsabpUID_.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="1c870-107">Fichier d’en-tête :</span><span class="sxs-lookup"><span data-stu-id="1c870-107">Header file:</span></span>  <br/> |<span data-ttu-id="1c870-108">abhelp.h</span><span class="sxs-lookup"><span data-stu-id="1c870-108">abhelp.h</span></span>  <br/> |
|<span data-ttu-id="1c870-109">Implémentée par :</span><span class="sxs-lookup"><span data-stu-id="1c870-109">Implemented by:</span></span>  <br/> |<span data-ttu-id="1c870-110">MAPI</span><span class="sxs-lookup"><span data-stu-id="1c870-110">MAPI</span></span>  <br/> |
|<span data-ttu-id="1c870-111">Appelée par :</span><span class="sxs-lookup"><span data-stu-id="1c870-111">Called by:</span></span>  <br/> |<span data-ttu-id="1c870-112">Les applications clientes et des fournisseurs de services</span><span class="sxs-lookup"><span data-stu-id="1c870-112">Client applications and service providers</span></span>  <br/> |
   
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

## <a name="parameters"></a><span data-ttu-id="1c870-113">Paramètres</span><span class="sxs-lookup"><span data-stu-id="1c870-113">Parameters</span></span>

 <span data-ttu-id="1c870-114">_pEmsabpUID_</span><span class="sxs-lookup"><span data-stu-id="1c870-114">_pEmsabpUID_</span></span>
  
> <span data-ttu-id="1c870-115">[in] Un pointeur vers un _emsabpUID_ qui identifie le fournisseur de carnet d’adresses Exchange cette fonction doit utiliser pour afficher plus d’informations sur l’identificateur d’entrée.</span><span class="sxs-lookup"><span data-stu-id="1c870-115">[in] A pointer to an  _emsabpUID_ that identifies the Exchange address book provider this function should use to display details on the entry identifier.</span></span> <span data-ttu-id="1c870-116">Si l’identificateur d’entrée entrant n’est pas un identificateur d’entrée Exchange adresse livre fournisseur, ce paramètre est ignoré et la fonction appel exactement joue [IAddrBook::Details](iaddrbook-details.md).</span><span class="sxs-lookup"><span data-stu-id="1c870-116">If the incoming entry identifier is not an Exchange address book provider entry identifier, this parameter is ignored and the function call acts exactly like [IAddrBook::Details](iaddrbook-details.md).</span></span> <span data-ttu-id="1c870-117">Si ce paramètre est NULL ou un zéro MAPIUID, cette fonction comporte également exactement comme [IAddrBook::Details](iaddrbook-details.md).</span><span class="sxs-lookup"><span data-stu-id="1c870-117">If this parameter is NULL or a zero MAPIUID, this function also acts exactly like [IAddrBook::Details](iaddrbook-details.md).</span></span>
    
 <span data-ttu-id="1c870-118">_pAddrBook_</span><span class="sxs-lookup"><span data-stu-id="1c870-118">_pAddrBook_</span></span>
  
> <span data-ttu-id="1c870-119">[in] Le carnet d’adresses utilisée pour ouvrir l’identificateur d’entrée.</span><span class="sxs-lookup"><span data-stu-id="1c870-119">[in] The address book used to open the entry identifier.</span></span> <span data-ttu-id="1c870-120">Il ne peut pas être NULL.</span><span class="sxs-lookup"><span data-stu-id="1c870-120">It cannot be NULL.</span></span>
    
 <span data-ttu-id="1c870-121">_lpulUIParam_</span><span class="sxs-lookup"><span data-stu-id="1c870-121">_lpulUIParam_</span></span>
  
> <span data-ttu-id="1c870-122">[out] Handle vers la fenêtre parente de la boîte de dialogue.</span><span class="sxs-lookup"><span data-stu-id="1c870-122">[out] A handle to the parent window for the dialog box.</span></span>
    
 <span data-ttu-id="1c870-123">_lpfnDismiss_</span><span class="sxs-lookup"><span data-stu-id="1c870-123">_lpfnDismiss_</span></span>
  
> <span data-ttu-id="1c870-124">[in] Pointeur vers une fonction basée sur le prototype **DISMISSMODELESS** ou NULL.</span><span class="sxs-lookup"><span data-stu-id="1c870-124">[in] A pointer to a function based on the **DISMISSMODELESS** prototype, or NULL.</span></span> <span data-ttu-id="1c870-125">Ce membre s’applique uniquement à la version de la boîte de dialogue non modale, telle qu’indiquée par l’indicateur DIALOG_SDI en cours.</span><span class="sxs-lookup"><span data-stu-id="1c870-125">This member applies only to the modeless version of the dialog box, as indicated by the DIALOG_SDI flag being set.</span></span> <span data-ttu-id="1c870-126">MAPI appelle la fonction **DISMISSMODELESS** lorsque l’utilisateur ferme la boîte de dialogue non modale adresse informant le client qui appelle plus d’informations que la boîte de dialogue n’est plus active.</span><span class="sxs-lookup"><span data-stu-id="1c870-126">MAPI calls the **DISMISSMODELESS** function when the user dismisses the modeless address dialog box, informing a client that is calling Details that the dialog box is no longer active.</span></span> 
    
 <span data-ttu-id="1c870-127">_lpvDismissContext_</span><span class="sxs-lookup"><span data-stu-id="1c870-127">_lpvDismissContext_</span></span>
  
> <span data-ttu-id="1c870-128">[in] Un pointeur vers les informations de contexte à transmettre à la fonction **DISMISSMODELESS** indiqué par le paramètre _lpfnDismiss_ .</span><span class="sxs-lookup"><span data-stu-id="1c870-128">[in] A pointer to context information to pass to the **DISMISSMODELESS** function pointed to by the  _lpfnDismiss_ parameter.</span></span> <span data-ttu-id="1c870-129">Ce paramètre s’applique uniquement à la version de la boîte de dialogue non modale en incluant l’indicateur **DIALOG_SDI** dans le paramètre _ulFlags_ .</span><span class="sxs-lookup"><span data-stu-id="1c870-129">This parameter applies only to the modeless version of the dialog box by including the **DIALOG_SDI** flag in the  _ulFlags_ parameter.</span></span> 
    
 <span data-ttu-id="1c870-130">_cbEntryID_</span><span class="sxs-lookup"><span data-stu-id="1c870-130">_cbEntryID_</span></span>
  
> <span data-ttu-id="1c870-131">[in] Nombre d’octets de l’identificateur d’entrée spécifié par le paramètre _lpEntryID_ .</span><span class="sxs-lookup"><span data-stu-id="1c870-131">[in] The byte count of the entry identifier specified by the  _lpEntryID_ parameter.</span></span> 
    
 <span data-ttu-id="1c870-132">_lpEntryID_</span><span class="sxs-lookup"><span data-stu-id="1c870-132">_lpEntryID_</span></span>
  
> <span data-ttu-id="1c870-133">[in] Pointeur vers l’identificateur d’entrée qui représente l’entrée du carnet d’adresses à ouvrir.</span><span class="sxs-lookup"><span data-stu-id="1c870-133">[in] A pointer to the entry identifier that represents the address book entry to open.</span></span>
    
 <span data-ttu-id="1c870-134">_lpfButtonCallback_</span><span class="sxs-lookup"><span data-stu-id="1c870-134">_lpfButtonCallback_</span></span>
  
> <span data-ttu-id="1c870-135">[in] Pointeur vers une fonction basée sur le prototype de fonction **LPFNBUTTON** .</span><span class="sxs-lookup"><span data-stu-id="1c870-135">[in] A pointer to a function based on the **LPFNBUTTON** function prototype.</span></span> <span data-ttu-id="1c870-136">Une fonction **LPFNBUTTON** ajoute un bouton à la boîte de dialogue Détails.</span><span class="sxs-lookup"><span data-stu-id="1c870-136">An **LPFNBUTTON** function adds a button to the details dialog box.</span></span> 
    
 <span data-ttu-id="1c870-137">_lpvButtonContext_</span><span class="sxs-lookup"><span data-stu-id="1c870-137">_lpvButtonContext_</span></span>
  
> <span data-ttu-id="1c870-138">[in] Pointeur vers les données qui a été utilisés en tant que paramètre pour la fonction spécifiée par le paramètre _lpfButtonCallback_ .</span><span class="sxs-lookup"><span data-stu-id="1c870-138">[in] A pointer to data that was used as a parameter for the function specified by the  _lpfButtonCallback_ parameter.</span></span> 
    
 <span data-ttu-id="1c870-139">_lpszButtonText_</span><span class="sxs-lookup"><span data-stu-id="1c870-139">_lpszButtonText_</span></span>
  
> <span data-ttu-id="1c870-140">[in] Pointeur vers une chaîne qui contient du texte à appliquer au bouton ajouté, si ce bouton est extensible.</span><span class="sxs-lookup"><span data-stu-id="1c870-140">[in] A pointer to a string that contains text to be applied to the added button, if that button is extensible.</span></span> <span data-ttu-id="1c870-141">Le paramètre _lpszButtonText_ doit être NULL lorsqu’un bouton extensible n’est pas nécessaire.</span><span class="sxs-lookup"><span data-stu-id="1c870-141">The  _lpszButtonText_ parameter should be NULL when an extensible button is not needed.</span></span> 
    
 <span data-ttu-id="1c870-142">_ulFlags_</span><span class="sxs-lookup"><span data-stu-id="1c870-142">_ulFlags_</span></span>
  
> <span data-ttu-id="1c870-143">[in] Masque de bits d’indicateurs qui contrôle le type du texte pour le paramètre _lpszButtonText_ .</span><span class="sxs-lookup"><span data-stu-id="1c870-143">[in] A bitmask of flags that controls the type of the text for the  _lpszButtonText_ parameter.</span></span> <span data-ttu-id="1c870-144">Les indicateurs suivants peuvent être définis :</span><span class="sxs-lookup"><span data-stu-id="1c870-144">The following flags can be set:</span></span> 
    
<span data-ttu-id="1c870-145">AB_TELL_DETAILS_CHANGE</span><span class="sxs-lookup"><span data-stu-id="1c870-145">AB_TELL_DETAILS_CHANGE</span></span>
  
> <span data-ttu-id="1c870-146">Indique que les détails renvoie la valeur TRUE si les modifications sont réellement apportées à l’adresse ; plus d’informations dans le cas contraire, renvoie la valeur FALSE.</span><span class="sxs-lookup"><span data-stu-id="1c870-146">Indicates that Details returns TRUE if changes are actually made to the address; otherwise, Details returns FALSE.</span></span>
    
<span data-ttu-id="1c870-147">DIALOG_MODAL</span><span class="sxs-lookup"><span data-stu-id="1c870-147">DIALOG_MODAL</span></span>
  
> <span data-ttu-id="1c870-148">Affiche la version de la boîte de dialogue adresse modale.</span><span class="sxs-lookup"><span data-stu-id="1c870-148">Displays the modal version of the common address dialog box.</span></span> <span data-ttu-id="1c870-149">Cet indicateur est mutuellement exclusif avec DIALOG_SDI.</span><span class="sxs-lookup"><span data-stu-id="1c870-149">This flag is mutually exclusive with DIALOG_SDI.</span></span>
    
<span data-ttu-id="1c870-150">DIALOG_SDI</span><span class="sxs-lookup"><span data-stu-id="1c870-150">DIALOG_SDI</span></span>
  
> <span data-ttu-id="1c870-151">Affiche la version de la boîte de dialogue adresse non modale.</span><span class="sxs-lookup"><span data-stu-id="1c870-151">Displays the modeless version of the common address dialog box.</span></span> <span data-ttu-id="1c870-152">Cet indicateur est mutuellement exclusif avec DIALOG_MODAL.</span><span class="sxs-lookup"><span data-stu-id="1c870-152">This flag is mutually exclusive with DIALOG_MODAL.</span></span>
    
<span data-ttu-id="1c870-153">MAPI_UNICODE</span><span class="sxs-lookup"><span data-stu-id="1c870-153">MAPI_UNICODE</span></span>
  
> <span data-ttu-id="1c870-154">Les chaînes passée sont au format Unicode.</span><span class="sxs-lookup"><span data-stu-id="1c870-154">The passed-in strings are in Unicode format.</span></span> <span data-ttu-id="1c870-155">Si l’indicateur MAPI_UNICODE n’est pas définie, les chaînes sont au format ANSI.</span><span class="sxs-lookup"><span data-stu-id="1c870-155">If the MAPI_UNICODE flag is not set, the strings are in ANSI format.</span></span>
    

