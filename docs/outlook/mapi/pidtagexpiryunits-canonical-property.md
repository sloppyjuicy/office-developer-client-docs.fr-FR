---
title: Propriété canonique PidTagExpiryUnits
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- PidTagExpiryUnits
api_type:
- HeaderDef
ms.assetid: f6a1ca22-cf4c-4e59-8846-6bd937fa8f6e
description: Dernière modification le 9 mars 2015
ms.openlocfilehash: 8e8deb67990ce25b10a3b0fc1d373f635f958013
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32316407"
---
# <a name="pidtagexpiryunits-canonical-property"></a><span data-ttu-id="30749-103">Propriété canonique PidTagExpiryUnits</span><span class="sxs-lookup"><span data-stu-id="30749-103">PidTagExpiryUnits Canonical Property</span></span>

  
  
<span data-ttu-id="30749-104">**S’applique à** : Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="30749-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="30749-105">Décrit l’unité de temps pendant **PR_EXPIRY_NUMBER** ([PidTagExpiryNumber](pidtagexpirynumber-canonical-property.md)) multiplie la propriété.</span><span class="sxs-lookup"><span data-stu-id="30749-105">Describes the unit of time when the **PR_EXPIRY_NUMBER** ([PidTagExpiryNumber](pidtagexpirynumber-canonical-property.md)) property multiplies.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="30749-106">Propriétés associées :</span><span class="sxs-lookup"><span data-stu-id="30749-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="30749-107">PR_EXPIRY_UNITS</span><span class="sxs-lookup"><span data-stu-id="30749-107">PR_EXPIRY_UNITS</span></span>  <br/> |
|<span data-ttu-id="30749-108">Identificateur :</span><span class="sxs-lookup"><span data-stu-id="30749-108">Identifier:</span></span>  <br/> |<span data-ttu-id="30749-109">0x3FEE</span><span class="sxs-lookup"><span data-stu-id="30749-109">0x3FEE</span></span>  <br/> |
|<span data-ttu-id="30749-110">Type de données :</span><span class="sxs-lookup"><span data-stu-id="30749-110">Data type:</span></span>  <br/> |<span data-ttu-id="30749-111">PT_LONG</span><span class="sxs-lookup"><span data-stu-id="30749-111">PT_LONG</span></span>  <br/> |
|<span data-ttu-id="30749-112">Domaine :</span><span class="sxs-lookup"><span data-stu-id="30749-112">Area:</span></span>  <br/> |<span data-ttu-id="30749-113">État MAPI</span><span class="sxs-lookup"><span data-stu-id="30749-113">MAPI status</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="30749-114">Remarques</span><span class="sxs-lookup"><span data-stu-id="30749-114">Remarks</span></span>

<span data-ttu-id="30749-115">Si elle est définie, cette propriété doit avoir l’une des valeurs suivantes :</span><span class="sxs-lookup"><span data-stu-id="30749-115">This property, if set, must be one of the following values:</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="30749-116">PidTagExpiryUnits</span><span class="sxs-lookup"><span data-stu-id="30749-116">PidTagExpiryUnits</span></span>  <br/> |<span data-ttu-id="30749-117">Description (TimeOf)</span><span class="sxs-lookup"><span data-stu-id="30749-117">Description (TimeOf)</span></span>  <br/> |
|<span data-ttu-id="30749-118">0x00000000</span><span class="sxs-lookup"><span data-stu-id="30749-118">0x00000000</span></span>  <br/> |<span data-ttu-id="30749-119">Minutes, par exemple 60 secondes</span><span class="sxs-lookup"><span data-stu-id="30749-119">Minutes, for example 60 seconds</span></span>  <br/> |
|<span data-ttu-id="30749-120">0x00000001</span><span class="sxs-lookup"><span data-stu-id="30749-120">0x00000001</span></span>  <br/> |<span data-ttu-id="30749-121">Heures, par exemple 60 x 60 secondes</span><span class="sxs-lookup"><span data-stu-id="30749-121">Hours, for example 60x60 seconds</span></span>  <br/> |
|<span data-ttu-id="30749-122">0x00000002</span><span class="sxs-lookup"><span data-stu-id="30749-122">0x00000002</span></span>  <br/> |<span data-ttu-id="30749-123">Jour, par exemple 24 x 60 x 60 secondes</span><span class="sxs-lookup"><span data-stu-id="30749-123">Day, for example 24x60x60 seconds</span></span>  <br/> |
|<span data-ttu-id="30749-124">0x00000003</span><span class="sxs-lookup"><span data-stu-id="30749-124">0x00000003</span></span>  <br/> |<span data-ttu-id="30749-125">Semaine, par exemple 7 x 24 x 60 x 60 secondes</span><span class="sxs-lookup"><span data-stu-id="30749-125">Week, for example 7x24x60x60 seconds</span></span>  <br/> |
   
## <a name="related-resources"></a><span data-ttu-id="30749-126">Ressources connexes</span><span class="sxs-lookup"><span data-stu-id="30749-126">Related resources</span></span>

### <a name="protocol-specifications"></a><span data-ttu-id="30749-127">Spécifications de protocole</span><span class="sxs-lookup"><span data-stu-id="30749-127">Protocol specifications</span></span>

<span data-ttu-id="30749-128">[[MS-OXOMSG]](https://msdn.microsoft.com/library/daa9120f-f325-4afb-a738-28f91049ab3c%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="30749-128">[[MS-OXOMSG]](https://msdn.microsoft.com/library/daa9120f-f325-4afb-a738-28f91049ab3c%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="30749-129">Spécifie les propriétés et opérations autorisées pour les objets de message électronique.</span><span class="sxs-lookup"><span data-stu-id="30749-129">Specifies the properties and operations that are permissible for email message objects.</span></span>
    
### <a name="header-files"></a><span data-ttu-id="30749-130">Fichiers d’en-tête</span><span class="sxs-lookup"><span data-stu-id="30749-130">Header files</span></span>

<span data-ttu-id="30749-131">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="30749-131">Mapidefs.h</span></span>
  
> <span data-ttu-id="30749-132">Fournit des définitions de type de données.</span><span class="sxs-lookup"><span data-stu-id="30749-132">Provides data type definitions.</span></span>
    
<span data-ttu-id="30749-133">Mapitags.h</span><span class="sxs-lookup"><span data-stu-id="30749-133">Mapitags.h</span></span>
  
> <span data-ttu-id="30749-134">Contient les définitions des propriétés répertoriées en tant que noms de remplacement.</span><span class="sxs-lookup"><span data-stu-id="30749-134">Contains definitions of properties listed as alternate names.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="30749-135">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="30749-135">See also</span></span>



[<span data-ttu-id="30749-136">Propriétés MAPI</span><span class="sxs-lookup"><span data-stu-id="30749-136">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="30749-137">Propriétés canoniques MAPI</span><span class="sxs-lookup"><span data-stu-id="30749-137">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="30749-138">Mappage des noms de propriétés canoniques aux noms MAPI</span><span class="sxs-lookup"><span data-stu-id="30749-138">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="30749-139">Mappage des noms MAPI aux noms de propriétés canoniques</span><span class="sxs-lookup"><span data-stu-id="30749-139">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

