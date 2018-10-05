---
title: IMAPIFormShutdownForm
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- IMAPIForm.ShutdownForm
api_type:
- COM
ms.assetid: f1e2a526-40ad-4a93-908f-8ab9a65928a8
description: 'Derniére modification : samedi 23 juillet 2011'
ms.openlocfilehash: 073a76766a296d86e7a23809921b832d494a8f1b
ms.sourcegitcommit: ef717c65d8dd41ababffb01eafc443c79950aed4
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 10/04/2018
ms.locfileid: "25384835"
---
# <a name="imapiformshutdownform"></a><span data-ttu-id="948ec-103">IMAPIForm::ShutdownForm</span><span class="sxs-lookup"><span data-stu-id="948ec-103">IMAPIForm::ShutdownForm</span></span>

  
  
<span data-ttu-id="948ec-104">**S’applique à** : Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="948ec-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="948ec-105">Ferme le formulaire.</span><span class="sxs-lookup"><span data-stu-id="948ec-105">Closes the form.</span></span>
  
```cpp
HRESULT ShutdownForm(
  ULONG ulSaveOptions
);
```

## <a name="parameters"></a><span data-ttu-id="948ec-106">Paramètres</span><span class="sxs-lookup"><span data-stu-id="948ec-106">Parameters</span></span>

 <span data-ttu-id="948ec-107">_ulSaveOptions_</span><span class="sxs-lookup"><span data-stu-id="948ec-107">_ulSaveOptions_</span></span>
  
> <span data-ttu-id="948ec-108">[in] Une valeur qui détermine comment ou si les données du formulaire sont enregistrées avant la fermeture du formulaire.</span><span class="sxs-lookup"><span data-stu-id="948ec-108">[in] A value that controls how or whether data in the form is saved before the form is closed.</span></span> <span data-ttu-id="948ec-109">Vous pouvez d�finir un des indicateurs suivants :</span><span class="sxs-lookup"><span data-stu-id="948ec-109">One of the following flags can be set:</span></span>
    
<span data-ttu-id="948ec-110">SAVEOPTS_NOSAVE</span><span class="sxs-lookup"><span data-stu-id="948ec-110">SAVEOPTS_NOSAVE</span></span> 
  
> <span data-ttu-id="948ec-111">Les données de formulaire ne doivent pas être enregistrées.</span><span class="sxs-lookup"><span data-stu-id="948ec-111">Form data should not be saved.</span></span>
    
<span data-ttu-id="948ec-112">SAVEOPTS_PROMPTSAVE</span><span class="sxs-lookup"><span data-stu-id="948ec-112">SAVEOPTS_PROMPTSAVE</span></span> 
  
> <span data-ttu-id="948ec-113">L’utilisateur doit être invité à enregistrer des données modifiées dans l’écran.</span><span class="sxs-lookup"><span data-stu-id="948ec-113">The user should be prompted to save any changed data in the form.</span></span>
    
<span data-ttu-id="948ec-114">SAVEOPTS_SAVEIFDIRTY</span><span class="sxs-lookup"><span data-stu-id="948ec-114">SAVEOPTS_SAVEIFDIRTY</span></span> 
  
> <span data-ttu-id="948ec-115">Les données de formulaire doivent être enregistrées si elles ont changé depuis le dernier enregistrement.</span><span class="sxs-lookup"><span data-stu-id="948ec-115">Form data should be saved if it has changed since the last save.</span></span> <span data-ttu-id="948ec-116">Si aucune interface utilisateur n’est affichée, le formulaire peut passer éventuellement à l’aide de la fonctionnalité pour l’option SAVEOPTS_NOSAVE.</span><span class="sxs-lookup"><span data-stu-id="948ec-116">If no user interface is being displayed, the form can optionally switch to using the functionality for the SAVEOPTS_NOSAVE option.</span></span>
    
## <a name="return-value"></a><span data-ttu-id="948ec-117">Valeur renvoyée</span><span class="sxs-lookup"><span data-stu-id="948ec-117">Return value</span></span>

<span data-ttu-id="948ec-118">S_OK</span><span class="sxs-lookup"><span data-stu-id="948ec-118">S_OK</span></span> 
  
> <span data-ttu-id="948ec-119">Le formulaire a été fermé.</span><span class="sxs-lookup"><span data-stu-id="948ec-119">The form was closed.</span></span>
    
