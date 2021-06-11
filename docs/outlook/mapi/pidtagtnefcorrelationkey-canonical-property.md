---
title: Propriété canonique PidTagTnefCorrelationKey
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- MAPI.PidTagTnefCorrelationKey
api_type:
- COM
ms.assetid: a7f05c8c-59b4-4d5b-8e70-ebcde5f2ed45
description: Dernière modification le 9 mars 2015
ms.openlocfilehash: e38cf93523c14d2d58c48e24a79249674298b4b2
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32341950"
---
# <a name="pidtagtnefcorrelationkey-canonical-property"></a><span data-ttu-id="02567-103">Propriété canonique PidTagTnefCorrelationKey</span><span class="sxs-lookup"><span data-stu-id="02567-103">PidTagTnefCorrelationKey Canonical Property</span></span>

  
  
<span data-ttu-id="02567-104">**S’applique à** : Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="02567-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="02567-105">Contient une valeur qui met en corrélation une pièce jointe TNEF (Transport Neutral Encapsulation Format) avec un message.</span><span class="sxs-lookup"><span data-stu-id="02567-105">Contains a value that correlates a Transport Neutral Encapsulation Format (TNEF) attachment with a message.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="02567-106">Propriétés associées :</span><span class="sxs-lookup"><span data-stu-id="02567-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="02567-107">PR_TNEF_CORRELATION_KEY</span><span class="sxs-lookup"><span data-stu-id="02567-107">PR_TNEF_CORRELATION_KEY</span></span>  <br/> |
|<span data-ttu-id="02567-108">Identificateur :</span><span class="sxs-lookup"><span data-stu-id="02567-108">Identifier:</span></span>  <br/> |<span data-ttu-id="02567-109">0x007F</span><span class="sxs-lookup"><span data-stu-id="02567-109">0x007F</span></span>  <br/> |
|<span data-ttu-id="02567-110">Type de données :</span><span class="sxs-lookup"><span data-stu-id="02567-110">Data type:</span></span>  <br/> |<span data-ttu-id="02567-111">PT_BINARY</span><span class="sxs-lookup"><span data-stu-id="02567-111">PT_BINARY</span></span>  <br/> |
|<span data-ttu-id="02567-112">Domaine :</span><span class="sxs-lookup"><span data-stu-id="02567-112">Area:</span></span>  <br/> |<span data-ttu-id="02567-113">Enveloppe MAPI</span><span class="sxs-lookup"><span data-stu-id="02567-113">MAPI envelope</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="02567-114">Remarques</span><span class="sxs-lookup"><span data-stu-id="02567-114">Remarks</span></span>

<span data-ttu-id="02567-115">Il est recommandé que les sous-objets de pièce jointe TNEF exposent cette propriété.</span><span class="sxs-lookup"><span data-stu-id="02567-115">It is recommended that TNEF attachment sub-objects expose this property.</span></span> <span data-ttu-id="02567-116">Cette propriété détermine si un fichier TNEF entrant appartient au message à qui il est joint.</span><span class="sxs-lookup"><span data-stu-id="02567-116">This property determines whether or not an inbound TNEF file belongs to the message it is attached to.</span></span> <span data-ttu-id="02567-117">Il est principalement utilisé par les fournisseurs de transport et les passerelles.</span><span class="sxs-lookup"><span data-stu-id="02567-117">It is used primarily by transport providers and gateways.</span></span>
  
<span data-ttu-id="02567-118">Sur un message sortant, le fournisseur de transport doit calculer une valeur binaire propre à ce message, ou utiliser une valeur existante qui répond à l’exigence d’unicité, telle qu’un identificateur de message.</span><span class="sxs-lookup"><span data-stu-id="02567-118">On an outbound message, the transport provider should compute a binary value unique to that message, or use an existing value that satisfies the uniqueness requirement, such as a message identifier.</span></span> <span data-ttu-id="02567-119">Le fournisseur de transport doit stocker cette valeur dans cette propriété, puis appeler la méthode [ITnef::AddProps](itnef-addprops.md) pour l’encapsuler.</span><span class="sxs-lookup"><span data-stu-id="02567-119">The transport provider should store this value in this property and then call the [ITnef::AddProps](itnef-addprops.md) method to encapsulate it.</span></span> <span data-ttu-id="02567-120">La même valeur doit également être stockée dans l’enveloppe de transport à un endroit défini par le fournisseur, tel que l’en-tête du message.</span><span class="sxs-lookup"><span data-stu-id="02567-120">The same value should also be stored in the transport envelope in a place defined by the provider, such as the message header.</span></span> 
  
