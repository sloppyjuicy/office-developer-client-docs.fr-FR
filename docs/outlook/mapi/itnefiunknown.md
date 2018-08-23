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
description: Dernière modification le 09 mars 2015
ms.openlocfilehash: 1803707b46b9b58e7372e7e58cc36241d0ebdb4d
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/23/2018
ms.locfileid: "22571723"
---
# <a name="itnef--iunknown"></a><span data-ttu-id="b875e-103">ITnef : IUnknown</span><span class="sxs-lookup"><span data-stu-id="b875e-103">ITnef : IUnknown</span></span>

  
  
<span data-ttu-id="b875e-104">**S’applique à**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="b875e-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="b875e-105">Fournit des méthodes pour encapsuler les propriétés MAPI qui ne sont pas pris en charge par un système de messagerie en flux binaires qui peuvent être joints aux messages.</span><span class="sxs-lookup"><span data-stu-id="b875e-105">Provides methods for encapsulating MAPI properties that are not supported by a messaging system into binary streams that can be attached to messages.</span></span> <span data-ttu-id="b875e-106">Le format utilisé pour cette encapsulation est le Transport-Neutral Encapsulation Format TNEF ().</span><span class="sxs-lookup"><span data-stu-id="b875e-106">The format used for this encapsulation is the Transport-Neutral Encapsulation Format (TNEF).</span></span> <span data-ttu-id="b875e-107">Le fournisseur de transport cible ou d’une application cliente basée sur MAPI permettre ensuite, reçoit un message contenant une pièce jointe TNEF, récupérer les propriétés de la pièce jointe.</span><span class="sxs-lookup"><span data-stu-id="b875e-107">The target transport provider or MAPI-based client application can then, on receiving a message that includes a TNEF attachment, recover the properties from the attachment.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="b875e-108">Fichier d’en-tête :</span><span class="sxs-lookup"><span data-stu-id="b875e-108">Header file:</span></span>  <br/> |<span data-ttu-id="b875e-109">TNEF.h</span><span class="sxs-lookup"><span data-stu-id="b875e-109">Tnef.h</span></span>  <br/> |
|<span data-ttu-id="b875e-110">Exposés par :</span><span class="sxs-lookup"><span data-stu-id="b875e-110">Exposed by:</span></span>  <br/> |<span data-ttu-id="b875e-111">Objets TNEF</span><span class="sxs-lookup"><span data-stu-id="b875e-111">TNEF objects</span></span>  <br/> |
|<span data-ttu-id="b875e-112">Implémentée par :</span><span class="sxs-lookup"><span data-stu-id="b875e-112">Implemented by:</span></span>  <br/> |<span data-ttu-id="b875e-113">MAPI</span><span class="sxs-lookup"><span data-stu-id="b875e-113">MAPI</span></span>  <br/> |
|<span data-ttu-id="b875e-114">Appelée par :</span><span class="sxs-lookup"><span data-stu-id="b875e-114">Called by:</span></span>  <br/> |<span data-ttu-id="b875e-115">Fournisseurs de transport, les fournisseurs de banque de message et passerelles</span><span class="sxs-lookup"><span data-stu-id="b875e-115">Transport providers, message store providers, and gateways</span></span>  <br/> |
|<span data-ttu-id="b875e-116">Identificateur de l’interface :</span><span class="sxs-lookup"><span data-stu-id="b875e-116">Interface identifier:</span></span>  <br/> |<span data-ttu-id="b875e-117">IID_ITNEF</span><span class="sxs-lookup"><span data-stu-id="b875e-117">IID_ITNEF</span></span>  <br/> |
|<span data-ttu-id="b875e-118">Type de pointeur :</span><span class="sxs-lookup"><span data-stu-id="b875e-118">Pointer type:</span></span>  <br/> |<span data-ttu-id="b875e-119">LPTNEF</span><span class="sxs-lookup"><span data-stu-id="b875e-119">LPTNEF</span></span>  <br/> |
   
