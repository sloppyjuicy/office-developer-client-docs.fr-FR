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
ms.openlocfilehash: e32157f41632b782fbacf87e0411c18d167b4279
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/23/2018
ms.locfileid: "22576679"
---
# <a name="imapiformadvisesinkonchange"></a><span data-ttu-id="cebd7-103">IMAPIFormAdviseSink::OnChange</span><span class="sxs-lookup"><span data-stu-id="cebd7-103">IMAPIFormAdviseSink::OnChange</span></span>

  
  
<span data-ttu-id="cebd7-104">**S’applique à**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="cebd7-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="cebd7-105">Indique qu’une modification s’est produite dans l’état de la visionneuse de formulaire.</span><span class="sxs-lookup"><span data-stu-id="cebd7-105">Indicates that a change has occurred in the status of the form viewer.</span></span> 
  
```cpp
HRESULT OnChange(
  ULONG ulDir
);
```

## <a name="parameters"></a><span data-ttu-id="cebd7-106">Paramètres</span><span class="sxs-lookup"><span data-stu-id="cebd7-106">Parameters</span></span>

 <span data-ttu-id="cebd7-107">_ulDir_</span><span class="sxs-lookup"><span data-stu-id="cebd7-107">_ulDir_</span></span>
  
> <span data-ttu-id="cebd7-108">[in] Masque de bits d’indicateurs qui fournit des informations sur la modification s’est produite dans la visionneuse et la réponse attendue dans le formulaire.</span><span class="sxs-lookup"><span data-stu-id="cebd7-108">[in] A bitmask of flags that provides information about the change that has occurred in the viewer and the expected response in the form.</span></span> <span data-ttu-id="cebd7-109">Les indicateurs suivants peuvent être définis :</span><span class="sxs-lookup"><span data-stu-id="cebd7-109">The following flags can be set:</span></span>
    
<span data-ttu-id="cebd7-110">VCSTATUS_CATEGORY</span><span class="sxs-lookup"><span data-stu-id="cebd7-110">VCSTATUS_CATEGORY</span></span> 
  
> <span data-ttu-id="cebd7-111">Il existe un message suivant ou précédent dans une autre catégorie.</span><span class="sxs-lookup"><span data-stu-id="cebd7-111">There is a next or previous message in another category.</span></span> 
    
<span data-ttu-id="cebd7-112">VCSTATUS_INTERACTIVE</span><span class="sxs-lookup"><span data-stu-id="cebd7-112">VCSTATUS_INTERACTIVE</span></span> 
  
> <span data-ttu-id="cebd7-113">Le formulaire doit afficher une interface utilisateur.</span><span class="sxs-lookup"><span data-stu-id="cebd7-113">The form should display a user interface.</span></span> <span data-ttu-id="cebd7-114">Si cet indicateur n’est pas défini, le formulaire doit supprimer l’affichage d’une interface utilisateur, même en réponse à un verbe qui provoque généralement une interface utilisateur à afficher.</span><span class="sxs-lookup"><span data-stu-id="cebd7-114">If this flag is not set, the form should suppress displaying a user interface, even in response to a verb that usually causes a user interface to be displayed.</span></span> 
    
<span data-ttu-id="cebd7-115">VCSTATUS_MODAL</span><span class="sxs-lookup"><span data-stu-id="cebd7-115">VCSTATUS_MODAL</span></span> 
  
> <span data-ttu-id="cebd7-116">Le formulaire est modal à la visionneuse de formulaire.</span><span class="sxs-lookup"><span data-stu-id="cebd7-116">The form is to be modal to the form viewer.</span></span> 
    
<span data-ttu-id="cebd7-117">VCSTATUS_NEXT</span><span class="sxs-lookup"><span data-stu-id="cebd7-117">VCSTATUS_NEXT</span></span> 
  
> <span data-ttu-id="cebd7-118">Il existe un message suivant dans la visionneuse de formulaire.</span><span class="sxs-lookup"><span data-stu-id="cebd7-118">There is a next message in the form viewer.</span></span> 
    
<span data-ttu-id="cebd7-119">VCSTATUS_PREV</span><span class="sxs-lookup"><span data-stu-id="cebd7-119">VCSTATUS_PREV</span></span> 
  
> <span data-ttu-id="cebd7-120">Il existe un message précédent dans la visionneuse de formulaire.</span><span class="sxs-lookup"><span data-stu-id="cebd7-120">There is a previous message in the form viewer.</span></span> 
    
<span data-ttu-id="cebd7-121">VCSTATUS_READONLY</span><span class="sxs-lookup"><span data-stu-id="cebd7-121">VCSTATUS_READONLY</span></span> 
  
