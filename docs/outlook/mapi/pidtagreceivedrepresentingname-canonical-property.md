---
title: Propriété canonique PidTagReceivedRepresentingName
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- MAPI.PidTagReceivedRepresentingName
api_type:
- COM
ms.assetid: 8f699782-8a82-4834-bc55-a0b3cf18a117
description: Dernière modification le 9 mars 2015
ms.openlocfilehash: 5fce7e6d2163bdb8d1682dbef10d627b34ddd889
ms.sourcegitcommit: ef717c65d8dd41ababffb01eafc443c79950aed4
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 10/04/2018
ms.locfileid: "25392381"
---
# <a name="pidtagreceivedrepresentingname-canonical-property"></a><span data-ttu-id="4dcef-103">Propriété canonique PidTagReceivedRepresentingName</span><span class="sxs-lookup"><span data-stu-id="4dcef-103">PidTagReceivedRepresentingName Canonical Property</span></span>

  
  
<span data-ttu-id="4dcef-104">**S’applique à** : Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="4dcef-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="4dcef-105">Contient le nom complet de l’utilisateur de messagerie qui est représenté par l’utilisateur destinataire.</span><span class="sxs-lookup"><span data-stu-id="4dcef-105">Contains the display name for the messaging user who is represented by the receiving user.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="4dcef-106">Propriétés associées :</span><span class="sxs-lookup"><span data-stu-id="4dcef-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="4dcef-107">PR_RCVD_REPRESENTING_NAME, PR_RCVD_REPRESENTING_NAME_A, PR_RCVD_REPRESENTING_NAME_W</span><span class="sxs-lookup"><span data-stu-id="4dcef-107">PR_RCVD_REPRESENTING_NAME, PR_RCVD_REPRESENTING_NAME_A, PR_RCVD_REPRESENTING_NAME_W</span></span>  <br/> |
|<span data-ttu-id="4dcef-108">Identificateur :</span><span class="sxs-lookup"><span data-stu-id="4dcef-108">Identifier:</span></span>  <br/> |<span data-ttu-id="4dcef-109">0x0044</span><span class="sxs-lookup"><span data-stu-id="4dcef-109">0x0044</span></span>  <br/> |
|<span data-ttu-id="4dcef-110">Type de données :</span><span class="sxs-lookup"><span data-stu-id="4dcef-110">Data type:</span></span>  <br/> |<span data-ttu-id="4dcef-111">PT_UNICODE, PT_STRING8</span><span class="sxs-lookup"><span data-stu-id="4dcef-111">PT_UNICODE, PT_STRING8</span></span>  <br/> |
|<span data-ttu-id="4dcef-112">Domaine :</span><span class="sxs-lookup"><span data-stu-id="4dcef-112">Area:</span></span>  <br/> |<span data-ttu-id="4dcef-113">Address</span><span class="sxs-lookup"><span data-stu-id="4dcef-113">Address</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="4dcef-114">Remarques</span><span class="sxs-lookup"><span data-stu-id="4dcef-114">Remarks</span></span>

<span data-ttu-id="4dcef-115">Ces propriétés sont des exemples de propriétés d’adresse de l’utilisateur de messagerie qui est représenté par l’utilisateur destinataire.</span><span class="sxs-lookup"><span data-stu-id="4dcef-115">These properties are examples of the address properties for the messaging user who is being represented by the receiving user.</span></span> <span data-ttu-id="4dcef-116">Ils doivent être définis par le fournisseur de transport entrant, qui est également responsable de l’autorisation ou de vérification du délégué.</span><span class="sxs-lookup"><span data-stu-id="4dcef-116">They must be set by the incoming transport provider, which is also responsible for authorization or verification of the delegate.</span></span> <span data-ttu-id="4dcef-117">Si aucun utilisateur de messagerie n’est représenté, ces propriétés doivent être définies pour le nom d’affichage contenu dans la propriété **PR_RECEIVED_BY_NAME** ([PidTagReceivedByName](pidtagreceivedbyname-canonical-property.md)).</span><span class="sxs-lookup"><span data-stu-id="4dcef-117">If no messaging user is being represented, these properties should be set to the display name contained in the **PR_RECEIVED_BY_NAME** ([PidTagReceivedByName](pidtagreceivedbyname-canonical-property.md)) property.</span></span>
  
<span data-ttu-id="4dcef-118">Une application client répondre à un message reçu de la part d’un autre client doit copier ces propriétés à partir du message reçu dans la propriété **PR_SENT_REPRESENTING_NAME** ([PidTagSentRepresentingName](pidtagsentrepresentingname-canonical-property.md)) pour la réponse.</span><span class="sxs-lookup"><span data-stu-id="4dcef-118">A client application replying to a message received on behalf of another client should copy these properties from the received message into the **PR_SENT_REPRESENTING_NAME** ([PidTagSentRepresentingName](pidtagsentrepresentingname-canonical-property.md)) property for the reply.</span></span>
  
## <a name="related-resources"></a><span data-ttu-id="4dcef-119">Ressources connexes</span><span class="sxs-lookup"><span data-stu-id="4dcef-119">Related resources</span></span>

