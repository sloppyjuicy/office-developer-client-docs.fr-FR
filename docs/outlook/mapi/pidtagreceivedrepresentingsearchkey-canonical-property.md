---
title: Propriété canonique PidTagReceivedRepresentingSearchKey
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- MAPI.PidTagReceivedRepresentingSearchKey
api_type:
- COM
ms.assetid: 234c797c-4a3c-4e05-be22-2a2fa377871f
description: Dernière modification le 9 mars 2015
ms.openlocfilehash: bcf310138e4b43b1cc36a177194f721c401caba6
ms.sourcegitcommit: ef717c65d8dd41ababffb01eafc443c79950aed4
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 10/04/2018
ms.locfileid: "25394761"
---
# <a name="pidtagreceivedrepresentingsearchkey-canonical-property"></a><span data-ttu-id="84ec8-103">Propriété canonique PidTagReceivedRepresentingSearchKey</span><span class="sxs-lookup"><span data-stu-id="84ec8-103">PidTagReceivedRepresentingSearchKey Canonical Property</span></span>

  
  
<span data-ttu-id="84ec8-104">**S’applique à** : Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="84ec8-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="84ec8-105">Contient la clé de recherche pour l’utilisateur de messagerie représenté par l’utilisateur destinataire.</span><span class="sxs-lookup"><span data-stu-id="84ec8-105">Contains the search key for the messaging user represented by the receiving user.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="84ec8-106">Propriétés associées :</span><span class="sxs-lookup"><span data-stu-id="84ec8-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="84ec8-107">PR_RCVD_REPRESENTING_SEARCH_KEY</span><span class="sxs-lookup"><span data-stu-id="84ec8-107">PR_RCVD_REPRESENTING_SEARCH_KEY</span></span>  <br/> |
|<span data-ttu-id="84ec8-108">Identificateur :</span><span class="sxs-lookup"><span data-stu-id="84ec8-108">Identifier:</span></span>  <br/> |<span data-ttu-id="84ec8-109">0x0052</span><span class="sxs-lookup"><span data-stu-id="84ec8-109">0x0052</span></span>  <br/> |
|<span data-ttu-id="84ec8-110">Type de données :</span><span class="sxs-lookup"><span data-stu-id="84ec8-110">Data type:</span></span>  <br/> |<span data-ttu-id="84ec8-111">PT_BINARY</span><span class="sxs-lookup"><span data-stu-id="84ec8-111">PT_BINARY</span></span>  <br/> |
|<span data-ttu-id="84ec8-112">Domaine :</span><span class="sxs-lookup"><span data-stu-id="84ec8-112">Area:</span></span>  <br/> |<span data-ttu-id="84ec8-113">Address</span><span class="sxs-lookup"><span data-stu-id="84ec8-113">Address</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="84ec8-114">Remarques</span><span class="sxs-lookup"><span data-stu-id="84ec8-114">Remarks</span></span>

<span data-ttu-id="84ec8-115">Cette propriété est une des propriétés d’adresse pour l’utilisateur de messagerie en cours représenté par l’utilisateur destinataire.</span><span class="sxs-lookup"><span data-stu-id="84ec8-115">This property is one of the address properties for the messaging user being represented by the receiving user.</span></span> <span data-ttu-id="84ec8-116">Elle doit être définie par le fournisseur de transport entrant, qui est également responsable de l’autorisation ou de vérification du délégué.</span><span class="sxs-lookup"><span data-stu-id="84ec8-116">It must be set by the incoming transport provider, which is also responsible for authorization or verification of the delegate.</span></span> <span data-ttu-id="84ec8-117">Si aucun utilisateur de messagerie n’est représenté, cette propriété doit être définie pour la clé de recherche contenue dans la propriété **PR_RECEIVED_BY_SEARCH_KEY** ([PidTagReceivedBySearchKey](pidtagreceivedbysearchkey-canonical-property.md)).</span><span class="sxs-lookup"><span data-stu-id="84ec8-117">If no messaging user is being represented, this property should be set to the search key contained in the **PR_RECEIVED_BY_SEARCH_KEY** ([PidTagReceivedBySearchKey](pidtagreceivedbysearchkey-canonical-property.md)) property.</span></span>
  
<span data-ttu-id="84ec8-118">Une application client répondre à un message reçu de la part d’un autre client doit copier cette propriété à partir du message reçu dans la propriété **PR_SENT_REPRESENTING_SEARCH_KEY** ([PidTagSentRepresentingSearchKey](pidtagsentrepresentingsearchkey-canonical-property.md)) pour la réponse.</span><span class="sxs-lookup"><span data-stu-id="84ec8-118">A client application replying to a message received on behalf of another client should copy this property from the received message into the **PR_SENT_REPRESENTING_SEARCH_KEY** ([PidTagSentRepresentingSearchKey](pidtagsentrepresentingsearchkey-canonical-property.md)) property for the reply.</span></span>
  
## <a name="related-resources"></a><span data-ttu-id="84ec8-119">Ressources connexes</span><span class="sxs-lookup"><span data-stu-id="84ec8-119">Related resources</span></span>

### <a name="protocol-specifications"></a><span data-ttu-id="84ec8-120">Spécifications du protocole</span><span class="sxs-lookup"><span data-stu-id="84ec8-120">Protocol specifications</span></span>

