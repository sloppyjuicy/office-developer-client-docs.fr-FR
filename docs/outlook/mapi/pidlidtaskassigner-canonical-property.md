---
title: Propriété canonique PidLidTaskAssigner
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- PidLidTaskAssigner
api_type:
- COM
ms.assetid: f7047e4e-0fb3-476b-9568-8f1135e6d970
description: Dernière modification le 9 mars 2015
ms.openlocfilehash: ef5f78fa36632227311d037ee61085c677920fb1
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32340088"
---
# <a name="pidlidtaskassigner-canonical-property"></a><span data-ttu-id="23f6c-103">Propriété canonique PidLidTaskAssigner</span><span class="sxs-lookup"><span data-stu-id="23f6c-103">PidLidTaskAssigner Canonical Property</span></span>

  
  
<span data-ttu-id="23f6c-104">**S’applique à** : Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="23f6c-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
 <span data-ttu-id="23f6c-105">Nomme l’utilisateur qui a été affecté pour la dernière fois à la tâche.</span><span class="sxs-lookup"><span data-stu-id="23f6c-105">Names the user who was last assigned the task.</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="23f6c-106">Propriétés associées :</span><span class="sxs-lookup"><span data-stu-id="23f6c-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="23f6c-107">dispidTaskDelegator</span><span class="sxs-lookup"><span data-stu-id="23f6c-107">dispidTaskDelegator</span></span>  <br/> |
|<span data-ttu-id="23f6c-108">Jeu de propriétés :</span><span class="sxs-lookup"><span data-stu-id="23f6c-108">Property set:</span></span>  <br/> |<span data-ttu-id="23f6c-109">PSETID_Task</span><span class="sxs-lookup"><span data-stu-id="23f6c-109">PSETID_Task</span></span>  <br/> |
|<span data-ttu-id="23f6c-110">ID long (LID) :</span><span class="sxs-lookup"><span data-stu-id="23f6c-110">Long ID (LID):</span></span>  <br/> |<span data-ttu-id="23f6c-111">0x00008121</span><span class="sxs-lookup"><span data-stu-id="23f6c-111">0x00008121</span></span>  <br/> |
|<span data-ttu-id="23f6c-112">Type de données :</span><span class="sxs-lookup"><span data-stu-id="23f6c-112">Data type:</span></span>  <br/> |<span data-ttu-id="23f6c-113">PT_UNICODE</span><span class="sxs-lookup"><span data-stu-id="23f6c-113">PT_UNICODE</span></span>  <br/> |
|<span data-ttu-id="23f6c-114">Domaine :</span><span class="sxs-lookup"><span data-stu-id="23f6c-114">Area:</span></span>  <br/> |<span data-ttu-id="23f6c-115">Tâche</span><span class="sxs-lookup"><span data-stu-id="23f6c-115">Task</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="23f6c-116">Remarques</span><span class="sxs-lookup"><span data-stu-id="23f6c-116">Remarks</span></span>

<span data-ttu-id="23f6c-117">Si la tâche n’a pas été affectée, cette propriété n’est pas affectée.</span><span class="sxs-lookup"><span data-stu-id="23f6c-117">If the task has not been assigned, this property is left unset.</span></span> <span data-ttu-id="23f6c-118">Étant donné que le client définit cette propriété une fois que la personne à la tâche a reçu une demande de tâche, la propriété n’est pas définie sur la copie de la tâche de l’assigneur de la tâche.</span><span class="sxs-lookup"><span data-stu-id="23f6c-118">Because the client sets this property after the task assignee receives a task request, the property will not be set on the task assigner's copy of the task.</span></span> <span data-ttu-id="23f6c-119">Lorsque le client ajoute ou supprime un assigneur de tâches de la liste des personnes qui affectent la tâche dans la propriété **dispidTaskMyDelegators** ([PidLidTaskAssigners](pidlidtaskassigners-canonical-property.md)), la propriété **dispidTaskDelegator** ([PidLidTaskAssigner](pidlidtaskassigner-canonical-property.md)) doit être définie sur l’assigneur de tâche ajouté ou supprimé.</span><span class="sxs-lookup"><span data-stu-id="23f6c-119">When the client adds or removes a task assigner from the task assigner list in the **dispidTaskMyDelegators** ([PidLidTaskAssigners](pidlidtaskassigners-canonical-property.md)) property, the **dispidTaskDelegator** ([PidLidTaskAssigner](pidlidtaskassigner-canonical-property.md)) property must be set to the added or removed task assigner.</span></span>
  
## <a name="related-resources"></a><span data-ttu-id="23f6c-120">Ressources connexes</span><span class="sxs-lookup"><span data-stu-id="23f6c-120">Related resources</span></span>

### <a name="protocol-specifications"></a><span data-ttu-id="23f6c-121">Spécifications de protocole</span><span class="sxs-lookup"><span data-stu-id="23f6c-121">Protocol specifications</span></span>

<span data-ttu-id="23f6c-122">[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="23f6c-122">[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="23f6c-123">Fournit des définitions de jeu de propriétés et des références aux spécifications Exchange Server protocole.</span><span class="sxs-lookup"><span data-stu-id="23f6c-123">Provides property set definitions and references to related Exchange Server protocol specifications.</span></span>
    
<span data-ttu-id="23f6c-124">[[MS-OXOTASK]](https://msdn.microsoft.com/library/55600ec0-6195-4730-8436-59c7931ef27e%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="23f6c-124">[[MS-OXOTASK]](https://msdn.microsoft.com/library/55600ec0-6195-4730-8436-59c7931ef27e%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="23f6c-125">Définit plusieurs objets qui modélisent l’équivalent électronique des tâches, des affectations de tâches et des mises à jour de tâches.</span><span class="sxs-lookup"><span data-stu-id="23f6c-125">Defines several objects that model the electronic equivalent of tasks, task assignments, and task updates.</span></span>
    
### <a name="header-files"></a><span data-ttu-id="23f6c-126">Fichiers d’en-tête</span><span class="sxs-lookup"><span data-stu-id="23f6c-126">Header files</span></span>

<span data-ttu-id="23f6c-127">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="23f6c-127">Mapidefs.h</span></span>
  
> <span data-ttu-id="23f6c-128">Fournit des définitions de type de données.</span><span class="sxs-lookup"><span data-stu-id="23f6c-128">Provides data type definitions.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="23f6c-129">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="23f6c-129">See also</span></span>



[<span data-ttu-id="23f6c-130">Propriétés MAPI</span><span class="sxs-lookup"><span data-stu-id="23f6c-130">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="23f6c-131">Propriétés canoniques MAPI</span><span class="sxs-lookup"><span data-stu-id="23f6c-131">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="23f6c-132">Mappage des noms de propriétés canoniques aux noms MAPI</span><span class="sxs-lookup"><span data-stu-id="23f6c-132">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="23f6c-133">Mappage des noms MAPI aux noms de propriétés canoniques</span><span class="sxs-lookup"><span data-stu-id="23f6c-133">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

