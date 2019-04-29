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
description: Dernière modification le 9 mars 2015
ms.openlocfilehash: db0c375218755c3a28475e2ebce2d097fb789f75
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/28/2019
ms.locfileid: "33406030"
---
# <a name="imapiviewcontext--iunknown"></a><span data-ttu-id="52178-103">IMAPIViewContext : IUnknown</span><span class="sxs-lookup"><span data-stu-id="52178-103">IMAPIViewContext : IUnknown</span></span>

  
  
<span data-ttu-id="52178-104">**S’applique à** : Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="52178-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="52178-105">Gère un formulaire dans la visionneuse de formulaires d'une application cliente.</span><span class="sxs-lookup"><span data-stu-id="52178-105">Manages a form in a client application's form viewer.</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="52178-106">Fichier d’en-tête :</span><span class="sxs-lookup"><span data-stu-id="52178-106">Header file:</span></span>  <br/> |<span data-ttu-id="52178-107">MAPIForm. h</span><span class="sxs-lookup"><span data-stu-id="52178-107">Mapiform.h</span></span>  <br/> |
|<span data-ttu-id="52178-108">Exposé par:</span><span class="sxs-lookup"><span data-stu-id="52178-108">Exposed by:</span></span>  <br/> |<span data-ttu-id="52178-109">Afficher les objets de contexte</span><span class="sxs-lookup"><span data-stu-id="52178-109">View context objects</span></span>  <br/> |
|<span data-ttu-id="52178-110">Implémenté par :</span><span class="sxs-lookup"><span data-stu-id="52178-110">Implemented by:</span></span>  <br/> |<span data-ttu-id="52178-111">Visionneuses de formulaires</span><span class="sxs-lookup"><span data-stu-id="52178-111">Form viewers</span></span>  <br/> |
|<span data-ttu-id="52178-112">Appelé par :</span><span class="sxs-lookup"><span data-stu-id="52178-112">Called by:</span></span>  <br/> |<span data-ttu-id="52178-113">Objets de formulaires</span><span class="sxs-lookup"><span data-stu-id="52178-113">Form objects</span></span>  <br/> |
|<span data-ttu-id="52178-114">Identificateur de l'interface:</span><span class="sxs-lookup"><span data-stu-id="52178-114">Interface identifier:</span></span>  <br/> |<span data-ttu-id="52178-115">IID_IMAPIViewContext</span><span class="sxs-lookup"><span data-stu-id="52178-115">IID_IMAPIViewContext</span></span>  <br/> |
|<span data-ttu-id="52178-116">Type de pointeur:</span><span class="sxs-lookup"><span data-stu-id="52178-116">Pointer type:</span></span>  <br/> |<span data-ttu-id="52178-117">LPMAPIVIEWCONTEXT</span><span class="sxs-lookup"><span data-stu-id="52178-117">LPMAPIVIEWCONTEXT</span></span>  <br/> |
   
## <a name="vtable-order"></a><span data-ttu-id="52178-118">Ordre vtable</span><span class="sxs-lookup"><span data-stu-id="52178-118">Vtable order</span></span>

|||
|:-----|:-----|
|[<span data-ttu-id="52178-119">SetAdviseSink</span><span class="sxs-lookup"><span data-stu-id="52178-119">SetAdviseSink</span></span>](imapiviewcontext-setadvisesink.md) <br/> |<span data-ttu-id="52178-120">Gère l'inscription d'un formulaire pour recevoir des notifications sur les modifications apportées à la visionneuse.</span><span class="sxs-lookup"><span data-stu-id="52178-120">Manages a form's registration to receive notifications about changes in the viewer.</span></span>  <br/> |
|[<span data-ttu-id="52178-121">ActivateNext</span><span class="sxs-lookup"><span data-stu-id="52178-121">ActivateNext</span></span>](imapiviewcontext-activatenext.md) <br/> |<span data-ttu-id="52178-122">Active le message suivant ou précédent dans la visionneuse de formulaires.</span><span class="sxs-lookup"><span data-stu-id="52178-122">Activates the next or previous message in the form viewer.</span></span>  <br/> |
|[<span data-ttu-id="52178-123">GetPrintSetup</span><span class="sxs-lookup"><span data-stu-id="52178-123">GetPrintSetup</span></span>](imapiviewcontext-getprintsetup.md) <br/> |<span data-ttu-id="52178-124">Récupère les informations d'impression actuelles.</span><span class="sxs-lookup"><span data-stu-id="52178-124">Retrieves current printing information.</span></span>  <br/> |
|[<span data-ttu-id="52178-125">GetSaveStream</span><span class="sxs-lookup"><span data-stu-id="52178-125">GetSaveStream</span></span>](imapiviewcontext-getsavestream.md) <br/> |<span data-ttu-id="52178-126">Récupère un flux à utiliser pour enregistrer le message actif.</span><span class="sxs-lookup"><span data-stu-id="52178-126">Retrieves a stream to be used for saving the current message.</span></span>  <br/> |
|[<span data-ttu-id="52178-127">GetViewStatus</span><span class="sxs-lookup"><span data-stu-id="52178-127">GetViewStatus</span></span>](imapiviewcontext-getviewstatus.md) <br/> |<span data-ttu-id="52178-128">Récupère l'état actuel de la visionneuse.</span><span class="sxs-lookup"><span data-stu-id="52178-128">Retrieves the current viewer status.</span></span>  <br/> |
|[<span data-ttu-id="52178-129">Généré</span><span class="sxs-lookup"><span data-stu-id="52178-129">GetLastError</span></span>](imapiviewcontext-getlasterror.md) <br/> |<span data-ttu-id="52178-130">Renvoie une structure [MAPIERROR](mapierror.md) qui contient des informations sur l'erreur précédente qui s'est produite dans l'objet de contexte d'affichage.</span><span class="sxs-lookup"><span data-stu-id="52178-130">Returns a [MAPIERROR](mapierror.md) structure that contains information about the previous error occurring in the view context object.</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="52178-131">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="52178-131">See also</span></span>



[<span data-ttu-id="52178-132">Interfaces MAPI</span><span class="sxs-lookup"><span data-stu-id="52178-132">MAPI Interfaces</span></span>](mapi-interfaces.md)

