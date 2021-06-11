---
title: Propriété canonique PidTagReceivedRepresentingEntryId
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- MAPI.PidTagReceivedRepresentingEntryId
api_type:
- COM
ms.assetid: 2ae2266c-f093-41e5-b4d0-e12aa0f03190
description: Dernière modification le 9 mars 2015
ms.openlocfilehash: 33e41343e0c159be20ed1499fc24223947975e1d
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32359093"
---
# <a name="pidtagreceivedrepresentingentryid-canonical-property"></a><span data-ttu-id="73389-103">Propriété canonique PidTagReceivedRepresentingEntryId</span><span class="sxs-lookup"><span data-stu-id="73389-103">PidTagReceivedRepresentingEntryId Canonical Property</span></span>

  
  
<span data-ttu-id="73389-104">**S’applique à** : Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="73389-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="73389-105">Contient l’identificateur d’entrée de l’utilisateur de messagerie représenté par l’utilisateur de réception.</span><span class="sxs-lookup"><span data-stu-id="73389-105">Contains the entry identifier for the messaging user who is represented by the receiving user.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="73389-106">Propriétés associées :</span><span class="sxs-lookup"><span data-stu-id="73389-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="73389-107">PR_RCVD_REPRESENTING_ENTRYID</span><span class="sxs-lookup"><span data-stu-id="73389-107">PR_RCVD_REPRESENTING_ENTRYID</span></span>  <br/> |
|<span data-ttu-id="73389-108">Identificateur :</span><span class="sxs-lookup"><span data-stu-id="73389-108">Identifier:</span></span>  <br/> |<span data-ttu-id="73389-109">0x0043</span><span class="sxs-lookup"><span data-stu-id="73389-109">0x0043</span></span>  <br/> |
|<span data-ttu-id="73389-110">Type de données :</span><span class="sxs-lookup"><span data-stu-id="73389-110">Data type:</span></span>  <br/> |<span data-ttu-id="73389-111">PT_BINARY</span><span class="sxs-lookup"><span data-stu-id="73389-111">PT_BINARY</span></span>  <br/> |
|<span data-ttu-id="73389-112">Domaine :</span><span class="sxs-lookup"><span data-stu-id="73389-112">Area:</span></span>  <br/> |<span data-ttu-id="73389-113">Adresse</span><span class="sxs-lookup"><span data-stu-id="73389-113">Address</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="73389-114">Remarques</span><span class="sxs-lookup"><span data-stu-id="73389-114">Remarks</span></span>

<span data-ttu-id="73389-115">Cette propriété est l’une des propriétés d’adresse de l’utilisateur de messagerie représenté par l’utilisateur de réception.</span><span class="sxs-lookup"><span data-stu-id="73389-115">This property is one of the address properties for the messaging user who is being represented by the receiving user.</span></span> <span data-ttu-id="73389-116">Elle doit être définie par le fournisseur de transport entrant, qui est également responsable de l’autorisation ou de la vérification du délégué.</span><span class="sxs-lookup"><span data-stu-id="73389-116">It must be set by the incoming transport provider, which is also responsible for authorization or verification of the delegate.</span></span> <span data-ttu-id="73389-117">Si aucun utilisateur de messagerie n’est représenté, cette propriété doit être définie sur l’identificateur d’entrée contenu dans la propriété **PR_RECEIVED_BY_ENTRYID** ([PidTagReceivedByEntryId](pidtagreceivedbyentryid-canonical-property.md)).</span><span class="sxs-lookup"><span data-stu-id="73389-117">If no messaging user is being represented, this property should be set to the entry identifier contained in the **PR_RECEIVED_BY_ENTRYID** ([PidTagReceivedByEntryId](pidtagreceivedbyentryid-canonical-property.md)) property.</span></span>
  
<span data-ttu-id="73389-118">Une application cliente répondant à un message reçu au nom d’un autre client doit copier cette propriété du message reçu dans la propriété **PR_SENT_REPRESENTING_ENTRYID** ([PidTagSentRepresentingEntryId](pidtagsentrepresentingentryid-canonical-property.md)) pour la réponse.</span><span class="sxs-lookup"><span data-stu-id="73389-118">A client application replying to a message received on behalf of another client should copy this property from the received message into the **PR_SENT_REPRESENTING_ENTRYID** ([PidTagSentRepresentingEntryId](pidtagsentrepresentingentryid-canonical-property.md)) property for the reply.</span></span>
  
