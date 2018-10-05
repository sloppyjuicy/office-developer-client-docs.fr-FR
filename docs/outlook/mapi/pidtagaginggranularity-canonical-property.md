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
description: Dernière modification le 9 mars 2015
ms.openlocfilehash: b4006b62758b32598a64eaa4eb333c7ce5b12605
ms.sourcegitcommit: ef717c65d8dd41ababffb01eafc443c79950aed4
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 10/04/2018
ms.locfileid: "25390435"
---
# <a name="pidtagaginggranularity-canonical-property"></a><span data-ttu-id="3427a-103">Propriété canonique PidTagAgingGranularity</span><span class="sxs-lookup"><span data-stu-id="3427a-103">PidTagAgingGranularity Canonical Property</span></span>

  
  
<span data-ttu-id="3427a-104">**S’applique à** : Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="3427a-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="3427a-105">Représente l’unité de temps qui sert à déterminer la durée pendant laquelle qu'un élément est conservée dans un dossier avant de l’élément est archivé.</span><span class="sxs-lookup"><span data-stu-id="3427a-105">Represents the unit of time that is used in determining the length of time an item remains in a folder before the item is archived.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="3427a-106">Propriétés associées :</span><span class="sxs-lookup"><span data-stu-id="3427a-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="3427a-107">PR_AGING_GRANULARITY</span><span class="sxs-lookup"><span data-stu-id="3427a-107">PR_AGING_GRANULARITY</span></span>  <br/> |
|<span data-ttu-id="3427a-108">Identificateur :</span><span class="sxs-lookup"><span data-stu-id="3427a-108">Identifier:</span></span>  <br/> |<span data-ttu-id="3427a-109">0x36EE</span><span class="sxs-lookup"><span data-stu-id="3427a-109">0x36EE</span></span>  <br/> |
|<span data-ttu-id="3427a-110">Type de données :</span><span class="sxs-lookup"><span data-stu-id="3427a-110">Data type:</span></span>  <br/> |<span data-ttu-id="3427a-111">PT_LONG</span><span class="sxs-lookup"><span data-stu-id="3427a-111">PT_LONG</span></span>  <br/> |
|<span data-ttu-id="3427a-112">Domaine :</span><span class="sxs-lookup"><span data-stu-id="3427a-112">Area:</span></span>  <br/> |<span data-ttu-id="3427a-113">Divers</span><span class="sxs-lookup"><span data-stu-id="3427a-113">Miscellaneous</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="3427a-114">Remarques</span><span class="sxs-lookup"><span data-stu-id="3427a-114">Remarks</span></span>

<span data-ttu-id="3427a-115">Les valeurs possibles de **PR_AGING_GRANULARITY** peuvent être une des options suivantes.</span><span class="sxs-lookup"><span data-stu-id="3427a-115">The possible values for **PR_AGING_GRANULARITY** can be one of the following.</span></span> 
  
|<span data-ttu-id="3427a-116">**Nom**</span><span class="sxs-lookup"><span data-stu-id="3427a-116">**Name**</span></span>|<span data-ttu-id="3427a-117">**Valeur**</span><span class="sxs-lookup"><span data-stu-id="3427a-117">**Value**</span></span>|<span data-ttu-id="3427a-118">**Description**</span><span class="sxs-lookup"><span data-stu-id="3427a-118">**Description**</span></span>|
|:-----|:-----|:-----|
|<span data-ttu-id="3427a-119">**AG_MONTHS**</span><span class="sxs-lookup"><span data-stu-id="3427a-119">**AG_MONTHS**</span></span> <br/> |<span data-ttu-id="3427a-120">0</span><span class="sxs-lookup"><span data-stu-id="3427a-120">0</span></span>  <br/> |<span data-ttu-id="3427a-121">**PR_AGING_PERIOD** est défini dans le nombre de mois.</span><span class="sxs-lookup"><span data-stu-id="3427a-121">**PR_AGING_PERIOD** is defined in number of months.</span></span>  <br/> |
|<span data-ttu-id="3427a-122">**AG_WEEKS**</span><span class="sxs-lookup"><span data-stu-id="3427a-122">**AG_WEEKS**</span></span> <br/> |<span data-ttu-id="3427a-123">1</span><span class="sxs-lookup"><span data-stu-id="3427a-123">1</span></span>  <br/> |<span data-ttu-id="3427a-124">**PR_AGING_PERIOD** est défini dans le nombre de semaines.</span><span class="sxs-lookup"><span data-stu-id="3427a-124">**PR_AGING_PERIOD** is defined in number of weeks.</span></span>  <br/> |
|<span data-ttu-id="3427a-125">**AG_DAYS**</span><span class="sxs-lookup"><span data-stu-id="3427a-125">**AG_DAYS**</span></span> <br/> |<span data-ttu-id="3427a-126">2</span><span class="sxs-lookup"><span data-stu-id="3427a-126">2</span></span>  <br/> |<span data-ttu-id="3427a-127">**PR_AGING_PERIOD** est défini dans le nombre de jours.</span><span class="sxs-lookup"><span data-stu-id="3427a-127">**PR_AGING_PERIOD** is defined in number of days.</span></span>  <br/> |
   
