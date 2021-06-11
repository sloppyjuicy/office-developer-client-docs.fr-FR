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
description: Dernière modification le 9 mars 2015
ms.openlocfilehash: 70f61fe33baa7870a58c4cbc7d75e0df119b5b1a
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/28/2019
ms.locfileid: "33429417"
---
# <a name="imapiviewadvisesink--iunknown"></a><span data-ttu-id="e6878-103">IMAPIViewAdviseSink : IUnknown</span><span class="sxs-lookup"><span data-stu-id="e6878-103">IMAPIViewAdviseSink : IUnknown</span></span>

  
  
<span data-ttu-id="e6878-104">**S’applique à** : Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="e6878-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="e6878-105">Reçoit des notifications à partir de formulaires.</span><span class="sxs-lookup"><span data-stu-id="e6878-105">Receives notifications from forms.</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="e6878-106">Fichier d’en-tête :</span><span class="sxs-lookup"><span data-stu-id="e6878-106">Header file:</span></span>  <br/> |<span data-ttu-id="e6878-107">Mapiform.h</span><span class="sxs-lookup"><span data-stu-id="e6878-107">Mapiform.h</span></span>  <br/> |
|<span data-ttu-id="e6878-108">Exposé par :</span><span class="sxs-lookup"><span data-stu-id="e6878-108">Exposed by:</span></span>  <br/> |<span data-ttu-id="e6878-109">Afficher les objets de sink de conseil</span><span class="sxs-lookup"><span data-stu-id="e6878-109">View advise sink objects</span></span>  <br/> |
|<span data-ttu-id="e6878-110">Implémenté par :</span><span class="sxs-lookup"><span data-stu-id="e6878-110">Implemented by:</span></span>  <br/> |<span data-ttu-id="e6878-111">Visionneuses de formulaires</span><span class="sxs-lookup"><span data-stu-id="e6878-111">Form viewers</span></span>  <br/> |
|<span data-ttu-id="e6878-112">Appelé par :</span><span class="sxs-lookup"><span data-stu-id="e6878-112">Called by:</span></span>  <br/> |<span data-ttu-id="e6878-113">Objets de formulaires</span><span class="sxs-lookup"><span data-stu-id="e6878-113">Form objects</span></span>  <br/> |
|<span data-ttu-id="e6878-114">Identificateur d’interface :</span><span class="sxs-lookup"><span data-stu-id="e6878-114">Interface identifier:</span></span>  <br/> |<span data-ttu-id="e6878-115">IID_IMAPIViewAdviseSink</span><span class="sxs-lookup"><span data-stu-id="e6878-115">IID_IMAPIViewAdviseSink</span></span>  <br/> |
|<span data-ttu-id="e6878-116">Type de pointeur :</span><span class="sxs-lookup"><span data-stu-id="e6878-116">Pointer type:</span></span>  <br/> |<span data-ttu-id="e6878-117">LPMAPIVIEWADVISESINK</span><span class="sxs-lookup"><span data-stu-id="e6878-117">LPMAPIVIEWADVISESINK</span></span>  <br/> |
   
## <a name="vtable-order"></a><span data-ttu-id="e6878-118">Ordre des vtables</span><span class="sxs-lookup"><span data-stu-id="e6878-118">Vtable order</span></span>

|||
|:-----|:-----|
|[<span data-ttu-id="e6878-119">OnShutdown</span><span class="sxs-lookup"><span data-stu-id="e6878-119">OnShutdown</span></span>](imapiviewadvisesink-onshutdown.md) <br/> |<span data-ttu-id="e6878-120">Avertit la visionneuse de formulaires qu’un formulaire est en cours de fermeture.</span><span class="sxs-lookup"><span data-stu-id="e6878-120">Notifies the form viewer that a form is being closed.</span></span>  <br/> |
|[<span data-ttu-id="e6878-121">OnNewMessage</span><span class="sxs-lookup"><span data-stu-id="e6878-121">OnNewMessage</span></span>](imapiviewadvisesink-onnewmessage.md) <br/> |<span data-ttu-id="e6878-122">Avertit la visionneuse de formulaire qu’un nouveau message ou un message existant a été chargé dans un formulaire.</span><span class="sxs-lookup"><span data-stu-id="e6878-122">Notifies the form viewer that either a new or an existing message has been loaded in a form.</span></span>  <br/> |
|[<span data-ttu-id="e6878-123">OnPrint</span><span class="sxs-lookup"><span data-stu-id="e6878-123">OnPrint</span></span>](imapiviewadvisesink-onprint.md) <br/> |<span data-ttu-id="e6878-124">Avertit la visionneuse de formulaires de l’état d’impression d’un formulaire.</span><span class="sxs-lookup"><span data-stu-id="e6878-124">Notifies the form viewer of the printing status of a form.</span></span>  <br/> |
|[<span data-ttu-id="e6878-125">OnSubmitted</span><span class="sxs-lookup"><span data-stu-id="e6878-125">OnSubmitted</span></span>](imapiviewadvisesink-onsubmitted.md) <br/> |<span data-ttu-id="e6878-126">Avertit la visionneuse de formulaire que le message actuel a été envoyé aupooler MAPI.</span><span class="sxs-lookup"><span data-stu-id="e6878-126">Notifies the form viewer that the current message has been submitted to MAPI spooler.</span></span>  <br/> |
|[<span data-ttu-id="e6878-127">OnSaved</span><span class="sxs-lookup"><span data-stu-id="e6878-127">OnSaved</span></span>](imapiviewadvisesink-onsaved.md) <br/> |<span data-ttu-id="e6878-128">Avertit la visionneuse de formulaire que le message en cours dans un formulaire a été enregistré.</span><span class="sxs-lookup"><span data-stu-id="e6878-128">Notifies the form viewer that the current message in a form has been saved.</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="e6878-129">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="e6878-129">See also</span></span>



[<span data-ttu-id="e6878-130">Interfaces MAPI</span><span class="sxs-lookup"><span data-stu-id="e6878-130">MAPI Interfaces</span></span>](mapi-interfaces.md)

