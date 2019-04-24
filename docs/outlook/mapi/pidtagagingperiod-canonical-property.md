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
description: 'Derni�re modification�: lundi 9 mars 2015'
ms.openlocfilehash: d42b58bf4fd445f34064b179c873c8bc15b11b3f
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32360115"
---
# <a name="pidtagagingperiod-canonical-property"></a><span data-ttu-id="bedde-103">Propriété canonique PidTagAgingPeriod</span><span class="sxs-lookup"><span data-stu-id="bedde-103">PidTagAgingPeriod Canonical Property</span></span>

  
  
<span data-ttu-id="bedde-104">**S’applique à** : Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="bedde-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="bedde-105">Représente le nombre d'unités de temps qui sont utilisées pour déterminer la durée pendant laquelle un élément reste dans un dossier avant l'archivage de l'élément.</span><span class="sxs-lookup"><span data-stu-id="bedde-105">Represents the number of time units that are used to determine the length of time that an item remains in a folder before the item is archived.</span></span>
  
## 

|||
|:-----|:-----|
|<span data-ttu-id="bedde-106">Propriétés associées :</span><span class="sxs-lookup"><span data-stu-id="bedde-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="bedde-107">PR_AGING_PERIOD</span><span class="sxs-lookup"><span data-stu-id="bedde-107">PR_AGING_PERIOD</span></span>  <br/> |
|<span data-ttu-id="bedde-108">Identificateur :</span><span class="sxs-lookup"><span data-stu-id="bedde-108">Identifier:</span></span>  <br/> |<span data-ttu-id="bedde-109">0x36EC</span><span class="sxs-lookup"><span data-stu-id="bedde-109">0x36EC</span></span>  <br/> |
|<span data-ttu-id="bedde-110">Type de propriété:</span><span class="sxs-lookup"><span data-stu-id="bedde-110">Property type:</span></span>  <br/> |<span data-ttu-id="bedde-111">PT_LONG</span><span class="sxs-lookup"><span data-stu-id="bedde-111">PT_LONG</span></span>  <br/> |
|<span data-ttu-id="bedde-112">Domaine :</span><span class="sxs-lookup"><span data-stu-id="bedde-112">Area:</span></span>  <br/> |<span data-ttu-id="bedde-113">Divers</span><span class="sxs-lookup"><span data-stu-id="bedde-113">Miscellaneous</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="bedde-114">Remarques</span><span class="sxs-lookup"><span data-stu-id="bedde-114">Remarks</span></span>

<span data-ttu-id="bedde-115">La durée pendant laquelle un élément reste dans un dossier avant l'archivage de l'élément est déterminée par deux propriétés, **PR_AGING_PERIOD** et **[PR_AGING_GRANULARITY](pidtagaginggranularity-canonical-property.md)**.</span><span class="sxs-lookup"><span data-stu-id="bedde-115">The length of time that an item remains in a folder before the item is archived is determined by two properties, **PR_AGING_PERIOD** and **[PR_AGING_GRANULARITY](pidtagaginggranularity-canonical-property.md)**.</span></span> <span data-ttu-id="bedde-116">**PR_AGING_GRANULARITY** représente l'unité de temps dans laquelle **PR_AGING_PERIOD** est exprimée, lors de la détermination de ce laps de temps.</span><span class="sxs-lookup"><span data-stu-id="bedde-116">**PR_AGING_GRANULARITY** represents the time unit in which **PR_AGING_PERIOD** is expressed, when determining this length of time.</span></span> 
  
<span data-ttu-id="bedde-117">Les valeurs possibles pour **PR_AGING_GRANULARITY** peuvent être l'une des valeurs suivantes:</span><span class="sxs-lookup"><span data-stu-id="bedde-117">The possible values for **PR_AGING_GRANULARITY** can be one of the following.</span></span> 
  
****

|<span data-ttu-id="bedde-118">**Nom**</span><span class="sxs-lookup"><span data-stu-id="bedde-118">**Name**</span></span>|<span data-ttu-id="bedde-119">**Description**</span><span class="sxs-lookup"><span data-stu-id="bedde-119">**Description**</span></span>|
|:-----|:-----|
|<span data-ttu-id="bedde-120">**AG_MONTHS**</span><span class="sxs-lookup"><span data-stu-id="bedde-120">**AG_MONTHS**</span></span> <br/> |<span data-ttu-id="bedde-121">**PR_AGING_PERIOD** est défini en nombre de mois.</span><span class="sxs-lookup"><span data-stu-id="bedde-121">**PR_AGING_PERIOD** is defined in number of months.</span></span>  <br/> |
|<span data-ttu-id="bedde-122">**AG_WEEKS**</span><span class="sxs-lookup"><span data-stu-id="bedde-122">**AG_WEEKS**</span></span> <br/> |<span data-ttu-id="bedde-123">**PR_AGING_PERIOD** est défini en nombre de semaines.</span><span class="sxs-lookup"><span data-stu-id="bedde-123">**PR_AGING_PERIOD** is defined in number of weeks.</span></span>  <br/> |
|<span data-ttu-id="bedde-124">**AG_DAYS**</span><span class="sxs-lookup"><span data-stu-id="bedde-124">**AG_DAYS**</span></span> <br/> |<span data-ttu-id="bedde-125">**PR_AGING_PERIOD** est défini en nombre de jours.</span><span class="sxs-lookup"><span data-stu-id="bedde-125">**PR_AGING_PERIOD** is defined in number of days.</span></span>  <br/> |
   
