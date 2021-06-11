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
description: Dernière modification le 9 mars 2015
ms.openlocfilehash: ddf4b81ed35f500dad0029ea6375e9a75a996186
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32355670"
---
# <a name="pidlidtasklastdelegate-canonical-property"></a><span data-ttu-id="58d07-103">Propriété canonique PidLidTaskLastDelegate</span><span class="sxs-lookup"><span data-stu-id="58d07-103">PidLidTaskLastDelegate Canonical Property</span></span>

  
  
<span data-ttu-id="58d07-104">**S’applique à** : Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="58d07-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
 <span data-ttu-id="58d07-105">Nomme l’utilisateur qui a été le plus récemment affecté ou qui a été affecté à la tâche.</span><span class="sxs-lookup"><span data-stu-id="58d07-105">Names the user who most recently assigned or was assigned the task.</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="58d07-106">Propriétés associées :</span><span class="sxs-lookup"><span data-stu-id="58d07-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="58d07-107">dispidTaskLastDelegate</span><span class="sxs-lookup"><span data-stu-id="58d07-107">dispidTaskLastDelegate</span></span>  <br/> |
|<span data-ttu-id="58d07-108">Jeu de propriétés :</span><span class="sxs-lookup"><span data-stu-id="58d07-108">Property set:</span></span>  <br/> |<span data-ttu-id="58d07-109">PSETID_Task</span><span class="sxs-lookup"><span data-stu-id="58d07-109">PSETID_Task</span></span>  <br/> |
|<span data-ttu-id="58d07-110">ID long (LID) :</span><span class="sxs-lookup"><span data-stu-id="58d07-110">Long ID (LID):</span></span>  <br/> |<span data-ttu-id="58d07-111">0x00008125</span><span class="sxs-lookup"><span data-stu-id="58d07-111">0x00008125</span></span>  <br/> |
|<span data-ttu-id="58d07-112">Type de données :</span><span class="sxs-lookup"><span data-stu-id="58d07-112">Data type:</span></span>  <br/> |<span data-ttu-id="58d07-113">PT_UNICODE</span><span class="sxs-lookup"><span data-stu-id="58d07-113">PT_UNICODE</span></span>  <br/> |
|<span data-ttu-id="58d07-114">Domaine :</span><span class="sxs-lookup"><span data-stu-id="58d07-114">Area:</span></span>  <br/> |<span data-ttu-id="58d07-115">Tâche</span><span class="sxs-lookup"><span data-stu-id="58d07-115">Task</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="58d07-116">Remarques</span><span class="sxs-lookup"><span data-stu-id="58d07-116">Remarks</span></span>

<span data-ttu-id="58d07-117">Avant d’envoyer une demande de tâche, le client définit cette propriété sur le nom de l’assigneur de tâche.</span><span class="sxs-lookup"><span data-stu-id="58d07-117">Before sending a task request, the client sets this property to the name of the task assigner.</span></span> <span data-ttu-id="58d07-118">Avant d’envoyer une réponse de tâche, le client définit cette propriété sur le nom de la personne assignée à la tâche.</span><span class="sxs-lookup"><span data-stu-id="58d07-118">Before sending a task response, the client sets this property to the name of the task assignee.</span></span>
  
## <a name="related-resources"></a><span data-ttu-id="58d07-119">Ressources connexes</span><span class="sxs-lookup"><span data-stu-id="58d07-119">Related resources</span></span>

### <a name="protocol-specifications"></a><span data-ttu-id="58d07-120">Spécifications de protocole</span><span class="sxs-lookup"><span data-stu-id="58d07-120">Protocol specifications</span></span>

<span data-ttu-id="58d07-121">[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="58d07-121">[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="58d07-122">Fournit une définition de jeu de propriétés et des références aux spécifications Exchange Server protocole.</span><span class="sxs-lookup"><span data-stu-id="58d07-122">Provides property set definition and references to related Exchange Server protocol specifications.</span></span>
    
<span data-ttu-id="58d07-123">[[MS-OXOTASK]](https://msdn.microsoft.com/library/55600ec0-6195-4730-8436-59c7931ef27e%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="58d07-123">[[MS-OXOTASK]](https://msdn.microsoft.com/library/55600ec0-6195-4730-8436-59c7931ef27e%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="58d07-124">Définit plusieurs objets qui modélisent l’équivalent électronique des tâches, des affectations de tâches et des mises à jour de tâches.</span><span class="sxs-lookup"><span data-stu-id="58d07-124">Defines several objects that model the electronic equivalent of tasks, task assignments, and task updates.</span></span>
    
### <a name="header-files"></a><span data-ttu-id="58d07-125">Fichiers d’en-tête</span><span class="sxs-lookup"><span data-stu-id="58d07-125">Header files</span></span>

<span data-ttu-id="58d07-126">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="58d07-126">Mapidefs.h</span></span>
  
> <span data-ttu-id="58d07-127">Fournit des définitions de type de données.</span><span class="sxs-lookup"><span data-stu-id="58d07-127">Provides data type definitions.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="58d07-128">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="58d07-128">See also</span></span>



[<span data-ttu-id="58d07-129">Propriétés MAPI</span><span class="sxs-lookup"><span data-stu-id="58d07-129">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="58d07-130">Propriétés canoniques MAPI</span><span class="sxs-lookup"><span data-stu-id="58d07-130">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="58d07-131">Mappage des noms de propriétés canoniques aux noms MAPI</span><span class="sxs-lookup"><span data-stu-id="58d07-131">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="58d07-132">Mappage des noms MAPI aux noms de propriétés canoniques</span><span class="sxs-lookup"><span data-stu-id="58d07-132">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

