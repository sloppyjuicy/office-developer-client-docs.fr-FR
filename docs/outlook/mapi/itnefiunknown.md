---
title: ITnef IUnknown
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- ITnef
api_type:
- COM
ms.assetid: eddca896-9497-4425-9904-87ef3cbae298
description: Dernière modification le 9 mars 2015
ms.openlocfilehash: 1f815a914deb5e21f3d913abe46a84cc7a32b4ee
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/28/2019
ms.locfileid: "33428514"
---
# <a name="itnef--iunknown"></a><span data-ttu-id="e9e4a-103">ITnef : IUnknown</span><span class="sxs-lookup"><span data-stu-id="e9e4a-103">ITnef : IUnknown</span></span>

  
  
<span data-ttu-id="e9e4a-104">**S’applique à** : Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="e9e4a-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="e9e4a-105">Fournit des méthodes pour encapsuler des propriétés MAPI qui ne sont pas prises en charge par un système de messagerie dans des flux binaires qui peuvent être attachés à des messages.</span><span class="sxs-lookup"><span data-stu-id="e9e4a-105">Provides methods for encapsulating MAPI properties that are not supported by a messaging system into binary streams that can be attached to messages.</span></span> <span data-ttu-id="e9e4a-106">Le format utilisé pour cette encapsulation est le format TNEF (Transport-Neutral Encapsulation Format).</span><span class="sxs-lookup"><span data-stu-id="e9e4a-106">The format used for this encapsulation is the Transport-Neutral Encapsulation Format (TNEF).</span></span> <span data-ttu-id="e9e4a-107">Le fournisseur de transport cible ou l'application cliente basée sur MAPI peut ensuite, lors de la réception d'un message incluant une pièce jointe TNEF, récupérer les propriétés à partir de la pièce jointe.</span><span class="sxs-lookup"><span data-stu-id="e9e4a-107">The target transport provider or MAPI-based client application can then, on receiving a message that includes a TNEF attachment, recover the properties from the attachment.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="e9e4a-108">Fichier d’en-tête :</span><span class="sxs-lookup"><span data-stu-id="e9e4a-108">Header file:</span></span>  <br/> |<span data-ttu-id="e9e4a-109">TNEF. h</span><span class="sxs-lookup"><span data-stu-id="e9e4a-109">Tnef.h</span></span>  <br/> |
|<span data-ttu-id="e9e4a-110">Exposé par:</span><span class="sxs-lookup"><span data-stu-id="e9e4a-110">Exposed by:</span></span>  <br/> |<span data-ttu-id="e9e4a-111">Objets TNEF</span><span class="sxs-lookup"><span data-stu-id="e9e4a-111">TNEF objects</span></span>  <br/> |
|<span data-ttu-id="e9e4a-112">Implémenté par :</span><span class="sxs-lookup"><span data-stu-id="e9e4a-112">Implemented by:</span></span>  <br/> |<span data-ttu-id="e9e4a-113">MAPI</span><span class="sxs-lookup"><span data-stu-id="e9e4a-113">MAPI</span></span>  <br/> |
|<span data-ttu-id="e9e4a-114">Appelé par :</span><span class="sxs-lookup"><span data-stu-id="e9e4a-114">Called by:</span></span>  <br/> |<span data-ttu-id="e9e4a-115">Fournisseurs de transport, fournisseurs de banques de messages et passerelles</span><span class="sxs-lookup"><span data-stu-id="e9e4a-115">Transport providers, message store providers, and gateways</span></span>  <br/> |
|<span data-ttu-id="e9e4a-116">Identificateur de l'interface:</span><span class="sxs-lookup"><span data-stu-id="e9e4a-116">Interface identifier:</span></span>  <br/> |<span data-ttu-id="e9e4a-117">IID_ITNEF</span><span class="sxs-lookup"><span data-stu-id="e9e4a-117">IID_ITNEF</span></span>  <br/> |
|<span data-ttu-id="e9e4a-118">Type de pointeur:</span><span class="sxs-lookup"><span data-stu-id="e9e4a-118">Pointer type:</span></span>  <br/> |<span data-ttu-id="e9e4a-119">LPTNEF</span><span class="sxs-lookup"><span data-stu-id="e9e4a-119">LPTNEF</span></span>  <br/> |
   
