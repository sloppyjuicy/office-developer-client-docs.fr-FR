---
title: Propriété canonique PidLidTaskEstimatedEffort
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- PidLidTaskEstimatedEffort
api_type:
- COM
ms.assetid: c84167d8-f726-45c6-9b21-bcde64473148
description: Dernière modification le 09 mars 2015
ms.openlocfilehash: 987188db4a3aceb4b065f59cdf449f943f68e70d
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/23/2018
ms.locfileid: "22565318"
---
# <a name="pidlidtaskestimatedeffort-canonical-property"></a><span data-ttu-id="91004-103">Propriété canonique PidLidTaskEstimatedEffort</span><span class="sxs-lookup"><span data-stu-id="91004-103">PidLidTaskEstimatedEffort Canonical Property</span></span>

  
  
<span data-ttu-id="91004-104">**S’applique à**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="91004-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="91004-105">Indique la quantité de temps, en minutes, pendant laquelle l’utilisateur souhaite effectuer une tâche.</span><span class="sxs-lookup"><span data-stu-id="91004-105">Indicates the amount of time, in minutes, that the user expects to perform a task.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="91004-106">Propriétés associées :</span><span class="sxs-lookup"><span data-stu-id="91004-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="91004-107">dispidTaskEstimatedEffort</span><span class="sxs-lookup"><span data-stu-id="91004-107">dispidTaskEstimatedEffort</span></span>  <br/> |
|<span data-ttu-id="91004-108">Jeu de propriétés :</span><span class="sxs-lookup"><span data-stu-id="91004-108">Property set:</span></span>  <br/> |<span data-ttu-id="91004-109">PSETID_Task</span><span class="sxs-lookup"><span data-stu-id="91004-109">PSETID_Task</span></span>  <br/> |
|<span data-ttu-id="91004-110">ID de type long (capot) :</span><span class="sxs-lookup"><span data-stu-id="91004-110">Long ID (LID):</span></span>  <br/> |<span data-ttu-id="91004-111">0x00008111</span><span class="sxs-lookup"><span data-stu-id="91004-111">0x00008111</span></span>  <br/> |
|<span data-ttu-id="91004-112">Type de données :</span><span class="sxs-lookup"><span data-stu-id="91004-112">Data type:</span></span>  <br/> |<span data-ttu-id="91004-113">PT_LONG</span><span class="sxs-lookup"><span data-stu-id="91004-113">PT_LONG</span></span>  <br/> |
|<span data-ttu-id="91004-114">Domaine :</span><span class="sxs-lookup"><span data-stu-id="91004-114">Area:</span></span>  <br/> |<span data-ttu-id="91004-115">Task</span><span class="sxs-lookup"><span data-stu-id="91004-115">Task</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="91004-116">Remarques</span><span class="sxs-lookup"><span data-stu-id="91004-116">Remarks</span></span>

<span data-ttu-id="91004-117">La valeur doit être supérieure ou égale à 0 et inférieur à 0x5AE980DF (1,525,252,319), où 480 minutes égal à un jour et 2 400 minutes égale une semaine (huit heures dans une journée de travail et cinq jours dans une semaine de travail).</span><span class="sxs-lookup"><span data-stu-id="91004-117">The value must be greater than or equal to 0 and less than 0x5AE980DF (1,525,252,319), where 480 minutes equal one day and 2400 minutes equal one week (eight hours in a work day and five days in a work week).</span></span>
  
## <a name="related-resources"></a><span data-ttu-id="91004-118">Ressources connexes</span><span class="sxs-lookup"><span data-stu-id="91004-118">Related resources</span></span>

### <a name="protocol-specifications"></a><span data-ttu-id="91004-119">Spécifications du protocole</span><span class="sxs-lookup"><span data-stu-id="91004-119">Protocol specifications</span></span>

<span data-ttu-id="91004-120">[[MS-OXPROPS]](http://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="91004-120">[[MS-OXPROPS]](http://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="91004-121">Fournit des définitions de jeu de propriétés et des références aux spécifications du protocole Exchange Server connexes.</span><span class="sxs-lookup"><span data-stu-id="91004-121">Provides property set definitions and references to related Exchange Server protocol specifications.</span></span>
    
<span data-ttu-id="91004-122">[[MS-OXOTASK]](http://msdn.microsoft.com/library/55600ec0-6195-4730-8436-59c7931ef27e%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="91004-122">[[MS-OXOTASK]](http://msdn.microsoft.com/library/55600ec0-6195-4730-8436-59c7931ef27e%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="91004-123">Définit plusieurs objets qui représentent l’équivalent électronique des tâches, les affectations de tâches et les mises à jour de tâche.</span><span class="sxs-lookup"><span data-stu-id="91004-123">Defines several objects that model the electronic equivalent of tasks, task assignments, and task updates.</span></span> 
    
### <a name="header-files"></a><span data-ttu-id="91004-124">Fichiers d’en-tête</span><span class="sxs-lookup"><span data-stu-id="91004-124">Header files</span></span>

<span data-ttu-id="91004-125">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="91004-125">Mapidefs.h</span></span>
  
> <span data-ttu-id="91004-126">Fournit des définitions de type de données.</span><span class="sxs-lookup"><span data-stu-id="91004-126">Provides data type definitions.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="91004-127">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="91004-127">See also</span></span>



[<span data-ttu-id="91004-128">Propriétés MAPI</span><span class="sxs-lookup"><span data-stu-id="91004-128">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="91004-129">Propriétés canoniques MAPI</span><span class="sxs-lookup"><span data-stu-id="91004-129">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="91004-130">Mappage des noms de propriétés canoniques aux noms MAPI</span><span class="sxs-lookup"><span data-stu-id="91004-130">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="91004-131">Mappage des noms MAPI aux noms de propriétés canoniques</span><span class="sxs-lookup"><span data-stu-id="91004-131">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

