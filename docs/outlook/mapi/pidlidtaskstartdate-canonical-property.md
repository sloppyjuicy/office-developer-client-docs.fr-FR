---
title: Propriété canonique PidLidTaskStartDate
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- PidLidTaskStartDate
api_type:
- COM
ms.assetid: fe87eb3d-21d1-45bb-b848-e141ce1be6a0
description: 'Derni�re modification�: lundi 9 mars 2015'
ms.openlocfilehash: 3bc475292e47a9ad8dd9565e17640ef95e7b3c76
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32316680"
---
# <a name="pidlidtaskstartdate-canonical-property"></a><span data-ttu-id="db22d-103">Propriété canonique PidLidTaskStartDate</span><span class="sxs-lookup"><span data-stu-id="db22d-103">PidLidTaskStartDate Canonical Property</span></span>

  
  
<span data-ttu-id="db22d-104">**S’applique à** : Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="db22d-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="db22d-105">Date à laquelle l'utilisateur s'attend à commencer la tâche.</span><span class="sxs-lookup"><span data-stu-id="db22d-105">The date when the user expects to begin the task.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="db22d-106">Propriétés associées :</span><span class="sxs-lookup"><span data-stu-id="db22d-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="db22d-107">dispidTaskStartDate</span><span class="sxs-lookup"><span data-stu-id="db22d-107">dispidTaskStartDate</span></span>  <br/> |
|<span data-ttu-id="db22d-108">Jeu de propriétés:</span><span class="sxs-lookup"><span data-stu-id="db22d-108">Property set:</span></span>  <br/> |<span data-ttu-id="db22d-109">PSETID_Task</span><span class="sxs-lookup"><span data-stu-id="db22d-109">PSETID_Task</span></span>  <br/> |
|<span data-ttu-id="db22d-110">ID long (couvercle):</span><span class="sxs-lookup"><span data-stu-id="db22d-110">Long ID (LID):</span></span>  <br/> |<span data-ttu-id="db22d-111">0x00008104</span><span class="sxs-lookup"><span data-stu-id="db22d-111">0x00008104</span></span>  <br/> |
|<span data-ttu-id="db22d-112">Type de données :</span><span class="sxs-lookup"><span data-stu-id="db22d-112">Data type:</span></span>  <br/> |<span data-ttu-id="db22d-113">PT_SYSTIME</span><span class="sxs-lookup"><span data-stu-id="db22d-113">PT_SYSTIME</span></span>  <br/> |
|<span data-ttu-id="db22d-114">Domaine :</span><span class="sxs-lookup"><span data-stu-id="db22d-114">Area:</span></span>  <br/> |<span data-ttu-id="db22d-115">Tâche</span><span class="sxs-lookup"><span data-stu-id="db22d-115">Task</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="db22d-116">Remarques</span><span class="sxs-lookup"><span data-stu-id="db22d-116">Remarks</span></span>

<span data-ttu-id="db22d-117">Si la valeur de la propriété n'est pas définie, la tâche n'a pas de date de début.</span><span class="sxs-lookup"><span data-stu-id="db22d-117">If this property value is left unset, the task does not have a start date.</span></span> <span data-ttu-id="db22d-118">La valeur «0x5AE980E0» (1 525 252 320) signifie également que la tâche n'a pas de date de début.</span><span class="sxs-lookup"><span data-stu-id="db22d-118">A value of "0x5AE980E0" (1,525,252,320) also means that the task does not have a start date.</span></span> <span data-ttu-id="db22d-119">Si la tâche a une date de début, la valeur doit avoir un composant heure de minuit et les propriétés **dispidTaskDueDate** ([PidLidTaskDueDate](pidlidtaskduedate-canonical-property.md)) et **dispidCommonStart** ([PidLidCommonStart](pidlidcommonstart-canonical-property.md)) doivent également être définies.</span><span class="sxs-lookup"><span data-stu-id="db22d-119">If the task has a start date, the value must have a time component of midnight, and the **dispidTaskDueDate** ([PidLidTaskDueDate](pidlidtaskduedate-canonical-property.md)) and **dispidCommonStart** ([PidLidCommonStart](pidlidcommonstart-canonical-property.md)) properties must also be set.</span></span>
  
