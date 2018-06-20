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
description: 'Derni�re modification�: lundi 9 mars 2015'
ms.openlocfilehash: d26a686573a9dc178a46b7dfdc5c18485303b7ca
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19785463"
---
# <a name="pidlidtaskduedate-canonical-property"></a><span data-ttu-id="4b346-103">Propriété canonique PidLidTaskDueDate</span><span class="sxs-lookup"><span data-stu-id="4b346-103">PidLidTaskDueDate Canonical Property</span></span>

  
  
<span data-ttu-id="4b346-104">**S’applique à**: Outlook</span><span class="sxs-lookup"><span data-stu-id="4b346-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="4b346-105">Représente la date lorsque l’utilisateur souhaite effectuer la tâche.</span><span class="sxs-lookup"><span data-stu-id="4b346-105">Represents the date when the user expects to complete the task.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="4b346-106">Propriétés associées :</span><span class="sxs-lookup"><span data-stu-id="4b346-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="4b346-107">dispidTaskDueDate</span><span class="sxs-lookup"><span data-stu-id="4b346-107">dispidTaskDueDate</span></span>  <br/> |
|<span data-ttu-id="4b346-108">Jeu de propriétés :</span><span class="sxs-lookup"><span data-stu-id="4b346-108">Property set:</span></span>  <br/> |<span data-ttu-id="4b346-109">PSETID_Task</span><span class="sxs-lookup"><span data-stu-id="4b346-109">PSETID_Task</span></span>  <br/> |
|<span data-ttu-id="4b346-110">ID de type long (capot) :</span><span class="sxs-lookup"><span data-stu-id="4b346-110">Long ID (LID):</span></span>  <br/> |<span data-ttu-id="4b346-111">0x00008105</span><span class="sxs-lookup"><span data-stu-id="4b346-111">0x00008105</span></span>  <br/> |
|<span data-ttu-id="4b346-112">Type de données :</span><span class="sxs-lookup"><span data-stu-id="4b346-112">Data type:</span></span>  <br/> |<span data-ttu-id="4b346-113">PT_SYSTIME</span><span class="sxs-lookup"><span data-stu-id="4b346-113">PT_SYSTIME</span></span>  <br/> |
|<span data-ttu-id="4b346-114">Zone :</span><span class="sxs-lookup"><span data-stu-id="4b346-114">Area:</span></span>  <br/> |<span data-ttu-id="4b346-115">Tâche</span><span class="sxs-lookup"><span data-stu-id="4b346-115">Task</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="4b346-116">Remarques</span><span class="sxs-lookup"><span data-stu-id="4b346-116">Remarks</span></span>

<span data-ttu-id="4b346-117">La tâche n’a aucune date d’échéance si cette propriété est définie ou défini comme 0x5AE980E0 (1,525,252,320).</span><span class="sxs-lookup"><span data-stu-id="4b346-117">The task has no due date if this property is unset or set to 0x5AE980E0 (1,525,252,320).</span></span> <span data-ttu-id="4b346-118">Toutefois, une date d’échéance est facultative uniquement si aucune date de début n’est indiqué dans la propriété **dispidTaskStartDate** ([PidLidTaskStartDate](pidlidtaskstartdate-canonical-property.md)).</span><span class="sxs-lookup"><span data-stu-id="4b346-118">However, a due date is optional only if no start date is indicated in the **dispidTaskStartDate** ([PidLidTaskStartDate](pidlidtaskstartdate-canonical-property.md)) property.</span></span> <span data-ttu-id="4b346-119">Si la tâche a une date d’échéance, la valeur doit avoir un composant de minuit, et la propriété **dispidCommonEnd** ([PidLidCommonEnd](pidlidcommonend-canonical-property.md)) doit également être définie.</span><span class="sxs-lookup"><span data-stu-id="4b346-119">If the task has a due date, the value must have a time component of midnight, and the **dispidCommonEnd** ([PidLidCommonEnd](pidlidcommonend-canonical-property.md)) property must also be set.</span></span> <span data-ttu-id="4b346-120">Si **dispidTaskStartDate** a une date de début, la valeur de la propriété **dispidTaskDueDate** doit être supérieure ou égale à la valeur de **dispidTaskStartDate**.</span><span class="sxs-lookup"><span data-stu-id="4b346-120">If **dispidTaskStartDate** has a start date, then the value of the **dispidTaskDueDate** property must be greater than or equal to the value of **dispidTaskStartDate**.</span></span>
  
## <a name="related-resources"></a><span data-ttu-id="4b346-121">Ressources connexes</span><span class="sxs-lookup"><span data-stu-id="4b346-121">Related resources</span></span>

### <a name="protocol-specifications"></a><span data-ttu-id="4b346-122">Spécifications du protocole</span><span class="sxs-lookup"><span data-stu-id="4b346-122">Protocol specifications</span></span>

<span data-ttu-id="4b346-123">[[MS-OXPROPS]](http://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="4b346-123">[[MS-OXPROPS]](http://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="4b346-124">Fournit des définitions de jeu de propriétés et des références aux spécifications du protocole Exchange Server connexes.</span><span class="sxs-lookup"><span data-stu-id="4b346-124">Provides property set definitions and references to related Exchange Server protocol specifications.</span></span>
    
<span data-ttu-id="4b346-125">[[MS-OXOTASK]](http://msdn.microsoft.com/library/55600ec0-6195-4730-8436-59c7931ef27e%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="4b346-125">[[MS-OXOTASK]](http://msdn.microsoft.com/library/55600ec0-6195-4730-8436-59c7931ef27e%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="4b346-126">Définit plusieurs objets qui représentent l’équivalent électronique des tâches, les affectations de tâches et les mises à jour de tâche.</span><span class="sxs-lookup"><span data-stu-id="4b346-126">Defines several objects that model the electronic equivalent of tasks, task assignments, and task updates.</span></span>
    
<span data-ttu-id="4b346-127">[[MS-OXORMDR]](http://msdn.microsoft.com/library/5454ebcc-e5d1-4da8-a598-d393b101caab%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="4b346-127">[[MS-OXORMDR]](http://msdn.microsoft.com/library/5454ebcc-e5d1-4da8-a598-d393b101caab%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="4b346-128">Spécifie les propriétés et le modèle d’interaction pour la messagerie et autres rappels de l’objet.</span><span class="sxs-lookup"><span data-stu-id="4b346-128">Specifies the properties and the interaction model for email and other object reminders.</span></span>
    
### <a name="header-files"></a><span data-ttu-id="4b346-129">Fichiers d’en-tête</span><span class="sxs-lookup"><span data-stu-id="4b346-129">Header files</span></span>

<span data-ttu-id="4b346-130">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="4b346-130">Mapidefs.h</span></span>
  
> <span data-ttu-id="4b346-131">Fournit des définitions de type de données.</span><span class="sxs-lookup"><span data-stu-id="4b346-131">Provides data type definitions.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="4b346-132">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="4b346-132">See also</span></span>



[<span data-ttu-id="4b346-133">Propriétés MAPI</span><span class="sxs-lookup"><span data-stu-id="4b346-133">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="4b346-134">Propriétés canoniques MAPI</span><span class="sxs-lookup"><span data-stu-id="4b346-134">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="4b346-135">Mappage de noms de propriété canonique aux noms MAPI</span><span class="sxs-lookup"><span data-stu-id="4b346-135">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="4b346-136">Mappage de noms MAPI pour les noms de propriété canonique</span><span class="sxs-lookup"><span data-stu-id="4b346-136">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

