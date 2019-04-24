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
description: 'Derni�re modification�: lundi 9 mars 2015'
ms.openlocfilehash: bb8699746b3f4207ee70edd4e56d0ec6041beac2
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32351176"
---
# <a name="imapiviewcontextgetviewstatus"></a><span data-ttu-id="5b46e-103">IMAPIViewContext::GetViewStatus</span><span class="sxs-lookup"><span data-stu-id="5b46e-103">IMAPIViewContext::GetViewStatus</span></span>

  
  
<span data-ttu-id="5b46e-104">**S’applique à** : Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="5b46e-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="5b46e-105">Récupère l'état actuel de la visionneuse.</span><span class="sxs-lookup"><span data-stu-id="5b46e-105">Retrieves the current viewer status.</span></span> 
  
```cpp
HRESULT GetViewStatus(
ULONG FAR * lpulStatus
);
```

## <a name="parameters"></a><span data-ttu-id="5b46e-106">Paramètres</span><span class="sxs-lookup"><span data-stu-id="5b46e-106">Parameters</span></span>

 <span data-ttu-id="5b46e-107">_lpulStatus_</span><span class="sxs-lookup"><span data-stu-id="5b46e-107">_lpulStatus_</span></span>
  
> <span data-ttu-id="5b46e-108">remarquer Pointeur vers un masque de réindicateur qui fournit l'état de la visionneuse.</span><span class="sxs-lookup"><span data-stu-id="5b46e-108">[out] Pointer to a bitmask of flags providing the status of the viewer.</span></span> <span data-ttu-id="5b46e-109">Les indicateurs suivants peuvent être définis:</span><span class="sxs-lookup"><span data-stu-id="5b46e-109">The following flags can be set:</span></span>
    
<span data-ttu-id="5b46e-110">VCSTATUS_CATEGORY</span><span class="sxs-lookup"><span data-stu-id="5b46e-110">VCSTATUS_CATEGORY</span></span> 
  
> <span data-ttu-id="5b46e-111">Il existe un message suivant ou précédent dans une autre catégorie.</span><span class="sxs-lookup"><span data-stu-id="5b46e-111">There is a next or previous message in another category.</span></span> 
    
<span data-ttu-id="5b46e-112">VCSTATUS_DELETE</span><span class="sxs-lookup"><span data-stu-id="5b46e-112">VCSTATUS_DELETE</span></span> 
  
> <span data-ttu-id="5b46e-113">Le formulaire permet la suppression des messages.</span><span class="sxs-lookup"><span data-stu-id="5b46e-113">The form allows messages to be removed.</span></span> 
    
<span data-ttu-id="5b46e-114">VCSTATUS_INTERACTIVE</span><span class="sxs-lookup"><span data-stu-id="5b46e-114">VCSTATUS_INTERACTIVE</span></span> 
  
> <span data-ttu-id="5b46e-115">Le formulaire doit afficher une interface utilisateur.</span><span class="sxs-lookup"><span data-stu-id="5b46e-115">The form should display a user interface.</span></span> <span data-ttu-id="5b46e-116">Si cet indicateur n'est pas défini, le formulaire doit supprimer l'affichage d'une interface utilisateur même en réponse à un verbe qui entraîne généralement l'affichage d'une interface utilisateur.</span><span class="sxs-lookup"><span data-stu-id="5b46e-116">If this flag is not set, the form should suppress displaying a user interface even in response to a verb that usually causes a user interface to be displayed.</span></span> 
    
<span data-ttu-id="5b46e-117">VCSTATUS_MODAL</span><span class="sxs-lookup"><span data-stu-id="5b46e-117">VCSTATUS_MODAL</span></span> 
  
> <span data-ttu-id="5b46e-118">Le formulaire est modal dans la visionneuse.</span><span class="sxs-lookup"><span data-stu-id="5b46e-118">The form is modal to the viewer.</span></span> 
    
<span data-ttu-id="5b46e-119">VCSTATUS_NEXT</span><span class="sxs-lookup"><span data-stu-id="5b46e-119">VCSTATUS_NEXT</span></span> 
  
> <span data-ttu-id="5b46e-120">Il y a un message suivant dans l'affichage.</span><span class="sxs-lookup"><span data-stu-id="5b46e-120">There is a next message in the view.</span></span> 
    
<span data-ttu-id="5b46e-121">VCSTATUS_PREV</span><span class="sxs-lookup"><span data-stu-id="5b46e-121">VCSTATUS_PREV</span></span> 
  
