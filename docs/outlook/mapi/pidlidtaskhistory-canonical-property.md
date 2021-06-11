---
title: Propriété canonique PidLidTaskHistory
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- PidLidTaskHistory
api_type:
- COM
ms.assetid: 104ef21c-b607-48b7-9b06-bc53b7d9b68a
description: Dernière modification le 9 mars 2015
ms.openlocfilehash: 39f2e6aeb4026f0b33be08b3bd8123283e5df3e1
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32303009"
---
# <a name="pidlidtaskhistory-canonical-property"></a><span data-ttu-id="3f88a-103">Propriété canonique PidLidTaskHistory</span><span class="sxs-lookup"><span data-stu-id="3f88a-103">PidLidTaskHistory Canonical Property</span></span>

  
  
<span data-ttu-id="3f88a-104">**S’applique à** : Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="3f88a-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="3f88a-105">Indique le type de modification qui a été apporté pour la dernière fois à la tâche.</span><span class="sxs-lookup"><span data-stu-id="3f88a-105">Indicates the type of change that was last made to the task.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="3f88a-106">Propriétés associées :</span><span class="sxs-lookup"><span data-stu-id="3f88a-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="3f88a-107">dispidTaskHistory</span><span class="sxs-lookup"><span data-stu-id="3f88a-107">dispidTaskHistory</span></span>  <br/> |
|<span data-ttu-id="3f88a-108">Jeu de propriétés :</span><span class="sxs-lookup"><span data-stu-id="3f88a-108">Property set:</span></span>  <br/> |<span data-ttu-id="3f88a-109">PSETID_Task</span><span class="sxs-lookup"><span data-stu-id="3f88a-109">PSETID_Task</span></span>  <br/> |
|<span data-ttu-id="3f88a-110">ID long (LID) :</span><span class="sxs-lookup"><span data-stu-id="3f88a-110">Long ID (LID):</span></span>  <br/> |<span data-ttu-id="3f88a-111">0x0000811A</span><span class="sxs-lookup"><span data-stu-id="3f88a-111">0x0000811A</span></span>  <br/> |
|<span data-ttu-id="3f88a-112">Type de données :</span><span class="sxs-lookup"><span data-stu-id="3f88a-112">Data type:</span></span>  <br/> |<span data-ttu-id="3f88a-113">PT_LONG</span><span class="sxs-lookup"><span data-stu-id="3f88a-113">PT_LONG</span></span>  <br/> |
|<span data-ttu-id="3f88a-114">Domaine :</span><span class="sxs-lookup"><span data-stu-id="3f88a-114">Area:</span></span>  <br/> |<span data-ttu-id="3f88a-115">Tâche</span><span class="sxs-lookup"><span data-stu-id="3f88a-115">Task</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="3f88a-116">Remarques</span><span class="sxs-lookup"><span data-stu-id="3f88a-116">Remarks</span></span>

<span data-ttu-id="3f88a-117">Lorsque la valeur de cette propriété est définie, la propriété **dispidTaskLastUpdate** ([PidLidTaskLastUpdate](pidlidtasklastupdate-canonical-property.md)) doit également être définie sur l’heure actuelle.</span><span class="sxs-lookup"><span data-stu-id="3f88a-117">When the value of this property is set, the **dispidTaskLastUpdate** ([PidLidTaskLastUpdate](pidlidtasklastupdate-canonical-property.md)) property must also be set to the current time.</span></span> <span data-ttu-id="3f88a-118">Le tableau suivant indique les valeurs de la **propriété dispidTaskHistory,** répertoriées par ordre de priorité décroissante.</span><span class="sxs-lookup"><span data-stu-id="3f88a-118">The following table shows the **dispidTaskHistory** property values, listed in order of decreasing priority.</span></span> 
  
