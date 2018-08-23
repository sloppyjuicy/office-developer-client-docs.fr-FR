---
title: Propriété canonique PidTagSentRepresentingSmtpAddress
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: 5ed122a2-0967-4de3-a2ee-69f81ae77b16
description: Dernière modification le 09 mars 2015
ms.openlocfilehash: afb50c2aaffd507cb269b80f1fb59f548685f2cc
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/23/2018
ms.locfileid: "22564919"
---
# <a name="pidtagsentrepresentingsmtpaddress-canonical-property"></a><span data-ttu-id="14c6d-103">Propriété canonique PidTagSentRepresentingSmtpAddress</span><span class="sxs-lookup"><span data-stu-id="14c6d-103">PidTagSentRepresentingSmtpAddress Canonical Property</span></span>

  
  
<span data-ttu-id="14c6d-104">**S’applique à**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="14c6d-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="14c6d-105">Contient l’adresse de messagerie Simple Mail Transport Protocol (SMTP) de l’utilisateur de messagerie qui est représenté par l’expéditeur.</span><span class="sxs-lookup"><span data-stu-id="14c6d-105">Contains the Simple Mail Transport Protocol (SMTP) email address for the messaging user who is represented by the sender.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="14c6d-106">Propriétés associées :</span><span class="sxs-lookup"><span data-stu-id="14c6d-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="14c6d-107">PR_SENT_REPRESENTING_SMTP_ADDRESS, PR_SENT_REPRESENTING_SMTP_ADDRESS_A, PR_SENT_REPRESENTING_SMTP_ADDRESS_W</span><span class="sxs-lookup"><span data-stu-id="14c6d-107">PR_SENT_REPRESENTING_SMTP_ADDRESS, PR_SENT_REPRESENTING_SMTP_ADDRESS_A, PR_SENT_REPRESENTING_SMTP_ADDRESS_W</span></span>  <br/> |
|<span data-ttu-id="14c6d-108">Identificateur :</span><span class="sxs-lookup"><span data-stu-id="14c6d-108">Identifier:</span></span>  <br/> |<span data-ttu-id="14c6d-109">0x5D02</span><span class="sxs-lookup"><span data-stu-id="14c6d-109">0x5D02</span></span>  <br/> |
|<span data-ttu-id="14c6d-110">Type de données :</span><span class="sxs-lookup"><span data-stu-id="14c6d-110">Data type:</span></span>  <br/> |<span data-ttu-id="14c6d-111">PT_UNICODE, PT_STRING8</span><span class="sxs-lookup"><span data-stu-id="14c6d-111">PT_UNICODE, PT_STRING8</span></span>  <br/> |
|<span data-ttu-id="14c6d-112">Domaine :</span><span class="sxs-lookup"><span data-stu-id="14c6d-112">Area:</span></span>  <br/> |<span data-ttu-id="14c6d-113">Address</span><span class="sxs-lookup"><span data-stu-id="14c6d-113">Address</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="14c6d-114">Remarques</span><span class="sxs-lookup"><span data-stu-id="14c6d-114">Remarks</span></span>

<span data-ttu-id="14c6d-115">Cette propriété est un exemple des propriétés d’adresse de l’utilisateur de messagerie est représenté par l’expéditeur.</span><span class="sxs-lookup"><span data-stu-id="14c6d-115">This property is an example of the address properties for the messaging user being represented by the sender.</span></span> <span data-ttu-id="14c6d-116">Lorsqu’une application cliente envoie un message de la part d’un autre client, il doit définir toutes les propriétés de l’expéditeur représenté aux valeurs pour que le client.</span><span class="sxs-lookup"><span data-stu-id="14c6d-116">When a client application sends a message on behalf of another client, it should set all the represented sender properties to the values for that client.</span></span> <span data-ttu-id="14c6d-117">Un utilisateur de messagerie envoi généralement sur son propre compte conserve les propriétés de l’expéditeur représenté non définie.</span><span class="sxs-lookup"><span data-stu-id="14c6d-117">A messaging user sending on its own behalf typically leaves the represented sender properties unset.</span></span>
  
