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
description: Dernière modification le 9 mars 2015
ms.openlocfilehash: 9a438fb2b1862d44905a63fda3e5f68b7878cd99
ms.sourcegitcommit: ef717c65d8dd41ababffb01eafc443c79950aed4
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 10/04/2018
ms.locfileid: "25384954"
---
# <a name="pidlidtaskresetreminder-canonical-property"></a><span data-ttu-id="98be9-103">Propriété canonique PidLidTaskResetReminder</span><span class="sxs-lookup"><span data-stu-id="98be9-103">PidLidTaskResetReminder Canonical Property</span></span>

  
  
<span data-ttu-id="98be9-104">**S’applique à** : Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="98be9-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="98be9-105">Indique si les instances futures de tâches périodiques doivent rappels, même si **dispidReminderSet** ([PidLidReminderSet](pidlidreminderset-canonical-property.md)) a la valeur FALSE.</span><span class="sxs-lookup"><span data-stu-id="98be9-105">Indicates whether future instances of recurring tasks need reminders, even though **dispidReminderSet** ([PidLidReminderSet](pidlidreminderset-canonical-property.md)) is FALSE.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="98be9-106">Propriétés associées :</span><span class="sxs-lookup"><span data-stu-id="98be9-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="98be9-107">dispidTaskResetReminder</span><span class="sxs-lookup"><span data-stu-id="98be9-107">dispidTaskResetReminder</span></span>  <br/> |
|<span data-ttu-id="98be9-108">Jeu de propriétés :</span><span class="sxs-lookup"><span data-stu-id="98be9-108">Property set:</span></span>  <br/> |<span data-ttu-id="98be9-109">PSETID_Task</span><span class="sxs-lookup"><span data-stu-id="98be9-109">PSETID_Task</span></span>  <br/> |
|<span data-ttu-id="98be9-110">ID de type long (capot) :</span><span class="sxs-lookup"><span data-stu-id="98be9-110">Long ID (LID):</span></span>  <br/> |<span data-ttu-id="98be9-111">0x00008107</span><span class="sxs-lookup"><span data-stu-id="98be9-111">0x00008107</span></span>  <br/> |
|<span data-ttu-id="98be9-112">Type de données :</span><span class="sxs-lookup"><span data-stu-id="98be9-112">Data type:</span></span>  <br/> |<span data-ttu-id="98be9-113">PT_BOOLEAN</span><span class="sxs-lookup"><span data-stu-id="98be9-113">PT_BOOLEAN</span></span>  <br/> |
|<span data-ttu-id="98be9-114">Domaine :</span><span class="sxs-lookup"><span data-stu-id="98be9-114">Area:</span></span>  <br/> |<span data-ttu-id="98be9-115">Task</span><span class="sxs-lookup"><span data-stu-id="98be9-115">Task</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="98be9-116">Remarques</span><span class="sxs-lookup"><span data-stu-id="98be9-116">Remarks</span></span>

<span data-ttu-id="98be9-117">Cette valeur est définie sur TRUE lorsque le rappel de la tâche est rejeté et la valeur FALSE dans le cas contraire.</span><span class="sxs-lookup"><span data-stu-id="98be9-117">This value is set to TRUE when the task's reminder is dismissed, and set to FALSE otherwise.</span></span> <span data-ttu-id="98be9-118">Si pas définies, une valeur FALSE par défaut est supposé.</span><span class="sxs-lookup"><span data-stu-id="98be9-118">If left unset, a default of FALSE is assumed.</span></span>
  