|<span data-ttu-id="3f88a-119">**Valeur**</span><span class="sxs-lookup"><span data-stu-id="3f88a-119">**Value**</span></span>|<span data-ttu-id="3f88a-120">**Description**</span><span class="sxs-lookup"><span data-stu-id="3f88a-120">**Description**</span></span>|
|:-----|:-----|
|<span data-ttu-id="3f88a-121">0x00000004</span><span class="sxs-lookup"><span data-stu-id="3f88a-121">0x00000004</span></span>  <br/> |<span data-ttu-id="3f88a-122">La **propriété dispidTaskDueDate** ([PidLidTaskDueDate](pidlidtaskduedate-canonical-property.md)) a été modifiée.</span><span class="sxs-lookup"><span data-stu-id="3f88a-122">The **dispidTaskDueDate** ([PidLidTaskDueDate](pidlidtaskduedate-canonical-property.md)) property changed.</span></span>  <br/> |
|<span data-ttu-id="3f88a-123">0x00000003</span><span class="sxs-lookup"><span data-stu-id="3f88a-123">0x00000003</span></span>  <br/> |<span data-ttu-id="3f88a-124">Une autre propriété a été modifiée.</span><span class="sxs-lookup"><span data-stu-id="3f88a-124">Another property was changed.</span></span>  <br/> |
|<span data-ttu-id="3f88a-125">0x00000001</span><span class="sxs-lookup"><span data-stu-id="3f88a-125">0x00000001</span></span>  <br/> |<span data-ttu-id="3f88a-126">L’affectation de la tâche a accepté cette tâche.</span><span class="sxs-lookup"><span data-stu-id="3f88a-126">The task assignee accepted this task.</span></span>  <br/> |
|<span data-ttu-id="3f88a-127">0x00000002</span><span class="sxs-lookup"><span data-stu-id="3f88a-127">0x00000002</span></span>  <br/> |<span data-ttu-id="3f88a-128">La personne à l’emploi de la tâche a rejeté cette tâche.</span><span class="sxs-lookup"><span data-stu-id="3f88a-128">The task assignee rejected this task.</span></span>  <br/> |
|<span data-ttu-id="3f88a-129">0x00000005</span><span class="sxs-lookup"><span data-stu-id="3f88a-129">0x00000005</span></span>  <br/> |<span data-ttu-id="3f88a-130">La tâche a été affectée à une personne affectée à la tâche.</span><span class="sxs-lookup"><span data-stu-id="3f88a-130">The task was assigned to a task assignee.</span></span>  <br/> |
|<span data-ttu-id="3f88a-131">0x00000000</span><span class="sxs-lookup"><span data-stu-id="3f88a-131">0x00000000</span></span>  <br/> |<span data-ttu-id="3f88a-132">Aucune modification n’a été apportée.</span><span class="sxs-lookup"><span data-stu-id="3f88a-132">No changes were made.</span></span>  <br/> |
   
## <a name="related-resources"></a><span data-ttu-id="3f88a-133">Ressources connexes</span><span class="sxs-lookup"><span data-stu-id="3f88a-133">Related resources</span></span>

### <a name="protocol-specifications"></a><span data-ttu-id="3f88a-134">Spécifications de protocole</span><span class="sxs-lookup"><span data-stu-id="3f88a-134">Protocol specifications</span></span>

<span data-ttu-id="3f88a-135">[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="3f88a-135">[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="3f88a-136">Fournit des définitions de jeu de propriétés et des références aux spécifications Exchange Server protocole.</span><span class="sxs-lookup"><span data-stu-id="3f88a-136">Provides property set definitions and references to related Exchange Server protocol specifications.</span></span>
    
<span data-ttu-id="3f88a-137">[[MS-OXOTASK]](https://msdn.microsoft.com/library/55600ec0-6195-4730-8436-59c7931ef27e%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="3f88a-137">[[MS-OXOTASK]](https://msdn.microsoft.com/library/55600ec0-6195-4730-8436-59c7931ef27e%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="3f88a-138">Définit plusieurs objets qui modélisent l’équivalent électronique des tâches, des affectations de tâches et des mises à jour de tâches.</span><span class="sxs-lookup"><span data-stu-id="3f88a-138">Defines several objects that model the electronic equivalent of tasks, task assignments, and task updates.</span></span>
    
### <a name="header-files"></a><span data-ttu-id="3f88a-139">Fichiers d’en-tête</span><span class="sxs-lookup"><span data-stu-id="3f88a-139">Header files</span></span>

<span data-ttu-id="3f88a-140">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="3f88a-140">Mapidefs.h</span></span>
  
> <span data-ttu-id="3f88a-141">Fournit des définitions de type de données.</span><span class="sxs-lookup"><span data-stu-id="3f88a-141">Provides data type definitions.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="3f88a-142">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="3f88a-142">See also</span></span>



[<span data-ttu-id="3f88a-143">Propriétés MAPI</span><span class="sxs-lookup"><span data-stu-id="3f88a-143">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="3f88a-144">Propriétés canoniques MAPI</span><span class="sxs-lookup"><span data-stu-id="3f88a-144">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="3f88a-145">Mappage des noms de propriétés canoniques aux noms MAPI</span><span class="sxs-lookup"><span data-stu-id="3f88a-145">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="3f88a-146">Mappage des noms MAPI aux noms de propriétés canoniques</span><span class="sxs-lookup"><span data-stu-id="3f88a-146">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