<span data-ttu-id="14c6d-118">Le fournisseur de transport sortant doit toujours laissez cette propriété inchangée si elle a été définie par le client d’envoi.</span><span class="sxs-lookup"><span data-stu-id="14c6d-118">The outgoing transport provider must always leave this property unchanged if it has been set by the sending client.</span></span> <span data-ttu-id="14c6d-119">Si elle n’est pas définie, le fournisseur de transport doit définir la propriété **PR_SENDER_SMTP_ADDRESS** ([PidTagSenderSmtpAddress](pidtagsendersmtpaddress-canonical-property.md)) sur la copie du message sortante et laissez non définies sur la copie locale.</span><span class="sxs-lookup"><span data-stu-id="14c6d-119">If it is unset, the transport provider should set it to the **PR_SENDER_SMTP_ADDRESS** ([PidTagSenderSmtpAddress](pidtagsendersmtpaddress-canonical-property.md)) property on the outbound copy of the message, and leave it unset on the local copy.</span></span>
  
## <a name="related-resources"></a><span data-ttu-id="14c6d-120">Ressources connexes</span><span class="sxs-lookup"><span data-stu-id="14c6d-120">Related resources</span></span>

### <a name="protocol-specifications"></a><span data-ttu-id="14c6d-121">Spécifications du protocole</span><span class="sxs-lookup"><span data-stu-id="14c6d-121">Protocol specifications</span></span>