<span data-ttu-id="02567-121">Sur un message entrant, le fournisseur de transport doit appeler la méthode [ITnef::ExtractProps](itnef-extractprops.md) pour décaler la pièce jointe TNEF, puis comparer cette propriété à la valeur stockée dans l’enveloppe de transport.</span><span class="sxs-lookup"><span data-stu-id="02567-121">On an inbound message, the transport provider should call the [ITnef::ExtractProps](itnef-extractprops.md) method to decapsulate the TNEF attachment and then compare this property with the value stored in the transport envelope.</span></span> <span data-ttu-id="02567-122">Si les valeurs correspondent, le TNEF doit être traitée normalement, c’est-à-dire que toutes les propriétés extraites de la pièce jointe TNEF doivent être utilisées.</span><span class="sxs-lookup"><span data-stu-id="02567-122">If the values match, TNEF should be processed normally, that is, all the properties extracted from the TNEF attachment should be used.</span></span> <span data-ttu-id="02567-123">Si les valeurs ne correspondent pas, toutes les propriétés de la pièce jointe TNEF doivent être ignorées.</span><span class="sxs-lookup"><span data-stu-id="02567-123">If the values do not match, all the properties from the TNEF attachment should be ignored.</span></span> <span data-ttu-id="02567-124">Si cette propriété n’est pas définie, le fichier TNEF doit être considéré comme appartenant à ce message et les autres propriétés extraites de celui-ci doivent être utilisées.</span><span class="sxs-lookup"><span data-stu-id="02567-124">If this property is not set, the TNEF file should be considered to belong to this message, and the other properties extracted from it should be used.</span></span> 
  
## <a name="related-resources"></a><span data-ttu-id="02567-125">Ressources connexes</span><span class="sxs-lookup"><span data-stu-id="02567-125">Related resources</span></span>

### <a name="protocol-specifications"></a><span data-ttu-id="02567-126">Spécifications de protocole</span><span class="sxs-lookup"><span data-stu-id="02567-126">Protocol specifications</span></span>

<span data-ttu-id="02567-127">[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="02567-127">[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="02567-128">Fournit des références aux spécifications Exchange Server protocole.</span><span class="sxs-lookup"><span data-stu-id="02567-128">Provides references to related Exchange Server protocol specifications.</span></span>
    
<span data-ttu-id="02567-129">[[MS-OXCFXICS]](https://msdn.microsoft.com/library/b9752f3d-d50d-44b8-9e6b-608a117c8532%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="02567-129">[[MS-OXCFXICS]](https://msdn.microsoft.com/library/b9752f3d-d50d-44b8-9e6b-608a117c8532%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="02567-130">Gère l’ordre et le flux des transferts de données entre un client et un serveur.</span><span class="sxs-lookup"><span data-stu-id="02567-130">Handles the order and flow for data transfers between a client and server.</span></span>
    
<span data-ttu-id="02567-131">[[MS-OXCMAIL]](https://msdn.microsoft.com/library/b60d48db-183f-4bf5-a908-f584e62cb2d4%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="02567-131">[[MS-OXCMAIL]](https://msdn.microsoft.com/library/b60d48db-183f-4bf5-a908-f584e62cb2d4%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="02567-132">Convertit des conventions de messagerie standard Internet en objets de message.</span><span class="sxs-lookup"><span data-stu-id="02567-132">Converts from Internet standard email conventions to message objects.</span></span>
    
<span data-ttu-id="02567-133">[[MS-OXTNEF]](https://msdn.microsoft.com/library/1f0544d7-30b7-4194-b58f-adc82f3763bb%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="02567-133">[[MS-OXTNEF]](https://msdn.microsoft.com/library/1f0544d7-30b7-4194-b58f-adc82f3763bb%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="02567-134">Encode et décode les objets de message et de pièce jointe dans une représentation de flux efficace.</span><span class="sxs-lookup"><span data-stu-id="02567-134">Encodes and decodes message and attachment objects to an efficient stream representation.</span></span>
    
### <a name="header-files"></a><span data-ttu-id="02567-135">Fichiers d’en-tête</span><span class="sxs-lookup"><span data-stu-id="02567-135">Header files</span></span>

<span data-ttu-id="02567-136">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="02567-136">Mapidefs.h</span></span>
  
> <span data-ttu-id="02567-137">Fournit des définitions de type de données.</span><span class="sxs-lookup"><span data-stu-id="02567-137">Provides data type definitions.</span></span>
    
<span data-ttu-id="02567-138">Mapitags.h</span><span class="sxs-lookup"><span data-stu-id="02567-138">Mapitags.h</span></span>
  
> <span data-ttu-id="02567-139">Contient les définitions des propriétés répertoriées en tant que noms de remplacement.</span><span class="sxs-lookup"><span data-stu-id="02567-139">Contains definitions of properties listed as alternate names.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="02567-140">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="02567-140">See also</span></span>



[<span data-ttu-id="02567-141">Propriétés MAPI</span><span class="sxs-lookup"><span data-stu-id="02567-141">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="02567-142">Propriétés canoniques MAPI</span><span class="sxs-lookup"><span data-stu-id="02567-142">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="02567-143">Mappage des noms de propriétés canoniques aux noms MAPI</span><span class="sxs-lookup"><span data-stu-id="02567-143">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="02567-144">Mappage des noms MAPI aux noms de propriétés canoniques</span><span class="sxs-lookup"><span data-stu-id="02567-144">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