> <span data-ttu-id="cebd7-122">Supprimer, soumettre et déplacer des opérations doivent être désactivées.</span><span class="sxs-lookup"><span data-stu-id="cebd7-122">Delete, submit, and move operations should be disabled.</span></span> 
    
<span data-ttu-id="cebd7-123">VCSTATUS_UNREAD</span><span class="sxs-lookup"><span data-stu-id="cebd7-123">VCSTATUS_UNREAD</span></span> 
  
> <span data-ttu-id="cebd7-124">Il existe un message non lu suivant ou précédent dans la visionneuse de formulaire.</span><span class="sxs-lookup"><span data-stu-id="cebd7-124">There is a next or previous unread message in the form viewer.</span></span>
    
## <a name="return-value"></a><span data-ttu-id="cebd7-125">Valeur renvoy�e</span><span class="sxs-lookup"><span data-stu-id="cebd7-125">Return value</span></span>

<span data-ttu-id="cebd7-126">S_OK</span><span class="sxs-lookup"><span data-stu-id="cebd7-126">S_OK</span></span> 
  
> <span data-ttu-id="cebd7-127">La notification a réussi.</span><span class="sxs-lookup"><span data-stu-id="cebd7-127">The notification was successful.</span></span>
    
## <a name="remarks"></a><span data-ttu-id="cebd7-128">Remarques</span><span class="sxs-lookup"><span data-stu-id="cebd7-128">Remarks</span></span>

<span data-ttu-id="cebd7-129">Visionneuses de formulaire appeler la méthode **IMAPIFormAdviseSink::OnChange** pour notifier le formulaire sur un changement d’état d’un utilisateur donné.</span><span class="sxs-lookup"><span data-stu-id="cebd7-129">Form viewers call the **IMAPIFormAdviseSink::OnChange** method to notify the form about a change in a viewer's status.</span></span> <span data-ttu-id="cebd7-130">En règle générale, la seule modification est définir ou effacer l’indicateur VCSTATUS_NEXT ou VCSTATUS_PREVIOUS en fonction de la présence ou non d’un message suivant ou précédent dans la visionneuse.</span><span class="sxs-lookup"><span data-stu-id="cebd7-130">Usually, the only change is setting or clearing the VCSTATUS_NEXT or VCSTATUS_PREVIOUS flag based on the presence or absence of a next or previous message in the viewer.</span></span> <span data-ttu-id="cebd7-131">En conséquence, l’objet form puis l’Active ou désactive toutes les actions suivante ou précédentes que pris en charge.</span><span class="sxs-lookup"><span data-stu-id="cebd7-131">Accordingly, the form object then enables or disables any next or previous actions it supports.</span></span> 
  
<span data-ttu-id="cebd7-132">Impossible de modifier les paramètres de VCSTATUS_MODAL et VCSTATUS_INTERACTIVE dans un contexte de vue après que qu’elle a été créée.</span><span class="sxs-lookup"><span data-stu-id="cebd7-132">The settings of VCSTATUS_MODAL and VCSTATUS_INTERACTIVE cannot change in a view context after it has been created.</span></span>
  
## <a name="notes-to-implementers"></a><span data-ttu-id="cebd7-133">Remarques destinées aux responsables de l’implémentation</span><span class="sxs-lookup"><span data-stu-id="cebd7-133">Notes to implementers</span></span>

<span data-ttu-id="cebd7-134">L’implémentation de cette méthode est complètement varie selon les caractéristiques du formulaire.</span><span class="sxs-lookup"><span data-stu-id="cebd7-134">The specific implementation of this method is completely dependent on the specifics of the form.</span></span> <span data-ttu-id="cebd7-135">La plupart des objets de formulaire utiliser cette méthode pour modifier leur interface utilisateur (par exemple, pour activer ou désactiver les commandes de menu ou les boutons pour correspondre au paramètre d’indicateurs de statut visionneuse).</span><span class="sxs-lookup"><span data-stu-id="cebd7-135">Most form objects use this method to change their user interface (for example, to enable or disable menu commands or buttons to match the viewer status flags parameter).</span></span>
  
## <a name="see-also"></a><span data-ttu-id="cebd7-136">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="cebd7-136">See also</span></span>



[<span data-ttu-id="cebd7-137">IMAPIViewContext::ActivateNext</span><span class="sxs-lookup"><span data-stu-id="cebd7-137">IMAPIViewContext::ActivateNext</span></span>](imapiviewcontext-activatenext.md)
  
[<span data-ttu-id="cebd7-138">IMAPIFormAdviseSink : IUnknown</span><span class="sxs-lookup"><span data-stu-id="cebd7-138">IMAPIFormAdviseSink : IUnknown</span></span>](imapiformadvisesinkiunknown.md)

