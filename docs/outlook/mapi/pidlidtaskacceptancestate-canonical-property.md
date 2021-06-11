---
title: Propriété canonique PidLidTaskAcceptanceState
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- PidLidTaskAcceptanceState
api_type:
- COM
ms.assetid: 7012f524-bc66-48ea-85b5-163e05029d35
description: Dernière modification le 9 mars 2015
ms.openlocfilehash: b42be4b42d085aba8999a8c3f1a780ed972fa136
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32331289"
---
# <a name="pidlidtaskacceptancestate-canonical-property"></a><span data-ttu-id="dff1c-103">Propriété canonique PidLidTaskAcceptanceState</span><span class="sxs-lookup"><span data-stu-id="dff1c-103">PidLidTaskAcceptanceState Canonical Property</span></span>

  
  
<span data-ttu-id="dff1c-104">**S’applique à** : Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="dff1c-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="dff1c-105">Indique l’état d’acceptation de la tâche.</span><span class="sxs-lookup"><span data-stu-id="dff1c-105">Indicates the acceptance state of the task.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="dff1c-106">Propriétés associées :</span><span class="sxs-lookup"><span data-stu-id="dff1c-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="dff1c-107">dispidTaskDelegValue</span><span class="sxs-lookup"><span data-stu-id="dff1c-107">dispidTaskDelegValue</span></span>  <br/> |
|<span data-ttu-id="dff1c-108">Jeu de propriétés :</span><span class="sxs-lookup"><span data-stu-id="dff1c-108">Property set:</span></span>  <br/> |<span data-ttu-id="dff1c-109">PSETID_Task</span><span class="sxs-lookup"><span data-stu-id="dff1c-109">PSETID_Task</span></span>  <br/> |
|<span data-ttu-id="dff1c-110">ID long (LID) :</span><span class="sxs-lookup"><span data-stu-id="dff1c-110">Long ID (LID):</span></span>  <br/> |<span data-ttu-id="dff1c-111">0x0000812A</span><span class="sxs-lookup"><span data-stu-id="dff1c-111">0x0000812A</span></span>  <br/> |
|<span data-ttu-id="dff1c-112">Type de données :</span><span class="sxs-lookup"><span data-stu-id="dff1c-112">Data type:</span></span>  <br/> |<span data-ttu-id="dff1c-113">PT_LONG</span><span class="sxs-lookup"><span data-stu-id="dff1c-113">PT_LONG</span></span>  <br/> |
|<span data-ttu-id="dff1c-114">Domaine :</span><span class="sxs-lookup"><span data-stu-id="dff1c-114">Area:</span></span>  <br/> |<span data-ttu-id="dff1c-115">Tâche</span><span class="sxs-lookup"><span data-stu-id="dff1c-115">Task</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="dff1c-116">Remarques</span><span class="sxs-lookup"><span data-stu-id="dff1c-116">Remarks</span></span>

<span data-ttu-id="dff1c-117">Le tableau suivant indique les valeurs possibles pour cette propriété.</span><span class="sxs-lookup"><span data-stu-id="dff1c-117">The following table shows the possible values for this property.</span></span>
  
