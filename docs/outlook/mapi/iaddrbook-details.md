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
description: 'Derni�re modification�: lundi 9 mars 2015'
ms.openlocfilehash: fbe7f02555f76532896c951f50648c528c250a58
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19783636"
---
# <a name="iaddrbookdetails"></a><span data-ttu-id="9e781-103">IAddrBook::Details</span><span class="sxs-lookup"><span data-stu-id="9e781-103">IAddrBook::Details</span></span>

  
  
<span data-ttu-id="9e781-104">**S’applique à**: Outlook</span><span class="sxs-lookup"><span data-stu-id="9e781-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="9e781-105">Affiche une boîte de dialogue qui affiche des informations sur une entrée de carnet d’adresses particulière.</span><span class="sxs-lookup"><span data-stu-id="9e781-105">Displays a dialog box that shows details about a particular address book entry.</span></span>
  
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

## <a name="parameters"></a><span data-ttu-id="9e781-106">Paramètres</span><span class="sxs-lookup"><span data-stu-id="9e781-106">Parameters</span></span>

 <span data-ttu-id="9e781-107">_lpulUIParam_</span><span class="sxs-lookup"><span data-stu-id="9e781-107">_lpulUIParam_</span></span>
  
> <span data-ttu-id="9e781-108">[in] Pointeur vers un handle de fenêtre parente de la boîte de dialogue.</span><span class="sxs-lookup"><span data-stu-id="9e781-108">[in] A pointer to a handle of the parent window for the dialog box.</span></span>
    
 <span data-ttu-id="9e781-109">_lpfnDismiss_</span><span class="sxs-lookup"><span data-stu-id="9e781-109">_lpfnDismiss_</span></span>
  
> <span data-ttu-id="9e781-110">[in] Pointeur vers une fonction basée sur le prototype [DISMISSMODELESS](dismissmodeless.md) ou NULL.</span><span class="sxs-lookup"><span data-stu-id="9e781-110">[in] A pointer to a function based on the [DISMISSMODELESS](dismissmodeless.md) prototype, or NULL.</span></span> <span data-ttu-id="9e781-111">Ce membre s’applique uniquement à la version de la boîte de dialogue non modale, telle qu’indiquée par l’indicateur DIALOG_SDI en cours.</span><span class="sxs-lookup"><span data-stu-id="9e781-111">This member applies only to the modeless version of the dialog box, as indicated by the DIALOG_SDI flag being set.</span></span> <span data-ttu-id="9e781-112">MAPI appelle la fonction **DISMISSMODELESS** lorsque l’utilisateur ferme la boîte de dialogue non modale adresse informant le client qui appelle **plus d’informations** que la boîte de dialogue n’est plus active.</span><span class="sxs-lookup"><span data-stu-id="9e781-112">MAPI calls the **DISMISSMODELESS** function when the user dismisses the modeless address dialog box, informing a client that is calling **Details** that the dialog box is no longer active.</span></span> 
    
 <span data-ttu-id="9e781-113">_lpvDismissContext_</span><span class="sxs-lookup"><span data-stu-id="9e781-113">_lpvDismissContext_</span></span>
  
> <span data-ttu-id="9e781-114">[in] Un pointeur vers les informations de contexte à transmettre à la fonction **DISMISSMODELESS** indiqué par le paramètre _lpfnDismiss_ .</span><span class="sxs-lookup"><span data-stu-id="9e781-114">[in] A pointer to context information to pass to the **DISMISSMODELESS** function pointed to by the  _lpfnDismiss_ parameter.</span></span> <span data-ttu-id="9e781-115">Ce paramètre s’applique uniquement à la version de la boîte de dialogue non modale en incluant l’indicateur DIALOG_SDI dans le paramètre _ulFlags_ .</span><span class="sxs-lookup"><span data-stu-id="9e781-115">This parameter applies only to the modeless version of the dialog box, by including the DIALOG_SDI flag in the  _ulFlags_ parameter.</span></span> 
    
 <span data-ttu-id="9e781-116">_cbEntryID_</span><span class="sxs-lookup"><span data-stu-id="9e781-116">_cbEntryID_</span></span>
  
