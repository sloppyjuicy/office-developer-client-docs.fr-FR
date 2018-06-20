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
description: 'Derni�re modification�: lundi 9 mars 2015'
ms.openlocfilehash: 970fc57a3fd129f0ac50af3f71e0d5e15ff22371
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19785436"
---
# <a name="pidlidtaskacceptancestate-canonical-property"></a><span data-ttu-id="e21ab-103">Propriété canonique PidLidTaskAcceptanceState</span><span class="sxs-lookup"><span data-stu-id="e21ab-103">PidLidTaskAcceptanceState Canonical Property</span></span>

  
  
<span data-ttu-id="e21ab-104">**S’applique à**: Outlook</span><span class="sxs-lookup"><span data-stu-id="e21ab-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="e21ab-105">Indique l’état d’acceptation de la tâche.</span><span class="sxs-lookup"><span data-stu-id="e21ab-105">Indicates the acceptance state of the task.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="e21ab-106">Propriétés associées :</span><span class="sxs-lookup"><span data-stu-id="e21ab-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="e21ab-107">dispidTaskDelegValue</span><span class="sxs-lookup"><span data-stu-id="e21ab-107">dispidTaskDelegValue</span></span>  <br/> |
|<span data-ttu-id="e21ab-108">Jeu de propriétés :</span><span class="sxs-lookup"><span data-stu-id="e21ab-108">Property set:</span></span>  <br/> |<span data-ttu-id="e21ab-109">PSETID_Task</span><span class="sxs-lookup"><span data-stu-id="e21ab-109">PSETID_Task</span></span>  <br/> |
|<span data-ttu-id="e21ab-110">ID de type long (capot) :</span><span class="sxs-lookup"><span data-stu-id="e21ab-110">Long ID (LID):</span></span>  <br/> |<span data-ttu-id="e21ab-111">0x0000812A</span><span class="sxs-lookup"><span data-stu-id="e21ab-111">0x0000812A</span></span>  <br/> |
|<span data-ttu-id="e21ab-112">Type de données :</span><span class="sxs-lookup"><span data-stu-id="e21ab-112">Data type:</span></span>  <br/> |<span data-ttu-id="e21ab-113">PT_LONG</span><span class="sxs-lookup"><span data-stu-id="e21ab-113">PT_LONG</span></span>  <br/> |
|<span data-ttu-id="e21ab-114">Zone :</span><span class="sxs-lookup"><span data-stu-id="e21ab-114">Area:</span></span>  <br/> |<span data-ttu-id="e21ab-115">Tâche</span><span class="sxs-lookup"><span data-stu-id="e21ab-115">Task</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="e21ab-116">Remarques</span><span class="sxs-lookup"><span data-stu-id="e21ab-116">Remarks</span></span>

<span data-ttu-id="e21ab-117">Le tableau suivant présente les valeurs possibles pour cette propriété.</span><span class="sxs-lookup"><span data-stu-id="e21ab-117">The following table shows the possible values for this property.</span></span>
  