> <span data-ttu-id="5b46e-122">Il existe un message précédent dans l'affichage.</span><span class="sxs-lookup"><span data-stu-id="5b46e-122">There is a previous message in the view.</span></span> 
    
<span data-ttu-id="5b46e-123">VCSTATUS_READONLY</span><span class="sxs-lookup"><span data-stu-id="5b46e-123">VCSTATUS_READONLY</span></span> 
  
> <span data-ttu-id="5b46e-124">Le message doit être ouvert en mode lecture seule.</span><span class="sxs-lookup"><span data-stu-id="5b46e-124">The message is to be opened in read-only mode.</span></span> <span data-ttu-id="5b46e-125">Les opérations de suppression, d'envoi et de déplacement doivent être désactivées.</span><span class="sxs-lookup"><span data-stu-id="5b46e-125">Delete, submit, and move operations should be disabled.</span></span> 
    
<span data-ttu-id="5b46e-126">VCSTATUS_UNREAD</span><span class="sxs-lookup"><span data-stu-id="5b46e-126">VCSTATUS_UNREAD</span></span> 
  
> <span data-ttu-id="5b46e-127">Il y a un message non lu suivant ou précédent dans la vue.</span><span class="sxs-lookup"><span data-stu-id="5b46e-127">There is a next or previous unread message in the view.</span></span>
    
## <a name="return-value"></a><span data-ttu-id="5b46e-128">Valeur renvoyée</span><span class="sxs-lookup"><span data-stu-id="5b46e-128">Return value</span></span>

<span data-ttu-id="5b46e-129">S_OK</span><span class="sxs-lookup"><span data-stu-id="5b46e-129">S_OK</span></span> 
  
> <span data-ttu-id="5b46e-130">L'état de la visionneuse a été renvoyé avec succès.</span><span class="sxs-lookup"><span data-stu-id="5b46e-130">The viewer's status was successfully returned.</span></span>
    
## <a name="remarks"></a><span data-ttu-id="5b46e-131">Remarques</span><span class="sxs-lookup"><span data-stu-id="5b46e-131">Remarks</span></span>

<span data-ttu-id="5b46e-132">Les objets de formulaire appellent la méthode **IMAPIViewContext:: GetViewStatus** pour déterminer s'il y a plus de messages à activer dans une vue de formulaire dans l'une ou l'autre des directions, dans le sens où une commande **suivante** active les messages, dans le sens dans lequel une commande **précédente** active les messages, ou dans les deux sens.</span><span class="sxs-lookup"><span data-stu-id="5b46e-132">Form objects call the **IMAPIViewContext::GetViewStatus** method to determine whether there are more messages to be activated in a form view in either or both directions that is, in the direction in which a **Next** command activates messages, in the direction in which a **Previous** command activates messages, or in both directions.</span></span> <span data-ttu-id="5b46e-133">La valeur indiquée par le paramètre _lpulStatus_ est utilisée pour déterminer si les indicateurs VCSTATUS_NEXT et VCSTATUS_PREV sont valides pour [IMAPIViewContext:: ActivateNext,](imapiviewcontext-activatenext.md).</span><span class="sxs-lookup"><span data-stu-id="5b46e-133">The value pointed to by the  _lpulStatus_ parameter is used to determine whether the VCSTATUS_NEXT and VCSTATUS_PREV flags are valid for [IMAPIViewContext::ActivateNext](imapiviewcontext-activatenext.md).</span></span> <span data-ttu-id="5b46e-134">Si l'indicateur VCSTATUS_DELETE est défini, mais pas l'indicateur VCSTATUS_READONLY, le message peut être supprimé à l'aide de la méthode [IMAPIMessageSite::D eletemessage](imapimessagesite-deletemessage.md) .</span><span class="sxs-lookup"><span data-stu-id="5b46e-134">If the VCSTATUS_DELETE flag is set, but not the VCSTATUS_READONLY flag, then the message can be deleted using the [IMAPIMessageSite::DeleteMessage](imapimessagesite-deletemessage.md) method.</span></span> 
  
