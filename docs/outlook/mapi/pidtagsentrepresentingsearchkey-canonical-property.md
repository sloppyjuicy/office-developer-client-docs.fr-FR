---
title: Propriété canonique PidTagSentRepresentingSearchKey
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- MAPI.PidTagSentRepresentingSearchKey
api_type:
- COM
ms.assetid: 7a49b944-cef1-4642-9208-b137fd61171a
description: Dernière modification le 09 mars 2015
ms.openlocfilehash: 954e63e5b669ffdd15bbc2548d75c4d420eaf88d
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/23/2018
ms.locfileid: "22591043"
---
# <a name="pidtagsentrepresentingsearchkey-canonical-property"></a><span data-ttu-id="d9818-103">Propriété canonique PidTagSentRepresentingSearchKey</span><span class="sxs-lookup"><span data-stu-id="d9818-103">PidTagSentRepresentingSearchKey Canonical Property</span></span>

  
  
<span data-ttu-id="d9818-104">**S’applique à**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="d9818-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="d9818-105">Contient la clé de recherche pour l’utilisateur de messagerie représenté par l’expéditeur.</span><span class="sxs-lookup"><span data-stu-id="d9818-105">Contains the search key for the messaging user represented by the sender.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="d9818-106">Propriétés associées :</span><span class="sxs-lookup"><span data-stu-id="d9818-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="d9818-107">PR_SENT_REPRESENTING_SEARCH_KEY</span><span class="sxs-lookup"><span data-stu-id="d9818-107">PR_SENT_REPRESENTING_SEARCH_KEY</span></span>  <br/> |
|<span data-ttu-id="d9818-108">Identificateur :</span><span class="sxs-lookup"><span data-stu-id="d9818-108">Identifier:</span></span>  <br/> |<span data-ttu-id="d9818-109">0x003B</span><span class="sxs-lookup"><span data-stu-id="d9818-109">0x003B</span></span>  <br/> |
|<span data-ttu-id="d9818-110">Type de données :</span><span class="sxs-lookup"><span data-stu-id="d9818-110">Data type:</span></span>  <br/> |<span data-ttu-id="d9818-111">PT_BINARY</span><span class="sxs-lookup"><span data-stu-id="d9818-111">PT_BINARY</span></span>  <br/> |
|<span data-ttu-id="d9818-112">Domaine :</span><span class="sxs-lookup"><span data-stu-id="d9818-112">Area:</span></span>  <br/> |<span data-ttu-id="d9818-113">Address</span><span class="sxs-lookup"><span data-stu-id="d9818-113">Address</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="d9818-114">Remarques</span><span class="sxs-lookup"><span data-stu-id="d9818-114">Remarks</span></span>

<span data-ttu-id="d9818-115">Cette propriété est une des propriétés d’adresse de l’utilisateur de messagerie qui est représenté par l’expéditeur.</span><span class="sxs-lookup"><span data-stu-id="d9818-115">This property is one of the address properties for the messaging user who is being represented by the sender.</span></span> <span data-ttu-id="d9818-116">Lorsqu’une application cliente envoie un message de la part d’un autre client, il doit définir toutes les propriétés de l’expéditeur représenté aux valeurs pour que le client.</span><span class="sxs-lookup"><span data-stu-id="d9818-116">When a client application sends a message on behalf of another client, it should set all the represented sender properties to the values for that client.</span></span> <span data-ttu-id="d9818-117">Un utilisateur de messagerie envoi généralement sur son propre compte conserve les propriétés de l’expéditeur représenté non définie.</span><span class="sxs-lookup"><span data-stu-id="d9818-117">A messaging user sending on its own behalf typically leaves the represented sender properties unset.</span></span>
  
<span data-ttu-id="d9818-118">Le fournisseur de transport sortant doit toujours laissez cette propriété inchangée si elle a été définie par le client d’envoi.</span><span class="sxs-lookup"><span data-stu-id="d9818-118">The outgoing transport provider must always leave this property unchanged if it has been set by the sending client.</span></span> <span data-ttu-id="d9818-119">Si elle n’est pas définie, le fournisseur de transport doit définir à **PR_SENDER_SEARCH_KEY** ([PidTagSenderSearchKey](pidtagsendersearchkey-canonical-property.md)) sur la copie du message sortante et laissez non définies sur la copie locale.</span><span class="sxs-lookup"><span data-stu-id="d9818-119">If it is unset, the transport provider should set it to **PR_SENDER_SEARCH_KEY** ([PidTagSenderSearchKey](pidtagsendersearchkey-canonical-property.md)) on the outbound copy of the message, and leave it unset on the local copy.</span></span>
  
## <a name="related-resources"></a><span data-ttu-id="d9818-120">Ressources connexes</span><span class="sxs-lookup"><span data-stu-id="d9818-120">Related resources</span></span>

### <a name="protocol-specifications"></a><span data-ttu-id="d9818-121">Spécifications du protocole</span><span class="sxs-lookup"><span data-stu-id="d9818-121">Protocol specifications</span></span>

