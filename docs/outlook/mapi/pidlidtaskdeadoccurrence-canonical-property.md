---
title: Propriété canonique PidLidTaskDeadOccurrence
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- PidLidTaskDeadOccurrence
api_type:
- COM
ms.assetid: e78287ff-f8cc-45ea-8da8-e7a7359e651c
description: 'Derni�re modification�: lundi 9 mars 2015'
ms.openlocfilehash: 14207e513e935a296ff9b953b92ab1ab9ab41fd2
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19785437"
---
# <a name="pidlidtaskdeadoccurrence-canonical-property"></a><span data-ttu-id="61a70-103">Propriété canonique PidLidTaskDeadOccurrence</span><span class="sxs-lookup"><span data-stu-id="61a70-103">PidLidTaskDeadOccurrence Canonical Property</span></span>

  
  
<span data-ttu-id="61a70-104">**S’applique à**: Outlook</span><span class="sxs-lookup"><span data-stu-id="61a70-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="61a70-105">Indique si les nouvelles occurrences doivent être générés.</span><span class="sxs-lookup"><span data-stu-id="61a70-105">Indicates whether new occurrences must be generated.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="61a70-106">Propriétés associées :</span><span class="sxs-lookup"><span data-stu-id="61a70-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="61a70-107">dispidTaskDeadOccur</span><span class="sxs-lookup"><span data-stu-id="61a70-107">dispidTaskDeadOccur</span></span>  <br/> |
|<span data-ttu-id="61a70-108">Jeu de propriétés :</span><span class="sxs-lookup"><span data-stu-id="61a70-108">Property set:</span></span>  <br/> |<span data-ttu-id="61a70-109">PSETID_Task</span><span class="sxs-lookup"><span data-stu-id="61a70-109">PSETID_Task</span></span>  <br/> |
|<span data-ttu-id="61a70-110">ID de type long (capot) :</span><span class="sxs-lookup"><span data-stu-id="61a70-110">Long ID (LID):</span></span>  <br/> |<span data-ttu-id="61a70-111">0x00008109</span><span class="sxs-lookup"><span data-stu-id="61a70-111">0x00008109</span></span>  <br/> |
|<span data-ttu-id="61a70-112">Type de données :</span><span class="sxs-lookup"><span data-stu-id="61a70-112">Data type:</span></span>  <br/> |<span data-ttu-id="61a70-113">PT_BOOLEAN</span><span class="sxs-lookup"><span data-stu-id="61a70-113">PT_BOOLEAN</span></span>  <br/> |
|<span data-ttu-id="61a70-114">Zone :</span><span class="sxs-lookup"><span data-stu-id="61a70-114">Area:</span></span>  <br/> |<span data-ttu-id="61a70-115">Tâche</span><span class="sxs-lookup"><span data-stu-id="61a70-115">Task</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="61a70-116">Remarques</span><span class="sxs-lookup"><span data-stu-id="61a70-116">Remarks</span></span>

<span data-ttu-id="61a70-117">Une périodicité n’est plus en vigueur lors de sa dernière instance est passée ou son nombre spécifié d’instances a été généré.</span><span class="sxs-lookup"><span data-stu-id="61a70-117">A recurrence pattern is no longer in effect when its final instance is in the past or its specified number of instances has been generated.</span></span> <span data-ttu-id="61a70-118">Le client définit cette propriété sur FALSE pour une nouvelle tâche ou la valeur True lorsqu’il génère la dernière instance d’une tâche périodique.</span><span class="sxs-lookup"><span data-stu-id="61a70-118">The client sets this property to FALSE for a new task or to TRUE when it generates the last instance of a recurring task.</span></span> <span data-ttu-id="61a70-119">Lorsque vous copiez une tâche à générer une nouvelle instance, cette propriété est définie sur TRUE sur la copie, qui est l’instance terminée.</span><span class="sxs-lookup"><span data-stu-id="61a70-119">When you copy a task to generate a new instance, this property is set to TRUE on the copy, which is the completed instance.</span></span>
  
## <a name="related-resources"></a><span data-ttu-id="61a70-120">Ressources connexes</span><span class="sxs-lookup"><span data-stu-id="61a70-120">Related resources</span></span>

### <a name="protocol-specifications"></a><span data-ttu-id="61a70-121">Spécifications du protocole</span><span class="sxs-lookup"><span data-stu-id="61a70-121">Protocol specifications</span></span>

<span data-ttu-id="61a70-122">[[MS-OXPROPS]](http://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="61a70-122">[[MS-OXPROPS]](http://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="61a70-123">Fournit des définitions de jeu de propriétés et des références aux spécifications du protocole Exchange Server connexes.</span><span class="sxs-lookup"><span data-stu-id="61a70-123">Provides property set definitions and references to related Exchange Server protocol specifications.</span></span>
    
<span data-ttu-id="61a70-124">[[MS-OXOTASK]](http://msdn.microsoft.com/library/55600ec0-6195-4730-8436-59c7931ef27e%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="61a70-124">[[MS-OXOTASK]](http://msdn.microsoft.com/library/55600ec0-6195-4730-8436-59c7931ef27e%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="61a70-125">Définit plusieurs objets qui représentent l’équivalent électronique des tâches, les affectations de tâches et les mises à jour de tâche.</span><span class="sxs-lookup"><span data-stu-id="61a70-125">Defines several objects that model the electronic equivalent of tasks, task assignments, and task updates.</span></span> 
    
### <a name="header-files"></a><span data-ttu-id="61a70-126">Fichiers d’en-tête</span><span class="sxs-lookup"><span data-stu-id="61a70-126">Header files</span></span>

<span data-ttu-id="61a70-127">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="61a70-127">Mapidefs.h</span></span>
  
> <span data-ttu-id="61a70-128">Fournit des définitions de type de données.</span><span class="sxs-lookup"><span data-stu-id="61a70-128">Provides data type definitions.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="61a70-129">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="61a70-129">See also</span></span>



[<span data-ttu-id="61a70-130">Propriétés MAPI</span><span class="sxs-lookup"><span data-stu-id="61a70-130">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="61a70-131">Propriétés canoniques MAPI</span><span class="sxs-lookup"><span data-stu-id="61a70-131">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="61a70-132">Mappage de noms de propriété canonique aux noms MAPI</span><span class="sxs-lookup"><span data-stu-id="61a70-132">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="61a70-133">Mappage de noms MAPI pour les noms de propriété canonique</span><span class="sxs-lookup"><span data-stu-id="61a70-133">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