<span data-ttu-id="5b46e-135">En règle générale, les formulaires désactivent les commandes de menu et les boutons s'ils ne sont pas valides pour le contexte de l'utilisateur.</span><span class="sxs-lookup"><span data-stu-id="5b46e-135">Typically, forms disable menu commands and buttons if they are not valid for the viewer's context.</span></span> <span data-ttu-id="5b46e-136">Une visionneuse peut alerter un formulaire à une modification de l'État en appelant sa méthode [IMAPIFormAdviseSink:: OnChange](imapiformadvisesink-onchange.md) .</span><span class="sxs-lookup"><span data-stu-id="5b46e-136">A viewer can alert a form to a change in status by calling its [IMAPIFormAdviseSink::OnChange](imapiformadvisesink-onchange.md) method.</span></span> 
  
<span data-ttu-id="5b46e-137">L'indicateur VCSTATUS_MODAL est défini si le formulaire doit être modal dans la fenêtre dont le descripteur est passé dans l' [IMAPIForm précédent::D overb](imapiform-doverb.md) .</span><span class="sxs-lookup"><span data-stu-id="5b46e-137">The VCSTATUS_MODAL flag is set if the form must be modal to the window whose handle is passed in the earlier [IMAPIForm::DoVerb](imapiform-doverb.md) call.</span></span> <span data-ttu-id="5b46e-138">Si VCSTATUS_MODAL est défini, le formulaire peut utiliser le thread sur lequel l'appel de **verbe** a été effectué jusqu'à la fermeture du formulaire.</span><span class="sxs-lookup"><span data-stu-id="5b46e-138">If VCSTATUS_MODAL is set, the form can use the thread on which the **DoVerb** call was made until the form closes.</span></span> <span data-ttu-id="5b46e-139">Si VCSTATUS_MODAL n'est pas défini, le formulaire ne doit pas être modal dans cette fenêtre et ne doit pas utiliser le thread.</span><span class="sxs-lookup"><span data-stu-id="5b46e-139">If VCSTATUS_MODAL is not set, the form should not be modal to this window and must not use the thread.</span></span> 
  
## <a name="mfcmapi-reference"></a><span data-ttu-id="5b46e-140">Référence MFCMAPI</span><span class="sxs-lookup"><span data-stu-id="5b46e-140">MFCMAPI reference</span></span>

<span data-ttu-id="5b46e-141">Pour voir un exemple de code MFCMAPI, consultez le tableau suivant.</span><span class="sxs-lookup"><span data-stu-id="5b46e-141">For MFCMAPI sample code, see the following table.</span></span>
  
|<span data-ttu-id="5b46e-142">**Fichier**</span><span class="sxs-lookup"><span data-stu-id="5b46e-142">**File**</span></span>|<span data-ttu-id="5b46e-143">**Fonction**</span><span class="sxs-lookup"><span data-stu-id="5b46e-143">**Function**</span></span>|<span data-ttu-id="5b46e-144">**Commentaire**</span><span class="sxs-lookup"><span data-stu-id="5b46e-144">**Comment**</span></span>|
|:-----|:-----|:-----|
|<span data-ttu-id="5b46e-145">MyMAPIFormViewer. cpp</span><span class="sxs-lookup"><span data-stu-id="5b46e-145">MyMAPIFormViewer.cpp</span></span>  <br/> |<span data-ttu-id="5b46e-146">CMyMAPIFormViewer:: GetViewStatus</span><span class="sxs-lookup"><span data-stu-id="5b46e-146">CMyMAPIFormViewer::GetViewStatus</span></span>  <br/> |<span data-ttu-id="5b46e-147">MFCMAPI implémente la méthode **IMAPIViewContext:: GetViewStatus** dans cette fonction.</span><span class="sxs-lookup"><span data-stu-id="5b46e-147">MFCMAPI implements the **IMAPIViewContext::GetViewStatus** method in this function.</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="5b46e-148">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="5b46e-148">See also</span></span>



[<span data-ttu-id="5b46e-149">IMAPIMessageSite::GetSiteStatus</span><span class="sxs-lookup"><span data-stu-id="5b46e-149">IMAPIMessageSite::GetSiteStatus</span></span>](imapimessagesite-getsitestatus.md)
  
[<span data-ttu-id="5b46e-150">IMAPIViewContext : IUnknown</span><span class="sxs-lookup"><span data-stu-id="5b46e-150">IMAPIViewContext : IUnknown</span></span>](imapiviewcontextiunknown.md)


[<span data-ttu-id="5b46e-151">MFCMAPI comme un exemple de Code</span><span class="sxs-lookup"><span data-stu-id="5b46e-151">MFCMAPI as a Code Sample</span></span>](mfcmapi-as-a-code-sample.md)

