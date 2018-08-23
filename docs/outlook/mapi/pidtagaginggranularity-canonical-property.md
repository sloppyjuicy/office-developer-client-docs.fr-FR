---
title: Propriété canonique PidTagAgingGranularity
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- PidTagAgingGranularity
api_type:
- HeaderDef
ms.assetid: b79ec87d-d97c-4e6c-899b-78ebf1b485a7
description: Dernière modification le 09 mars 2015
ms.openlocfilehash: c1b5b36c3a05ef17e319ef236b032b7d07ce8fa8
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/23/2018
ms.locfileid: "22589419"
---
# <a name="pidtagaginggranularity-canonical-property"></a><span data-ttu-id="5ab86-103">Propriété canonique PidTagAgingGranularity</span><span class="sxs-lookup"><span data-stu-id="5ab86-103">PidTagAgingGranularity Canonical Property</span></span>

  
  
<span data-ttu-id="5ab86-104">**S’applique à**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="5ab86-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="5ab86-105">Représente l’unité de temps qui sert à déterminer la durée pendant laquelle qu'un élément est conservée dans un dossier avant de l’élément est archivé.</span><span class="sxs-lookup"><span data-stu-id="5ab86-105">Represents the unit of time that is used in determining the length of time an item remains in a folder before the item is archived.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="5ab86-106">Propriétés associées :</span><span class="sxs-lookup"><span data-stu-id="5ab86-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="5ab86-107">PR_AGING_GRANULARITY</span><span class="sxs-lookup"><span data-stu-id="5ab86-107">PR_AGING_GRANULARITY</span></span>  <br/> |
|<span data-ttu-id="5ab86-108">Identificateur :</span><span class="sxs-lookup"><span data-stu-id="5ab86-108">Identifier:</span></span>  <br/> |<span data-ttu-id="5ab86-109">0x36EE</span><span class="sxs-lookup"><span data-stu-id="5ab86-109">0x36EE</span></span>  <br/> |
|<span data-ttu-id="5ab86-110">Type de données :</span><span class="sxs-lookup"><span data-stu-id="5ab86-110">Data type:</span></span>  <br/> |<span data-ttu-id="5ab86-111">PT_LONG</span><span class="sxs-lookup"><span data-stu-id="5ab86-111">PT_LONG</span></span>  <br/> |
|<span data-ttu-id="5ab86-112">Domaine :</span><span class="sxs-lookup"><span data-stu-id="5ab86-112">Area:</span></span>  <br/> |<span data-ttu-id="5ab86-113">Divers</span><span class="sxs-lookup"><span data-stu-id="5ab86-113">Miscellaneous</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="5ab86-114">Remarques</span><span class="sxs-lookup"><span data-stu-id="5ab86-114">Remarks</span></span>

<span data-ttu-id="5ab86-115">Les valeurs possibles de **PR_AGING_GRANULARITY** peuvent être une des options suivantes.</span><span class="sxs-lookup"><span data-stu-id="5ab86-115">The possible values for **PR_AGING_GRANULARITY** can be one of the following.</span></span> 
  
|<span data-ttu-id="5ab86-116">**Nom**</span><span class="sxs-lookup"><span data-stu-id="5ab86-116">**Name**</span></span>|<span data-ttu-id="5ab86-117">**Valeur**</span><span class="sxs-lookup"><span data-stu-id="5ab86-117">**Value**</span></span>|<span data-ttu-id="5ab86-118">**Description**</span><span class="sxs-lookup"><span data-stu-id="5ab86-118">**Description**</span></span>|
|:-----|:-----|:-----|
|<span data-ttu-id="5ab86-119">**AG_MONTHS**</span><span class="sxs-lookup"><span data-stu-id="5ab86-119">**AG_MONTHS**</span></span> <br/> |<span data-ttu-id="5ab86-120">0</span><span class="sxs-lookup"><span data-stu-id="5ab86-120">0</span></span>  <br/> |<span data-ttu-id="5ab86-121">**PR_AGING_PERIOD** est défini dans le nombre de mois.</span><span class="sxs-lookup"><span data-stu-id="5ab86-121">**PR_AGING_PERIOD** is defined in number of months.</span></span>  <br/> |
|<span data-ttu-id="5ab86-122">**AG_WEEKS**</span><span class="sxs-lookup"><span data-stu-id="5ab86-122">**AG_WEEKS**</span></span> <br/> |<span data-ttu-id="5ab86-123">1</span><span class="sxs-lookup"><span data-stu-id="5ab86-123">1</span></span>  <br/> |<span data-ttu-id="5ab86-124">**PR_AGING_PERIOD** est défini dans le nombre de semaines.</span><span class="sxs-lookup"><span data-stu-id="5ab86-124">**PR_AGING_PERIOD** is defined in number of weeks.</span></span>  <br/> |
|<span data-ttu-id="5ab86-125">**AG_DAYS**</span><span class="sxs-lookup"><span data-stu-id="5ab86-125">**AG_DAYS**</span></span> <br/> |<span data-ttu-id="5ab86-126">2</span><span class="sxs-lookup"><span data-stu-id="5ab86-126">2</span></span>  <br/> |<span data-ttu-id="5ab86-127">**PR_AGING_PERIOD** est défini dans le nombre de jours.</span><span class="sxs-lookup"><span data-stu-id="5ab86-127">**PR_AGING_PERIOD** is defined in number of days.</span></span>  <br/> |
   
