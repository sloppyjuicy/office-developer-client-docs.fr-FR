---
title: IMAPIFormDoVerb
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- IMAPIForm.DoVerb
api_type:
- COM
ms.assetid: 8b582571-b448-4476-91d9-4cc94dbec710
description: Dernière modification le 09 mars 2015
ms.openlocfilehash: fe6270d82d227f52dfd5dfa5454c73e815ad9f42
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/23/2018
ms.locfileid: "22573816"
---
# <a name="imapiformdoverb"></a><span data-ttu-id="8b598-103">IMAPIForm::DoVerb</span><span class="sxs-lookup"><span data-stu-id="8b598-103">IMAPIForm::DoVerb</span></span>

  
  
<span data-ttu-id="8b598-104">**S’applique à**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="8b598-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="8b598-105">Exige que le formulaire exécute ce que les tâches associe un verbe spécifique.</span><span class="sxs-lookup"><span data-stu-id="8b598-105">Requests that the form perform whatever tasks it associates with a specific verb.</span></span>
  
```cpp
HRESULT DoVerb(
  LONG iVerb,
  LPMAPIVIEWCONTEXT lpViewContext,
  ULONG_PTR hwndParent,
  LPCRECT lprcPosRect
);
```

## <a name="parameters"></a><span data-ttu-id="8b598-106">Paramètres</span><span class="sxs-lookup"><span data-stu-id="8b598-106">Parameters</span></span>

 <span data-ttu-id="8b598-107">_iVerb_</span><span class="sxs-lookup"><span data-stu-id="8b598-107">_iVerb_</span></span>
  
> <span data-ttu-id="8b598-108">[in] Le numéro associé à un des verbes du formulaire.</span><span class="sxs-lookup"><span data-stu-id="8b598-108">[in] The number associated with one of the form's verbs.</span></span>
    
 <span data-ttu-id="8b598-109">_lpViewContext_</span><span class="sxs-lookup"><span data-stu-id="8b598-109">_lpViewContext_</span></span>
  
> <span data-ttu-id="8b598-110">[in] Pointeur vers un objet de contexte de vue.</span><span class="sxs-lookup"><span data-stu-id="8b598-110">[in] A pointer to a view context object.</span></span> <span data-ttu-id="8b598-111">Le paramètre _lpViewContext_ peut être **null**.</span><span class="sxs-lookup"><span data-stu-id="8b598-111">The  _lpViewContext_ parameter can be **null**.</span></span>
    
 <span data-ttu-id="8b598-112">_hwndParent_</span><span class="sxs-lookup"><span data-stu-id="8b598-112">_hwndParent_</span></span>
  
> <span data-ttu-id="8b598-113">[in] Un handle vers la fenêtre parent des boîtes de dialogue ni windows cette méthode affiche.</span><span class="sxs-lookup"><span data-stu-id="8b598-113">[in] A handle to the parent window of any dialog boxes or windows this method displays.</span></span> <span data-ttu-id="8b598-114">Le paramètre _hwndParent_ doit être **null** si la boîte de dialogue ou fenêtre n’est pas modal.</span><span class="sxs-lookup"><span data-stu-id="8b598-114">The  _hwndParent_ parameter should be **null** if the dialog box or window is not modal.</span></span> 
    
 <span data-ttu-id="8b598-115">_lprcPosRect_</span><span class="sxs-lookup"><span data-stu-id="8b598-115">_lprcPosRect_</span></span>
  
