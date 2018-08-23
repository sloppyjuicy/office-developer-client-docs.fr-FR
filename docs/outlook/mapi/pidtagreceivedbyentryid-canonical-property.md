---
title: Propriété canonique PidTagReceivedByEntryId
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- MAPI.PidTagReceivedByEntryId
api_type:
- COM
ms.assetid: 737f8584-fc52-4324-ac40-2fc554a3095d
description: Dernière modification le 09 mars 2015
ms.openlocfilehash: ab3ffed8dd5b8d73d8024d27790f18397d615c2c
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/23/2018
ms.locfileid: "22567467"
---
# <a name="pidtagreceivedbyentryid-canonical-property"></a><span data-ttu-id="98000-103">Propriété canonique PidTagReceivedByEntryId</span><span class="sxs-lookup"><span data-stu-id="98000-103">PidTagReceivedByEntryId Canonical Property</span></span>

  
  
<span data-ttu-id="98000-104">**S’applique à**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="98000-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="98000-105">Contient l’identificateur d’entrée de l’utilisateur de messagerie qui ne reçoive effectivement le message.</span><span class="sxs-lookup"><span data-stu-id="98000-105">Contains the entry identifier of the messaging user who actually receives the message.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="98000-106">Propriétés associées :</span><span class="sxs-lookup"><span data-stu-id="98000-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="98000-107">PR_RECEIVED_BY_ENTRYID</span><span class="sxs-lookup"><span data-stu-id="98000-107">PR_RECEIVED_BY_ENTRYID</span></span>  <br/> |
|<span data-ttu-id="98000-108">Identificateur :</span><span class="sxs-lookup"><span data-stu-id="98000-108">Identifier:</span></span>  <br/> |<span data-ttu-id="98000-109">0x003F</span><span class="sxs-lookup"><span data-stu-id="98000-109">0x003F</span></span>  <br/> |
|<span data-ttu-id="98000-110">Type de données :</span><span class="sxs-lookup"><span data-stu-id="98000-110">Data type:</span></span>  <br/> |<span data-ttu-id="98000-111">PT_BINARY</span><span class="sxs-lookup"><span data-stu-id="98000-111">PT_BINARY</span></span>  <br/> |
|<span data-ttu-id="98000-112">Domaine :</span><span class="sxs-lookup"><span data-stu-id="98000-112">Area:</span></span>  <br/> |<span data-ttu-id="98000-113">Carnet d’adresses</span><span class="sxs-lookup"><span data-stu-id="98000-113">Address book</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="98000-114">Remarques</span><span class="sxs-lookup"><span data-stu-id="98000-114">Remarks</span></span>

<span data-ttu-id="98000-115">Cette propriété est une des propriétés d’adresse de l’utilisateur de messagerie qui reçoit le message.</span><span class="sxs-lookup"><span data-stu-id="98000-115">This property is one of the address properties for the messaging user who receives the message.</span></span> <span data-ttu-id="98000-116">Elle doit être définie par le fournisseur de transport entrant.</span><span class="sxs-lookup"><span data-stu-id="98000-116">It must be set by the incoming transport provider.</span></span>
  
<span data-ttu-id="98000-117">Cette propriété correspond à un attribut X.400 remise enveloppe par message MH_T_.</span><span class="sxs-lookup"><span data-stu-id="98000-117">This property corresponds to an X.400 delivery envelope per-message MH_T_ attribute.</span></span>
  
## <a name="related-resources"></a><span data-ttu-id="98000-118">Ressources connexes</span><span class="sxs-lookup"><span data-stu-id="98000-118">Related resources</span></span>

### <a name="protocol-specifications"></a><span data-ttu-id="98000-119">Spécifications du protocole</span><span class="sxs-lookup"><span data-stu-id="98000-119">Protocol specifications</span></span>