<span data-ttu-id="db22d-120">Cette propriété est partagée par la spécification du protocole d'indicateur d'information et la spécification du protocole d'objet lié aux tâches, qui se trouve dans [[MS-OXOTASK]](https://msdn.microsoft.com/library/55600ec0-6195-4730-8436-59c7931ef27e%28Office.15%29.aspx).</span><span class="sxs-lookup"><span data-stu-id="db22d-120">This property is shared by the Informational Flagging Protocol Specification and Task-Related Object Protocol Specification located in [[MS-OXOTASK]](https://msdn.microsoft.com/library/55600ec0-6195-4730-8436-59c7931ef27e%28Office.15%29.aspx).</span></span>
  
## <a name="related-resources"></a><span data-ttu-id="db22d-121">Ressources associées</span><span class="sxs-lookup"><span data-stu-id="db22d-121">Related resources</span></span>

### <a name="protocol-specifications"></a><span data-ttu-id="db22d-122">Spécifications de protocole</span><span class="sxs-lookup"><span data-stu-id="db22d-122">Protocol specifications</span></span>

<span data-ttu-id="db22d-123">[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="db22d-123">[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="db22d-124">Fournit des définitions de jeu de propriétés et des références à des spécifications de protocole Exchange Server connexes.</span><span class="sxs-lookup"><span data-stu-id="db22d-124">Provides property set definitions and references to related Exchange Server protocol specifications.</span></span>
    
<span data-ttu-id="db22d-125">[[MS-OXOTASK]](https://msdn.microsoft.com/library/55600ec0-6195-4730-8436-59c7931ef27e%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="db22d-125">[[MS-OXOTASK]](https://msdn.microsoft.com/library/55600ec0-6195-4730-8436-59c7931ef27e%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="db22d-126">Spécifie les propriétés et les opérations qui sont autorisées sur les contacts et les listes de distribution personnelles.</span><span class="sxs-lookup"><span data-stu-id="db22d-126">Specifies the properties and operations that are permissible on contacts and personal distribution lists.</span></span>
    
### <a name="header-files"></a><span data-ttu-id="db22d-127">Fichiers d'en-tête</span><span class="sxs-lookup"><span data-stu-id="db22d-127">Header files</span></span>

<span data-ttu-id="db22d-128">Mapidefs. h</span><span class="sxs-lookup"><span data-stu-id="db22d-128">Mapidefs.h</span></span>
  
> <span data-ttu-id="db22d-129">Fournit des définitions de type de données.</span><span class="sxs-lookup"><span data-stu-id="db22d-129">Provides data type definitions.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="db22d-130">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="db22d-130">See also</span></span>



[<span data-ttu-id="db22d-131">Propri�t� canonique PidLidTaskDueDate</span><span class="sxs-lookup"><span data-stu-id="db22d-131">PidLidTaskDueDate Canonical Property</span></span>](pidlidtaskduedate-canonical-property.md)
  
[<span data-ttu-id="db22d-132">Propri�t� canonique PidLidCommonStart</span><span class="sxs-lookup"><span data-stu-id="db22d-132">PidLidCommonStart Canonical Property</span></span>](pidlidcommonstart-canonical-property.md)


[<span data-ttu-id="db22d-133">Propriétés MAPI</span><span class="sxs-lookup"><span data-stu-id="db22d-133">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="db22d-134">Propriétés canoniques MAPI</span><span class="sxs-lookup"><span data-stu-id="db22d-134">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="db22d-135">Mappage des noms de propriétés canoniques aux noms MAPI</span><span class="sxs-lookup"><span data-stu-id="db22d-135">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="db22d-136">Mappage des noms MAPI aux noms de propriétés canoniques</span><span class="sxs-lookup"><span data-stu-id="db22d-136">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

