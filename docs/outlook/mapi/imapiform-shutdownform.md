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
description: 'Dernière modification : 23 juillet 2011'
ms.openlocfilehash: 073a76766a296d86e7a23809921b832d494a8f1b
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32329476"
---
# <a name="imapiformshutdownform"></a><span data-ttu-id="ad212-103">IMAPIForm::ShutdownForm</span><span class="sxs-lookup"><span data-stu-id="ad212-103">IMAPIForm::ShutdownForm</span></span>

  
  
<span data-ttu-id="ad212-104">**S’applique à** : Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="ad212-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="ad212-105">Ferme le formulaire.</span><span class="sxs-lookup"><span data-stu-id="ad212-105">Closes the form.</span></span>
  
```cpp
HRESULT ShutdownForm(
  ULONG ulSaveOptions
);
```

## <a name="parameters"></a><span data-ttu-id="ad212-106">Paramètres</span><span class="sxs-lookup"><span data-stu-id="ad212-106">Parameters</span></span>

 <span data-ttu-id="ad212-107">_ulSaveOptions_</span><span class="sxs-lookup"><span data-stu-id="ad212-107">_ulSaveOptions_</span></span>
  
> <span data-ttu-id="ad212-108">dans Valeur qui contrôle comment ou si les données du formulaire sont enregistrées avant la fermeture du formulaire.</span><span class="sxs-lookup"><span data-stu-id="ad212-108">[in] A value that controls how or whether data in the form is saved before the form is closed.</span></span> <span data-ttu-id="ad212-109">Vous pouvez d�finir un des indicateurs suivants :</span><span class="sxs-lookup"><span data-stu-id="ad212-109">One of the following flags can be set:</span></span>
    
<span data-ttu-id="ad212-110">SAVEOPTS_NOSAVE</span><span class="sxs-lookup"><span data-stu-id="ad212-110">SAVEOPTS_NOSAVE</span></span> 
  
> <span data-ttu-id="ad212-111">Les données de formulaire ne doivent pas être enregistrées.</span><span class="sxs-lookup"><span data-stu-id="ad212-111">Form data should not be saved.</span></span>
    
<span data-ttu-id="ad212-112">SAVEOPTS_PROMPTSAVE</span><span class="sxs-lookup"><span data-stu-id="ad212-112">SAVEOPTS_PROMPTSAVE</span></span> 
  
> <span data-ttu-id="ad212-113">L'utilisateur doit être invité à enregistrer toutes les données modifiées dans le formulaire.</span><span class="sxs-lookup"><span data-stu-id="ad212-113">The user should be prompted to save any changed data in the form.</span></span>
    
<span data-ttu-id="ad212-114">SAVEOPTS_SAVEIFDIRTY</span><span class="sxs-lookup"><span data-stu-id="ad212-114">SAVEOPTS_SAVEIFDIRTY</span></span> 
  
> <span data-ttu-id="ad212-115">Les données de formulaire doivent être enregistrées si elles ont été modifiées depuis le dernier enregistrement.</span><span class="sxs-lookup"><span data-stu-id="ad212-115">Form data should be saved if it has changed since the last save.</span></span> <span data-ttu-id="ad212-116">Si aucune interface utilisateur n'est affichée, le formulaire peut éventuellement passer à l'aide de la fonctionnalité de l'option SAVEOPTS_NOSAVE.</span><span class="sxs-lookup"><span data-stu-id="ad212-116">If no user interface is being displayed, the form can optionally switch to using the functionality for the SAVEOPTS_NOSAVE option.</span></span>
    
## <a name="return-value"></a><span data-ttu-id="ad212-117">Valeur renvoyée</span><span class="sxs-lookup"><span data-stu-id="ad212-117">Return value</span></span>

<span data-ttu-id="ad212-118">S_OK</span><span class="sxs-lookup"><span data-stu-id="ad212-118">S_OK</span></span> 
  
> <span data-ttu-id="ad212-119">Le formulaire a été fermé.</span><span class="sxs-lookup"><span data-stu-id="ad212-119">The form was closed.</span></span>
    
<span data-ttu-id="ad212-120">E_UNEXPECTED</span><span class="sxs-lookup"><span data-stu-id="ad212-120">E_UNEXPECTED</span></span> 
  
