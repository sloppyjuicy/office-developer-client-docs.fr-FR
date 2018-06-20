---
title: Propriété canonique PidLidTaskGlobalId
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- PidLidTaskGlobalId
api_type:
- COM
ms.assetid: 369d8c78-3cf6-4a55-ba14-9da0377d6ccf
description: 'Derni�re modification�: lundi 9 mars 2015'
ms.openlocfilehash: 33f3b8e7d3d0e0d4461c947aa8e9b3ee66373d2e
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19785449"
---
# <a name="pidlidtaskglobalid-canonical-property"></a><span data-ttu-id="c55c7-103">Propriété canonique PidLidTaskGlobalId</span><span class="sxs-lookup"><span data-stu-id="c55c7-103">PidLidTaskGlobalId Canonical Property</span></span>

  
  
<span data-ttu-id="c55c7-104">**S’applique à**: Outlook</span><span class="sxs-lookup"><span data-stu-id="c55c7-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="c55c7-105">Localise une tâche existante, à l’aide d’un GUID, à la réception d’une réponse de la tâche ou de la mise à jour de tâche.</span><span class="sxs-lookup"><span data-stu-id="c55c7-105">Locates an existing task, by using a GUID, upon receipt of a task response or task update.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="c55c7-106">Propriétés associées :</span><span class="sxs-lookup"><span data-stu-id="c55c7-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="c55c7-107">dispidTaskGlobalObjId</span><span class="sxs-lookup"><span data-stu-id="c55c7-107">dispidTaskGlobalObjId</span></span>  <br/> |
|<span data-ttu-id="c55c7-108">Jeu de propriétés :</span><span class="sxs-lookup"><span data-stu-id="c55c7-108">Property set:</span></span>  <br/> |<span data-ttu-id="c55c7-109">PSETID_Common</span><span class="sxs-lookup"><span data-stu-id="c55c7-109">PSETID_Common</span></span>  <br/> |
|<span data-ttu-id="c55c7-110">ID de type long (capot) :</span><span class="sxs-lookup"><span data-stu-id="c55c7-110">Long ID (LID):</span></span>  <br/> |<span data-ttu-id="c55c7-111">0x00008519</span><span class="sxs-lookup"><span data-stu-id="c55c7-111">0x00008519</span></span>  <br/> |
|<span data-ttu-id="c55c7-112">Type de données :</span><span class="sxs-lookup"><span data-stu-id="c55c7-112">Data type:</span></span>  <br/> |<span data-ttu-id="c55c7-113">PT_BINARY</span><span class="sxs-lookup"><span data-stu-id="c55c7-113">PT_BINARY</span></span>  <br/> |
|<span data-ttu-id="c55c7-114">Zone :</span><span class="sxs-lookup"><span data-stu-id="c55c7-114">Area:</span></span>  <br/> |<span data-ttu-id="c55c7-115">Tâche</span><span class="sxs-lookup"><span data-stu-id="c55c7-115">Task</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="c55c7-116">Remarques</span><span class="sxs-lookup"><span data-stu-id="c55c7-116">Remarks</span></span>

<span data-ttu-id="c55c7-117">Cette propriété est pas définie pour les tâches non affectées.</span><span class="sxs-lookup"><span data-stu-id="c55c7-117">This property is left unset for unassigned tasks.</span></span>
  
## <a name="related-resources"></a><span data-ttu-id="c55c7-118">Ressources connexes</span><span class="sxs-lookup"><span data-stu-id="c55c7-118">Related resources</span></span>

### <a name="protocol-specifications"></a><span data-ttu-id="c55c7-119">Spécifications du protocole</span><span class="sxs-lookup"><span data-stu-id="c55c7-119">Protocol specifications</span></span>

<span data-ttu-id="c55c7-120">[[MS-OXPROPS]](http://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="c55c7-120">[[MS-OXPROPS] ](http://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="c55c7-121">Fournit des définitions de jeu de propriétés et des références aux spécifications du protocole Exchange Server connexes.</span><span class="sxs-lookup"><span data-stu-id="c55c7-121">Provides property set definitions and references to related Exchange Server protocol specifications.</span></span>
    
<span data-ttu-id="c55c7-122">[[MS-OXOTASK]](http://msdn.microsoft.com/library/55600ec0-6195-4730-8436-59c7931ef27e%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="c55c7-122">[[MS-OXOTASK]](http://msdn.microsoft.com/library/55600ec0-6195-4730-8436-59c7931ef27e%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="c55c7-123">Définit plusieurs objets qui représentent l’équivalent électronique des tâches, les affectations de tâches et les mises à jour de tâche.</span><span class="sxs-lookup"><span data-stu-id="c55c7-123">Defines several objects that model the electronic equivalent of tasks, task assignments, and task updates.</span></span>
    
### <a name="header-files"></a><span data-ttu-id="c55c7-124">Fichiers d’en-tête</span><span class="sxs-lookup"><span data-stu-id="c55c7-124">Header files</span></span>

<span data-ttu-id="c55c7-125">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="c55c7-125">Mapidefs.h</span></span>
  
> <span data-ttu-id="c55c7-126">Fournit des définitions de type de données.</span><span class="sxs-lookup"><span data-stu-id="c55c7-126">Provides data type definitions.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="c55c7-127">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="c55c7-127">See also</span></span>



[<span data-ttu-id="c55c7-128">Propriétés MAPI</span><span class="sxs-lookup"><span data-stu-id="c55c7-128">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="c55c7-129">Propriétés canoniques MAPI</span><span class="sxs-lookup"><span data-stu-id="c55c7-129">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="c55c7-130">Mappage de noms de propriété canonique aux noms MAPI</span><span class="sxs-lookup"><span data-stu-id="c55c7-130">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="c55c7-131">Mappage de noms MAPI pour les noms de propriété canonique</span><span class="sxs-lookup"><span data-stu-id="c55c7-131">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

