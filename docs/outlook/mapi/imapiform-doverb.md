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
description: Dernière modification le 9 mars 2015
ms.openlocfilehash: 60a8c89afe0d70a1737c6ce694c66359fd6aae4f
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32329455"
---
# <a name="imapiformdoverb"></a><span data-ttu-id="21e93-103">IMAPIForm::DoVerb</span><span class="sxs-lookup"><span data-stu-id="21e93-103">IMAPIForm::DoVerb</span></span>

  
  
<span data-ttu-id="21e93-104">**S’applique à** : Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="21e93-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="21e93-105">Demande au formulaire d’effectuer les tâches qu’il associe à un verbe spécifique.</span><span class="sxs-lookup"><span data-stu-id="21e93-105">Requests that the form perform whatever tasks it associates with a specific verb.</span></span>
  
```cpp
HRESULT DoVerb(
  LONG iVerb,
  LPMAPIVIEWCONTEXT lpViewContext,
  ULONG_PTR hwndParent,
  LPCRECT lprcPosRect
);
```

## <a name="parameters"></a><span data-ttu-id="21e93-106">Parameters</span><span class="sxs-lookup"><span data-stu-id="21e93-106">Parameters</span></span>

 <span data-ttu-id="21e93-107">_iVerb_</span><span class="sxs-lookup"><span data-stu-id="21e93-107">_iVerb_</span></span>
  
> <span data-ttu-id="21e93-108">[in] Nombre associé à l’un des verbes du formulaire.</span><span class="sxs-lookup"><span data-stu-id="21e93-108">[in] The number associated with one of the form's verbs.</span></span>
    
 <span data-ttu-id="21e93-109">_lpViewContext_</span><span class="sxs-lookup"><span data-stu-id="21e93-109">_lpViewContext_</span></span>
  
> <span data-ttu-id="21e93-110">[in] Pointeur vers un objet de contexte d’affichage.</span><span class="sxs-lookup"><span data-stu-id="21e93-110">[in] A pointer to a view context object.</span></span> <span data-ttu-id="21e93-111">Le  _paramètre lpViewContext_ peut être **null**.</span><span class="sxs-lookup"><span data-stu-id="21e93-111">The  _lpViewContext_ parameter can be **null**.</span></span>
    
 <span data-ttu-id="21e93-112">_hwndParent_</span><span class="sxs-lookup"><span data-stu-id="21e93-112">_hwndParent_</span></span>
  
> <span data-ttu-id="21e93-113">[in] Poignée vers la fenêtre parente de toutes les boîtes de dialogue ou fenêtres affichées par cette méthode.</span><span class="sxs-lookup"><span data-stu-id="21e93-113">[in] A handle to the parent window of any dialog boxes or windows this method displays.</span></span> <span data-ttu-id="21e93-114">Le  _paramètre hwndParent_ doit être **null** si la boîte de dialogue ou la fenêtre n’est pas modale.</span><span class="sxs-lookup"><span data-stu-id="21e93-114">The  _hwndParent_ parameter should be **null** if the dialog box or window is not modal.</span></span> 
    
 <span data-ttu-id="21e93-115">_lprcPosRect_</span><span class="sxs-lookup"><span data-stu-id="21e93-115">_lprcPosRect_</span></span>
  
