---
title: Propriété canonique PidLidTaskMode
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- PidLidTaskMode
api_type:
- COM
ms.assetid: 185db683-301a-4d91-a583-6959853fa1ad
description: Dernière modification le 9 mars 2015
ms.openlocfilehash: d0ae319a6b5fa4c901ec7d318c7ebdd216a2adeb
ms.sourcegitcommit: ef717c65d8dd41ababffb01eafc443c79950aed4
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 10/04/2018
ms.locfileid: "25398968"
---
# <a name="pidlidtaskmode-canonical-property"></a><span data-ttu-id="1a1f7-103">Propriété canonique PidLidTaskMode</span><span class="sxs-lookup"><span data-stu-id="1a1f7-103">PidLidTaskMode Canonical Property</span></span>

  
  
<span data-ttu-id="1a1f7-104">**S’applique à** : Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="1a1f7-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="1a1f7-105">Spécifie l’état de l’affectation de la tâche.</span><span class="sxs-lookup"><span data-stu-id="1a1f7-105">Specifies the assignment status of the task.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="1a1f7-106">Propriétés associées :</span><span class="sxs-lookup"><span data-stu-id="1a1f7-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="1a1f7-107">dispidTaskMode</span><span class="sxs-lookup"><span data-stu-id="1a1f7-107">dispidTaskMode</span></span>  <br/> |
|<span data-ttu-id="1a1f7-108">Jeu de propriétés :</span><span class="sxs-lookup"><span data-stu-id="1a1f7-108">Property set:</span></span>  <br/> |<span data-ttu-id="1a1f7-109">PSETID_Common</span><span class="sxs-lookup"><span data-stu-id="1a1f7-109">PSETID_Common</span></span>  <br/> |
|<span data-ttu-id="1a1f7-110">ID de type long (capot) :</span><span class="sxs-lookup"><span data-stu-id="1a1f7-110">Long ID (LID):</span></span>  <br/> |<span data-ttu-id="1a1f7-111">0x00008518</span><span class="sxs-lookup"><span data-stu-id="1a1f7-111">0x00008518</span></span>  <br/> |
|<span data-ttu-id="1a1f7-112">Type de données :</span><span class="sxs-lookup"><span data-stu-id="1a1f7-112">Data type:</span></span>  <br/> |<span data-ttu-id="1a1f7-113">PT_LONG</span><span class="sxs-lookup"><span data-stu-id="1a1f7-113">PT_LONG</span></span>  <br/> |
|<span data-ttu-id="1a1f7-114">Domaine :</span><span class="sxs-lookup"><span data-stu-id="1a1f7-114">Area:</span></span>  <br/> |<span data-ttu-id="1a1f7-115">Task</span><span class="sxs-lookup"><span data-stu-id="1a1f7-115">Task</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="1a1f7-116">Remarques</span><span class="sxs-lookup"><span data-stu-id="1a1f7-116">Remarks</span></span>

<span data-ttu-id="1a1f7-117">La valeur doit être une des options suivantes.</span><span class="sxs-lookup"><span data-stu-id="1a1f7-117">The value must be one of the following.</span></span>
  