|<span data-ttu-id="dff1c-118">**Valeur**</span><span class="sxs-lookup"><span data-stu-id="dff1c-118">**Value**</span></span>|<span data-ttu-id="dff1c-119">**Description**</span><span class="sxs-lookup"><span data-stu-id="dff1c-119">**Description**</span></span>|
|:-----|:-----|
|<span data-ttu-id="dff1c-120">0x00000000</span><span class="sxs-lookup"><span data-stu-id="dff1c-120">0x00000000</span></span>  <br/> |<span data-ttu-id="dff1c-121">La tâche n’est pas affectée.</span><span class="sxs-lookup"><span data-stu-id="dff1c-121">The task is not assigned.</span></span>  <br/> |
|<span data-ttu-id="dff1c-122">0x00000001</span><span class="sxs-lookup"><span data-stu-id="dff1c-122">0x00000001</span></span>  <br/> |<span data-ttu-id="dff1c-123">L’état d’acceptation de la tâche est inconnu.</span><span class="sxs-lookup"><span data-stu-id="dff1c-123">The task's acceptance status is unknown.</span></span>  <br/> |
|<span data-ttu-id="dff1c-124">0x00000002</span><span class="sxs-lookup"><span data-stu-id="dff1c-124">0x00000002</span></span>  <br/> |<span data-ttu-id="dff1c-125">La personne à qui la tâche a été assignée a accepté la tâche.</span><span class="sxs-lookup"><span data-stu-id="dff1c-125">The task assignee accepted the task.</span></span> <span data-ttu-id="dff1c-126">Cette valeur est définie lorsque le client traite une acceptation de tâche.</span><span class="sxs-lookup"><span data-stu-id="dff1c-126">This value is set when the client processes a task acceptance.</span></span>  <br/> |
|<span data-ttu-id="dff1c-127">0x00000003</span><span class="sxs-lookup"><span data-stu-id="dff1c-127">0x00000003</span></span>  <br/> |<span data-ttu-id="dff1c-128">L’affectation de la tâche a rejeté la tâche.</span><span class="sxs-lookup"><span data-stu-id="dff1c-128">The task assignee rejected the task.</span></span> <span data-ttu-id="dff1c-129">Cette valeur est définie lorsque le client traite un rejet de tâche.</span><span class="sxs-lookup"><span data-stu-id="dff1c-129">This value is set when the client processes a task rejection.</span></span>  <br/> |
   
## <a name="related-resources"></a><span data-ttu-id="dff1c-130">Ressources connexes</span><span class="sxs-lookup"><span data-stu-id="dff1c-130">Related resources</span></span>

### <a name="protocol-specifications"></a><span data-ttu-id="dff1c-131">Spécifications de protocole</span><span class="sxs-lookup"><span data-stu-id="dff1c-131">Protocol specifications</span></span>

<span data-ttu-id="dff1c-132">[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="dff1c-132">[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="dff1c-133">Fournit des définitions de jeu de propriétés et des références aux spécifications Exchange Server protocole.</span><span class="sxs-lookup"><span data-stu-id="dff1c-133">Provides property set definitions and references to related Exchange Server protocol specifications.</span></span>
    
<span data-ttu-id="dff1c-134">[[MS-OXOTASK]](https://msdn.microsoft.com/library/55600ec0-6195-4730-8436-59c7931ef27e%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="dff1c-134">[[MS-OXOTASK]](https://msdn.microsoft.com/library/55600ec0-6195-4730-8436-59c7931ef27e%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="dff1c-135">Définit plusieurs objets qui modélisent l’équivalent électronique des tâches, des affectations de tâches et des mises à jour de tâches.</span><span class="sxs-lookup"><span data-stu-id="dff1c-135">Defines several objects that model the electronic equivalent of tasks, task assignments, and task updates.</span></span>
    
### <a name="header-files"></a><span data-ttu-id="dff1c-136">Fichiers d’en-tête</span><span class="sxs-lookup"><span data-stu-id="dff1c-136">Header files</span></span>

<span data-ttu-id="dff1c-137">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="dff1c-137">Mapidefs.h</span></span>
  
> <span data-ttu-id="dff1c-138">Fournit des définitions de type de données.</span><span class="sxs-lookup"><span data-stu-id="dff1c-138">Provides data type definitions.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="dff1c-139">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="dff1c-139">See also</span></span>



[<span data-ttu-id="dff1c-140">Propriétés MAPI</span><span class="sxs-lookup"><span data-stu-id="dff1c-140">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="dff1c-141">Propriétés canoniques MAPI</span><span class="sxs-lookup"><span data-stu-id="dff1c-141">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="dff1c-142">Mappage des noms de propriétés canoniques aux noms MAPI</span><span class="sxs-lookup"><span data-stu-id="dff1c-142">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="dff1c-143">Mappage des noms MAPI aux noms de propriétés canoniques</span><span class="sxs-lookup"><span data-stu-id="dff1c-143">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

