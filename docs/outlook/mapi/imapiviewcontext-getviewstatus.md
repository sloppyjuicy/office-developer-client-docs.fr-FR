---
title: IMAPIViewContextGetViewStatus
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- IMAPIViewContext.GetViewStatus
api_type:
- COM
ms.assetid: 2e5ec914-7171-41ce-a6fe-78dd80ac32ff
description: Dernière modification le 9 mars 2015
ms.openlocfilehash: 992d51526c45334f6db3738e36994f4bb9c07c6e
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/23/2018
ms.locfileid: "22572255"
---
# <a name="imapiviewcontextgetviewstatus"></a><span data-ttu-id="41e18-103">IMAPIViewContext::GetViewStatus</span><span class="sxs-lookup"><span data-stu-id="41e18-103">IMAPIViewContext::GetViewStatus</span></span>

  
  
<span data-ttu-id="41e18-104">**S’applique à** : Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="41e18-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="41e18-105">Récupère l’état actuel de la visionneuse.</span><span class="sxs-lookup"><span data-stu-id="41e18-105">Retrieves the current viewer status.</span></span> 
  
```cpp
HRESULT GetViewStatus(
ULONG FAR * lpulStatus
);
```

## <a name="parameters"></a><span data-ttu-id="41e18-106">Paramètres</span><span class="sxs-lookup"><span data-stu-id="41e18-106">Parameters</span></span>

 <span data-ttu-id="41e18-107">_lpulStatus_</span><span class="sxs-lookup"><span data-stu-id="41e18-107">_lpulStatus_</span></span>
  
> <span data-ttu-id="41e18-108">[out] Pointeur vers un masque de bits d’indicateurs fournissant l’état de la visionneuse.</span><span class="sxs-lookup"><span data-stu-id="41e18-108">[out] Pointer to a bitmask of flags providing the status of the viewer.</span></span> <span data-ttu-id="41e18-109">Les indicateurs suivants peuvent être définis :</span><span class="sxs-lookup"><span data-stu-id="41e18-109">The following flags can be set:</span></span>
    
<span data-ttu-id="41e18-110">VCSTATUS_CATEGORY</span><span class="sxs-lookup"><span data-stu-id="41e18-110">VCSTATUS_CATEGORY</span></span> 
  
> <span data-ttu-id="41e18-111">Il existe un message suivant ou précédent dans une autre catégorie.</span><span class="sxs-lookup"><span data-stu-id="41e18-111">There is a next or previous message in another category.</span></span> 
    
<span data-ttu-id="41e18-112">VCSTATUS_DELETE</span><span class="sxs-lookup"><span data-stu-id="41e18-112">VCSTATUS_DELETE</span></span> 
  
> <span data-ttu-id="41e18-113">Le formulaire permet aux messages à supprimer.</span><span class="sxs-lookup"><span data-stu-id="41e18-113">The form allows messages to be removed.</span></span> 
    
<span data-ttu-id="41e18-114">VCSTATUS_INTERACTIVE</span><span class="sxs-lookup"><span data-stu-id="41e18-114">VCSTATUS_INTERACTIVE</span></span> 
  
> <span data-ttu-id="41e18-115">Le formulaire doit afficher une interface utilisateur.</span><span class="sxs-lookup"><span data-stu-id="41e18-115">The form should display a user interface.</span></span> <span data-ttu-id="41e18-116">Si cet indicateur n’est pas défini, le formulaire doit supprimer affichant une interface utilisateur même en réponse à un verbe qui provoque généralement une interface utilisateur à afficher.</span><span class="sxs-lookup"><span data-stu-id="41e18-116">If this flag is not set, the form should suppress displaying a user interface even in response to a verb that usually causes a user interface to be displayed.</span></span> 
    
<span data-ttu-id="41e18-117">VCSTATUS_MODAL</span><span class="sxs-lookup"><span data-stu-id="41e18-117">VCSTATUS_MODAL</span></span> 
  
> <span data-ttu-id="41e18-118">Le formulaire est modal à l’afficheur.</span><span class="sxs-lookup"><span data-stu-id="41e18-118">The form is modal to the viewer.</span></span> 
    
<span data-ttu-id="41e18-119">VCSTATUS_NEXT</span><span class="sxs-lookup"><span data-stu-id="41e18-119">VCSTATUS_NEXT</span></span> 
  
> <span data-ttu-id="41e18-120">Il existe un message suivant dans l’affichage.</span><span class="sxs-lookup"><span data-stu-id="41e18-120">There is a next message in the view.</span></span> 
    
