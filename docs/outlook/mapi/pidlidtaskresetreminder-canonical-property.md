---
title: Propriété canonique PidLidTaskResetReminder
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- PidLidTaskResetReminder
api_type:
- COM
ms.assetid: f6da69ff-a913-4a65-bb07-8ad3c5685e5e
description: 'Derni�re modification�: lundi 9 mars 2015'
ms.openlocfilehash: 9a438fb2b1862d44905a63fda3e5f68b7878cd99
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32316617"
---
# <a name="pidlidtaskresetreminder-canonical-property"></a><span data-ttu-id="415ed-103">Propriété canonique PidLidTaskResetReminder</span><span class="sxs-lookup"><span data-stu-id="415ed-103">PidLidTaskResetReminder Canonical Property</span></span>

  
  
<span data-ttu-id="415ed-104">**S’applique à** : Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="415ed-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="415ed-105">Indique si les instances futures des tâches périodiques ont besoin de rappels, même si **dispidReminderSet** ([PidLidReminderSet](pidlidreminderset-canonical-property.md)) a la valeur false.</span><span class="sxs-lookup"><span data-stu-id="415ed-105">Indicates whether future instances of recurring tasks need reminders, even though **dispidReminderSet** ([PidLidReminderSet](pidlidreminderset-canonical-property.md)) is FALSE.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="415ed-106">Propriétés associées :</span><span class="sxs-lookup"><span data-stu-id="415ed-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="415ed-107">dispidTaskResetReminder</span><span class="sxs-lookup"><span data-stu-id="415ed-107">dispidTaskResetReminder</span></span>  <br/> |
|<span data-ttu-id="415ed-108">Jeu de propriétés:</span><span class="sxs-lookup"><span data-stu-id="415ed-108">Property set:</span></span>  <br/> |<span data-ttu-id="415ed-109">PSETID_Task</span><span class="sxs-lookup"><span data-stu-id="415ed-109">PSETID_Task</span></span>  <br/> |
|<span data-ttu-id="415ed-110">ID long (couvercle):</span><span class="sxs-lookup"><span data-stu-id="415ed-110">Long ID (LID):</span></span>  <br/> |<span data-ttu-id="415ed-111">0x00008107</span><span class="sxs-lookup"><span data-stu-id="415ed-111">0x00008107</span></span>  <br/> |
|<span data-ttu-id="415ed-112">Type de données :</span><span class="sxs-lookup"><span data-stu-id="415ed-112">Data type:</span></span>  <br/> |<span data-ttu-id="415ed-113">PT_BOOLEAN</span><span class="sxs-lookup"><span data-stu-id="415ed-113">PT_BOOLEAN</span></span>  <br/> |
|<span data-ttu-id="415ed-114">Domaine :</span><span class="sxs-lookup"><span data-stu-id="415ed-114">Area:</span></span>  <br/> |<span data-ttu-id="415ed-115">Tâche</span><span class="sxs-lookup"><span data-stu-id="415ed-115">Task</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="415ed-116">Remarques</span><span class="sxs-lookup"><span data-stu-id="415ed-116">Remarks</span></span>

<span data-ttu-id="415ed-117">Cette valeur est définie sur TRUE lorsque le rappel de la tâche est fermée et sur FALSe dans le cas contraire.</span><span class="sxs-lookup"><span data-stu-id="415ed-117">This value is set to TRUE when the task's reminder is dismissed, and set to FALSE otherwise.</span></span> <span data-ttu-id="415ed-118">S'il n'est pas défini, la valeur par défaut est «FALSe».</span><span class="sxs-lookup"><span data-stu-id="415ed-118">If left unset, a default of FALSE is assumed.</span></span>
  
