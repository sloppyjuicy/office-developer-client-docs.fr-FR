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
ms.openlocfilehash: d12e8510686f51698981c47327f79ef40d3ec342
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32342538"
---
# <a name="pidtagmappingsignature-canonical-property"></a><span data-ttu-id="e0101-103">Propriété canonique PidTagMappingSignature</span><span class="sxs-lookup"><span data-stu-id="e0101-103">PidTagMappingSignature Canonical Property</span></span>

  
  
<span data-ttu-id="e0101-104">**S’applique à** : Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="e0101-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="e0101-105">Contient la signature de mappage pour les propriétés nommées d'un objet MAPI particulier.</span><span class="sxs-lookup"><span data-stu-id="e0101-105">Contains the mapping signature for named properties of a particular MAPI object.</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="e0101-106">Propriétés associées :</span><span class="sxs-lookup"><span data-stu-id="e0101-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="e0101-107">PR_MAPPING_SIGNATURE</span><span class="sxs-lookup"><span data-stu-id="e0101-107">PR_MAPPING_SIGNATURE</span></span>  <br/> |
|<span data-ttu-id="e0101-108">Identificateur :</span><span class="sxs-lookup"><span data-stu-id="e0101-108">Identifier:</span></span>  <br/> |<span data-ttu-id="e0101-109">0x0FF8</span><span class="sxs-lookup"><span data-stu-id="e0101-109">0x0FF8</span></span>  <br/> |
|<span data-ttu-id="e0101-110">Type de données :</span><span class="sxs-lookup"><span data-stu-id="e0101-110">Data type:</span></span>  <br/> |<span data-ttu-id="e0101-111">PT_BINARY</span><span class="sxs-lookup"><span data-stu-id="e0101-111">PT_BINARY</span></span>  <br/> |
|<span data-ttu-id="e0101-112">Domaine :</span><span class="sxs-lookup"><span data-stu-id="e0101-112">Area:</span></span>  <br/> |<span data-ttu-id="e0101-113">Divers</span><span class="sxs-lookup"><span data-stu-id="e0101-113">Miscellaneous</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="e0101-114">Remarques</span><span class="sxs-lookup"><span data-stu-id="e0101-114">Remarks</span></span>

<span data-ttu-id="e0101-115">Il est recommandé que les objets ayant des propriétés nommées exposent cette propriété.</span><span class="sxs-lookup"><span data-stu-id="e0101-115">It is recommended that objects having named properties expose this property.</span></span> <span data-ttu-id="e0101-116">Une application cliente doit vérifier la propriété **PR_MAPPING_SIGNATURE** des deux objets lors de la copie des propriétés nommées d'un objet à un autre.</span><span class="sxs-lookup"><span data-stu-id="e0101-116">A client application should check the **PR_MAPPING_SIGNATURE** property of both objects when copying named properties from one object to another.</span></span> <span data-ttu-id="e0101-117">L'utilisation de cette propriété peut réduire la traduction entre les noms et les identificateurs des propriétés copiées.</span><span class="sxs-lookup"><span data-stu-id="e0101-117">Use of this property can minimize translating between copied properties' names and identifiers.</span></span> 
  
<span data-ttu-id="e0101-118">Si cette propriété n'existe pas pour un objet MAPI donné, l'objet possède son propre mappage unique des noms et des identificateurs.</span><span class="sxs-lookup"><span data-stu-id="e0101-118">If this property does not exist for a given MAPI object, then the object has its own unique mapping of names and identifiers.</span></span> <span data-ttu-id="e0101-119">Dans ce cas, le client doit appeler la méthode [IMAPIProp:: GetNamesFromIDs](imapiprop-getnamesfromids.md) sur l'objet source, puis la méthode [IMAPIProp:: GetIDsFromNames](imapiprop-getidsfromnames.md) sur l'objet de destination.</span><span class="sxs-lookup"><span data-stu-id="e0101-119">In this case the client must call the [IMAPIProp::GetNamesFromIDs](imapiprop-getnamesfromids.md) method on the source object and then the [IMAPIProp::GetIDsFromNames](imapiprop-getidsfromnames.md) method on the destination object.</span></span> 
  
