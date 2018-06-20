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
description: 'Derni�re modification�: samedi 23 juillet 2011'
ms.openlocfilehash: 9923813d821e2b34497e3b498c19ce22ceda2eb0
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19783974"
---
# <a name="imapisupportdetails"></a><span data-ttu-id="e1ed0-103">IMAPISupport::Details</span><span class="sxs-lookup"><span data-stu-id="e1ed0-103">IMAPISupport::Details</span></span>

  
  
<span data-ttu-id="e1ed0-104">**S’applique à**: Outlook</span><span class="sxs-lookup"><span data-stu-id="e1ed0-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="e1ed0-105">Affiche une boîte de dialogue qui affiche des informations sur une entrée de carnet d’adresses particulière.</span><span class="sxs-lookup"><span data-stu-id="e1ed0-105">Displays a dialog box that shows details about a particular address book entry.</span></span>
  
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

## <a name="parameters"></a><span data-ttu-id="e1ed0-106">Paramètres</span><span class="sxs-lookup"><span data-stu-id="e1ed0-106">Parameters</span></span>

 <span data-ttu-id="e1ed0-107">_lpulUIParam_</span><span class="sxs-lookup"><span data-stu-id="e1ed0-107">_lpulUIParam_</span></span>
  
> <span data-ttu-id="e1ed0-108">[out] Pointeur vers le handle vers la fenêtre parent de la boîte de dialogue renvoyée.</span><span class="sxs-lookup"><span data-stu-id="e1ed0-108">[out] A pointer to the handle to the parent window of the returned dialog box.</span></span>
    
 <span data-ttu-id="e1ed0-109">_lpfnDismiss_</span><span class="sxs-lookup"><span data-stu-id="e1ed0-109">_lpfnDismiss_</span></span>
  
> <span data-ttu-id="e1ed0-110">[in] Pointeur vers une fonction basée sur le prototype [DISMISSMODELESS](dismissmodeless.md) ou NULL.</span><span class="sxs-lookup"><span data-stu-id="e1ed0-110">[in] A pointer to a function based on the [DISMISSMODELESS](dismissmodeless.md) prototype, or NULL.</span></span> <span data-ttu-id="e1ed0-111">Ce membre s’applique uniquement à la version de la boîte de dialogue non modale, telle qu’indiquée par l’indicateur DIALOG_SDI en cours.</span><span class="sxs-lookup"><span data-stu-id="e1ed0-111">This member applies only to the modeless version of the dialog box, as indicated by the DIALOG_SDI flag being set.</span></span> <span data-ttu-id="e1ed0-112">MAPI appelle la fonction **DISMISSMODELESS** lorsque l’utilisateur ferme la boîte de dialogue non modale adresse informant le client qui appelle **IMAPISupport::Details** que la boîte de dialogue n’est plus active.</span><span class="sxs-lookup"><span data-stu-id="e1ed0-112">MAPI calls the **DISMISSMODELESS** function when the user dismisses the modeless address dialog box, informing a client that is calling **IMAPISupport::Details** that the dialog box is no longer active.</span></span> 
    
 <span data-ttu-id="e1ed0-113">_lpvDismissContext_</span><span class="sxs-lookup"><span data-stu-id="e1ed0-113">_lpvDismissContext_</span></span>
  
> <span data-ttu-id="e1ed0-114">[in] Un pointeur vers les informations de contexte à transmettre à la fonction **DISMISSMODELESS** indiqué par le paramètre _lpfnDismiss_ .</span><span class="sxs-lookup"><span data-stu-id="e1ed0-114">[in] A pointer to context information to pass to the **DISMISSMODELESS** function pointed to by the  _lpfnDismiss_ parameter.</span></span> <span data-ttu-id="e1ed0-115">Ce paramètre s’applique uniquement à la version de la boîte de dialogue non modale en incluant l’indicateur DIALOG_SDI dans le paramètre _ulFlags_ .</span><span class="sxs-lookup"><span data-stu-id="e1ed0-115">This parameter applies only to the modeless version of the dialog box, by including the DIALOG_SDI flag in the  _ulFlags_ parameter.</span></span> 
    
 <span data-ttu-id="e1ed0-116">_cbEntryID_</span><span class="sxs-lookup"><span data-stu-id="e1ed0-116">_cbEntryID_</span></span>
  
> <span data-ttu-id="e1ed0-117">[in] Le nombre d’octets dans l’identificateur d’entrée indiqué par le paramètre _lpEntryID_ .</span><span class="sxs-lookup"><span data-stu-id="e1ed0-117">[in] The byte count in the entry identifier pointed to by the  _lpEntryID_ parameter.</span></span> 
    
 <span data-ttu-id="e1ed0-118">_lpEntryID_</span><span class="sxs-lookup"><span data-stu-id="e1ed0-118">_lpEntryID_</span></span>
  
