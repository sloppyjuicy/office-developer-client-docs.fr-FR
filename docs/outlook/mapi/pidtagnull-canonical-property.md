---
title: Propriété canonique PidTagNull
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- PidTagNull
api_type:
- HeaderDef
ms.assetid: 192cdab8-c615-47b9-9f04-a1414eaf0c77
description: Dernière modification le 09 mars 2015
ms.openlocfilehash: efb0812a88ad435c2456a729a6e950b371cc0250
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/23/2018
ms.locfileid: "22595348"
---
# <a name="pidtagnull-canonical-property"></a><span data-ttu-id="365f0-103">Propriété canonique PidTagNull</span><span class="sxs-lookup"><span data-stu-id="365f0-103">PidTagNull Canonical Property</span></span>

  
  
<span data-ttu-id="365f0-104">**S’applique à**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="365f0-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="365f0-105">Représente un paramètre d’une propriété ou une valeur null ou réserve de l’espace de tableau.</span><span class="sxs-lookup"><span data-stu-id="365f0-105">Represents a null value or setting of a property or reserves array space.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="365f0-106">Propriétés associées :</span><span class="sxs-lookup"><span data-stu-id="365f0-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="365f0-107">PR_NULL</span><span class="sxs-lookup"><span data-stu-id="365f0-107">PR_NULL</span></span>  <br/> |
|<span data-ttu-id="365f0-108">Identificateur :</span><span class="sxs-lookup"><span data-stu-id="365f0-108">Identifier:</span></span>  <br/> |<span data-ttu-id="365f0-109">0x0000</span><span class="sxs-lookup"><span data-stu-id="365f0-109">0x0000</span></span>  <br/> |
|<span data-ttu-id="365f0-110">Type de données :</span><span class="sxs-lookup"><span data-stu-id="365f0-110">Data type:</span></span>  <br/> |<span data-ttu-id="365f0-111">PT_NULL</span><span class="sxs-lookup"><span data-stu-id="365f0-111">PT_NULL</span></span>  <br/> |
|<span data-ttu-id="365f0-112">Domaine :</span><span class="sxs-lookup"><span data-stu-id="365f0-112">Area:</span></span>  <br/> |<span data-ttu-id="365f0-113">Common</span><span class="sxs-lookup"><span data-stu-id="365f0-113">Common</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="365f0-114">Remarques</span><span class="sxs-lookup"><span data-stu-id="365f0-114">Remarks</span></span>

<span data-ttu-id="365f0-115">Cette propriété est utilisée pour réserver un espace dans les tableaux de structures [SPropValue](spropvalue.md) .</span><span class="sxs-lookup"><span data-stu-id="365f0-115">This property is used to reserve space in arrays of [SPropValue](spropvalue.md) structures.</span></span> <span data-ttu-id="365f0-116">Il est utilisé dans un tableau de structures [SPropTagArray](sproptagarray.md) pour indiquer la méthode à réserver un espace dans le tableau retourné des structures **SPropValue** .</span><span class="sxs-lookup"><span data-stu-id="365f0-116">It is used in an array of [SPropTagArray](sproptagarray.md) structures to tell the method to reserve space in the returned array of **SPropValue** structures.</span></span> <span data-ttu-id="365f0-117">Ainsi, pour les propriétés calculées à remplir de manière économique.</span><span class="sxs-lookup"><span data-stu-id="365f0-117">This allows for computed properties to be filled in an inexpensive way.</span></span> 
  
<span data-ttu-id="365f0-118">Pour plus d’informations, voir [Vue d’ensemble des types de propriété MAPI](mapi-property-type-overview.md).</span><span class="sxs-lookup"><span data-stu-id="365f0-118">For more information, see [MAPI Property Type Overview](mapi-property-type-overview.md).</span></span>
  
## <a name="related-resources"></a><span data-ttu-id="365f0-119">Ressources connexes</span><span class="sxs-lookup"><span data-stu-id="365f0-119">Related resources</span></span>

### <a name="protocol-specifications"></a><span data-ttu-id="365f0-120">Spécifications du protocole</span><span class="sxs-lookup"><span data-stu-id="365f0-120">Protocol specifications</span></span>

<span data-ttu-id="365f0-121">[[MS-OXOCNTC]](http://msdn.microsoft.com/library/9b636532-9150-4836-9635-9c9b756c9ccf%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="365f0-121">[[MS-OXOCNTC]](http://msdn.microsoft.com/library/9b636532-9150-4836-9635-9c9b756c9ccf%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="365f0-122">Spécifie les propriétés et les opérations qui sont autorisées sur les contacts et les listes de distribution personnelle.</span><span class="sxs-lookup"><span data-stu-id="365f0-122">Specifies the properties and operations that are permissible on contacts and personal distribution lists.</span></span>
    
### <a name="header-files"></a><span data-ttu-id="365f0-123">Fichiers d’en-tête</span><span class="sxs-lookup"><span data-stu-id="365f0-123">Header files</span></span>

<span data-ttu-id="365f0-124">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="365f0-124">Mapidefs.h</span></span>
  
> <span data-ttu-id="365f0-125">Fournit des définitions de type de données.</span><span class="sxs-lookup"><span data-stu-id="365f0-125">Provides data type definitions.</span></span>
    
<span data-ttu-id="365f0-126">MAPITAGS.h</span><span class="sxs-lookup"><span data-stu-id="365f0-126">Mapitags.h</span></span>
  
> <span data-ttu-id="365f0-127">Contient les définitions des propriétés répertoriées en tant que propriétés associées.</span><span class="sxs-lookup"><span data-stu-id="365f0-127">Contains definitions of properties listed as associated properties.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="365f0-128">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="365f0-128">See also</span></span>



[<span data-ttu-id="365f0-129">Propriétés MAPI</span><span class="sxs-lookup"><span data-stu-id="365f0-129">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="365f0-130">Propriétés canoniques MAPI</span><span class="sxs-lookup"><span data-stu-id="365f0-130">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="365f0-131">Mappage des noms de propriétés canoniques aux noms MAPI</span><span class="sxs-lookup"><span data-stu-id="365f0-131">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="365f0-132">Mappage des noms MAPI aux noms de propriétés canoniques</span><span class="sxs-lookup"><span data-stu-id="365f0-132">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

