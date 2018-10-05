---
title: Propriété canonique PidLidTaskDateCompleted
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- PidLidTaskDateCompleted
api_type:
- COM
ms.assetid: ae384529-55e2-4da1-9a41-acc292591a7c
description: Dernière modification le 9 mars 2015
ms.openlocfilehash: 3096e7ab2133d2984be0534cb091d61d2c7157bd
ms.sourcegitcommit: ef717c65d8dd41ababffb01eafc443c79950aed4
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 10/04/2018
ms.locfileid: "25400921"
---
# <a name="pidlidtaskdatecompleted-canonical-property"></a><span data-ttu-id="5173d-103">Propriété canonique PidLidTaskDateCompleted</span><span class="sxs-lookup"><span data-stu-id="5173d-103">PidLidTaskDateCompleted Canonical Property</span></span>

  
  
<span data-ttu-id="5173d-104">**S’applique à** : Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="5173d-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="5173d-105">Spécifie la date lorsque l’utilisateur termine la tâche.</span><span class="sxs-lookup"><span data-stu-id="5173d-105">Specifies the date when the user completes the task.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="5173d-106">Propriétés associées :</span><span class="sxs-lookup"><span data-stu-id="5173d-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="5173d-107">dispidTaskDateCompleted</span><span class="sxs-lookup"><span data-stu-id="5173d-107">dispidTaskDateCompleted</span></span>  <br/> |
|<span data-ttu-id="5173d-108">Jeu de propriétés :</span><span class="sxs-lookup"><span data-stu-id="5173d-108">Property set:</span></span>  <br/> |<span data-ttu-id="5173d-109">PSETID_Task</span><span class="sxs-lookup"><span data-stu-id="5173d-109">PSETID_Task</span></span>  <br/> |
|<span data-ttu-id="5173d-110">ID de type long (capot) :</span><span class="sxs-lookup"><span data-stu-id="5173d-110">Long ID (LID):</span></span>  <br/> |<span data-ttu-id="5173d-111">0x0000810F</span><span class="sxs-lookup"><span data-stu-id="5173d-111">0x0000810F</span></span>  <br/> |
|<span data-ttu-id="5173d-112">Type de données :</span><span class="sxs-lookup"><span data-stu-id="5173d-112">Data type:</span></span>  <br/> |<span data-ttu-id="5173d-113">PT_SYSTIME</span><span class="sxs-lookup"><span data-stu-id="5173d-113">PT_SYSTIME</span></span>  <br/> |
|<span data-ttu-id="5173d-114">Domaine :</span><span class="sxs-lookup"><span data-stu-id="5173d-114">Area:</span></span>  <br/> |<span data-ttu-id="5173d-115">Task</span><span class="sxs-lookup"><span data-stu-id="5173d-115">Task</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="5173d-116">Remarques</span><span class="sxs-lookup"><span data-stu-id="5173d-116">Remarks</span></span>

<span data-ttu-id="5173d-117">Si la valeur, cette propriété doit avoir un composant de minuit dans le fuseau horaire local, converti en temps universel coordonné (UTC).</span><span class="sxs-lookup"><span data-stu-id="5173d-117">If set, this property must have a time component of midnight in the local time zone, converted to Coordinated Universal Time (UTC).</span></span>
  
## <a name="related-resources"></a><span data-ttu-id="5173d-118">Ressources connexes</span><span class="sxs-lookup"><span data-stu-id="5173d-118">Related resources</span></span>

### <a name="protocol-specifications"></a><span data-ttu-id="5173d-119">Spécifications du protocole</span><span class="sxs-lookup"><span data-stu-id="5173d-119">Protocol specifications</span></span>

<span data-ttu-id="5173d-120">[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="5173d-120">[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="5173d-121">Fournit des définitions de jeu de propriétés et des références aux spécifications du protocole Exchange Server connexes.</span><span class="sxs-lookup"><span data-stu-id="5173d-121">Provides property set definitions and references to related Exchange Server protocol specifications.</span></span>
    
<span data-ttu-id="5173d-122">[[MS-OXOTASK]](https://msdn.microsoft.com/library/55600ec0-6195-4730-8436-59c7931ef27e%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="5173d-122">[[MS-OXOTASK]](https://msdn.microsoft.com/library/55600ec0-6195-4730-8436-59c7931ef27e%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="5173d-123">Définit plusieurs objets qui représentent l’équivalent électronique des tâches, les affectations de tâches et les mises à jour de tâche.</span><span class="sxs-lookup"><span data-stu-id="5173d-123">Defines several objects that model the electronic equivalent of tasks, task assignments, and task updates.</span></span> 
    
### <a name="header-files"></a><span data-ttu-id="5173d-124">Fichiers d’en-tête</span><span class="sxs-lookup"><span data-stu-id="5173d-124">Header files</span></span>

<span data-ttu-id="5173d-125">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="5173d-125">Mapidefs.h</span></span>
  
> <span data-ttu-id="5173d-126">Fournit des définitions de type de données.</span><span class="sxs-lookup"><span data-stu-id="5173d-126">Provides data type definitions.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="5173d-127">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="5173d-127">See also</span></span>



[<span data-ttu-id="5173d-128">Propriétés MAPI</span><span class="sxs-lookup"><span data-stu-id="5173d-128">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="5173d-129">Propriétés canoniques MAPI</span><span class="sxs-lookup"><span data-stu-id="5173d-129">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="5173d-130">Mappage des noms de propriétés canoniques aux noms MAPI</span><span class="sxs-lookup"><span data-stu-id="5173d-130">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="5173d-131">Mappage des noms MAPI aux noms de propriétés canoniques</span><span class="sxs-lookup"><span data-stu-id="5173d-131">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