<span data-ttu-id="98000-120">[[MS-OXPROPS]](http://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="98000-120">[[MS-OXPROPS]](http://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="98000-121">Fournit des références aux spécifications du protocole Exchange Server associées.</span><span class="sxs-lookup"><span data-stu-id="98000-121">Provides references to related Exchange Server protocol specifications.</span></span>
    
<span data-ttu-id="98000-122">[[MS-OXOMSG]](http://msdn.microsoft.com/library/daa9120f-f325-4afb-a738-28f91049ab3c%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="98000-122">[[MS-OXOMSG]](http://msdn.microsoft.com/library/daa9120f-f325-4afb-a738-28f91049ab3c%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="98000-123">Spécifie les propriétés et les opérations qui sont autorisées pour les objets de message électronique.</span><span class="sxs-lookup"><span data-stu-id="98000-123">Specifies the properties and operations that are permissible for email message objects.</span></span>
    
<span data-ttu-id="98000-124">[[MS-OXCFXICS]](http://msdn.microsoft.com/library/b9752f3d-d50d-44b8-9e6b-608a117c8532%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="98000-124">[[MS-OXCFXICS]](http://msdn.microsoft.com/library/b9752f3d-d50d-44b8-9e6b-608a117c8532%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="98000-125">Gère l’ordre et le flux pour les transferts de données entre un client et le serveur.</span><span class="sxs-lookup"><span data-stu-id="98000-125">Handles the order and flow for data transfers between a client and server.</span></span>
    
<span data-ttu-id="98000-126">[[MS-OXCICAL]](http://msdn.microsoft.com/library/a685a040-5b69-4c84-b084-795113fb4012%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="98000-126">[[MS-OXCICAL]](http://msdn.microsoft.com/library/a685a040-5b69-4c84-b084-795113fb4012%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="98000-127">La conversion entre IETF RFC2445, RFC2446, RFC2447 et rendez-vous et des éléments de réunion.</span><span class="sxs-lookup"><span data-stu-id="98000-127">Converts between IETF RFC2445, RFC2446, and RFC2447, and appointment and meeting items.</span></span>
    
<span data-ttu-id="98000-128">[[MS-OXODLGT]](http://msdn.microsoft.com/library/01a89b11-9c43-4c40-b147-8f6a1ef5a44f%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="98000-128">[[MS-OXODLGT]](http://msdn.microsoft.com/library/01a89b11-9c43-4c40-b147-8f6a1ef5a44f%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="98000-129">Spécifie les méthodes pour la connexion et configurer des boîtes aux lettres en tant que les délégués et les interactions avec les objets de messagerie et de calendrier lorsqu’ils agissent au nom d’un autre utilisateur.</span><span class="sxs-lookup"><span data-stu-id="98000-129">Specifies methods for connecting to and configuring mailboxes as delegates, and interactions with message and calendar objects when they act on behalf of another user.</span></span>
    
<span data-ttu-id="98000-130">[[MS-OXTNEF]](http://msdn.microsoft.com/library/1f0544d7-30b7-4194-b58f-adc82f3763bb%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="98000-130">[[MS-OXTNEF]](http://msdn.microsoft.com/library/1f0544d7-30b7-4194-b58f-adc82f3763bb%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="98000-131">Code et décode des objets message et la pièce jointe à une représentation sous forme de flux efficace.</span><span class="sxs-lookup"><span data-stu-id="98000-131">Encodes and decodes message and attachment objects to an efficient stream representation.</span></span>
    
### <a name="header-files"></a><span data-ttu-id="98000-132">Fichiers d’en-tête</span><span class="sxs-lookup"><span data-stu-id="98000-132">Header files</span></span>

<span data-ttu-id="98000-133">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="98000-133">Mapidefs.h</span></span>
  
> <span data-ttu-id="98000-134">Fournit des définitions de type de données.</span><span class="sxs-lookup"><span data-stu-id="98000-134">Provides data type definitions.</span></span>
    
<span data-ttu-id="98000-135">MAPITAGS.h</span><span class="sxs-lookup"><span data-stu-id="98000-135">Mapitags.h</span></span>
  
> <span data-ttu-id="98000-136">Contient les définitions des propriétés répertoriées en tant que propriétés associées.</span><span class="sxs-lookup"><span data-stu-id="98000-136">Contains definitions of properties listed as associated properties.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="98000-137">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="98000-137">See also</span></span>



[<span data-ttu-id="98000-138">Propriété canonique PidTagEntryId</span><span class="sxs-lookup"><span data-stu-id="98000-138">PidTagEntryId Canonical Property</span></span>](pidtagentryid-canonical-property.md)


[<span data-ttu-id="98000-139">Propriétés MAPI</span><span class="sxs-lookup"><span data-stu-id="98000-139">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="98000-140">Propriétés canoniques MAPI</span><span class="sxs-lookup"><span data-stu-id="98000-140">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="98000-141">Mappage des noms de propriétés canoniques aux noms MAPI</span><span class="sxs-lookup"><span data-stu-id="98000-141">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="98000-142">Mappage des noms MAPI aux noms de propriétés canoniques</span><span class="sxs-lookup"><span data-stu-id="98000-142">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

