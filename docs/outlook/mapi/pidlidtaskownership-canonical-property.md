---
title: Propriété canonique PidLidTaskOwnership
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- PidLidTaskOwnership
api_type:
- COM
ms.assetid: 805dcb6c-f405-4c4d-8bca-af4bd9cd44fa
description: Dernière modification le 09 mars 2015
ms.openlocfilehash: 5c335d8fab820c9876adbe8f001696a02068460c
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/23/2018
ms.locfileid: "22591407"
---
# <a name="pidlidtaskownership-canonical-property"></a><span data-ttu-id="00c84-103">Propriété canonique PidLidTaskOwnership</span><span class="sxs-lookup"><span data-stu-id="00c84-103">PidLidTaskOwnership Canonical Property</span></span>

  
  
<span data-ttu-id="00c84-104">**S’applique à**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="00c84-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="00c84-105">Indique le rôle de l’utilisateur actuel par rapport à la tâche.</span><span class="sxs-lookup"><span data-stu-id="00c84-105">Indicates the role of the current user relative to the task.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="00c84-106">Propriétés associées :</span><span class="sxs-lookup"><span data-stu-id="00c84-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="00c84-107">dispidTaskOwnership</span><span class="sxs-lookup"><span data-stu-id="00c84-107">dispidTaskOwnership</span></span>  <br/> |
|<span data-ttu-id="00c84-108">Jeu de propriétés :</span><span class="sxs-lookup"><span data-stu-id="00c84-108">Property set:</span></span>  <br/> |<span data-ttu-id="00c84-109">PSETID_Task</span><span class="sxs-lookup"><span data-stu-id="00c84-109">PSETID_Task</span></span>  <br/> |
|<span data-ttu-id="00c84-110">ID de type long (capot) :</span><span class="sxs-lookup"><span data-stu-id="00c84-110">Long ID (LID):</span></span>  <br/> |<span data-ttu-id="00c84-111">0x00008129</span><span class="sxs-lookup"><span data-stu-id="00c84-111">0x00008129</span></span>  <br/> |
|<span data-ttu-id="00c84-112">Type de données :</span><span class="sxs-lookup"><span data-stu-id="00c84-112">Data type:</span></span>  <br/> |<span data-ttu-id="00c84-113">PT_LONG</span><span class="sxs-lookup"><span data-stu-id="00c84-113">PT_LONG</span></span>  <br/> |
|<span data-ttu-id="00c84-114">Domaine :</span><span class="sxs-lookup"><span data-stu-id="00c84-114">Area:</span></span>  <br/> |<span data-ttu-id="00c84-115">Task</span><span class="sxs-lookup"><span data-stu-id="00c84-115">Task</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="00c84-116">Remarques</span><span class="sxs-lookup"><span data-stu-id="00c84-116">Remarks</span></span>

<span data-ttu-id="00c84-117">Cette propriété doit être une des valeurs suivantes.</span><span class="sxs-lookup"><span data-stu-id="00c84-117">This property must be one of the following values.</span></span>
  
|<span data-ttu-id="00c84-118">**Valeur**</span><span class="sxs-lookup"><span data-stu-id="00c84-118">**Value**</span></span>|<span data-ttu-id="00c84-119">**Description**</span><span class="sxs-lookup"><span data-stu-id="00c84-119">**Description**</span></span>|
|:-----|:-----|
|<span data-ttu-id="00c84-120">0x00000000</span><span class="sxs-lookup"><span data-stu-id="00c84-120">0x00000000</span></span>  <br/> |<span data-ttu-id="00c84-121">La tâche n’est pas affectée.</span><span class="sxs-lookup"><span data-stu-id="00c84-121">The task is not assigned.</span></span>  <br/> |
|<span data-ttu-id="00c84-122">0x00000001</span><span class="sxs-lookup"><span data-stu-id="00c84-122">0x00000001</span></span>  <br/> |<span data-ttu-id="00c84-123">La tâche est la copie d’assigne la tâche de la tâche.</span><span class="sxs-lookup"><span data-stu-id="00c84-123">The task is the task assigner's copy of the task.</span></span>  <br/> |
|<span data-ttu-id="00c84-124">0x00000002</span><span class="sxs-lookup"><span data-stu-id="00c84-124">0x00000002</span></span>  <br/> |<span data-ttu-id="00c84-125">La tâche est copie du destinataire de la tâche de la tâche.</span><span class="sxs-lookup"><span data-stu-id="00c84-125">The task is the task assignee's copy of the task.</span></span>  <br/> |
   
## <a name="related-resources"></a><span data-ttu-id="00c84-126">Ressources connexes</span><span class="sxs-lookup"><span data-stu-id="00c84-126">Related resources</span></span>

### <a name="protocol-specifications"></a><span data-ttu-id="00c84-127">Spécifications du protocole</span><span class="sxs-lookup"><span data-stu-id="00c84-127">Protocol specifications</span></span>

<span data-ttu-id="00c84-128">[[MS-OXPROPS]](http://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="00c84-128">[[MS-OXPROPS]](http://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="00c84-129">Fournit des définitions de jeu de propriétés et des références aux spécifications du protocole Exchange Server connexes.</span><span class="sxs-lookup"><span data-stu-id="00c84-129">Provides property set definitions and references to related Exchange Server protocol specifications.</span></span>
    
<span data-ttu-id="00c84-130">[[MS-OXOTASK]](http://msdn.microsoft.com/library/55600ec0-6195-4730-8436-59c7931ef27e%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="00c84-130">[[MS-OXOTASK]](http://msdn.microsoft.com/library/55600ec0-6195-4730-8436-59c7931ef27e%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="00c84-131">Définit plusieurs objets qui représentent l’équivalent électronique des tâches, les affectations de tâches et les mises à jour de tâche.</span><span class="sxs-lookup"><span data-stu-id="00c84-131">Defines several objects that model the electronic equivalent of tasks, task assignments, and task updates.</span></span>
    
### <a name="header-files"></a><span data-ttu-id="00c84-132">Fichiers d’en-tête</span><span class="sxs-lookup"><span data-stu-id="00c84-132">Header files</span></span>

<span data-ttu-id="00c84-133">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="00c84-133">Mapidefs.h</span></span>
  
> <span data-ttu-id="00c84-134">Fournit des définitions de type de données.</span><span class="sxs-lookup"><span data-stu-id="00c84-134">Provides data type definitions.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="00c84-135">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="00c84-135">See also</span></span>



[<span data-ttu-id="00c84-136">Propriétés MAPI</span><span class="sxs-lookup"><span data-stu-id="00c84-136">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="00c84-137">Propriétés canoniques MAPI</span><span class="sxs-lookup"><span data-stu-id="00c84-137">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="00c84-138">Mappage des noms de propriétés canoniques aux noms MAPI</span><span class="sxs-lookup"><span data-stu-id="00c84-138">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="00c84-139">Mappage des noms MAPI aux noms de propriétés canoniques</span><span class="sxs-lookup"><span data-stu-id="00c84-139">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

