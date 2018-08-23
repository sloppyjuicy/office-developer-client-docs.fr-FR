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
description: Dernière modification le 09 mars 2015
ms.openlocfilehash: 26ca126603ac1e695bd14a10cd8d9e637382b2e9
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/23/2018
ms.locfileid: "22584302"
---
# <a name="imapiformsetviewcontext"></a><span data-ttu-id="fe2d5-103">IMAPIForm::SetViewContext</span><span class="sxs-lookup"><span data-stu-id="fe2d5-103">IMAPIForm::SetViewContext</span></span>

  
  
<span data-ttu-id="fe2d5-104">**S’applique à**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="fe2d5-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="fe2d5-105">Établissement d’un contexte de vue pour le formulaire.</span><span class="sxs-lookup"><span data-stu-id="fe2d5-105">Establishes a view context for the form.</span></span> 
  
```cpp
HRESULT SetViewContext(
  LPMAPIVIEWCONTEXT pViewContext
);
```

## <a name="parameters"></a><span data-ttu-id="fe2d5-106">Paramètres</span><span class="sxs-lookup"><span data-stu-id="fe2d5-106">Parameters</span></span>

 <span data-ttu-id="fe2d5-107">_pViewContext_</span><span class="sxs-lookup"><span data-stu-id="fe2d5-107">_pViewContext_</span></span>
  
> <span data-ttu-id="fe2d5-108">[in] Pointeur vers le nouveau contexte de vue pour le formulaire.</span><span class="sxs-lookup"><span data-stu-id="fe2d5-108">[in] A pointer to the new view context for the form.</span></span>
    
## <a name="return-value"></a><span data-ttu-id="fe2d5-109">Valeur renvoy�e</span><span class="sxs-lookup"><span data-stu-id="fe2d5-109">Return value</span></span>

<span data-ttu-id="fe2d5-110">S_OK</span><span class="sxs-lookup"><span data-stu-id="fe2d5-110">S_OK</span></span> 
  
> <span data-ttu-id="fe2d5-111">Le contexte d’affichage a été défini.</span><span class="sxs-lookup"><span data-stu-id="fe2d5-111">The view context was successfully set.</span></span>
    
## <a name="remarks"></a><span data-ttu-id="fe2d5-112">Remarques</span><span class="sxs-lookup"><span data-stu-id="fe2d5-112">Remarks</span></span>

<span data-ttu-id="fe2d5-113">Visionneuses de formulaire appeler la méthode de **IMAPIForm::SetViewContext** pour établir un contexte de vue de formulaire donné comme actif.</span><span class="sxs-lookup"><span data-stu-id="fe2d5-113">Form viewers call the **IMAPIForm::SetViewContext** method to establish a particular form view context as current.</span></span> <span data-ttu-id="fe2d5-114">Un formulaire peut avoir qu’un seul contexte de vue à la fois.</span><span class="sxs-lookup"><span data-stu-id="fe2d5-114">A form can have only one view context at a time.</span></span> 
  
## <a name="notes-to-implementers"></a><span data-ttu-id="fe2d5-115">Remarques destinées aux responsables de l’implémentation</span><span class="sxs-lookup"><span data-stu-id="fe2d5-115">Notes to implementers</span></span>

<span data-ttu-id="fe2d5-116">La plupart des serveurs de formulaire implémenter **SetViewContext** à l’aide de l’algorithme suivant :</span><span class="sxs-lookup"><span data-stu-id="fe2d5-116">Most form servers implement **SetViewContext** by using the following algorithm:</span></span> 
  
