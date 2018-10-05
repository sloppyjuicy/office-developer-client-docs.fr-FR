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
description: Dernière modification le 9 mars 2015
ms.openlocfilehash: 68c2af0cd8d7ccddf6aa6017cfb830b196ac0771
ms.sourcegitcommit: ef717c65d8dd41ababffb01eafc443c79950aed4
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 10/04/2018
ms.locfileid: "25392059"
---
# <a name="imapiformadvisesink--iunknown"></a><span data-ttu-id="f9710-103">IMAPIFormAdviseSink : IUnknown</span><span class="sxs-lookup"><span data-stu-id="f9710-103">IMAPIFormAdviseSink : IUnknown</span></span>

  
  
<span data-ttu-id="f9710-104">**S’applique à** : Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="f9710-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="f9710-105">Permet aux serveurs de formulaire de recevoir des notifications de visionneuses de formulaire.</span><span class="sxs-lookup"><span data-stu-id="f9710-105">Enables form servers to receive notifications from form viewers.</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="f9710-106">Fichier d’en-tête :</span><span class="sxs-lookup"><span data-stu-id="f9710-106">Header file:</span></span>  <br/> |<span data-ttu-id="f9710-107">MAPIForm.h</span><span class="sxs-lookup"><span data-stu-id="f9710-107">Mapiform.h</span></span>  <br/> |
|<span data-ttu-id="f9710-108">Exposés par :</span><span class="sxs-lookup"><span data-stu-id="f9710-108">Exposed by:</span></span>  <br/> |<span data-ttu-id="f9710-109">Objets de récepteur de notification de formulaire</span><span class="sxs-lookup"><span data-stu-id="f9710-109">Form advise sink objects</span></span>  <br/> |
|<span data-ttu-id="f9710-110">Implémenté par :</span><span class="sxs-lookup"><span data-stu-id="f9710-110">Implemented by:</span></span>  <br/> |<span data-ttu-id="f9710-111">Serveurs de formulaire</span><span class="sxs-lookup"><span data-stu-id="f9710-111">Form servers</span></span>  <br/> |
|<span data-ttu-id="f9710-112">Appelé par :</span><span class="sxs-lookup"><span data-stu-id="f9710-112">Called by:</span></span>  <br/> |<span data-ttu-id="f9710-113">Visionneuses de formulaire</span><span class="sxs-lookup"><span data-stu-id="f9710-113">Form viewers</span></span>  <br/> |
|<span data-ttu-id="f9710-114">Identificateur de l’interface :</span><span class="sxs-lookup"><span data-stu-id="f9710-114">Interface identifier:</span></span>  <br/> |<span data-ttu-id="f9710-115">IID_IMAPIFormAdviseSink</span><span class="sxs-lookup"><span data-stu-id="f9710-115">IID_IMAPIFormAdviseSink</span></span>  <br/> |
|<span data-ttu-id="f9710-116">Type de pointeur :</span><span class="sxs-lookup"><span data-stu-id="f9710-116">Pointer type:</span></span>  <br/> |<span data-ttu-id="f9710-117">LPMAPIFORMADVISESINK</span><span class="sxs-lookup"><span data-stu-id="f9710-117">LPMAPIFORMADVISESINK</span></span>  <br/> |
   
## <a name="vtable-order"></a><span data-ttu-id="f9710-118">Ordre vtable</span><span class="sxs-lookup"><span data-stu-id="f9710-118">Vtable order</span></span>

|||
|:-----|:-----|
|[<span data-ttu-id="f9710-119">OnChange</span><span class="sxs-lookup"><span data-stu-id="f9710-119">OnChange</span></span>](imapiformadvisesink-onchange.md) <br/> |<span data-ttu-id="f9710-120">Indique qu’une modification s’est produite dans l’état de la visionneuse de formulaire.</span><span class="sxs-lookup"><span data-stu-id="f9710-120">Indicates that a change has occurred in the status of the form viewer.</span></span>  <br/> |
|[<span data-ttu-id="f9710-121">OnActivateNext</span><span class="sxs-lookup"><span data-stu-id="f9710-121">OnActivateNext</span></span>](imapiformadvisesink-onactivatenext.md) <br/> |<span data-ttu-id="f9710-122">Indique si le formulaire peut gérer la classe de message du message suivant à afficher.</span><span class="sxs-lookup"><span data-stu-id="f9710-122">Indicates whether the form can handle the message class of the next message to display.</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="f9710-123">Remarques</span><span class="sxs-lookup"><span data-stu-id="f9710-123">Remarks</span></span>

<span data-ttu-id="f9710-124">Écran serveurs utilisent un formulaire de notification objet récepteur d’implémenter **IMAPIFormAdviseSink** au lieu d’y compris avec l’objet de formulaire.</span><span class="sxs-lookup"><span data-stu-id="f9710-124">Form servers use a form advise sink object to implement **IMAPIFormAdviseSink** instead of including it with their form object.</span></span> <span data-ttu-id="f9710-125">Par conséquent, les visionneuses de formulaire être confronté à un appel ayant échoué à la méthode [IUnknown::QueryInterface](https://msdn.microsoft.com/library/ms682521%28v=VS.85%29.aspx) d’un formulaire pour obtenir un pointeur vers cette interface.</span><span class="sxs-lookup"><span data-stu-id="f9710-125">Therefore, form viewers should expect a failed call to a form's [IUnknown::QueryInterface](https://msdn.microsoft.com/library/ms682521%28v=VS.85%29.aspx) method to obtain a pointer to this interface.</span></span> 
  
<span data-ttu-id="f9710-126">Serveurs de formulaire appellent la méthode de [IMAPIViewContext::SetAdviseSink](imapiviewcontext-setadvisesink.md) d’un utilisateur pour s’inscrire pour les notifications.</span><span class="sxs-lookup"><span data-stu-id="f9710-126">Form servers call a viewer's [IMAPIViewContext::SetAdviseSink](imapiviewcontext-setadvisesink.md) method to register for notifications.</span></span> <span data-ttu-id="f9710-127">Un pointeur vers leur mise en oeuvre **IMAPIFormAdviseSink** est inclus en tant que paramètre.</span><span class="sxs-lookup"><span data-stu-id="f9710-127">A pointer to their **IMAPIFormAdviseSink** implementation is included as a parameter.</span></span> 
  
## <a name="see-also"></a><span data-ttu-id="f9710-128">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="f9710-128">See also</span></span>



[<span data-ttu-id="f9710-129">Interfaces MAPI</span><span class="sxs-lookup"><span data-stu-id="f9710-129">MAPI Interfaces</span></span>](mapi-interfaces.md)

