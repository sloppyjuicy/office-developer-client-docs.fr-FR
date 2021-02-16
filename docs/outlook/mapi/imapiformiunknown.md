---
title: IMAPIForm IUnknown
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- IMAPIForm
api_type:
- COM
ms.assetid: e9059739-51b4-4574-bd0f-709eb5144ae7
description: Dernière modification le 9 mars 2015
ms.openlocfilehash: 172cbf9478d3206742df61d211051594e69ab173
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/28/2019
ms.locfileid: "33436383"
---
# <a name="imapiform--iunknown"></a><span data-ttu-id="d2f27-103">IMAPIForm : IUnknown</span><span class="sxs-lookup"><span data-stu-id="d2f27-103">IMAPIForm : IUnknown</span></span>

  
  
<span data-ttu-id="d2f27-104">**S’applique à** : Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="d2f27-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="d2f27-105">Permet aux visionneuses de formulaires de fonctionner avec des contextes d’affichage de formulaire et des notifications de formulaire, d’exécuter des verbes de formulaire et d’arrêter des formulaires.</span><span class="sxs-lookup"><span data-stu-id="d2f27-105">Enables form viewers to work with form view contexts and form notification, to perform form verbs, and to shut down forms.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="d2f27-106">Fichier d’en-tête :</span><span class="sxs-lookup"><span data-stu-id="d2f27-106">Header file:</span></span>  <br/> |<span data-ttu-id="d2f27-107">Mapiform.h</span><span class="sxs-lookup"><span data-stu-id="d2f27-107">Mapiform.h</span></span>  <br/> |
|<span data-ttu-id="d2f27-108">Exposé par :</span><span class="sxs-lookup"><span data-stu-id="d2f27-108">Exposed by:</span></span>  <br/> |<span data-ttu-id="d2f27-109">Objets de formulaires</span><span class="sxs-lookup"><span data-stu-id="d2f27-109">Form objects</span></span>  <br/> |
|<span data-ttu-id="d2f27-110">Implémenté par :</span><span class="sxs-lookup"><span data-stu-id="d2f27-110">Implemented by:</span></span>  <br/> |<span data-ttu-id="d2f27-111">Serveurs de formulaires</span><span class="sxs-lookup"><span data-stu-id="d2f27-111">Form servers</span></span>  <br/> |
|<span data-ttu-id="d2f27-112">Appelé par :</span><span class="sxs-lookup"><span data-stu-id="d2f27-112">Called by:</span></span>  <br/> |<span data-ttu-id="d2f27-113">Visionneuses de formulaires</span><span class="sxs-lookup"><span data-stu-id="d2f27-113">Form viewers</span></span>  <br/> |
|<span data-ttu-id="d2f27-114">Identificateur d’interface :</span><span class="sxs-lookup"><span data-stu-id="d2f27-114">Interface identifier:</span></span>  <br/> |<span data-ttu-id="d2f27-115">IID_IMAPIForm</span><span class="sxs-lookup"><span data-stu-id="d2f27-115">IID_IMAPIForm</span></span>  <br/> |
|<span data-ttu-id="d2f27-116">Type de pointeur :</span><span class="sxs-lookup"><span data-stu-id="d2f27-116">Pointer type:</span></span>  <br/> |<span data-ttu-id="d2f27-117">LPMAPIFORM</span><span class="sxs-lookup"><span data-stu-id="d2f27-117">LPMAPIFORM</span></span>  <br/> |
   
## <a name="vtable-order"></a><span data-ttu-id="d2f27-118">Ordre des vtables</span><span class="sxs-lookup"><span data-stu-id="d2f27-118">Vtable order</span></span>

|||
|:-----|:-----|
|[<span data-ttu-id="d2f27-119">SetViewContext</span><span class="sxs-lookup"><span data-stu-id="d2f27-119">SetViewContext</span></span>](imapiform-setviewcontext.md) <br/> |<span data-ttu-id="d2f27-120">Établit un contexte d’affichage pour le formulaire.</span><span class="sxs-lookup"><span data-stu-id="d2f27-120">Establishes a view context for the form.</span></span>  <br/> |
|[<span data-ttu-id="d2f27-121">GetViewContext</span><span class="sxs-lookup"><span data-stu-id="d2f27-121">GetViewContext</span></span>](imapiform-getviewcontext.md) <br/> |<span data-ttu-id="d2f27-122">Renvoie le contexte d’affichage actuel du formulaire.</span><span class="sxs-lookup"><span data-stu-id="d2f27-122">Returns the current view context for the form.</span></span>  <br/> |
|[<span data-ttu-id="d2f27-123">ShutdownForm</span><span class="sxs-lookup"><span data-stu-id="d2f27-123">ShutdownForm</span></span>](imapiform-shutdownform.md) <br/> |<span data-ttu-id="d2f27-124">Ferme le formulaire.</span><span class="sxs-lookup"><span data-stu-id="d2f27-124">Closes the form.</span></span>  <br/> |
|[<span data-ttu-id="d2f27-125">DoVerb</span><span class="sxs-lookup"><span data-stu-id="d2f27-125">DoVerb</span></span>](imapiform-doverb.md) <br/> |<span data-ttu-id="d2f27-126">Demande au formulaire d’effectuer toutes les tâches qu’il associe à un verbe spécifique.</span><span class="sxs-lookup"><span data-stu-id="d2f27-126">Requests that the form perform whatever tasks it associates with a specific verb.</span></span>  <br/> |
|[<span data-ttu-id="d2f27-127">Conseiller</span><span class="sxs-lookup"><span data-stu-id="d2f27-127">Advise</span></span>](imapiform-advise.md) <br/> |<span data-ttu-id="d2f27-128">Inscrit une visionneuse de formulaires pour les notifications sur les événements qui affectent le formulaire.</span><span class="sxs-lookup"><span data-stu-id="d2f27-128">Registers a form viewer for notifications about events that affect the form.</span></span>  <br/> |
|[<span data-ttu-id="d2f27-129">Unadvise</span><span class="sxs-lookup"><span data-stu-id="d2f27-129">Unadvise</span></span>](imapiform-unadvise.md) <br/> |<span data-ttu-id="d2f27-130">Annule une inscription pour les notifications auprès d’une visionneuse de formulaires précédemment établie en appelant **Advise**.</span><span class="sxs-lookup"><span data-stu-id="d2f27-130">Cancels a registration for notifications with a form viewer previously established by calling **Advise**.</span></span>  <br/> |
|[<span data-ttu-id="d2f27-131">GetLastError</span><span class="sxs-lookup"><span data-stu-id="d2f27-131">GetLastError</span></span>](imapiform-getlasterror.md) <br/> |<span data-ttu-id="d2f27-132">Renvoie une structure [MAPIERROR](mapierror.md) qui contient des informations sur l’erreur précédente qui s’est produite sur l’objet de formulaire.</span><span class="sxs-lookup"><span data-stu-id="d2f27-132">Returns a [MAPIERROR](mapierror.md) structure that contains information about the previous error occurring to the form object.</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="d2f27-133">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="d2f27-133">See also</span></span>



[<span data-ttu-id="d2f27-134">Interfaces MAPI</span><span class="sxs-lookup"><span data-stu-id="d2f27-134">MAPI Interfaces</span></span>](mapi-interfaces.md)

