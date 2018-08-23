---
title: IXPLogon IUnknown
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- IXPLogon
api_type:
- COM
ms.assetid: 4d24ecaf-11d0-4362-8207-be3407736d7b
description: Dernière modification le 09 mars 2015
ms.openlocfilehash: ecfbf33641c86d4f162c521466ca2bf0b79a61d5
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/23/2018
ms.locfileid: "22581404"
---
# <a name="ixplogon--iunknown"></a><span data-ttu-id="fa21b-103">IXPLogon : IUnknown</span><span class="sxs-lookup"><span data-stu-id="fa21b-103">IXPLogon : IUnknown</span></span>

  
  
<span data-ttu-id="fa21b-104">**S’applique à**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="fa21b-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="fa21b-105">Fournit l’accès de spouleur MAPI à un fournisseur de transport.</span><span class="sxs-lookup"><span data-stu-id="fa21b-105">Gives the MAPI spooler access to a transport provider.</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="fa21b-106">Fichier d’en-tête :</span><span class="sxs-lookup"><span data-stu-id="fa21b-106">Header file:</span></span>  <br/> |<span data-ttu-id="fa21b-107">Mapispi.h</span><span class="sxs-lookup"><span data-stu-id="fa21b-107">Mapispi.h</span></span>  <br/> |
|<span data-ttu-id="fa21b-108">Exposés par :</span><span class="sxs-lookup"><span data-stu-id="fa21b-108">Exposed by:</span></span>  <br/> |<span data-ttu-id="fa21b-109">Objets d’ouverture de session de transport</span><span class="sxs-lookup"><span data-stu-id="fa21b-109">Transport logon objects</span></span>  <br/> |
|<span data-ttu-id="fa21b-110">Implémentée par :</span><span class="sxs-lookup"><span data-stu-id="fa21b-110">Implemented by:</span></span>  <br/> |<span data-ttu-id="fa21b-111">Fournisseurs de transport</span><span class="sxs-lookup"><span data-stu-id="fa21b-111">Transport providers</span></span>  <br/> |
|<span data-ttu-id="fa21b-112">Appelée par :</span><span class="sxs-lookup"><span data-stu-id="fa21b-112">Called by:</span></span>  <br/> |<span data-ttu-id="fa21b-113">Le spouleur MAPI</span><span class="sxs-lookup"><span data-stu-id="fa21b-113">The MAPI spooler</span></span>  <br/> |
|<span data-ttu-id="fa21b-114">Identificateur de l’interface :</span><span class="sxs-lookup"><span data-stu-id="fa21b-114">Interface identifier:</span></span>  <br/> |<span data-ttu-id="fa21b-115">IID_IXPLogon</span><span class="sxs-lookup"><span data-stu-id="fa21b-115">IID_IXPLogon</span></span>  <br/> |
|<span data-ttu-id="fa21b-116">Type de pointeur :</span><span class="sxs-lookup"><span data-stu-id="fa21b-116">Pointer type:</span></span>  <br/> |<span data-ttu-id="fa21b-117">LXPLOGON</span><span class="sxs-lookup"><span data-stu-id="fa21b-117">LXPLOGON</span></span>  <br/> |
   
## <a name="vtable-order"></a><span data-ttu-id="fa21b-118">Ordre vtable</span><span class="sxs-lookup"><span data-stu-id="fa21b-118">Vtable order</span></span>

