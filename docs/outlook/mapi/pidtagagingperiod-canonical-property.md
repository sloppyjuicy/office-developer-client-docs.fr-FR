---
title: Propriété canonique PidTagAgingPeriod
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- PidTagAgingPeriod
api_type:
- HeaderDef
ms.assetid: 762020d1-4bc8-d60d-0f66-3929aae24bfb
description: Dernière modification le 09 mars 2015
ms.openlocfilehash: caaa01982ff9e66fe7e17df4eaf37dcd25281d4e
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/23/2018
ms.locfileid: "22569553"
---
# <a name="pidtagagingperiod-canonical-property"></a><span data-ttu-id="0873e-103">Propriété canonique PidTagAgingPeriod</span><span class="sxs-lookup"><span data-stu-id="0873e-103">PidTagAgingPeriod Canonical Property</span></span>

  
  
<span data-ttu-id="0873e-104">**S’applique à**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="0873e-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="0873e-105">Représente le nombre d’unités de temps qui sont utilisés pour déterminer la durée pendant laquelle un élément est conservée dans un dossier avant de l’élément est archivé.</span><span class="sxs-lookup"><span data-stu-id="0873e-105">Represents the number of time units that are used to determine the length of time that an item remains in a folder before the item is archived.</span></span>
  
## 

|||
|:-----|:-----|
|<span data-ttu-id="0873e-106">Propriétés associées :</span><span class="sxs-lookup"><span data-stu-id="0873e-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="0873e-107">PR_AGING_PERIOD</span><span class="sxs-lookup"><span data-stu-id="0873e-107">PR_AGING_PERIOD</span></span>  <br/> |
|<span data-ttu-id="0873e-108">Identificateur :</span><span class="sxs-lookup"><span data-stu-id="0873e-108">Identifier:</span></span>  <br/> |<span data-ttu-id="0873e-109">0x36EC</span><span class="sxs-lookup"><span data-stu-id="0873e-109">0x36EC</span></span>  <br/> |
|<span data-ttu-id="0873e-110">Type de propriété :</span><span class="sxs-lookup"><span data-stu-id="0873e-110">Property type:</span></span>  <br/> |<span data-ttu-id="0873e-111">PT_LONG</span><span class="sxs-lookup"><span data-stu-id="0873e-111">PT_LONG</span></span>  <br/> |
|<span data-ttu-id="0873e-112">Domaine :</span><span class="sxs-lookup"><span data-stu-id="0873e-112">Area:</span></span>  <br/> |<span data-ttu-id="0873e-113">Divers</span><span class="sxs-lookup"><span data-stu-id="0873e-113">Miscellaneous</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="0873e-114">Remarques</span><span class="sxs-lookup"><span data-stu-id="0873e-114">Remarks</span></span>

<span data-ttu-id="0873e-115">La durée pendant laquelle un élément est conservée dans un dossier avant de l’élément est archivé est déterminée par les deux propriétés, **PR_AGING_PERIOD** et **[PR_AGING_GRANULARITY](pidtagaginggranularity-canonical-property.md)**.</span><span class="sxs-lookup"><span data-stu-id="0873e-115">The length of time that an item remains in a folder before the item is archived is determined by two properties, **PR_AGING_PERIOD** and **[PR_AGING_GRANULARITY](pidtagaginggranularity-canonical-property.md)**.</span></span> <span data-ttu-id="0873e-116">**PR_AGING_GRANULARITY** représente l’unité de temps dans laquelle **PR_AGING_PERIOD** est exprimé, lors de la détermination de cette durée.</span><span class="sxs-lookup"><span data-stu-id="0873e-116">**PR_AGING_GRANULARITY** represents the time unit in which **PR_AGING_PERIOD** is expressed, when determining this length of time.</span></span> 
  
<span data-ttu-id="0873e-117">Les valeurs possibles de **PR_AGING_GRANULARITY** peuvent être une des options suivantes.</span><span class="sxs-lookup"><span data-stu-id="0873e-117">The possible values for **PR_AGING_GRANULARITY** can be one of the following.</span></span> 
  
****

