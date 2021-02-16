---
title: IMAPIFormSetViewContext
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- IMAPIForm.SetViewContext
api_type:
- COM
ms.assetid: a7b10007-42d8-4755-8362-f8ad9a8dad68
description: Dernière modification le 9 mars 2015
ms.openlocfilehash: 81d99b2bbe6ef7914a4b7d253a3472026872260d
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32350945"
---
# <a name="imapiformsetviewcontext"></a><span data-ttu-id="3f719-103">IMAPIForm::SetViewContext</span><span class="sxs-lookup"><span data-stu-id="3f719-103">IMAPIForm::SetViewContext</span></span>

  
  
<span data-ttu-id="3f719-104">**S’applique à** : Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="3f719-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="3f719-105">Établit un contexte d’affichage pour le formulaire.</span><span class="sxs-lookup"><span data-stu-id="3f719-105">Establishes a view context for the form.</span></span> 
  
```cpp
HRESULT SetViewContext(
  LPMAPIVIEWCONTEXT pViewContext
);
```

## <a name="parameters"></a><span data-ttu-id="3f719-106">Paramètres</span><span class="sxs-lookup"><span data-stu-id="3f719-106">Parameters</span></span>

 <span data-ttu-id="3f719-107">_pViewContext_</span><span class="sxs-lookup"><span data-stu-id="3f719-107">_pViewContext_</span></span>
  
> <span data-ttu-id="3f719-108">[in] Pointeur vers le nouveau contexte d’affichage du formulaire.</span><span class="sxs-lookup"><span data-stu-id="3f719-108">[in] A pointer to the new view context for the form.</span></span>
    
## <a name="return-value"></a><span data-ttu-id="3f719-109">Valeur renvoyée</span><span class="sxs-lookup"><span data-stu-id="3f719-109">Return value</span></span>

<span data-ttu-id="3f719-110">S_OK</span><span class="sxs-lookup"><span data-stu-id="3f719-110">S_OK</span></span> 
  
> <span data-ttu-id="3f719-111">Le contexte d’affichage a été correctement définie.</span><span class="sxs-lookup"><span data-stu-id="3f719-111">The view context was successfully set.</span></span>
    
## <a name="remarks"></a><span data-ttu-id="3f719-112">Remarques</span><span class="sxs-lookup"><span data-stu-id="3f719-112">Remarks</span></span>

<span data-ttu-id="3f719-113">Les visionneuses de formulaires appellent la méthode **IMAPIForm::SetViewContext** pour établir un contexte d’affichage de formulaire particulier comme étant actuel.</span><span class="sxs-lookup"><span data-stu-id="3f719-113">Form viewers call the **IMAPIForm::SetViewContext** method to establish a particular form view context as current.</span></span> <span data-ttu-id="3f719-114">Un formulaire ne peut avoir qu’un contexte d’affichage à la fois.</span><span class="sxs-lookup"><span data-stu-id="3f719-114">A form can have only one view context at a time.</span></span> 
  
## <a name="notes-to-implementers"></a><span data-ttu-id="3f719-115">Remarques pour les responsables de l’implémentation</span><span class="sxs-lookup"><span data-stu-id="3f719-115">Notes to implementers</span></span>

<span data-ttu-id="3f719-116">La plupart des serveurs de formulaire **implémentent SetViewContext** à l’aide de l’algorithme suivant :</span><span class="sxs-lookup"><span data-stu-id="3f719-116">Most form servers implement **SetViewContext** by using the following algorithm:</span></span> 
  
