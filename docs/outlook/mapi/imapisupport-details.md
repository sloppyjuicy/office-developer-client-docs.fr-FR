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
description: 'Derniére modification : samedi 23 juillet 2011'
ms.openlocfilehash: bdc57a6e951e54640fe3c638977c6a5f16986e68
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/28/2019
ms.locfileid: "33426778"
---
# <a name="imapisupportdetails"></a><span data-ttu-id="c4635-103">IMAPISupport::Details</span><span class="sxs-lookup"><span data-stu-id="c4635-103">IMAPISupport::Details</span></span>

  
  
<span data-ttu-id="c4635-104">**S’applique à** : Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="c4635-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="c4635-105">Affiche une boîte de dialogue qui affiche des détails sur une entrée de carnet d’adresses particulière.</span><span class="sxs-lookup"><span data-stu-id="c4635-105">Displays a dialog box that shows details about a particular address book entry.</span></span>
  
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

## <a name="parameters"></a><span data-ttu-id="c4635-106">Parameters</span><span class="sxs-lookup"><span data-stu-id="c4635-106">Parameters</span></span>

 <span data-ttu-id="c4635-107">_lpulUIParam_</span><span class="sxs-lookup"><span data-stu-id="c4635-107">_lpulUIParam_</span></span>
  
> <span data-ttu-id="c4635-108">[out] Pointeur vers la poignée vers la fenêtre parente de la boîte de dialogue renvoyée.</span><span class="sxs-lookup"><span data-stu-id="c4635-108">[out] A pointer to the handle to the parent window of the returned dialog box.</span></span>
    
 <span data-ttu-id="c4635-109">_lpfnDismiss_</span><span class="sxs-lookup"><span data-stu-id="c4635-109">_lpfnDismiss_</span></span>
  
> <span data-ttu-id="c4635-110">[in] Pointeur vers une fonction basée sur le prototype [DISMISSMODELESS](dismissmodeless.md) ou NULL.</span><span class="sxs-lookup"><span data-stu-id="c4635-110">[in] A pointer to a function based on the [DISMISSMODELESS](dismissmodeless.md) prototype, or NULL.</span></span> <span data-ttu-id="c4635-111">Ce membre s’applique uniquement à la version sans mode de la boîte de dialogue, comme indiqué par l’indicateur DIALOG_SDI en cours de mise en place.</span><span class="sxs-lookup"><span data-stu-id="c4635-111">This member applies only to the modeless version of the dialog box, as indicated by the DIALOG_SDI flag being set.</span></span> <span data-ttu-id="c4635-112">MAPI appelle la fonction **DISMISSMODELESS** lorsque l’utilisateur fait disparaître la boîte de dialogue d’adresses sans mode, informant un client qui appelle **IMAPISupport::D etails** que la boîte de dialogue n’est plus active.</span><span class="sxs-lookup"><span data-stu-id="c4635-112">MAPI calls the **DISMISSMODELESS** function when the user dismisses the modeless address dialog box, informing a client that is calling **IMAPISupport::Details** that the dialog box is no longer active.</span></span> 
    
 <span data-ttu-id="c4635-113">_lpvDismissContext_</span><span class="sxs-lookup"><span data-stu-id="c4635-113">_lpvDismissContext_</span></span>
  
> <span data-ttu-id="c4635-114">[in] Pointeur vers les informations de contexte à transmettre à la **fonction DISMISSMODELESS** pointée par le paramètre _lpfnDismiss._</span><span class="sxs-lookup"><span data-stu-id="c4635-114">[in] A pointer to context information to pass to the **DISMISSMODELESS** function pointed to by the  _lpfnDismiss_ parameter.</span></span> <span data-ttu-id="c4635-115">Ce paramètre s’applique uniquement à la version sans mode de la boîte de dialogue, en incluant l’indicateur DIALOG_SDI dans le _paramètre ulFlags._</span><span class="sxs-lookup"><span data-stu-id="c4635-115">This parameter applies only to the modeless version of the dialog box, by including the DIALOG_SDI flag in the  _ulFlags_ parameter.</span></span> 
    
 <span data-ttu-id="c4635-116">_cbEntryID_</span><span class="sxs-lookup"><span data-stu-id="c4635-116">_cbEntryID_</span></span>
  
> <span data-ttu-id="c4635-117">[in] Nombre d’bytes dans l’identificateur d’entrée pointé par _le paramètre lpEntryID._</span><span class="sxs-lookup"><span data-stu-id="c4635-117">[in] The byte count in the entry identifier pointed to by the  _lpEntryID_ parameter.</span></span> 
    
 <span data-ttu-id="c4635-118">_lpEntryID_</span><span class="sxs-lookup"><span data-stu-id="c4635-118">_lpEntryID_</span></span>
  