<span data-ttu-id="5ab86-128">La durée pendant laquelle un élément est conservée dans un dossier avant de l’élément est archivé est déterminée par les deux propriétés, [PR_AGING_PERIOD](pidtagagingperiod-canonical-property.md) et **PR_AGING_GRANULARITY**.</span><span class="sxs-lookup"><span data-stu-id="5ab86-128">The length of time that an item remains in a folder before the item is archived is determined by two properties, [PR_AGING_PERIOD](pidtagagingperiod-canonical-property.md) and **PR_AGING_GRANULARITY**.</span></span> <span data-ttu-id="5ab86-129">**PR_AGING_PERIOD** représente le nombre d’unités de temps que l’élément reste dans le dossier avant leur archivage.</span><span class="sxs-lookup"><span data-stu-id="5ab86-129">**PR_AGING_PERIOD** represents the number of time units that the item remains in the folder before it is archived.</span></span> 
  
## <a name="related-resources"></a><span data-ttu-id="5ab86-130">Ressources connexes</span><span class="sxs-lookup"><span data-stu-id="5ab86-130">Related resources</span></span>

### <a name="protocol-specifications"></a><span data-ttu-id="5ab86-131">Spécifications du protocole</span><span class="sxs-lookup"><span data-stu-id="5ab86-131">Protocol specifications</span></span>

<span data-ttu-id="5ab86-132">[[MS-OXPROPS]](http://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="5ab86-132">[[MS-OXPROPS]](http://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="5ab86-133">Fournit des références aux spécifications du protocole Exchange Server associées.</span><span class="sxs-lookup"><span data-stu-id="5ab86-133">Provides references to related Exchange Server protocol specifications.</span></span>
    
<span data-ttu-id="5ab86-134">[[MS-OXCFXICS]](http://msdn.microsoft.com/library/b9752f3d-d50d-44b8-9e6b-608a117c8532%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="5ab86-134">[[MS-OXCFXICS]](http://msdn.microsoft.com/library/b9752f3d-d50d-44b8-9e6b-608a117c8532%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="5ab86-135">Définit les structures de base de données qui sont utilisés dans les opérations à distance.</span><span class="sxs-lookup"><span data-stu-id="5ab86-135">Defines the basic data structures that are used in remote operations.</span></span>
    
<span data-ttu-id="5ab86-136">[[MS-OXOMSG]](http://msdn.microsoft.com/library/daa9120f-f325-4afb-a738-28f91049ab3c%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="5ab86-136">[[MS-OXOMSG]](http://msdn.microsoft.com/library/daa9120f-f325-4afb-a738-28f91049ab3c%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="5ab86-137">Spécifie les propriétés et les opérations qui sont autorisées pour les objets de message électronique.</span><span class="sxs-lookup"><span data-stu-id="5ab86-137">Specifies the properties and operations that are permissible for email message objects.</span></span>
    
### <a name="header-files"></a><span data-ttu-id="5ab86-138">Fichiers d’en-tête</span><span class="sxs-lookup"><span data-stu-id="5ab86-138">Header files</span></span>

<span data-ttu-id="5ab86-139">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="5ab86-139">Mapidefs.h</span></span>
  
> <span data-ttu-id="5ab86-140">Fournit des définitions de type de données.</span><span class="sxs-lookup"><span data-stu-id="5ab86-140">Provides data type definitions.</span></span>
    
<span data-ttu-id="5ab86-141">MAPITAGS.h</span><span class="sxs-lookup"><span data-stu-id="5ab86-141">Mapitags.h</span></span>
  
> <span data-ttu-id="5ab86-142">Contient les définitions des propriétés répertoriées en tant que d’autres noms.</span><span class="sxs-lookup"><span data-stu-id="5ab86-142">Contains definitions of properties listed as alternate names.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="5ab86-143">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="5ab86-143">See also</span></span>



[<span data-ttu-id="5ab86-144">Propriétés MAPI</span><span class="sxs-lookup"><span data-stu-id="5ab86-144">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="5ab86-145">Propriétés canoniques MAPI</span><span class="sxs-lookup"><span data-stu-id="5ab86-145">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="5ab86-146">Mappage des noms de propriétés canoniques aux noms MAPI</span><span class="sxs-lookup"><span data-stu-id="5ab86-146">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="5ab86-147">Mappage des noms MAPI aux noms de propriétés canoniques</span><span class="sxs-lookup"><span data-stu-id="5ab86-147">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