<span data-ttu-id="41e18-121">VCSTATUS_PREV</span><span class="sxs-lookup"><span data-stu-id="41e18-121">VCSTATUS_PREV</span></span> 
  
> <span data-ttu-id="41e18-122">Il existe un message précédent dans l’affichage.</span><span class="sxs-lookup"><span data-stu-id="41e18-122">There is a previous message in the view.</span></span> 
    
<span data-ttu-id="41e18-123">VCSTATUS_READONLY</span><span class="sxs-lookup"><span data-stu-id="41e18-123">VCSTATUS_READONLY</span></span> 
  
> <span data-ttu-id="41e18-124">Le message doit être ouvert en mode lecture seule.</span><span class="sxs-lookup"><span data-stu-id="41e18-124">The message is to be opened in read-only mode.</span></span> <span data-ttu-id="41e18-125">Supprimer, soumettre et déplacer des opérations doivent être désactivées.</span><span class="sxs-lookup"><span data-stu-id="41e18-125">Delete, submit, and move operations should be disabled.</span></span> 
    
<span data-ttu-id="41e18-126">VCSTATUS_UNREAD</span><span class="sxs-lookup"><span data-stu-id="41e18-126">VCSTATUS_UNREAD</span></span> 
  
> <span data-ttu-id="41e18-127">Il existe un message non lu suivant ou précédent dans l’affichage.</span><span class="sxs-lookup"><span data-stu-id="41e18-127">There is a next or previous unread message in the view.</span></span>
    
## <a name="return-value"></a><span data-ttu-id="41e18-128">Valeur renvoyée</span><span class="sxs-lookup"><span data-stu-id="41e18-128">Return value</span></span>

<span data-ttu-id="41e18-129">S_OK</span><span class="sxs-lookup"><span data-stu-id="41e18-129">S_OK</span></span> 
  
> <span data-ttu-id="41e18-130">État de l’utilisateur a été renvoyée avec succès.</span><span class="sxs-lookup"><span data-stu-id="41e18-130">The viewer's status was successfully returned.</span></span>
    
## <a name="remarks"></a><span data-ttu-id="41e18-131">Remarques</span><span class="sxs-lookup"><span data-stu-id="41e18-131">Remarks</span></span>

<span data-ttu-id="41e18-132">Objets formulaire appeler la méthode **IMAPIViewContext::GetViewStatus** pour déterminer s’il existe plus de messages pour être activé en mode formulaire dans un ou les deux sens, autrement dit, dans le sens dans lequel une commande **suivant** Active les messages, dans la sens dans lequel une commande **précédente** Active les messages, ou dans les deux sens.</span><span class="sxs-lookup"><span data-stu-id="41e18-132">Form objects call the **IMAPIViewContext::GetViewStatus** method to determine whether there are more messages to be activated in a form view in either or both directions that is, in the direction in which a **Next** command activates messages, in the direction in which a **Previous** command activates messages, or in both directions.</span></span> <span data-ttu-id="41e18-133">La valeur indiquée par le paramètre _lpulStatus_ est utilisée pour déterminer si les indicateurs VCSTATUS_NEXT et VCSTATUS_PREV sont valides pour [IMAPIViewContext::ActivateNext](imapiviewcontext-activatenext.md).</span><span class="sxs-lookup"><span data-stu-id="41e18-133">The value pointed to by the  _lpulStatus_ parameter is used to determine whether the VCSTATUS_NEXT and VCSTATUS_PREV flags are valid for [IMAPIViewContext::ActivateNext](imapiviewcontext-activatenext.md).</span></span> <span data-ttu-id="41e18-134">Si l’indicateur VCSTATUS_DELETE est set, mais pas l’indicateur VCSTATUS_READONLY, le message peut être supprimé à l’aide de la méthode [IMAPIMessageSite::DeleteMessage](imapimessagesite-deletemessage.md) .</span><span class="sxs-lookup"><span data-stu-id="41e18-134">If the VCSTATUS_DELETE flag is set, but not the VCSTATUS_READONLY flag, then the message can be deleted using the [IMAPIMessageSite::DeleteMessage](imapimessagesite-deletemessage.md) method.</span></span> 
  
