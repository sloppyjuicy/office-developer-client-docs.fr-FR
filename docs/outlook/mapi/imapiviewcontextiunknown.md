---
title: IMAPIViewContext IUnknown
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- IMAPIViewContext
api_type:
- COM
ms.assetid: d566ff39-92c1-4a14-85e5-1c406825f805
description: 'Derni�re modification�: lundi 9 mars 2015'
ms.openlocfilehash: a7d62253baaaae7955e722874a15d05ed16e566e
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19784127"
---
# <a name="imapiviewcontext--iunknown"></a><span data-ttu-id="03c11-103">IMAPIViewContext : IUnknown</span><span class="sxs-lookup"><span data-stu-id="03c11-103">IMAPIViewContext : IUnknown</span></span>

  
  
<span data-ttu-id="03c11-104">**S’applique à**: Outlook</span><span class="sxs-lookup"><span data-stu-id="03c11-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="03c11-105">Gère un formulaire dans l’Observateur d’une application cliente formulaire.</span><span class="sxs-lookup"><span data-stu-id="03c11-105">Manages a form in a client application's form viewer.</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="03c11-106">Fichier d’en-tête :</span><span class="sxs-lookup"><span data-stu-id="03c11-106">Header file:</span></span>  <br/> |<span data-ttu-id="03c11-107">MAPIForm.h</span><span class="sxs-lookup"><span data-stu-id="03c11-107">Mapiform.h</span></span>  <br/> |
|<span data-ttu-id="03c11-108">Exposés par :</span><span class="sxs-lookup"><span data-stu-id="03c11-108">Exposed by:</span></span>  <br/> |<span data-ttu-id="03c11-109">Afficher les objets de contexte</span><span class="sxs-lookup"><span data-stu-id="03c11-109">View context objects</span></span>  <br/> |
|<span data-ttu-id="03c11-110">Implémentée par :</span><span class="sxs-lookup"><span data-stu-id="03c11-110">Implemented by:</span></span>  <br/> |<span data-ttu-id="03c11-111">Visionneuses de formulaire</span><span class="sxs-lookup"><span data-stu-id="03c11-111">Form viewers</span></span>  <br/> |
|<span data-ttu-id="03c11-112">Appelée par :</span><span class="sxs-lookup"><span data-stu-id="03c11-112">Called by:</span></span>  <br/> |<span data-ttu-id="03c11-113">Objets de formulaire</span><span class="sxs-lookup"><span data-stu-id="03c11-113">Form objects</span></span>  <br/> |
|<span data-ttu-id="03c11-114">Identificateur de l’interface :</span><span class="sxs-lookup"><span data-stu-id="03c11-114">Interface identifier:</span></span>  <br/> |<span data-ttu-id="03c11-115">IID_IMAPIViewContext</span><span class="sxs-lookup"><span data-stu-id="03c11-115">IID_IMAPIViewContext</span></span>  <br/> |
|<span data-ttu-id="03c11-116">Type de pointeur :</span><span class="sxs-lookup"><span data-stu-id="03c11-116">Pointer type:</span></span>  <br/> |<span data-ttu-id="03c11-117">LPMAPIVIEWCONTEXT</span><span class="sxs-lookup"><span data-stu-id="03c11-117">LPMAPIVIEWCONTEXT</span></span>  <br/> |
   
## <a name="vtable-order"></a><span data-ttu-id="03c11-118">Ordre vtable</span><span class="sxs-lookup"><span data-stu-id="03c11-118">Vtable order</span></span>

|||
|:-----|:-----|
|[<span data-ttu-id="03c11-119">SetAdviseSink</span><span class="sxs-lookup"><span data-stu-id="03c11-119">SetAdviseSink</span></span>](imapiviewcontext-setadvisesink.md) <br/> |<span data-ttu-id="03c11-120">Gère l’inscription d’un formulaire pour recevoir des notifications sur les modifications dans la visionneuse.</span><span class="sxs-lookup"><span data-stu-id="03c11-120">Manages a form's registration to receive notifications about changes in the viewer.</span></span>  <br/> |
|[<span data-ttu-id="03c11-121">ActivateNext</span><span class="sxs-lookup"><span data-stu-id="03c11-121">ActivateNext</span></span>](imapiviewcontext-activatenext.md) <br/> |<span data-ttu-id="03c11-122">Active le message suivant ou précédent dans la visionneuse de formulaire.</span><span class="sxs-lookup"><span data-stu-id="03c11-122">Activates the next or previous message in the form viewer.</span></span>  <br/> |
|[<span data-ttu-id="03c11-123">GetPrintSetup</span><span class="sxs-lookup"><span data-stu-id="03c11-123">GetPrintSetup</span></span>](imapiviewcontext-getprintsetup.md) <br/> |<span data-ttu-id="03c11-124">Récupère les informations d’impression en cours.</span><span class="sxs-lookup"><span data-stu-id="03c11-124">Retrieves current printing information.</span></span>  <br/> |
|[<span data-ttu-id="03c11-125">GetSaveStream</span><span class="sxs-lookup"><span data-stu-id="03c11-125">GetSaveStream</span></span>](imapiviewcontext-getsavestream.md) <br/> |<span data-ttu-id="03c11-126">Récupère un flux de données à utiliser pour l’enregistrement du message en cours.</span><span class="sxs-lookup"><span data-stu-id="03c11-126">Retrieves a stream to be used for saving the current message.</span></span>  <br/> |
|[<span data-ttu-id="03c11-127">GetViewStatus</span><span class="sxs-lookup"><span data-stu-id="03c11-127">GetViewStatus</span></span>](imapiviewcontext-getviewstatus.md) <br/> |<span data-ttu-id="03c11-128">Récupère l’état actuel de la visionneuse.</span><span class="sxs-lookup"><span data-stu-id="03c11-128">Retrieves the current viewer status.</span></span>  <br/> |
|[<span data-ttu-id="03c11-129">GetLastError</span><span class="sxs-lookup"><span data-stu-id="03c11-129">GetLastError</span></span>](imapiviewcontext-getlasterror.md) <br/> |<span data-ttu-id="03c11-130">Retourne une structure [MAPIERROR](mapierror.md) qui contient des informations sur l’erreur précédente qui se produisent dans l’objet de contexte de vue.</span><span class="sxs-lookup"><span data-stu-id="03c11-130">Returns a [MAPIERROR](mapierror.md) structure that contains information about the previous error occurring in the view context object.</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="03c11-131">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="03c11-131">See also</span></span>



[<span data-ttu-id="03c11-132">Interfaces MAPI</span><span class="sxs-lookup"><span data-stu-id="03c11-132">MAPI Interfaces</span></span>](mapi-interfaces.md)