### <a name="protocol-specifications"></a><span data-ttu-id="4dcef-120">Spécifications du protocole</span><span class="sxs-lookup"><span data-stu-id="4dcef-120">Protocol specifications</span></span>

<span data-ttu-id="4dcef-121">[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="4dcef-121">[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="4dcef-122">Fournit des références aux spécifications du protocole Exchange Server associées.</span><span class="sxs-lookup"><span data-stu-id="4dcef-122">Provides references to related Exchange Server protocol specifications.</span></span>
    
<span data-ttu-id="4dcef-123">[[MS-OXOMSG]](https://msdn.microsoft.com/library/daa9120f-f325-4afb-a738-28f91049ab3c%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="4dcef-123">[[MS-OXOMSG]](https://msdn.microsoft.com/library/daa9120f-f325-4afb-a738-28f91049ab3c%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="4dcef-124">Spécifie les propriétés et les opérations qui sont autorisées pour les objets de message électronique.</span><span class="sxs-lookup"><span data-stu-id="4dcef-124">Specifies the properties and operations that are permissible for email message objects.</span></span>
    
<span data-ttu-id="4dcef-125">[[MS-OXCFXICS]](https://msdn.microsoft.com/library/b9752f3d-d50d-44b8-9e6b-608a117c8532%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="4dcef-125">[[MS-OXCFXICS]](https://msdn.microsoft.com/library/b9752f3d-d50d-44b8-9e6b-608a117c8532%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="4dcef-126">Gère l’ordre et le flux pour les transferts de données entre un client et le serveur.</span><span class="sxs-lookup"><span data-stu-id="4dcef-126">Handles the order and flow for data transfers between a client and server.</span></span>
    
<span data-ttu-id="4dcef-127">[[MS-OXCICAL]](https://msdn.microsoft.com/library/a685a040-5b69-4c84-b084-795113fb4012%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="4dcef-127">[[MS-OXCICAL]](https://msdn.microsoft.com/library/a685a040-5b69-4c84-b084-795113fb4012%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="4dcef-128">La conversion entre IETF RFC2445, RFC2446, RFC2447 et rendez-vous et des objets de la conférence.</span><span class="sxs-lookup"><span data-stu-id="4dcef-128">Converts between IETF RFC2445, RFC2446, and RFC2447, and appointment and meeting objects.</span></span>
    
<span data-ttu-id="4dcef-129">[[MS-OXODLGT]](https://msdn.microsoft.com/library/01a89b11-9c43-4c40-b147-8f6a1ef5a44f%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="4dcef-129">[[MS-OXODLGT]](https://msdn.microsoft.com/library/01a89b11-9c43-4c40-b147-8f6a1ef5a44f%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="4dcef-130">Spécifie les méthodes pour la connexion et configurer des boîtes aux lettres en tant que les délégués et les interactions avec les objets de messagerie et de calendrier lorsqu’ils agissent au nom d’un autre utilisateur.</span><span class="sxs-lookup"><span data-stu-id="4dcef-130">Specifies methods for connecting to and configuring mailboxes as delegates, and interactions with message and calendar objects when they act on behalf of another user.</span></span>
    
<span data-ttu-id="4dcef-131">[[MS-OXTNEF]](https://msdn.microsoft.com/library/1f0544d7-30b7-4194-b58f-adc82f3763bb%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="4dcef-131">[[MS-OXTNEF]](https://msdn.microsoft.com/library/1f0544d7-30b7-4194-b58f-adc82f3763bb%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="4dcef-132">Code et décode des objets message et la pièce jointe à une représentation sous forme de flux efficace.</span><span class="sxs-lookup"><span data-stu-id="4dcef-132">Encodes and decodes message and attachment objects to an efficient stream representation.</span></span>
    
### <a name="header-files"></a><span data-ttu-id="4dcef-133">Fichiers d’en-tête</span><span class="sxs-lookup"><span data-stu-id="4dcef-133">Header files</span></span>

<span data-ttu-id="4dcef-134">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="4dcef-134">Mapidefs.h</span></span>
  
> <span data-ttu-id="4dcef-135">Fournit des définitions de type de données.</span><span class="sxs-lookup"><span data-stu-id="4dcef-135">Provides data type definitions.</span></span>
    
<span data-ttu-id="4dcef-136">MAPITAGS.h</span><span class="sxs-lookup"><span data-stu-id="4dcef-136">Mapitags.h</span></span>
  
> <span data-ttu-id="4dcef-137">Contient les définitions des propriétés répertoriées en tant que propriétés associées.</span><span class="sxs-lookup"><span data-stu-id="4dcef-137">Contains definitions of properties listed as associated properties.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="4dcef-138">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="4dcef-138">See also</span></span>



[<span data-ttu-id="4dcef-139">Propriétés MAPI</span><span class="sxs-lookup"><span data-stu-id="4dcef-139">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="4dcef-140">Propriétés canoniques MAPI</span><span class="sxs-lookup"><span data-stu-id="4dcef-140">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="4dcef-141">Mappage des noms de propriétés canoniques aux noms MAPI</span><span class="sxs-lookup"><span data-stu-id="4dcef-141">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="4dcef-142">Mappage des noms MAPI aux noms de propriétés canoniques</span><span class="sxs-lookup"><span data-stu-id="4dcef-142">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