|<span data-ttu-id="e21ab-118">**Valeur**</span><span class="sxs-lookup"><span data-stu-id="e21ab-118">**Value**</span></span>|<span data-ttu-id="e21ab-119">**Description**</span><span class="sxs-lookup"><span data-stu-id="e21ab-119">**Description**</span></span>|
|:-----|:-----|
|<span data-ttu-id="e21ab-120">0x00000000</span><span class="sxs-lookup"><span data-stu-id="e21ab-120">0x00000000</span></span>  <br/> |<span data-ttu-id="e21ab-121">La tâche n’est pas affectée.</span><span class="sxs-lookup"><span data-stu-id="e21ab-121">The task is not assigned.</span></span>  <br/> |
|<span data-ttu-id="e21ab-122">0x00000001</span><span class="sxs-lookup"><span data-stu-id="e21ab-122">0x00000001</span></span>  <br/> |<span data-ttu-id="e21ab-123">Statut d’acceptation de la tâche est inconnue.</span><span class="sxs-lookup"><span data-stu-id="e21ab-123">The task's acceptance status is unknown.</span></span>  <br/> |
|<span data-ttu-id="e21ab-124">0x00000002</span><span class="sxs-lookup"><span data-stu-id="e21ab-124">0x00000002</span></span>  <br/> |<span data-ttu-id="e21ab-125">Destinataire de la tâche a accepté la tâche.</span><span class="sxs-lookup"><span data-stu-id="e21ab-125">The task assignee accepted the task.</span></span> <span data-ttu-id="e21ab-126">Cette valeur est définie lorsque le client traite une acceptation de la tâche.</span><span class="sxs-lookup"><span data-stu-id="e21ab-126">This value is set when the client processes a task acceptance.</span></span>  <br/> |
|<span data-ttu-id="e21ab-127">0 x 00000003</span><span class="sxs-lookup"><span data-stu-id="e21ab-127">0x00000003</span></span>  <br/> |<span data-ttu-id="e21ab-128">Destinataire de la tâche refusé la tâche.</span><span class="sxs-lookup"><span data-stu-id="e21ab-128">The task assignee rejected the task.</span></span> <span data-ttu-id="e21ab-129">Cette valeur est définie lorsque le client traite un refus de tâche.</span><span class="sxs-lookup"><span data-stu-id="e21ab-129">This value is set when the client processes a task rejection.</span></span>  <br/> |
   
## <a name="related-resources"></a><span data-ttu-id="e21ab-130">Ressources connexes</span><span class="sxs-lookup"><span data-stu-id="e21ab-130">Related resources</span></span>

### <a name="protocol-specifications"></a><span data-ttu-id="e21ab-131">Spécifications du protocole</span><span class="sxs-lookup"><span data-stu-id="e21ab-131">Protocol specifications</span></span>

<span data-ttu-id="e21ab-132">[[MS-OXPROPS]](http://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="e21ab-132">[[MS-OXPROPS]](http://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="e21ab-133">Fournit des définitions de jeu de propriétés et des références aux spécifications du protocole Exchange Server connexes.</span><span class="sxs-lookup"><span data-stu-id="e21ab-133">Provides property set definitions and references to related Exchange Server protocol specifications.</span></span>
    
<span data-ttu-id="e21ab-134">[[MS-OXOTASK]](http://msdn.microsoft.com/library/55600ec0-6195-4730-8436-59c7931ef27e%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="e21ab-134">[[MS-OXOTASK]](http://msdn.microsoft.com/library/55600ec0-6195-4730-8436-59c7931ef27e%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="e21ab-135">Définit plusieurs objets qui représentent l’équivalent électronique des tâches, les affectations de tâches et les mises à jour de tâche.</span><span class="sxs-lookup"><span data-stu-id="e21ab-135">Defines several objects that model the electronic equivalent of tasks, task assignments, and task updates.</span></span>
    
### <a name="header-files"></a><span data-ttu-id="e21ab-136">Fichiers d’en-tête</span><span class="sxs-lookup"><span data-stu-id="e21ab-136">Header files</span></span>

<span data-ttu-id="e21ab-137">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="e21ab-137">Mapidefs.h</span></span>
  
> <span data-ttu-id="e21ab-138">Fournit des définitions de type de données.</span><span class="sxs-lookup"><span data-stu-id="e21ab-138">Provides data type definitions.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="e21ab-139">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="e21ab-139">See also</span></span>



[<span data-ttu-id="e21ab-140">Propriétés MAPI</span><span class="sxs-lookup"><span data-stu-id="e21ab-140">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="e21ab-141">Propriétés canoniques MAPI</span><span class="sxs-lookup"><span data-stu-id="e21ab-141">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="e21ab-142">Mappage de noms de propriété canonique aux noms MAPI</span><span class="sxs-lookup"><span data-stu-id="e21ab-142">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="e21ab-143">Mappage de noms MAPI pour les noms de propriété canonique</span><span class="sxs-lookup"><span data-stu-id="e21ab-143">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