<span data-ttu-id="bedde-126">Par exemple, si un dossier archive un élément uniquement une fois que l'élément se trouve dans le dossier pendant deux semaines, **PR_AGING_GRANULARITY** est **AG_WEEKS** et **PR_AGING_PERIOD** est 2.</span><span class="sxs-lookup"><span data-stu-id="bedde-126">For example, if a folder archives an item only after the item has been in the folder for two weeks, then **PR_AGING_GRANULARITY** is **AG_WEEKS** and **PR_AGING_PERIOD** is 2.</span></span> 
  
## <a name="related-resources"></a><span data-ttu-id="bedde-127">Ressources associées</span><span class="sxs-lookup"><span data-stu-id="bedde-127">Related resources</span></span>

### <a name="protocol-specifications"></a><span data-ttu-id="bedde-128">Spécifications de protocole</span><span class="sxs-lookup"><span data-stu-id="bedde-128">Protocol specifications</span></span>

<span data-ttu-id="bedde-129">[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="bedde-129">[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="bedde-130">Fournit des définitions de jeu de propriétés.</span><span class="sxs-lookup"><span data-stu-id="bedde-130">Provides property set definitions.</span></span>
    
<span data-ttu-id="bedde-131">[[MS-OXCFXICS]](https://msdn.microsoft.com/library/b9752f3d-d50d-44b8-9e6b-608a117c8532%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="bedde-131">[[MS-OXCFXICS]](https://msdn.microsoft.com/library/b9752f3d-d50d-44b8-9e6b-608a117c8532%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="bedde-132">Définit les structures de données de base qui sont utilisées dans les opérations distantes.</span><span class="sxs-lookup"><span data-stu-id="bedde-132">Defines the basic data structures that are used in remote operations.</span></span>
    
<span data-ttu-id="bedde-133">[[MS-OXOMSG]](https://msdn.microsoft.com/library/daa9120f-f325-4afb-a738-28f91049ab3c%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="bedde-133">[[MS-OXOMSG]](https://msdn.microsoft.com/library/daa9120f-f325-4afb-a738-28f91049ab3c%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="bedde-134">Spécifie les propriétés et les opérations autorisées pour les objets de message électronique.</span><span class="sxs-lookup"><span data-stu-id="bedde-134">Specifies the properties and operations that are permitted for email message objects.</span></span>
    
### <a name="header-files"></a><span data-ttu-id="bedde-135">Fichiers d'en-tête</span><span class="sxs-lookup"><span data-stu-id="bedde-135">Header files</span></span>

<span data-ttu-id="bedde-136">Mapidefs. h</span><span class="sxs-lookup"><span data-stu-id="bedde-136">Mapidefs.h</span></span>
  
> <span data-ttu-id="bedde-137">Fournit des définitions de type de données.</span><span class="sxs-lookup"><span data-stu-id="bedde-137">Provides data type definitions.</span></span>
    
<span data-ttu-id="bedde-138">Mapitags. h</span><span class="sxs-lookup"><span data-stu-id="bedde-138">Mapitags.h</span></span>
  
> <span data-ttu-id="bedde-139">Contient les définitions des propriétés figurant en tant que noms de substitution.</span><span class="sxs-lookup"><span data-stu-id="bedde-139">Contains definitions of properties listed as alternate names.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="bedde-140">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="bedde-140">See also</span></span>



[<span data-ttu-id="bedde-141">Propriétés MAPI</span><span class="sxs-lookup"><span data-stu-id="bedde-141">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="bedde-142">Propriétés canoniques MAPI</span><span class="sxs-lookup"><span data-stu-id="bedde-142">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="bedde-143">Mappage des noms de propriétés canoniques aux noms MAPI</span><span class="sxs-lookup"><span data-stu-id="bedde-143">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="bedde-144">Mappage des noms MAPI aux noms de propriétés canoniques</span><span class="sxs-lookup"><span data-stu-id="bedde-144">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

