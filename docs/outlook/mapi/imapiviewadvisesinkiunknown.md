---
title: IMAPIViewAdviseSink IUnknown
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- IMAPIViewAdviseSink
api_type:
- COM
ms.assetid: 1231391d-803a-4b41-b252-4d986f99361a
description: 'Derni�re modification�: lundi 9 mars 2015'
ms.openlocfilehash: f16585a96164835784bfa1af3752bd652daf76e8
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19784106"
---
# <a name="imapiviewadvisesink--iunknown"></a><span data-ttu-id="7acd9-103">IMAPIViewAdviseSink : IUnknown</span><span class="sxs-lookup"><span data-stu-id="7acd9-103">IMAPIViewAdviseSink : IUnknown</span></span>

  
  
<span data-ttu-id="7acd9-104">**S’applique à**: Outlook</span><span class="sxs-lookup"><span data-stu-id="7acd9-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="7acd9-105">Reçoit des notifications à partir de formulaires.</span><span class="sxs-lookup"><span data-stu-id="7acd9-105">Receives notifications from forms.</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="7acd9-106">Fichier d’en-tête :</span><span class="sxs-lookup"><span data-stu-id="7acd9-106">Header file:</span></span>  <br/> |<span data-ttu-id="7acd9-107">MAPIForm.h</span><span class="sxs-lookup"><span data-stu-id="7acd9-107">Mapiform.h</span></span>  <br/> |
|<span data-ttu-id="7acd9-108">Exposés par :</span><span class="sxs-lookup"><span data-stu-id="7acd9-108">Exposed by:</span></span>  <br/> |<span data-ttu-id="7acd9-109">Affichage des objets de récepteur de notification</span><span class="sxs-lookup"><span data-stu-id="7acd9-109">View advise sink objects</span></span>  <br/> |
|<span data-ttu-id="7acd9-110">Implémentée par :</span><span class="sxs-lookup"><span data-stu-id="7acd9-110">Implemented by:</span></span>  <br/> |<span data-ttu-id="7acd9-111">Visionneuses de formulaire</span><span class="sxs-lookup"><span data-stu-id="7acd9-111">Form viewers</span></span>  <br/> |
|<span data-ttu-id="7acd9-112">Appelée par :</span><span class="sxs-lookup"><span data-stu-id="7acd9-112">Called by:</span></span>  <br/> |<span data-ttu-id="7acd9-113">Objets de formulaire</span><span class="sxs-lookup"><span data-stu-id="7acd9-113">Form objects</span></span>  <br/> |
|<span data-ttu-id="7acd9-114">Identificateur de l’interface :</span><span class="sxs-lookup"><span data-stu-id="7acd9-114">Interface identifier:</span></span>  <br/> |<span data-ttu-id="7acd9-115">IID_IMAPIViewAdviseSink</span><span class="sxs-lookup"><span data-stu-id="7acd9-115">IID_IMAPIViewAdviseSink</span></span>  <br/> |
|<span data-ttu-id="7acd9-116">Type de pointeur :</span><span class="sxs-lookup"><span data-stu-id="7acd9-116">Pointer type:</span></span>  <br/> |<span data-ttu-id="7acd9-117">LPMAPIVIEWADVISESINK</span><span class="sxs-lookup"><span data-stu-id="7acd9-117">LPMAPIVIEWADVISESINK</span></span>  <br/> |
   
## <a name="vtable-order"></a><span data-ttu-id="7acd9-118">Ordre vtable</span><span class="sxs-lookup"><span data-stu-id="7acd9-118">Vtable order</span></span>

|||
|:-----|:-----|
|[<span data-ttu-id="7acd9-119">OnShutdown</span><span class="sxs-lookup"><span data-stu-id="7acd9-119">OnShutdown</span></span>](imapiviewadvisesink-onshutdown.md) <br/> |<span data-ttu-id="7acd9-120">Avertit la visionneuse de formulaire fermeture d’un formulaire.</span><span class="sxs-lookup"><span data-stu-id="7acd9-120">Notifies the form viewer that a form is being closed.</span></span>  <br/> |
|[<span data-ttu-id="7acd9-121">OnNewMessage</span><span class="sxs-lookup"><span data-stu-id="7acd9-121">OnNewMessage</span></span>](imapiviewadvisesink-onnewmessage.md) <br/> |<span data-ttu-id="7acd9-122">Indique la visionneuse de formulaire à une nouvelle ou un message existant a été chargé dans un formulaire.</span><span class="sxs-lookup"><span data-stu-id="7acd9-122">Notifies the form viewer that either a new or an existing message has been loaded in a form.</span></span>  <br/> |
|[<span data-ttu-id="7acd9-123">OnPrint</span><span class="sxs-lookup"><span data-stu-id="7acd9-123">OnPrint</span></span>](imapiviewadvisesink-onprint.md) <br/> |<span data-ttu-id="7acd9-124">Avertit l’utilisateur du formulaire de l’état d’impression d’un formulaire.</span><span class="sxs-lookup"><span data-stu-id="7acd9-124">Notifies the form viewer of the printing status of a form.</span></span>  <br/> |
|[<span data-ttu-id="7acd9-125">OnSubmitted</span><span class="sxs-lookup"><span data-stu-id="7acd9-125">OnSubmitted</span></span>](imapiviewadvisesink-onsubmitted.md) <br/> |<span data-ttu-id="7acd9-126">Indique que le message en cours a été soumis au spouleur MAPI à la visionneuse de formulaire.</span><span class="sxs-lookup"><span data-stu-id="7acd9-126">Notifies the form viewer that the current message has been submitted to MAPI spooler.</span></span>  <br/> |
|[<span data-ttu-id="7acd9-127">OnSaved</span><span class="sxs-lookup"><span data-stu-id="7acd9-127">OnSaved</span></span>](imapiviewadvisesink-onsaved.md) <br/> |<span data-ttu-id="7acd9-128">Avertit la visionneuse de formulaire le message actuel dans un formulaire a été enregistré.</span><span class="sxs-lookup"><span data-stu-id="7acd9-128">Notifies the form viewer that the current message in a form has been saved.</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="7acd9-129">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="7acd9-129">See also</span></span>



[<span data-ttu-id="7acd9-130">Interfaces MAPI</span><span class="sxs-lookup"><span data-stu-id="7acd9-130">MAPI Interfaces</span></span>](mapi-interfaces.md)