<span data-ttu-id="d9818-122">[[MS-OXPROPS]](http://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="d9818-122">[[MS-OXPROPS]](http://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="d9818-123">Fournit des références aux spécifications du protocole Exchange Server associées.</span><span class="sxs-lookup"><span data-stu-id="d9818-123">Provides references to related Exchange Server protocol specifications.</span></span>
    
<span data-ttu-id="d9818-124">[[MS-OXOMSG]](http://msdn.microsoft.com/library/daa9120f-f325-4afb-a738-28f91049ab3c%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="d9818-124">[[MS-OXOMSG]](http://msdn.microsoft.com/library/daa9120f-f325-4afb-a738-28f91049ab3c%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="d9818-125">Spécifie les propriétés et les opérations qui sont autorisées pour les objets de message électronique.</span><span class="sxs-lookup"><span data-stu-id="d9818-125">Specifies the properties and operations that are permissible for email message objects.</span></span>
    
<span data-ttu-id="d9818-126">[[MS-OXCFXICS]](http://msdn.microsoft.com/library/b9752f3d-d50d-44b8-9e6b-608a117c8532%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="d9818-126">[[MS-OXCFXICS]](http://msdn.microsoft.com/library/b9752f3d-d50d-44b8-9e6b-608a117c8532%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="d9818-127">Gère l’ordre et le flux pour les transferts de données entre un client et le serveur.</span><span class="sxs-lookup"><span data-stu-id="d9818-127">Handles the order and flow for data transfers between a client and server.</span></span>
    
<span data-ttu-id="d9818-128">[[MS-OXCICAL]](http://msdn.microsoft.com/library/a685a040-5b69-4c84-b084-795113fb4012%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="d9818-128">[[MS-OXCICAL]](http://msdn.microsoft.com/library/a685a040-5b69-4c84-b084-795113fb4012%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="d9818-129">La conversion entre IETF RFC2445, RFC2446, RFC2447 et rendez-vous et des objets de la conférence.</span><span class="sxs-lookup"><span data-stu-id="d9818-129">Converts between IETF RFC2445, RFC2446, and RFC2447, and appointment and meeting objects.</span></span>
    
<span data-ttu-id="d9818-130">[[MS-OXOCAL]](http://msdn.microsoft.com/library/09861fde-c8e4-4028-9346-e7c214cfdba1%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="d9818-130">[[MS-OXOCAL]](http://msdn.microsoft.com/library/09861fde-c8e4-4028-9346-e7c214cfdba1%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="d9818-131">Spécifie les propriétés et opérations pour un rendez-vous, une demande de réunion et les messages de réponse.</span><span class="sxs-lookup"><span data-stu-id="d9818-131">Specifies the properties and operations for appointment, meeting request, and response messages.</span></span>
    
<span data-ttu-id="d9818-132">[[MS-OXOPOST]](http://msdn.microsoft.com/library/9b18fdab-aacd-4d73-9534-be9b6ba2f115%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="d9818-132">[[MS-OXOPOST]](http://msdn.microsoft.com/library/9b18fdab-aacd-4d73-9534-be9b6ba2f115%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="d9818-133">Spécifie les propriétés et les opérations qui sont autorisées pour publier des objets.</span><span class="sxs-lookup"><span data-stu-id="d9818-133">Specifies the properties and operations that are permissible for post objects.</span></span>
    
<span data-ttu-id="d9818-134">[[MS-OXOTASK]](http://msdn.microsoft.com/library/55600ec0-6195-4730-8436-59c7931ef27e%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="d9818-134">[[MS-OXOTASK]](http://msdn.microsoft.com/library/55600ec0-6195-4730-8436-59c7931ef27e%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="d9818-135">Spécifie les propriétés et les opérations qui sont autorisées pour les listes de distribution personnelles et de contact.</span><span class="sxs-lookup"><span data-stu-id="d9818-135">Specifies the properties and operations that are permissible for contact and personal distribution lists.</span></span>
    
### <a name="header-files"></a><span data-ttu-id="d9818-136">Fichiers d’en-tête</span><span class="sxs-lookup"><span data-stu-id="d9818-136">Header files</span></span>

<span data-ttu-id="d9818-137">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="d9818-137">Mapidefs.h</span></span>
  
> <span data-ttu-id="d9818-138">Fournit des définitions de type de données.</span><span class="sxs-lookup"><span data-stu-id="d9818-138">Provides data type definitions.</span></span>
    
<span data-ttu-id="d9818-139">MAPITAGS.h</span><span class="sxs-lookup"><span data-stu-id="d9818-139">Mapitags.h</span></span>
  
> <span data-ttu-id="d9818-140">Contient les définitions des propriétés répertoriées en tant que propriétés associées.</span><span class="sxs-lookup"><span data-stu-id="d9818-140">Contains definitions of properties listed as associated properties.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="d9818-141">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="d9818-141">See also</span></span>



[<span data-ttu-id="d9818-142">Propriétés MAPI</span><span class="sxs-lookup"><span data-stu-id="d9818-142">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="d9818-143">Propriétés canoniques MAPI</span><span class="sxs-lookup"><span data-stu-id="d9818-143">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="d9818-144">Mappage des noms de propriétés canoniques aux noms MAPI</span><span class="sxs-lookup"><span data-stu-id="d9818-144">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="d9818-145">Mappage des noms MAPI aux noms de propriétés canoniques</span><span class="sxs-lookup"><span data-stu-id="d9818-145">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

