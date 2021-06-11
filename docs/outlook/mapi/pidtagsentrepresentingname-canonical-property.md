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
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32314930"
---
# <a name="pidtagsentrepresentingname-canonical-property"></a><span data-ttu-id="8eadd-103">Propriété canonique PidTagSentRepresentingName</span><span class="sxs-lookup"><span data-stu-id="8eadd-103">PidTagSentRepresentingName Canonical Property</span></span>

  
  
<span data-ttu-id="8eadd-104">**S’applique à** : Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="8eadd-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="8eadd-105">Contient le nom complet de l’utilisateur de messagerie représenté par l’expéditeur.</span><span class="sxs-lookup"><span data-stu-id="8eadd-105">Contains the display name for the messaging user represented by the sender.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="8eadd-106">Propriétés associées :</span><span class="sxs-lookup"><span data-stu-id="8eadd-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="8eadd-107">PR_SENT_REPRESENTING_NAME, PR_SENT_REPRESENTING_NAME_A, PR_SENT_REPRESENTING_NAME_W</span><span class="sxs-lookup"><span data-stu-id="8eadd-107">PR_SENT_REPRESENTING_NAME, PR_SENT_REPRESENTING_NAME_A, PR_SENT_REPRESENTING_NAME_W</span></span>  <br/> |
|<span data-ttu-id="8eadd-108">Identificateur :</span><span class="sxs-lookup"><span data-stu-id="8eadd-108">Identifier:</span></span>  <br/> |<span data-ttu-id="8eadd-109">0x0042</span><span class="sxs-lookup"><span data-stu-id="8eadd-109">0x0042</span></span>  <br/> |
|<span data-ttu-id="8eadd-110">Type de données :</span><span class="sxs-lookup"><span data-stu-id="8eadd-110">Data type:</span></span>  <br/> |<span data-ttu-id="8eadd-111">PT_UNICODE, PT_STRING8</span><span class="sxs-lookup"><span data-stu-id="8eadd-111">PT_UNICODE, PT_STRING8</span></span>  <br/> |
|<span data-ttu-id="8eadd-112">Domaine :</span><span class="sxs-lookup"><span data-stu-id="8eadd-112">Area:</span></span>  <br/> |<span data-ttu-id="8eadd-113">Adresse</span><span class="sxs-lookup"><span data-stu-id="8eadd-113">Address</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="8eadd-114">Remarques</span><span class="sxs-lookup"><span data-stu-id="8eadd-114">Remarks</span></span>

<span data-ttu-id="8eadd-115">Ces propriétés sont des exemples de propriétés d’adresse pour l’utilisateur de messagerie représenté par l’expéditeur.</span><span class="sxs-lookup"><span data-stu-id="8eadd-115">These properties are examples of the address properties for the messaging user being represented by the sender.</span></span> <span data-ttu-id="8eadd-116">Lorsqu’une application cliente envoie un message pour le compte d’un autre client, elle doit définir toutes les propriétés d’expéditeur représentées sur les valeurs de ce client.</span><span class="sxs-lookup"><span data-stu-id="8eadd-116">When a client application sends a message on behalf of another client, it should set all the represented sender properties to the values for that client.</span></span> <span data-ttu-id="8eadd-117">Un utilisateur de messagerie envoyant en son propre nom laisse généralement les propriétés de l’expéditeur représenté non jeu.</span><span class="sxs-lookup"><span data-stu-id="8eadd-117">A messaging user sending on its own behalf typically leaves the represented sender properties unset.</span></span>
  
<span data-ttu-id="8eadd-118">Le fournisseur de transport sortant doit toujours laisser cette propriété inchangée si elle a été définie par le client d’envoi.</span><span class="sxs-lookup"><span data-stu-id="8eadd-118">The outgoing transport provider must always leave this property unchanged if it has been set by the sending client.</span></span> <span data-ttu-id="8eadd-119">Si elle n’est pas définie, le fournisseur de transport doit la définir sur **PR_SENDER_NAME** ([PidTagSenderName](pidtagsendername-canonical-property.md)) sur la copie sortante du message et la laisser non définie sur la copie locale.</span><span class="sxs-lookup"><span data-stu-id="8eadd-119">If it is unset, the transport provider should set it to **PR_SENDER_NAME** ([PidTagSenderName](pidtagsendername-canonical-property.md)) on the outbound copy of the message, and leave it unset on the local copy.</span></span>
  
## <a name="related-resources"></a><span data-ttu-id="8eadd-120">Ressources connexes</span><span class="sxs-lookup"><span data-stu-id="8eadd-120">Related resources</span></span>

