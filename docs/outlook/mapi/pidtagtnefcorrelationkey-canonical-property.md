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
description: 'Derni�re modification�: lundi 9 mars 2015'
ms.openlocfilehash: 5a0216616d9a35ef5ad4509bc377044c1d217d79
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19786879"
---
# <a name="pidtagtnefcorrelationkey-canonical-property"></a><span data-ttu-id="ac54a-103">Propriété canonique PidTagTnefCorrelationKey</span><span class="sxs-lookup"><span data-stu-id="ac54a-103">PidTagTnefCorrelationKey Canonical Property</span></span>

  
  
<span data-ttu-id="ac54a-104">**S’applique à**: Outlook</span><span class="sxs-lookup"><span data-stu-id="ac54a-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="ac54a-105">Contient une valeur qui met en corrélation une pièce jointe TNEF Transport Neutral Encapsulation Format () avec un message.</span><span class="sxs-lookup"><span data-stu-id="ac54a-105">Contains a value that correlates a Transport Neutral Encapsulation Format (TNEF) attachment with a message.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="ac54a-106">Propriétés associées :</span><span class="sxs-lookup"><span data-stu-id="ac54a-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="ac54a-107">PR_TNEF_CORRELATION_KEY</span><span class="sxs-lookup"><span data-stu-id="ac54a-107">PR_TNEF_CORRELATION_KEY</span></span>  <br/> |
|<span data-ttu-id="ac54a-108">Identificateur :</span><span class="sxs-lookup"><span data-stu-id="ac54a-108">Identifier:</span></span>  <br/> |<span data-ttu-id="ac54a-109">0x007F</span><span class="sxs-lookup"><span data-stu-id="ac54a-109">0x007F</span></span>  <br/> |
|<span data-ttu-id="ac54a-110">Type de données :</span><span class="sxs-lookup"><span data-stu-id="ac54a-110">Data type:</span></span>  <br/> |<span data-ttu-id="ac54a-111">PT_BINARY</span><span class="sxs-lookup"><span data-stu-id="ac54a-111">PT_BINARY</span></span>  <br/> |
|<span data-ttu-id="ac54a-112">Zone :</span><span class="sxs-lookup"><span data-stu-id="ac54a-112">Area:</span></span>  <br/> |<span data-ttu-id="ac54a-113">Enveloppe MAPI</span><span class="sxs-lookup"><span data-stu-id="ac54a-113">MAPI envelope</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="ac54a-114">Remarques</span><span class="sxs-lookup"><span data-stu-id="ac54a-114">Remarks</span></span>

<span data-ttu-id="ac54a-115">Il est recommandé que les sous-objets de pièce jointe TNEF exposent cette propriété.</span><span class="sxs-lookup"><span data-stu-id="ac54a-115">It is recommended that TNEF attachment sub-objects expose this property.</span></span> <span data-ttu-id="ac54a-116">Cette propriété détermine si un fichier TNEF entrant appartient au message, à qu'il est connecté.</span><span class="sxs-lookup"><span data-stu-id="ac54a-116">This property determines whether or not an inbound TNEF file belongs to the message it is attached to.</span></span> <span data-ttu-id="ac54a-117">Il est utilisé principalement par les passerelles et les fournisseurs de transport.</span><span class="sxs-lookup"><span data-stu-id="ac54a-117">It is used primarily by transport providers and gateways.</span></span>
  
<span data-ttu-id="ac54a-118">Dans un message sortant, le fournisseur de transport doit calculer une valeur binaire unique à ce message, ou utiliser une valeur existante qui satisfait les règles d’unicité, par exemple un identificateur de message.</span><span class="sxs-lookup"><span data-stu-id="ac54a-118">On an outbound message, the transport provider should compute a binary value unique to that message, or use an existing value that satisfies the uniqueness requirement, such as a message identifier.</span></span> <span data-ttu-id="ac54a-119">Le fournisseur de transport doit stocker cette valeur dans cette propriété, puis appelez la méthode [ITnef::AddProps](itnef-addprops.md) pour encapsuler.</span><span class="sxs-lookup"><span data-stu-id="ac54a-119">The transport provider should store this value in this property and then call the [ITnef::AddProps](itnef-addprops.md) method to encapsulate it.</span></span> <span data-ttu-id="ac54a-120">La même valeur doit également être stockée dans l’enveloppe de transport dans un emplacement défini par le fournisseur, telles que l’en-tête du message.</span><span class="sxs-lookup"><span data-stu-id="ac54a-120">The same value should also be stored in the transport envelope in a place defined by the provider, such as the message header.</span></span> 
  
