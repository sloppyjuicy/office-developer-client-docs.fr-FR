---
title: Propriété canonique PidTagSentRepresentingName
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_type:
- COM
ms.assetid: bfee6c5e-d4c6-442e-af71-23156569fed5
description: Dernière modification le 9 mars 2015
ms.openlocfilehash: 8e2df13f4e9c5d1d636c4f71ea6805ac031899e9
ms.sourcegitcommit: ef717c65d8dd41ababffb01eafc443c79950aed4
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 10/04/2018
ms.locfileid: "25383071"
---
# <a name="pidtagsentrepresentingname-canonical-property"></a><span data-ttu-id="83b9c-103">Propriété canonique PidTagSentRepresentingName</span><span class="sxs-lookup"><span data-stu-id="83b9c-103">PidTagSentRepresentingName Canonical Property</span></span>

  
  
<span data-ttu-id="83b9c-104">**S’applique à** : Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="83b9c-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="83b9c-105">Contient le nom complet de l’utilisateur de messagerie représenté par l’expéditeur.</span><span class="sxs-lookup"><span data-stu-id="83b9c-105">Contains the display name for the messaging user represented by the sender.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="83b9c-106">Propriétés associées :</span><span class="sxs-lookup"><span data-stu-id="83b9c-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="83b9c-107">PR_SENT_REPRESENTING_NAME, PR_SENT_REPRESENTING_NAME_A, PR_SENT_REPRESENTING_NAME_W</span><span class="sxs-lookup"><span data-stu-id="83b9c-107">PR_SENT_REPRESENTING_NAME, PR_SENT_REPRESENTING_NAME_A, PR_SENT_REPRESENTING_NAME_W</span></span>  <br/> |
|<span data-ttu-id="83b9c-108">Identificateur :</span><span class="sxs-lookup"><span data-stu-id="83b9c-108">Identifier:</span></span>  <br/> |<span data-ttu-id="83b9c-109">0x0042</span><span class="sxs-lookup"><span data-stu-id="83b9c-109">0x0042</span></span>  <br/> |
|<span data-ttu-id="83b9c-110">Type de données :</span><span class="sxs-lookup"><span data-stu-id="83b9c-110">Data type:</span></span>  <br/> |<span data-ttu-id="83b9c-111">PT_UNICODE, PT_STRING8</span><span class="sxs-lookup"><span data-stu-id="83b9c-111">PT_UNICODE, PT_STRING8</span></span>  <br/> |
|<span data-ttu-id="83b9c-112">Domaine :</span><span class="sxs-lookup"><span data-stu-id="83b9c-112">Area:</span></span>  <br/> |<span data-ttu-id="83b9c-113">Address</span><span class="sxs-lookup"><span data-stu-id="83b9c-113">Address</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="83b9c-114">Remarques</span><span class="sxs-lookup"><span data-stu-id="83b9c-114">Remarks</span></span>

<span data-ttu-id="83b9c-115">Ces propriétés sont des exemples de propriétés d’adresse de l’utilisateur de messagerie est représenté par l’expéditeur.</span><span class="sxs-lookup"><span data-stu-id="83b9c-115">These properties are examples of the address properties for the messaging user being represented by the sender.</span></span> <span data-ttu-id="83b9c-116">Lorsqu’une application cliente envoie un message de la part d’un autre client, il doit définir toutes les propriétés de l’expéditeur représenté aux valeurs pour que le client.</span><span class="sxs-lookup"><span data-stu-id="83b9c-116">When a client application sends a message on behalf of another client, it should set all the represented sender properties to the values for that client.</span></span> <span data-ttu-id="83b9c-117">Un utilisateur de messagerie envoi généralement sur son propre compte conserve les propriétés de l’expéditeur représenté non définie.</span><span class="sxs-lookup"><span data-stu-id="83b9c-117">A messaging user sending on its own behalf typically leaves the represented sender properties unset.</span></span>
  
<span data-ttu-id="83b9c-118">Le fournisseur de transport sortant doit toujours laissez cette propriété inchangée si elle a été définie par le client d’envoi.</span><span class="sxs-lookup"><span data-stu-id="83b9c-118">The outgoing transport provider must always leave this property unchanged if it has been set by the sending client.</span></span> <span data-ttu-id="83b9c-119">Si elle n’est pas définie, le fournisseur de transport doit définir à **PR_SENDER_NAME** ([PidTagSenderName](pidtagsendername-canonical-property.md)) sur la copie du message sortante et laissez non définies sur la copie locale.</span><span class="sxs-lookup"><span data-stu-id="83b9c-119">If it is unset, the transport provider should set it to **PR_SENDER_NAME** ([PidTagSenderName](pidtagsendername-canonical-property.md)) on the outbound copy of the message, and leave it unset on the local copy.</span></span>
  