> <span data-ttu-id="ad212-121">Le formulaire a déjà été fermé par un appel antérieur à **ShutdownForm**.</span><span class="sxs-lookup"><span data-stu-id="ad212-121">The form was already closed by a prior call to **ShutdownForm**.</span></span>
    
## <a name="remarks"></a><span data-ttu-id="ad212-122">Remarques</span><span class="sxs-lookup"><span data-stu-id="ad212-122">Remarks</span></span>

<span data-ttu-id="ad212-123">Les visionneuses de formulaires appellent la méthode **IMAPIForm:: ShutdownForm** pour fermer un formulaire.</span><span class="sxs-lookup"><span data-stu-id="ad212-123">Form viewers call the **IMAPIForm::ShutdownForm** method to close a form.</span></span> 
  
## <a name="notes-to-implementers"></a><span data-ttu-id="ad212-124">Remarques pour les responsables de l’implémentation</span><span class="sxs-lookup"><span data-stu-id="ad212-124">Notes to implementers</span></span>

<span data-ttu-id="ad212-125">Effectuez les tâches suivantes dans votre implémentation de **ShutdownForm**:</span><span class="sxs-lookup"><span data-stu-id="ad212-125">Perform the following tasks in your implementation of **ShutdownForm**:</span></span>
  
1. <span data-ttu-id="ad212-126">Vérifiez qu'un visionneur n'a pas déjà appelé **ShutdownForm**et renvoyé E_UNEXPECTED, le cas échéant.</span><span class="sxs-lookup"><span data-stu-id="ad212-126">Check that a viewer has not already called **ShutdownForm**, and return E_UNEXPECTED if it has.</span></span> <span data-ttu-id="ad212-127">Bien que cela soit improbable, vérifiez.</span><span class="sxs-lookup"><span data-stu-id="ad212-127">Although this is unlikely, you should check.</span></span>
    