> <span data-ttu-id="e1ed0-119">[in] Pointeur vers l’identificateur d’entrée pour lesquels les détails sont affichés.</span><span class="sxs-lookup"><span data-stu-id="e1ed0-119">[in] A pointer to the entry identifier for which details are displayed.</span></span>
    
 <span data-ttu-id="e1ed0-120">_lpfButtonCallback_</span><span class="sxs-lookup"><span data-stu-id="e1ed0-120">_lpfButtonCallback_</span></span>
  
> <span data-ttu-id="e1ed0-121">[in] Pointeur vers une fonction basée sur le prototype de fonction [LPFNBUTTON](lpfnbutton.md) .</span><span class="sxs-lookup"><span data-stu-id="e1ed0-121">[in] A pointer to a function based on the [LPFNBUTTON](lpfnbutton.md) function prototype.</span></span> <span data-ttu-id="e1ed0-122">Une fonction **LPFNBUTTON** ajoute un bouton à la boîte de dialogue Détails.</span><span class="sxs-lookup"><span data-stu-id="e1ed0-122">An **LPFNBUTTON** function adds a button to the details dialog box.</span></span> 
    
 <span data-ttu-id="e1ed0-123">_lpvButtonContext_</span><span class="sxs-lookup"><span data-stu-id="e1ed0-123">_lpvButtonContext_</span></span>
  
> <span data-ttu-id="e1ed0-124">[in] Pointeur vers les données utilisées en tant que paramètre pour la fonction spécifiée par le paramètre _lpfButtonCallback_ .</span><span class="sxs-lookup"><span data-stu-id="e1ed0-124">[in] A pointer to data used as a parameter for the function specified by the  _lpfButtonCallback_ parameter.</span></span> 
    
 <span data-ttu-id="e1ed0-125">_lpszButtonText_</span><span class="sxs-lookup"><span data-stu-id="e1ed0-125">_lpszButtonText_</span></span>
  
> <span data-ttu-id="e1ed0-126">[in] Pointeur vers une chaîne qui contient du texte peut être appliqué au bouton Ajout si ce bouton est extensible.</span><span class="sxs-lookup"><span data-stu-id="e1ed0-126">[in] A pointer to a string that contains text to be applied to the added button if that button is extensible.</span></span> <span data-ttu-id="e1ed0-127">Le paramètre _lpszButtonText_ doit être NULL si un bouton extensible n’est pas nécessaire.</span><span class="sxs-lookup"><span data-stu-id="e1ed0-127">The  _lpszButtonText_ parameter should be NULL if an extensible button is not needed.</span></span> 
    
 <span data-ttu-id="e1ed0-128">_ulFlags_</span><span class="sxs-lookup"><span data-stu-id="e1ed0-128">_ulFlags_</span></span>
  
> <span data-ttu-id="e1ed0-129">[in] Masque de bits d’indicateurs qui contrôle le type du texte pour le paramètre _lpszButtonText_ .</span><span class="sxs-lookup"><span data-stu-id="e1ed0-129">[in] A bitmask of flags that controls the type of the text for the  _lpszButtonText_ parameter.</span></span> <span data-ttu-id="e1ed0-130">Vous pouvez définir l’indicateur suivant :</span><span class="sxs-lookup"><span data-stu-id="e1ed0-130">The following flag can be set:</span></span> 
    
<span data-ttu-id="e1ed0-131">DIALOG_MODAL</span><span class="sxs-lookup"><span data-stu-id="e1ed0-131">DIALOG_MODAL</span></span>
  
> <span data-ttu-id="e1ed0-132">Afficher la version de la boîte de dialogue adresse modale.</span><span class="sxs-lookup"><span data-stu-id="e1ed0-132">Display the modal version of the common address dialog box.</span></span> <span data-ttu-id="e1ed0-133">Cet indicateur est mutuellement exclusif avec DIALOG_SDI.</span><span class="sxs-lookup"><span data-stu-id="e1ed0-133">This flag is mutually exclusive with DIALOG_SDI.</span></span>
    
<span data-ttu-id="e1ed0-134">DIALOG_SDI</span><span class="sxs-lookup"><span data-stu-id="e1ed0-134">DIALOG_SDI</span></span>
  
>  <span data-ttu-id="e1ed0-135">Afficher la version de la boîte de dialogue adresse non modale.</span><span class="sxs-lookup"><span data-stu-id="e1ed0-135">Display the modeless version of the common address dialog box.</span></span> <span data-ttu-id="e1ed0-136">Cet indicateur est mutuellement exclusif avec DIALOG_MODAL.</span><span class="sxs-lookup"><span data-stu-id="e1ed0-136">This flag is mutually exclusive with DIALOG_MODAL.</span></span> 
    