> <span data-ttu-id="21e93-116">[in] Pointeur vers une structure [RECT](https://msdn.microsoft.com/library/dd162897%28VS.85%29.aspx) Win32 qui contient la taille et la position de la fenêtre du formulaire.</span><span class="sxs-lookup"><span data-stu-id="21e93-116">[in] A pointer to a Win32 [RECT](https://msdn.microsoft.com/library/dd162897%28VS.85%29.aspx) structure that contains the size and position of the form's window.</span></span> 
    
## <a name="return-value"></a><span data-ttu-id="21e93-117">Valeur renvoyée</span><span class="sxs-lookup"><span data-stu-id="21e93-117">Return value</span></span>

<span data-ttu-id="21e93-118">S_OK</span><span class="sxs-lookup"><span data-stu-id="21e93-118">S_OK</span></span> 
  
> <span data-ttu-id="21e93-119">Le verbe a été appelé avec succès.</span><span class="sxs-lookup"><span data-stu-id="21e93-119">The verb was successfully invoked.</span></span>
    
<span data-ttu-id="21e93-120">OLEOBJ_S_CANNOT_DOVERB_NOW</span><span class="sxs-lookup"><span data-stu-id="21e93-120">OLEOBJ_S_CANNOT_DOVERB_NOW</span></span> 
  
> <span data-ttu-id="21e93-121">Le verbe représenté par le  _paramètre iVerb_ est valide, mais le formulaire ne peut pas effectuer les opérations qui lui sont actuellement associées.</span><span class="sxs-lookup"><span data-stu-id="21e93-121">The verb represented by the  _iVerb_ parameter is valid, but the form cannot perform the operations currently associated with it.</span></span> 
    
## <a name="remarks"></a><span data-ttu-id="21e93-122">Remarques</span><span class="sxs-lookup"><span data-stu-id="21e93-122">Remarks</span></span>

<span data-ttu-id="21e93-123">Les visionneuses de formulaire appellent la méthode **IMAPIForm::D oVerb** pour demander au formulaire d’effectuer les tâches qu’il associe à chaque verbe qu’il prend en charge.</span><span class="sxs-lookup"><span data-stu-id="21e93-123">Form viewers call the **IMAPIForm::DoVerb** method to request that the form perform the tasks that it associates with each verb that the form supports.</span></span> 
  
<span data-ttu-id="21e93-124">Chacun des verbes pris en charge est identifié par une valeur numérique, transmise à **DoVerb** dans le _paramètre iVerb._</span><span class="sxs-lookup"><span data-stu-id="21e93-124">Each of the supported verbs is identified by a numeric value, passed to **DoVerb** in the  _iVerb_ parameter.</span></span> <span data-ttu-id="21e93-125">Les implémentations classiques **de DoVerb** contiennent une instruction **switch** qui teste les valeurs valides pour le paramètre  _iVerb_ du formulaire.</span><span class="sxs-lookup"><span data-stu-id="21e93-125">Typical implementations of **DoVerb** contain a **switch** statement that tests the values that are valid for the  _iVerb_ parameter for the form.</span></span> 
  
## <a name="notes-to-implementers"></a><span data-ttu-id="21e93-126">Remarques pour les responsables de l’implémentation</span><span class="sxs-lookup"><span data-stu-id="21e93-126">Notes to implementers</span></span>

<span data-ttu-id="21e93-127">Si la visionneuse de formulaire spécifie un contexte d’affichage dans le paramètre _lpViewContext,_ utilisez-le dans votre implémentation **DoVerb** au lieu du contexte d’affichage passé dans un appel précédent à la méthode [IMAPIForm::SetViewContext.](imapiform-setviewcontext.md)</span><span class="sxs-lookup"><span data-stu-id="21e93-127">If the form viewer specifies a view context in the  _lpViewContext_ parameter, use it in your **DoVerb** implementation instead of the view context passed in an earlier call to the [IMAPIForm::SetViewContext](imapiform-setviewcontext.md) method.</span></span> <span data-ttu-id="21e93-128">A apporter les modifications nécessaires à vos structures de données internes et n’enregistrez pas le contexte d’affichage.</span><span class="sxs-lookup"><span data-stu-id="21e93-128">Make whatever changes are necessary to your internal data structures and do not save the view context.</span></span> 
  
<span data-ttu-id="21e93-129">Effectuez les tâches suivantes dans votre **implémentation DoVerb** :</span><span class="sxs-lookup"><span data-stu-id="21e93-129">Perform the following tasks in your **DoVerb** implementation:</span></span> 
  
- <span data-ttu-id="21e93-130">Exécutez le code nécessaire pour le verbe particulier associé au _paramètre iVerb._</span><span class="sxs-lookup"><span data-stu-id="21e93-130">Execute whatever code is necessary for the particular verb that is associated with the  _iVerb_ parameter.</span></span> 
    
- <span data-ttu-id="21e93-131">Si nécessaire, restituer le contexte de l’affichage d’origine.</span><span class="sxs-lookup"><span data-stu-id="21e93-131">If necessary, restore the original view context.</span></span>
    
- <span data-ttu-id="21e93-132">Si un nombre de verbes inconnu a été transmis, renvoyez-MAPI_E_NO_SUPPORT.</span><span class="sxs-lookup"><span data-stu-id="21e93-132">If an unknown verb number was passed in, return MAPI_E_NO_SUPPORT.</span></span> <span data-ttu-id="21e93-133">Sinon, renvoyer un résultat en fonction de la réussite ou de l’échec du verbe exécuté.</span><span class="sxs-lookup"><span data-stu-id="21e93-133">Otherwise, return a result based on the success or failure of whatever verb was executed.</span></span>
    
- <span data-ttu-id="21e93-134">Fermez le formulaire.</span><span class="sxs-lookup"><span data-stu-id="21e93-134">Close the form.</span></span> <span data-ttu-id="21e93-135">Il est toujours de votre responsabilité de fermer le formulaire une fois qu’un appel **DoVerb** est terminé.</span><span class="sxs-lookup"><span data-stu-id="21e93-135">It is always your responsibility to close the form after a **DoVerb** call completes.</span></span> 
    
<span data-ttu-id="21e93-136">Certains verbes, tels que Print, doivent être modaux par rapport à l’appel **DoVerb,** c’est-à-dire que l’opération indiquée doit être terminée avant le retour de **l’appel DoVerb.**</span><span class="sxs-lookup"><span data-stu-id="21e93-136">Some verbs, such as Print, should be modal with respect to the **DoVerb** call — that is, the indicated operation must be finished before the **DoVerb** call returns.</span></span> 
  
<span data-ttu-id="21e93-137">Pour obtenir la structure **RECT** utilisée par la fenêtre d’un formulaire, appelez la [fonction GetWindowRect.](https://msdn.microsoft.com/library/ms633519)</span><span class="sxs-lookup"><span data-stu-id="21e93-137">To obtain the **RECT** structure used by a form's window, call the [GetWindowRect](https://msdn.microsoft.com/library/ms633519) function.</span></span> 
  
<span data-ttu-id="21e93-138">N’enregistrez pas le handle dans le paramètre  _hwndParent_ car, bien qu’il reste généralement valide jusqu’à la fin de **DoVerb,** il peut être détruit immédiatement au retour de l’appel.</span><span class="sxs-lookup"><span data-stu-id="21e93-138">Do not save the handle in the  _hwndParent_ parameter because, although it usually remains valid until the completion of **DoVerb**, it can be destroyed immediately upon the call's return.</span></span>
  
## <a name="notes-to-callers"></a><span data-ttu-id="21e93-139">Remarques pour les appelants</span><span class="sxs-lookup"><span data-stu-id="21e93-139">Notes to callers</span></span>

<span data-ttu-id="21e93-140">Vous pouvez faire en sorte que les verbes non modaux agissent en tant que verbes modaux en pointant _lpViewContext_ vers une implémentation de contexte d’affichage qui renvoie l’indicateur VCSTATUS_MODAL à partir de sa méthode [IMAPIViewContext::GetViewStatus.](imapiviewcontext-getviewstatus.md)</span><span class="sxs-lookup"><span data-stu-id="21e93-140">You can make non-modal verbs act as modal verbs by pointing  _lpViewContext_ to a view context implementation that returns the VCSTATUS_MODAL flag from its [IMAPIViewContext::GetViewStatus](imapiviewcontext-getviewstatus.md) method.</span></span> 
  
<span data-ttu-id="21e93-141">Pour plus d’informations sur les verbes dans MAPI, voir [Verbes de formulaire.](form-verbs.md)</span><span class="sxs-lookup"><span data-stu-id="21e93-141">For more information about verbs in MAPI, see [Form Verbs](form-verbs.md).</span></span> <span data-ttu-id="21e93-142">Pour plus d’informations sur la façon dont les verbes sont gérés dans OLE, voir [OLE et Transfert de données.](https://msdn.microsoft.com/library/ms693425%28VS.85%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="21e93-142">For more information about how verbs are handled in OLE, see [OLE and Data Transfer](https://msdn.microsoft.com/library/ms693425%28VS.85%29.aspx).</span></span>
  
## <a name="mfcmapi-reference"></a><span data-ttu-id="21e93-143">Référence MFCMAPI</span><span class="sxs-lookup"><span data-stu-id="21e93-143">MFCMAPI reference</span></span>

<span data-ttu-id="21e93-144">Pour voir un exemple de code MFCMAPI, consultez le tableau suivant.</span><span class="sxs-lookup"><span data-stu-id="21e93-144">For MFCMAPI sample code, see the following table.</span></span>
  
|<span data-ttu-id="21e93-145">**Fichier**</span><span class="sxs-lookup"><span data-stu-id="21e93-145">**File**</span></span>|<span data-ttu-id="21e93-146">**Fonction**</span><span class="sxs-lookup"><span data-stu-id="21e93-146">**Function**</span></span>|<span data-ttu-id="21e93-147">**Commentaire**</span><span class="sxs-lookup"><span data-stu-id="21e93-147">**Comment**</span></span>|
|:-----|:-----|:-----|
|<span data-ttu-id="21e93-148">MyMAPIFormViewer.cpp</span><span class="sxs-lookup"><span data-stu-id="21e93-148">MyMAPIFormViewer.cpp</span></span>  <br/> |<span data-ttu-id="21e93-149">CMyMAPIFormViewer::CallDoVerb</span><span class="sxs-lookup"><span data-stu-id="21e93-149">CMyMAPIFormViewer::CallDoVerb</span></span>  <br/> |<span data-ttu-id="21e93-150">MFCMAPI utilise **la méthode IMAPIForm::D oVerb** pour appeler un verbe sur un formulaire.</span><span class="sxs-lookup"><span data-stu-id="21e93-150">MFCMAPI uses the **IMAPIForm::DoVerb** method to invoke a verb on a form.</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="21e93-151">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="21e93-151">See also</span></span>



[<span data-ttu-id="21e93-152">IMAPIForm::SetViewContext</span><span class="sxs-lookup"><span data-stu-id="21e93-152">IMAPIForm::SetViewContext</span></span>](imapiform-setviewcontext.md)
  
[<span data-ttu-id="21e93-153">IMAPIViewContext::GetViewStatus</span><span class="sxs-lookup"><span data-stu-id="21e93-153">IMAPIViewContext::GetViewStatus</span></span>](imapiviewcontext-getviewstatus.md)
  
[<span data-ttu-id="21e93-154">IMAPIForm : IUnknown</span><span class="sxs-lookup"><span data-stu-id="21e93-154">IMAPIForm : IUnknown</span></span>](imapiformiunknown.md)


[<span data-ttu-id="21e93-155">MFCMAPI comme un exemple de Code</span><span class="sxs-lookup"><span data-stu-id="21e93-155">MFCMAPI as a Code Sample</span></span>](mfcmapi-as-a-code-sample.md)
  
[<span data-ttu-id="21e93-156">Verbes de formulaire</span><span class="sxs-lookup"><span data-stu-id="21e93-156">Form Verbs</span></span>](form-verbs.md)

