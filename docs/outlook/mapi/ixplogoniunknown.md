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
description: Dernière modification le 9 mars 2015
ms.openlocfilehash: 46f4e3fc8f554f332ab9b1d8a6cb33e9e21dd9a5
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/28/2019
ms.locfileid: "33432533"
---
# <a name="ixplogon--iunknown"></a><span data-ttu-id="20c3c-103">IXPLogon : IUnknown</span><span class="sxs-lookup"><span data-stu-id="20c3c-103">IXPLogon : IUnknown</span></span>

  
  
<span data-ttu-id="20c3c-104">**S’applique à** : Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="20c3c-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="20c3c-105">Donne aupooler MAPI l’accès à un fournisseur de transport.</span><span class="sxs-lookup"><span data-stu-id="20c3c-105">Gives the MAPI spooler access to a transport provider.</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="20c3c-106">Fichier d’en-tête :</span><span class="sxs-lookup"><span data-stu-id="20c3c-106">Header file:</span></span>  <br/> |<span data-ttu-id="20c3c-107">Mapispi.h</span><span class="sxs-lookup"><span data-stu-id="20c3c-107">Mapispi.h</span></span>  <br/> |
|<span data-ttu-id="20c3c-108">Exposé par :</span><span class="sxs-lookup"><span data-stu-id="20c3c-108">Exposed by:</span></span>  <br/> |<span data-ttu-id="20c3c-109">Objets d’logo de transport</span><span class="sxs-lookup"><span data-stu-id="20c3c-109">Transport logon objects</span></span>  <br/> |
|<span data-ttu-id="20c3c-110">Implémenté par :</span><span class="sxs-lookup"><span data-stu-id="20c3c-110">Implemented by:</span></span>  <br/> |<span data-ttu-id="20c3c-111">Fournisseurs de transport</span><span class="sxs-lookup"><span data-stu-id="20c3c-111">Transport providers</span></span>  <br/> |
|<span data-ttu-id="20c3c-112">Appelé par :</span><span class="sxs-lookup"><span data-stu-id="20c3c-112">Called by:</span></span>  <br/> |<span data-ttu-id="20c3c-113">Lepooler MAPI</span><span class="sxs-lookup"><span data-stu-id="20c3c-113">The MAPI spooler</span></span>  <br/> |
|<span data-ttu-id="20c3c-114">Identificateur d’interface :</span><span class="sxs-lookup"><span data-stu-id="20c3c-114">Interface identifier:</span></span>  <br/> |<span data-ttu-id="20c3c-115">IID_IXPLogon</span><span class="sxs-lookup"><span data-stu-id="20c3c-115">IID_IXPLogon</span></span>  <br/> |
|<span data-ttu-id="20c3c-116">Type de pointeur :</span><span class="sxs-lookup"><span data-stu-id="20c3c-116">Pointer type:</span></span>  <br/> |<span data-ttu-id="20c3c-117">LXPLOGON</span><span class="sxs-lookup"><span data-stu-id="20c3c-117">LXPLOGON</span></span>  <br/> |
   
## <a name="vtable-order"></a><span data-ttu-id="20c3c-118">Ordre des vtables</span><span class="sxs-lookup"><span data-stu-id="20c3c-118">Vtable order</span></span>