<span data-ttu-id="e1ed0-137">MAPI_UNICODE</span><span class="sxs-lookup"><span data-stu-id="e1ed0-137">MAPI_UNICODE</span></span> 
  
> <span data-ttu-id="e1ed0-138">Les chaînes passée sont au format Unicode.</span><span class="sxs-lookup"><span data-stu-id="e1ed0-138">The passed-in strings are in Unicode format.</span></span> <span data-ttu-id="e1ed0-139">Si l’indicateur MAPI_UNICODE n’est pas définie, les chaînes sont au format ANSI.</span><span class="sxs-lookup"><span data-stu-id="e1ed0-139">If the MAPI_UNICODE flag is not set, the strings are in ANSI format.</span></span>
    
## <a name="return-value"></a><span data-ttu-id="e1ed0-140">Valeur renvoy�e</span><span class="sxs-lookup"><span data-stu-id="e1ed0-140">Return value</span></span>

<span data-ttu-id="e1ed0-141">S_OK</span><span class="sxs-lookup"><span data-stu-id="e1ed0-141">S_OK</span></span> 
  
> <span data-ttu-id="e1ed0-142">La boîte de dialogue a été correctement affichée pour l’entrée du carnet d’adresses.</span><span class="sxs-lookup"><span data-stu-id="e1ed0-142">The details dialog box was successfully displayed for the address book entry.</span></span>
    
## <a name="remarks"></a><span data-ttu-id="e1ed0-143">Remarques</span><span class="sxs-lookup"><span data-stu-id="e1ed0-143">Remarks</span></span>

<span data-ttu-id="e1ed0-144">La méthode **IMAPISupport::Details** est implémentée pour les objets de prise en charge du fournisseur adresse téléchargeable.</span><span class="sxs-lookup"><span data-stu-id="e1ed0-144">The **IMAPISupport::Details** method is implemented for address book provider support objects.</span></span> <span data-ttu-id="e1ed0-145">Fournisseurs de carnet d’adresses appeler **Détails** pour afficher une boîte de dialogue qui donne des détails sur une entrée particulière dans le carnet d’adresses.</span><span class="sxs-lookup"><span data-stu-id="e1ed0-145">Address book providers call **Details** to display a dialog box that gives details on a particular entry in the address book.</span></span> <span data-ttu-id="e1ed0-146">Les paramètres _lpfButtonCallback_, _lpvButtonContext_et _lpszButtonText_ peuvent être utilisés pour ajouter un bouton défini par le client à la boîte de dialogue.</span><span class="sxs-lookup"><span data-stu-id="e1ed0-146">The  _lpfButtonCallback_,  _lpvButtonContext_, and  _lpszButtonText_ parameters can be used to add a client-defined button to the dialog box.</span></span> <span data-ttu-id="e1ed0-147">Lorsque le bouton est activé, MAPI appelle la fonction de rappel désignée par _lpfButtonCallback_, en passant l’identificateur de l’entrée du bouton et les données _lpvButtonContext_.</span><span class="sxs-lookup"><span data-stu-id="e1ed0-147">When the button is clicked, MAPI calls the callback function pointed to by  _lpfButtonCallback_, passing both the entry identifier of the button and the data in  _lpvButtonContext_.</span></span> <span data-ttu-id="e1ed0-148">Si un bouton extensible n’est pas nécessaire, _lpszButtonText_ doit être NULL.</span><span class="sxs-lookup"><span data-stu-id="e1ed0-148">If an extensible button is not needed,  _lpszButtonText_ should be NULL.</span></span> 
  
## <a name="see-also"></a><span data-ttu-id="e1ed0-149">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="e1ed0-149">See also</span></span>



[<span data-ttu-id="e1ed0-150">ADRPARM</span><span class="sxs-lookup"><span data-stu-id="e1ed0-150">ADRPARM</span></span>](adrparm.md)
  
[<span data-ttu-id="e1ed0-151">IMAPISupport::Address</span><span class="sxs-lookup"><span data-stu-id="e1ed0-151">IMAPISupport::Address</span></span>](imapisupport-address.md)
  
[<span data-ttu-id="e1ed0-152">LPFNBUTTON</span><span class="sxs-lookup"><span data-stu-id="e1ed0-152">LPFNBUTTON</span></span>](lpfnbutton.md)
  
[<span data-ttu-id="e1ed0-153">IMAPISupport : IUnknown</span><span class="sxs-lookup"><span data-stu-id="e1ed0-153">IMAPISupport : IUnknown</span></span>](imapisupportiunknown.md)