<span data-ttu-id="41e18-135">En règle générale, formulaires désactiver les commandes de menu et les boutons si elles ne sont pas valides pour le contexte de l’utilisateur.</span><span class="sxs-lookup"><span data-stu-id="41e18-135">Typically, forms disable menu commands and buttons if they are not valid for the viewer's context.</span></span> <span data-ttu-id="41e18-136">Une visionneuse peut alerter un formulaire à un changement d’état en appelant la méthode [IMAPIFormAdviseSink::OnChange](imapiformadvisesink-onchange.md) .</span><span class="sxs-lookup"><span data-stu-id="41e18-136">A viewer can alert a form to a change in status by calling its [IMAPIFormAdviseSink::OnChange](imapiformadvisesink-onchange.md) method.</span></span> 
  
<span data-ttu-id="41e18-137">L’indicateur VCSTATUS_MODAL est défini si le formulaire doit être modal à la fenêtre dont le descripteur est transmis dans l’appel [IMAPIForm::DoVerb](imapiform-doverb.md) antérieur.</span><span class="sxs-lookup"><span data-stu-id="41e18-137">The VCSTATUS_MODAL flag is set if the form must be modal to the window whose handle is passed in the earlier [IMAPIForm::DoVerb](imapiform-doverb.md) call.</span></span> <span data-ttu-id="41e18-138">Si VCSTATUS_MODAL est défini, le formulaire peut utiliser le thread sur lequel l’appel de **DoVerb** a été effectué jusqu'à ce que le formulaire se ferme.</span><span class="sxs-lookup"><span data-stu-id="41e18-138">If VCSTATUS_MODAL is set, the form can use the thread on which the **DoVerb** call was made until the form closes.</span></span> <span data-ttu-id="41e18-139">Si VCSTATUS_MODAL n’est pas défini, le formulaire ne doit pas être modal dans cette fenêtre et ne doit pas utiliser le thread.</span><span class="sxs-lookup"><span data-stu-id="41e18-139">If VCSTATUS_MODAL is not set, the form should not be modal to this window and must not use the thread.</span></span> 
  
## <a name="mfcmapi-reference"></a><span data-ttu-id="41e18-140">Référence MFCMAPI</span><span class="sxs-lookup"><span data-stu-id="41e18-140">MFCMAPI reference</span></span>

<span data-ttu-id="41e18-141">Pour voir un exemple de code MFCMAPI, consultez le tableau suivant.</span><span class="sxs-lookup"><span data-stu-id="41e18-141">For MFCMAPI sample code, see the following table.</span></span>
  
|<span data-ttu-id="41e18-142">**Fichier**</span><span class="sxs-lookup"><span data-stu-id="41e18-142">**File**</span></span>|<span data-ttu-id="41e18-143">**Fonction**</span><span class="sxs-lookup"><span data-stu-id="41e18-143">**Function**</span></span>|<span data-ttu-id="41e18-144">**Commentaire**</span><span class="sxs-lookup"><span data-stu-id="41e18-144">**Comment**</span></span>|
|:-----|:-----|:-----|
|<span data-ttu-id="41e18-145">MyMAPIFormViewer.cpp</span><span class="sxs-lookup"><span data-stu-id="41e18-145">MyMAPIFormViewer.cpp</span></span>  <br/> |<span data-ttu-id="41e18-146">CMyMAPIFormViewer::GetViewStatus</span><span class="sxs-lookup"><span data-stu-id="41e18-146">CMyMAPIFormViewer::GetViewStatus</span></span>  <br/> |<span data-ttu-id="41e18-147">MFCMAPI implémente la méthode **IMAPIViewContext::GetViewStatus** dans cette fonction.</span><span class="sxs-lookup"><span data-stu-id="41e18-147">MFCMAPI implements the **IMAPIViewContext::GetViewStatus** method in this function.</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="41e18-148">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="41e18-148">See also</span></span>



[<span data-ttu-id="41e18-149">IMAPIMessageSite::GetSiteStatus</span><span class="sxs-lookup"><span data-stu-id="41e18-149">IMAPIMessageSite::GetSiteStatus</span></span>](imapimessagesite-getsitestatus.md)
  
[<span data-ttu-id="41e18-150">IMAPIViewContext : IUnknown</span><span class="sxs-lookup"><span data-stu-id="41e18-150">IMAPIViewContext : IUnknown</span></span>](imapiviewcontextiunknown.md)


[<span data-ttu-id="41e18-151">MFCMAPI comme un exemple de Code</span><span class="sxs-lookup"><span data-stu-id="41e18-151">MFCMAPI as a Code Sample</span></span>](mfcmapi-as-a-code-sample.md)