<span data-ttu-id="ac54a-121">Sur un message entrant, le fournisseur de transport doit appeler la méthode [ITnef::ExtractProps](itnef-extractprops.md) à décapsulent la pièce jointe TNEF et comparez cette propriété avec la valeur stockée dans l’enveloppe de transport.</span><span class="sxs-lookup"><span data-stu-id="ac54a-121">On an inbound message, the transport provider should call the [ITnef::ExtractProps](itnef-extractprops.md) method to decapsulate the TNEF attachment and then compare this property with the value stored in the transport envelope.</span></span> <span data-ttu-id="ac54a-122">Si les valeurs correspondent, TNEF sera traité normalement, autrement dit, toutes les propriétés extraites de la pièce jointe TNEF doivent être utilisées.</span><span class="sxs-lookup"><span data-stu-id="ac54a-122">If the values match, TNEF should be processed normally, that is, all the properties extracted from the TNEF attachment should be used.</span></span> <span data-ttu-id="ac54a-123">Si les valeurs ne correspondent pas, toutes les propriétés de la pièce jointe TNEF doivent être ignorées.</span><span class="sxs-lookup"><span data-stu-id="ac54a-123">If the values do not match, all the properties from the TNEF attachment should be ignored.</span></span> <span data-ttu-id="ac54a-124">Si cette propriété n’est pas définie, le fichier TNEF doit être considérées comme appartenant à ce message, et les autres propriétés extraites d’elle doivent être utilisées.</span><span class="sxs-lookup"><span data-stu-id="ac54a-124">If this property is not set, the TNEF file should be considered to belong to this message, and the other properties extracted from it should be used.</span></span> 
  
## <a name="related-resources"></a><span data-ttu-id="ac54a-125">Ressources connexes</span><span class="sxs-lookup"><span data-stu-id="ac54a-125">Related resources</span></span>

### <a name="protocol-specifications"></a><span data-ttu-id="ac54a-126">Spécifications du protocole</span><span class="sxs-lookup"><span data-stu-id="ac54a-126">Protocol specifications</span></span>

<span data-ttu-id="ac54a-127">[[MS-OXPROPS]](http://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="ac54a-127">[[MS-OXPROPS]](http://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="ac54a-128">Fournit des références aux spécifications du protocole Exchange Server associées.</span><span class="sxs-lookup"><span data-stu-id="ac54a-128">Provides references to related Exchange Server protocol specifications.</span></span>
    
<span data-ttu-id="ac54a-129">[[MS-OXCFXICS]](http://msdn.microsoft.com/library/b9752f3d-d50d-44b8-9e6b-608a117c8532%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="ac54a-129">[[MS-OXCFXICS]](http://msdn.microsoft.com/library/b9752f3d-d50d-44b8-9e6b-608a117c8532%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="ac54a-130">Gère l’ordre et le flux pour les transferts de données entre un client et le serveur.</span><span class="sxs-lookup"><span data-stu-id="ac54a-130">Handles the order and flow for data transfers between a client and server.</span></span>
    
<span data-ttu-id="ac54a-131">[[MS-OXCMAIL]](http://msdn.microsoft.com/library/b60d48db-183f-4bf5-a908-f584e62cb2d4%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="ac54a-131">[[MS-OXCMAIL]](http://msdn.microsoft.com/library/b60d48db-183f-4bf5-a908-f584e62cb2d4%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="ac54a-132">Convertit des conventions de messagerie standard Internet aux objets de message.</span><span class="sxs-lookup"><span data-stu-id="ac54a-132">Converts from Internet standard email conventions to message objects.</span></span>
    
<span data-ttu-id="ac54a-133">[[MS-OXTNEF]](http://msdn.microsoft.com/library/1f0544d7-30b7-4194-b58f-adc82f3763bb%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="ac54a-133">[[MS-OXTNEF]](http://msdn.microsoft.com/library/1f0544d7-30b7-4194-b58f-adc82f3763bb%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="ac54a-134">Code et décode des objets message et la pièce jointe à une représentation sous forme de flux efficace.</span><span class="sxs-lookup"><span data-stu-id="ac54a-134">Encodes and decodes message and attachment objects to an efficient stream representation.</span></span>
    
### <a name="header-files"></a><span data-ttu-id="ac54a-135">Fichiers d’en-tête</span><span class="sxs-lookup"><span data-stu-id="ac54a-135">Header files</span></span>

<span data-ttu-id="ac54a-136">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="ac54a-136">Mapidefs.h</span></span>
  
> <span data-ttu-id="ac54a-137">Fournit des définitions de type de données.</span><span class="sxs-lookup"><span data-stu-id="ac54a-137">Provides data type definitions.</span></span>
    
<span data-ttu-id="ac54a-138">MAPITAGS.h</span><span class="sxs-lookup"><span data-stu-id="ac54a-138">Mapitags.h</span></span>
  
> <span data-ttu-id="ac54a-139">Contient les définitions des propriétés répertoriées en tant que d’autres noms.</span><span class="sxs-lookup"><span data-stu-id="ac54a-139">Contains definitions of properties listed as alternate names.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="ac54a-140">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="ac54a-140">See also</span></span>



[<span data-ttu-id="ac54a-141">Propriétés MAPI</span><span class="sxs-lookup"><span data-stu-id="ac54a-141">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="ac54a-142">Propriétés canoniques MAPI</span><span class="sxs-lookup"><span data-stu-id="ac54a-142">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="ac54a-143">Mappage de noms de propriété canonique aux noms MAPI</span><span class="sxs-lookup"><span data-stu-id="ac54a-143">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="ac54a-144">Mappage de noms MAPI pour les noms de propriété canonique</span><span class="sxs-lookup"><span data-stu-id="ac54a-144">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

