---
title: Propriété canonique PidTagMappingSignature
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- PidTagMappingSignature
api_type:
- HeaderDef
ms.assetid: a5e9f807-12a9-4bc9-a6a5-17579e747ffa
description: 'Derni�re modification�: lundi 9 mars 2015'
ms.openlocfilehash: 0a83e0aa8f7ab1eb1f30e3ba97d3ea36f16fd873
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19786204"
---
# <a name="pidtagmappingsignature-canonical-property"></a><span data-ttu-id="58659-103">Propriété canonique PidTagMappingSignature</span><span class="sxs-lookup"><span data-stu-id="58659-103">PidTagMappingSignature Canonical Property</span></span>

  
  
<span data-ttu-id="58659-104">**S’applique à**: Outlook</span><span class="sxs-lookup"><span data-stu-id="58659-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="58659-105">Contient la signature de mappage de propriétés nommées d’un objet MAPI particulier.</span><span class="sxs-lookup"><span data-stu-id="58659-105">Contains the mapping signature for named properties of a particular MAPI object.</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="58659-106">Propriétés associées :</span><span class="sxs-lookup"><span data-stu-id="58659-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="58659-107">PR_MAPPING_SIGNATURE</span><span class="sxs-lookup"><span data-stu-id="58659-107">PR_MAPPING_SIGNATURE</span></span>  <br/> |
|<span data-ttu-id="58659-108">Identificateur :</span><span class="sxs-lookup"><span data-stu-id="58659-108">Identifier:</span></span>  <br/> |<span data-ttu-id="58659-109">0x0FF8</span><span class="sxs-lookup"><span data-stu-id="58659-109">0x0FF8</span></span>  <br/> |
|<span data-ttu-id="58659-110">Type de données :</span><span class="sxs-lookup"><span data-stu-id="58659-110">Data type:</span></span>  <br/> |<span data-ttu-id="58659-111">PT_BINARY</span><span class="sxs-lookup"><span data-stu-id="58659-111">PT_BINARY</span></span>  <br/> |
|<span data-ttu-id="58659-112">Zone :</span><span class="sxs-lookup"><span data-stu-id="58659-112">Area:</span></span>  <br/> |<span data-ttu-id="58659-113">Divers</span><span class="sxs-lookup"><span data-stu-id="58659-113">Miscellaneous</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="58659-114">Remarques</span><span class="sxs-lookup"><span data-stu-id="58659-114">Remarks</span></span>

<span data-ttu-id="58659-115">Il est recommandé que les objets ayant des propriétés nommées exposent cette propriété.</span><span class="sxs-lookup"><span data-stu-id="58659-115">It is recommended that objects having named properties expose this property.</span></span> <span data-ttu-id="58659-116">Une application cliente doit vérifier la propriété **PR_MAPPING_SIGNATURE** des deux objets lors de la copie des propriétés d’un objet à un autre nommées.</span><span class="sxs-lookup"><span data-stu-id="58659-116">A client application should check the **PR_MAPPING_SIGNATURE** property of both objects when copying named properties from one object to another.</span></span> <span data-ttu-id="58659-117">Utilisation de cette propriété peut réduire la traduction entre les noms et les identificateurs des propriétés copiées.</span><span class="sxs-lookup"><span data-stu-id="58659-117">Use of this property can minimize translating between copied properties' names and identifiers.</span></span> 
  
<span data-ttu-id="58659-118">Si cette propriété n’existe pas pour un objet MAPI donné, l’objet possède son propre mappage de noms et identificateurs unique.</span><span class="sxs-lookup"><span data-stu-id="58659-118">If this property does not exist for a given MAPI object, then the object has its own unique mapping of names and identifiers.</span></span> <span data-ttu-id="58659-119">Dans ce cas le client doit appeler la méthode [IMAPIProp::GetNamesFromIDs](imapiprop-getnamesfromids.md) sur l’objet source, puis la méthode [IMAPIProp::GetIDsFromNames](imapiprop-getidsfromnames.md) sur l’objet de destination.</span><span class="sxs-lookup"><span data-stu-id="58659-119">In this case the client must call the [IMAPIProp::GetNamesFromIDs](imapiprop-getnamesfromids.md) method on the source object and then the [IMAPIProp::GetIDsFromNames](imapiprop-getidsfromnames.md) method on the destination object.</span></span> 
  