## <a name="vtable-order"></a><span data-ttu-id="b875e-120">Ordre vtable</span><span class="sxs-lookup"><span data-stu-id="b875e-120">Vtable order</span></span>

|||
|:-----|:-----|
|[<span data-ttu-id="b875e-121">AddProps</span><span class="sxs-lookup"><span data-stu-id="b875e-121">AddProps</span></span>](itnef-addprops.md) <br/> |<span data-ttu-id="b875e-122">Permet à l’appelant fournisseur de services ou la passerelle ajouter des propriétés à l’encapsulation d’un message ou d’une pièce jointe.</span><span class="sxs-lookup"><span data-stu-id="b875e-122">Enables the calling service provider or gateway to add properties to the encapsulation of a message or an attachment.</span></span>  <br/> |
|[<span data-ttu-id="b875e-123">ExtractProps</span><span class="sxs-lookup"><span data-stu-id="b875e-123">ExtractProps</span></span>](itnef-extractprops.md) <br/> |<span data-ttu-id="b875e-124">Extrait les propriétés d’une encapsulation TNEF.</span><span class="sxs-lookup"><span data-stu-id="b875e-124">Extracts the properties from a TNEF encapsulation.</span></span>  <br/> |
|[<span data-ttu-id="b875e-125">Terminer</span><span class="sxs-lookup"><span data-stu-id="b875e-125">Finish</span></span>](itnef-finish.md) <br/> |<span data-ttu-id="b875e-126">Fin de traitement de toutes les opérations TNEF sont en file d’attente et en attente.</span><span class="sxs-lookup"><span data-stu-id="b875e-126">Finishes processing for all TNEF operations that are queued and waiting.</span></span>  <br/> |
|[<span data-ttu-id="b875e-127">OpenTaggedBody</span><span class="sxs-lookup"><span data-stu-id="b875e-127">OpenTaggedBody</span></span>](itnef-opentaggedbody.md) <br/> |<span data-ttu-id="b875e-128">Ouvre une interface de flux sur le texte d’un message encapsulé.</span><span class="sxs-lookup"><span data-stu-id="b875e-128">Opens a stream interface on the text of an encapsulated message.</span></span>  <br/> |
|[<span data-ttu-id="b875e-129">SetProps</span><span class="sxs-lookup"><span data-stu-id="b875e-129">SetProps</span></span>](itnef-setprops.md) <br/> |<span data-ttu-id="b875e-130">Définit la valeur d’une ou plusieurs propriétés d’un message encapsulé ou d’une pièce jointe sans modifier le message d’origine ou une pièce jointe.</span><span class="sxs-lookup"><span data-stu-id="b875e-130">Sets the value of one or more properties for an encapsulated message or attachment without modifying the original message or attachment.</span></span>  <br/> |
|[<span data-ttu-id="b875e-131">EncodeRecips</span><span class="sxs-lookup"><span data-stu-id="b875e-131">EncodeRecips</span></span>](itnef-encoderecips.md) <br/> |<span data-ttu-id="b875e-132">Encode un affichage pour la table des destinataires d’un message dans le flux de données TNEF pour le message.</span><span class="sxs-lookup"><span data-stu-id="b875e-132">Encodes a view for a message's recipient table in the TNEF data stream for the message.</span></span>  <br/> |
|[<span data-ttu-id="b875e-133">FinishComponent</span><span class="sxs-lookup"><span data-stu-id="b875e-133">FinishComponent</span></span>](itnef-finishcomponent.md) <br/> |<span data-ttu-id="b875e-134">Traite des composants individuels à partir d’un message à la fois dans un objet stream TNEF.</span><span class="sxs-lookup"><span data-stu-id="b875e-134">Processes individual components from a message one at a time into a TNEF stream.</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="b875e-135">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="b875e-135">See also</span></span>



[<span data-ttu-id="b875e-136">Interfaces MAPI</span><span class="sxs-lookup"><span data-stu-id="b875e-136">MAPI Interfaces</span></span>](mapi-interfaces.md)