|||
|:-----|:-----|
|[<span data-ttu-id="20c3c-119">AddressTypes</span><span class="sxs-lookup"><span data-stu-id="20c3c-119">AddressTypes</span></span>](ixplogon-addresstypes.md) <br/> |<span data-ttu-id="20c3c-120">Renvoie les types de destinataires gérés par le fournisseur de transport.</span><span class="sxs-lookup"><span data-stu-id="20c3c-120">Returns the types of recipients that the transport provider handles.</span></span>  <br/> |
|<span data-ttu-id="20c3c-121">**RegisterOptions**</span><span class="sxs-lookup"><span data-stu-id="20c3c-121">**RegisterOptions**</span></span> <br/> | <span data-ttu-id="20c3c-122">*Non pris en charge ou documenté.*</span><span class="sxs-lookup"><span data-stu-id="20c3c-122">*Not supported or documented.*</span></span>  <br/> |
|[<span data-ttu-id="20c3c-123">TransportNotify</span><span class="sxs-lookup"><span data-stu-id="20c3c-123">TransportNotify</span></span>](ixplogon-transportnotify.md) <br/> |<span data-ttu-id="20c3c-124">Signale l’occurrence d’un événement sur lequel le fournisseur de transport a demandé une notification.</span><span class="sxs-lookup"><span data-stu-id="20c3c-124">Signals the occurrence of an event about which the transport provider requested notification.</span></span>  <br/> |
|[<span data-ttu-id="20c3c-125">Inactif</span><span class="sxs-lookup"><span data-stu-id="20c3c-125">Idle</span></span>](ixplogon-idle.md) <br/> |<span data-ttu-id="20c3c-126">Indique que le système est inactif, ce qui permet au fournisseur de transport d’effectuer des opérations de faible priorité.</span><span class="sxs-lookup"><span data-stu-id="20c3c-126">Indicates that the system is idle, enabling the transport provider to perform low-priority operations.</span></span>  <br/> |
|[<span data-ttu-id="20c3c-127">TransportLogoff</span><span class="sxs-lookup"><span data-stu-id="20c3c-127">TransportLogoff</span></span>](ixplogon-transportlogoff.md) <br/> |<span data-ttu-id="20c3c-128">Lance le processus de ffage de logo.</span><span class="sxs-lookup"><span data-stu-id="20c3c-128">Initiates the logoff process.</span></span>  <br/> |
|[<span data-ttu-id="20c3c-129">SubmitMessage</span><span class="sxs-lookup"><span data-stu-id="20c3c-129">SubmitMessage</span></span>](ixplogon-submitmessage.md) <br/> |<span data-ttu-id="20c3c-130">Indique que lepooler MAPI a un message à remettre au fournisseur de transport.</span><span class="sxs-lookup"><span data-stu-id="20c3c-130">Indicates that the MAPI spooler has a message for the transport provider to deliver.</span></span>  <br/> |
|[<span data-ttu-id="20c3c-131">EndMessage</span><span class="sxs-lookup"><span data-stu-id="20c3c-131">EndMessage</span></span>](ixplogon-endmessage.md) <br/> |<span data-ttu-id="20c3c-132">Informe le fournisseur de transport que lepooler MAPI a terminé son traitement sur un message sortant.</span><span class="sxs-lookup"><span data-stu-id="20c3c-132">Informs the transport provider that the MAPI spooler completed its processing on an outbound message.</span></span>  <br/> |
|[<span data-ttu-id="20c3c-133">Sondage</span><span class="sxs-lookup"><span data-stu-id="20c3c-133">Poll</span></span>](ixplogon-poll.md) <br/> |<span data-ttu-id="20c3c-134">Indique si le fournisseur de transport a reçu un ou plusieurs messages entrants.</span><span class="sxs-lookup"><span data-stu-id="20c3c-134">Indicates whether the transport provider has received one or more inbound messages.</span></span>  <br/> |
|[<span data-ttu-id="20c3c-135">StartMessage</span><span class="sxs-lookup"><span data-stu-id="20c3c-135">StartMessage</span></span>](ixplogon-startmessage.md) <br/> |<span data-ttu-id="20c3c-136">Lance le transfert d’un message entrant du fournisseur de transport vers lepooler MAPI.</span><span class="sxs-lookup"><span data-stu-id="20c3c-136">Initiates the transfer of an inbound message from the transport provider to the MAPI spooler.</span></span>  <br/> |
|[<span data-ttu-id="20c3c-137">OpenStatusEntry</span><span class="sxs-lookup"><span data-stu-id="20c3c-137">OpenStatusEntry</span></span>](ixplogon-openstatusentry.md) <br/> |<span data-ttu-id="20c3c-138">Ouvre l’objet d’état du fournisseur de transport.</span><span class="sxs-lookup"><span data-stu-id="20c3c-138">Opens the transport provider's status object.</span></span>  <br/> |
|[<span data-ttu-id="20c3c-139">ValidateState</span><span class="sxs-lookup"><span data-stu-id="20c3c-139">ValidateState</span></span>](ixplogon-validatestate.md) <br/> |<span data-ttu-id="20c3c-140">Vérifie l’état externe du fournisseur de transport.</span><span class="sxs-lookup"><span data-stu-id="20c3c-140">Checks the transport provider's external status.</span></span>  <br/> |
|[<span data-ttu-id="20c3c-141">FlushQueues</span><span class="sxs-lookup"><span data-stu-id="20c3c-141">FlushQueues</span></span>](ixplogon-flushqueues.md) <br/> |<span data-ttu-id="20c3c-142">Demande au fournisseur de transport de remettre immédiatement tous les messages entrants ou sortants en attente.</span><span class="sxs-lookup"><span data-stu-id="20c3c-142">Requests that the transport provider immediately deliver all pending inbound or outbound messages.</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="20c3c-143">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="20c3c-143">See also</span></span>



[<span data-ttu-id="20c3c-144">Interfaces MAPI</span><span class="sxs-lookup"><span data-stu-id="20c3c-144">MAPI Interfaces</span></span>](mapi-interfaces.md)

