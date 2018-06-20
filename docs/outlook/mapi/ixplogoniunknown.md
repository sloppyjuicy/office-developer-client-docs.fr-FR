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
description: 'Derni�re modification�: lundi 9 mars 2015'
ms.openlocfilehash: 0b16fba054533f1cb5d21f3f4b1788c073eca13b
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19784520"
---
# <a name="ixplogon--iunknown"></a><span data-ttu-id="a5922-103">IXPLogon : IUnknown</span><span class="sxs-lookup"><span data-stu-id="a5922-103">IXPLogon : IUnknown</span></span>

  
  
<span data-ttu-id="a5922-104">**S’applique à**: Outlook</span><span class="sxs-lookup"><span data-stu-id="a5922-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="a5922-105">Fournit l’accès de spouleur MAPI à un fournisseur de transport.</span><span class="sxs-lookup"><span data-stu-id="a5922-105">Gives the MAPI spooler access to a transport provider.</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="a5922-106">Fichier d’en-tête :</span><span class="sxs-lookup"><span data-stu-id="a5922-106">Header file:</span></span>  <br/> |<span data-ttu-id="a5922-107">Mapispi.h</span><span class="sxs-lookup"><span data-stu-id="a5922-107">Mapispi.h</span></span>  <br/> |
|<span data-ttu-id="a5922-108">Exposés par :</span><span class="sxs-lookup"><span data-stu-id="a5922-108">Exposed by:</span></span>  <br/> |<span data-ttu-id="a5922-109">Objets d’ouverture de session de transport</span><span class="sxs-lookup"><span data-stu-id="a5922-109">Transport logon objects</span></span>  <br/> |
|<span data-ttu-id="a5922-110">Implémentée par :</span><span class="sxs-lookup"><span data-stu-id="a5922-110">Implemented by:</span></span>  <br/> |<span data-ttu-id="a5922-111">Fournisseurs de transport</span><span class="sxs-lookup"><span data-stu-id="a5922-111">Transport providers</span></span>  <br/> |
|<span data-ttu-id="a5922-112">Appelée par :</span><span class="sxs-lookup"><span data-stu-id="a5922-112">Called by:</span></span>  <br/> |<span data-ttu-id="a5922-113">Le spouleur MAPI</span><span class="sxs-lookup"><span data-stu-id="a5922-113">The MAPI spooler</span></span>  <br/> |
|<span data-ttu-id="a5922-114">Identificateur de l’interface :</span><span class="sxs-lookup"><span data-stu-id="a5922-114">Interface identifier:</span></span>  <br/> |<span data-ttu-id="a5922-115">IID_IXPLogon</span><span class="sxs-lookup"><span data-stu-id="a5922-115">IID_IXPLogon</span></span>  <br/> |
|<span data-ttu-id="a5922-116">Type de pointeur :</span><span class="sxs-lookup"><span data-stu-id="a5922-116">Pointer type:</span></span>  <br/> |<span data-ttu-id="a5922-117">LXPLOGON</span><span class="sxs-lookup"><span data-stu-id="a5922-117">LXPLOGON</span></span>  <br/> |
   
## <a name="vtable-order"></a><span data-ttu-id="a5922-118">Ordre vtable</span><span class="sxs-lookup"><span data-stu-id="a5922-118">Vtable order</span></span>