> <span data-ttu-id="9e781-117">[in] Le nombre d’octets dans l’identificateur d’entrée indiqué par le paramètre _lpEntryID_ .</span><span class="sxs-lookup"><span data-stu-id="9e781-117">[in] The byte count in the entry identifier pointed to by the  _lpEntryID_ parameter.</span></span> 
    
 <span data-ttu-id="9e781-118">_lpEntryID_</span><span class="sxs-lookup"><span data-stu-id="9e781-118">_lpEntryID_</span></span>
  
> <span data-ttu-id="9e781-119">[in] Pointeur vers l’identificateur d’entrée pour l’entrée pour laquelle les détails sont affichés.</span><span class="sxs-lookup"><span data-stu-id="9e781-119">[in] A pointer to the entry identifier for the entry for which details are displayed.</span></span>
    
 <span data-ttu-id="9e781-120">_lpfButtonCallback_</span><span class="sxs-lookup"><span data-stu-id="9e781-120">_lpfButtonCallback_</span></span>
  
> <span data-ttu-id="9e781-121">[in] Pointeur vers une fonction basée sur le prototype de fonction [LPFNBUTTON](lpfnbutton.md) .</span><span class="sxs-lookup"><span data-stu-id="9e781-121">[in] A pointer to a function based on the [LPFNBUTTON](lpfnbutton.md) function prototype.</span></span> <span data-ttu-id="9e781-122">Une fonction **LPFNBUTTON** ajoute un bouton à la boîte de dialogue Détails.</span><span class="sxs-lookup"><span data-stu-id="9e781-122">An **LPFNBUTTON** function adds a button to the details dialog box.</span></span> 
    
 <span data-ttu-id="9e781-123">_lpvButtonContext_</span><span class="sxs-lookup"><span data-stu-id="9e781-123">_lpvButtonContext_</span></span>
  
> <span data-ttu-id="9e781-124">[in] Pointeur vers les données qui a été utilisés en tant que paramètre pour la fonction spécifiée par le paramètre _lpfButtonCallback_ .</span><span class="sxs-lookup"><span data-stu-id="9e781-124">[in] A pointer to data that was used as a parameter for the function specified by the  _lpfButtonCallback_ parameter.</span></span> 
    
 <span data-ttu-id="9e781-125">_lpszButtonText_</span><span class="sxs-lookup"><span data-stu-id="9e781-125">_lpszButtonText_</span></span>
  
> <span data-ttu-id="9e781-126">[in] Pointeur vers une chaîne qui contient du texte à appliquer au bouton ajouté, si ce bouton est extensible.</span><span class="sxs-lookup"><span data-stu-id="9e781-126">[in] A pointer to a string that contains text to be applied to the added button, if that button is extensible.</span></span> <span data-ttu-id="9e781-127">Le paramètre _lpszButtonText_ doit être NULL si vous n’avez pas besoin d’un bouton extensible.</span><span class="sxs-lookup"><span data-stu-id="9e781-127">The  _lpszButtonText_ parameter should be NULL if you do not need an extensible button.</span></span> 
    
 <span data-ttu-id="9e781-128">_ulFlags_</span><span class="sxs-lookup"><span data-stu-id="9e781-128">_ulFlags_</span></span>
  
> <span data-ttu-id="9e781-129">[in] Masque de bits d’indicateurs qui contrôle le type du texte pour le paramètre _lpszButtonText_ .</span><span class="sxs-lookup"><span data-stu-id="9e781-129">[in] A bitmask of flags that controls the type of the text for the  _lpszButtonText_ parameter.</span></span> <span data-ttu-id="9e781-130">Les indicateurs suivants peuvent être définis :</span><span class="sxs-lookup"><span data-stu-id="9e781-130">The following flags can be set:</span></span> 
    
<span data-ttu-id="9e781-131">AB_TELL_DETAILS_CHANGE</span><span class="sxs-lookup"><span data-stu-id="9e781-131">AB_TELL_DETAILS_CHANGE</span></span>
  
