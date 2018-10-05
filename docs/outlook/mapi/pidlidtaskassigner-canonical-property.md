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
ms.sourcegitcommit: ef717c65d8dd41ababffb01eafc443c79950aed4
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 10/04/2018
ms.locfileid: "25400564"
---
# <a name="pidlidtaskassigner-canonical-property"></a><span data-ttu-id="6b841-103">Propriété canonique PidLidTaskAssigner</span><span class="sxs-lookup"><span data-stu-id="6b841-103">PidLidTaskAssigner Canonical Property</span></span>

  
  
<span data-ttu-id="6b841-104">**S’applique à** : Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="6b841-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
 <span data-ttu-id="6b841-105">Noms de l’utilisateur qui a été affecté à la tâche.</span><span class="sxs-lookup"><span data-stu-id="6b841-105">Names the user who was last assigned the task.</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="6b841-106">Propriétés associées :</span><span class="sxs-lookup"><span data-stu-id="6b841-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="6b841-107">dispidTaskDelegator</span><span class="sxs-lookup"><span data-stu-id="6b841-107">dispidTaskDelegator</span></span>  <br/> |
|<span data-ttu-id="6b841-108">Jeu de propriétés :</span><span class="sxs-lookup"><span data-stu-id="6b841-108">Property set:</span></span>  <br/> |<span data-ttu-id="6b841-109">PSETID_Task</span><span class="sxs-lookup"><span data-stu-id="6b841-109">PSETID_Task</span></span>  <br/> |
|<span data-ttu-id="6b841-110">ID de type long (capot) :</span><span class="sxs-lookup"><span data-stu-id="6b841-110">Long ID (LID):</span></span>  <br/> |<span data-ttu-id="6b841-111">0x00008121</span><span class="sxs-lookup"><span data-stu-id="6b841-111">0x00008121</span></span>  <br/> |
|<span data-ttu-id="6b841-112">Type de données :</span><span class="sxs-lookup"><span data-stu-id="6b841-112">Data type:</span></span>  <br/> |<span data-ttu-id="6b841-113">PT_UNICODE</span><span class="sxs-lookup"><span data-stu-id="6b841-113">PT_UNICODE</span></span>  <br/> |
|<span data-ttu-id="6b841-114">Domaine :</span><span class="sxs-lookup"><span data-stu-id="6b841-114">Area:</span></span>  <br/> |<span data-ttu-id="6b841-115">Task</span><span class="sxs-lookup"><span data-stu-id="6b841-115">Task</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="6b841-116">Remarques</span><span class="sxs-lookup"><span data-stu-id="6b841-116">Remarks</span></span>

<span data-ttu-id="6b841-117">Si la tâche n’a pas été assignée, cette propriété est pas définie.</span><span class="sxs-lookup"><span data-stu-id="6b841-117">If the task has not been assigned, this property is left unset.</span></span> <span data-ttu-id="6b841-118">Étant donné que le client définit cette propriété une fois que le destinataire de la tâche reçoit une demande de tâche, la propriété ne sera pas être définie sur la copie d’assigne la tâche de la tâche.</span><span class="sxs-lookup"><span data-stu-id="6b841-118">Because the client sets this property after the task assignee receives a task request, the property will not be set on the task assigner's copy of the task.</span></span> <span data-ttu-id="6b841-119">Lorsque le client ajoute ou supprime un assigne des tâches de la liste des tâches assigne dans la propriété **dispidTaskMyDelegators** ([PidLidTaskAssigners](pidlidtaskassigners-canonical-property.md)), la propriété **dispidTaskDelegator** ([PidLidTaskAssigner](pidlidtaskassigner-canonical-property.md)) doit être définie sur l’ajout ou assigne une tâche supprimée.</span><span class="sxs-lookup"><span data-stu-id="6b841-119">When the client adds or removes a task assigner from the task assigner list in the **dispidTaskMyDelegators** ([PidLidTaskAssigners](pidlidtaskassigners-canonical-property.md)) property, the **dispidTaskDelegator** ([PidLidTaskAssigner](pidlidtaskassigner-canonical-property.md)) property must be set to the added or removed task assigner.</span></span>
  
## <a name="related-resources"></a><span data-ttu-id="6b841-120">Ressources connexes</span><span class="sxs-lookup"><span data-stu-id="6b841-120">Related resources</span></span>

### <a name="protocol-specifications"></a><span data-ttu-id="6b841-121">Spécifications du protocole</span><span class="sxs-lookup"><span data-stu-id="6b841-121">Protocol specifications</span></span>

<span data-ttu-id="6b841-122">[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="6b841-122">[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="6b841-123">Fournit des définitions de jeu de propriétés et des références aux spécifications du protocole Exchange Server connexes.</span><span class="sxs-lookup"><span data-stu-id="6b841-123">Provides property set definitions and references to related Exchange Server protocol specifications.</span></span>
    
<span data-ttu-id="6b841-124">[[MS-OXOTASK]](https://msdn.microsoft.com/library/55600ec0-6195-4730-8436-59c7931ef27e%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="6b841-124">[[MS-OXOTASK]](https://msdn.microsoft.com/library/55600ec0-6195-4730-8436-59c7931ef27e%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="6b841-125">Définit plusieurs objets qui représentent l’équivalent électronique des tâches, les affectations de tâches et les mises à jour de tâche.</span><span class="sxs-lookup"><span data-stu-id="6b841-125">Defines several objects that model the electronic equivalent of tasks, task assignments, and task updates.</span></span>
    
### <a name="header-files"></a><span data-ttu-id="6b841-126">Fichiers d’en-tête</span><span class="sxs-lookup"><span data-stu-id="6b841-126">Header files</span></span>

<span data-ttu-id="6b841-127">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="6b841-127">Mapidefs.h</span></span>
  
> <span data-ttu-id="6b841-128">Fournit des définitions de type de données.</span><span class="sxs-lookup"><span data-stu-id="6b841-128">Provides data type definitions.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="6b841-129">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="6b841-129">See also</span></span>



[<span data-ttu-id="6b841-130">Propriétés MAPI</span><span class="sxs-lookup"><span data-stu-id="6b841-130">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="6b841-131">Propriétés canoniques MAPI</span><span class="sxs-lookup"><span data-stu-id="6b841-131">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="6b841-132">Mappage des noms de propriétés canoniques aux noms MAPI</span><span class="sxs-lookup"><span data-stu-id="6b841-132">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="6b841-133">Mappage des noms MAPI aux noms de propriétés canoniques</span><span class="sxs-lookup"><span data-stu-id="6b841-133">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

