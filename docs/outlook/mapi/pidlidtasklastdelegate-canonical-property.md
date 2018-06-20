---
title: Propriété canonique PidLidTaskLastDelegate
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- PidLidTaskLastDelegate
api_type:
- COM
ms.assetid: 5eb8c1ce-063f-4273-acba-e6f9c994e7d3
description: 'Derni�re modification�: lundi 9 mars 2015'
ms.openlocfilehash: 8e1a343486e78daae45ca7315ba4d29d44b688bc
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19785460"
---
# <a name="pidlidtasklastdelegate-canonical-property"></a><span data-ttu-id="f30d6-103">Propriété canonique PidLidTaskLastDelegate</span><span class="sxs-lookup"><span data-stu-id="f30d6-103">PidLidTaskLastDelegate Canonical Property</span></span>

  
  
<span data-ttu-id="f30d6-104">**S’applique à**: Outlook</span><span class="sxs-lookup"><span data-stu-id="f30d6-104">**Applies to**: Outlook</span></span> 
  
 <span data-ttu-id="f30d6-105">Noms de l’utilisateur qui récemment ou a été affecté à la tâche.</span><span class="sxs-lookup"><span data-stu-id="f30d6-105">Names the user who most recently assigned or was assigned the task.</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="f30d6-106">Propriétés associées :</span><span class="sxs-lookup"><span data-stu-id="f30d6-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="f30d6-107">dispidTaskLastDelegate</span><span class="sxs-lookup"><span data-stu-id="f30d6-107">dispidTaskLastDelegate</span></span>  <br/> |
|<span data-ttu-id="f30d6-108">Jeu de propriétés :</span><span class="sxs-lookup"><span data-stu-id="f30d6-108">Property set:</span></span>  <br/> |<span data-ttu-id="f30d6-109">PSETID_Task</span><span class="sxs-lookup"><span data-stu-id="f30d6-109">PSETID_Task</span></span>  <br/> |
|<span data-ttu-id="f30d6-110">ID de type long (capot) :</span><span class="sxs-lookup"><span data-stu-id="f30d6-110">Long ID (LID):</span></span>  <br/> |<span data-ttu-id="f30d6-111">0x00008125</span><span class="sxs-lookup"><span data-stu-id="f30d6-111">0x00008125</span></span>  <br/> |
|<span data-ttu-id="f30d6-112">Type de données :</span><span class="sxs-lookup"><span data-stu-id="f30d6-112">Data type:</span></span>  <br/> |<span data-ttu-id="f30d6-113">PT_UNICODE</span><span class="sxs-lookup"><span data-stu-id="f30d6-113">PT_UNICODE</span></span>  <br/> |
|<span data-ttu-id="f30d6-114">Zone :</span><span class="sxs-lookup"><span data-stu-id="f30d6-114">Area:</span></span>  <br/> |<span data-ttu-id="f30d6-115">Tâche</span><span class="sxs-lookup"><span data-stu-id="f30d6-115">Task</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="f30d6-116">Remarques</span><span class="sxs-lookup"><span data-stu-id="f30d6-116">Remarks</span></span>

<span data-ttu-id="f30d6-117">Avant d’envoyer une demande de tâche, le client définit cette propriété sur le nom de l’assigne de tâche.</span><span class="sxs-lookup"><span data-stu-id="f30d6-117">Before sending a task request, the client sets this property to the name of the task assigner.</span></span> <span data-ttu-id="f30d6-118">Avant d’envoyer une réponse de la tâche, le client définit cette propriété sur le nom du destinataire de la tâche.</span><span class="sxs-lookup"><span data-stu-id="f30d6-118">Before sending a task response, the client sets this property to the name of the task assignee.</span></span>
  
## <a name="related-resources"></a><span data-ttu-id="f30d6-119">Ressources connexes</span><span class="sxs-lookup"><span data-stu-id="f30d6-119">Related resources</span></span>

### <a name="protocol-specifications"></a><span data-ttu-id="f30d6-120">Spécifications du protocole</span><span class="sxs-lookup"><span data-stu-id="f30d6-120">Protocol specifications</span></span>

<span data-ttu-id="f30d6-121">[[MS-OXPROPS]](http://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="f30d6-121">[[MS-OXPROPS]](http://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="f30d6-122">Fournit une définition de propriété et des références aux spécifications du protocole Exchange Server connexes.</span><span class="sxs-lookup"><span data-stu-id="f30d6-122">Provides property set definition and references to related Exchange Server protocol specifications.</span></span>
    
<span data-ttu-id="f30d6-123">[[MS-OXOTASK]](http://msdn.microsoft.com/library/55600ec0-6195-4730-8436-59c7931ef27e%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="f30d6-123">[[MS-OXOTASK]](http://msdn.microsoft.com/library/55600ec0-6195-4730-8436-59c7931ef27e%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="f30d6-124">Définit plusieurs objets qui représentent l’équivalent électronique des tâches, les affectations de tâches et les mises à jour de tâche.</span><span class="sxs-lookup"><span data-stu-id="f30d6-124">Defines several objects that model the electronic equivalent of tasks, task assignments, and task updates.</span></span>
    
### <a name="header-files"></a><span data-ttu-id="f30d6-125">Fichiers d’en-tête</span><span class="sxs-lookup"><span data-stu-id="f30d6-125">Header files</span></span>

<span data-ttu-id="f30d6-126">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="f30d6-126">Mapidefs.h</span></span>
  
> <span data-ttu-id="f30d6-127">Fournit des définitions de type de données.</span><span class="sxs-lookup"><span data-stu-id="f30d6-127">Provides data type definitions.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="f30d6-128">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="f30d6-128">See also</span></span>



[<span data-ttu-id="f30d6-129">Propriétés MAPI</span><span class="sxs-lookup"><span data-stu-id="f30d6-129">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="f30d6-130">Propriétés canoniques MAPI</span><span class="sxs-lookup"><span data-stu-id="f30d6-130">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="f30d6-131">Mappage de noms de propriété canonique aux noms MAPI</span><span class="sxs-lookup"><span data-stu-id="f30d6-131">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="f30d6-132">Mappage de noms MAPI pour les noms de propriété canonique</span><span class="sxs-lookup"><span data-stu-id="f30d6-132">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

