---
title: IAddrBookDetails
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- IAddrBook.Details
api_type:
- COM
ms.assetid: 4eee4382-98c3-4714-8920-8d72edef00b8
description: Dernière modification le 9 mars 2015
ms.openlocfilehash: 5fbd20a6b5d5598b8fa51f9c369eefac9a1ea2e9
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/28/2019
ms.locfileid: "33424678"
---
# <a name="iaddrbookdetails"></a><span data-ttu-id="ec280-103">IAddrBook::Details</span><span class="sxs-lookup"><span data-stu-id="ec280-103">IAddrBook::Details</span></span>

  
  
<span data-ttu-id="ec280-104">**S’applique à** : Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="ec280-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="ec280-105">Affiche une boîte de dialogue qui affiche des détails sur une entrée de carnet d’adresses particulière.</span><span class="sxs-lookup"><span data-stu-id="ec280-105">Displays a dialog box that shows details about a particular address book entry.</span></span>
  
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

## <a name="parameters"></a><span data-ttu-id="ec280-106">Parameters</span><span class="sxs-lookup"><span data-stu-id="ec280-106">Parameters</span></span>

 <span data-ttu-id="ec280-107">_lpulUIParam_</span><span class="sxs-lookup"><span data-stu-id="ec280-107">_lpulUIParam_</span></span>
  
> <span data-ttu-id="ec280-108">[in] Pointeur vers un handle de la fenêtre parente de la boîte de dialogue.</span><span class="sxs-lookup"><span data-stu-id="ec280-108">[in] A pointer to a handle of the parent window for the dialog box.</span></span>
    
 <span data-ttu-id="ec280-109">_lpfnDismiss_</span><span class="sxs-lookup"><span data-stu-id="ec280-109">_lpfnDismiss_</span></span>
  
> <span data-ttu-id="ec280-110">[in] Pointeur vers une fonction basée sur le prototype [DISMISSMODELESS](dismissmodeless.md) ou NULL.</span><span class="sxs-lookup"><span data-stu-id="ec280-110">[in] A pointer to a function based on the [DISMISSMODELESS](dismissmodeless.md) prototype, or NULL.</span></span> <span data-ttu-id="ec280-111">Ce membre s’applique uniquement à la version sans mode de la boîte de dialogue, comme indiqué par l’indicateur DIALOG_SDI en cours de mise en place.</span><span class="sxs-lookup"><span data-stu-id="ec280-111">This member applies only to the modeless version of the dialog box, as indicated by the DIALOG_SDI flag being set.</span></span> <span data-ttu-id="ec280-112">MAPI appelle la **fonction DISMISSMODELESS** lorsque l’utilisateur fait disparaître la boîte de dialogue d’adresses sans mode, informant un client qui appelle **Details** que la boîte de dialogue n’est plus active.</span><span class="sxs-lookup"><span data-stu-id="ec280-112">MAPI calls the **DISMISSMODELESS** function when the user dismisses the modeless address dialog box, informing a client that is calling **Details** that the dialog box is no longer active.</span></span> 
    
 <span data-ttu-id="ec280-113">_lpvDismissContext_</span><span class="sxs-lookup"><span data-stu-id="ec280-113">_lpvDismissContext_</span></span>
  
> <span data-ttu-id="ec280-114">[in] Pointeur vers les informations de contexte à transmettre à la **fonction DISMISSMODELESS** pointée par le paramètre _lpfnDismiss._</span><span class="sxs-lookup"><span data-stu-id="ec280-114">[in] A pointer to context information to pass to the **DISMISSMODELESS** function pointed to by the  _lpfnDismiss_ parameter.</span></span> <span data-ttu-id="ec280-115">Ce paramètre s’applique uniquement à la version sans mode de la boîte de dialogue, en incluant l’indicateur DIALOG_SDI dans le _paramètre ulFlags._</span><span class="sxs-lookup"><span data-stu-id="ec280-115">This parameter applies only to the modeless version of the dialog box, by including the DIALOG_SDI flag in the  _ulFlags_ parameter.</span></span> 
    
 <span data-ttu-id="ec280-116">_cbEntryID_</span><span class="sxs-lookup"><span data-stu-id="ec280-116">_cbEntryID_</span></span>
  
