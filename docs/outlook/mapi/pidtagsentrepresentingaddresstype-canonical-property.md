---
title: Propriété canonique PidTagSentRepresentingAddressType
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- MAPI.PidTagSentRepresentingAddressType
api_type:
- COM
ms.assetid: 6ecbf653-1faf-47bd-81a4-20157859fdfd
description: Dernière modification le 09 mars 2015
ms.openlocfilehash: 86b4b4056c86baacc63ea88d00ba81195eef762a
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/23/2018
ms.locfileid: "22572276"
---
# <a name="pidtagsentrepresentingaddresstype-canonical-property"></a><span data-ttu-id="60e98-103">Propriété canonique PidTagSentRepresentingAddressType</span><span class="sxs-lookup"><span data-stu-id="60e98-103">PidTagSentRepresentingAddressType Canonical Property</span></span>

  
  
<span data-ttu-id="60e98-104">**S’applique à**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="60e98-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="60e98-105">Contient le type d’adresse de l’utilisateur de messagerie qui est représenté par l’expéditeur.</span><span class="sxs-lookup"><span data-stu-id="60e98-105">Contains the address type for the messaging user who is represented by the sender.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="60e98-106">Propriétés associées :</span><span class="sxs-lookup"><span data-stu-id="60e98-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="60e98-107">PR_SENT_REPRESENTING_ADDRTYPE, PR_SENT_REPRESENTING_ADDRTYPE_A, PR_SENT_REPRESENTING_ADDRTYPE_W</span><span class="sxs-lookup"><span data-stu-id="60e98-107">PR_SENT_REPRESENTING_ADDRTYPE, PR_SENT_REPRESENTING_ADDRTYPE_A, PR_SENT_REPRESENTING_ADDRTYPE_W</span></span>  <br/> |
|<span data-ttu-id="60e98-108">Identificateur :</span><span class="sxs-lookup"><span data-stu-id="60e98-108">Identifier:</span></span>  <br/> |<span data-ttu-id="60e98-109">0x0064</span><span class="sxs-lookup"><span data-stu-id="60e98-109">0x0064</span></span>  <br/> |
|<span data-ttu-id="60e98-110">Type de données :</span><span class="sxs-lookup"><span data-stu-id="60e98-110">Data type:</span></span>  <br/> |<span data-ttu-id="60e98-111">PT_UNICODE, PT_STRING8</span><span class="sxs-lookup"><span data-stu-id="60e98-111">PT_UNICODE, PT_STRING8</span></span>  <br/> |
|<span data-ttu-id="60e98-112">Domaine :</span><span class="sxs-lookup"><span data-stu-id="60e98-112">Area:</span></span>  <br/> |<span data-ttu-id="60e98-113">Address</span><span class="sxs-lookup"><span data-stu-id="60e98-113">Address</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="60e98-114">Remarques</span><span class="sxs-lookup"><span data-stu-id="60e98-114">Remarks</span></span>

<span data-ttu-id="60e98-115">Ces propriétés sont des exemples de propriétés d’adresse de l’utilisateur de messagerie est représenté par l’expéditeur.</span><span class="sxs-lookup"><span data-stu-id="60e98-115">These properties are examples of the address properties for the messaging user being represented by the sender.</span></span> <span data-ttu-id="60e98-116">Lorsqu’une application cliente envoie un message de la part d’un autre client, il doit définir toutes les propriétés de l’expéditeur représenté aux valeurs pour que le client.</span><span class="sxs-lookup"><span data-stu-id="60e98-116">When a client application sends a message on behalf of another client, it should set all the represented sender properties to the values for that client.</span></span> <span data-ttu-id="60e98-117">Un utilisateur de messagerie envoi généralement sur son propre compte conserve les propriétés de l’expéditeur représenté non définie.</span><span class="sxs-lookup"><span data-stu-id="60e98-117">A messaging user sending on its own behalf typically leaves the represented sender properties unset.</span></span>
  
