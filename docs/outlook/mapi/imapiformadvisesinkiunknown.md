---
title: IMAPIFormAdviseSink IUnknown
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- IMAPIFormAdviseSink
api_type:
- COM
ms.assetid: 180022af-4c1c-408c-a3fe-ed075cef79ab
description: Dernière modification le 09 mars 2015
ms.openlocfilehash: cee58299147c9f97ff61a3b8c460125349910637
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/23/2018
ms.locfileid: "22594459"
---
# <a name="imapiformadvisesink--iunknown"></a><span data-ttu-id="72819-103">IMAPIFormAdviseSink : IUnknown</span><span class="sxs-lookup"><span data-stu-id="72819-103">IMAPIFormAdviseSink : IUnknown</span></span>

  
  
<span data-ttu-id="72819-104">**S’applique à**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="72819-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="72819-105">Permet aux serveurs de formulaire de recevoir des notifications de visionneuses de formulaire.</span><span class="sxs-lookup"><span data-stu-id="72819-105">Enables form servers to receive notifications from form viewers.</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="72819-106">Fichier d’en-tête :</span><span class="sxs-lookup"><span data-stu-id="72819-106">Header file:</span></span>  <br/> |<span data-ttu-id="72819-107">MAPIForm.h</span><span class="sxs-lookup"><span data-stu-id="72819-107">Mapiform.h</span></span>  <br/> |
|<span data-ttu-id="72819-108">Exposés par :</span><span class="sxs-lookup"><span data-stu-id="72819-108">Exposed by:</span></span>  <br/> |<span data-ttu-id="72819-109">Objets de récepteur de notification de formulaire</span><span class="sxs-lookup"><span data-stu-id="72819-109">Form advise sink objects</span></span>  <br/> |
|<span data-ttu-id="72819-110">Implémentée par :</span><span class="sxs-lookup"><span data-stu-id="72819-110">Implemented by:</span></span>  <br/> |<span data-ttu-id="72819-111">Serveurs de formulaire</span><span class="sxs-lookup"><span data-stu-id="72819-111">Form servers</span></span>  <br/> |
|<span data-ttu-id="72819-112">Appelée par :</span><span class="sxs-lookup"><span data-stu-id="72819-112">Called by:</span></span>  <br/> |<span data-ttu-id="72819-113">Visionneuses de formulaire</span><span class="sxs-lookup"><span data-stu-id="72819-113">Form viewers</span></span>  <br/> |
|<span data-ttu-id="72819-114">Identificateur de l’interface :</span><span class="sxs-lookup"><span data-stu-id="72819-114">Interface identifier:</span></span>  <br/> |<span data-ttu-id="72819-115">IID_IMAPIFormAdviseSink</span><span class="sxs-lookup"><span data-stu-id="72819-115">IID_IMAPIFormAdviseSink</span></span>  <br/> |
|<span data-ttu-id="72819-116">Type de pointeur :</span><span class="sxs-lookup"><span data-stu-id="72819-116">Pointer type:</span></span>  <br/> |<span data-ttu-id="72819-117">LPMAPIFORMADVISESINK</span><span class="sxs-lookup"><span data-stu-id="72819-117">LPMAPIFORMADVISESINK</span></span>  <br/> |
   
## <a name="vtable-order"></a><span data-ttu-id="72819-118">Ordre vtable</span><span class="sxs-lookup"><span data-stu-id="72819-118">Vtable order</span></span>

|||
|:-----|:-----|
|[<span data-ttu-id="72819-119">OnChange</span><span class="sxs-lookup"><span data-stu-id="72819-119">OnChange</span></span>](imapiformadvisesink-onchange.md) <br/> |<span data-ttu-id="72819-120">Indique qu’une modification s’est produite dans l’état de la visionneuse de formulaire.</span><span class="sxs-lookup"><span data-stu-id="72819-120">Indicates that a change has occurred in the status of the form viewer.</span></span>  <br/> |
|[<span data-ttu-id="72819-121">OnActivateNext</span><span class="sxs-lookup"><span data-stu-id="72819-121">OnActivateNext</span></span>](imapiformadvisesink-onactivatenext.md) <br/> |<span data-ttu-id="72819-122">Indique si le formulaire peut gérer la classe de message du message suivant à afficher.</span><span class="sxs-lookup"><span data-stu-id="72819-122">Indicates whether the form can handle the message class of the next message to display.</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="72819-123">Remarques</span><span class="sxs-lookup"><span data-stu-id="72819-123">Remarks</span></span>

<span data-ttu-id="72819-124">Écran serveurs utilisent un formulaire de notification objet récepteur d’implémenter **IMAPIFormAdviseSink** au lieu d’y compris avec l’objet de formulaire.</span><span class="sxs-lookup"><span data-stu-id="72819-124">Form servers use a form advise sink object to implement **IMAPIFormAdviseSink** instead of including it with their form object.</span></span> <span data-ttu-id="72819-125">Par conséquent, les visionneuses de formulaire être confronté à un appel ayant échoué à la méthode [IUnknown::QueryInterface](http://msdn.microsoft.com/en-us/library/ms682521%28v=VS.85%29.aspx) d’un formulaire pour obtenir un pointeur vers cette interface.</span><span class="sxs-lookup"><span data-stu-id="72819-125">Therefore, form viewers should expect a failed call to a form's [IUnknown::QueryInterface](http://msdn.microsoft.com/en-us/library/ms682521%28v=VS.85%29.aspx) method to obtain a pointer to this interface.</span></span> 
  
<span data-ttu-id="72819-126">Serveurs de formulaire appellent la méthode de [IMAPIViewContext::SetAdviseSink](imapiviewcontext-setadvisesink.md) d’un utilisateur pour s’inscrire pour les notifications.</span><span class="sxs-lookup"><span data-stu-id="72819-126">Form servers call a viewer's [IMAPIViewContext::SetAdviseSink](imapiviewcontext-setadvisesink.md) method to register for notifications.</span></span> <span data-ttu-id="72819-127">Un pointeur vers leur mise en oeuvre **IMAPIFormAdviseSink** est inclus en tant que paramètre.</span><span class="sxs-lookup"><span data-stu-id="72819-127">A pointer to their **IMAPIFormAdviseSink** implementation is included as a parameter.</span></span> 
  
## <a name="see-also"></a><span data-ttu-id="72819-128">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="72819-128">See also</span></span>



[<span data-ttu-id="72819-129">Interfaces MAPI</span><span class="sxs-lookup"><span data-stu-id="72819-129">MAPI Interfaces</span></span>](mapi-interfaces.md)

