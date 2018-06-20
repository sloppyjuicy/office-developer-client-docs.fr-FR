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
description: 'Derni�re modification�: lundi 9 mars 2015'
ms.openlocfilehash: fce8bc45d5cc87c238288653ab989b62076ad451
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19783799"
---
# <a name="imapiform--iunknown"></a><span data-ttu-id="91dff-103">IMAPIForm : IUnknown</span><span class="sxs-lookup"><span data-stu-id="91dff-103">IMAPIForm : IUnknown</span></span>

  
  
<span data-ttu-id="91dff-104">**S’applique à**: Outlook</span><span class="sxs-lookup"><span data-stu-id="91dff-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="91dff-105">Permet de visionneuses de formulaire travailler avec des contextes d’affichage de formulaire et les notifications de formulaire, effectuer des verbes formulaire et arrêt de formulaires.</span><span class="sxs-lookup"><span data-stu-id="91dff-105">Enables form viewers to work with form view contexts and form notification, to perform form verbs, and to shut down forms.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="91dff-106">Fichier d’en-tête :</span><span class="sxs-lookup"><span data-stu-id="91dff-106">Header file:</span></span>  <br/> |<span data-ttu-id="91dff-107">MAPIForm.h</span><span class="sxs-lookup"><span data-stu-id="91dff-107">Mapiform.h</span></span>  <br/> |
|<span data-ttu-id="91dff-108">Exposés par :</span><span class="sxs-lookup"><span data-stu-id="91dff-108">Exposed by:</span></span>  <br/> |<span data-ttu-id="91dff-109">Objets de formulaire</span><span class="sxs-lookup"><span data-stu-id="91dff-109">Form objects</span></span>  <br/> |
|<span data-ttu-id="91dff-110">Implémentée par :</span><span class="sxs-lookup"><span data-stu-id="91dff-110">Implemented by:</span></span>  <br/> |<span data-ttu-id="91dff-111">Serveurs de formulaire</span><span class="sxs-lookup"><span data-stu-id="91dff-111">Form servers</span></span>  <br/> |
|<span data-ttu-id="91dff-112">Appelée par :</span><span class="sxs-lookup"><span data-stu-id="91dff-112">Called by:</span></span>  <br/> |<span data-ttu-id="91dff-113">Visionneuses de formulaire</span><span class="sxs-lookup"><span data-stu-id="91dff-113">Form viewers</span></span>  <br/> |
|<span data-ttu-id="91dff-114">Identificateur de l’interface :</span><span class="sxs-lookup"><span data-stu-id="91dff-114">Interface identifier:</span></span>  <br/> |<span data-ttu-id="91dff-115">IID_IMAPIForm</span><span class="sxs-lookup"><span data-stu-id="91dff-115">IID_IMAPIForm</span></span>  <br/> |
|<span data-ttu-id="91dff-116">Type de pointeur :</span><span class="sxs-lookup"><span data-stu-id="91dff-116">Pointer type:</span></span>  <br/> |<span data-ttu-id="91dff-117">LPMAPIFORM</span><span class="sxs-lookup"><span data-stu-id="91dff-117">LPMAPIFORM</span></span>  <br/> |
   
## <a name="vtable-order"></a><span data-ttu-id="91dff-118">Ordre vtable</span><span class="sxs-lookup"><span data-stu-id="91dff-118">Vtable order</span></span>

|||
|:-----|:-----|
|[<span data-ttu-id="91dff-119">SetViewContext</span><span class="sxs-lookup"><span data-stu-id="91dff-119">SetViewContext</span></span>](imapiform-setviewcontext.md) <br/> |<span data-ttu-id="91dff-120">Établissement d’un contexte de vue pour le formulaire.</span><span class="sxs-lookup"><span data-stu-id="91dff-120">Establishes a view context for the form.</span></span>  <br/> |
|[<span data-ttu-id="91dff-121">GetViewContext</span><span class="sxs-lookup"><span data-stu-id="91dff-121">GetViewContext</span></span>](imapiform-getviewcontext.md) <br/> |<span data-ttu-id="91dff-122">Renvoie le contexte actuel de la vue pour le formulaire.</span><span class="sxs-lookup"><span data-stu-id="91dff-122">Returns the current view context for the form.</span></span>  <br/> |
|[<span data-ttu-id="91dff-123">ShutdownForm</span><span class="sxs-lookup"><span data-stu-id="91dff-123">ShutdownForm</span></span>](imapiform-shutdownform.md) <br/> |<span data-ttu-id="91dff-124">Ferme le formulaire.</span><span class="sxs-lookup"><span data-stu-id="91dff-124">Closes the form.</span></span>  <br/> |
|[<span data-ttu-id="91dff-125">DoVerb</span><span class="sxs-lookup"><span data-stu-id="91dff-125">DoVerb</span></span>](imapiform-doverb.md) <br/> |<span data-ttu-id="91dff-126">Exige que le formulaire exécute ce que les tâches associe un verbe spécifique.</span><span class="sxs-lookup"><span data-stu-id="91dff-126">Requests that the form perform whatever tasks it associates with a specific verb.</span></span>  <br/> |
|[<span data-ttu-id="91dff-127">Conseiller</span><span class="sxs-lookup"><span data-stu-id="91dff-127">Advise</span></span>](imapiform-advise.md) <br/> |<span data-ttu-id="91dff-128">Enregistre une visionneuse de formulaire pour les notifications concernant les événements qui affectent le formulaire.</span><span class="sxs-lookup"><span data-stu-id="91dff-128">Registers a form viewer for notifications about events that affect the form.</span></span>  <br/> |
|[<span data-ttu-id="91dff-129">L’avertissement</span><span class="sxs-lookup"><span data-stu-id="91dff-129">Unadvise</span></span>](imapiform-unadvise.md) <br/> |<span data-ttu-id="91dff-130">Annule une inscription pour les notifications avec une visionneuse de formulaire précédemment établie via un appel **Advise**.</span><span class="sxs-lookup"><span data-stu-id="91dff-130">Cancels a registration for notifications with a form viewer previously established by calling **Advise**.</span></span>  <br/> |
|[<span data-ttu-id="91dff-131">GetLastError</span><span class="sxs-lookup"><span data-stu-id="91dff-131">GetLastError</span></span>](imapiform-getlasterror.md) <br/> |<span data-ttu-id="91dff-132">Retourne une structure [MAPIERROR](mapierror.md) qui contient des informations sur l’erreur précédente se produisant à l’objet form.</span><span class="sxs-lookup"><span data-stu-id="91dff-132">Returns a [MAPIERROR](mapierror.md) structure that contains information about the previous error occurring to the form object.</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="91dff-133">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="91dff-133">See also</span></span>



[<span data-ttu-id="91dff-134">Interfaces MAPI</span><span class="sxs-lookup"><span data-stu-id="91dff-134">MAPI Interfaces</span></span>](mapi-interfaces.md)