> <span data-ttu-id="9e781-132">Indique que **les détails** renvoie S_OK si les modifications sont réellement apportées à l’adresse ; dans le cas contraire, les **Détails** renvoie S_FALSE.</span><span class="sxs-lookup"><span data-stu-id="9e781-132">Indicates that **Details** returns S_OK if changes are actually made to the address; otherwise, **Details** returns S_FALSE.</span></span> 
    
<span data-ttu-id="9e781-133">DIALOG_MODAL</span><span class="sxs-lookup"><span data-stu-id="9e781-133">DIALOG_MODAL</span></span>
  
> <span data-ttu-id="9e781-134">Afficher la version de la boîte de dialogue adresse, qui est toujours affichée dans les clients Outlook-non modale.</span><span class="sxs-lookup"><span data-stu-id="9e781-134">Display the modal version of the common address dialog box, which is always shown in non-Outlook clients.</span></span> <span data-ttu-id="9e781-135">Cet indicateur est mutuellement exclusif avec DIALOG_SDI.</span><span class="sxs-lookup"><span data-stu-id="9e781-135">This flag is mutually exclusive with DIALOG_SDI.</span></span>
    
<span data-ttu-id="9e781-136">DIALOG_SDI</span><span class="sxs-lookup"><span data-stu-id="9e781-136">DIALOG_SDI</span></span>
  
>  <span data-ttu-id="9e781-137">Afficher la version de la boîte de dialogue adresse non modale.</span><span class="sxs-lookup"><span data-stu-id="9e781-137">Display the modeless version of the common address dialog box.</span></span> <span data-ttu-id="9e781-138">Cet indicateur est ignoré pour les clients non Outlook.</span><span class="sxs-lookup"><span data-stu-id="9e781-138">This flag is ignored for non-Outlook clients.</span></span> 
    
<span data-ttu-id="9e781-139">MAPI_UNICODE</span><span class="sxs-lookup"><span data-stu-id="9e781-139">MAPI_UNICODE</span></span> 
  
> <span data-ttu-id="9e781-140">Les chaînes passée sont au format Unicode.</span><span class="sxs-lookup"><span data-stu-id="9e781-140">The passed-in strings are in Unicode format.</span></span> <span data-ttu-id="9e781-141">Si l’indicateur MAPI_UNICODE n’est pas définie, les chaînes sont au format ANSI.</span><span class="sxs-lookup"><span data-stu-id="9e781-141">If the MAPI_UNICODE flag is not set, the strings are in ANSI format.</span></span>
    
## <a name="return-value"></a><span data-ttu-id="9e781-142">Valeur renvoy�e</span><span class="sxs-lookup"><span data-stu-id="9e781-142">Return value</span></span>

<span data-ttu-id="9e781-143">S_OK</span><span class="sxs-lookup"><span data-stu-id="9e781-143">S_OK</span></span> 
  
> <span data-ttu-id="9e781-144">La boîte de dialogue a été correctement affichée pour l’entrée du carnet d’adresses.</span><span class="sxs-lookup"><span data-stu-id="9e781-144">The details dialog box was successfully displayed for the address book entry.</span></span>
    
## <a name="remarks"></a><span data-ttu-id="9e781-145">Remarques</span><span class="sxs-lookup"><span data-stu-id="9e781-145">Remarks</span></span>