<span data-ttu-id="84ec8-121">[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="84ec8-121">[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="84ec8-122">Fournit des références aux spécifications du protocole Exchange Server associées.</span><span class="sxs-lookup"><span data-stu-id="84ec8-122">Provides references to related Exchange Server protocol specifications.</span></span>
    
<span data-ttu-id="84ec8-123">[[MS-OXOMSG]](https://msdn.microsoft.com/library/daa9120f-f325-4afb-a738-28f91049ab3c%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="84ec8-123">[[MS-OXOMSG]](https://msdn.microsoft.com/library/daa9120f-f325-4afb-a738-28f91049ab3c%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="84ec8-124">Spécifie les propriétés et les opérations qui sont autorisées pour les objets de message électronique.</span><span class="sxs-lookup"><span data-stu-id="84ec8-124">Specifies the properties and operations that are permissible for email message objects.</span></span>
    
<span data-ttu-id="84ec8-125">[[MS-OXCFXICS]](https://msdn.microsoft.com/library/b9752f3d-d50d-44b8-9e6b-608a117c8532%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="84ec8-125">[[MS-OXCFXICS]](https://msdn.microsoft.com/library/b9752f3d-d50d-44b8-9e6b-608a117c8532%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="84ec8-126">Gère l’ordre et le flux pour les transferts de données entre un client et le serveur.</span><span class="sxs-lookup"><span data-stu-id="84ec8-126">Handles the order and flow for data transfers between a client and server.</span></span>
    
<span data-ttu-id="84ec8-127">[[MS-OXCICAL]](https://msdn.microsoft.com/library/a685a040-5b69-4c84-b084-795113fb4012%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="84ec8-127">[[MS-OXCICAL]](https://msdn.microsoft.com/library/a685a040-5b69-4c84-b084-795113fb4012%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="84ec8-128">La conversion entre IETF RFC2445, RFC2446, RFC2447 et rendez-vous et des objets de la conférence.</span><span class="sxs-lookup"><span data-stu-id="84ec8-128">Converts between IETF RFC2445, RFC2446, and RFC2447, and appointment and meeting objects.</span></span>
    
<span data-ttu-id="84ec8-129">[[MS-OXODLGT]](https://msdn.microsoft.com/library/01a89b11-9c43-4c40-b147-8f6a1ef5a44f%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="84ec8-129">[[MS-OXODLGT]](https://msdn.microsoft.com/library/01a89b11-9c43-4c40-b147-8f6a1ef5a44f%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="84ec8-130">Spécifie les méthodes pour la connexion et configurer des boîtes aux lettres en tant que les délégués et les interactions avec les objets de messagerie et de calendrier lorsqu’ils agissent au nom d’un autre utilisateur.</span><span class="sxs-lookup"><span data-stu-id="84ec8-130">Specifies methods for connecting to and configuring mailboxes as delegates, and interactions with message and calendar objects when they act on behalf of another user.</span></span>
    
<span data-ttu-id="84ec8-131">[[MS-OXTNEF]](https://msdn.microsoft.com/library/1f0544d7-30b7-4194-b58f-adc82f3763bb%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="84ec8-131">[[MS-OXTNEF]](https://msdn.microsoft.com/library/1f0544d7-30b7-4194-b58f-adc82f3763bb%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="84ec8-132">Code et décode des objets message et la pièce jointe à une représentation sous forme de flux efficace.</span><span class="sxs-lookup"><span data-stu-id="84ec8-132">Encodes and decodes message and attachment objects to an efficient stream representation.</span></span>
    
### <a name="header-files"></a><span data-ttu-id="84ec8-133">Fichiers d’en-tête</span><span class="sxs-lookup"><span data-stu-id="84ec8-133">Header files</span></span>

<span data-ttu-id="84ec8-134">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="84ec8-134">Mapidefs.h</span></span>
  
> <span data-ttu-id="84ec8-135">Fournit des définitions de type de données.</span><span class="sxs-lookup"><span data-stu-id="84ec8-135">Provides data type definitions.</span></span>
    
<span data-ttu-id="84ec8-136">MAPITAGS.h</span><span class="sxs-lookup"><span data-stu-id="84ec8-136">Mapitags.h</span></span>
  
> <span data-ttu-id="84ec8-137">Contient les définitions des propriétés répertoriées en tant que propriétés associées.</span><span class="sxs-lookup"><span data-stu-id="84ec8-137">Contains definitions of properties listed as associated properties.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="84ec8-138">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="84ec8-138">See also</span></span>



[<span data-ttu-id="84ec8-139">Propriété canonique PidTagSearchKey</span><span class="sxs-lookup"><span data-stu-id="84ec8-139">PidTagSearchKey Canonical Property</span></span>](pidtagsearchkey-canonical-property.md)


[<span data-ttu-id="84ec8-140">Propriétés MAPI</span><span class="sxs-lookup"><span data-stu-id="84ec8-140">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="84ec8-141">Propriétés canoniques MAPI</span><span class="sxs-lookup"><span data-stu-id="84ec8-141">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="84ec8-142">Mappage des noms de propriétés canoniques aux noms MAPI</span><span class="sxs-lookup"><span data-stu-id="84ec8-142">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="84ec8-143">Mappage des noms MAPI aux noms de propriétés canoniques</span><span class="sxs-lookup"><span data-stu-id="84ec8-143">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