<span data-ttu-id="e0101-120">Lorsque deux objets ont la même valeur **PR_MAPPING_SIGNATURE** , le client n'a pas besoin de convertir Name en identifier et identifier en Name.</span><span class="sxs-lookup"><span data-stu-id="e0101-120">When two objects have the same **PR_MAPPING_SIGNATURE** value, the client does not need to translate name to identifier and identifier to name.</span></span> <span data-ttu-id="e0101-121">Le client peut simplement appeler la méthode [IMAPIProp:: GetProps](imapiprop-getprops.md) sur la source, puis la méthode [IMAPIProp:: SetProps](imapiprop-setprops.md) sur la destination.</span><span class="sxs-lookup"><span data-stu-id="e0101-121">The client can simply call the [IMAPIProp::GetProps](imapiprop-getprops.md) method on the source and then the [IMAPIProp::SetProps](imapiprop-setprops.md) method on the destination.</span></span> <span data-ttu-id="e0101-122">Cela est pratique pour les clients qui effectuent une copie personnalisée des propriétés nommées et pour les fournisseurs qui implémentent les méthodes [IMAPIProp:: CopyTo](imapiprop-copyto.md) et [IMAPIProp:: CopyProps](imapiprop-copyprops.md) .</span><span class="sxs-lookup"><span data-stu-id="e0101-122">This is convenient for clients that perform custom copying of named properties, and for providers implementing the [IMAPIProp::CopyTo](imapiprop-copyto.md) and [IMAPIProp::CopyProps](imapiprop-copyprops.md) methods.</span></span> 
  
<span data-ttu-id="e0101-123">Pour plus d'informations sur les propriétés nommées et le mappage des noms et des identificateurs, consultez la rubrique [MAPI named Properties](mapi-named-properties.md).</span><span class="sxs-lookup"><span data-stu-id="e0101-123">For more information on named properties and mapping of names and identifiers, see [MAPI Named Properties](mapi-named-properties.md).</span></span> 
  
## <a name="related-resources"></a><span data-ttu-id="e0101-124">Ressources associées</span><span class="sxs-lookup"><span data-stu-id="e0101-124">Related resources</span></span>

### <a name="protocol-specifications"></a><span data-ttu-id="e0101-125">Spécifications de protocole</span><span class="sxs-lookup"><span data-stu-id="e0101-125">Protocol specifications</span></span>

<span data-ttu-id="e0101-126">[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="e0101-126">[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="e0101-127">Fournit des références à des spécifications de protocole Exchange Server connexes.</span><span class="sxs-lookup"><span data-stu-id="e0101-127">Provides references to related Exchange Server protocol specifications.</span></span>
    
<span data-ttu-id="e0101-128">[[MS-OXOABK]](https://msdn.microsoft.com/library/f4cf9b4c-9232-4506-9e71-2270de217614%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="e0101-128">[[MS-OXOABK]](https://msdn.microsoft.com/library/f4cf9b4c-9232-4506-9e71-2270de217614%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="e0101-129">Spécifie les propriétés et les opérations pour les listes d'utilisateurs, de contacts, de groupes et de ressources.</span><span class="sxs-lookup"><span data-stu-id="e0101-129">Specifies the properties and operations for lists of users, contacts, groups, and resources.</span></span>
    
### <a name="header-files"></a><span data-ttu-id="e0101-130">Fichiers d'en-tête</span><span class="sxs-lookup"><span data-stu-id="e0101-130">Header files</span></span>

<span data-ttu-id="e0101-131">Mapidefs. h</span><span class="sxs-lookup"><span data-stu-id="e0101-131">Mapidefs.h</span></span>
  
> <span data-ttu-id="e0101-132">Fournit des définitions de type de données.</span><span class="sxs-lookup"><span data-stu-id="e0101-132">Provides data type definitions.</span></span>
    
<span data-ttu-id="e0101-133">Mapitags. h</span><span class="sxs-lookup"><span data-stu-id="e0101-133">Mapitags.h</span></span>
  
> <span data-ttu-id="e0101-134">Contient les définitions des propriétés figurant en tant que noms de substitution.</span><span class="sxs-lookup"><span data-stu-id="e0101-134">Contains definitions of properties listed as alternate names.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="e0101-135">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="e0101-135">See also</span></span>



[<span data-ttu-id="e0101-136">MAPINAMEID</span><span class="sxs-lookup"><span data-stu-id="e0101-136">MAPINAMEID</span></span>](mapinameid.md)


[<span data-ttu-id="e0101-137">Propriétés MAPI</span><span class="sxs-lookup"><span data-stu-id="e0101-137">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="e0101-138">Propriétés canoniques MAPI</span><span class="sxs-lookup"><span data-stu-id="e0101-138">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="e0101-139">Mappage des noms de propriétés canoniques aux noms MAPI</span><span class="sxs-lookup"><span data-stu-id="e0101-139">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="e0101-140">Mappage des noms MAPI aux noms de propriétés canoniques</span><span class="sxs-lookup"><span data-stu-id="e0101-140">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