> <span data-ttu-id="ec280-117">[in] Nombre d’bytes dans l’identificateur d’entrée pointé par _le paramètre lpEntryID._</span><span class="sxs-lookup"><span data-stu-id="ec280-117">[in] The byte count in the entry identifier pointed to by the  _lpEntryID_ parameter.</span></span> 
    
 <span data-ttu-id="ec280-118">_lpEntryID_</span><span class="sxs-lookup"><span data-stu-id="ec280-118">_lpEntryID_</span></span>
  
> <span data-ttu-id="ec280-119">[in] Pointeur vers l’identificateur d’entrée pour lequel les détails sont affichés.</span><span class="sxs-lookup"><span data-stu-id="ec280-119">[in] A pointer to the entry identifier for the entry for which details are displayed.</span></span>
    
 <span data-ttu-id="ec280-120">_lpfButtonCallback_</span><span class="sxs-lookup"><span data-stu-id="ec280-120">_lpfButtonCallback_</span></span>
  
> <span data-ttu-id="ec280-121">[in] Pointeur vers une fonction basée sur le prototype de fonction [LPFNBUTTON.](lpfnbutton.md)</span><span class="sxs-lookup"><span data-stu-id="ec280-121">[in] A pointer to a function based on the [LPFNBUTTON](lpfnbutton.md) function prototype.</span></span> <span data-ttu-id="ec280-122">Une **fonction LPFNBUTTON** ajoute un bouton à la boîte de dialogue Détails.</span><span class="sxs-lookup"><span data-stu-id="ec280-122">An **LPFNBUTTON** function adds a button to the details dialog box.</span></span> 
    
 <span data-ttu-id="ec280-123">_lpvButtonContext_</span><span class="sxs-lookup"><span data-stu-id="ec280-123">_lpvButtonContext_</span></span>
  
> <span data-ttu-id="ec280-124">[in] Pointeur vers des données qui a été utilisé comme paramètre pour la fonction spécifiée par le _paramètre lpfButtonCallback._</span><span class="sxs-lookup"><span data-stu-id="ec280-124">[in] A pointer to data that was used as a parameter for the function specified by the  _lpfButtonCallback_ parameter.</span></span> 
    
 <span data-ttu-id="ec280-125">_lpszButtonText_</span><span class="sxs-lookup"><span data-stu-id="ec280-125">_lpszButtonText_</span></span>
  
> <span data-ttu-id="ec280-126">[in] Pointeur vers une chaîne qui contient du texte à appliquer au bouton ajouté, si ce bouton est extensible.</span><span class="sxs-lookup"><span data-stu-id="ec280-126">[in] A pointer to a string that contains text to be applied to the added button, if that button is extensible.</span></span> <span data-ttu-id="ec280-127">Le  _paramètre lpszButtonText_ doit être NULL si vous n’avez pas besoin d’un bouton extensible.</span><span class="sxs-lookup"><span data-stu-id="ec280-127">The  _lpszButtonText_ parameter should be NULL if you do not need an extensible button.</span></span> 
    
 <span data-ttu-id="ec280-128">_ulFlags_</span><span class="sxs-lookup"><span data-stu-id="ec280-128">_ulFlags_</span></span>
  
> <span data-ttu-id="ec280-129">[in] Masque de bits d’indicateurs qui contrôle le type du texte pour le _paramètre lpszButtonText._</span><span class="sxs-lookup"><span data-stu-id="ec280-129">[in] A bitmask of flags that controls the type of the text for the  _lpszButtonText_ parameter.</span></span> <span data-ttu-id="ec280-130">Les indicateurs suivants peuvent être définies :</span><span class="sxs-lookup"><span data-stu-id="ec280-130">The following flags can be set:</span></span> 
    
<span data-ttu-id="ec280-131">AB_TELL_DETAILS_CHANGE</span><span class="sxs-lookup"><span data-stu-id="ec280-131">AB_TELL_DETAILS_CHANGE</span></span>
  
