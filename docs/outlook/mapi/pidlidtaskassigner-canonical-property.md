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
description: 'Derni�re modification�: lundi 9 mars 2015'
ms.openlocfilehash: 5b711b1e0db0fab93016d3f1c979d81a142c9946
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19785441"
---
# <a name="pidlidtaskassigner-canonical-property"></a><span data-ttu-id="a1dcd-103">Propriété canonique PidLidTaskAssigner</span><span class="sxs-lookup"><span data-stu-id="a1dcd-103">PidLidTaskAssigner Canonical Property</span></span>

  
  
<span data-ttu-id="a1dcd-104">**S’applique à**: Outlook</span><span class="sxs-lookup"><span data-stu-id="a1dcd-104">**Applies to**: Outlook</span></span> 
  
 <span data-ttu-id="a1dcd-105">Noms de l’utilisateur qui a été affecté à la tâche.</span><span class="sxs-lookup"><span data-stu-id="a1dcd-105">Names the user who was last assigned the task.</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="a1dcd-106">Propriétés associées :</span><span class="sxs-lookup"><span data-stu-id="a1dcd-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="a1dcd-107">dispidTaskDelegator</span><span class="sxs-lookup"><span data-stu-id="a1dcd-107">dispidTaskDelegator</span></span>  <br/> |
|<span data-ttu-id="a1dcd-108">Jeu de propriétés :</span><span class="sxs-lookup"><span data-stu-id="a1dcd-108">Property set:</span></span>  <br/> |<span data-ttu-id="a1dcd-109">PSETID_Task</span><span class="sxs-lookup"><span data-stu-id="a1dcd-109">PSETID_Task</span></span>  <br/> |
|<span data-ttu-id="a1dcd-110">ID de type long (capot) :</span><span class="sxs-lookup"><span data-stu-id="a1dcd-110">Long ID (LID):</span></span>  <br/> |<span data-ttu-id="a1dcd-111">0x00008121</span><span class="sxs-lookup"><span data-stu-id="a1dcd-111">0x00008121</span></span>  <br/> |
|<span data-ttu-id="a1dcd-112">Type de données :</span><span class="sxs-lookup"><span data-stu-id="a1dcd-112">Data type:</span></span>  <br/> |<span data-ttu-id="a1dcd-113">PT_UNICODE</span><span class="sxs-lookup"><span data-stu-id="a1dcd-113">PT_UNICODE</span></span>  <br/> |
|<span data-ttu-id="a1dcd-114">Zone :</span><span class="sxs-lookup"><span data-stu-id="a1dcd-114">Area:</span></span>  <br/> |<span data-ttu-id="a1dcd-115">Tâche</span><span class="sxs-lookup"><span data-stu-id="a1dcd-115">Task</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="a1dcd-116">Remarques</span><span class="sxs-lookup"><span data-stu-id="a1dcd-116">Remarks</span></span>

<span data-ttu-id="a1dcd-117">Si la tâche n’a pas été assignée, cette propriété est pas définie.</span><span class="sxs-lookup"><span data-stu-id="a1dcd-117">If the task has not been assigned, this property is left unset.</span></span> <span data-ttu-id="a1dcd-118">Étant donné que le client définit cette propriété une fois que le destinataire de la tâche reçoit une demande de tâche, la propriété ne sera pas être définie sur la copie d’assigne la tâche de la tâche.</span><span class="sxs-lookup"><span data-stu-id="a1dcd-118">Because the client sets this property after the task assignee receives a task request, the property will not be set on the task assigner's copy of the task.</span></span> <span data-ttu-id="a1dcd-119">Lorsque le client ajoute ou supprime un assigne des tâches de la liste des tâches assigne dans la propriété **dispidTaskMyDelegators** ([PidLidTaskAssigners](pidlidtaskassigners-canonical-property.md)), la propriété **dispidTaskDelegator** ([PidLidTaskAssigner](pidlidtaskassigner-canonical-property.md)) doit être définie sur l’ajout ou assigne une tâche supprimée.</span><span class="sxs-lookup"><span data-stu-id="a1dcd-119">When the client adds or removes a task assigner from the task assigner list in the **dispidTaskMyDelegators** ([PidLidTaskAssigners](pidlidtaskassigners-canonical-property.md)) property, the **dispidTaskDelegator** ([PidLidTaskAssigner](pidlidtaskassigner-canonical-property.md)) property must be set to the added or removed task assigner.</span></span>
  
## <a name="related-resources"></a><span data-ttu-id="a1dcd-120">Ressources connexes</span><span class="sxs-lookup"><span data-stu-id="a1dcd-120">Related resources</span></span>

### <a name="protocol-specifications"></a><span data-ttu-id="a1dcd-121">Spécifications du protocole</span><span class="sxs-lookup"><span data-stu-id="a1dcd-121">Protocol specifications</span></span>

<span data-ttu-id="a1dcd-122">[[MS-OXPROPS]](http://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="a1dcd-122">[[MS-OXPROPS]](http://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="a1dcd-123">Fournit des définitions de jeu de propriétés et des références aux spécifications du protocole Exchange Server connexes.</span><span class="sxs-lookup"><span data-stu-id="a1dcd-123">Provides property set definitions and references to related Exchange Server protocol specifications.</span></span>
    
<span data-ttu-id="a1dcd-124">[[MS-OXOTASK]](http://msdn.microsoft.com/library/55600ec0-6195-4730-8436-59c7931ef27e%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="a1dcd-124">[[MS-OXOTASK]](http://msdn.microsoft.com/library/55600ec0-6195-4730-8436-59c7931ef27e%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="a1dcd-125">Définit plusieurs objets qui représentent l’équivalent électronique des tâches, les affectations de tâches et les mises à jour de tâche.</span><span class="sxs-lookup"><span data-stu-id="a1dcd-125">Defines several objects that model the electronic equivalent of tasks, task assignments, and task updates.</span></span>
    
### <a name="header-files"></a><span data-ttu-id="a1dcd-126">Fichiers d’en-tête</span><span class="sxs-lookup"><span data-stu-id="a1dcd-126">Header files</span></span>

<span data-ttu-id="a1dcd-127">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="a1dcd-127">Mapidefs.h</span></span>
  
> <span data-ttu-id="a1dcd-128">Fournit des définitions de type de données.</span><span class="sxs-lookup"><span data-stu-id="a1dcd-128">Provides data type definitions.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="a1dcd-129">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="a1dcd-129">See also</span></span>



[<span data-ttu-id="a1dcd-130">Propriétés MAPI</span><span class="sxs-lookup"><span data-stu-id="a1dcd-130">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="a1dcd-131">Propriétés canoniques MAPI</span><span class="sxs-lookup"><span data-stu-id="a1dcd-131">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="a1dcd-132">Mappage de noms de propriété canonique aux noms MAPI</span><span class="sxs-lookup"><span data-stu-id="a1dcd-132">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="a1dcd-133">Mappage de noms MAPI pour les noms de propriété canonique</span><span class="sxs-lookup"><span data-stu-id="a1dcd-133">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

