---
title: IMAPISupportDetails
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- IMAPISupport.Details
api_type:
- COM
ms.assetid: 1a62efa2-dd6b-4acb-a760-defa601c20c9
description: 'Dernière modification : 23 juillet 2011'
ms.openlocfilehash: bdc57a6e951e54640fe3c638977c6a5f16986e68
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32322357"
---
# <a name="imapisupportdetails"></a><span data-ttu-id="4555a-103">IMAPISupport::Details</span><span class="sxs-lookup"><span data-stu-id="4555a-103">IMAPISupport::Details</span></span>

  
  
<span data-ttu-id="4555a-104">**S’applique à** : Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="4555a-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="4555a-105">Affiche une boîte de dialogue qui affiche des détails sur une entrée de carnet d'adresses particulière.</span><span class="sxs-lookup"><span data-stu-id="4555a-105">Displays a dialog box that shows details about a particular address book entry.</span></span>
  
```cpp
HRESULT Details(
  ULONG_PTR FAR * lpulUIParam,
  LPFNDISMISS lpfnDismiss,
  LPVOID lpvDismissContext,
  ULONG cbEntryID,
  LPENTRYID lpEntryID,
  LPFNBUTTON lpfButtonCallback,
  LPVOID lpvButtonContext,
  LPSTR lpszButtonText,
  ULONG ulFlags
);
```

## <a name="parameters"></a><span data-ttu-id="4555a-106">Paramètres</span><span class="sxs-lookup"><span data-stu-id="4555a-106">Parameters</span></span>

 <span data-ttu-id="4555a-107">_lpulUIParam_</span><span class="sxs-lookup"><span data-stu-id="4555a-107">_lpulUIParam_</span></span>
  
> <span data-ttu-id="4555a-108">remarquer Pointeur vers le handle de la fenêtre parente de la boîte de dialogue renvoyée.</span><span class="sxs-lookup"><span data-stu-id="4555a-108">[out] A pointer to the handle to the parent window of the returned dialog box.</span></span>
    
 <span data-ttu-id="4555a-109">_lpfnDismiss_</span><span class="sxs-lookup"><span data-stu-id="4555a-109">_lpfnDismiss_</span></span>
  
> <span data-ttu-id="4555a-110">dans Pointeur vers une fonction basée sur le prototype [DISMISSMODELESS](dismissmodeless.md) , ou valeur null.</span><span class="sxs-lookup"><span data-stu-id="4555a-110">[in] A pointer to a function based on the [DISMISSMODELESS](dismissmodeless.md) prototype, or NULL.</span></span> <span data-ttu-id="4555a-111">Ce membre s'applique uniquement à la version non modale de la boîte de dialogue, comme indiqué par l'indicateur DIALOG_SDI défini.</span><span class="sxs-lookup"><span data-stu-id="4555a-111">This member applies only to the modeless version of the dialog box, as indicated by the DIALOG_SDI flag being set.</span></span> <span data-ttu-id="4555a-112">MAPI appelle la fonction **DISMISSMODELESS** lorsque l'utilisateur fait disparaître la boîte de dialogue d'adresses non modale, en informant un client qui appelle **IMAPISupport::D etails** que la boîte de dialogue n'est plus active.</span><span class="sxs-lookup"><span data-stu-id="4555a-112">MAPI calls the **DISMISSMODELESS** function when the user dismisses the modeless address dialog box, informing a client that is calling **IMAPISupport::Details** that the dialog box is no longer active.</span></span> 
    
 <span data-ttu-id="4555a-113">_lpvDismissContext_</span><span class="sxs-lookup"><span data-stu-id="4555a-113">_lpvDismissContext_</span></span>
  
> <span data-ttu-id="4555a-114">dans Pointeur vers les informations de contexte à transmettre à la fonction **DISMISSMODELESS** vers laquelle pointe le paramètre _lpfnDismiss_ .</span><span class="sxs-lookup"><span data-stu-id="4555a-114">[in] A pointer to context information to pass to the **DISMISSMODELESS** function pointed to by the  _lpfnDismiss_ parameter.</span></span> <span data-ttu-id="4555a-115">Ce paramètre s'applique uniquement à la version non modale de la boîte de dialogue, en incluant l'indicateur DIALOG_SDI dans le paramètre _ulFlags_ .</span><span class="sxs-lookup"><span data-stu-id="4555a-115">This parameter applies only to the modeless version of the dialog box, by including the DIALOG_SDI flag in the  _ulFlags_ parameter.</span></span> 
    
 <span data-ttu-id="4555a-116">_cbEntryID_</span><span class="sxs-lookup"><span data-stu-id="4555a-116">_cbEntryID_</span></span>
  