### <a name="protocol-specifications"></a><span data-ttu-id="8eadd-121">Spécifications de protocole</span><span class="sxs-lookup"><span data-stu-id="8eadd-121">Protocol specifications</span></span>

<span data-ttu-id="8eadd-122">[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="8eadd-122">[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="8eadd-123">Fournit des références aux spécifications Exchange Server protocole.</span><span class="sxs-lookup"><span data-stu-id="8eadd-123">Provides references to related Exchange Server protocol specifications.</span></span>
    
<span data-ttu-id="8eadd-124">[[MS-OXOMSG]](https://msdn.microsoft.com/library/cc433482%28EXCHG.80%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="8eadd-124">[[MS-OXOMSG]](https://msdn.microsoft.com/library/cc433482%28EXCHG.80%29.aspx)</span></span>
  
> <span data-ttu-id="8eadd-125">Spécifie les propriétés et opérations autorisées pour les objets de message électronique.</span><span class="sxs-lookup"><span data-stu-id="8eadd-125">Specifies the properties and operations that are permissible for email message objects.</span></span>
    
<span data-ttu-id="8eadd-126">[[MS-OXORSS]](https://msdn.microsoft.com/library/cc463884%28EXCHG.80%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="8eadd-126">[[MS-OXORSS]](https://msdn.microsoft.com/library/cc463884%28EXCHG.80%29.aspx)</span></span>
  
> <span data-ttu-id="8eadd-127">Spécifie les propriétés et les opérations qui représentent des éléments RSS.</span><span class="sxs-lookup"><span data-stu-id="8eadd-127">Specifies the properties and operations that represent RSS items.</span></span>
    
<span data-ttu-id="8eadd-128">[[MS-OXCFXICS]](https://msdn.microsoft.com/library/b9752f3d-d50d-44b8-9e6b-608a117c8532%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="8eadd-128">[[MS-OXCFXICS]](https://msdn.microsoft.com/library/b9752f3d-d50d-44b8-9e6b-608a117c8532%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="8eadd-129">Gère l’ordre et le flux des transferts de données entre un client et un serveur.</span><span class="sxs-lookup"><span data-stu-id="8eadd-129">Handles the order and flow for data transfers between a client and server.</span></span>
    
<span data-ttu-id="8eadd-130">[[MS-OXCICAL]](https://msdn.microsoft.com/library/a685a040-5b69-4c84-b084-795113fb4012%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="8eadd-130">[[MS-OXCICAL]](https://msdn.microsoft.com/library/a685a040-5b69-4c84-b084-795113fb4012%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="8eadd-131">Convertit les objets RFC2445, RFC2446 et RFC2447 de l’IETF, ainsi que les objets de rendez-vous et de réunion.</span><span class="sxs-lookup"><span data-stu-id="8eadd-131">Converts between IETF RFC2445, RFC2446, and RFC2447, and appointment and meeting objects.</span></span>
    
<span data-ttu-id="8eadd-132">[[MS-OXCMAIL]](https://msdn.microsoft.com/library/b60d48db-183f-4bf5-a908-f584e62cb2d4%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="8eadd-132">[[MS-OXCMAIL]](https://msdn.microsoft.com/library/b60d48db-183f-4bf5-a908-f584e62cb2d4%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="8eadd-133">Convertit des conventions de messagerie standard Internet en objets de message.</span><span class="sxs-lookup"><span data-stu-id="8eadd-133">Converts from Internet standard email conventions to message objects.</span></span>
    
<span data-ttu-id="8eadd-134">[[MS-OXOCAL]](https://msdn.microsoft.com/library/09861fde-c8e4-4028-9346-e7c214cfdba1%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="8eadd-134">[[MS-OXOCAL]](https://msdn.microsoft.com/library/09861fde-c8e4-4028-9346-e7c214cfdba1%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="8eadd-135">Spécifie les propriétés et les opérations pour les messages de rendez-vous, de demande de réunion et de réponse.</span><span class="sxs-lookup"><span data-stu-id="8eadd-135">Specifies the properties and operations for appointment, meeting request, and response messages.</span></span>
    
<span data-ttu-id="8eadd-136">[[MS-OXOCFG]](https://msdn.microsoft.com/library/7d466dd5-c156-4da9-9a01-75c78e7e1a67%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="8eadd-136">[[MS-OXOCFG]](https://msdn.microsoft.com/library/7d466dd5-c156-4da9-9a01-75c78e7e1a67%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="8eadd-137">Spécifie l’emplacement et les propriétés des données de configuration client et serveur, telles que les listes de catégories partagées et les heures de travail.</span><span class="sxs-lookup"><span data-stu-id="8eadd-137">Specifies the location and properties of client and server configuration data, such as shared category lists and working hours.</span></span>
    
<span data-ttu-id="8eadd-138">[[MS-OXODLGT]](https://msdn.microsoft.com/library/01a89b11-9c43-4c40-b147-8f6a1ef5a44f%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="8eadd-138">[[MS-OXODLGT]](https://msdn.microsoft.com/library/01a89b11-9c43-4c40-b147-8f6a1ef5a44f%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="8eadd-139">Spécifie les méthodes de connexion et de configuration des boîtes aux lettres en tant que délégués, ainsi que les interactions avec les objets de message et de calendrier lorsqu’ils agissent pour le compte d’un autre utilisateur.</span><span class="sxs-lookup"><span data-stu-id="8eadd-139">Specifies methods for connecting to and configuring mailboxes as delegates, and interactions with message and calendar objects when they act on behalf of another user.</span></span>
    
<span data-ttu-id="8eadd-140">[[MS-OXOPOST]](https://msdn.microsoft.com/library/9b18fdab-aacd-4d73-9534-be9b6ba2f115%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="8eadd-140">[[MS-OXOPOST]](https://msdn.microsoft.com/library/9b18fdab-aacd-4d73-9534-be9b6ba2f115%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="8eadd-141">Spécifie les propriétés et opérations autorisées pour les objets de publication.</span><span class="sxs-lookup"><span data-stu-id="8eadd-141">Specifies the properties and operations that are permissible for post objects.</span></span>
    
<span data-ttu-id="8eadd-142">[[MS-OXOTASK]](https://msdn.microsoft.com/library/55600ec0-6195-4730-8436-59c7931ef27e%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="8eadd-142">[[MS-OXOTASK]](https://msdn.microsoft.com/library/55600ec0-6195-4730-8436-59c7931ef27e%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="8eadd-143">Spécifie les propriétés et opérations autorisées pour les objets de liste de distribution personnelle et de contact.</span><span class="sxs-lookup"><span data-stu-id="8eadd-143">Specifies the properties and operations that are permissible for contact and personal distribution list objects.</span></span>
    
<span data-ttu-id="8eadd-144">[[MS-OXTNEF]](https://msdn.microsoft.com/library/1f0544d7-30b7-4194-b58f-adc82f3763bb%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="8eadd-144">[[MS-OXTNEF]](https://msdn.microsoft.com/library/1f0544d7-30b7-4194-b58f-adc82f3763bb%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="8eadd-145">Encode et décode les objets de message et de pièce jointe dans une représentation de flux efficace.</span><span class="sxs-lookup"><span data-stu-id="8eadd-145">Encodes and decodes message and attachment objects to an efficient stream representation.</span></span>
    
### <a name="header-files"></a><span data-ttu-id="8eadd-146">Fichiers d’en-tête</span><span class="sxs-lookup"><span data-stu-id="8eadd-146">Header files</span></span>

<span data-ttu-id="8eadd-147">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="8eadd-147">Mapidefs.h</span></span>
  
> <span data-ttu-id="8eadd-148">Fournit des définitions de type de données.</span><span class="sxs-lookup"><span data-stu-id="8eadd-148">Provides data type definitions.</span></span>
    
<span data-ttu-id="8eadd-149">Mapitags.h</span><span class="sxs-lookup"><span data-stu-id="8eadd-149">Mapitags.h</span></span>
  
> <span data-ttu-id="8eadd-150">Contient les définitions des propriétés répertoriées en tant que propriétés associées.</span><span class="sxs-lookup"><span data-stu-id="8eadd-150">Contains definitions of properties listed as associated properties.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="8eadd-151">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="8eadd-151">See also</span></span>



[<span data-ttu-id="8eadd-152">Propriété canonique PidTagDisplayName</span><span class="sxs-lookup"><span data-stu-id="8eadd-152">PidTagDisplayName Canonical Property</span></span>](pidtagdisplayname-canonical-property.md)


[<span data-ttu-id="8eadd-153">Propriétés MAPI</span><span class="sxs-lookup"><span data-stu-id="8eadd-153">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="8eadd-154">Propriétés canoniques MAPI</span><span class="sxs-lookup"><span data-stu-id="8eadd-154">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="8eadd-155">Mappage des noms de propriétés canoniques aux noms MAPI</span><span class="sxs-lookup"><span data-stu-id="8eadd-155">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="8eadd-156">Mappage des noms MAPI aux noms de propriétés canoniques</span><span class="sxs-lookup"><span data-stu-id="8eadd-156">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