## <a name="related-resources"></a><span data-ttu-id="83b9c-120">Ressources connexes</span><span class="sxs-lookup"><span data-stu-id="83b9c-120">Related resources</span></span>

### <a name="protocol-specifications"></a><span data-ttu-id="83b9c-121">Spécifications du protocole</span><span class="sxs-lookup"><span data-stu-id="83b9c-121">Protocol specifications</span></span>

<span data-ttu-id="83b9c-122">[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="83b9c-122">[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="83b9c-123">Fournit des références aux spécifications du protocole Exchange Server associées.</span><span class="sxs-lookup"><span data-stu-id="83b9c-123">Provides references to related Exchange Server protocol specifications.</span></span>
    
<span data-ttu-id="83b9c-124">[[MS-OXOMSG]](https://msdn.microsoft.com/library/cc433482%28EXCHG.80%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="83b9c-124">[[MS-OXOMSG]](https://msdn.microsoft.com/library/cc433482%28EXCHG.80%29.aspx)</span></span>
  
> <span data-ttu-id="83b9c-125">Spécifie les propriétés et les opérations qui sont autorisées pour les objets de message électronique.</span><span class="sxs-lookup"><span data-stu-id="83b9c-125">Specifies the properties and operations that are permissible for email message objects.</span></span>
    
<span data-ttu-id="83b9c-126">[[MS-OXORSS]](https://msdn.microsoft.com/library/cc463884%28EXCHG.80%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="83b9c-126">[[MS-OXORSS]](https://msdn.microsoft.com/library/cc463884%28EXCHG.80%29.aspx)</span></span>
  
> <span data-ttu-id="83b9c-127">Spécifie les propriétés et les opérations qui représentent les éléments RSS.</span><span class="sxs-lookup"><span data-stu-id="83b9c-127">Specifies the properties and operations that represent RSS items.</span></span>
    
<span data-ttu-id="83b9c-128">[[MS-OXCFXICS]](https://msdn.microsoft.com/library/b9752f3d-d50d-44b8-9e6b-608a117c8532%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="83b9c-128">[[MS-OXCFXICS]](https://msdn.microsoft.com/library/b9752f3d-d50d-44b8-9e6b-608a117c8532%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="83b9c-129">Gère l’ordre et le flux pour les transferts de données entre un client et le serveur.</span><span class="sxs-lookup"><span data-stu-id="83b9c-129">Handles the order and flow for data transfers between a client and server.</span></span>
    
<span data-ttu-id="83b9c-130">[[MS-OXCICAL]](https://msdn.microsoft.com/library/a685a040-5b69-4c84-b084-795113fb4012%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="83b9c-130">[[MS-OXCICAL]](https://msdn.microsoft.com/library/a685a040-5b69-4c84-b084-795113fb4012%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="83b9c-131">La conversion entre IETF RFC2445, RFC2446, RFC2447 et rendez-vous et des objets de la conférence.</span><span class="sxs-lookup"><span data-stu-id="83b9c-131">Converts between IETF RFC2445, RFC2446, and RFC2447, and appointment and meeting objects.</span></span>
    
<span data-ttu-id="83b9c-132">[[MS-OXCMAIL]](https://msdn.microsoft.com/library/b60d48db-183f-4bf5-a908-f584e62cb2d4%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="83b9c-132">[[MS-OXCMAIL]](https://msdn.microsoft.com/library/b60d48db-183f-4bf5-a908-f584e62cb2d4%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="83b9c-133">Convertit des conventions de messagerie standard Internet aux objets de message.</span><span class="sxs-lookup"><span data-stu-id="83b9c-133">Converts from Internet standard email conventions to message objects.</span></span>
    
<span data-ttu-id="83b9c-134">[[MS-OXOCAL]](https://msdn.microsoft.com/library/09861fde-c8e4-4028-9346-e7c214cfdba1%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="83b9c-134">[[MS-OXOCAL]](https://msdn.microsoft.com/library/09861fde-c8e4-4028-9346-e7c214cfdba1%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="83b9c-135">Spécifie les propriétés et opérations pour un rendez-vous, une demande de réunion et les messages de réponse.</span><span class="sxs-lookup"><span data-stu-id="83b9c-135">Specifies the properties and operations for appointment, meeting request, and response messages.</span></span>
    
<span data-ttu-id="83b9c-136">[[MS-OXOCFG]](https://msdn.microsoft.com/library/7d466dd5-c156-4da9-9a01-75c78e7e1a67%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="83b9c-136">[[MS-OXOCFG]](https://msdn.microsoft.com/library/7d466dd5-c156-4da9-9a01-75c78e7e1a67%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="83b9c-137">Spécifie l’emplacement et les propriétés des données de configuration client et serveur, telles que des listes de catégorie partagée et les heures de travail.</span><span class="sxs-lookup"><span data-stu-id="83b9c-137">Specifies the location and properties of client and server configuration data, such as shared category lists and working hours.</span></span>
    
<span data-ttu-id="83b9c-138">[[MS-OXODLGT]](https://msdn.microsoft.com/library/01a89b11-9c43-4c40-b147-8f6a1ef5a44f%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="83b9c-138">[[MS-OXODLGT]](https://msdn.microsoft.com/library/01a89b11-9c43-4c40-b147-8f6a1ef5a44f%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="83b9c-139">Spécifie les méthodes pour la connexion et configurer des boîtes aux lettres en tant que les délégués et les interactions avec les objets de messagerie et de calendrier lorsqu’ils agissent au nom d’un autre utilisateur.</span><span class="sxs-lookup"><span data-stu-id="83b9c-139">Specifies methods for connecting to and configuring mailboxes as delegates, and interactions with message and calendar objects when they act on behalf of another user.</span></span>
    
<span data-ttu-id="83b9c-140">[[MS-OXOPOST]](https://msdn.microsoft.com/library/9b18fdab-aacd-4d73-9534-be9b6ba2f115%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="83b9c-140">[[MS-OXOPOST]](https://msdn.microsoft.com/library/9b18fdab-aacd-4d73-9534-be9b6ba2f115%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="83b9c-141">Spécifie les propriétés et les opérations qui sont autorisées pour publier des objets.</span><span class="sxs-lookup"><span data-stu-id="83b9c-141">Specifies the properties and operations that are permissible for post objects.</span></span>
    
<span data-ttu-id="83b9c-142">[[MS-OXOTASK]](https://msdn.microsoft.com/library/55600ec0-6195-4730-8436-59c7931ef27e%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="83b9c-142">[[MS-OXOTASK]](https://msdn.microsoft.com/library/55600ec0-6195-4730-8436-59c7931ef27e%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="83b9c-143">Spécifie les propriétés et les opérations qui sont autorisées pour les contacts et les objets de liste de distribution personnelle.</span><span class="sxs-lookup"><span data-stu-id="83b9c-143">Specifies the properties and operations that are permissible for contact and personal distribution list objects.</span></span>
    
<span data-ttu-id="83b9c-144">[[MS-OXTNEF]](https://msdn.microsoft.com/library/1f0544d7-30b7-4194-b58f-adc82f3763bb%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="83b9c-144">[[MS-OXTNEF]](https://msdn.microsoft.com/library/1f0544d7-30b7-4194-b58f-adc82f3763bb%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="83b9c-145">Code et décode des objets message et la pièce jointe à une représentation sous forme de flux efficace.</span><span class="sxs-lookup"><span data-stu-id="83b9c-145">Encodes and decodes message and attachment objects to an efficient stream representation.</span></span>
    
### <a name="header-files"></a><span data-ttu-id="83b9c-146">Fichiers d’en-tête</span><span class="sxs-lookup"><span data-stu-id="83b9c-146">Header files</span></span>

<span data-ttu-id="83b9c-147">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="83b9c-147">Mapidefs.h</span></span>
  
> <span data-ttu-id="83b9c-148">Fournit des définitions de type de données.</span><span class="sxs-lookup"><span data-stu-id="83b9c-148">Provides data type definitions.</span></span>
    
<span data-ttu-id="83b9c-149">MAPITAGS.h</span><span class="sxs-lookup"><span data-stu-id="83b9c-149">Mapitags.h</span></span>
  
> <span data-ttu-id="83b9c-150">Contient les définitions des propriétés répertoriées en tant que propriétés associées.</span><span class="sxs-lookup"><span data-stu-id="83b9c-150">Contains definitions of properties listed as associated properties.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="83b9c-151">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="83b9c-151">See also</span></span>



[<span data-ttu-id="83b9c-152">Propriété canonique PidTagDisplayName</span><span class="sxs-lookup"><span data-stu-id="83b9c-152">PidTagDisplayName Canonical Property</span></span>](pidtagdisplayname-canonical-property.md)


[<span data-ttu-id="83b9c-153">Propriétés MAPI</span><span class="sxs-lookup"><span data-stu-id="83b9c-153">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="83b9c-154">Propriétés canoniques MAPI</span><span class="sxs-lookup"><span data-stu-id="83b9c-154">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="83b9c-155">Mappage des noms de propriétés canoniques aux noms MAPI</span><span class="sxs-lookup"><span data-stu-id="83b9c-155">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="83b9c-156">Mappage des noms MAPI aux noms de propriétés canoniques</span><span class="sxs-lookup"><span data-stu-id="83b9c-156">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