## <a name="related-resources"></a><span data-ttu-id="73389-119">Ressources connexes</span><span class="sxs-lookup"><span data-stu-id="73389-119">Related resources</span></span>

### <a name="protocol-specifications"></a><span data-ttu-id="73389-120">Spécifications de protocole</span><span class="sxs-lookup"><span data-stu-id="73389-120">Protocol specifications</span></span>

<span data-ttu-id="73389-121">[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="73389-121">[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="73389-122">Fournit des références aux spécifications Exchange Server protocole.</span><span class="sxs-lookup"><span data-stu-id="73389-122">Provides references to related Exchange Server protocol specifications.</span></span>
    
<span data-ttu-id="73389-123">[[MS-OXOMSG]](https://msdn.microsoft.com/library/daa9120f-f325-4afb-a738-28f91049ab3c%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="73389-123">[[MS-OXOMSG]](https://msdn.microsoft.com/library/daa9120f-f325-4afb-a738-28f91049ab3c%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="73389-124">Spécifie les propriétés et opérations autorisées pour les objets de message électronique.</span><span class="sxs-lookup"><span data-stu-id="73389-124">Specifies the properties and operations that are permissible for email message objects.</span></span>
    
<span data-ttu-id="73389-125">[[MS-OXCFXICS]](https://msdn.microsoft.com/library/b9752f3d-d50d-44b8-9e6b-608a117c8532%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="73389-125">[[MS-OXCFXICS]](https://msdn.microsoft.com/library/b9752f3d-d50d-44b8-9e6b-608a117c8532%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="73389-126">Gère l’ordre et le flux des transferts de données entre un client et un serveur.</span><span class="sxs-lookup"><span data-stu-id="73389-126">Handles the order and flow for data transfers between a client and server.</span></span>
    
<span data-ttu-id="73389-127">[[MS-OXODLGT]](https://msdn.microsoft.com/library/01a89b11-9c43-4c40-b147-8f6a1ef5a44f%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="73389-127">[[MS-OXODLGT]](https://msdn.microsoft.com/library/01a89b11-9c43-4c40-b147-8f6a1ef5a44f%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="73389-128">Spécifie les méthodes de connexion et de configuration des boîtes aux lettres en tant que délégués, ainsi que les interactions avec les objets de message et de calendrier lorsqu’ils agissent pour le compte d’un autre utilisateur.</span><span class="sxs-lookup"><span data-stu-id="73389-128">Specifies methods for connecting to and configuring mailboxes as delegates, and interactions with message and calendar objects when they act on behalf of another user.</span></span>
    
### <a name="header-files"></a><span data-ttu-id="73389-129">Fichiers d’en-tête</span><span class="sxs-lookup"><span data-stu-id="73389-129">Header files</span></span>

<span data-ttu-id="73389-130">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="73389-130">Mapidefs.h</span></span>
  
> <span data-ttu-id="73389-131">Fournit des définitions de type de données.</span><span class="sxs-lookup"><span data-stu-id="73389-131">Provides data type definitions.</span></span>
    
<span data-ttu-id="73389-132">Mapitags.h</span><span class="sxs-lookup"><span data-stu-id="73389-132">Mapitags.h</span></span>
  
> <span data-ttu-id="73389-133">Contient les définitions des propriétés répertoriées en tant que propriétés associées.</span><span class="sxs-lookup"><span data-stu-id="73389-133">Contains definitions of properties listed as associated properties.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="73389-134">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="73389-134">See also</span></span>



[<span data-ttu-id="73389-135">Propriétés MAPI</span><span class="sxs-lookup"><span data-stu-id="73389-135">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="73389-136">Propriétés canoniques MAPI</span><span class="sxs-lookup"><span data-stu-id="73389-136">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="73389-137">Mappage des noms de propriétés canoniques aux noms MAPI</span><span class="sxs-lookup"><span data-stu-id="73389-137">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="73389-138">Mappage des noms MAPI aux noms de propriétés canoniques</span><span class="sxs-lookup"><span data-stu-id="73389-138">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