|||
|:-----|:-----|
|[<span data-ttu-id="fa21b-119">AddressTypes</span><span class="sxs-lookup"><span data-stu-id="fa21b-119">AddressTypes</span></span>](ixplogon-addresstypes.md) <br/> |<span data-ttu-id="fa21b-120">Renvoie les types de destinataires qui gère le fournisseur de transport.</span><span class="sxs-lookup"><span data-stu-id="fa21b-120">Returns the types of recipients that the transport provider handles.</span></span>  <br/> |
|<span data-ttu-id="fa21b-121">**RegisterOptions**</span><span class="sxs-lookup"><span data-stu-id="fa21b-121">**RegisterOptions**</span></span> <br/> | <span data-ttu-id="fa21b-122">*Non pris en charge ou documentés.*</span><span class="sxs-lookup"><span data-stu-id="fa21b-122">*Not supported or documented.*</span></span>  <br/> |
|[<span data-ttu-id="fa21b-123">TransportNotify</span><span class="sxs-lookup"><span data-stu-id="fa21b-123">TransportNotify</span></span>](ixplogon-transportnotify.md) <br/> |<span data-ttu-id="fa21b-124">Indique l’occurrence d’un événement demandé une notification sur lequel le fournisseur de transport.</span><span class="sxs-lookup"><span data-stu-id="fa21b-124">Signals the occurrence of an event about which the transport provider requested notification.</span></span>  <br/> |
|[<span data-ttu-id="fa21b-125">Inactif</span><span class="sxs-lookup"><span data-stu-id="fa21b-125">Idle</span></span>](ixplogon-idle.md) <br/> |<span data-ttu-id="fa21b-126">Indique que le système est inactif, l’activation du fournisseur de transport effectuer des opérations de priorité basse.</span><span class="sxs-lookup"><span data-stu-id="fa21b-126">Indicates that the system is idle, enabling the transport provider to perform low-priority operations.</span></span>  <br/> |
|[<span data-ttu-id="fa21b-127">TransportLogoff</span><span class="sxs-lookup"><span data-stu-id="fa21b-127">TransportLogoff</span></span>](ixplogon-transportlogoff.md) <br/> |<span data-ttu-id="fa21b-128">Lance le processus de fermeture de session.</span><span class="sxs-lookup"><span data-stu-id="fa21b-128">Initiates the logoff process.</span></span>  <br/> |
|[<span data-ttu-id="fa21b-129">SubmitMessage</span><span class="sxs-lookup"><span data-stu-id="fa21b-129">SubmitMessage</span></span>](ixplogon-submitmessage.md) <br/> |<span data-ttu-id="fa21b-130">Indique qu’un message pour le fournisseur de transport fournir le spouleur MAPI.</span><span class="sxs-lookup"><span data-stu-id="fa21b-130">Indicates that the MAPI spooler has a message for the transport provider to deliver.</span></span>  <br/> |
|[<span data-ttu-id="fa21b-131">EndMessage</span><span class="sxs-lookup"><span data-stu-id="fa21b-131">EndMessage</span></span>](ixplogon-endmessage.md) <br/> |<span data-ttu-id="fa21b-132">Informe le fournisseur de transport que le spouleur MAPI terminé son traitement d’un message sortant.</span><span class="sxs-lookup"><span data-stu-id="fa21b-132">Informs the transport provider that the MAPI spooler completed its processing on an outbound message.</span></span>  <br/> |
|[<span data-ttu-id="fa21b-133">Sondage</span><span class="sxs-lookup"><span data-stu-id="fa21b-133">Poll</span></span>](ixplogon-poll.md) <br/> |<span data-ttu-id="fa21b-134">Indique si le fournisseur de transport a reçu un ou plusieurs messages entrants.</span><span class="sxs-lookup"><span data-stu-id="fa21b-134">Indicates whether the transport provider has received one or more inbound messages.</span></span>  <br/> |
|[<span data-ttu-id="fa21b-135">StartMessage</span><span class="sxs-lookup"><span data-stu-id="fa21b-135">StartMessage</span></span>](ixplogon-startmessage.md) <br/> |<span data-ttu-id="fa21b-136">Lance le transfert d’un message entrant à partir du fournisseur de transport pour le spouleur MAPI.</span><span class="sxs-lookup"><span data-stu-id="fa21b-136">Initiates the transfer of an inbound message from the transport provider to the MAPI spooler.</span></span>  <br/> |
|[<span data-ttu-id="fa21b-137">OpenStatusEntry</span><span class="sxs-lookup"><span data-stu-id="fa21b-137">OpenStatusEntry</span></span>](ixplogon-openstatusentry.md) <br/> |<span data-ttu-id="fa21b-138">Ouvre l’objet d’état du fournisseur de transport.</span><span class="sxs-lookup"><span data-stu-id="fa21b-138">Opens the transport provider's status object.</span></span>  <br/> |
|[<span data-ttu-id="fa21b-139">ValidateState</span><span class="sxs-lookup"><span data-stu-id="fa21b-139">ValidateState</span></span>](ixplogon-validatestate.md) <br/> |<span data-ttu-id="fa21b-140">Vérifie l’état externe du fournisseur de transport.</span><span class="sxs-lookup"><span data-stu-id="fa21b-140">Checks the transport provider's external status.</span></span>  <br/> |
|[<span data-ttu-id="fa21b-141">FlushQueues</span><span class="sxs-lookup"><span data-stu-id="fa21b-141">FlushQueues</span></span>](ixplogon-flushqueues.md) <br/> |<span data-ttu-id="fa21b-142">Demande que le fournisseur de transport remettre immédiatement tous les messages entrants ou sortants en attente.</span><span class="sxs-lookup"><span data-stu-id="fa21b-142">Requests that the transport provider immediately deliver all pending inbound or outbound messages.</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="fa21b-143">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="fa21b-143">See also</span></span>



[<span data-ttu-id="fa21b-144">Interfaces MAPI</span><span class="sxs-lookup"><span data-stu-id="fa21b-144">MAPI Interfaces</span></span>](mapi-interfaces.md)