<span data-ttu-id="14c6d-122">[[MS-OXPROPS]](http://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="14c6d-122">[[MS-OXPROPS]](http://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="14c6d-123">Fournit des références aux spécifications du protocole Exchange Server associées.</span><span class="sxs-lookup"><span data-stu-id="14c6d-123">Provides references to related Exchange Server protocol specifications.</span></span>
    
<span data-ttu-id="14c6d-124">[[MS-OXOMSG]](http://msdn.microsoft.com/library/daa9120f-f325-4afb-a738-28f91049ab3c%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="14c6d-124">[[MS-OXOMSG]](http://msdn.microsoft.com/library/daa9120f-f325-4afb-a738-28f91049ab3c%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="14c6d-125">Spécifie les propriétés et les opérations qui sont autorisées pour les objets de message électronique.</span><span class="sxs-lookup"><span data-stu-id="14c6d-125">Specifies the properties and operations that are permissible for email message objects.</span></span>
    
<span data-ttu-id="14c6d-126">[[MS-OXCFXICS]](http://msdn.microsoft.com/library/b9752f3d-d50d-44b8-9e6b-608a117c8532%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="14c6d-126">[[MS-OXCFXICS]](http://msdn.microsoft.com/library/b9752f3d-d50d-44b8-9e6b-608a117c8532%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="14c6d-127">Gère l’ordre et le flux pour les transferts de données entre un client et le serveur.</span><span class="sxs-lookup"><span data-stu-id="14c6d-127">Handles the order and flow for data transfers between a client and server.</span></span>
    
<span data-ttu-id="14c6d-128">[[MS-OXODLGT]](http://msdn.microsoft.com/library/01a89b11-9c43-4c40-b147-8f6a1ef5a44f%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="14c6d-128">[[MS-OXODLGT]](http://msdn.microsoft.com/library/01a89b11-9c43-4c40-b147-8f6a1ef5a44f%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="14c6d-129">Spécifie les méthodes pour la connexion et configurer des boîtes aux lettres en tant que les délégués et les interactions avec les objets de messagerie et de calendrier lorsqu’ils agissent au nom d’un autre utilisateur.</span><span class="sxs-lookup"><span data-stu-id="14c6d-129">Specifies methods for connecting to and configuring mailboxes as delegates, and interactions with message and calendar objects when they act on behalf of another user.</span></span>
    
<span data-ttu-id="14c6d-130">[[MS-OXCICAL]](http://msdn.microsoft.com/library/a685a040-5b69-4c84-b084-795113fb4012%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="14c6d-130">[[MS-OXCICAL]](http://msdn.microsoft.com/library/a685a040-5b69-4c84-b084-795113fb4012%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="14c6d-131">La conversion entre IETF RFC2445, RFC2446, RFC2447 et rendez-vous et des objets de la conférence.</span><span class="sxs-lookup"><span data-stu-id="14c6d-131">Converts between IETF RFC2445, RFC2446, and RFC2447, and appointment and meeting objects.</span></span>
    
<span data-ttu-id="14c6d-132">[[MS-OXCMAIL]](http://msdn.microsoft.com/library/b60d48db-183f-4bf5-a908-f584e62cb2d4%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="14c6d-132">[[MS-OXCMAIL]](http://msdn.microsoft.com/library/b60d48db-183f-4bf5-a908-f584e62cb2d4%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="14c6d-133">Convertit des conventions de messagerie standard Internet aux objets de message.</span><span class="sxs-lookup"><span data-stu-id="14c6d-133">Converts from Internet standard email conventions to message objects.</span></span>
    
<span data-ttu-id="14c6d-134">[[MS-OXOTASK]](http://msdn.microsoft.com/library/55600ec0-6195-4730-8436-59c7931ef27e%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="14c6d-134">[[MS-OXOTASK]](http://msdn.microsoft.com/library/55600ec0-6195-4730-8436-59c7931ef27e%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="14c6d-135">Spécifie les propriétés et les opérations qui sont autorisées pour les contacts et les listes de distribution personnelles.</span><span class="sxs-lookup"><span data-stu-id="14c6d-135">Specifies the properties and operations that are permissible for contacts and personal distribution lists.</span></span>
    
<span data-ttu-id="14c6d-136">[[MS-OXTNEF]](http://msdn.microsoft.com/library/1f0544d7-30b7-4194-b58f-adc82f3763bb%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="14c6d-136">[[MS-OXTNEF]](http://msdn.microsoft.com/library/1f0544d7-30b7-4194-b58f-adc82f3763bb%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="14c6d-137">Code et décode des objets message et la pièce jointe à une représentation sous forme de flux efficace.</span><span class="sxs-lookup"><span data-stu-id="14c6d-137">Encodes and decodes message and attachment objects to an efficient stream representation.</span></span>
    
### <a name="header-files"></a><span data-ttu-id="14c6d-138">Fichiers d’en-tête</span><span class="sxs-lookup"><span data-stu-id="14c6d-138">Header files</span></span>

<span data-ttu-id="14c6d-139">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="14c6d-139">Mapidefs.h</span></span>
  
> <span data-ttu-id="14c6d-140">Fournit des définitions de type de données.</span><span class="sxs-lookup"><span data-stu-id="14c6d-140">Provides data type definitions.</span></span>
    
<span data-ttu-id="14c6d-141">MAPITAGS.h</span><span class="sxs-lookup"><span data-stu-id="14c6d-141">Mapitags.h</span></span>
  
> <span data-ttu-id="14c6d-142">Contient les définitions des propriétés répertoriées en tant que propriétés associées.</span><span class="sxs-lookup"><span data-stu-id="14c6d-142">Contains definitions of properties listed as associated properties.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="14c6d-143">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="14c6d-143">See also</span></span>



[<span data-ttu-id="14c6d-144">Propriétés MAPI</span><span class="sxs-lookup"><span data-stu-id="14c6d-144">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="14c6d-145">Propriétés canoniques MAPI</span><span class="sxs-lookup"><span data-stu-id="14c6d-145">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="14c6d-146">Mappage des noms de propriétés canoniques aux noms MAPI</span><span class="sxs-lookup"><span data-stu-id="14c6d-146">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="14c6d-147">Mappage des noms MAPI aux noms de propriétés canoniques</span><span class="sxs-lookup"><span data-stu-id="14c6d-147">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

