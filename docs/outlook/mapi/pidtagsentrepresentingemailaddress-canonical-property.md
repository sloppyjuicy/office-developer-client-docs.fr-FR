---
title: Propriété canonique PidTagSentRepresentingEmailAddress
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- MAPI.PidTagSentRepresentingEmailAddress
api_type:
- COM
ms.assetid: 5fa4edde-475c-4568-946b-73eb08f97a61
description: 'Derni�re modification�: lundi 9 mars 2015'
ms.openlocfilehash: 1b82e1e96a5ffbb5c17dd919e78a9f07342194c5
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32341089"
---
# <a name="pidtagsentrepresentingemailaddress-canonical-property"></a><span data-ttu-id="5093e-103">Propriété canonique PidTagSentRepresentingEmailAddress</span><span class="sxs-lookup"><span data-stu-id="5093e-103">PidTagSentRepresentingEmailAddress Canonical Property</span></span>

  
  
<span data-ttu-id="5093e-104">**S’applique à** : Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="5093e-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="5093e-105">Contient l'adresse de messagerie de l'utilisateur de messagerie représenté par l'expéditeur.</span><span class="sxs-lookup"><span data-stu-id="5093e-105">Contains the email address for the messaging user who is represented by the sender.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="5093e-106">Propriétés associées :</span><span class="sxs-lookup"><span data-stu-id="5093e-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="5093e-107">PR_SENT_REPRESENTING_EMAIL_ADDRESS, PR_SENT_REPRESENTING_EMAIL_ADDRESS_A, PR_SENT_REPRESENTING_EMAIL_ADDRESS_W</span><span class="sxs-lookup"><span data-stu-id="5093e-107">PR_SENT_REPRESENTING_EMAIL_ADDRESS, PR_SENT_REPRESENTING_EMAIL_ADDRESS_A, PR_SENT_REPRESENTING_EMAIL_ADDRESS_W</span></span>  <br/> |
|<span data-ttu-id="5093e-108">Identificateur :</span><span class="sxs-lookup"><span data-stu-id="5093e-108">Identifier:</span></span>  <br/> |<span data-ttu-id="5093e-109">0x0065</span><span class="sxs-lookup"><span data-stu-id="5093e-109">0x0065</span></span>  <br/> |
|<span data-ttu-id="5093e-110">Type de données :</span><span class="sxs-lookup"><span data-stu-id="5093e-110">Data type:</span></span>  <br/> |<span data-ttu-id="5093e-111">PT_UNICODE, PT_STRING8</span><span class="sxs-lookup"><span data-stu-id="5093e-111">PT_UNICODE, PT_STRING8</span></span>  <br/> |
|<span data-ttu-id="5093e-112">Domaine :</span><span class="sxs-lookup"><span data-stu-id="5093e-112">Area:</span></span>  <br/> |<span data-ttu-id="5093e-113">Address</span><span class="sxs-lookup"><span data-stu-id="5093e-113">Address</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="5093e-114">Remarques</span><span class="sxs-lookup"><span data-stu-id="5093e-114">Remarks</span></span>

<span data-ttu-id="5093e-115">Ces propriétés sont des exemples de propriétés d'adresse pour l'utilisateur de messagerie représenté par l'expéditeur.</span><span class="sxs-lookup"><span data-stu-id="5093e-115">These properties are examples of the address properties for the messaging user being represented by the sender.</span></span> <span data-ttu-id="5093e-116">Lorsqu'une application cliente envoie un message au nom d'un autre client, il convient de définir toutes les propriétés d'expéditeur représentées sur les valeurs de ce client.</span><span class="sxs-lookup"><span data-stu-id="5093e-116">When a client application sends a message on behalf of another client, it should set all the represented sender properties to the values for that client.</span></span> <span data-ttu-id="5093e-117">Un utilisateur de messagerie qui envoie son propre nom laisse généralement les propriétés de l'expéditeur dédéfinies.</span><span class="sxs-lookup"><span data-stu-id="5093e-117">A messaging user sending on its own behalf typically leaves the represented sender properties unset.</span></span>
  
<span data-ttu-id="5093e-118">Le fournisseur de transport sortant doit toujours laisser ces propriétés inchangées si elle a été définie par le client expéditeur.</span><span class="sxs-lookup"><span data-stu-id="5093e-118">The outgoing transport provider must always leave these properties unchanged if it has been set by the sending client.</span></span> <span data-ttu-id="5093e-119">S'il n'est pas défini, le fournisseur de transport doit le définir sur la propriété **PR_SENDER_EMAIL_ADDRESS** ([PidTagSenderEmailAddress](pidtagsenderemailaddress-canonical-property.md)) sur la copie sortante du message et le laisser désactivé sur la copie locale.</span><span class="sxs-lookup"><span data-stu-id="5093e-119">If it is unset, the transport provider should set it to the **PR_SENDER_EMAIL_ADDRESS** ([PidTagSenderEmailAddress](pidtagsenderemailaddress-canonical-property.md)) property on the outbound copy of the message, and leave it unset on the local copy.</span></span>
  
## <a name="related-resources"></a><span data-ttu-id="5093e-120">Ressources associées</span><span class="sxs-lookup"><span data-stu-id="5093e-120">Related resources</span></span>

### <a name="protocol-specifications"></a><span data-ttu-id="5093e-121">Spécifications de protocole</span><span class="sxs-lookup"><span data-stu-id="5093e-121">Protocol specifications</span></span>

