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
description: 'Derni�re modification�: lundi 9 mars 2015'
ms.openlocfilehash: 39f2e6aeb4026f0b33be08b3bd8123283e5df3e1
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32303009"
---
# <a name="pidlidtaskhistory-canonical-property"></a><span data-ttu-id="27685-103">Propriété canonique PidLidTaskHistory</span><span class="sxs-lookup"><span data-stu-id="27685-103">PidLidTaskHistory Canonical Property</span></span>

  
  
<span data-ttu-id="27685-104">**S’applique à** : Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="27685-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="27685-105">Indique le type de modification qui a été apportée à la tâche.</span><span class="sxs-lookup"><span data-stu-id="27685-105">Indicates the type of change that was last made to the task.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="27685-106">Propriétés associées :</span><span class="sxs-lookup"><span data-stu-id="27685-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="27685-107">dispidTaskHistory</span><span class="sxs-lookup"><span data-stu-id="27685-107">dispidTaskHistory</span></span>  <br/> |
|<span data-ttu-id="27685-108">Jeu de propriétés:</span><span class="sxs-lookup"><span data-stu-id="27685-108">Property set:</span></span>  <br/> |<span data-ttu-id="27685-109">PSETID_Task</span><span class="sxs-lookup"><span data-stu-id="27685-109">PSETID_Task</span></span>  <br/> |
|<span data-ttu-id="27685-110">ID long (couvercle):</span><span class="sxs-lookup"><span data-stu-id="27685-110">Long ID (LID):</span></span>  <br/> |<span data-ttu-id="27685-111">0x0000811A</span><span class="sxs-lookup"><span data-stu-id="27685-111">0x0000811A</span></span>  <br/> |
|<span data-ttu-id="27685-112">Type de données :</span><span class="sxs-lookup"><span data-stu-id="27685-112">Data type:</span></span>  <br/> |<span data-ttu-id="27685-113">PT_LONG</span><span class="sxs-lookup"><span data-stu-id="27685-113">PT_LONG</span></span>  <br/> |
|<span data-ttu-id="27685-114">Domaine :</span><span class="sxs-lookup"><span data-stu-id="27685-114">Area:</span></span>  <br/> |<span data-ttu-id="27685-115">Tâche</span><span class="sxs-lookup"><span data-stu-id="27685-115">Task</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="27685-116">Remarques</span><span class="sxs-lookup"><span data-stu-id="27685-116">Remarks</span></span>

<span data-ttu-id="27685-117">Lorsque la valeur de cette propriété est définie, la propriété **dispidTaskLastUpdate** ([PidLidTaskLastUpdate](pidlidtasklastupdate-canonical-property.md)) doit également être définie sur l'heure actuelle.</span><span class="sxs-lookup"><span data-stu-id="27685-117">When the value of this property is set, the **dispidTaskLastUpdate** ([PidLidTaskLastUpdate](pidlidtasklastupdate-canonical-property.md)) property must also be set to the current time.</span></span> <span data-ttu-id="27685-118">Le tableau suivant indique les valeurs de propriété **dispidTaskHistory** , indiquées dans l'ordre de priorité décroissante.</span><span class="sxs-lookup"><span data-stu-id="27685-118">The following table shows the **dispidTaskHistory** property values, listed in order of decreasing priority.</span></span> 
  
