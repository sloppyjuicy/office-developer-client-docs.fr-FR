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
description: 'Derni�re modification�: lundi 9 mars 2015'
ms.openlocfilehash: 68c2af0cd8d7ccddf6aa6017cfb830b196ac0771
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32286603"
---
# <a name="imapiformadvisesink--iunknown"></a><span data-ttu-id="85ac1-103">IMAPIFormAdviseSink : IUnknown</span><span class="sxs-lookup"><span data-stu-id="85ac1-103">IMAPIFormAdviseSink : IUnknown</span></span>

  
  
<span data-ttu-id="85ac1-104">**S’applique à** : Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="85ac1-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="85ac1-105">Permet aux serveurs de formulaires de recevoir des notifications des observateurs de formulaires.</span><span class="sxs-lookup"><span data-stu-id="85ac1-105">Enables form servers to receive notifications from form viewers.</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="85ac1-106">Fichier d’en-tête :</span><span class="sxs-lookup"><span data-stu-id="85ac1-106">Header file:</span></span>  <br/> |<span data-ttu-id="85ac1-107">MAPIForm. h</span><span class="sxs-lookup"><span data-stu-id="85ac1-107">Mapiform.h</span></span>  <br/> |
|<span data-ttu-id="85ac1-108">Exposé par:</span><span class="sxs-lookup"><span data-stu-id="85ac1-108">Exposed by:</span></span>  <br/> |<span data-ttu-id="85ac1-109">Objets de récepteur de formulaire advise</span><span class="sxs-lookup"><span data-stu-id="85ac1-109">Form advise sink objects</span></span>  <br/> |
|<span data-ttu-id="85ac1-110">Implémenté par :</span><span class="sxs-lookup"><span data-stu-id="85ac1-110">Implemented by:</span></span>  <br/> |<span data-ttu-id="85ac1-111">Serveurs de formulaires</span><span class="sxs-lookup"><span data-stu-id="85ac1-111">Form servers</span></span>  <br/> |
|<span data-ttu-id="85ac1-112">Appelé par :</span><span class="sxs-lookup"><span data-stu-id="85ac1-112">Called by:</span></span>  <br/> |<span data-ttu-id="85ac1-113">Visionneuses de formulaires</span><span class="sxs-lookup"><span data-stu-id="85ac1-113">Form viewers</span></span>  <br/> |
|<span data-ttu-id="85ac1-114">Identificateur de l'interface:</span><span class="sxs-lookup"><span data-stu-id="85ac1-114">Interface identifier:</span></span>  <br/> |<span data-ttu-id="85ac1-115">IID_IMAPIFormAdviseSink</span><span class="sxs-lookup"><span data-stu-id="85ac1-115">IID_IMAPIFormAdviseSink</span></span>  <br/> |
|<span data-ttu-id="85ac1-116">Type de pointeur:</span><span class="sxs-lookup"><span data-stu-id="85ac1-116">Pointer type:</span></span>  <br/> |<span data-ttu-id="85ac1-117">LPMAPIFORMADVISESINK</span><span class="sxs-lookup"><span data-stu-id="85ac1-117">LPMAPIFORMADVISESINK</span></span>  <br/> |
   
## <a name="vtable-order"></a><span data-ttu-id="85ac1-118">Ordre vtable</span><span class="sxs-lookup"><span data-stu-id="85ac1-118">Vtable order</span></span>

|||
|:-----|:-----|
|[<span data-ttu-id="85ac1-119">OnChange</span><span class="sxs-lookup"><span data-stu-id="85ac1-119">OnChange</span></span>](imapiformadvisesink-onchange.md) <br/> |<span data-ttu-id="85ac1-120">Indique qu'une modification a eu lieu dans l'état de la visionneuse de formulaires.</span><span class="sxs-lookup"><span data-stu-id="85ac1-120">Indicates that a change has occurred in the status of the form viewer.</span></span>  <br/> |
|[<span data-ttu-id="85ac1-121">OnActivateNext</span><span class="sxs-lookup"><span data-stu-id="85ac1-121">OnActivateNext</span></span>](imapiformadvisesink-onactivatenext.md) <br/> |<span data-ttu-id="85ac1-122">Indique si le formulaire peut gérer la classe de message du prochain message à afficher.</span><span class="sxs-lookup"><span data-stu-id="85ac1-122">Indicates whether the form can handle the message class of the next message to display.</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="85ac1-123">Remarques</span><span class="sxs-lookup"><span data-stu-id="85ac1-123">Remarks</span></span>

<span data-ttu-id="85ac1-124">Les serveurs de formulaires utilisent un objet récepteur de formulaire pour implémenter **IMAPIFormAdviseSink** au lieu de l'inclure dans l'objet Form.</span><span class="sxs-lookup"><span data-stu-id="85ac1-124">Form servers use a form advise sink object to implement **IMAPIFormAdviseSink** instead of including it with their form object.</span></span> <span data-ttu-id="85ac1-125">Par conséquent, les visionneuses de formulaires doivent attendre un appel ayant échoué à la méthode [IUnknown:: QueryInterface](https://msdn.microsoft.com/library/ms682521%28v=VS.85%29.aspx) d'un formulaire pour obtenir un pointeur vers cette interface.</span><span class="sxs-lookup"><span data-stu-id="85ac1-125">Therefore, form viewers should expect a failed call to a form's [IUnknown::QueryInterface](https://msdn.microsoft.com/library/ms682521%28v=VS.85%29.aspx) method to obtain a pointer to this interface.</span></span> 
  
<span data-ttu-id="85ac1-126">Les serveurs de formulaires appellent la méthode [IMAPIViewContext:: SetAdviseSink](imapiviewcontext-setadvisesink.md) de la visionneuse pour s'inscrire aux notifications.</span><span class="sxs-lookup"><span data-stu-id="85ac1-126">Form servers call a viewer's [IMAPIViewContext::SetAdviseSink](imapiviewcontext-setadvisesink.md) method to register for notifications.</span></span> <span data-ttu-id="85ac1-127">Un pointeur vers son implémentation **IMAPIFormAdviseSink** est inclus en tant que paramètre.</span><span class="sxs-lookup"><span data-stu-id="85ac1-127">A pointer to their **IMAPIFormAdviseSink** implementation is included as a parameter.</span></span> 
  
## <a name="see-also"></a><span data-ttu-id="85ac1-128">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="85ac1-128">See also</span></span>



[<span data-ttu-id="85ac1-129">Interfaces MAPI</span><span class="sxs-lookup"><span data-stu-id="85ac1-129">MAPI Interfaces</span></span>](mapi-interfaces.md)

