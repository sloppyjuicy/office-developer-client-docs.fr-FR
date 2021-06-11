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
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32325584"
---
# <a name="pidtagaginggranularity-canonical-property"></a><span data-ttu-id="25fc1-103">Propriété canonique PidTagAgingGranularity</span><span class="sxs-lookup"><span data-stu-id="25fc1-103">PidTagAgingGranularity Canonical Property</span></span>

  
  
<span data-ttu-id="25fc1-104">**S’applique à** : Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="25fc1-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="25fc1-105">Représente l’unité de temps utilisée pour déterminer la durée pendant qu’un élément reste dans un dossier avant l’archivage de l’élément.</span><span class="sxs-lookup"><span data-stu-id="25fc1-105">Represents the unit of time that is used in determining the length of time an item remains in a folder before the item is archived.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="25fc1-106">Propriétés associées :</span><span class="sxs-lookup"><span data-stu-id="25fc1-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="25fc1-107">PR_AGING_GRANULARITY</span><span class="sxs-lookup"><span data-stu-id="25fc1-107">PR_AGING_GRANULARITY</span></span>  <br/> |
|<span data-ttu-id="25fc1-108">Identificateur :</span><span class="sxs-lookup"><span data-stu-id="25fc1-108">Identifier:</span></span>  <br/> |<span data-ttu-id="25fc1-109">0x36EE</span><span class="sxs-lookup"><span data-stu-id="25fc1-109">0x36EE</span></span>  <br/> |
|<span data-ttu-id="25fc1-110">Type de données :</span><span class="sxs-lookup"><span data-stu-id="25fc1-110">Data type:</span></span>  <br/> |<span data-ttu-id="25fc1-111">PT_LONG</span><span class="sxs-lookup"><span data-stu-id="25fc1-111">PT_LONG</span></span>  <br/> |
|<span data-ttu-id="25fc1-112">Domaine :</span><span class="sxs-lookup"><span data-stu-id="25fc1-112">Area:</span></span>  <br/> |<span data-ttu-id="25fc1-113">Divers</span><span class="sxs-lookup"><span data-stu-id="25fc1-113">Miscellaneous</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="25fc1-114">Remarques</span><span class="sxs-lookup"><span data-stu-id="25fc1-114">Remarks</span></span>

<span data-ttu-id="25fc1-115">Les valeurs possibles **pour PR_AGING_GRANULARITY** peuvent être l’une des valeurs suivantes.</span><span class="sxs-lookup"><span data-stu-id="25fc1-115">The possible values for **PR_AGING_GRANULARITY** can be one of the following.</span></span> 
  
|<span data-ttu-id="25fc1-116">**Name**</span><span class="sxs-lookup"><span data-stu-id="25fc1-116">**Name**</span></span>|<span data-ttu-id="25fc1-117">**Valeur**</span><span class="sxs-lookup"><span data-stu-id="25fc1-117">**Value**</span></span>|<span data-ttu-id="25fc1-118">**Description**</span><span class="sxs-lookup"><span data-stu-id="25fc1-118">**Description**</span></span>|
|:-----|:-----|:-----|
|<span data-ttu-id="25fc1-119">**AG_MONTHS**</span><span class="sxs-lookup"><span data-stu-id="25fc1-119">**AG_MONTHS**</span></span> <br/> |<span data-ttu-id="25fc1-120">0</span><span class="sxs-lookup"><span data-stu-id="25fc1-120">0</span></span>  <br/> |<span data-ttu-id="25fc1-121">**PR_AGING_PERIOD** est défini en nombre de mois.</span><span class="sxs-lookup"><span data-stu-id="25fc1-121">**PR_AGING_PERIOD** is defined in number of months.</span></span>  <br/> |
|<span data-ttu-id="25fc1-122">**AG_WEEKS**</span><span class="sxs-lookup"><span data-stu-id="25fc1-122">**AG_WEEKS**</span></span> <br/> |<span data-ttu-id="25fc1-123">1</span><span class="sxs-lookup"><span data-stu-id="25fc1-123">1</span></span>  <br/> |<span data-ttu-id="25fc1-124">**PR_AGING_PERIOD** est défini en nombre de semaines.</span><span class="sxs-lookup"><span data-stu-id="25fc1-124">**PR_AGING_PERIOD** is defined in number of weeks.</span></span>  <br/> |
|<span data-ttu-id="25fc1-125">**AG_DAYS**</span><span class="sxs-lookup"><span data-stu-id="25fc1-125">**AG_DAYS**</span></span> <br/> |<span data-ttu-id="25fc1-126">2</span><span class="sxs-lookup"><span data-stu-id="25fc1-126">2</span></span>  <br/> |<span data-ttu-id="25fc1-127">**PR_AGING_PERIOD** est défini en nombre de jours.</span><span class="sxs-lookup"><span data-stu-id="25fc1-127">**PR_AGING_PERIOD** is defined in number of days.</span></span>  <br/> |
   