|<span data-ttu-id="1a1f7-118">**Valeur**</span><span class="sxs-lookup"><span data-stu-id="1a1f7-118">**Value**</span></span>|<span data-ttu-id="1a1f7-119">**Description**</span><span class="sxs-lookup"><span data-stu-id="1a1f7-119">**Description**</span></span>|
|:-----|:-----|
|<span data-ttu-id="1a1f7-120">0x00000000</span><span class="sxs-lookup"><span data-stu-id="1a1f7-120">0x00000000</span></span>  <br/> |<span data-ttu-id="1a1f7-121">La tâche n’est pas affectée.</span><span class="sxs-lookup"><span data-stu-id="1a1f7-121">The task is not assigned.</span></span>  <br/> |
|<span data-ttu-id="1a1f7-122">0x00000001</span><span class="sxs-lookup"><span data-stu-id="1a1f7-122">0x00000001</span></span>  <br/> |<span data-ttu-id="1a1f7-123">La tâche est incorporée dans une demande de tâche.</span><span class="sxs-lookup"><span data-stu-id="1a1f7-123">The task is embedded in a task request.</span></span>  <br/> |
|<span data-ttu-id="1a1f7-124">0x00000002</span><span class="sxs-lookup"><span data-stu-id="1a1f7-124">0x00000002</span></span>  <br/> |<span data-ttu-id="1a1f7-125">La tâche a été acceptée par le destinataire de la tâche.</span><span class="sxs-lookup"><span data-stu-id="1a1f7-125">The task was accepted by the task assignee.</span></span>  <br/> |
|<span data-ttu-id="1a1f7-126">0 x 00000003</span><span class="sxs-lookup"><span data-stu-id="1a1f7-126">0x00000003</span></span>  <br/> |<span data-ttu-id="1a1f7-127">La tâche a été rejetée par le destinataire de la tâche.</span><span class="sxs-lookup"><span data-stu-id="1a1f7-127">The task was rejected by the task assignee.</span></span>  <br/> |
|<span data-ttu-id="1a1f7-128">0 x 00000004</span><span class="sxs-lookup"><span data-stu-id="1a1f7-128">0x00000004</span></span>  <br/> |<span data-ttu-id="1a1f7-129">La tâche est incorporée dans une mise à jour de tâche.</span><span class="sxs-lookup"><span data-stu-id="1a1f7-129">The task is embedded in a task update.</span></span>  <br/> |
|<span data-ttu-id="1a1f7-130">0 x 00000005</span><span class="sxs-lookup"><span data-stu-id="1a1f7-130">0x00000005</span></span>  <br/> |<span data-ttu-id="1a1f7-131">La tâche a été affectée à l’assigne de tâche.</span><span class="sxs-lookup"><span data-stu-id="1a1f7-131">The task was assigned to the task assigner.</span></span>  <br/> |
   
## <a name="related-resources"></a><span data-ttu-id="1a1f7-132">Ressources connexes</span><span class="sxs-lookup"><span data-stu-id="1a1f7-132">Related resources</span></span>

### <a name="protocol-specifications"></a><span data-ttu-id="1a1f7-133">Spécifications du protocole</span><span class="sxs-lookup"><span data-stu-id="1a1f7-133">Protocol specifications</span></span>

<span data-ttu-id="1a1f7-134">[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="1a1f7-134">[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="1a1f7-135">Fournit des définitions de jeu de propriétés et des références aux spécifications du protocole Exchange Server connexes.</span><span class="sxs-lookup"><span data-stu-id="1a1f7-135">Provides property set definitions and references to related Exchange Server protocol specifications.</span></span>
    
<span data-ttu-id="1a1f7-136">[[MS-OXOTASK]](https://msdn.microsoft.com/library/55600ec0-6195-4730-8436-59c7931ef27e%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="1a1f7-136">[[MS-OXOTASK]](https://msdn.microsoft.com/library/55600ec0-6195-4730-8436-59c7931ef27e%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="1a1f7-137">Définit plusieurs objets qui représentent l’équivalent électronique des tâches, les affectations de tâches et les mises à jour de tâche.</span><span class="sxs-lookup"><span data-stu-id="1a1f7-137">Defines several objects that model the electronic equivalent of tasks, task assignments, and task updates.</span></span>
    
### <a name="header-files"></a><span data-ttu-id="1a1f7-138">Fichiers d’en-tête</span><span class="sxs-lookup"><span data-stu-id="1a1f7-138">Header files</span></span>

<span data-ttu-id="1a1f7-139">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="1a1f7-139">Mapidefs.h</span></span>
  
> <span data-ttu-id="1a1f7-140">Fournit des définitions de type de données.</span><span class="sxs-lookup"><span data-stu-id="1a1f7-140">Provides data type definitions.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="1a1f7-141">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="1a1f7-141">See also</span></span>



[<span data-ttu-id="1a1f7-142">Propriétés MAPI</span><span class="sxs-lookup"><span data-stu-id="1a1f7-142">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="1a1f7-143">Propriétés canoniques MAPI</span><span class="sxs-lookup"><span data-stu-id="1a1f7-143">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="1a1f7-144">Mappage des noms de propriétés canoniques aux noms MAPI</span><span class="sxs-lookup"><span data-stu-id="1a1f7-144">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="1a1f7-145">Mappage des noms MAPI aux noms de propriétés canoniques</span><span class="sxs-lookup"><span data-stu-id="1a1f7-145">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