> <span data-ttu-id="ec280-132">Indique que **les détails renvoient** S_OK si des modifications sont réellement apportées à l’adresse ; Dans le **cas contraire, details** renvoie S_FALSE.</span><span class="sxs-lookup"><span data-stu-id="ec280-132">Indicates that **Details** returns S_OK if changes are actually made to the address; otherwise, **Details** returns S_FALSE.</span></span> 
    
<span data-ttu-id="ec280-133">DIALOG_MODAL</span><span class="sxs-lookup"><span data-stu-id="ec280-133">DIALOG_MODAL</span></span>
  
> <span data-ttu-id="ec280-134">Affichez la version modale de la boîte de dialogue d’adresses commune, qui est toujours affichée dans les clients Outlook courants.</span><span class="sxs-lookup"><span data-stu-id="ec280-134">Display the modal version of the common address dialog box, which is always shown in non-Outlook clients.</span></span> <span data-ttu-id="ec280-135">Cet indicateur s’exclue mutuellement avec DIALOG_SDI.</span><span class="sxs-lookup"><span data-stu-id="ec280-135">This flag is mutually exclusive with DIALOG_SDI.</span></span>
    
<span data-ttu-id="ec280-136">DIALOG_SDI</span><span class="sxs-lookup"><span data-stu-id="ec280-136">DIALOG_SDI</span></span>
  
>  <span data-ttu-id="ec280-137">Affiche la version non modée de la boîte de dialogue d’adresse commune.</span><span class="sxs-lookup"><span data-stu-id="ec280-137">Display the modeless version of the common address dialog box.</span></span> <span data-ttu-id="ec280-138">Cet indicateur est ignoré pour les clients non Outlook client.</span><span class="sxs-lookup"><span data-stu-id="ec280-138">This flag is ignored for non-Outlook clients.</span></span> 
    
<span data-ttu-id="ec280-139">MAPI_UNICODE</span><span class="sxs-lookup"><span data-stu-id="ec280-139">MAPI_UNICODE</span></span> 
  
> <span data-ttu-id="ec280-140">Les chaînes transmises sont au format Unicode.</span><span class="sxs-lookup"><span data-stu-id="ec280-140">The passed-in strings are in Unicode format.</span></span> <span data-ttu-id="ec280-141">Si l’MAPI_UNICODE n’est pas définie, les chaînes sont au format ANSI.</span><span class="sxs-lookup"><span data-stu-id="ec280-141">If the MAPI_UNICODE flag is not set, the strings are in ANSI format.</span></span>
    
## <a name="return-value"></a><span data-ttu-id="ec280-142">Valeur renvoyée</span><span class="sxs-lookup"><span data-stu-id="ec280-142">Return value</span></span>

<span data-ttu-id="ec280-143">S_OK</span><span class="sxs-lookup"><span data-stu-id="ec280-143">S_OK</span></span> 
  
> <span data-ttu-id="ec280-144">La boîte de dialogue Détails a été affichée avec succès pour l’entrée du carnet d’adresses.</span><span class="sxs-lookup"><span data-stu-id="ec280-144">The details dialog box was successfully displayed for the address book entry.</span></span>
    
## <a name="remarks"></a><span data-ttu-id="ec280-145">Remarques</span><span class="sxs-lookup"><span data-stu-id="ec280-145">Remarks</span></span>

