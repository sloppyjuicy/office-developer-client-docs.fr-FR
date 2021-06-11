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
description: Dernière modification le 9 mars 2015
ms.openlocfilehash: 7e9c3340dfad47a811b56c86e8e6104fb6aac7c2
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32329266"
---
# <a name="pidtagnull-canonical-property"></a><span data-ttu-id="6c5b8-103">Propriété canonique PidTagNull</span><span class="sxs-lookup"><span data-stu-id="6c5b8-103">PidTagNull Canonical Property</span></span>

  
  
<span data-ttu-id="6c5b8-104">**S’applique à** : Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="6c5b8-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="6c5b8-105">Représente une valeur null ou un paramètre d’une propriété ou réserve de l’espace de tableau.</span><span class="sxs-lookup"><span data-stu-id="6c5b8-105">Represents a null value or setting of a property or reserves array space.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="6c5b8-106">Propriétés associées :</span><span class="sxs-lookup"><span data-stu-id="6c5b8-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="6c5b8-107">PR_NULL</span><span class="sxs-lookup"><span data-stu-id="6c5b8-107">PR_NULL</span></span>  <br/> |
|<span data-ttu-id="6c5b8-108">Identificateur :</span><span class="sxs-lookup"><span data-stu-id="6c5b8-108">Identifier:</span></span>  <br/> |<span data-ttu-id="6c5b8-109">0x0000</span><span class="sxs-lookup"><span data-stu-id="6c5b8-109">0x0000</span></span>  <br/> |
|<span data-ttu-id="6c5b8-110">Type de données :</span><span class="sxs-lookup"><span data-stu-id="6c5b8-110">Data type:</span></span>  <br/> |<span data-ttu-id="6c5b8-111">PT_NULL</span><span class="sxs-lookup"><span data-stu-id="6c5b8-111">PT_NULL</span></span>  <br/> |
|<span data-ttu-id="6c5b8-112">Domaine :</span><span class="sxs-lookup"><span data-stu-id="6c5b8-112">Area:</span></span>  <br/> |<span data-ttu-id="6c5b8-113">Courant</span><span class="sxs-lookup"><span data-stu-id="6c5b8-113">Common</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="6c5b8-114">Remarques</span><span class="sxs-lookup"><span data-stu-id="6c5b8-114">Remarks</span></span>

<span data-ttu-id="6c5b8-115">Cette propriété permet de réserver de l’espace dans des tableaux de structures [SPropValue.](spropvalue.md)</span><span class="sxs-lookup"><span data-stu-id="6c5b8-115">This property is used to reserve space in arrays of [SPropValue](spropvalue.md) structures.</span></span> <span data-ttu-id="6c5b8-116">Il est utilisé dans un tableau de structures [SPropTagArray](sproptagarray.md) pour indiquer à la méthode de réserver de l’espace dans le tableau renvoyé de structures **SPropValue.**</span><span class="sxs-lookup"><span data-stu-id="6c5b8-116">It is used in an array of [SPropTagArray](sproptagarray.md) structures to tell the method to reserve space in the returned array of **SPropValue** structures.</span></span> <span data-ttu-id="6c5b8-117">Cela permet de remplir les propriétés calculées de manière peu coûteuse.</span><span class="sxs-lookup"><span data-stu-id="6c5b8-117">This allows for computed properties to be filled in an inexpensive way.</span></span> 
  
<span data-ttu-id="6c5b8-118">Pour plus d’informations, voir [Vue d’ensemble du type de propriété MAPI.](mapi-property-type-overview.md)</span><span class="sxs-lookup"><span data-stu-id="6c5b8-118">For more information, see [MAPI Property Type Overview](mapi-property-type-overview.md).</span></span>
  
## <a name="related-resources"></a><span data-ttu-id="6c5b8-119">Ressources connexes</span><span class="sxs-lookup"><span data-stu-id="6c5b8-119">Related resources</span></span>

### <a name="protocol-specifications"></a><span data-ttu-id="6c5b8-120">Spécifications de protocole</span><span class="sxs-lookup"><span data-stu-id="6c5b8-120">Protocol specifications</span></span>

<span data-ttu-id="6c5b8-121">[[MS-OXOCNTC]](https://msdn.microsoft.com/library/9b636532-9150-4836-9635-9c9b756c9ccf%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="6c5b8-121">[[MS-OXOCNTC]](https://msdn.microsoft.com/library/9b636532-9150-4836-9635-9c9b756c9ccf%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="6c5b8-122">Spécifie les propriétés et opérations autorisées sur les contacts et les listes de distribution personnelles.</span><span class="sxs-lookup"><span data-stu-id="6c5b8-122">Specifies the properties and operations that are permissible on contacts and personal distribution lists.</span></span>
    
### <a name="header-files"></a><span data-ttu-id="6c5b8-123">Fichiers d’en-tête</span><span class="sxs-lookup"><span data-stu-id="6c5b8-123">Header files</span></span>

<span data-ttu-id="6c5b8-124">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="6c5b8-124">Mapidefs.h</span></span>
  
> <span data-ttu-id="6c5b8-125">Fournit des définitions de type de données.</span><span class="sxs-lookup"><span data-stu-id="6c5b8-125">Provides data type definitions.</span></span>
    
<span data-ttu-id="6c5b8-126">Mapitags.h</span><span class="sxs-lookup"><span data-stu-id="6c5b8-126">Mapitags.h</span></span>
  
> <span data-ttu-id="6c5b8-127">Contient les définitions des propriétés répertoriées en tant que propriétés associées.</span><span class="sxs-lookup"><span data-stu-id="6c5b8-127">Contains definitions of properties listed as associated properties.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="6c5b8-128">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="6c5b8-128">See also</span></span>



[<span data-ttu-id="6c5b8-129">Propriétés MAPI</span><span class="sxs-lookup"><span data-stu-id="6c5b8-129">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="6c5b8-130">Propriétés canoniques MAPI</span><span class="sxs-lookup"><span data-stu-id="6c5b8-130">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="6c5b8-131">Mappage des noms de propriétés canoniques aux noms MAPI</span><span class="sxs-lookup"><span data-stu-id="6c5b8-131">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="6c5b8-132">Mappage des noms MAPI aux noms de propriétés canoniques</span><span class="sxs-lookup"><span data-stu-id="6c5b8-132">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