<span data-ttu-id="415ed-119">Comme spécifié dans [[MS-OXORMDR]](https://msdn.microsoft.com/library/5454ebcc-e5d1-4da8-a598-d393b101caab%28Office.15%29.aspx), la propriété **dispidReminderSet** indique si un rappel est défini sur la tâche.</span><span class="sxs-lookup"><span data-stu-id="415ed-119">As specified in [[MS-OXORMDR]](https://msdn.microsoft.com/library/5454ebcc-e5d1-4da8-a598-d393b101caab%28Office.15%29.aspx), the **dispidReminderSet** property indicates whether a reminder is set on the task.</span></span> <span data-ttu-id="415ed-120">Toutefois, cette propriété indique uniquement la présence d'un rappel sur une seule tâche.</span><span class="sxs-lookup"><span data-stu-id="415ed-120">However, this property only indicates the presence of a reminder on a single task.</span></span> <span data-ttu-id="415ed-121">Il ne peut pas être utilisé seul pour déterminer si une instance future d'une tâche périodique a besoin d'un rappel.</span><span class="sxs-lookup"><span data-stu-id="415ed-121">It cannot be used alone to determine whether a future instance of a recurring task needs a reminder.</span></span> 
  
## <a name="related-resources"></a><span data-ttu-id="415ed-122">Ressources associées</span><span class="sxs-lookup"><span data-stu-id="415ed-122">Related resources</span></span>

### <a name="protocol-specifications"></a><span data-ttu-id="415ed-123">Spécifications de protocole</span><span class="sxs-lookup"><span data-stu-id="415ed-123">Protocol specifications</span></span>

<span data-ttu-id="415ed-124">[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="415ed-124">[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="415ed-125">Fournit des définitions de jeu de propriétés et des références à des spécifications de protocole Exchange Server connexes.</span><span class="sxs-lookup"><span data-stu-id="415ed-125">Provides property set definitions and references to related Exchange Server protocol specifications.</span></span>
    
<span data-ttu-id="415ed-126">[[MS-OXOTASK]](https://msdn.microsoft.com/library/55600ec0-6195-4730-8436-59c7931ef27e%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="415ed-126">[[MS-OXOTASK]](https://msdn.microsoft.com/library/55600ec0-6195-4730-8436-59c7931ef27e%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="415ed-127">Définit plusieurs objets qui modélisent l'équivalent électronique des tâches, des affectations de tâches et des mises à jour de tâches.</span><span class="sxs-lookup"><span data-stu-id="415ed-127">Defines several objects that model the electronic equivalent of tasks, task assignments, and task updates.</span></span>
    
<span data-ttu-id="415ed-128">[[MS-OXORMDR]](https://msdn.microsoft.com/library/5454ebcc-e5d1-4da8-a598-d393b101caab%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="415ed-128">[[MS-OXORMDR]](https://msdn.microsoft.com/library/5454ebcc-e5d1-4da8-a598-d393b101caab%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="415ed-129">Spécifie les propriétés et le modèle d'interaction pour les rappels de messagerie et d'objet.</span><span class="sxs-lookup"><span data-stu-id="415ed-129">Specifies the properties and the interaction model for email and other object reminders.</span></span>
    
### <a name="header-files"></a><span data-ttu-id="415ed-130">Fichiers d'en-tête</span><span class="sxs-lookup"><span data-stu-id="415ed-130">Header files</span></span>

<span data-ttu-id="415ed-131">Mapidefs. h</span><span class="sxs-lookup"><span data-stu-id="415ed-131">Mapidefs.h</span></span>
  
> <span data-ttu-id="415ed-132">Fournit des définitions de type de données.</span><span class="sxs-lookup"><span data-stu-id="415ed-132">Provides data type definitions.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="415ed-133">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="415ed-133">See also</span></span>



[<span data-ttu-id="415ed-134">Propri�t� canonique PidLidReminderSet</span><span class="sxs-lookup"><span data-stu-id="415ed-134">PidLidReminderSet Canonical Property</span></span>](pidlidreminderset-canonical-property.md)


[<span data-ttu-id="415ed-135">Propriétés MAPI</span><span class="sxs-lookup"><span data-stu-id="415ed-135">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="415ed-136">Propriétés canoniques MAPI</span><span class="sxs-lookup"><span data-stu-id="415ed-136">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="415ed-137">Mappage des noms de propriétés canoniques aux noms MAPI</span><span class="sxs-lookup"><span data-stu-id="415ed-137">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="415ed-138">Mappage des noms MAPI aux noms de propriétés canoniques</span><span class="sxs-lookup"><span data-stu-id="415ed-138">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