|<span data-ttu-id="27685-119">**Value**</span><span class="sxs-lookup"><span data-stu-id="27685-119">**Value**</span></span>|<span data-ttu-id="27685-120">**Description**</span><span class="sxs-lookup"><span data-stu-id="27685-120">**Description**</span></span>|
|:-----|:-----|
|<span data-ttu-id="27685-121">0x00000004</span><span class="sxs-lookup"><span data-stu-id="27685-121">0x00000004</span></span>  <br/> |<span data-ttu-id="27685-122">La propriété **dispidTaskDueDate** ([PidLidTaskDueDate](pidlidtaskduedate-canonical-property.md)) a changé.</span><span class="sxs-lookup"><span data-stu-id="27685-122">The **dispidTaskDueDate** ([PidLidTaskDueDate](pidlidtaskduedate-canonical-property.md)) property changed.</span></span>  <br/> |
|<span data-ttu-id="27685-123">0x00000003</span><span class="sxs-lookup"><span data-stu-id="27685-123">0x00000003</span></span>  <br/> |<span data-ttu-id="27685-124">Une autre propriété a été modifiée.</span><span class="sxs-lookup"><span data-stu-id="27685-124">Another property was changed.</span></span>  <br/> |
|<span data-ttu-id="27685-125">0x00000001</span><span class="sxs-lookup"><span data-stu-id="27685-125">0x00000001</span></span>  <br/> |<span data-ttu-id="27685-126">Le cessionnaire de la tâche a accepté cette tâche.</span><span class="sxs-lookup"><span data-stu-id="27685-126">The task assignee accepted this task.</span></span>  <br/> |
|<span data-ttu-id="27685-127">0x00000002</span><span class="sxs-lookup"><span data-stu-id="27685-127">0x00000002</span></span>  <br/> |<span data-ttu-id="27685-128">La tâche affectée a rejeté cette tâche.</span><span class="sxs-lookup"><span data-stu-id="27685-128">The task assignee rejected this task.</span></span>  <br/> |
|<span data-ttu-id="27685-129">0x00000005</span><span class="sxs-lookup"><span data-stu-id="27685-129">0x00000005</span></span>  <br/> |<span data-ttu-id="27685-130">La tâche a été affectée à un cessionnaire de tâche.</span><span class="sxs-lookup"><span data-stu-id="27685-130">The task was assigned to a task assignee.</span></span>  <br/> |
|<span data-ttu-id="27685-131">0x00000000</span><span class="sxs-lookup"><span data-stu-id="27685-131">0x00000000</span></span>  <br/> |<span data-ttu-id="27685-132">Aucune modification n'a été apportée.</span><span class="sxs-lookup"><span data-stu-id="27685-132">No changes were made.</span></span>  <br/> |
   
## <a name="related-resources"></a><span data-ttu-id="27685-133">Ressources associées</span><span class="sxs-lookup"><span data-stu-id="27685-133">Related resources</span></span>

### <a name="protocol-specifications"></a><span data-ttu-id="27685-134">Spécifications de protocole</span><span class="sxs-lookup"><span data-stu-id="27685-134">Protocol specifications</span></span>

<span data-ttu-id="27685-135">[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="27685-135">[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="27685-136">Fournit des définitions de jeu de propriétés et des références à des spécifications de protocole Exchange Server connexes.</span><span class="sxs-lookup"><span data-stu-id="27685-136">Provides property set definitions and references to related Exchange Server protocol specifications.</span></span>
    
<span data-ttu-id="27685-137">[[MS-OXOTASK]](https://msdn.microsoft.com/library/55600ec0-6195-4730-8436-59c7931ef27e%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="27685-137">[[MS-OXOTASK]](https://msdn.microsoft.com/library/55600ec0-6195-4730-8436-59c7931ef27e%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="27685-138">Définit plusieurs objets qui modélisent l'équivalent électronique des tâches, des affectations de tâches et des mises à jour de tâches.</span><span class="sxs-lookup"><span data-stu-id="27685-138">Defines several objects that model the electronic equivalent of tasks, task assignments, and task updates.</span></span>
    
### <a name="header-files"></a><span data-ttu-id="27685-139">Fichiers d'en-tête</span><span class="sxs-lookup"><span data-stu-id="27685-139">Header files</span></span>

<span data-ttu-id="27685-140">Mapidefs. h</span><span class="sxs-lookup"><span data-stu-id="27685-140">Mapidefs.h</span></span>
  
> <span data-ttu-id="27685-141">Fournit des définitions de type de données.</span><span class="sxs-lookup"><span data-stu-id="27685-141">Provides data type definitions.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="27685-142">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="27685-142">See also</span></span>



[<span data-ttu-id="27685-143">Propriétés MAPI</span><span class="sxs-lookup"><span data-stu-id="27685-143">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="27685-144">Propriétés canoniques MAPI</span><span class="sxs-lookup"><span data-stu-id="27685-144">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="27685-145">Mappage des noms de propriétés canoniques aux noms MAPI</span><span class="sxs-lookup"><span data-stu-id="27685-145">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="27685-146">Mappage des noms MAPI aux noms de propriétés canoniques</span><span class="sxs-lookup"><span data-stu-id="27685-146">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