<span data-ttu-id="9e781-146">Applications clientes appellent la méthode **Details** pour afficher une boîte de dialogue qui fournit des détails sur une entrée particulière dans le carnet d’adresses.</span><span class="sxs-lookup"><span data-stu-id="9e781-146">Client applications call the **Details** method to display a dialog box that provides details about a particular entry in the address book.</span></span> <span data-ttu-id="9e781-147">Vous pouvez utiliser les paramètres _lpfButtonCallback_, _lpvButtonContext_et _lpszButtonText_ pour ajouter un bouton défini par le client à la boîte de dialogue.</span><span class="sxs-lookup"><span data-stu-id="9e781-147">You can use the  _lpfButtonCallback_,  _lpvButtonContext_, and  _lpszButtonText_ parameters to add a client-defined button to the dialog box.</span></span> <span data-ttu-id="9e781-148">Lorsque le bouton est activé, MAPI appelle la fonction de rappel désignée par _lpfButtonCallback_, en passant l’identificateur de l’entrée du bouton et les données _lpvButtonContext_.</span><span class="sxs-lookup"><span data-stu-id="9e781-148">When the button is clicked, MAPI calls the callback function pointed to by  _lpfButtonCallback_, passing both the entry identifier of the button and the data in  _lpvButtonContext_.</span></span> <span data-ttu-id="9e781-149">Si vous n’avez pas besoin d’un bouton extensible, _lpszButtonText_ doit être NULL.</span><span class="sxs-lookup"><span data-stu-id="9e781-149">If you do not need an extensible button,  _lpszButtonText_ should be NULL.</span></span> 
  
 <span data-ttu-id="9e781-150">**Détails** prend en charge les chaînes de caractères Unicode ; Les chaînes Unicode sont convertis au format de chaîne (MBCS) codés avant qu’elles sont affichées dans la boîte de dialogue Détails.</span><span class="sxs-lookup"><span data-stu-id="9e781-150">**Details** supports Unicode character strings; Unicode strings are converted to the multibyte character string (MBCS) format before they are displayed in the details dialog box.</span></span> 
  
## <a name="mfcmapi-reference"></a><span data-ttu-id="9e781-151">Référence MFCMAPI</span><span class="sxs-lookup"><span data-stu-id="9e781-151">MFCMAPI reference</span></span>

<span data-ttu-id="9e781-152">Pour des exemples de code MFCMAPI, voir le tableau suivant.</span><span class="sxs-lookup"><span data-stu-id="9e781-152">For MFCMAPI sample code, see the following table.</span></span>
  
|<span data-ttu-id="9e781-153">**Fichier**</span><span class="sxs-lookup"><span data-stu-id="9e781-153">**File**</span></span>|<span data-ttu-id="9e781-154">**Fonction**</span><span class="sxs-lookup"><span data-stu-id="9e781-154">**Function**</span></span>|<span data-ttu-id="9e781-155">**Commentaire**</span><span class="sxs-lookup"><span data-stu-id="9e781-155">**Comment**</span></span>|
|:-----|:-----|:-----|
|<span data-ttu-id="9e781-156">BaseDialog.cpp</span><span class="sxs-lookup"><span data-stu-id="9e781-156">BaseDialog.cpp</span></span>  <br/> |<span data-ttu-id="9e781-157">CBaseDialog::OnOpenEntryID</span><span class="sxs-lookup"><span data-stu-id="9e781-157">CBaseDialog::OnOpenEntryID</span></span>  <br/> |<span data-ttu-id="9e781-158">MFCMAPI utilise la méthode **Details** pour afficher une boîte de dialogue qui affiche les détails d’une entrée de carnet d’adresses.</span><span class="sxs-lookup"><span data-stu-id="9e781-158">MFCMAPI uses the **Details** method to display a dialog box that shows the details for an address book entry.</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="9e781-159">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="9e781-159">See also</span></span>



[<span data-ttu-id="9e781-160">ADRPARM</span><span class="sxs-lookup"><span data-stu-id="9e781-160">ADRPARM</span></span>](adrparm.md)
  
[<span data-ttu-id="9e781-161">IAddrBook::Address</span><span class="sxs-lookup"><span data-stu-id="9e781-161">IAddrBook::Address</span></span>](iaddrbook-address.md)
  
[<span data-ttu-id="9e781-162">LPFNBUTTON</span><span class="sxs-lookup"><span data-stu-id="9e781-162">LPFNBUTTON</span></span>](lpfnbutton.md)
  
[<span data-ttu-id="9e781-163">IAddrBook : IMAPIProp</span><span class="sxs-lookup"><span data-stu-id="9e781-163">IAddrBook : IMAPIProp</span></span>](iaddrbookimapiprop.md)


[<span data-ttu-id="9e781-164">MFCMAPI comme un exemple de Code</span><span class="sxs-lookup"><span data-stu-id="9e781-164">MFCMAPI as a Code Sample</span></span>](mfcmapi-as-a-code-sample.md)

