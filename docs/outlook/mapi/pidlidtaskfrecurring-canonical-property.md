---
title: Propriété canonique PidLidTaskFRecurring
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- PidLidTaskFRecurring
api_type:
- COM
ms.assetid: 47c9ccbb-161c-4829-8ffb-201f3b54cd45
description: Dernière modification le 9 mars 2015
ms.openlocfilehash: aec9dd328e802e185c870d3ecd94cbd1d10ac67d
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32303051"
---
# <a name="pidlidtaskfrecurring-canonical-property"></a><span data-ttu-id="5e56a-103">Propriété canonique PidLidTaskFRecurring</span><span class="sxs-lookup"><span data-stu-id="5e56a-103">PidLidTaskFRecurring Canonical Property</span></span>

  
  
<span data-ttu-id="5e56a-104">**S’applique à** : Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="5e56a-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="5e56a-105">Indique si la tâche inclut une récurrence.</span><span class="sxs-lookup"><span data-stu-id="5e56a-105">Indicates whether the task includes a recurrence pattern.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="5e56a-106">Propriétés associées :</span><span class="sxs-lookup"><span data-stu-id="5e56a-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="5e56a-107">dispidTaskFRecur</span><span class="sxs-lookup"><span data-stu-id="5e56a-107">dispidTaskFRecur</span></span>  <br/> |
|<span data-ttu-id="5e56a-108">Jeu de propriétés :</span><span class="sxs-lookup"><span data-stu-id="5e56a-108">Property set:</span></span>  <br/> |<span data-ttu-id="5e56a-109">PSETID_Task</span><span class="sxs-lookup"><span data-stu-id="5e56a-109">PSETID_Task</span></span>  <br/> |
|<span data-ttu-id="5e56a-110">ID long (LID) :</span><span class="sxs-lookup"><span data-stu-id="5e56a-110">Long ID (LID):</span></span>  <br/> |<span data-ttu-id="5e56a-111">0x00008126</span><span class="sxs-lookup"><span data-stu-id="5e56a-111">0x00008126</span></span>  <br/> |
|<span data-ttu-id="5e56a-112">Type de données :</span><span class="sxs-lookup"><span data-stu-id="5e56a-112">Data type:</span></span>  <br/> |<span data-ttu-id="5e56a-113">PT_BOOLEAN</span><span class="sxs-lookup"><span data-stu-id="5e56a-113">PT_BOOLEAN</span></span>  <br/> |
|<span data-ttu-id="5e56a-114">Domaine :</span><span class="sxs-lookup"><span data-stu-id="5e56a-114">Area:</span></span>  <br/> |<span data-ttu-id="5e56a-115">Tâche</span><span class="sxs-lookup"><span data-stu-id="5e56a-115">Task</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="5e56a-116">Remarques</span><span class="sxs-lookup"><span data-stu-id="5e56a-116">Remarks</span></span>

<span data-ttu-id="5e56a-117">Si cette propriété n’est pas jeu, la valeur par défaut FALSE est supposée.</span><span class="sxs-lookup"><span data-stu-id="5e56a-117">If this property is left unset, a default value of FALSE is assumed.</span></span> <span data-ttu-id="5e56a-118">Si elle est définie sur TRUE, les propriétés **dispidTaskRecur** ([PidLidTaskRecurrence](pidlidtaskrecurrence-canonical-property.md)) et **dispidTaskDeadOccur** ([PidLidTaskDeadOccurrence](pidlidtaskdeadoccurrence-canonical-property.md)) doivent également être définies comme spécifié dans [[MS-OXOTASK]](https://msdn.microsoft.com/library/55600ec0-6195-4730-8436-59c7931ef27e%28Office.15%29.aspx).</span><span class="sxs-lookup"><span data-stu-id="5e56a-118">If it is set to TRUE, the **dispidTaskRecur** ([PidLidTaskRecurrence](pidlidtaskrecurrence-canonical-property.md)) and **dispidTaskDeadOccur** ([PidLidTaskDeadOccurrence](pidlidtaskdeadoccurrence-canonical-property.md)) properties must also be set as specified in [[MS-OXOTASK]](https://msdn.microsoft.com/library/55600ec0-6195-4730-8436-59c7931ef27e%28Office.15%29.aspx).</span></span>
  
## <a name="related-resources"></a><span data-ttu-id="5e56a-119">Ressources connexes</span><span class="sxs-lookup"><span data-stu-id="5e56a-119">Related resources</span></span>

### <a name="protocol-specifications"></a><span data-ttu-id="5e56a-120">Spécifications de protocole</span><span class="sxs-lookup"><span data-stu-id="5e56a-120">Protocol specifications</span></span>

<span data-ttu-id="5e56a-121">[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="5e56a-121">[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="5e56a-122">Fournit des définitions de jeu de propriétés et des références aux spécifications Exchange Server protocole.</span><span class="sxs-lookup"><span data-stu-id="5e56a-122">Provides property set definitions and references to related Exchange Server protocol specifications.</span></span>
    
<span data-ttu-id="5e56a-123">[[MS-OXOTASK]](https://msdn.microsoft.com/library/55600ec0-6195-4730-8436-59c7931ef27e%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="5e56a-123">[[MS-OXOTASK]](https://msdn.microsoft.com/library/55600ec0-6195-4730-8436-59c7931ef27e%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="5e56a-124">Définit plusieurs objets qui modélisent l’équivalent électronique des tâches, des affectations de tâches et des mises à jour de tâches.</span><span class="sxs-lookup"><span data-stu-id="5e56a-124">Defines several objects that model the electronic equivalent of tasks, task assignments, and task updates.</span></span>
    
### <a name="header-files"></a><span data-ttu-id="5e56a-125">Fichiers d’en-tête</span><span class="sxs-lookup"><span data-stu-id="5e56a-125">Header files</span></span>

<span data-ttu-id="5e56a-126">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="5e56a-126">Mapidefs.h</span></span>
  
> <span data-ttu-id="5e56a-127">Fournit des définitions de type de données.</span><span class="sxs-lookup"><span data-stu-id="5e56a-127">Provides data type definitions.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="5e56a-128">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="5e56a-128">See also</span></span>



[<span data-ttu-id="5e56a-129">Propriétés MAPI</span><span class="sxs-lookup"><span data-stu-id="5e56a-129">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="5e56a-130">Propriétés canoniques MAPI</span><span class="sxs-lookup"><span data-stu-id="5e56a-130">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="5e56a-131">Mappage des noms de propriétés canoniques aux noms MAPI</span><span class="sxs-lookup"><span data-stu-id="5e56a-131">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="5e56a-132">Mappage des noms MAPI aux noms de propriétés canoniques</span><span class="sxs-lookup"><span data-stu-id="5e56a-132">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