<span data-ttu-id="60e98-118">Le fournisseur de transport sortant doit toujours laissez cette propriété inchangée si elle a été définie par le client d’envoi.</span><span class="sxs-lookup"><span data-stu-id="60e98-118">The outgoing transport provider must always leave this property unchanged if it has been set by the sending client.</span></span> <span data-ttu-id="60e98-119">Si elle n’est pas définie, le fournisseur de transport doit définir la propriété **PR_SENDER_ADDRTYPE** ([PidTagSenderAddressType](pidtagsenderaddresstype-canonical-property.md)) sur la copie du message sortante et laissez non définies sur la copie locale.</span><span class="sxs-lookup"><span data-stu-id="60e98-119">If it is unset, the transport provider should set it to the **PR_SENDER_ADDRTYPE** ([PidTagSenderAddressType](pidtagsenderaddresstype-canonical-property.md)) property on the outbound copy of the message, and leave it unset on the local copy.</span></span>
  
## <a name="related-resources"></a><span data-ttu-id="60e98-120">Ressources connexes</span><span class="sxs-lookup"><span data-stu-id="60e98-120">Related resources</span></span>

### <a name="protocol-specifications"></a><span data-ttu-id="60e98-121">Spécifications du protocole</span><span class="sxs-lookup"><span data-stu-id="60e98-121">Protocol specifications</span></span>