<span data-ttu-id="948ec-120">E_UNEXPECTED</span><span class="sxs-lookup"><span data-stu-id="948ec-120">E_UNEXPECTED</span></span> 
  
> <span data-ttu-id="948ec-121">Le formulaire a été fermé déjà par un appel précédent à **ShutdownForm**.</span><span class="sxs-lookup"><span data-stu-id="948ec-121">The form was already closed by a prior call to **ShutdownForm**.</span></span>
    
## <a name="remarks"></a><span data-ttu-id="948ec-122">Remarques</span><span class="sxs-lookup"><span data-stu-id="948ec-122">Remarks</span></span>

<span data-ttu-id="948ec-123">Visionneuses de formulaire appeler la méthode **IMAPIForm::ShutdownForm** pour fermer un formulaire.</span><span class="sxs-lookup"><span data-stu-id="948ec-123">Form viewers call the **IMAPIForm::ShutdownForm** method to close a form.</span></span> 
  
## <a name="notes-to-implementers"></a><span data-ttu-id="948ec-124">Remarques à l’attention des responsables de l’implémentation</span><span class="sxs-lookup"><span data-stu-id="948ec-124">Notes to implementers</span></span>

<span data-ttu-id="948ec-125">Dans votre implémentation de **ShutdownForm**, effectuez les tâches suivantes :</span><span class="sxs-lookup"><span data-stu-id="948ec-125">Perform the following tasks in your implementation of **ShutdownForm**:</span></span>
  
1. <span data-ttu-id="948ec-126">Vérifiez qu’une visionneuse n’a pas déjà appelée **ShutdownForm**et retourner E_UNEXPECTED si elle a.</span><span class="sxs-lookup"><span data-stu-id="948ec-126">Check that a viewer has not already called **ShutdownForm**, and return E_UNEXPECTED if it has.</span></span> <span data-ttu-id="948ec-127">Bien qu’il s’agit probablement pas, vous devez vérifier.</span><span class="sxs-lookup"><span data-stu-id="948ec-127">Although this is unlikely, you should check.</span></span>
    
