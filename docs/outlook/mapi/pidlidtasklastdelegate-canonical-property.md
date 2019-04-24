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
ms.openlocfilehash: ddf4b81ed35f500dad0029ea6375e9a75a996186
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32355670"
---
# <a name="pidlidtasklastdelegate-canonical-property"></a><span data-ttu-id="54ba2-103">Propriété canonique PidLidTaskLastDelegate</span><span class="sxs-lookup"><span data-stu-id="54ba2-103">PidLidTaskLastDelegate Canonical Property</span></span>

  
  
<span data-ttu-id="54ba2-104">**S’applique à** : Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="54ba2-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
 <span data-ttu-id="54ba2-105">Nom de l'utilisateur auquel la tâche a été affectée la plus récemment.</span><span class="sxs-lookup"><span data-stu-id="54ba2-105">Names the user who most recently assigned or was assigned the task.</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="54ba2-106">Propriétés associées :</span><span class="sxs-lookup"><span data-stu-id="54ba2-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="54ba2-107">dispidTaskLastDelegate</span><span class="sxs-lookup"><span data-stu-id="54ba2-107">dispidTaskLastDelegate</span></span>  <br/> |
|<span data-ttu-id="54ba2-108">Jeu de propriétés:</span><span class="sxs-lookup"><span data-stu-id="54ba2-108">Property set:</span></span>  <br/> |<span data-ttu-id="54ba2-109">PSETID_Task</span><span class="sxs-lookup"><span data-stu-id="54ba2-109">PSETID_Task</span></span>  <br/> |
|<span data-ttu-id="54ba2-110">ID long (couvercle):</span><span class="sxs-lookup"><span data-stu-id="54ba2-110">Long ID (LID):</span></span>  <br/> |<span data-ttu-id="54ba2-111">0x00008125</span><span class="sxs-lookup"><span data-stu-id="54ba2-111">0x00008125</span></span>  <br/> |
|<span data-ttu-id="54ba2-112">Type de données :</span><span class="sxs-lookup"><span data-stu-id="54ba2-112">Data type:</span></span>  <br/> |<span data-ttu-id="54ba2-113">PT_UNICODE</span><span class="sxs-lookup"><span data-stu-id="54ba2-113">PT_UNICODE</span></span>  <br/> |
|<span data-ttu-id="54ba2-114">Domaine :</span><span class="sxs-lookup"><span data-stu-id="54ba2-114">Area:</span></span>  <br/> |<span data-ttu-id="54ba2-115">Tâche</span><span class="sxs-lookup"><span data-stu-id="54ba2-115">Task</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="54ba2-116">Remarques</span><span class="sxs-lookup"><span data-stu-id="54ba2-116">Remarks</span></span>

<span data-ttu-id="54ba2-117">Avant d'envoyer une demande de tâche, le client définit cette propriété sur le nom de l'attribution de tâches.</span><span class="sxs-lookup"><span data-stu-id="54ba2-117">Before sending a task request, the client sets this property to the name of the task assigner.</span></span> <span data-ttu-id="54ba2-118">Avant d'envoyer une réponse à une tâche, le client définit cette propriété sur le nom de la tâche assignée.</span><span class="sxs-lookup"><span data-stu-id="54ba2-118">Before sending a task response, the client sets this property to the name of the task assignee.</span></span>
  
## <a name="related-resources"></a><span data-ttu-id="54ba2-119">Ressources associées</span><span class="sxs-lookup"><span data-stu-id="54ba2-119">Related resources</span></span>

### <a name="protocol-specifications"></a><span data-ttu-id="54ba2-120">Spécifications de protocole</span><span class="sxs-lookup"><span data-stu-id="54ba2-120">Protocol specifications</span></span>

<span data-ttu-id="54ba2-121">[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="54ba2-121">[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="54ba2-122">Fournit la définition des jeux de propriétés et les références aux spécifications du protocole Exchange Server associé.</span><span class="sxs-lookup"><span data-stu-id="54ba2-122">Provides property set definition and references to related Exchange Server protocol specifications.</span></span>
    
<span data-ttu-id="54ba2-123">[[MS-OXOTASK]](https://msdn.microsoft.com/library/55600ec0-6195-4730-8436-59c7931ef27e%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="54ba2-123">[[MS-OXOTASK]](https://msdn.microsoft.com/library/55600ec0-6195-4730-8436-59c7931ef27e%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="54ba2-124">Définit plusieurs objets qui modélisent l'équivalent électronique des tâches, des affectations de tâches et des mises à jour de tâches.</span><span class="sxs-lookup"><span data-stu-id="54ba2-124">Defines several objects that model the electronic equivalent of tasks, task assignments, and task updates.</span></span>
    
### <a name="header-files"></a><span data-ttu-id="54ba2-125">Fichiers d'en-tête</span><span class="sxs-lookup"><span data-stu-id="54ba2-125">Header files</span></span>

<span data-ttu-id="54ba2-126">Mapidefs. h</span><span class="sxs-lookup"><span data-stu-id="54ba2-126">Mapidefs.h</span></span>
  
> <span data-ttu-id="54ba2-127">Fournit des définitions de type de données.</span><span class="sxs-lookup"><span data-stu-id="54ba2-127">Provides data type definitions.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="54ba2-128">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="54ba2-128">See also</span></span>



[<span data-ttu-id="54ba2-129">Propriétés MAPI</span><span class="sxs-lookup"><span data-stu-id="54ba2-129">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="54ba2-130">Propriétés canoniques MAPI</span><span class="sxs-lookup"><span data-stu-id="54ba2-130">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="54ba2-131">Mappage des noms de propriétés canoniques aux noms MAPI</span><span class="sxs-lookup"><span data-stu-id="54ba2-131">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="54ba2-132">Mappage des noms MAPI aux noms de propriétés canoniques</span><span class="sxs-lookup"><span data-stu-id="54ba2-132">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