> <span data-ttu-id="c4635-119">[in] Pointeur vers l’identificateur d’entrée pour lequel les détails sont affichés.</span><span class="sxs-lookup"><span data-stu-id="c4635-119">[in] A pointer to the entry identifier for which details are displayed.</span></span>
    
 <span data-ttu-id="c4635-120">_lpfButtonCallback_</span><span class="sxs-lookup"><span data-stu-id="c4635-120">_lpfButtonCallback_</span></span>
  
> <span data-ttu-id="c4635-121">[in] Pointeur vers une fonction basée sur le prototype de fonction [LPFNBUTTON.](lpfnbutton.md)</span><span class="sxs-lookup"><span data-stu-id="c4635-121">[in] A pointer to a function based on the [LPFNBUTTON](lpfnbutton.md) function prototype.</span></span> <span data-ttu-id="c4635-122">Une **fonction LPFNBUTTON** ajoute un bouton à la boîte de dialogue Détails.</span><span class="sxs-lookup"><span data-stu-id="c4635-122">An **LPFNBUTTON** function adds a button to the details dialog box.</span></span> 
    
 <span data-ttu-id="c4635-123">_lpvButtonContext_</span><span class="sxs-lookup"><span data-stu-id="c4635-123">_lpvButtonContext_</span></span>
  
> <span data-ttu-id="c4635-124">[in] Pointeur vers des données utilisées comme paramètre pour la fonction spécifiée par le paramètre _lpfButtonCallback._</span><span class="sxs-lookup"><span data-stu-id="c4635-124">[in] A pointer to data used as a parameter for the function specified by the  _lpfButtonCallback_ parameter.</span></span> 
    
 <span data-ttu-id="c4635-125">_lpszButtonText_</span><span class="sxs-lookup"><span data-stu-id="c4635-125">_lpszButtonText_</span></span>
  
> <span data-ttu-id="c4635-126">[in] Pointeur vers une chaîne qui contient du texte à appliquer au bouton ajouté si ce bouton est extensible.</span><span class="sxs-lookup"><span data-stu-id="c4635-126">[in] A pointer to a string that contains text to be applied to the added button if that button is extensible.</span></span> <span data-ttu-id="c4635-127">Le  _paramètre lpszButtonText_ doit être NULL si un bouton extensible n’est pas nécessaire.</span><span class="sxs-lookup"><span data-stu-id="c4635-127">The  _lpszButtonText_ parameter should be NULL if an extensible button is not needed.</span></span> 
    
 <span data-ttu-id="c4635-128">_ulFlags_</span><span class="sxs-lookup"><span data-stu-id="c4635-128">_ulFlags_</span></span>
  
> <span data-ttu-id="c4635-129">[in] Masque de bits d’indicateurs qui contrôle le type du texte pour le _paramètre lpszButtonText._</span><span class="sxs-lookup"><span data-stu-id="c4635-129">[in] A bitmask of flags that controls the type of the text for the  _lpszButtonText_ parameter.</span></span> <span data-ttu-id="c4635-130">L’indicateur suivant peut être définie :</span><span class="sxs-lookup"><span data-stu-id="c4635-130">The following flag can be set:</span></span> 
    
<span data-ttu-id="c4635-131">DIALOG_MODAL</span><span class="sxs-lookup"><span data-stu-id="c4635-131">DIALOG_MODAL</span></span>
  
> <span data-ttu-id="c4635-132">Affiche la version modale de la boîte de dialogue d’adresse commune.</span><span class="sxs-lookup"><span data-stu-id="c4635-132">Display the modal version of the common address dialog box.</span></span> <span data-ttu-id="c4635-133">Cet indicateur s’exclue mutuellement avec DIALOG_SDI.</span><span class="sxs-lookup"><span data-stu-id="c4635-133">This flag is mutually exclusive with DIALOG_SDI.</span></span>
    
<span data-ttu-id="c4635-134">DIALOG_SDI</span><span class="sxs-lookup"><span data-stu-id="c4635-134">DIALOG_SDI</span></span>
  
>  <span data-ttu-id="c4635-135">Affiche la version non modée de la boîte de dialogue d’adresse commune.</span><span class="sxs-lookup"><span data-stu-id="c4635-135">Display the modeless version of the common address dialog box.</span></span> <span data-ttu-id="c4635-136">Cet indicateur s’exclue mutuellement avec DIALOG_MODAL.</span><span class="sxs-lookup"><span data-stu-id="c4635-136">This flag is mutually exclusive with DIALOG_MODAL.</span></span> 
    
