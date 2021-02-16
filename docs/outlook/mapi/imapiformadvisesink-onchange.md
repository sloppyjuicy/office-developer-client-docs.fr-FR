---
title: IMAPIFormAdviseSinkOnChange
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- IMAPIFormAdviseSink.OnChange
api_type:
- COM
ms.assetid: d700b40f-e5b2-4d37-bf1f-8fd3dfa0dda5
description: 'Derniére modification : samedi 23 juillet 2011'
ms.openlocfilehash: 02663570e3173bbd696af732e71f060d9dee49bc
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/28/2019
ms.locfileid: "33431896"
---
# <a name="imapiformadvisesinkonchange"></a><span data-ttu-id="d6352-103">IMAPIFormAdviseSink::OnChange</span><span class="sxs-lookup"><span data-stu-id="d6352-103">IMAPIFormAdviseSink::OnChange</span></span>

  
  
<span data-ttu-id="d6352-104">**S’applique à** : Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="d6352-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="d6352-105">Indique qu’une modification s’est produite dans l’état de la visionneuse de formulaires.</span><span class="sxs-lookup"><span data-stu-id="d6352-105">Indicates that a change has occurred in the status of the form viewer.</span></span> 
  
```cpp
HRESULT OnChange(
  ULONG ulDir
);
```

## <a name="parameters"></a><span data-ttu-id="d6352-106">Paramètres</span><span class="sxs-lookup"><span data-stu-id="d6352-106">Parameters</span></span>

 <span data-ttu-id="d6352-107">_ulDir_</span><span class="sxs-lookup"><span data-stu-id="d6352-107">_ulDir_</span></span>
  
> <span data-ttu-id="d6352-108">[in] Masque de bits d’indicateurs qui fournit des informations sur la modification qui s’est produite dans la visionneuse et la réponse attendue dans le formulaire.</span><span class="sxs-lookup"><span data-stu-id="d6352-108">[in] A bitmask of flags that provides information about the change that has occurred in the viewer and the expected response in the form.</span></span> <span data-ttu-id="d6352-109">Les indicateurs suivants peuvent être définies :</span><span class="sxs-lookup"><span data-stu-id="d6352-109">The following flags can be set:</span></span>
    
<span data-ttu-id="d6352-110">VCSTATUS_CATEGORY</span><span class="sxs-lookup"><span data-stu-id="d6352-110">VCSTATUS_CATEGORY</span></span> 
  
> <span data-ttu-id="d6352-111">Il existe un message suivant ou précédent dans une autre catégorie.</span><span class="sxs-lookup"><span data-stu-id="d6352-111">There is a next or previous message in another category.</span></span> 
    
<span data-ttu-id="d6352-112">VCSTATUS_INTERACTIVE</span><span class="sxs-lookup"><span data-stu-id="d6352-112">VCSTATUS_INTERACTIVE</span></span> 
  
> <span data-ttu-id="d6352-113">Le formulaire doit afficher une interface utilisateur.</span><span class="sxs-lookup"><span data-stu-id="d6352-113">The form should display a user interface.</span></span> <span data-ttu-id="d6352-114">Si cet indicateur n’est pas définie, le formulaire doit supprimer l’affichage d’une interface utilisateur, même en réponse à un verbe qui entraîne généralement l’affichage d’une interface utilisateur.</span><span class="sxs-lookup"><span data-stu-id="d6352-114">If this flag is not set, the form should suppress displaying a user interface, even in response to a verb that usually causes a user interface to be displayed.</span></span> 
    
<span data-ttu-id="d6352-115">VCSTATUS_MODAL</span><span class="sxs-lookup"><span data-stu-id="d6352-115">VCSTATUS_MODAL</span></span> 
  
> <span data-ttu-id="d6352-116">Le formulaire doit être modal pour la visionneuse de formulaires.</span><span class="sxs-lookup"><span data-stu-id="d6352-116">The form is to be modal to the form viewer.</span></span> 
    
<span data-ttu-id="d6352-117">VCSTATUS_NEXT</span><span class="sxs-lookup"><span data-stu-id="d6352-117">VCSTATUS_NEXT</span></span> 
  
> <span data-ttu-id="d6352-118">Il y a un message suivant dans la visionneuse de formulaires.</span><span class="sxs-lookup"><span data-stu-id="d6352-118">There is a next message in the form viewer.</span></span> 
    
<span data-ttu-id="d6352-119">VCSTATUS_PREV</span><span class="sxs-lookup"><span data-stu-id="d6352-119">VCSTATUS_PREV</span></span> 
  
> <span data-ttu-id="d6352-120">Il existe un message précédent dans la visionneuse de formulaires.</span><span class="sxs-lookup"><span data-stu-id="d6352-120">There is a previous message in the form viewer.</span></span> 
    