> <span data-ttu-id="4555a-117">dans Nombre d'octets dans l'identificateur d'entrée pointé par le paramètre _lpEntryID_ .</span><span class="sxs-lookup"><span data-stu-id="4555a-117">[in] The byte count in the entry identifier pointed to by the  _lpEntryID_ parameter.</span></span> 
    
 <span data-ttu-id="4555a-118">_lpEntryID_</span><span class="sxs-lookup"><span data-stu-id="4555a-118">_lpEntryID_</span></span>
  
> <span data-ttu-id="4555a-119">dans Pointeur vers l'identificateur d'entrée pour laquelle les détails sont affichés.</span><span class="sxs-lookup"><span data-stu-id="4555a-119">[in] A pointer to the entry identifier for which details are displayed.</span></span>
    
 <span data-ttu-id="4555a-120">_lpfButtonCallback_</span><span class="sxs-lookup"><span data-stu-id="4555a-120">_lpfButtonCallback_</span></span>
  
> <span data-ttu-id="4555a-121">dans Pointeur vers une fonction basée sur le prototype de fonction [LPFNBUTTON](lpfnbutton.md) .</span><span class="sxs-lookup"><span data-stu-id="4555a-121">[in] A pointer to a function based on the [LPFNBUTTON](lpfnbutton.md) function prototype.</span></span> <span data-ttu-id="4555a-122">Une fonction **LPFNBUTTON** ajoute un bouton à la boîte de dialogue détails.</span><span class="sxs-lookup"><span data-stu-id="4555a-122">An **LPFNBUTTON** function adds a button to the details dialog box.</span></span> 
    
 <span data-ttu-id="4555a-123">_lpvButtonContext_</span><span class="sxs-lookup"><span data-stu-id="4555a-123">_lpvButtonContext_</span></span>
  
> <span data-ttu-id="4555a-124">dans Pointeur vers les données utilisées comme paramètre pour la fonction spécifiée par le paramètre _lpfButtonCallback_ .</span><span class="sxs-lookup"><span data-stu-id="4555a-124">[in] A pointer to data used as a parameter for the function specified by the  _lpfButtonCallback_ parameter.</span></span> 
    
 <span data-ttu-id="4555a-125">_lpszButtonText_</span><span class="sxs-lookup"><span data-stu-id="4555a-125">_lpszButtonText_</span></span>
  
> <span data-ttu-id="4555a-126">dans Pointeur vers une chaîne qui contient le texte à appliquer au bouton ajouté si ce bouton est extensible.</span><span class="sxs-lookup"><span data-stu-id="4555a-126">[in] A pointer to a string that contains text to be applied to the added button if that button is extensible.</span></span> <span data-ttu-id="4555a-127">Le paramètre _lpszButtonText_ doit être null si aucun bouton extensible n'est nécessaire.</span><span class="sxs-lookup"><span data-stu-id="4555a-127">The  _lpszButtonText_ parameter should be NULL if an extensible button is not needed.</span></span> 
    
 <span data-ttu-id="4555a-128">_ulFlags_</span><span class="sxs-lookup"><span data-stu-id="4555a-128">_ulFlags_</span></span>
  
> <span data-ttu-id="4555a-129">dans Masque de des indicateurs qui contrôle le type de texte pour le paramètre _lpszButtonText_ .</span><span class="sxs-lookup"><span data-stu-id="4555a-129">[in] A bitmask of flags that controls the type of the text for the  _lpszButtonText_ parameter.</span></span> <span data-ttu-id="4555a-130">L'indicateur suivant peut être défini:</span><span class="sxs-lookup"><span data-stu-id="4555a-130">The following flag can be set:</span></span> 
    
<span data-ttu-id="4555a-131">DIALOG_MODAL</span><span class="sxs-lookup"><span data-stu-id="4555a-131">DIALOG_MODAL</span></span>
  
> <span data-ttu-id="4555a-132">Affiche la version modale de la boîte de dialogue adresse commune.</span><span class="sxs-lookup"><span data-stu-id="4555a-132">Display the modal version of the common address dialog box.</span></span> <span data-ttu-id="4555a-133">Cet indicateur est mutuellement exclusif avec DIALOG_SDI.</span><span class="sxs-lookup"><span data-stu-id="4555a-133">This flag is mutually exclusive with DIALOG_SDI.</span></span>
    
<span data-ttu-id="4555a-134">DIALOG_SDI</span><span class="sxs-lookup"><span data-stu-id="4555a-134">DIALOG_SDI</span></span>
  
