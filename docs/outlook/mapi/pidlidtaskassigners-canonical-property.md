---
title: Propriété canonique PidLidTaskAssigners
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- PidLidTaskAssigners
api_type:
- COM
ms.assetid: 07500bd0-bcff-4b03-8ed3-80508875e253
description: Dernière modification le 9 mars 2015
ms.openlocfilehash: 97a4915d5422f6c5463ed399835172725b83407f
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32303064"
---
# <a name="pidlidtaskassigners-canonical-property"></a><span data-ttu-id="d5a0a-103">Propriété canonique PidLidTaskAssigners</span><span class="sxs-lookup"><span data-stu-id="d5a0a-103">PidLidTaskAssigners Canonical Property</span></span>

  
  
<span data-ttu-id="d5a0a-104">**S’applique à** : Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="d5a0a-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="d5a0a-105">Contient une pile d’entrées qui représentent les personnes qui affectent des tâches.</span><span class="sxs-lookup"><span data-stu-id="d5a0a-105">Contains a stack of entries that represent task assigners.</span></span> <span data-ttu-id="d5a0a-106">L’assigneur de tâches le plus récent apparaît en haut de la pile.</span><span class="sxs-lookup"><span data-stu-id="d5a0a-106">The most recent task assigner appears at the top of the stack.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="d5a0a-107">Propriétés associées :</span><span class="sxs-lookup"><span data-stu-id="d5a0a-107">Associated properties:</span></span>  <br/> |<span data-ttu-id="d5a0a-108">dispidTaskMyDelegators</span><span class="sxs-lookup"><span data-stu-id="d5a0a-108">dispidTaskMyDelegators</span></span>  <br/> |
|<span data-ttu-id="d5a0a-109">Jeu de propriétés :</span><span class="sxs-lookup"><span data-stu-id="d5a0a-109">Property set:</span></span>  <br/> |<span data-ttu-id="d5a0a-110">PSETID_Task</span><span class="sxs-lookup"><span data-stu-id="d5a0a-110">PSETID_Task</span></span>  <br/> |
|<span data-ttu-id="d5a0a-111">ID long (LID) :</span><span class="sxs-lookup"><span data-stu-id="d5a0a-111">Long ID (LID):</span></span>  <br/> |<span data-ttu-id="d5a0a-112">0x00008117</span><span class="sxs-lookup"><span data-stu-id="d5a0a-112">0x00008117</span></span>  <br/> |
|<span data-ttu-id="d5a0a-113">Type de données :</span><span class="sxs-lookup"><span data-stu-id="d5a0a-113">Data type:</span></span>  <br/> |<span data-ttu-id="d5a0a-114">PT_BINARY</span><span class="sxs-lookup"><span data-stu-id="d5a0a-114">PT_BINARY</span></span>  <br/> |
|<span data-ttu-id="d5a0a-115">Domaine :</span><span class="sxs-lookup"><span data-stu-id="d5a0a-115">Area:</span></span>  <br/> |<span data-ttu-id="d5a0a-116">Tâche</span><span class="sxs-lookup"><span data-stu-id="d5a0a-116">Task</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="d5a0a-117">Remarques</span><span class="sxs-lookup"><span data-stu-id="d5a0a-117">Remarks</span></span>

<span data-ttu-id="d5a0a-118">Lorsque le client reçoit une demande de tâche, il l’append à cette propriété, dont la structure est définie dans [[MS-OXOTASK]](https://msdn.microsoft.com/library/55600ec0-6195-4730-8436-59c7931ef27e%28Office.15%29.aspx), une entrée qui représente l’expéditeur de la tâche.</span><span class="sxs-lookup"><span data-stu-id="d5a0a-118">When the client receives a task request, it appends to this property, which structure is defined in [[MS-OXOTASK]](https://msdn.microsoft.com/library/55600ec0-6195-4730-8436-59c7931ef27e%28Office.15%29.aspx), an entry that represents the task's sender.</span></span> <span data-ttu-id="d5a0a-119">Lorsque le client reçoit un rejet de tâche, il supprime la dernière entrée de l’assigneur de la tâche de cette propriété.</span><span class="sxs-lookup"><span data-stu-id="d5a0a-119">When the client receives a task rejection, the client removes the last task assigner entry from this property.</span></span> <span data-ttu-id="d5a0a-120">Lorsque le client envoie une réponse de tâche, il l’envoie au dernier assigneur de tâche répertorié dans la valeur de cette propriété.</span><span class="sxs-lookup"><span data-stu-id="d5a0a-120">When the client sends a task response, the client sends it to the last task assigner listed in the value of this property.</span></span>
  
## <a name="related-resources"></a><span data-ttu-id="d5a0a-121">Ressources connexes</span><span class="sxs-lookup"><span data-stu-id="d5a0a-121">Related resources</span></span>

### <a name="protocol-specifications"></a><span data-ttu-id="d5a0a-122">Spécifications de protocole</span><span class="sxs-lookup"><span data-stu-id="d5a0a-122">Protocol specifications</span></span>

<span data-ttu-id="d5a0a-123">[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="d5a0a-123">[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="d5a0a-124">Fournit des définitions de jeu de propriétés et des références aux spécifications Exchange Server protocole.</span><span class="sxs-lookup"><span data-stu-id="d5a0a-124">Provides property set definitions and references to related Exchange Server protocol specifications.</span></span>
    
<span data-ttu-id="d5a0a-125">[[MS-OXOTASK]](https://msdn.microsoft.com/library/55600ec0-6195-4730-8436-59c7931ef27e%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="d5a0a-125">[[MS-OXOTASK]](https://msdn.microsoft.com/library/55600ec0-6195-4730-8436-59c7931ef27e%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="d5a0a-126">Définit plusieurs objets qui modélisent l’équivalent électronique des tâches, des affectations de tâches et des mises à jour de tâches</span><span class="sxs-lookup"><span data-stu-id="d5a0a-126">Defines several objects that model the electronic equivalent of tasks, task assignments, and task updates</span></span> 
    
### <a name="header-files"></a><span data-ttu-id="d5a0a-127">Fichiers d’en-tête</span><span class="sxs-lookup"><span data-stu-id="d5a0a-127">Header files</span></span>

<span data-ttu-id="d5a0a-128">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="d5a0a-128">Mapidefs.h</span></span>
  
> <span data-ttu-id="d5a0a-129">Fournit des définitions de type de données.</span><span class="sxs-lookup"><span data-stu-id="d5a0a-129">Provides data type definitions.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="d5a0a-130">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="d5a0a-130">See also</span></span>



[<span data-ttu-id="d5a0a-131">Propriétés MAPI</span><span class="sxs-lookup"><span data-stu-id="d5a0a-131">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="d5a0a-132">Propriétés canoniques MAPI</span><span class="sxs-lookup"><span data-stu-id="d5a0a-132">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="d5a0a-133">Mappage des noms de propriétés canoniques aux noms MAPI</span><span class="sxs-lookup"><span data-stu-id="d5a0a-133">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="d5a0a-134">Mappage des noms MAPI aux noms de propriétés canoniques</span><span class="sxs-lookup"><span data-stu-id="d5a0a-134">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

