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
description: Dernière modification le 9 mars 2015
ms.openlocfilehash: 45fcba3f18aeb9092b71e28a6b68e42ad1abe77d
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32332108"
---
# <a name="pidlidtaskownership-canonical-property"></a><span data-ttu-id="dc1a3-103">Propriété canonique PidLidTaskOwnership</span><span class="sxs-lookup"><span data-stu-id="dc1a3-103">PidLidTaskOwnership Canonical Property</span></span>

  
  
<span data-ttu-id="dc1a3-104">**S’applique à** : Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="dc1a3-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="dc1a3-105">Indique le rôle de l’utilisateur actuel par rapport à la tâche.</span><span class="sxs-lookup"><span data-stu-id="dc1a3-105">Indicates the role of the current user relative to the task.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="dc1a3-106">Propriétés associées :</span><span class="sxs-lookup"><span data-stu-id="dc1a3-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="dc1a3-107">dispidTaskOwnership</span><span class="sxs-lookup"><span data-stu-id="dc1a3-107">dispidTaskOwnership</span></span>  <br/> |
|<span data-ttu-id="dc1a3-108">Jeu de propriétés :</span><span class="sxs-lookup"><span data-stu-id="dc1a3-108">Property set:</span></span>  <br/> |<span data-ttu-id="dc1a3-109">PSETID_Task</span><span class="sxs-lookup"><span data-stu-id="dc1a3-109">PSETID_Task</span></span>  <br/> |
|<span data-ttu-id="dc1a3-110">ID long (LID) :</span><span class="sxs-lookup"><span data-stu-id="dc1a3-110">Long ID (LID):</span></span>  <br/> |<span data-ttu-id="dc1a3-111">0x00008129</span><span class="sxs-lookup"><span data-stu-id="dc1a3-111">0x00008129</span></span>  <br/> |
|<span data-ttu-id="dc1a3-112">Type de données :</span><span class="sxs-lookup"><span data-stu-id="dc1a3-112">Data type:</span></span>  <br/> |<span data-ttu-id="dc1a3-113">PT_LONG</span><span class="sxs-lookup"><span data-stu-id="dc1a3-113">PT_LONG</span></span>  <br/> |
|<span data-ttu-id="dc1a3-114">Domaine :</span><span class="sxs-lookup"><span data-stu-id="dc1a3-114">Area:</span></span>  <br/> |<span data-ttu-id="dc1a3-115">Tâche</span><span class="sxs-lookup"><span data-stu-id="dc1a3-115">Task</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="dc1a3-116">Remarques</span><span class="sxs-lookup"><span data-stu-id="dc1a3-116">Remarks</span></span>

<span data-ttu-id="dc1a3-117">Cette propriété doit être l’une des valeurs suivantes.</span><span class="sxs-lookup"><span data-stu-id="dc1a3-117">This property must be one of the following values.</span></span>
  
|<span data-ttu-id="dc1a3-118">**Valeur**</span><span class="sxs-lookup"><span data-stu-id="dc1a3-118">**Value**</span></span>|<span data-ttu-id="dc1a3-119">**Description**</span><span class="sxs-lookup"><span data-stu-id="dc1a3-119">**Description**</span></span>|
|:-----|:-----|
|<span data-ttu-id="dc1a3-120">0x00000000</span><span class="sxs-lookup"><span data-stu-id="dc1a3-120">0x00000000</span></span>  <br/> |<span data-ttu-id="dc1a3-121">La tâche n’est pas affectée.</span><span class="sxs-lookup"><span data-stu-id="dc1a3-121">The task is not assigned.</span></span>  <br/> |
|<span data-ttu-id="dc1a3-122">0x00000001</span><span class="sxs-lookup"><span data-stu-id="dc1a3-122">0x00000001</span></span>  <br/> |<span data-ttu-id="dc1a3-123">La tâche est la copie de la tâche de l’assigneur de la tâche.</span><span class="sxs-lookup"><span data-stu-id="dc1a3-123">The task is the task assigner's copy of the task.</span></span>  <br/> |
|<span data-ttu-id="dc1a3-124">0x00000002</span><span class="sxs-lookup"><span data-stu-id="dc1a3-124">0x00000002</span></span>  <br/> |<span data-ttu-id="dc1a3-125">La tâche est la copie de la tâche de la personne à qui la tâche est assignée.</span><span class="sxs-lookup"><span data-stu-id="dc1a3-125">The task is the task assignee's copy of the task.</span></span>  <br/> |
   
## <a name="related-resources"></a><span data-ttu-id="dc1a3-126">Ressources connexes</span><span class="sxs-lookup"><span data-stu-id="dc1a3-126">Related resources</span></span>

### <a name="protocol-specifications"></a><span data-ttu-id="dc1a3-127">Spécifications de protocole</span><span class="sxs-lookup"><span data-stu-id="dc1a3-127">Protocol specifications</span></span>

<span data-ttu-id="dc1a3-128">[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="dc1a3-128">[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="dc1a3-129">Fournit des définitions de jeu de propriétés et des références aux spécifications Exchange Server protocole.</span><span class="sxs-lookup"><span data-stu-id="dc1a3-129">Provides property set definitions and references to related Exchange Server protocol specifications.</span></span>
    
<span data-ttu-id="dc1a3-130">[[MS-OXOTASK]](https://msdn.microsoft.com/library/55600ec0-6195-4730-8436-59c7931ef27e%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="dc1a3-130">[[MS-OXOTASK]](https://msdn.microsoft.com/library/55600ec0-6195-4730-8436-59c7931ef27e%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="dc1a3-131">Définit plusieurs objets qui modélisent l’équivalent électronique des tâches, des affectations de tâches et des mises à jour de tâches.</span><span class="sxs-lookup"><span data-stu-id="dc1a3-131">Defines several objects that model the electronic equivalent of tasks, task assignments, and task updates.</span></span>
    
### <a name="header-files"></a><span data-ttu-id="dc1a3-132">Fichiers d’en-tête</span><span class="sxs-lookup"><span data-stu-id="dc1a3-132">Header files</span></span>

<span data-ttu-id="dc1a3-133">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="dc1a3-133">Mapidefs.h</span></span>
  
> <span data-ttu-id="dc1a3-134">Fournit des définitions de type de données.</span><span class="sxs-lookup"><span data-stu-id="dc1a3-134">Provides data type definitions.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="dc1a3-135">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="dc1a3-135">See also</span></span>



[<span data-ttu-id="dc1a3-136">Propriétés MAPI</span><span class="sxs-lookup"><span data-stu-id="dc1a3-136">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="dc1a3-137">Propriétés canoniques MAPI</span><span class="sxs-lookup"><span data-stu-id="dc1a3-137">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="dc1a3-138">Mappage des noms de propriétés canoniques aux noms MAPI</span><span class="sxs-lookup"><span data-stu-id="dc1a3-138">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="dc1a3-139">Mappage des noms MAPI aux noms de propriétés canoniques</span><span class="sxs-lookup"><span data-stu-id="dc1a3-139">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

