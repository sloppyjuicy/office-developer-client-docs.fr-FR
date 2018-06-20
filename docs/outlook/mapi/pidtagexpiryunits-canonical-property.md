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
description: 'Derni�re modification�: lundi 9 mars 2015'
ms.openlocfilehash: 1c753bb84ccbfe2fa6869d56806fd042a6d60e9c
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19785971"
---
# <a name="pidtagexpiryunits-canonical-property"></a><span data-ttu-id="037ec-103">Propriété canonique PidTagExpiryUnits</span><span class="sxs-lookup"><span data-stu-id="037ec-103">PidTagExpiryUnits Canonical Property</span></span>

  
  
<span data-ttu-id="037ec-104">**S’applique à**: Outlook</span><span class="sxs-lookup"><span data-stu-id="037ec-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="037ec-105">Décrit l’unité de temps lorsque la propriété **PR_EXPIRY_NUMBER** ([PidTagExpiryNumber](pidtagexpirynumber-canonical-property.md)) multiplie.</span><span class="sxs-lookup"><span data-stu-id="037ec-105">Describes the unit of time when the **PR_EXPIRY_NUMBER** ([PidTagExpiryNumber](pidtagexpirynumber-canonical-property.md)) property multiplies.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="037ec-106">Propriétés associées :</span><span class="sxs-lookup"><span data-stu-id="037ec-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="037ec-107">PR_EXPIRY_UNITS</span><span class="sxs-lookup"><span data-stu-id="037ec-107">PR_EXPIRY_UNITS</span></span>  <br/> |
|<span data-ttu-id="037ec-108">Identificateur :</span><span class="sxs-lookup"><span data-stu-id="037ec-108">Identifier:</span></span>  <br/> |<span data-ttu-id="037ec-109">0x3FEE</span><span class="sxs-lookup"><span data-stu-id="037ec-109">0x3FEE</span></span>  <br/> |
|<span data-ttu-id="037ec-110">Type de données :</span><span class="sxs-lookup"><span data-stu-id="037ec-110">Data type:</span></span>  <br/> |<span data-ttu-id="037ec-111">PT_LONG</span><span class="sxs-lookup"><span data-stu-id="037ec-111">PT_LONG</span></span>  <br/> |
|<span data-ttu-id="037ec-112">Zone :</span><span class="sxs-lookup"><span data-stu-id="037ec-112">Area:</span></span>  <br/> |<span data-ttu-id="037ec-113">État MAPI</span><span class="sxs-lookup"><span data-stu-id="037ec-113">MAPI status</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="037ec-114">Remarques</span><span class="sxs-lookup"><span data-stu-id="037ec-114">Remarks</span></span>

<span data-ttu-id="037ec-115">Cette propriété, si la valeur, doit être une des valeurs suivantes :</span><span class="sxs-lookup"><span data-stu-id="037ec-115">This property, if set, must be one of the following values:</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="037ec-116">PidTagExpiryUnits</span><span class="sxs-lookup"><span data-stu-id="037ec-116">PidTagExpiryUnits</span></span>  <br/> |<span data-ttu-id="037ec-117">Description (heure)</span><span class="sxs-lookup"><span data-stu-id="037ec-117">Description (TimeOf)</span></span>  <br/> |
|<span data-ttu-id="037ec-118">0x00000000</span><span class="sxs-lookup"><span data-stu-id="037ec-118">0x00000000</span></span>  <br/> |<span data-ttu-id="037ec-119">Minutes, par exemple 60 secondes.</span><span class="sxs-lookup"><span data-stu-id="037ec-119">Minutes, for example 60 seconds</span></span>  <br/> |
|<span data-ttu-id="037ec-120">0x00000001</span><span class="sxs-lookup"><span data-stu-id="037ec-120">0x00000001</span></span>  <br/> |<span data-ttu-id="037ec-121">Heures, par exemple 60 x 60 secondes</span><span class="sxs-lookup"><span data-stu-id="037ec-121">Hours, for example 60x60 seconds</span></span>  <br/> |
|<span data-ttu-id="037ec-122">0x00000002</span><span class="sxs-lookup"><span data-stu-id="037ec-122">0x00000002</span></span>  <br/> |<span data-ttu-id="037ec-123">Jour, par exemple 24 x 60 x 60 secondes</span><span class="sxs-lookup"><span data-stu-id="037ec-123">Day, for example 24x60x60 seconds</span></span>  <br/> |
|<span data-ttu-id="037ec-124">0 x 00000003</span><span class="sxs-lookup"><span data-stu-id="037ec-124">0x00000003</span></span>  <br/> |<span data-ttu-id="037ec-125">Semaine, par exemple 7x24x60x60 secondes</span><span class="sxs-lookup"><span data-stu-id="037ec-125">Week, for example 7x24x60x60 seconds</span></span>  <br/> |
   
## <a name="related-resources"></a><span data-ttu-id="037ec-126">Ressources connexes</span><span class="sxs-lookup"><span data-stu-id="037ec-126">Related resources</span></span>

### <a name="protocol-specifications"></a><span data-ttu-id="037ec-127">Spécifications du protocole</span><span class="sxs-lookup"><span data-stu-id="037ec-127">Protocol specifications</span></span>

<span data-ttu-id="037ec-128">[[MS-OXOMSG]](http://msdn.microsoft.com/library/daa9120f-f325-4afb-a738-28f91049ab3c%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="037ec-128">[[MS-OXOMSG]](http://msdn.microsoft.com/library/daa9120f-f325-4afb-a738-28f91049ab3c%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="037ec-129">Spécifie les propriétés et les opérations qui sont autorisées pour les objets de message électronique.</span><span class="sxs-lookup"><span data-stu-id="037ec-129">Specifies the properties and operations that are permissible for email message objects.</span></span>
    
### <a name="header-files"></a><span data-ttu-id="037ec-130">Fichiers d’en-tête</span><span class="sxs-lookup"><span data-stu-id="037ec-130">Header files</span></span>

<span data-ttu-id="037ec-131">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="037ec-131">Mapidefs.h</span></span>
  
> <span data-ttu-id="037ec-132">Fournit des définitions de type de données.</span><span class="sxs-lookup"><span data-stu-id="037ec-132">Provides data type definitions.</span></span>
    
<span data-ttu-id="037ec-133">MAPITAGS.h</span><span class="sxs-lookup"><span data-stu-id="037ec-133">Mapitags.h</span></span>
  
> <span data-ttu-id="037ec-134">Contient les définitions des propriétés répertoriées en tant que d’autres noms.</span><span class="sxs-lookup"><span data-stu-id="037ec-134">Contains definitions of properties listed as alternate names.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="037ec-135">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="037ec-135">See also</span></span>



[<span data-ttu-id="037ec-136">Propriétés MAPI</span><span class="sxs-lookup"><span data-stu-id="037ec-136">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="037ec-137">Propriétés canoniques MAPI</span><span class="sxs-lookup"><span data-stu-id="037ec-137">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="037ec-138">Mappage de noms de propriété canonique aux noms MAPI</span><span class="sxs-lookup"><span data-stu-id="037ec-138">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="037ec-139">Mappage de noms MAPI pour les noms de propriété canonique</span><span class="sxs-lookup"><span data-stu-id="037ec-139">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