<span data-ttu-id="60e98-122">[[MS-OXPROPS]](http://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="60e98-122">[[MS-OXPROPS]](http://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="60e98-123">Fournit des références aux spécifications du protocole Exchange Server associées.</span><span class="sxs-lookup"><span data-stu-id="60e98-123">Provides references to related Exchange Server protocol specifications.</span></span>
    
<span data-ttu-id="60e98-124">[[MS-OXCFXICS]](http://msdn.microsoft.com/library/b9752f3d-d50d-44b8-9e6b-608a117c8532%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="60e98-124">[[MS-OXCFXICS]](http://msdn.microsoft.com/library/b9752f3d-d50d-44b8-9e6b-608a117c8532%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="60e98-125">Gère l’ordre et le flux pour les transferts de données entre un client et le serveur.</span><span class="sxs-lookup"><span data-stu-id="60e98-125">Handles the order and flow for data transfers between a client and server.</span></span>
    
<span data-ttu-id="60e98-126">[[MS-OXCICAL]](http://msdn.microsoft.com/library/a685a040-5b69-4c84-b084-795113fb4012%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="60e98-126">[[MS-OXCICAL]](http://msdn.microsoft.com/library/a685a040-5b69-4c84-b084-795113fb4012%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="60e98-127">La conversion entre IETF RFC2445, RFC2446, RFC2447 et rendez-vous et des objets de la conférence.</span><span class="sxs-lookup"><span data-stu-id="60e98-127">Converts between IETF RFC2445, RFC2446, and RFC2447, and appointment and meeting objects.</span></span>
    
<span data-ttu-id="60e98-128">[[MS-OXCMAIL]](http://msdn.microsoft.com/library/b60d48db-183f-4bf5-a908-f584e62cb2d4%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="60e98-128">[[MS-OXCMAIL]](http://msdn.microsoft.com/library/b60d48db-183f-4bf5-a908-f584e62cb2d4%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="60e98-129">Convertit des conventions de messagerie standard Internet aux objets de message.</span><span class="sxs-lookup"><span data-stu-id="60e98-129">Converts from Internet standard email conventions to message objects.</span></span>
    
<span data-ttu-id="60e98-130">[[MS-OXODLGT]](http://msdn.microsoft.com/library/01a89b11-9c43-4c40-b147-8f6a1ef5a44f%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="60e98-130">[[MS-OXODLGT]](http://msdn.microsoft.com/library/01a89b11-9c43-4c40-b147-8f6a1ef5a44f%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="60e98-131">Spécifie les méthodes pour la connexion et configurer des boîtes aux lettres en tant que les délégués et les interactions avec les objets de messagerie et de calendrier lorsqu’ils agissent au nom d’un autre utilisateur.</span><span class="sxs-lookup"><span data-stu-id="60e98-131">Specifies methods for connecting to and configuring mailboxes as delegates, and interactions with message and calendar objects when they act on behalf of another user.</span></span>
    
<span data-ttu-id="60e98-132">[[MS-OXOMSG]](http://msdn.microsoft.com/library/daa9120f-f325-4afb-a738-28f91049ab3c%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="60e98-132">[[MS-OXOMSG]](http://msdn.microsoft.com/library/daa9120f-f325-4afb-a738-28f91049ab3c%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="60e98-133">Spécifie les propriétés et les opérations qui sont autorisées pour les objets de message électronique.</span><span class="sxs-lookup"><span data-stu-id="60e98-133">Specifies the properties and operations that are permissible for email message objects.</span></span>
    
<span data-ttu-id="60e98-134">[[MS-OXOPOST]](http://msdn.microsoft.com/library/9b18fdab-aacd-4d73-9534-be9b6ba2f115%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="60e98-134">[[MS-OXOPOST]](http://msdn.microsoft.com/library/9b18fdab-aacd-4d73-9534-be9b6ba2f115%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="60e98-135">Spécifie les propriétés et les opérations qui sont autorisées pour publier des objets.</span><span class="sxs-lookup"><span data-stu-id="60e98-135">Specifies the properties and operations that are permissible for post objects.</span></span>
    
<span data-ttu-id="60e98-136">[[MS-OXOTASK]](http://msdn.microsoft.com/library/55600ec0-6195-4730-8436-59c7931ef27e%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="60e98-136">[[MS-OXOTASK]](http://msdn.microsoft.com/library/55600ec0-6195-4730-8436-59c7931ef27e%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="60e98-137">Spécifie les propriétés et les opérations qui sont autorisées pour les contacts et les listes de distribution personnelles.</span><span class="sxs-lookup"><span data-stu-id="60e98-137">Specifies the properties and operations that are permissible for contacts and personal distribution lists.</span></span>
    
<span data-ttu-id="60e98-138">[[MS-OXTNEF]](http://msdn.microsoft.com/library/1f0544d7-30b7-4194-b58f-adc82f3763bb%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="60e98-138">[[MS-OXTNEF]](http://msdn.microsoft.com/library/1f0544d7-30b7-4194-b58f-adc82f3763bb%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="60e98-139">Code et décode des objets message et la pièce jointe à une représentation sous forme de flux efficace.</span><span class="sxs-lookup"><span data-stu-id="60e98-139">Encodes and decodes message and attachment objects to an efficient stream representation.</span></span>
    
### <a name="header-files"></a><span data-ttu-id="60e98-140">Fichiers d’en-tête</span><span class="sxs-lookup"><span data-stu-id="60e98-140">Header files</span></span>

<span data-ttu-id="60e98-141">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="60e98-141">Mapidefs.h</span></span>
  
> <span data-ttu-id="60e98-142">Fournit des définitions de type de données.</span><span class="sxs-lookup"><span data-stu-id="60e98-142">Provides data type definitions.</span></span>
    
<span data-ttu-id="60e98-143">MAPITAGS.h</span><span class="sxs-lookup"><span data-stu-id="60e98-143">Mapitags.h</span></span>
  
> <span data-ttu-id="60e98-144">Contient les définitions des propriétés répertoriées en tant que propriétés associées.</span><span class="sxs-lookup"><span data-stu-id="60e98-144">Contains definitions of properties listed as associated properties.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="60e98-145">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="60e98-145">See also</span></span>



[<span data-ttu-id="60e98-146">Propriété canonique PidTagAddressType</span><span class="sxs-lookup"><span data-stu-id="60e98-146">PidTagAddressType Canonical Property</span></span>](pidtagaddresstype-canonical-property.md)


[<span data-ttu-id="60e98-147">Propriétés MAPI</span><span class="sxs-lookup"><span data-stu-id="60e98-147">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="60e98-148">Propriétés canoniques MAPI</span><span class="sxs-lookup"><span data-stu-id="60e98-148">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="60e98-149">Mappage des noms de propriétés canoniques aux noms MAPI</span><span class="sxs-lookup"><span data-stu-id="60e98-149">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="60e98-150">Mappage des noms MAPI aux noms de propriétés canoniques</span><span class="sxs-lookup"><span data-stu-id="60e98-150">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