>  <span data-ttu-id="4555a-135">Affiche la version non modale de la boîte de dialogue adresse commune.</span><span class="sxs-lookup"><span data-stu-id="4555a-135">Display the modeless version of the common address dialog box.</span></span> <span data-ttu-id="4555a-136">Cet indicateur est mutuellement exclusif avec DIALOG_MODAL.</span><span class="sxs-lookup"><span data-stu-id="4555a-136">This flag is mutually exclusive with DIALOG_MODAL.</span></span> 
    
<span data-ttu-id="4555a-137">MAPI_UNICODE</span><span class="sxs-lookup"><span data-stu-id="4555a-137">MAPI_UNICODE</span></span> 
  
> <span data-ttu-id="4555a-138">Les chaînes transmises sont au format Unicode.</span><span class="sxs-lookup"><span data-stu-id="4555a-138">The passed-in strings are in Unicode format.</span></span> <span data-ttu-id="4555a-139">Si l'indicateur MAPI_UNICODE n'est pas défini, les chaînes sont au format ANSI.</span><span class="sxs-lookup"><span data-stu-id="4555a-139">If the MAPI_UNICODE flag is not set, the strings are in ANSI format.</span></span>
    
## <a name="return-value"></a><span data-ttu-id="4555a-140">Valeur renvoyée</span><span class="sxs-lookup"><span data-stu-id="4555a-140">Return value</span></span>

<span data-ttu-id="4555a-141">S_OK</span><span class="sxs-lookup"><span data-stu-id="4555a-141">S_OK</span></span> 
  
> <span data-ttu-id="4555a-142">La boîte de dialogue détails a été affichée pour l'entrée de carnet d'adresses.</span><span class="sxs-lookup"><span data-stu-id="4555a-142">The details dialog box was successfully displayed for the address book entry.</span></span>
    
## <a name="remarks"></a><span data-ttu-id="4555a-143">Remarques</span><span class="sxs-lookup"><span data-stu-id="4555a-143">Remarks</span></span>

<span data-ttu-id="4555a-144">La méthode **IMAPISupport::D etails** est implémentée pour les objets de prise en charge du fournisseur de carnets d'adresses.</span><span class="sxs-lookup"><span data-stu-id="4555a-144">The **IMAPISupport::Details** method is implemented for address book provider support objects.</span></span> <span data-ttu-id="4555a-145">Fournisseurs de carnet d'adresses **Détails** des appels pour afficher une boîte de dialogue qui fournit des détails sur une entrée particulière dans le carnet d'adresses.</span><span class="sxs-lookup"><span data-stu-id="4555a-145">Address book providers call **Details** to display a dialog box that gives details on a particular entry in the address book.</span></span> <span data-ttu-id="4555a-146">Les paramètres _lpfButtonCallback_, _lpvButtonContext_et _lpszButtonText_ peuvent être utilisés pour ajouter un bouton défini par le client à la boîte de dialogue.</span><span class="sxs-lookup"><span data-stu-id="4555a-146">The  _lpfButtonCallback_,  _lpvButtonContext_, and  _lpszButtonText_ parameters can be used to add a client-defined button to the dialog box.</span></span> <span data-ttu-id="4555a-147">Lorsque l'utilisateur clique sur le bouton, MAPI appelle la fonction de rappel pointée par _lpfButtonCallback_, en transmettant l'identificateur d'entrée du bouton et les données dans _lpvButtonContext_.</span><span class="sxs-lookup"><span data-stu-id="4555a-147">When the button is clicked, MAPI calls the callback function pointed to by  _lpfButtonCallback_, passing both the entry identifier of the button and the data in  _lpvButtonContext_.</span></span> <span data-ttu-id="4555a-148">Si un bouton extensible n'est pas nécessaire, _lpszButtonText_ doit être null.</span><span class="sxs-lookup"><span data-stu-id="4555a-148">If an extensible button is not needed,  _lpszButtonText_ should be NULL.</span></span> 
  
## <a name="see-also"></a><span data-ttu-id="4555a-149">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="4555a-149">See also</span></span>



[<span data-ttu-id="4555a-150">ADRPARM</span><span class="sxs-lookup"><span data-stu-id="4555a-150">ADRPARM</span></span>](adrparm.md)
  
[<span data-ttu-id="4555a-151">IMAPISupport::Address</span><span class="sxs-lookup"><span data-stu-id="4555a-151">IMAPISupport::Address</span></span>](imapisupport-address.md)
  
[<span data-ttu-id="4555a-152">LPFNBUTTON</span><span class="sxs-lookup"><span data-stu-id="4555a-152">LPFNBUTTON</span></span>](lpfnbutton.md)
  
[<span data-ttu-id="4555a-153">IMAPISupport : IUnknown</span><span class="sxs-lookup"><span data-stu-id="4555a-153">IMAPISupport : IUnknown</span></span>](imapisupportiunknown.md)