<span data-ttu-id="ec280-146">Les applications clientes **appellent la méthode Details** pour afficher une boîte de dialogue qui fournit des détails sur une entrée particulière dans le carnet d’adresses.</span><span class="sxs-lookup"><span data-stu-id="ec280-146">Client applications call the **Details** method to display a dialog box that provides details about a particular entry in the address book.</span></span> <span data-ttu-id="ec280-147">Vous pouvez utiliser les paramètres  _lpfButtonCallback,_  _lpvButtonContext_ et  _lpszButtonText_ pour ajouter un bouton défini par le client à la boîte de dialogue.</span><span class="sxs-lookup"><span data-stu-id="ec280-147">You can use the  _lpfButtonCallback_,  _lpvButtonContext_, and  _lpszButtonText_ parameters to add a client-defined button to the dialog box.</span></span> <span data-ttu-id="ec280-148">Lorsque vous cliquez sur le bouton, MAPI appelle la fonction de rappel pointée par  _lpfButtonCallback_, en passant l’identificateur d’entrée du bouton et les données dans  _lpvButtonContext_.</span><span class="sxs-lookup"><span data-stu-id="ec280-148">When the button is clicked, MAPI calls the callback function pointed to by  _lpfButtonCallback_, passing both the entry identifier of the button and the data in  _lpvButtonContext_.</span></span> <span data-ttu-id="ec280-149">Si vous n’avez pas besoin d’un bouton extensible,  _lpszButtonText_ doit être NULL.</span><span class="sxs-lookup"><span data-stu-id="ec280-149">If you do not need an extensible button,  _lpszButtonText_ should be NULL.</span></span> 
  
 <span data-ttu-id="ec280-150">**Les détails prend** en charge les chaînes de caractères Unicode ; Les chaînes Unicode sont converties au format de chaîne de caractères multioctets (MBCS) avant d’être affichées dans la boîte de dialogue d’informations.</span><span class="sxs-lookup"><span data-stu-id="ec280-150">**Details** supports Unicode character strings; Unicode strings are converted to the multibyte character string (MBCS) format before they are displayed in the details dialog box.</span></span> 
  
## <a name="mfcmapi-reference"></a><span data-ttu-id="ec280-151">Référence MFCMAPI</span><span class="sxs-lookup"><span data-stu-id="ec280-151">MFCMAPI reference</span></span>

<span data-ttu-id="ec280-152">Pour voir un exemple de code MFCMAPI, consultez le tableau suivant.</span><span class="sxs-lookup"><span data-stu-id="ec280-152">For MFCMAPI sample code, see the following table.</span></span>
  
|<span data-ttu-id="ec280-153">**Fichier**</span><span class="sxs-lookup"><span data-stu-id="ec280-153">**File**</span></span>|<span data-ttu-id="ec280-154">**Fonction**</span><span class="sxs-lookup"><span data-stu-id="ec280-154">**Function**</span></span>|<span data-ttu-id="ec280-155">**Commentaire**</span><span class="sxs-lookup"><span data-stu-id="ec280-155">**Comment**</span></span>|
|:-----|:-----|:-----|
|<span data-ttu-id="ec280-156">BaseDialog.cpp</span><span class="sxs-lookup"><span data-stu-id="ec280-156">BaseDialog.cpp</span></span>  <br/> |<span data-ttu-id="ec280-157">CBaseDialog::OnOpenEntryID</span><span class="sxs-lookup"><span data-stu-id="ec280-157">CBaseDialog::OnOpenEntryID</span></span>  <br/> |<span data-ttu-id="ec280-158">MFCMAPI utilise la **méthode Details** pour afficher une boîte de dialogue qui affiche les détails d’une entrée de carnet d’adresses.</span><span class="sxs-lookup"><span data-stu-id="ec280-158">MFCMAPI uses the **Details** method to display a dialog box that shows the details for an address book entry.</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="ec280-159">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="ec280-159">See also</span></span>



[<span data-ttu-id="ec280-160">ADRPARM</span><span class="sxs-lookup"><span data-stu-id="ec280-160">ADRPARM</span></span>](adrparm.md)
  
[<span data-ttu-id="ec280-161">IAddrBook::Address</span><span class="sxs-lookup"><span data-stu-id="ec280-161">IAddrBook::Address</span></span>](iaddrbook-address.md)
  
[<span data-ttu-id="ec280-162">LPFNBUTTON</span><span class="sxs-lookup"><span data-stu-id="ec280-162">LPFNBUTTON</span></span>](lpfnbutton.md)
  
[<span data-ttu-id="ec280-163">IAddrBook : IMAPIProp</span><span class="sxs-lookup"><span data-stu-id="ec280-163">IAddrBook : IMAPIProp</span></span>](iaddrbookimapiprop.md)


[<span data-ttu-id="ec280-164">MFCMAPI comme un exemple de Code</span><span class="sxs-lookup"><span data-stu-id="ec280-164">MFCMAPI as a Code Sample</span></span>](mfcmapi-as-a-code-sample.md)

