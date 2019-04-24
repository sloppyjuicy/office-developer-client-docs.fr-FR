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
ms.openlocfilehash: 70f61fe33baa7870a58c4cbc7d75e0df119b5b1a
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32351139"
---
# <a name="imapiviewadvisesink--iunknown"></a><span data-ttu-id="94a22-103">IMAPIViewAdviseSink : IUnknown</span><span class="sxs-lookup"><span data-stu-id="94a22-103">IMAPIViewAdviseSink : IUnknown</span></span>

  
  
<span data-ttu-id="94a22-104">**S’applique à** : Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="94a22-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="94a22-105">Reçoit des notifications des formulaires.</span><span class="sxs-lookup"><span data-stu-id="94a22-105">Receives notifications from forms.</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="94a22-106">Fichier d’en-tête :</span><span class="sxs-lookup"><span data-stu-id="94a22-106">Header file:</span></span>  <br/> |<span data-ttu-id="94a22-107">MAPIForm. h</span><span class="sxs-lookup"><span data-stu-id="94a22-107">Mapiform.h</span></span>  <br/> |
|<span data-ttu-id="94a22-108">Exposé par:</span><span class="sxs-lookup"><span data-stu-id="94a22-108">Exposed by:</span></span>  <br/> |<span data-ttu-id="94a22-109">Afficher les objets du récepteur de notifications</span><span class="sxs-lookup"><span data-stu-id="94a22-109">View advise sink objects</span></span>  <br/> |
|<span data-ttu-id="94a22-110">Implémenté par :</span><span class="sxs-lookup"><span data-stu-id="94a22-110">Implemented by:</span></span>  <br/> |<span data-ttu-id="94a22-111">Visionneuses de formulaires</span><span class="sxs-lookup"><span data-stu-id="94a22-111">Form viewers</span></span>  <br/> |
|<span data-ttu-id="94a22-112">Appelé par :</span><span class="sxs-lookup"><span data-stu-id="94a22-112">Called by:</span></span>  <br/> |<span data-ttu-id="94a22-113">Objets de formulaires</span><span class="sxs-lookup"><span data-stu-id="94a22-113">Form objects</span></span>  <br/> |
|<span data-ttu-id="94a22-114">Identificateur de l'interface:</span><span class="sxs-lookup"><span data-stu-id="94a22-114">Interface identifier:</span></span>  <br/> |<span data-ttu-id="94a22-115">IID_IMAPIViewAdviseSink</span><span class="sxs-lookup"><span data-stu-id="94a22-115">IID_IMAPIViewAdviseSink</span></span>  <br/> |
|<span data-ttu-id="94a22-116">Type de pointeur:</span><span class="sxs-lookup"><span data-stu-id="94a22-116">Pointer type:</span></span>  <br/> |<span data-ttu-id="94a22-117">LPMAPIVIEWADVISESINK</span><span class="sxs-lookup"><span data-stu-id="94a22-117">LPMAPIVIEWADVISESINK</span></span>  <br/> |
   
## <a name="vtable-order"></a><span data-ttu-id="94a22-118">Ordre vtable</span><span class="sxs-lookup"><span data-stu-id="94a22-118">Vtable order</span></span>

|||
|:-----|:-----|
|[<span data-ttu-id="94a22-119">OnShutdown</span><span class="sxs-lookup"><span data-stu-id="94a22-119">OnShutdown</span></span>](imapiviewadvisesink-onshutdown.md) <br/> |<span data-ttu-id="94a22-120">Avertit la visionneuse de formulaires qu'un formulaire est en cours de fermeture.</span><span class="sxs-lookup"><span data-stu-id="94a22-120">Notifies the form viewer that a form is being closed.</span></span>  <br/> |
|[<span data-ttu-id="94a22-121">OnNewMessage</span><span class="sxs-lookup"><span data-stu-id="94a22-121">OnNewMessage</span></span>](imapiviewadvisesink-onnewmessage.md) <br/> |<span data-ttu-id="94a22-122">Avertit la visionneuse de formulaires qu'un nouveau message ou un message existant a été chargé dans un formulaire.</span><span class="sxs-lookup"><span data-stu-id="94a22-122">Notifies the form viewer that either a new or an existing message has been loaded in a form.</span></span>  <br/> |
|[<span data-ttu-id="94a22-123">OnPrint</span><span class="sxs-lookup"><span data-stu-id="94a22-123">OnPrint</span></span>](imapiviewadvisesink-onprint.md) <br/> |<span data-ttu-id="94a22-124">Avertit la visionneuse de formulaires de l'état d'impression d'un formulaire.</span><span class="sxs-lookup"><span data-stu-id="94a22-124">Notifies the form viewer of the printing status of a form.</span></span>  <br/> |
|[<span data-ttu-id="94a22-125">OnSubmitted</span><span class="sxs-lookup"><span data-stu-id="94a22-125">OnSubmitted</span></span>](imapiviewadvisesink-onsubmitted.md) <br/> |<span data-ttu-id="94a22-126">Avertit la visionneuse de formulaires que le message actif a été envoyé au spouleur MAPI.</span><span class="sxs-lookup"><span data-stu-id="94a22-126">Notifies the form viewer that the current message has been submitted to MAPI spooler.</span></span>  <br/> |
|[<span data-ttu-id="94a22-127">OnSaved</span><span class="sxs-lookup"><span data-stu-id="94a22-127">OnSaved</span></span>](imapiviewadvisesink-onsaved.md) <br/> |<span data-ttu-id="94a22-128">Avertit la visionneuse de formulaires que le message actif d'un formulaire a été enregistré.</span><span class="sxs-lookup"><span data-stu-id="94a22-128">Notifies the form viewer that the current message in a form has been saved.</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="94a22-129">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="94a22-129">See also</span></span>



[<span data-ttu-id="94a22-130">Interfaces MAPI</span><span class="sxs-lookup"><span data-stu-id="94a22-130">MAPI Interfaces</span></span>](mapi-interfaces.md)