<span data-ttu-id="58659-120">Lorsque deux objets ont la même valeur **PR_MAPPING_SIGNATURE** , le client n’a pas besoin traduire le nom d’identificateur et identificateur de nom.</span><span class="sxs-lookup"><span data-stu-id="58659-120">When two objects have the same **PR_MAPPING_SIGNATURE** value, the client does not need to translate name to identifier and identifier to name.</span></span> <span data-ttu-id="58659-121">Le client peut simplement appeler la méthode [IMAPIProp::GetProps](imapiprop-getprops.md) sur la source, puis la méthode [IMAPIProp::SetProps](imapiprop-setprops.md) sur la destination.</span><span class="sxs-lookup"><span data-stu-id="58659-121">The client can simply call the [IMAPIProp::GetProps](imapiprop-getprops.md) method on the source and then the [IMAPIProp::SetProps](imapiprop-setprops.md) method on the destination.</span></span> <span data-ttu-id="58659-122">Cela est utile pour les clients qui effectuent une copie personnalisée de propriétés nommées et pour les fournisseurs de mise en œuvre les méthodes [IMAPIProp::CopyTo](imapiprop-copyto.md) et [IMAPIProp::CopyProps](imapiprop-copyprops.md) .</span><span class="sxs-lookup"><span data-stu-id="58659-122">This is convenient for clients that perform custom copying of named properties, and for providers implementing the [IMAPIProp::CopyTo](imapiprop-copyto.md) and [IMAPIProp::CopyProps](imapiprop-copyprops.md) methods.</span></span> 
  
<span data-ttu-id="58659-123">Pour plus d’informations sur les propriétés nommées et le mappage des noms et identificateurs, voir [Les propriétés MAPI nommée](mapi-named-properties.md).</span><span class="sxs-lookup"><span data-stu-id="58659-123">For more information on named properties and mapping of names and identifiers, see [MAPI Named Properties](mapi-named-properties.md).</span></span> 
  
## <a name="related-resources"></a><span data-ttu-id="58659-124">Ressources connexes</span><span class="sxs-lookup"><span data-stu-id="58659-124">Related resources</span></span>

### <a name="protocol-specifications"></a><span data-ttu-id="58659-125">Spécifications du protocole</span><span class="sxs-lookup"><span data-stu-id="58659-125">Protocol specifications</span></span>

<span data-ttu-id="58659-126">[[MS-OXPROPS]](http://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="58659-126">[[MS-OXPROPS]](http://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="58659-127">Fournit des références aux spécifications du protocole Exchange Server associées.</span><span class="sxs-lookup"><span data-stu-id="58659-127">Provides references to related Exchange Server protocol specifications.</span></span>
    
<span data-ttu-id="58659-128">[[MS-OXOABK]](http://msdn.microsoft.com/library/f4cf9b4c-9232-4506-9e71-2270de217614%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="58659-128">[[MS-OXOABK]](http://msdn.microsoft.com/library/f4cf9b4c-9232-4506-9e71-2270de217614%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="58659-129">Spécifie les propriétés et opérations pour les listes des utilisateurs, des contacts, des groupes et des ressources.</span><span class="sxs-lookup"><span data-stu-id="58659-129">Specifies the properties and operations for lists of users, contacts, groups, and resources.</span></span>
    
### <a name="header-files"></a><span data-ttu-id="58659-130">Fichiers d’en-tête</span><span class="sxs-lookup"><span data-stu-id="58659-130">Header files</span></span>

<span data-ttu-id="58659-131">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="58659-131">Mapidefs.h</span></span>
  
> <span data-ttu-id="58659-132">Fournit des définitions de type de données.</span><span class="sxs-lookup"><span data-stu-id="58659-132">Provides data type definitions.</span></span>
    
<span data-ttu-id="58659-133">MAPITAGS.h</span><span class="sxs-lookup"><span data-stu-id="58659-133">Mapitags.h</span></span>
  
> <span data-ttu-id="58659-134">Contient les définitions des propriétés répertoriées en tant que d’autres noms.</span><span class="sxs-lookup"><span data-stu-id="58659-134">Contains definitions of properties listed as alternate names.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="58659-135">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="58659-135">See also</span></span>



[<span data-ttu-id="58659-136">MAPINAMEID</span><span class="sxs-lookup"><span data-stu-id="58659-136">MAPINAMEID</span></span>](mapinameid.md)


[<span data-ttu-id="58659-137">Propriétés MAPI</span><span class="sxs-lookup"><span data-stu-id="58659-137">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="58659-138">Propriétés canoniques MAPI</span><span class="sxs-lookup"><span data-stu-id="58659-138">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="58659-139">Mappage de noms de propriété canonique aux noms MAPI</span><span class="sxs-lookup"><span data-stu-id="58659-139">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="58659-140">Mappage de noms MAPI pour les noms de propriété canonique</span><span class="sxs-lookup"><span data-stu-id="58659-140">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