|<span data-ttu-id="0873e-118">**Nom**</span><span class="sxs-lookup"><span data-stu-id="0873e-118">**Name**</span></span>|<span data-ttu-id="0873e-119">**Description**</span><span class="sxs-lookup"><span data-stu-id="0873e-119">**Description**</span></span>|
|:-----|:-----|
|<span data-ttu-id="0873e-120">**AG_MONTHS**</span><span class="sxs-lookup"><span data-stu-id="0873e-120">**AG_MONTHS**</span></span> <br/> |<span data-ttu-id="0873e-121">**PR_AGING_PERIOD** est défini dans le nombre de mois.</span><span class="sxs-lookup"><span data-stu-id="0873e-121">**PR_AGING_PERIOD** is defined in number of months.</span></span>  <br/> |
|<span data-ttu-id="0873e-122">**AG_WEEKS**</span><span class="sxs-lookup"><span data-stu-id="0873e-122">**AG_WEEKS**</span></span> <br/> |<span data-ttu-id="0873e-123">**PR_AGING_PERIOD** est défini dans le nombre de semaines.</span><span class="sxs-lookup"><span data-stu-id="0873e-123">**PR_AGING_PERIOD** is defined in number of weeks.</span></span>  <br/> |
|<span data-ttu-id="0873e-124">**AG_DAYS**</span><span class="sxs-lookup"><span data-stu-id="0873e-124">**AG_DAYS**</span></span> <br/> |<span data-ttu-id="0873e-125">**PR_AGING_PERIOD** est défini dans le nombre de jours.</span><span class="sxs-lookup"><span data-stu-id="0873e-125">**PR_AGING_PERIOD** is defined in number of days.</span></span>  <br/> |
   
<span data-ttu-id="0873e-126">Par exemple, si un archives de dossier est un élément uniquement une fois que l’élément a été dans le dossier pour les deux semaines, puis **PR_AGING_GRANULARITY** **AG_WEEKS** et **PR_AGING_PERIOD** est 2.</span><span class="sxs-lookup"><span data-stu-id="0873e-126">For example, if a folder archives an item only after the item has been in the folder for two weeks, then **PR_AGING_GRANULARITY** is **AG_WEEKS** and **PR_AGING_PERIOD** is 2.</span></span> 
  
## <a name="related-resources"></a><span data-ttu-id="0873e-127">Ressources connexes</span><span class="sxs-lookup"><span data-stu-id="0873e-127">Related resources</span></span>

### <a name="protocol-specifications"></a><span data-ttu-id="0873e-128">Spécifications du protocole</span><span class="sxs-lookup"><span data-stu-id="0873e-128">Protocol specifications</span></span>

<span data-ttu-id="0873e-129">[[MS-OXPROPS]](http://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="0873e-129">[[MS-OXPROPS]](http://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="0873e-130">Fournit des définitions de jeu de propriétés.</span><span class="sxs-lookup"><span data-stu-id="0873e-130">Provides property set definitions.</span></span>
    
<span data-ttu-id="0873e-131">[[MS-OXCFXICS]](http://msdn.microsoft.com/library/b9752f3d-d50d-44b8-9e6b-608a117c8532%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="0873e-131">[[MS-OXCFXICS]](http://msdn.microsoft.com/library/b9752f3d-d50d-44b8-9e6b-608a117c8532%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="0873e-132">Définit les structures de base de données qui sont utilisés dans les opérations à distance.</span><span class="sxs-lookup"><span data-stu-id="0873e-132">Defines the basic data structures that are used in remote operations.</span></span>
    
<span data-ttu-id="0873e-133">[[MS-OXOMSG]](http://msdn.microsoft.com/library/daa9120f-f325-4afb-a738-28f91049ab3c%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="0873e-133">[[MS-OXOMSG]](http://msdn.microsoft.com/library/daa9120f-f325-4afb-a738-28f91049ab3c%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="0873e-134">Spécifie les propriétés et les opérations qui sont autorisées pour les objets de message électronique.</span><span class="sxs-lookup"><span data-stu-id="0873e-134">Specifies the properties and operations that are permitted for email message objects.</span></span>
    
### <a name="header-files"></a><span data-ttu-id="0873e-135">Fichiers d’en-tête</span><span class="sxs-lookup"><span data-stu-id="0873e-135">Header files</span></span>

<span data-ttu-id="0873e-136">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="0873e-136">Mapidefs.h</span></span>
  
> <span data-ttu-id="0873e-137">Fournit des définitions de type de données.</span><span class="sxs-lookup"><span data-stu-id="0873e-137">Provides data type definitions.</span></span>
    
<span data-ttu-id="0873e-138">MAPITAGS.h</span><span class="sxs-lookup"><span data-stu-id="0873e-138">Mapitags.h</span></span>
  
> <span data-ttu-id="0873e-139">Contient les définitions des propriétés répertoriées en tant que d’autres noms.</span><span class="sxs-lookup"><span data-stu-id="0873e-139">Contains definitions of properties listed as alternate names.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="0873e-140">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="0873e-140">See also</span></span>



[<span data-ttu-id="0873e-141">Propriétés MAPI</span><span class="sxs-lookup"><span data-stu-id="0873e-141">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="0873e-142">Propriétés canoniques MAPI</span><span class="sxs-lookup"><span data-stu-id="0873e-142">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="0873e-143">Mappage des noms de propriétés canoniques aux noms MAPI</span><span class="sxs-lookup"><span data-stu-id="0873e-143">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="0873e-144">Mappage des noms MAPI aux noms de propriétés canoniques</span><span class="sxs-lookup"><span data-stu-id="0873e-144">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