## <a name="vtable-order"></a><span data-ttu-id="e9e4a-120">Ordre vtable</span><span class="sxs-lookup"><span data-stu-id="e9e4a-120">Vtable order</span></span>

|||
|:-----|:-----|
|[<span data-ttu-id="e9e4a-121">AddProps</span><span class="sxs-lookup"><span data-stu-id="e9e4a-121">AddProps</span></span>](itnef-addprops.md) <br/> |<span data-ttu-id="e9e4a-122">Permet au fournisseur de services d'appel ou à la passerelle d'ajouter des propriétés à l'encapsulation d'un message ou d'une pièce jointe.</span><span class="sxs-lookup"><span data-stu-id="e9e4a-122">Enables the calling service provider or gateway to add properties to the encapsulation of a message or an attachment.</span></span>  <br/> |
|[<span data-ttu-id="e9e4a-123">ExtractProps</span><span class="sxs-lookup"><span data-stu-id="e9e4a-123">ExtractProps</span></span>](itnef-extractprops.md) <br/> |<span data-ttu-id="e9e4a-124">Extrait les propriétés d'une encapsulation TNEF.</span><span class="sxs-lookup"><span data-stu-id="e9e4a-124">Extracts the properties from a TNEF encapsulation.</span></span>  <br/> |
|[<span data-ttu-id="e9e4a-125">Finish</span><span class="sxs-lookup"><span data-stu-id="e9e4a-125">Finish</span></span>](itnef-finish.md) <br/> |<span data-ttu-id="e9e4a-126">Termine le traitement de toutes les opérations TNEF mises en file d'attente et en attente.</span><span class="sxs-lookup"><span data-stu-id="e9e4a-126">Finishes processing for all TNEF operations that are queued and waiting.</span></span>  <br/> |
|[<span data-ttu-id="e9e4a-127">OpenTaggedBody</span><span class="sxs-lookup"><span data-stu-id="e9e4a-127">OpenTaggedBody</span></span>](itnef-opentaggedbody.md) <br/> |<span data-ttu-id="e9e4a-128">Ouvre une interface de flux sur le texte d'un message encapsulé.</span><span class="sxs-lookup"><span data-stu-id="e9e4a-128">Opens a stream interface on the text of an encapsulated message.</span></span>  <br/> |
|[<span data-ttu-id="e9e4a-129">SetProps</span><span class="sxs-lookup"><span data-stu-id="e9e4a-129">SetProps</span></span>](itnef-setprops.md) <br/> |<span data-ttu-id="e9e4a-130">Définit la valeur d'une ou plusieurs propriétés pour un message encapsulé ou une pièce jointe sans modifier le message ou la pièce jointe d'origine.</span><span class="sxs-lookup"><span data-stu-id="e9e4a-130">Sets the value of one or more properties for an encapsulated message or attachment without modifying the original message or attachment.</span></span>  <br/> |
|[<span data-ttu-id="e9e4a-131">EncodeRecips</span><span class="sxs-lookup"><span data-stu-id="e9e4a-131">EncodeRecips</span></span>](itnef-encoderecips.md) <br/> |<span data-ttu-id="e9e4a-132">Encode une vue pour la table de destinataires d'un message dans le flux de données TNEF pour le message.</span><span class="sxs-lookup"><span data-stu-id="e9e4a-132">Encodes a view for a message's recipient table in the TNEF data stream for the message.</span></span>  <br/> |
|[<span data-ttu-id="e9e4a-133">FinishComponent</span><span class="sxs-lookup"><span data-stu-id="e9e4a-133">FinishComponent</span></span>](itnef-finishcomponent.md) <br/> |<span data-ttu-id="e9e4a-134">Traite les composants individuels d'un message un à la fois dans un flux TNEF.</span><span class="sxs-lookup"><span data-stu-id="e9e4a-134">Processes individual components from a message one at a time into a TNEF stream.</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="e9e4a-135">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="e9e4a-135">See also</span></span>



[<span data-ttu-id="e9e4a-136">Interfaces MAPI</span><span class="sxs-lookup"><span data-stu-id="e9e4a-136">MAPI Interfaces</span></span>](mapi-interfaces.md)