<span data-ttu-id="25fc1-128">La durée pendant qu’un élément reste dans un dossier avant d’être archivé est déterminée par deux propriétés, [PR_AGING_PERIOD](pidtagagingperiod-canonical-property.md) et **PR_AGING_GRANULARITY**.</span><span class="sxs-lookup"><span data-stu-id="25fc1-128">The length of time that an item remains in a folder before the item is archived is determined by two properties, [PR_AGING_PERIOD](pidtagagingperiod-canonical-property.md) and **PR_AGING_GRANULARITY**.</span></span> <span data-ttu-id="25fc1-129">**PR_AGING_PERIOD** représente le nombre d’unités de temps pendant que l’élément reste dans le dossier avant d’être archivé.</span><span class="sxs-lookup"><span data-stu-id="25fc1-129">**PR_AGING_PERIOD** represents the number of time units that the item remains in the folder before it is archived.</span></span> 
  
## <a name="related-resources"></a><span data-ttu-id="25fc1-130">Ressources connexes</span><span class="sxs-lookup"><span data-stu-id="25fc1-130">Related resources</span></span>

### <a name="protocol-specifications"></a><span data-ttu-id="25fc1-131">Spécifications de protocole</span><span class="sxs-lookup"><span data-stu-id="25fc1-131">Protocol specifications</span></span>

<span data-ttu-id="25fc1-132">[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="25fc1-132">[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="25fc1-133">Fournit des références aux spécifications Exchange Server protocole.</span><span class="sxs-lookup"><span data-stu-id="25fc1-133">Provides references to related Exchange Server protocol specifications.</span></span>
    
<span data-ttu-id="25fc1-134">[[MS-OXCFXICS]](https://msdn.microsoft.com/library/b9752f3d-d50d-44b8-9e6b-608a117c8532%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="25fc1-134">[[MS-OXCFXICS]](https://msdn.microsoft.com/library/b9752f3d-d50d-44b8-9e6b-608a117c8532%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="25fc1-135">Définit les structures de données de base utilisées dans les opérations distantes.</span><span class="sxs-lookup"><span data-stu-id="25fc1-135">Defines the basic data structures that are used in remote operations.</span></span>
    
<span data-ttu-id="25fc1-136">[[MS-OXOMSG]](https://msdn.microsoft.com/library/daa9120f-f325-4afb-a738-28f91049ab3c%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="25fc1-136">[[MS-OXOMSG]](https://msdn.microsoft.com/library/daa9120f-f325-4afb-a738-28f91049ab3c%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="25fc1-137">Spécifie les propriétés et opérations autorisées pour les objets de message électronique.</span><span class="sxs-lookup"><span data-stu-id="25fc1-137">Specifies the properties and operations that are permissible for email message objects.</span></span>
    
### <a name="header-files"></a><span data-ttu-id="25fc1-138">Fichiers d’en-tête</span><span class="sxs-lookup"><span data-stu-id="25fc1-138">Header files</span></span>

<span data-ttu-id="25fc1-139">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="25fc1-139">Mapidefs.h</span></span>
  
> <span data-ttu-id="25fc1-140">Fournit des définitions de type de données.</span><span class="sxs-lookup"><span data-stu-id="25fc1-140">Provides data type definitions.</span></span>
    
<span data-ttu-id="25fc1-141">Mapitags.h</span><span class="sxs-lookup"><span data-stu-id="25fc1-141">Mapitags.h</span></span>
  
> <span data-ttu-id="25fc1-142">Contient les définitions des propriétés répertoriées en tant que noms de remplacement.</span><span class="sxs-lookup"><span data-stu-id="25fc1-142">Contains definitions of properties listed as alternate names.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="25fc1-143">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="25fc1-143">See also</span></span>



[<span data-ttu-id="25fc1-144">Propriétés MAPI</span><span class="sxs-lookup"><span data-stu-id="25fc1-144">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="25fc1-145">Propriétés canoniques MAPI</span><span class="sxs-lookup"><span data-stu-id="25fc1-145">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="25fc1-146">Mappage des noms de propriétés canoniques aux noms MAPI</span><span class="sxs-lookup"><span data-stu-id="25fc1-146">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="25fc1-147">Mappage des noms MAPI aux noms de propriétés canoniques</span><span class="sxs-lookup"><span data-stu-id="25fc1-147">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