|||
|:-----|:-----|
|[<span data-ttu-id="a5922-119">AddressTypes</span><span class="sxs-lookup"><span data-stu-id="a5922-119">AddressTypes</span></span>](ixplogon-addresstypes.md) <br/> |<span data-ttu-id="a5922-120">Renvoie les types de destinataires qui gère le fournisseur de transport.</span><span class="sxs-lookup"><span data-stu-id="a5922-120">Returns the types of recipients that the transport provider handles.</span></span>  <br/> |
|<span data-ttu-id="a5922-121">**RegisterOptions**</span><span class="sxs-lookup"><span data-stu-id="a5922-121">**RegisterOptions**</span></span> <br/> | <span data-ttu-id="a5922-122">*Non pris en charge ou documentés.*</span><span class="sxs-lookup"><span data-stu-id="a5922-122">*Not supported or documented.*</span></span>  <br/> |
|[<span data-ttu-id="a5922-123">TransportNotify</span><span class="sxs-lookup"><span data-stu-id="a5922-123">TransportNotify</span></span>](ixplogon-transportnotify.md) <br/> |<span data-ttu-id="a5922-124">Indique l’occurrence d’un événement demandé une notification sur lequel le fournisseur de transport.</span><span class="sxs-lookup"><span data-stu-id="a5922-124">Signals the occurrence of an event about which the transport provider requested notification.</span></span>  <br/> |
|[<span data-ttu-id="a5922-125">Inactif</span><span class="sxs-lookup"><span data-stu-id="a5922-125">Idle</span></span>](ixplogon-idle.md) <br/> |<span data-ttu-id="a5922-126">Indique que le système est inactif, l’activation du fournisseur de transport effectuer des opérations de priorité basse.</span><span class="sxs-lookup"><span data-stu-id="a5922-126">Indicates that the system is idle, enabling the transport provider to perform low-priority operations.</span></span>  <br/> |
|[<span data-ttu-id="a5922-127">TransportLogoff</span><span class="sxs-lookup"><span data-stu-id="a5922-127">TransportLogoff</span></span>](ixplogon-transportlogoff.md) <br/> |<span data-ttu-id="a5922-128">Lance le processus de fermeture de session.</span><span class="sxs-lookup"><span data-stu-id="a5922-128">Initiates the logoff process.</span></span>  <br/> |
|[<span data-ttu-id="a5922-129">SubmitMessage</span><span class="sxs-lookup"><span data-stu-id="a5922-129">SubmitMessage</span></span>](ixplogon-submitmessage.md) <br/> |<span data-ttu-id="a5922-130">Indique qu’un message pour le fournisseur de transport fournir le spouleur MAPI.</span><span class="sxs-lookup"><span data-stu-id="a5922-130">Indicates that the MAPI spooler has a message for the transport provider to deliver.</span></span>  <br/> |
|[<span data-ttu-id="a5922-131">EndMessage</span><span class="sxs-lookup"><span data-stu-id="a5922-131">EndMessage</span></span>](ixplogon-endmessage.md) <br/> |<span data-ttu-id="a5922-132">Informe le fournisseur de transport que le spouleur MAPI terminé son traitement d’un message sortant.</span><span class="sxs-lookup"><span data-stu-id="a5922-132">Informs the transport provider that the MAPI spooler completed its processing on an outbound message.</span></span>  <br/> |
|[<span data-ttu-id="a5922-133">Sondage</span><span class="sxs-lookup"><span data-stu-id="a5922-133">Poll</span></span>](ixplogon-poll.md) <br/> |<span data-ttu-id="a5922-134">Indique si le fournisseur de transport a reçu un ou plusieurs messages entrants.</span><span class="sxs-lookup"><span data-stu-id="a5922-134">Indicates whether the transport provider has received one or more inbound messages.</span></span>  <br/> |
|[<span data-ttu-id="a5922-135">StartMessage</span><span class="sxs-lookup"><span data-stu-id="a5922-135">StartMessage</span></span>](ixplogon-startmessage.md) <br/> |<span data-ttu-id="a5922-136">Lance le transfert d’un message entrant à partir du fournisseur de transport pour le spouleur MAPI.</span><span class="sxs-lookup"><span data-stu-id="a5922-136">Initiates the transfer of an inbound message from the transport provider to the MAPI spooler.</span></span>  <br/> |
|[<span data-ttu-id="a5922-137">OpenStatusEntry</span><span class="sxs-lookup"><span data-stu-id="a5922-137">OpenStatusEntry</span></span>](ixplogon-openstatusentry.md) <br/> |<span data-ttu-id="a5922-138">Ouvre l’objet d’état du fournisseur de transport.</span><span class="sxs-lookup"><span data-stu-id="a5922-138">Opens the transport provider's status object.</span></span>  <br/> |
|[<span data-ttu-id="a5922-139">ValidateState</span><span class="sxs-lookup"><span data-stu-id="a5922-139">ValidateState</span></span>](ixplogon-validatestate.md) <br/> |<span data-ttu-id="a5922-140">Vérifie l’état externe du fournisseur de transport.</span><span class="sxs-lookup"><span data-stu-id="a5922-140">Checks the transport provider's external status.</span></span>  <br/> |
|[<span data-ttu-id="a5922-141">FlushQueues</span><span class="sxs-lookup"><span data-stu-id="a5922-141">FlushQueues</span></span>](ixplogon-flushqueues.md) <br/> |<span data-ttu-id="a5922-142">Demande que le fournisseur de transport remettre immédiatement tous les messages entrants ou sortants en attente.</span><span class="sxs-lookup"><span data-stu-id="a5922-142">Requests that the transport provider immediately deliver all pending inbound or outbound messages.</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="a5922-143">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="a5922-143">See also</span></span>



[<span data-ttu-id="a5922-144">Interfaces MAPI</span><span class="sxs-lookup"><span data-stu-id="a5922-144">MAPI Interfaces</span></span>](mapi-interfaces.md)