<span data-ttu-id="3427a-128">La durée pendant laquelle un élément est conservée dans un dossier avant de l’élément est archivé est déterminée par les deux propriétés, [PR_AGING_PERIOD](pidtagagingperiod-canonical-property.md) et **PR_AGING_GRANULARITY**.</span><span class="sxs-lookup"><span data-stu-id="3427a-128">The length of time that an item remains in a folder before the item is archived is determined by two properties, [PR_AGING_PERIOD](pidtagagingperiod-canonical-property.md) and **PR_AGING_GRANULARITY**.</span></span> <span data-ttu-id="3427a-129">**PR_AGING_PERIOD** représente le nombre d’unités de temps que l’élément reste dans le dossier avant leur archivage.</span><span class="sxs-lookup"><span data-stu-id="3427a-129">**PR_AGING_PERIOD** represents the number of time units that the item remains in the folder before it is archived.</span></span> 
  
## <a name="related-resources"></a><span data-ttu-id="3427a-130">Ressources connexes</span><span class="sxs-lookup"><span data-stu-id="3427a-130">Related resources</span></span>

### <a name="protocol-specifications"></a><span data-ttu-id="3427a-131">Spécifications du protocole</span><span class="sxs-lookup"><span data-stu-id="3427a-131">Protocol specifications</span></span>

<span data-ttu-id="3427a-132">[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="3427a-132">[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="3427a-133">Fournit des références aux spécifications du protocole Exchange Server associées.</span><span class="sxs-lookup"><span data-stu-id="3427a-133">Provides references to related Exchange Server protocol specifications.</span></span>
    
<span data-ttu-id="3427a-134">[[MS-OXCFXICS]](https://msdn.microsoft.com/library/b9752f3d-d50d-44b8-9e6b-608a117c8532%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="3427a-134">[[MS-OXCFXICS]](https://msdn.microsoft.com/library/b9752f3d-d50d-44b8-9e6b-608a117c8532%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="3427a-135">Définit les structures de base de données qui sont utilisés dans les opérations à distance.</span><span class="sxs-lookup"><span data-stu-id="3427a-135">Defines the basic data structures that are used in remote operations.</span></span>
    
<span data-ttu-id="3427a-136">[[MS-OXOMSG]](https://msdn.microsoft.com/library/daa9120f-f325-4afb-a738-28f91049ab3c%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="3427a-136">[[MS-OXOMSG]](https://msdn.microsoft.com/library/daa9120f-f325-4afb-a738-28f91049ab3c%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="3427a-137">Spécifie les propriétés et les opérations qui sont autorisées pour les objets de message électronique.</span><span class="sxs-lookup"><span data-stu-id="3427a-137">Specifies the properties and operations that are permissible for email message objects.</span></span>
    
### <a name="header-files"></a><span data-ttu-id="3427a-138">Fichiers d’en-tête</span><span class="sxs-lookup"><span data-stu-id="3427a-138">Header files</span></span>

<span data-ttu-id="3427a-139">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="3427a-139">Mapidefs.h</span></span>
  
> <span data-ttu-id="3427a-140">Fournit des définitions de type de données.</span><span class="sxs-lookup"><span data-stu-id="3427a-140">Provides data type definitions.</span></span>
    
<span data-ttu-id="3427a-141">MAPITAGS.h</span><span class="sxs-lookup"><span data-stu-id="3427a-141">Mapitags.h</span></span>
  
> <span data-ttu-id="3427a-142">Contient les définitions des propriétés répertoriées en tant que d’autres noms.</span><span class="sxs-lookup"><span data-stu-id="3427a-142">Contains definitions of properties listed as alternate names.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="3427a-143">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="3427a-143">See also</span></span>



[<span data-ttu-id="3427a-144">Propriétés MAPI</span><span class="sxs-lookup"><span data-stu-id="3427a-144">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="3427a-145">Propriétés canoniques MAPI</span><span class="sxs-lookup"><span data-stu-id="3427a-145">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="3427a-146">Mappage des noms de propriétés canoniques aux noms MAPI</span><span class="sxs-lookup"><span data-stu-id="3427a-146">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="3427a-147">Mappage des noms MAPI aux noms de propriétés canoniques</span><span class="sxs-lookup"><span data-stu-id="3427a-147">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