<span data-ttu-id="98be9-119">Comme spécifié dans [[MS-OXORMDR]](https://msdn.microsoft.com/library/5454ebcc-e5d1-4da8-a598-d393b101caab%28Office.15%29.aspx), la propriété **dispidReminderSet** indique si un rappel est défini sur la tâche.</span><span class="sxs-lookup"><span data-stu-id="98be9-119">As specified in [[MS-OXORMDR]](https://msdn.microsoft.com/library/5454ebcc-e5d1-4da8-a598-d393b101caab%28Office.15%29.aspx), the **dispidReminderSet** property indicates whether a reminder is set on the task.</span></span> <span data-ttu-id="98be9-120">Toutefois, cette propriété indique uniquement la présence d’un rappel pour une seule tâche.</span><span class="sxs-lookup"><span data-stu-id="98be9-120">However, this property only indicates the presence of a reminder on a single task.</span></span> <span data-ttu-id="98be9-121">Il ne peut pas être utilisé pour déterminer si une instance d’une tâche périodique future nécessite un rappel.</span><span class="sxs-lookup"><span data-stu-id="98be9-121">It cannot be used alone to determine whether a future instance of a recurring task needs a reminder.</span></span> 
  
## <a name="related-resources"></a><span data-ttu-id="98be9-122">Ressources connexes</span><span class="sxs-lookup"><span data-stu-id="98be9-122">Related resources</span></span>

### <a name="protocol-specifications"></a><span data-ttu-id="98be9-123">Spécifications du protocole</span><span class="sxs-lookup"><span data-stu-id="98be9-123">Protocol specifications</span></span>

<span data-ttu-id="98be9-124">[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="98be9-124">[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="98be9-125">Fournit des définitions de jeu de propriétés et des références aux spécifications du protocole Exchange Server connexes.</span><span class="sxs-lookup"><span data-stu-id="98be9-125">Provides property set definitions and references to related Exchange Server protocol specifications.</span></span>
    
<span data-ttu-id="98be9-126">[[MS-OXOTASK]](https://msdn.microsoft.com/library/55600ec0-6195-4730-8436-59c7931ef27e%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="98be9-126">[[MS-OXOTASK]](https://msdn.microsoft.com/library/55600ec0-6195-4730-8436-59c7931ef27e%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="98be9-127">Définit plusieurs objets qui représentent l’équivalent électronique des tâches, les affectations de tâches et les mises à jour de tâche.</span><span class="sxs-lookup"><span data-stu-id="98be9-127">Defines several objects that model the electronic equivalent of tasks, task assignments, and task updates.</span></span>
    
<span data-ttu-id="98be9-128">[[MS-OXORMDR]](https://msdn.microsoft.com/library/5454ebcc-e5d1-4da8-a598-d393b101caab%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="98be9-128">[[MS-OXORMDR]](https://msdn.microsoft.com/library/5454ebcc-e5d1-4da8-a598-d393b101caab%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="98be9-129">Spécifie les propriétés et le modèle d’interaction pour la messagerie et autres rappels de l’objet.</span><span class="sxs-lookup"><span data-stu-id="98be9-129">Specifies the properties and the interaction model for email and other object reminders.</span></span>
    
### <a name="header-files"></a><span data-ttu-id="98be9-130">Fichiers d’en-tête</span><span class="sxs-lookup"><span data-stu-id="98be9-130">Header files</span></span>

<span data-ttu-id="98be9-131">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="98be9-131">Mapidefs.h</span></span>
  
> <span data-ttu-id="98be9-132">Fournit des définitions de type de données.</span><span class="sxs-lookup"><span data-stu-id="98be9-132">Provides data type definitions.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="98be9-133">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="98be9-133">See also</span></span>



[<span data-ttu-id="98be9-134">Propri�t� canonique PidLidReminderSet</span><span class="sxs-lookup"><span data-stu-id="98be9-134">PidLidReminderSet Canonical Property</span></span>](pidlidreminderset-canonical-property.md)


[<span data-ttu-id="98be9-135">Propriétés MAPI</span><span class="sxs-lookup"><span data-stu-id="98be9-135">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="98be9-136">Propriétés canoniques MAPI</span><span class="sxs-lookup"><span data-stu-id="98be9-136">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="98be9-137">Mappage des noms de propriétés canoniques aux noms MAPI</span><span class="sxs-lookup"><span data-stu-id="98be9-137">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="98be9-138">Mappage des noms MAPI aux noms de propriétés canoniques</span><span class="sxs-lookup"><span data-stu-id="98be9-138">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