> <span data-ttu-id="8b598-116">[in] Un pointeur vers un Win32 structure [RECT](http://msdn.microsoft.com/en-us/library/dd162897%28VS.85%29.aspx) qui contient la taille et la position de la fenêtre du formulaire.</span><span class="sxs-lookup"><span data-stu-id="8b598-116">[in] A pointer to a Win32 [RECT](http://msdn.microsoft.com/en-us/library/dd162897%28VS.85%29.aspx) structure that contains the size and position of the form's window.</span></span> 
    
## <a name="return-value"></a><span data-ttu-id="8b598-117">Valeur renvoy�e</span><span class="sxs-lookup"><span data-stu-id="8b598-117">Return value</span></span>

<span data-ttu-id="8b598-118">S_OK</span><span class="sxs-lookup"><span data-stu-id="8b598-118">S_OK</span></span> 
  
> <span data-ttu-id="8b598-119">Le verbe a été invoqué.</span><span class="sxs-lookup"><span data-stu-id="8b598-119">The verb was successfully invoked.</span></span>
    
<span data-ttu-id="8b598-120">OLEOBJ_S_CANNOT_DOVERB_NOW</span><span class="sxs-lookup"><span data-stu-id="8b598-120">OLEOBJ_S_CANNOT_DOVERB_NOW</span></span> 
  
> <span data-ttu-id="8b598-121">Le verbe représenté par le paramètre _iVerb_ est valid, mais le formulaire ne peut pas effectuer les opérations actuellement associées.</span><span class="sxs-lookup"><span data-stu-id="8b598-121">The verb represented by the  _iVerb_ parameter is valid, but the form cannot perform the operations currently associated with it.</span></span> 
    
## <a name="remarks"></a><span data-ttu-id="8b598-122">Remarques</span><span class="sxs-lookup"><span data-stu-id="8b598-122">Remarks</span></span>

<span data-ttu-id="8b598-123">Visionneuses de formulaire appeler la méthode **IMAPIForm::DoVerb** pour demander que le formulaire effectuer les tâches qu’elle associe à chaque verbe prenant en charge le formulaire.</span><span class="sxs-lookup"><span data-stu-id="8b598-123">Form viewers call the **IMAPIForm::DoVerb** method to request that the form perform the tasks that it associates with each verb that the form supports.</span></span> 
  
<span data-ttu-id="8b598-124">Chacun des verbes pris en charge est identifiée par une valeur numérique, transmise à **DoVerb** dans le paramètre _iVerb_ .</span><span class="sxs-lookup"><span data-stu-id="8b598-124">Each of the supported verbs is identified by a numeric value, passed to **DoVerb** in the  _iVerb_ parameter.</span></span> <span data-ttu-id="8b598-125">Implémentations classiques de **DoVerb** contient une instruction **switch** qui teste les valeurs valides pour le paramètre _iVerb_ pour le formulaire.</span><span class="sxs-lookup"><span data-stu-id="8b598-125">Typical implementations of **DoVerb** contain a **switch** statement that tests the values that are valid for the  _iVerb_ parameter for the form.</span></span> 
  
## <a name="notes-to-implementers"></a><span data-ttu-id="8b598-126">Remarques destinées aux responsables de l’implémentation</span><span class="sxs-lookup"><span data-stu-id="8b598-126">Notes to implementers</span></span>

<span data-ttu-id="8b598-127">Si la visionneuse de formulaire spécifie un contexte de vue dans le paramètre _lpViewContext_ , l’utiliser dans votre implémentation **DoVerb** au lieu du contexte de vue passée dans un appel précédent à la méthode [IMAPIForm::SetViewContext](imapiform-setviewcontext.md) .</span><span class="sxs-lookup"><span data-stu-id="8b598-127">If the form viewer specifies a view context in the  _lpViewContext_ parameter, use it in your **DoVerb** implementation instead of the view context passed in an earlier call to the [IMAPIForm::SetViewContext](imapiform-setviewcontext.md) method.</span></span> <span data-ttu-id="8b598-128">Apportez toutes les modifications sont nécessaires pour vos structures de données internes et ne pas enregistrent le contexte de vue.</span><span class="sxs-lookup"><span data-stu-id="8b598-128">Make whatever changes are necessary to your internal data structures and do not save the view context.</span></span> 
  
<span data-ttu-id="8b598-129">Dans votre implémentation **DoVerb** , effectuez les tâches suivantes :</span><span class="sxs-lookup"><span data-stu-id="8b598-129">Perform the following tasks in your **DoVerb** implementation:</span></span> 
  
- <span data-ttu-id="8b598-130">Exécuter le code est nécessaire pour le verbe qui est associé avec le paramètre _iVerb_ .</span><span class="sxs-lookup"><span data-stu-id="8b598-130">Execute whatever code is necessary for the particular verb that is associated with the  _iVerb_ parameter.</span></span> 
    
- <span data-ttu-id="8b598-131">Si nécessaire, restaurez le contexte de vue d’origine.</span><span class="sxs-lookup"><span data-stu-id="8b598-131">If necessary, restore the original view context.</span></span>
    
- <span data-ttu-id="8b598-132">Si un numéro de verbe inconnu a été passé, retourne MAPI_E_NO_SUPPORT.</span><span class="sxs-lookup"><span data-stu-id="8b598-132">If an unknown verb number was passed in, return MAPI_E_NO_SUPPORT.</span></span> <span data-ttu-id="8b598-133">Sinon, retourne un résultat basé sur la réussite ou l’échec de n’importe quel verbe a été exécuté.</span><span class="sxs-lookup"><span data-stu-id="8b598-133">Otherwise, return a result based on the success or failure of whatever verb was executed.</span></span>
    
- <span data-ttu-id="8b598-134">Fermer le formulaire.</span><span class="sxs-lookup"><span data-stu-id="8b598-134">Close the form.</span></span> <span data-ttu-id="8b598-135">Il est toujours votre responsabilité pour fermer le formulaire après un appel de **DoVerb** .</span><span class="sxs-lookup"><span data-stu-id="8b598-135">It is always your responsibility to close the form after a **DoVerb** call completes.</span></span> 
    
<span data-ttu-id="8b598-136">Certains verbes, telles qu’Imprimer, doivent être modales en ce qui concerne l’appel de **DoVerb** — autrement dit, l’opération indiquée doit être terminée avant l’appel de **DoVerb** retourné.</span><span class="sxs-lookup"><span data-stu-id="8b598-136">Some verbs, such as Print, should be modal with respect to the **DoVerb** call — that is, the indicated operation must be finished before the **DoVerb** call returns.</span></span> 
  
<span data-ttu-id="8b598-137">Pour obtenir la structure **RECT** utilisée par la fenêtre d’un formulaire, appelez la fonction [GetWindowRect](http://msdn.microsoft.com/en-us/library/ms633519) .</span><span class="sxs-lookup"><span data-stu-id="8b598-137">To obtain the **RECT** structure used by a form's window, call the [GetWindowRect](http://msdn.microsoft.com/en-us/library/ms633519) function.</span></span> 
  
<span data-ttu-id="8b598-138">N’enregistrez pas la poignée dans le paramètre _hwndParent_ car, même si elle reste généralement valide jusqu'à la fin de **DoVerb**, il peut être détruit immédiatement lors du retour de l’appel.</span><span class="sxs-lookup"><span data-stu-id="8b598-138">Do not save the handle in the  _hwndParent_ parameter because, although it usually remains valid until the completion of **DoVerb**, it can be destroyed immediately upon the call's return.</span></span>
  
## <a name="notes-to-callers"></a><span data-ttu-id="8b598-139">Notes aux appelants</span><span class="sxs-lookup"><span data-stu-id="8b598-139">Notes to callers</span></span>

<span data-ttu-id="8b598-140">Vous pouvez émettre des verbes non modal agir comme verbes modales, pointez sur une implémentation de contexte de vue qui retourne l’indicateur VCSTATUS_MODAL à partir de la méthode [IMAPIViewContext::GetViewStatus](imapiviewcontext-getviewstatus.md) _lpViewContext_ .</span><span class="sxs-lookup"><span data-stu-id="8b598-140">You can make non-modal verbs act as modal verbs by pointing  _lpViewContext_ to a view context implementation that returns the VCSTATUS_MODAL flag from its [IMAPIViewContext::GetViewStatus](imapiviewcontext-getviewstatus.md) method.</span></span> 
  
<span data-ttu-id="8b598-141">Pour plus d’informations sur les verbes MAPI, voir [Verbes du formulaire](form-verbs.md).</span><span class="sxs-lookup"><span data-stu-id="8b598-141">For more information about verbs in MAPI, see [Form Verbs](form-verbs.md).</span></span> <span data-ttu-id="8b598-142">Pour plus d’informations sur la gestion des verbes OLE, voir [OLE et transfert de données](http://msdn.microsoft.com/en-us/library/ms693425%28VS.85%29.aspx).</span><span class="sxs-lookup"><span data-stu-id="8b598-142">For more information about how verbs are handled in OLE, see [OLE and Data Transfer](http://msdn.microsoft.com/en-us/library/ms693425%28VS.85%29.aspx).</span></span>
  
## <a name="mfcmapi-reference"></a><span data-ttu-id="8b598-143">Référence MFCMAPI</span><span class="sxs-lookup"><span data-stu-id="8b598-143">MFCMAPI reference</span></span>

<span data-ttu-id="8b598-144">Pour des exemples de code MFCMAPI, voir le tableau suivant.</span><span class="sxs-lookup"><span data-stu-id="8b598-144">For MFCMAPI sample code, see the following table.</span></span>
  
|<span data-ttu-id="8b598-145">**Fichier**</span><span class="sxs-lookup"><span data-stu-id="8b598-145">**File**</span></span>|<span data-ttu-id="8b598-146">**Fonction**</span><span class="sxs-lookup"><span data-stu-id="8b598-146">**Function**</span></span>|<span data-ttu-id="8b598-147">**Commentaire**</span><span class="sxs-lookup"><span data-stu-id="8b598-147">**Comment**</span></span>|
|:-----|:-----|:-----|
|<span data-ttu-id="8b598-148">MyMAPIFormViewer.cpp</span><span class="sxs-lookup"><span data-stu-id="8b598-148">MyMAPIFormViewer.cpp</span></span>  <br/> |<span data-ttu-id="8b598-149">CMyMAPIFormViewer::CallDoVerb</span><span class="sxs-lookup"><span data-stu-id="8b598-149">CMyMAPIFormViewer::CallDoVerb</span></span>  <br/> |<span data-ttu-id="8b598-150">MFCMAPI utilise la méthode **IMAPIForm::DoVerb** pour appeler un verbe sur un formulaire.</span><span class="sxs-lookup"><span data-stu-id="8b598-150">MFCMAPI uses the **IMAPIForm::DoVerb** method to invoke a verb on a form.</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="8b598-151">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="8b598-151">See also</span></span>



[<span data-ttu-id="8b598-152">IMAPIForm::SetViewContext</span><span class="sxs-lookup"><span data-stu-id="8b598-152">IMAPIForm::SetViewContext</span></span>](imapiform-setviewcontext.md)
  
[<span data-ttu-id="8b598-153">IMAPIViewContext::GetViewStatus</span><span class="sxs-lookup"><span data-stu-id="8b598-153">IMAPIViewContext::GetViewStatus</span></span>](imapiviewcontext-getviewstatus.md)
  
[<span data-ttu-id="8b598-154">IMAPIForm : IUnknown</span><span class="sxs-lookup"><span data-stu-id="8b598-154">IMAPIForm : IUnknown</span></span>](imapiformiunknown.md)


[<span data-ttu-id="8b598-155">MFCMAPI comme un exemple de Code</span><span class="sxs-lookup"><span data-stu-id="8b598-155">MFCMAPI as a Code Sample</span></span>](mfcmapi-as-a-code-sample.md)
  
[<span data-ttu-id="8b598-156">Verbes de formulaires</span><span class="sxs-lookup"><span data-stu-id="8b598-156">Form Verbs</span></span>](form-verbs.md)