2. <span data-ttu-id="948ec-128">Appelez la méthode de [IUnknown::AddRef](https://msdn.microsoft.com/library/ms691379%28VS.85%29.aspx) de votre formulaire afin que le stockage pour le formulaire et les structures de données internes restent disponibles que le traitement est terminé.</span><span class="sxs-lookup"><span data-stu-id="948ec-128">Call your form's [IUnknown::AddRef](https://msdn.microsoft.com/library/ms691379%28VS.85%29.aspx) method so that storage for the form and any internal data structures remain available until processing is finished.</span></span> 
    
3. <span data-ttu-id="948ec-129">Déterminer s’il existe des modifications non enregistrées pour les données du formulaire.</span><span class="sxs-lookup"><span data-stu-id="948ec-129">Determine whether there are any unsaved changes to the form's data.</span></span> <span data-ttu-id="948ec-130">Enregistrer les données non enregistrées en fonction de la façon dont le paramètre _ulSaveOptions_ est défini en appelant la méthode [IMAPIMessageSite::SaveMessage](imapimessagesite-savemessage.md) de votre la visionneuse.</span><span class="sxs-lookup"><span data-stu-id="948ec-130">Save unsaved data according to how the  _ulSaveOptions_ parameter is set by calling your viewer's [IMAPIMessageSite::SaveMessage](imapimessagesite-savemessage.md) method.</span></span> 
    
4. <span data-ttu-id="948ec-131">Détruire la fenêtre de l’interface utilisateur de votre formulaire.</span><span class="sxs-lookup"><span data-stu-id="948ec-131">Destroy your form's user interface window.</span></span>
    
5. <span data-ttu-id="948ec-132">Libérer le message et les objets du site de votre formulaire en appelant leurs méthodes [IUnknown::Release](https://msdn.microsoft.com/library/ms682317%28v=VS.85%29.aspx) .</span><span class="sxs-lookup"><span data-stu-id="948ec-132">Release your form's message and message site objects by calling their [IUnknown::Release](https://msdn.microsoft.com/library/ms682317%28v=VS.85%29.aspx) methods.</span></span> 
    
6. <span data-ttu-id="948ec-133">Avertir inscrits toutes les visionneuses de l’arrêt en attente en appelant leurs méthodes [IMAPIViewAdviseSink::OnShutdown](imapiviewadvisesink-onshutdown.md) .</span><span class="sxs-lookup"><span data-stu-id="948ec-133">Notify all registered viewers of the pending shutdown by calling their [IMAPIViewAdviseSink::OnShutdown](imapiviewadvisesink-onshutdown.md) methods.</span></span> 
    
7. <span data-ttu-id="948ec-134">Appelez la méthode [IMAPIViewContext::SetAdviseSink](imapiviewcontext-setadvisesink.md) pour annuler l’inscription de votre formulaire de notification en définissant le pointeur du récepteur advise sur **null**.</span><span class="sxs-lookup"><span data-stu-id="948ec-134">Call the [IMAPIViewContext::SetAdviseSink](imapiviewcontext-setadvisesink.md) method to cancel your form's registration for notification by setting the advise sink pointer to **null**.</span></span>
    
8. <span data-ttu-id="948ec-135">Appelez la fonction [MAPIFreeBuffer](mapifreebuffer.md) pour libérer de la mémoire des propriétés de votre formulaire.</span><span class="sxs-lookup"><span data-stu-id="948ec-135">Call the [MAPIFreeBuffer](mapifreebuffer.md) function to free the memory for your form's properties.</span></span> 
    
9. <span data-ttu-id="948ec-136">Appelez la méthode **IUnknown::Release** de votre formulaire, correspondant à l’appel de **AddRef** effectuée à l’étape 2.</span><span class="sxs-lookup"><span data-stu-id="948ec-136">Call your form's **IUnknown::Release** method, matching the **AddRef** call made in step 2.</span></span> 
    
10. <span data-ttu-id="948ec-137">Elles retournent S_OK.</span><span class="sxs-lookup"><span data-stu-id="948ec-137">Return S_OK.</span></span>
    
> [!NOTE]
> <span data-ttu-id="948ec-138">Une fois ces opérations terminées, les méthodes sur l’objet form qui peut être appelée uniquement valides sont celles de l’interface [IUnknown](https://msdn.microsoft.com/library/ms680509%28v=VS.85%29.aspx) .</span><span class="sxs-lookup"><span data-stu-id="948ec-138">After these actions have been completed, the only valid methods on the form object that may be called are those from the [IUnknown](https://msdn.microsoft.com/library/ms680509%28v=VS.85%29.aspx) interface.</span></span> 
  
## <a name="notes-to-callers"></a><span data-ttu-id="948ec-139">Notes aux appelants</span><span class="sxs-lookup"><span data-stu-id="948ec-139">Notes to callers</span></span>

<span data-ttu-id="948ec-140">Lorsque **ShutdownForm** renvoie, indépendamment de si elle renvoie une erreur, relâchez le formulaire en appelant la méthode **IUnknown::Release** .</span><span class="sxs-lookup"><span data-stu-id="948ec-140">When **ShutdownForm** returns, regardless of whether it returns an error, release the form by calling its **IUnknown::Release** method.</span></span> <span data-ttu-id="948ec-141">Vous pouvez ignorer les erreurs retournées par **ShutdownForm**.</span><span class="sxs-lookup"><span data-stu-id="948ec-141">You can safely ignore any errors returned by **ShutdownForm**.</span></span>
  
## <a name="see-also"></a><span data-ttu-id="948ec-142">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="948ec-142">See also</span></span>



[<span data-ttu-id="948ec-143">IMAPIMessageSite::SaveMessage</span><span class="sxs-lookup"><span data-stu-id="948ec-143">IMAPIMessageSite::SaveMessage</span></span>](imapimessagesite-savemessage.md)
  
[<span data-ttu-id="948ec-144">IMAPIViewAdviseSink::OnShutdown</span><span class="sxs-lookup"><span data-stu-id="948ec-144">IMAPIViewAdviseSink::OnShutdown</span></span>](imapiviewadvisesink-onshutdown.md)
  
[<span data-ttu-id="948ec-145">IMAPIViewContext::SetAdviseSink</span><span class="sxs-lookup"><span data-stu-id="948ec-145">IMAPIViewContext::SetAdviseSink</span></span>](imapiviewcontext-setadvisesink.md)
  
[<span data-ttu-id="948ec-146">MAPIFreeBuffer</span><span class="sxs-lookup"><span data-stu-id="948ec-146">MAPIFreeBuffer</span></span>](mapifreebuffer.md)
  
[<span data-ttu-id="948ec-147">IMAPIForm : IUnknown</span><span class="sxs-lookup"><span data-stu-id="948ec-147">IMAPIForm : IUnknown</span></span>](imapiformiunknown.md)