<span data-ttu-id="5093e-122">[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="5093e-122">[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="5093e-123">Fournit des références à des spécifications de protocole Exchange Server connexes.</span><span class="sxs-lookup"><span data-stu-id="5093e-123">Provides references to related Exchange Server protocol specifications.</span></span>
    
<span data-ttu-id="5093e-124">[[MS-OXOMSG]](https://msdn.microsoft.com/library/daa9120f-f325-4afb-a738-28f91049ab3c%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="5093e-124">[[MS-OXOMSG]](https://msdn.microsoft.com/library/daa9120f-f325-4afb-a738-28f91049ab3c%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="5093e-125">Spécifie les propriétés et les opérations qui sont autorisées pour les objets message électronique.</span><span class="sxs-lookup"><span data-stu-id="5093e-125">Specifies the properties and operations that are permissible for email message objects.</span></span>
    
<span data-ttu-id="5093e-126">[[MS-OXORSS]](https://msdn.microsoft.com/library/53bc9634-0040-4b5a-aecd-29781d826009%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="5093e-126">[[MS-OXORSS]](https://msdn.microsoft.com/library/53bc9634-0040-4b5a-aecd-29781d826009%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="5093e-127">Spécifie les propriétés et les opérations qui représentent des éléments RSS.</span><span class="sxs-lookup"><span data-stu-id="5093e-127">Specifies the properties and operations that represent RSS items.</span></span>
    
<span data-ttu-id="5093e-128">[[MS-OXCFXICS]](https://msdn.microsoft.com/library/b9752f3d-d50d-44b8-9e6b-608a117c8532%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="5093e-128">[[MS-OXCFXICS]](https://msdn.microsoft.com/library/b9752f3d-d50d-44b8-9e6b-608a117c8532%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="5093e-129">Gère l'ordre et le flux de transfert de données entre un client et un serveur.</span><span class="sxs-lookup"><span data-stu-id="5093e-129">Handles the order and flow for data transfers between a client and server.</span></span>
    
<span data-ttu-id="5093e-130">[[MS-OXCICAL]](https://msdn.microsoft.com/library/a685a040-5b69-4c84-b084-795113fb4012%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="5093e-130">[[MS-OXCICAL]](https://msdn.microsoft.com/library/a685a040-5b69-4c84-b084-795113fb4012%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="5093e-131">Effectue une conversion entre l'IETF RFC2445, RFC2446 et RFC2447, et les objets de rendez-vous et de réunion.</span><span class="sxs-lookup"><span data-stu-id="5093e-131">Converts between IETF RFC2445, RFC2446, and RFC2447, and appointment and meeting objects.</span></span>
    
<span data-ttu-id="5093e-132">[[MS-OXCMAIL]](https://msdn.microsoft.com/library/b60d48db-183f-4bf5-a908-f584e62cb2d4%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="5093e-132">[[MS-OXCMAIL]](https://msdn.microsoft.com/library/b60d48db-183f-4bf5-a908-f584e62cb2d4%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="5093e-133">ConVertit des conventions de messagerie standard Internet en objets message.</span><span class="sxs-lookup"><span data-stu-id="5093e-133">Converts from Internet standard email conventions to message objects.</span></span>
    
<span data-ttu-id="5093e-134">[[MS-OXOTASK]](https://msdn.microsoft.com/library/55600ec0-6195-4730-8436-59c7931ef27e%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="5093e-134">[[MS-OXOTASK]](https://msdn.microsoft.com/library/55600ec0-6195-4730-8436-59c7931ef27e%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="5093e-135">Spécifie les propriétés et les opérations qui sont autorisées pour les contacts et les listes de distribution personnelle.</span><span class="sxs-lookup"><span data-stu-id="5093e-135">Specifies the properties and operations that are permissible for contacts and personal distribution lists.</span></span>
    
<span data-ttu-id="5093e-136">[[MS-OXTNEF]](https://msdn.microsoft.com/library/1f0544d7-30b7-4194-b58f-adc82f3763bb%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="5093e-136">[[MS-OXTNEF]](https://msdn.microsoft.com/library/1f0544d7-30b7-4194-b58f-adc82f3763bb%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="5093e-137">Encode et décode les objets message et Attachment en une représentation de flux efficace.</span><span class="sxs-lookup"><span data-stu-id="5093e-137">Encodes and decodes message and attachment objects to an efficient stream representation.</span></span>
    
### <a name="header-files"></a><span data-ttu-id="5093e-138">Fichiers d'en-tête</span><span class="sxs-lookup"><span data-stu-id="5093e-138">Header files</span></span>

<span data-ttu-id="5093e-139">Mapidefs. h</span><span class="sxs-lookup"><span data-stu-id="5093e-139">Mapidefs.h</span></span>
  
> <span data-ttu-id="5093e-140">Fournit des définitions de type de données.</span><span class="sxs-lookup"><span data-stu-id="5093e-140">Provides data type definitions.</span></span>
    
<span data-ttu-id="5093e-141">Mapitags. h</span><span class="sxs-lookup"><span data-stu-id="5093e-141">Mapitags.h</span></span>
  
> <span data-ttu-id="5093e-142">Contient les définitions des propriétés indiquées en tant que propriétés associées.</span><span class="sxs-lookup"><span data-stu-id="5093e-142">Contains definitions of properties listed as associated properties.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="5093e-143">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="5093e-143">See also</span></span>



[<span data-ttu-id="5093e-144">Propriétés MAPI</span><span class="sxs-lookup"><span data-stu-id="5093e-144">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="5093e-145">Propriétés canoniques MAPI</span><span class="sxs-lookup"><span data-stu-id="5093e-145">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="5093e-146">Mappage des noms de propriétés canoniques aux noms MAPI</span><span class="sxs-lookup"><span data-stu-id="5093e-146">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="5093e-147">Mappage des noms MAPI aux noms de propriétés canoniques</span><span class="sxs-lookup"><span data-stu-id="5093e-147">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