- <span data-ttu-id="3f719-117">Si un contexte d’affichage existe déjà pour le formulaire, annulez l’inscription du formulaire en appelant la méthode [IMAPIViewContext::SetAdviseSink](imapiviewcontext-setadvisesink.md) avec la valeur **null** dans le paramètre  _pmnvs,_ puis appelez la méthode [IUnknown::Release](https://msdn.microsoft.com/library/ms682317%28v=VS.85%29.aspx) du contexte d’affichage pour décrémenter son nombre de références.</span><span class="sxs-lookup"><span data-stu-id="3f719-117">If a view context already exists for the form, cancel the form's registration by calling the [IMAPIViewContext::SetAdviseSink](imapiviewcontext-setadvisesink.md) method with **null** in the  _pmnvs_ parameter, and then call the view context's [IUnknown::Release](https://msdn.microsoft.com/library/ms682317%28v=VS.85%29.aspx) method to decrement its reference count.</span></span> 
    
- <span data-ttu-id="3f719-118">Si le nouveau contexte d’affichage n’est pas **null,** appelez **IMAPIViewContext::SetAdviseSink** à l’aide du paramètre  _pViewContext_ pour configurer un nouveau sink de conseil d’affichage.</span><span class="sxs-lookup"><span data-stu-id="3f719-118">If the new view context is not **null**, call **IMAPIViewContext::SetAdviseSink** by using the  _pViewContext_ parameter to set up a new view advise sink.</span></span> 
    
- <span data-ttu-id="3f719-119">Si le nouveau contexte d’affichage n’est pas **null,** appelez la méthode [IMAPIViewContext::GetViewStatus](imapiviewcontext-getviewstatus.md) pour déterminer les indicateurs d’état qui ont été définies.</span><span class="sxs-lookup"><span data-stu-id="3f719-119">If the new view context is not **null**, call the [IMAPIViewContext::GetViewStatus](imapiviewcontext-getviewstatus.md) method to determine which status flags have been set.</span></span> 
    
- <span data-ttu-id="3f719-120">Si le nouveau contexte d’affichage n’est pas **null,** stockez-le et appelez sa méthode [IUnknown::AddRef](https://msdn.microsoft.com/library/ms691379%28VS.85%29.aspx) pour incrémenter son nombre de références.</span><span class="sxs-lookup"><span data-stu-id="3f719-120">If the new view context is not **null**, store it and call its [IUnknown::AddRef](https://msdn.microsoft.com/library/ms691379%28VS.85%29.aspx) method to increment its reference count.</span></span> 
    
- <span data-ttu-id="3f719-121">Mettez à jour tous les éléments de l’interface utilisateur qui dépendent du contexte d’affichage.</span><span class="sxs-lookup"><span data-stu-id="3f719-121">Update any user interface elements that depend on the view context.</span></span> 
    
<span data-ttu-id="3f719-122">Selon les indicateurs d’état renvoyés par **IMAPIViewContext::GetViewStatus**, **SetViewContext** peut également effectuer d’autres actions.</span><span class="sxs-lookup"><span data-stu-id="3f719-122">Depending on the status flags returned from **IMAPIViewContext::GetViewStatus**, **SetViewContext** can also perform other actions.</span></span> <span data-ttu-id="3f719-123">Par exemple, si les indicateurs VCSTATUS_NEXT et VCSTATUS_PREV sont renvoyés, **SetViewContext**  peut activer les boutons Suivant et Précédent pour le nouveau contexte d’affichage. </span><span class="sxs-lookup"><span data-stu-id="3f719-123">For example, if the VCSTATUS_NEXT and VCSTATUS_PREV flags are returned, **SetViewContext** can enable the **Next** and **Previous** buttons for the new view context.</span></span> 
  
## <a name="mfcmapi-reference"></a><span data-ttu-id="3f719-124">Référence MFCMAPI</span><span class="sxs-lookup"><span data-stu-id="3f719-124">MFCMAPI reference</span></span>

<span data-ttu-id="3f719-125">Pour voir un exemple de code MFCMAPI, consultez le tableau suivant.</span><span class="sxs-lookup"><span data-stu-id="3f719-125">For MFCMAPI sample code, see the following table.</span></span>
  
|<span data-ttu-id="3f719-126">**Fichier**</span><span class="sxs-lookup"><span data-stu-id="3f719-126">**File**</span></span>|<span data-ttu-id="3f719-127">**Fonction**</span><span class="sxs-lookup"><span data-stu-id="3f719-127">**Function**</span></span>|<span data-ttu-id="3f719-128">**Commentaire**</span><span class="sxs-lookup"><span data-stu-id="3f719-128">**Comment**</span></span>|
|:-----|:-----|:-----|
|<span data-ttu-id="3f719-129">MAPIFormFunctions.cpp</span><span class="sxs-lookup"><span data-stu-id="3f719-129">MAPIFormFunctions.cpp</span></span>  <br/> |<span data-ttu-id="3f719-130">CreateAndDisplayNewMailInFolder</span><span class="sxs-lookup"><span data-stu-id="3f719-130">CreateAndDisplayNewMailInFolder</span></span>  <br/> |<span data-ttu-id="3f719-131">MFCMAPI utilise la méthode **IMAPIForm::SetViewContext** pour définir le contexte d’affichage de MFCMAPI sur le formulaire avant l’affichage du formulaire.</span><span class="sxs-lookup"><span data-stu-id="3f719-131">MFCMAPI uses the **IMAPIForm::SetViewContext** method to set MFCMAPI's view context on the form before the form is displayed.</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="3f719-132">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="3f719-132">See also</span></span>



[<span data-ttu-id="3f719-133">IMAPIViewContext::GetViewStatus</span><span class="sxs-lookup"><span data-stu-id="3f719-133">IMAPIViewContext::GetViewStatus</span></span>](imapiviewcontext-getviewstatus.md)
  
[<span data-ttu-id="3f719-134">IMAPIViewContext::SetAdviseSink</span><span class="sxs-lookup"><span data-stu-id="3f719-134">IMAPIViewContext::SetAdviseSink</span></span>](imapiviewcontext-setadvisesink.md)
  
[<span data-ttu-id="3f719-135">IMAPIForm : IUnknown</span><span class="sxs-lookup"><span data-stu-id="3f719-135">IMAPIForm : IUnknown</span></span>](imapiformiunknown.md)


[<span data-ttu-id="3f719-136">MFCMAPI comme un exemple de Code</span><span class="sxs-lookup"><span data-stu-id="3f719-136">MFCMAPI as a Code Sample</span></span>](mfcmapi-as-a-code-sample.md)