2. <span data-ttu-id="ad212-128">Appelez la méthode [IUnknown:: AddRef](https://msdn.microsoft.com/library/ms691379%28VS.85%29.aspx) de votre formulaire afin que le stockage du formulaire et de toutes les structures de données internes reste disponible jusqu'à ce que le traitement soit terminé.</span><span class="sxs-lookup"><span data-stu-id="ad212-128">Call your form's [IUnknown::AddRef](https://msdn.microsoft.com/library/ms691379%28VS.85%29.aspx) method so that storage for the form and any internal data structures remain available until processing is finished.</span></span> 
    
3. <span data-ttu-id="ad212-129">Déterminez s'il existe des modifications non enregistrées sur les données du formulaire.</span><span class="sxs-lookup"><span data-stu-id="ad212-129">Determine whether there are any unsaved changes to the form's data.</span></span> <span data-ttu-id="ad212-130">Enregistrer les données non enregistrées en fonction de la définition du paramètre _ulSaveOptions_ en appelant la méthode [IMAPIMessageSite:: SaveMessage](imapimessagesite-savemessage.md) de votre visionneuse.</span><span class="sxs-lookup"><span data-stu-id="ad212-130">Save unsaved data according to how the  _ulSaveOptions_ parameter is set by calling your viewer's [IMAPIMessageSite::SaveMessage](imapimessagesite-savemessage.md) method.</span></span> 
    
4. <span data-ttu-id="ad212-131">Détruisez la fenêtre de l'interface utilisateur de votre formulaire.</span><span class="sxs-lookup"><span data-stu-id="ad212-131">Destroy your form's user interface window.</span></span>
    
5. <span data-ttu-id="ad212-132">Libérez les objets de site et de message de votre formulaire en appelant leurs méthodes [IUnknown:: Release](https://msdn.microsoft.com/library/ms682317%28v=VS.85%29.aspx) .</span><span class="sxs-lookup"><span data-stu-id="ad212-132">Release your form's message and message site objects by calling their [IUnknown::Release](https://msdn.microsoft.com/library/ms682317%28v=VS.85%29.aspx) methods.</span></span> 
    
6. <span data-ttu-id="ad212-133">Notifier toutes les visionneuses inscrites de l'arrêt en attente en appelant leurs méthodes [IMAPIViewAdviseSink:: OnShutdown](imapiviewadvisesink-onshutdown.md) .</span><span class="sxs-lookup"><span data-stu-id="ad212-133">Notify all registered viewers of the pending shutdown by calling their [IMAPIViewAdviseSink::OnShutdown](imapiviewadvisesink-onshutdown.md) methods.</span></span> 
    
7. <span data-ttu-id="ad212-134">Appelez la méthode [IMAPIViewContext:: SetAdviseSink](imapiviewcontext-setadvisesink.md) pour annuler l'inscription de votre formulaire pour la notification en définissant le pointeur du récepteur de notifications sur **null**.</span><span class="sxs-lookup"><span data-stu-id="ad212-134">Call the [IMAPIViewContext::SetAdviseSink](imapiviewcontext-setadvisesink.md) method to cancel your form's registration for notification by setting the advise sink pointer to **null**.</span></span>
    
8. <span data-ttu-id="ad212-135">Appelez la fonction [MAPIFreeBuffer](mapifreebuffer.md) pour libérer de la mémoire pour les propriétés de votre formulaire.</span><span class="sxs-lookup"><span data-stu-id="ad212-135">Call the [MAPIFreeBuffer](mapifreebuffer.md) function to free the memory for your form's properties.</span></span> 
    
9. <span data-ttu-id="ad212-136">Appelez la méthode **IUnknown:: Release** de votre formulaire, correspondant à l'appel de **AddRef** effectué à l'étape 2.</span><span class="sxs-lookup"><span data-stu-id="ad212-136">Call your form's **IUnknown::Release** method, matching the **AddRef** call made in step 2.</span></span> 
    
10. <span data-ttu-id="ad212-137">Elles retournent S_OK.</span><span class="sxs-lookup"><span data-stu-id="ad212-137">Return S_OK.</span></span>
    
> [!NOTE]
> <span data-ttu-id="ad212-138">Une fois ces actions terminées, les seules méthodes valides sur l'objet Form qui peuvent être appelées sont celles de l'interface [IUnknown](https://msdn.microsoft.com/library/ms680509%28v=VS.85%29.aspx) .</span><span class="sxs-lookup"><span data-stu-id="ad212-138">After these actions have been completed, the only valid methods on the form object that may be called are those from the [IUnknown](https://msdn.microsoft.com/library/ms680509%28v=VS.85%29.aspx) interface.</span></span> 
  
## <a name="notes-to-callers"></a><span data-ttu-id="ad212-139">Remarques pour les appelants</span><span class="sxs-lookup"><span data-stu-id="ad212-139">Notes to callers</span></span>

<span data-ttu-id="ad212-140">Lorsque **ShutdownForm** renvoie, qu'il renvoie ou non une erreur, libérez le formulaire en appelant sa méthode **IUnknown:: Release** .</span><span class="sxs-lookup"><span data-stu-id="ad212-140">When **ShutdownForm** returns, regardless of whether it returns an error, release the form by calling its **IUnknown::Release** method.</span></span> <span data-ttu-id="ad212-141">Vous pouvez ignorer en toute sécurité les erreurs renvoyées par **ShutdownForm**.</span><span class="sxs-lookup"><span data-stu-id="ad212-141">You can safely ignore any errors returned by **ShutdownForm**.</span></span>
  
## <a name="see-also"></a><span data-ttu-id="ad212-142">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="ad212-142">See also</span></span>



[<span data-ttu-id="ad212-143">IMAPIMessageSite::SaveMessage</span><span class="sxs-lookup"><span data-stu-id="ad212-143">IMAPIMessageSite::SaveMessage</span></span>](imapimessagesite-savemessage.md)
  
[<span data-ttu-id="ad212-144">IMAPIViewAdviseSink::OnShutdown</span><span class="sxs-lookup"><span data-stu-id="ad212-144">IMAPIViewAdviseSink::OnShutdown</span></span>](imapiviewadvisesink-onshutdown.md)
  
[<span data-ttu-id="ad212-145">IMAPIViewContext::SetAdviseSink</span><span class="sxs-lookup"><span data-stu-id="ad212-145">IMAPIViewContext::SetAdviseSink</span></span>](imapiviewcontext-setadvisesink.md)
  
[<span data-ttu-id="ad212-146">MAPIFreeBuffer</span><span class="sxs-lookup"><span data-stu-id="ad212-146">MAPIFreeBuffer</span></span>](mapifreebuffer.md)
  
[<span data-ttu-id="ad212-147">IMAPIForm : IUnknown</span><span class="sxs-lookup"><span data-stu-id="ad212-147">IMAPIForm : IUnknown</span></span>](imapiformiunknown.md)

