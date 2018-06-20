---
title: Propriété canonique PidLidTaskAssigners
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- PidLidTaskAssigners
api_type:
- COM
ms.assetid: 07500bd0-bcff-4b03-8ed3-80508875e253
description: 'Derni�re modification�: lundi 9 mars 2015'
ms.openlocfilehash: 89e0b6eae35de9e40dba411afb82e19aa81fb635
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19785429"
---
# <a name="pidlidtaskassigners-canonical-property"></a><span data-ttu-id="ffacc-103">Propriété canonique PidLidTaskAssigners</span><span class="sxs-lookup"><span data-stu-id="ffacc-103">PidLidTaskAssigners Canonical Property</span></span>

  
  
<span data-ttu-id="ffacc-104">**S’applique à**: Outlook</span><span class="sxs-lookup"><span data-stu-id="ffacc-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="ffacc-105">Contient une pile d’entrées qui représentent des assigners de tâche.</span><span class="sxs-lookup"><span data-stu-id="ffacc-105">Contains a stack of entries that represent task assigners.</span></span> <span data-ttu-id="ffacc-106">La plus récente assigne tâche s’affiche en haut de la pile.</span><span class="sxs-lookup"><span data-stu-id="ffacc-106">The most recent task assigner appears at the top of the stack.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="ffacc-107">Propriétés associées :</span><span class="sxs-lookup"><span data-stu-id="ffacc-107">Associated properties:</span></span>  <br/> |<span data-ttu-id="ffacc-108">dispidTaskMyDelegators</span><span class="sxs-lookup"><span data-stu-id="ffacc-108">dispidTaskMyDelegators</span></span>  <br/> |
|<span data-ttu-id="ffacc-109">Jeu de propriétés :</span><span class="sxs-lookup"><span data-stu-id="ffacc-109">Property set:</span></span>  <br/> |<span data-ttu-id="ffacc-110">PSETID_Task</span><span class="sxs-lookup"><span data-stu-id="ffacc-110">PSETID_Task</span></span>  <br/> |
|<span data-ttu-id="ffacc-111">ID de type long (capot) :</span><span class="sxs-lookup"><span data-stu-id="ffacc-111">Long ID (LID):</span></span>  <br/> |<span data-ttu-id="ffacc-112">0x00008117</span><span class="sxs-lookup"><span data-stu-id="ffacc-112">0x00008117</span></span>  <br/> |
|<span data-ttu-id="ffacc-113">Type de données :</span><span class="sxs-lookup"><span data-stu-id="ffacc-113">Data type:</span></span>  <br/> |<span data-ttu-id="ffacc-114">PT_BINARY</span><span class="sxs-lookup"><span data-stu-id="ffacc-114">PT_BINARY</span></span>  <br/> |
|<span data-ttu-id="ffacc-115">Zone :</span><span class="sxs-lookup"><span data-stu-id="ffacc-115">Area:</span></span>  <br/> |<span data-ttu-id="ffacc-116">Tâche</span><span class="sxs-lookup"><span data-stu-id="ffacc-116">Task</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="ffacc-117">Remarques</span><span class="sxs-lookup"><span data-stu-id="ffacc-117">Remarks</span></span>

<span data-ttu-id="ffacc-118">Lorsque le client reçoit une demande de tâche, il ajoute à cette propriété, la structure est définie dans [[MS-OXOTASK]](http://msdn.microsoft.com/library/55600ec0-6195-4730-8436-59c7931ef27e%28Office.15%29.aspx), une entrée qui représente l’expéditeur de la tâche.</span><span class="sxs-lookup"><span data-stu-id="ffacc-118">When the client receives a task request, it appends to this property, which structure is defined in [[MS-OXOTASK]](http://msdn.microsoft.com/library/55600ec0-6195-4730-8436-59c7931ef27e%28Office.15%29.aspx), an entry that represents the task's sender.</span></span> <span data-ttu-id="ffacc-119">Lorsque le client reçoit un refus de la tâche, le client supprime la dernière entrée assigne de tâche à partir de cette propriété.</span><span class="sxs-lookup"><span data-stu-id="ffacc-119">When the client receives a task rejection, the client removes the last task assigner entry from this property.</span></span> <span data-ttu-id="ffacc-120">Lorsque le client envoie une réponse, il l’envoie à la dernière assigne tâche répertoriée dans la valeur de cette propriété.</span><span class="sxs-lookup"><span data-stu-id="ffacc-120">When the client sends a task response, the client sends it to the last task assigner listed in the value of this property.</span></span>
  
## <a name="related-resources"></a><span data-ttu-id="ffacc-121">Ressources connexes</span><span class="sxs-lookup"><span data-stu-id="ffacc-121">Related resources</span></span>

### <a name="protocol-specifications"></a><span data-ttu-id="ffacc-122">Spécifications du protocole</span><span class="sxs-lookup"><span data-stu-id="ffacc-122">Protocol specifications</span></span>

<span data-ttu-id="ffacc-123">[[MS-OXPROPS]](http://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="ffacc-123">[[MS-OXPROPS]](http://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="ffacc-124">Fournit des définitions de jeu de propriétés et des références aux spécifications du protocole Exchange Server connexes.</span><span class="sxs-lookup"><span data-stu-id="ffacc-124">Provides property set definitions and references to related Exchange Server protocol specifications.</span></span>
    
<span data-ttu-id="ffacc-125">[[MS-OXOTASK]](http://msdn.microsoft.com/library/55600ec0-6195-4730-8436-59c7931ef27e%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="ffacc-125">[[MS-OXOTASK]](http://msdn.microsoft.com/library/55600ec0-6195-4730-8436-59c7931ef27e%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="ffacc-126">Définit plusieurs objets qui représentent l’équivalent électronique des tâches, les affectations de tâches et les mises à jour de tâche</span><span class="sxs-lookup"><span data-stu-id="ffacc-126">Defines several objects that model the electronic equivalent of tasks, task assignments, and task updates</span></span> 
    
### <a name="header-files"></a><span data-ttu-id="ffacc-127">Fichiers d’en-tête</span><span class="sxs-lookup"><span data-stu-id="ffacc-127">Header files</span></span>

<span data-ttu-id="ffacc-128">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="ffacc-128">Mapidefs.h</span></span>
  
> <span data-ttu-id="ffacc-129">Fournit des définitions de type de données.</span><span class="sxs-lookup"><span data-stu-id="ffacc-129">Provides data type definitions.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="ffacc-130">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="ffacc-130">See also</span></span>



[<span data-ttu-id="ffacc-131">Propriétés MAPI</span><span class="sxs-lookup"><span data-stu-id="ffacc-131">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="ffacc-132">Propriétés canoniques MAPI</span><span class="sxs-lookup"><span data-stu-id="ffacc-132">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="ffacc-133">Mappage de noms de propriété canonique aux noms MAPI</span><span class="sxs-lookup"><span data-stu-id="ffacc-133">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="ffacc-134">Mappage de noms MAPI pour les noms de propriété canonique</span><span class="sxs-lookup"><span data-stu-id="ffacc-134">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

