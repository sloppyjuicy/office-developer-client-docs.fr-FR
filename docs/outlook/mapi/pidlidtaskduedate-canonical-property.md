---
title: Propriété canonique PidLidTaskDueDate
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- PidLidTaskDueDate
api_type:
- COM
ms.assetid: 69ed3d48-3741-4a9a-8f98-51382b850c27
description: Dernière modification le 9 mars 2015
ms.openlocfilehash: 2e21d164cbb9403d3fa1dc05cf474359a517d64b
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32303324"
---
# <a name="pidlidtaskduedate-canonical-property"></a><span data-ttu-id="64011-103">Propriété canonique PidLidTaskDueDate</span><span class="sxs-lookup"><span data-stu-id="64011-103">PidLidTaskDueDate Canonical Property</span></span>

  
  
<span data-ttu-id="64011-104">**S’applique à** : Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="64011-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="64011-105">Représente la date à laquelle l’utilisateur s’attend à effectuer la tâche.</span><span class="sxs-lookup"><span data-stu-id="64011-105">Represents the date when the user expects to complete the task.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="64011-106">Propriétés associées :</span><span class="sxs-lookup"><span data-stu-id="64011-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="64011-107">dispidTaskDueDate</span><span class="sxs-lookup"><span data-stu-id="64011-107">dispidTaskDueDate</span></span>  <br/> |
|<span data-ttu-id="64011-108">Jeu de propriétés :</span><span class="sxs-lookup"><span data-stu-id="64011-108">Property set:</span></span>  <br/> |<span data-ttu-id="64011-109">PSETID_Task</span><span class="sxs-lookup"><span data-stu-id="64011-109">PSETID_Task</span></span>  <br/> |
|<span data-ttu-id="64011-110">ID long (LID) :</span><span class="sxs-lookup"><span data-stu-id="64011-110">Long ID (LID):</span></span>  <br/> |<span data-ttu-id="64011-111">0x00008105</span><span class="sxs-lookup"><span data-stu-id="64011-111">0x00008105</span></span>  <br/> |
|<span data-ttu-id="64011-112">Type de données :</span><span class="sxs-lookup"><span data-stu-id="64011-112">Data type:</span></span>  <br/> |<span data-ttu-id="64011-113">PT_SYSTIME</span><span class="sxs-lookup"><span data-stu-id="64011-113">PT_SYSTIME</span></span>  <br/> |
|<span data-ttu-id="64011-114">Domaine :</span><span class="sxs-lookup"><span data-stu-id="64011-114">Area:</span></span>  <br/> |<span data-ttu-id="64011-115">Tâche</span><span class="sxs-lookup"><span data-stu-id="64011-115">Task</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="64011-116">Remarques</span><span class="sxs-lookup"><span data-stu-id="64011-116">Remarks</span></span>

<span data-ttu-id="64011-117">La tâche n’a aucune date d’échéance si cette propriété n’est pas définie ou définie sur 0x5AE980E0 (1 525 252 320).</span><span class="sxs-lookup"><span data-stu-id="64011-117">The task has no due date if this property is unset or set to 0x5AE980E0 (1,525,252,320).</span></span> <span data-ttu-id="64011-118">Toutefois, une date d’échéance n’est facultative que si aucune date de début n’est indiquée dans la propriété **dispidTaskStartDate** ([PidLidTaskStartDate](pidlidtaskstartdate-canonical-property.md)).</span><span class="sxs-lookup"><span data-stu-id="64011-118">However, a due date is optional only if no start date is indicated in the **dispidTaskStartDate** ([PidLidTaskStartDate](pidlidtaskstartdate-canonical-property.md)) property.</span></span> <span data-ttu-id="64011-119">Si la tâche a une date d’échéance, la valeur doit avoir un composant d’heure de minuit et la propriété **dispidCommonEnd** ([PidLidCommonEnd](pidlidcommonend-canonical-property.md)) doit également être définie.</span><span class="sxs-lookup"><span data-stu-id="64011-119">If the task has a due date, the value must have a time component of midnight, and the **dispidCommonEnd** ([PidLidCommonEnd](pidlidcommonend-canonical-property.md)) property must also be set.</span></span> <span data-ttu-id="64011-120">Si **dispidTaskStartDate** a une date de début, la valeur de la propriété **dispidTaskDueDate** doit être supérieure ou égale à la valeur de **dispidTaskStartDate**.</span><span class="sxs-lookup"><span data-stu-id="64011-120">If **dispidTaskStartDate** has a start date, then the value of the **dispidTaskDueDate** property must be greater than or equal to the value of **dispidTaskStartDate**.</span></span>
  
## <a name="related-resources"></a><span data-ttu-id="64011-121">Ressources connexes</span><span class="sxs-lookup"><span data-stu-id="64011-121">Related resources</span></span>

### <a name="protocol-specifications"></a><span data-ttu-id="64011-122">Spécifications de protocole</span><span class="sxs-lookup"><span data-stu-id="64011-122">Protocol specifications</span></span>

<span data-ttu-id="64011-123">[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="64011-123">[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="64011-124">Fournit des définitions de jeu de propriétés et des références aux spécifications Exchange Server protocole.</span><span class="sxs-lookup"><span data-stu-id="64011-124">Provides property set definitions and references to related Exchange Server protocol specifications.</span></span>
    
<span data-ttu-id="64011-125">[[MS-OXOTASK]](https://msdn.microsoft.com/library/55600ec0-6195-4730-8436-59c7931ef27e%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="64011-125">[[MS-OXOTASK]](https://msdn.microsoft.com/library/55600ec0-6195-4730-8436-59c7931ef27e%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="64011-126">Définit plusieurs objets qui modélisent l’équivalent électronique des tâches, des affectations de tâches et des mises à jour de tâches.</span><span class="sxs-lookup"><span data-stu-id="64011-126">Defines several objects that model the electronic equivalent of tasks, task assignments, and task updates.</span></span>
    
<span data-ttu-id="64011-127">[[MS-OXORMDR]](https://msdn.microsoft.com/library/5454ebcc-e5d1-4da8-a598-d393b101caab%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="64011-127">[[MS-OXORMDR]](https://msdn.microsoft.com/library/5454ebcc-e5d1-4da8-a598-d393b101caab%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="64011-128">Spécifie les propriétés et le modèle d’interaction pour les messages électroniques et autres rappels d’objets.</span><span class="sxs-lookup"><span data-stu-id="64011-128">Specifies the properties and the interaction model for email and other object reminders.</span></span>
    
### <a name="header-files"></a><span data-ttu-id="64011-129">Fichiers d’en-tête</span><span class="sxs-lookup"><span data-stu-id="64011-129">Header files</span></span>

<span data-ttu-id="64011-130">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="64011-130">Mapidefs.h</span></span>
  
> <span data-ttu-id="64011-131">Fournit des définitions de type de données.</span><span class="sxs-lookup"><span data-stu-id="64011-131">Provides data type definitions.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="64011-132">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="64011-132">See also</span></span>



[<span data-ttu-id="64011-133">Propriétés MAPI</span><span class="sxs-lookup"><span data-stu-id="64011-133">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="64011-134">Propriétés canoniques MAPI</span><span class="sxs-lookup"><span data-stu-id="64011-134">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="64011-135">Mappage des noms de propriétés canoniques aux noms MAPI</span><span class="sxs-lookup"><span data-stu-id="64011-135">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="64011-136">Mappage des noms MAPI aux noms de propriétés canoniques</span><span class="sxs-lookup"><span data-stu-id="64011-136">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