- <span data-ttu-id="fe2d5-117">Si un contexte de vue existe déjà pour le formulaire, annuler l’inscription du formulaire en appelant la méthode [IMAPIViewContext::SetAdviseSink](imapiviewcontext-setadvisesink.md) avec la **valeur null** dans le paramètre _pmnvs_ et ensuite appeler [IUnknown::Release du contexte vue](http://msdn.microsoft.com/en-us/library/ms682317%28v=VS.85%29.aspx) méthode décrémente le décompte de références.</span><span class="sxs-lookup"><span data-stu-id="fe2d5-117">If a view context already exists for the form, cancel the form's registration by calling the [IMAPIViewContext::SetAdviseSink](imapiviewcontext-setadvisesink.md) method with **null** in the  _pmnvs_ parameter, and then call the view context's [IUnknown::Release](http://msdn.microsoft.com/en-us/library/ms682317%28v=VS.85%29.aspx) method to decrement its reference count.</span></span> 
    
- <span data-ttu-id="fe2d5-118">Si le contexte d’affichage n’est pas **null**, l’appel **IMAPIViewContext::SetAdviseSink** en utilisant le paramètre _pViewContext_ pour définir un nouvel affichage de notification récepteur.</span><span class="sxs-lookup"><span data-stu-id="fe2d5-118">If the new view context is not **null**, call **IMAPIViewContext::SetAdviseSink** by using the  _pViewContext_ parameter to set up a new view advise sink.</span></span> 
    
- <span data-ttu-id="fe2d5-119">Si le contexte d’affichage n’est pas **null**, appelez la méthode [IMAPIViewContext::GetViewStatus](imapiviewcontext-getviewstatus.md) pour déterminer les indicateurs d’état ont été définies.</span><span class="sxs-lookup"><span data-stu-id="fe2d5-119">If the new view context is not **null**, call the [IMAPIViewContext::GetViewStatus](imapiviewcontext-getviewstatus.md) method to determine which status flags have been set.</span></span> 
    
- <span data-ttu-id="fe2d5-120">Si le contexte d’affichage n’est pas **null**, stocker, appelez la méthode [IUnknown::AddRef](http://msdn.microsoft.com/en-us/library/ms691379%28VS.85%29.aspx) pour incrémenter son décompte de références.</span><span class="sxs-lookup"><span data-stu-id="fe2d5-120">If the new view context is not **null**, store it and call its [IUnknown::AddRef](http://msdn.microsoft.com/en-us/library/ms691379%28VS.85%29.aspx) method to increment its reference count.</span></span> 
    
- <span data-ttu-id="fe2d5-121">Mettre à jour les éléments d’interface utilisateur qui dépendent du contexte d’affichage.</span><span class="sxs-lookup"><span data-stu-id="fe2d5-121">Update any user interface elements that depend on the view context.</span></span> 
    
<span data-ttu-id="fe2d5-122">Selon les indicateurs d’état renvoyés par **IMAPIViewContext::GetViewStatus**, **SetViewContext** peut également exécuter d’autres actions.</span><span class="sxs-lookup"><span data-stu-id="fe2d5-122">Depending on the status flags returned from **IMAPIViewContext::GetViewStatus**, **SetViewContext** can also perform other actions.</span></span> <span data-ttu-id="fe2d5-123">Par exemple, si les indicateurs VCSTATUS_NEXT et VCSTATUS_PREV sont renvoyés, **SetViewContext** peut activer les boutons **suivant** et **précédent** pour le contexte d’affichage.</span><span class="sxs-lookup"><span data-stu-id="fe2d5-123">For example, if the VCSTATUS_NEXT and VCSTATUS_PREV flags are returned, **SetViewContext** can enable the **Next** and **Previous** buttons for the new view context.</span></span> 
  
## <a name="mfcmapi-reference"></a><span data-ttu-id="fe2d5-124">Référence MFCMAPI</span><span class="sxs-lookup"><span data-stu-id="fe2d5-124">MFCMAPI reference</span></span>

<span data-ttu-id="fe2d5-125">Pour des exemples de code MFCMAPI, voir le tableau suivant.</span><span class="sxs-lookup"><span data-stu-id="fe2d5-125">For MFCMAPI sample code, see the following table.</span></span>
  
|<span data-ttu-id="fe2d5-126">**Fichier**</span><span class="sxs-lookup"><span data-stu-id="fe2d5-126">**File**</span></span>|<span data-ttu-id="fe2d5-127">**Fonction**</span><span class="sxs-lookup"><span data-stu-id="fe2d5-127">**Function**</span></span>|<span data-ttu-id="fe2d5-128">**Commentaire**</span><span class="sxs-lookup"><span data-stu-id="fe2d5-128">**Comment**</span></span>|
|:-----|:-----|:-----|
|<span data-ttu-id="fe2d5-129">MAPIFormFunctions.cpp</span><span class="sxs-lookup"><span data-stu-id="fe2d5-129">MAPIFormFunctions.cpp</span></span>  <br/> |<span data-ttu-id="fe2d5-130">CreateAndDisplayNewMailInFolder</span><span class="sxs-lookup"><span data-stu-id="fe2d5-130">CreateAndDisplayNewMailInFolder</span></span>  <br/> |<span data-ttu-id="fe2d5-131">MFCMAPI utilise la méthode **IMAPIForm::SetViewContext** pour définir le contexte de vue de MFCMAPI sur le formulaire avant que le formulaire s’affiche.</span><span class="sxs-lookup"><span data-stu-id="fe2d5-131">MFCMAPI uses the **IMAPIForm::SetViewContext** method to set MFCMAPI's view context on the form before the form is displayed.</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="fe2d5-132">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="fe2d5-132">See also</span></span>



[<span data-ttu-id="fe2d5-133">IMAPIViewContext::GetViewStatus</span><span class="sxs-lookup"><span data-stu-id="fe2d5-133">IMAPIViewContext::GetViewStatus</span></span>](imapiviewcontext-getviewstatus.md)
  
[<span data-ttu-id="fe2d5-134">IMAPIViewContext::SetAdviseSink</span><span class="sxs-lookup"><span data-stu-id="fe2d5-134">IMAPIViewContext::SetAdviseSink</span></span>](imapiviewcontext-setadvisesink.md)
  
[<span data-ttu-id="fe2d5-135">IMAPIForm : IUnknown</span><span class="sxs-lookup"><span data-stu-id="fe2d5-135">IMAPIForm : IUnknown</span></span>](imapiformiunknown.md)


[<span data-ttu-id="fe2d5-136">MFCMAPI comme un exemple de Code</span><span class="sxs-lookup"><span data-stu-id="fe2d5-136">MFCMAPI as a Code Sample</span></span>](mfcmapi-as-a-code-sample.md)