<span data-ttu-id="d6352-121">VCSTATUS_READONLY</span><span class="sxs-lookup"><span data-stu-id="d6352-121">VCSTATUS_READONLY</span></span> 
  
> <span data-ttu-id="d6352-122">Les opérations de suppression, d’soumission et de déplacement doivent être désactivées.</span><span class="sxs-lookup"><span data-stu-id="d6352-122">Delete, submit, and move operations should be disabled.</span></span> 
    
<span data-ttu-id="d6352-123">VCSTATUS_UNREAD</span><span class="sxs-lookup"><span data-stu-id="d6352-123">VCSTATUS_UNREAD</span></span> 
  
> <span data-ttu-id="d6352-124">Il existe un message non lu suivant ou précédent dans la visionneuse de formulaires.</span><span class="sxs-lookup"><span data-stu-id="d6352-124">There is a next or previous unread message in the form viewer.</span></span>
    
## <a name="return-value"></a><span data-ttu-id="d6352-125">Valeur renvoyée</span><span class="sxs-lookup"><span data-stu-id="d6352-125">Return value</span></span>

<span data-ttu-id="d6352-126">S_OK</span><span class="sxs-lookup"><span data-stu-id="d6352-126">S_OK</span></span> 
  
> <span data-ttu-id="d6352-127">La notification a réussi.</span><span class="sxs-lookup"><span data-stu-id="d6352-127">The notification was successful.</span></span>
    
## <a name="remarks"></a><span data-ttu-id="d6352-128">Remarques</span><span class="sxs-lookup"><span data-stu-id="d6352-128">Remarks</span></span>

<span data-ttu-id="d6352-129">Les visionneuses de formulaires appellent la méthode **IMAPIFormAdviseSink::OnChange** pour informer le formulaire d’une modification de l’état d’une visionneuse.</span><span class="sxs-lookup"><span data-stu-id="d6352-129">Form viewers call the **IMAPIFormAdviseSink::OnChange** method to notify the form about a change in a viewer's status.</span></span> <span data-ttu-id="d6352-130">En règle générale, la seule modification consiste à définir ou effacer l’indicateur VCSTATUS_NEXT ou VCSTATUS_PREVIOUS en fonction de la présence ou de l’absence d’un message suivant ou précédent dans la visionneuse.</span><span class="sxs-lookup"><span data-stu-id="d6352-130">Usually, the only change is setting or clearing the VCSTATUS_NEXT or VCSTATUS_PREVIOUS flag based on the presence or absence of a next or previous message in the viewer.</span></span> <span data-ttu-id="d6352-131">Par conséquent, l’objet formulaire active ou désactive les actions suivantes ou précédentes qu’il prend en charge.</span><span class="sxs-lookup"><span data-stu-id="d6352-131">Accordingly, the form object then enables or disables any next or previous actions it supports.</span></span> 
  
<span data-ttu-id="d6352-132">Les paramètres des VCSTATUS_MODAL et VCSTATUS_INTERACTIVE ne peuvent pas être changés dans un contexte d’affichage après sa création.</span><span class="sxs-lookup"><span data-stu-id="d6352-132">The settings of VCSTATUS_MODAL and VCSTATUS_INTERACTIVE cannot change in a view context after it has been created.</span></span>
  
## <a name="notes-to-implementers"></a><span data-ttu-id="d6352-133">Remarques pour les responsables de l’implémentation</span><span class="sxs-lookup"><span data-stu-id="d6352-133">Notes to implementers</span></span>

<span data-ttu-id="d6352-134">L’implémentation spécifique de cette méthode dépend complètement des spécificités du formulaire.</span><span class="sxs-lookup"><span data-stu-id="d6352-134">The specific implementation of this method is completely dependent on the specifics of the form.</span></span> <span data-ttu-id="d6352-135">La plupart des objets de formulaire utilisent cette méthode pour modifier leur interface utilisateur (par exemple, pour activer ou désactiver des commandes de menu ou des boutons pour qu’ils correspondent au paramètre d’indicateur d’état de la visionneuse).</span><span class="sxs-lookup"><span data-stu-id="d6352-135">Most form objects use this method to change their user interface (for example, to enable or disable menu commands or buttons to match the viewer status flags parameter).</span></span>
  
## <a name="see-also"></a><span data-ttu-id="d6352-136">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="d6352-136">See also</span></span>



[<span data-ttu-id="d6352-137">IMAPIViewContext::ActivateNext</span><span class="sxs-lookup"><span data-stu-id="d6352-137">IMAPIViewContext::ActivateNext</span></span>](imapiviewcontext-activatenext.md)
  
[<span data-ttu-id="d6352-138">IMAPIFormAdviseSink : IUnknown</span><span class="sxs-lookup"><span data-stu-id="d6352-138">IMAPIFormAdviseSink : IUnknown</span></span>](imapiformadvisesinkiunknown.md)

