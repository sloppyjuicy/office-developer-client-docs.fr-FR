---
title: Propriété canonique PidTagSentRepresentingSmtpAddress
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: 5ed122a2-0967-4de3-a2ee-69f81ae77b16
description: Dernière modification le 9 mars 2015
ms.openlocfilehash: a9114b1c9c3f5b09c5636f7d55d7111dd86afc06
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32341936"
---
# <a name="pidtagsentrepresentingsmtpaddress-canonical-property"></a><span data-ttu-id="45388-103">Propriété canonique PidTagSentRepresentingSmtpAddress</span><span class="sxs-lookup"><span data-stu-id="45388-103">PidTagSentRepresentingSmtpAddress Canonical Property</span></span>

  
  
<span data-ttu-id="45388-104">**S’applique à** : Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="45388-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="45388-105">Contient l’adresse de messagerie SMTP (Simple Mail Transport Protocol) de l’utilisateur de messagerie représenté par l’expéditeur.</span><span class="sxs-lookup"><span data-stu-id="45388-105">Contains the Simple Mail Transport Protocol (SMTP) email address for the messaging user who is represented by the sender.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="45388-106">Propriétés associées :</span><span class="sxs-lookup"><span data-stu-id="45388-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="45388-107">PR_SENT_REPRESENTING_SMTP_ADDRESS, PR_SENT_REPRESENTING_SMTP_ADDRESS_A, PR_SENT_REPRESENTING_SMTP_ADDRESS_W</span><span class="sxs-lookup"><span data-stu-id="45388-107">PR_SENT_REPRESENTING_SMTP_ADDRESS, PR_SENT_REPRESENTING_SMTP_ADDRESS_A, PR_SENT_REPRESENTING_SMTP_ADDRESS_W</span></span>  <br/> |
|<span data-ttu-id="45388-108">Identificateur :</span><span class="sxs-lookup"><span data-stu-id="45388-108">Identifier:</span></span>  <br/> |<span data-ttu-id="45388-109">0x5D02</span><span class="sxs-lookup"><span data-stu-id="45388-109">0x5D02</span></span>  <br/> |
|<span data-ttu-id="45388-110">Type de données :</span><span class="sxs-lookup"><span data-stu-id="45388-110">Data type:</span></span>  <br/> |<span data-ttu-id="45388-111">PT_UNICODE, PT_STRING8</span><span class="sxs-lookup"><span data-stu-id="45388-111">PT_UNICODE, PT_STRING8</span></span>  <br/> |
|<span data-ttu-id="45388-112">Domaine :</span><span class="sxs-lookup"><span data-stu-id="45388-112">Area:</span></span>  <br/> |<span data-ttu-id="45388-113">Adresse</span><span class="sxs-lookup"><span data-stu-id="45388-113">Address</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="45388-114">Remarques</span><span class="sxs-lookup"><span data-stu-id="45388-114">Remarks</span></span>

<span data-ttu-id="45388-115">Cette propriété est un exemple des propriétés d’adresse de l’utilisateur de messagerie représenté par l’expéditeur.</span><span class="sxs-lookup"><span data-stu-id="45388-115">This property is an example of the address properties for the messaging user being represented by the sender.</span></span> <span data-ttu-id="45388-116">Lorsqu’une application cliente envoie un message pour le compte d’un autre client, elle doit définir toutes les propriétés d’expéditeur représentées sur les valeurs de ce client.</span><span class="sxs-lookup"><span data-stu-id="45388-116">When a client application sends a message on behalf of another client, it should set all the represented sender properties to the values for that client.</span></span> <span data-ttu-id="45388-117">Un utilisateur de messagerie envoyant en son propre nom laisse généralement les propriétés de l’expéditeur représenté non jeu.</span><span class="sxs-lookup"><span data-stu-id="45388-117">A messaging user sending on its own behalf typically leaves the represented sender properties unset.</span></span>
  
<span data-ttu-id="45388-118">Le fournisseur de transport sortant doit toujours laisser cette propriété inchangée si elle a été définie par le client d’envoi.</span><span class="sxs-lookup"><span data-stu-id="45388-118">The outgoing transport provider must always leave this property unchanged if it has been set by the sending client.</span></span> <span data-ttu-id="45388-119">Si elle n’est pas définie, le fournisseur de transport doit la définir sur la propriété **PR_SENDER_SMTP_ADDRESS** ([PidTagSenderSmtpAddress](pidtagsendersmtpaddress-canonical-property.md)) sur la copie sortante du message et la laisser non définie sur la copie locale.</span><span class="sxs-lookup"><span data-stu-id="45388-119">If it is unset, the transport provider should set it to the **PR_SENDER_SMTP_ADDRESS** ([PidTagSenderSmtpAddress](pidtagsendersmtpaddress-canonical-property.md)) property on the outbound copy of the message, and leave it unset on the local copy.</span></span>
  
## <a name="related-resources"></a><span data-ttu-id="45388-120">Ressources connexes</span><span class="sxs-lookup"><span data-stu-id="45388-120">Related resources</span></span>

### <a name="protocol-specifications"></a><span data-ttu-id="45388-121">Spécifications de protocole</span><span class="sxs-lookup"><span data-stu-id="45388-121">Protocol specifications</span></span>