<span data-ttu-id="c4635-137">MAPI_UNICODE</span><span class="sxs-lookup"><span data-stu-id="c4635-137">MAPI_UNICODE</span></span> 
  
> <span data-ttu-id="c4635-138">Les chaînes transmises sont au format Unicode.</span><span class="sxs-lookup"><span data-stu-id="c4635-138">The passed-in strings are in Unicode format.</span></span> <span data-ttu-id="c4635-139">Si l’MAPI_UNICODE n’est pas définie, les chaînes sont au format ANSI.</span><span class="sxs-lookup"><span data-stu-id="c4635-139">If the MAPI_UNICODE flag is not set, the strings are in ANSI format.</span></span>
    
## <a name="return-value"></a><span data-ttu-id="c4635-140">Valeur renvoyée</span><span class="sxs-lookup"><span data-stu-id="c4635-140">Return value</span></span>

<span data-ttu-id="c4635-141">S_OK</span><span class="sxs-lookup"><span data-stu-id="c4635-141">S_OK</span></span> 
  
> <span data-ttu-id="c4635-142">La boîte de dialogue Détails a été affichée avec succès pour l’entrée du carnet d’adresses.</span><span class="sxs-lookup"><span data-stu-id="c4635-142">The details dialog box was successfully displayed for the address book entry.</span></span>
    
## <a name="remarks"></a><span data-ttu-id="c4635-143">Remarques</span><span class="sxs-lookup"><span data-stu-id="c4635-143">Remarks</span></span>

<span data-ttu-id="c4635-144">La **méthode IMAPISupport::D etails** est implémentée pour les objets de prise en charge du fournisseur de carnet d’adresses.</span><span class="sxs-lookup"><span data-stu-id="c4635-144">The **IMAPISupport::Details** method is implemented for address book provider support objects.</span></span> <span data-ttu-id="c4635-145">Les fournisseurs de carnets d’adresses appellent **Details** pour afficher une boîte de dialogue qui fournit des détails sur une entrée particulière dans le carnet d’adresses.</span><span class="sxs-lookup"><span data-stu-id="c4635-145">Address book providers call **Details** to display a dialog box that gives details on a particular entry in the address book.</span></span> <span data-ttu-id="c4635-146">Les  _paramètres lpfButtonCallback,_  _lpvButtonContext_ et  _lpszButtonText_ peuvent être utilisés pour ajouter un bouton défini par le client à la boîte de dialogue.</span><span class="sxs-lookup"><span data-stu-id="c4635-146">The  _lpfButtonCallback_,  _lpvButtonContext_, and  _lpszButtonText_ parameters can be used to add a client-defined button to the dialog box.</span></span> <span data-ttu-id="c4635-147">Lorsque vous cliquez sur le bouton, MAPI appelle la fonction de rappel pointée par  _lpfButtonCallback_, en passant l’identificateur d’entrée du bouton et les données dans  _lpvButtonContext_.</span><span class="sxs-lookup"><span data-stu-id="c4635-147">When the button is clicked, MAPI calls the callback function pointed to by  _lpfButtonCallback_, passing both the entry identifier of the button and the data in  _lpvButtonContext_.</span></span> <span data-ttu-id="c4635-148">Si un bouton extensible n’est pas nécessaire,  _lpszButtonText_ doit être NULL.</span><span class="sxs-lookup"><span data-stu-id="c4635-148">If an extensible button is not needed,  _lpszButtonText_ should be NULL.</span></span> 
  
## <a name="see-also"></a><span data-ttu-id="c4635-149">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="c4635-149">See also</span></span>



[<span data-ttu-id="c4635-150">ADRPARM</span><span class="sxs-lookup"><span data-stu-id="c4635-150">ADRPARM</span></span>](adrparm.md)
  
[<span data-ttu-id="c4635-151">IMAPISupport::Address</span><span class="sxs-lookup"><span data-stu-id="c4635-151">IMAPISupport::Address</span></span>](imapisupport-address.md)
  
[<span data-ttu-id="c4635-152">LPFNBUTTON</span><span class="sxs-lookup"><span data-stu-id="c4635-152">LPFNBUTTON</span></span>](lpfnbutton.md)
  
[<span data-ttu-id="c4635-153">IMAPISupport : IUnknown</span><span class="sxs-lookup"><span data-stu-id="c4635-153">IMAPISupport : IUnknown</span></span>](imapisupportiunknown.md)

