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
description: 'Derni�re modification�: lundi 9 mars 2015'
ms.openlocfilehash: 9737b5f940f95c88c2d3c5c6e98fc885daf64219
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19785421"
---
# <a name="pidlidtaskdatecompleted-canonical-property"></a><span data-ttu-id="daed1-103">Propriété canonique PidLidTaskDateCompleted</span><span class="sxs-lookup"><span data-stu-id="daed1-103">PidLidTaskDateCompleted Canonical Property</span></span>

  
  
<span data-ttu-id="daed1-104">**S’applique à**: Outlook</span><span class="sxs-lookup"><span data-stu-id="daed1-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="daed1-105">Spécifie la date lorsque l’utilisateur termine la tâche.</span><span class="sxs-lookup"><span data-stu-id="daed1-105">Specifies the date when the user completes the task.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="daed1-106">Propriétés associées :</span><span class="sxs-lookup"><span data-stu-id="daed1-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="daed1-107">dispidTaskDateCompleted</span><span class="sxs-lookup"><span data-stu-id="daed1-107">dispidTaskDateCompleted</span></span>  <br/> |
|<span data-ttu-id="daed1-108">Jeu de propriétés :</span><span class="sxs-lookup"><span data-stu-id="daed1-108">Property set:</span></span>  <br/> |<span data-ttu-id="daed1-109">PSETID_Task</span><span class="sxs-lookup"><span data-stu-id="daed1-109">PSETID_Task</span></span>  <br/> |
|<span data-ttu-id="daed1-110">ID de type long (capot) :</span><span class="sxs-lookup"><span data-stu-id="daed1-110">Long ID (LID):</span></span>  <br/> |<span data-ttu-id="daed1-111">0x0000810F</span><span class="sxs-lookup"><span data-stu-id="daed1-111">0x0000810F</span></span>  <br/> |
|<span data-ttu-id="daed1-112">Type de données :</span><span class="sxs-lookup"><span data-stu-id="daed1-112">Data type:</span></span>  <br/> |<span data-ttu-id="daed1-113">PT_SYSTIME</span><span class="sxs-lookup"><span data-stu-id="daed1-113">PT_SYSTIME</span></span>  <br/> |
|<span data-ttu-id="daed1-114">Zone :</span><span class="sxs-lookup"><span data-stu-id="daed1-114">Area:</span></span>  <br/> |<span data-ttu-id="daed1-115">Tâche</span><span class="sxs-lookup"><span data-stu-id="daed1-115">Task</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="daed1-116">Remarques</span><span class="sxs-lookup"><span data-stu-id="daed1-116">Remarks</span></span>

<span data-ttu-id="daed1-117">Si la valeur, cette propriété doit avoir un composant de minuit dans le fuseau horaire local, converti en temps universel coordonné (UTC).</span><span class="sxs-lookup"><span data-stu-id="daed1-117">If set, this property must have a time component of midnight in the local time zone, converted to Coordinated Universal Time (UTC).</span></span>
  
## <a name="related-resources"></a><span data-ttu-id="daed1-118">Ressources connexes</span><span class="sxs-lookup"><span data-stu-id="daed1-118">Related resources</span></span>

### <a name="protocol-specifications"></a><span data-ttu-id="daed1-119">Spécifications du protocole</span><span class="sxs-lookup"><span data-stu-id="daed1-119">Protocol specifications</span></span>

<span data-ttu-id="daed1-120">[[MS-OXPROPS]](http://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="daed1-120">[[MS-OXPROPS]](http://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="daed1-121">Fournit des définitions de jeu de propriétés et des références aux spécifications du protocole Exchange Server connexes.</span><span class="sxs-lookup"><span data-stu-id="daed1-121">Provides property set definitions and references to related Exchange Server protocol specifications.</span></span>
    
<span data-ttu-id="daed1-122">[[MS-OXOTASK]](http://msdn.microsoft.com/library/55600ec0-6195-4730-8436-59c7931ef27e%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="daed1-122">[[MS-OXOTASK]](http://msdn.microsoft.com/library/55600ec0-6195-4730-8436-59c7931ef27e%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="daed1-123">Définit plusieurs objets qui représentent l’équivalent électronique des tâches, les affectations de tâches et les mises à jour de tâche.</span><span class="sxs-lookup"><span data-stu-id="daed1-123">Defines several objects that model the electronic equivalent of tasks, task assignments, and task updates.</span></span> 
    
### <a name="header-files"></a><span data-ttu-id="daed1-124">Fichiers d’en-tête</span><span class="sxs-lookup"><span data-stu-id="daed1-124">Header files</span></span>

<span data-ttu-id="daed1-125">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="daed1-125">Mapidefs.h</span></span>
  
> <span data-ttu-id="daed1-126">Fournit des définitions de type de données.</span><span class="sxs-lookup"><span data-stu-id="daed1-126">Provides data type definitions.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="daed1-127">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="daed1-127">See also</span></span>



[<span data-ttu-id="daed1-128">Propriétés MAPI</span><span class="sxs-lookup"><span data-stu-id="daed1-128">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="daed1-129">Propriétés canoniques MAPI</span><span class="sxs-lookup"><span data-stu-id="daed1-129">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="daed1-130">Mappage de noms de propriété canonique aux noms MAPI</span><span class="sxs-lookup"><span data-stu-id="daed1-130">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="daed1-131">Mappage de noms MAPI pour les noms de propriété canonique</span><span class="sxs-lookup"><span data-stu-id="daed1-131">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