<span data-ttu-id="45388-122">[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="45388-122">[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="45388-123">Fournit des références aux spécifications Exchange Server protocole.</span><span class="sxs-lookup"><span data-stu-id="45388-123">Provides references to related Exchange Server protocol specifications.</span></span>
    
<span data-ttu-id="45388-124">[[MS-OXOMSG]](https://msdn.microsoft.com/library/daa9120f-f325-4afb-a738-28f91049ab3c%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="45388-124">[[MS-OXOMSG]](https://msdn.microsoft.com/library/daa9120f-f325-4afb-a738-28f91049ab3c%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="45388-125">Spécifie les propriétés et opérations autorisées pour les objets de message électronique.</span><span class="sxs-lookup"><span data-stu-id="45388-125">Specifies the properties and operations that are permissible for email message objects.</span></span>
    
<span data-ttu-id="45388-126">[[MS-OXCFXICS]](https://msdn.microsoft.com/library/b9752f3d-d50d-44b8-9e6b-608a117c8532%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="45388-126">[[MS-OXCFXICS]](https://msdn.microsoft.com/library/b9752f3d-d50d-44b8-9e6b-608a117c8532%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="45388-127">Gère l’ordre et le flux des transferts de données entre un client et un serveur.</span><span class="sxs-lookup"><span data-stu-id="45388-127">Handles the order and flow for data transfers between a client and server.</span></span>
    
<span data-ttu-id="45388-128">[[MS-OXODLGT]](https://msdn.microsoft.com/library/01a89b11-9c43-4c40-b147-8f6a1ef5a44f%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="45388-128">[[MS-OXODLGT]](https://msdn.microsoft.com/library/01a89b11-9c43-4c40-b147-8f6a1ef5a44f%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="45388-129">Spécifie les méthodes de connexion et de configuration des boîtes aux lettres en tant que délégués, ainsi que les interactions avec les objets de message et de calendrier lorsqu’ils agissent pour le compte d’un autre utilisateur.</span><span class="sxs-lookup"><span data-stu-id="45388-129">Specifies methods for connecting to and configuring mailboxes as delegates, and interactions with message and calendar objects when they act on behalf of another user.</span></span>
    
<span data-ttu-id="45388-130">[[MS-OXCICAL]](https://msdn.microsoft.com/library/a685a040-5b69-4c84-b084-795113fb4012%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="45388-130">[[MS-OXCICAL]](https://msdn.microsoft.com/library/a685a040-5b69-4c84-b084-795113fb4012%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="45388-131">Convertit les objets RFC2445, RFC2446 et RFC2447 de l’IETF, ainsi que les objets de rendez-vous et de réunion.</span><span class="sxs-lookup"><span data-stu-id="45388-131">Converts between IETF RFC2445, RFC2446, and RFC2447, and appointment and meeting objects.</span></span>
    
<span data-ttu-id="45388-132">[[MS-OXCMAIL]](https://msdn.microsoft.com/library/b60d48db-183f-4bf5-a908-f584e62cb2d4%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="45388-132">[[MS-OXCMAIL]](https://msdn.microsoft.com/library/b60d48db-183f-4bf5-a908-f584e62cb2d4%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="45388-133">Convertit des conventions de messagerie standard Internet en objets de message.</span><span class="sxs-lookup"><span data-stu-id="45388-133">Converts from Internet standard email conventions to message objects.</span></span>
    
<span data-ttu-id="45388-134">[[MS-OXOTASK]](https://msdn.microsoft.com/library/55600ec0-6195-4730-8436-59c7931ef27e%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="45388-134">[[MS-OXOTASK]](https://msdn.microsoft.com/library/55600ec0-6195-4730-8436-59c7931ef27e%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="45388-135">Spécifie les propriétés et opérations autorisées pour les contacts et les listes de distribution personnelles.</span><span class="sxs-lookup"><span data-stu-id="45388-135">Specifies the properties and operations that are permissible for contacts and personal distribution lists.</span></span>
    
<span data-ttu-id="45388-136">[[MS-OXTNEF]](https://msdn.microsoft.com/library/1f0544d7-30b7-4194-b58f-adc82f3763bb%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="45388-136">[[MS-OXTNEF]](https://msdn.microsoft.com/library/1f0544d7-30b7-4194-b58f-adc82f3763bb%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="45388-137">Encode et décode les objets de message et de pièce jointe dans une représentation de flux efficace.</span><span class="sxs-lookup"><span data-stu-id="45388-137">Encodes and decodes message and attachment objects to an efficient stream representation.</span></span>
    
### <a name="header-files"></a><span data-ttu-id="45388-138">Fichiers d’en-tête</span><span class="sxs-lookup"><span data-stu-id="45388-138">Header files</span></span>

<span data-ttu-id="45388-139">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="45388-139">Mapidefs.h</span></span>
  
> <span data-ttu-id="45388-140">Fournit des définitions de type de données.</span><span class="sxs-lookup"><span data-stu-id="45388-140">Provides data type definitions.</span></span>
    
<span data-ttu-id="45388-141">Mapitags.h</span><span class="sxs-lookup"><span data-stu-id="45388-141">Mapitags.h</span></span>
  
> <span data-ttu-id="45388-142">Contient les définitions des propriétés répertoriées en tant que propriétés associées.</span><span class="sxs-lookup"><span data-stu-id="45388-142">Contains definitions of properties listed as associated properties.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="45388-143">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="45388-143">See also</span></span>



[<span data-ttu-id="45388-144">Propriétés MAPI</span><span class="sxs-lookup"><span data-stu-id="45388-144">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="45388-145">Propriétés canoniques MAPI</span><span class="sxs-lookup"><span data-stu-id="45388-145">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="45388-146">Mappage des noms de propriétés canoniques aux noms MAPI</span><span class="sxs-lookup"><span data-stu-id="45388-146">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="45388-147">Mappage des noms MAPI aux noms de propriétés canoniques</span><span class="sxs-lookup"><span data-stu-id="45388-147">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

