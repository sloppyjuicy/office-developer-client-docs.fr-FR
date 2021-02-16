---
title: Propriété canonique PidLidTaskLastUser
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- PidLidTaskLastUser
api_type:
- COM
ms.assetid: 914c55e9-cb36-46a4-b5ee-382413fa25f9
description: Dernière modification le 9 mars 2015
ms.openlocfilehash: 76311a76001b122bdfd984b9dedc37c2ff878fc7
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32360444"
---
# <a name="pidlidtasklastuser-canonical-property"></a><span data-ttu-id="43fdb-103">Propriété canonique PidLidTaskLastUser</span><span class="sxs-lookup"><span data-stu-id="43fdb-103">PidLidTaskLastUser Canonical Property</span></span>

  
  
<span data-ttu-id="43fdb-104">**S’applique à** : Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="43fdb-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="43fdb-105">Nomme l’utilisateur le plus récent qui était le propriétaire de la tâche.</span><span class="sxs-lookup"><span data-stu-id="43fdb-105">Names the most recent user who was the task owner.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="43fdb-106">Propriétés associées :</span><span class="sxs-lookup"><span data-stu-id="43fdb-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="43fdb-107">dispidTaskLastUser</span><span class="sxs-lookup"><span data-stu-id="43fdb-107">dispidTaskLastUser</span></span>  <br/> |
|<span data-ttu-id="43fdb-108">Jeu de propriétés :</span><span class="sxs-lookup"><span data-stu-id="43fdb-108">Property set:</span></span>  <br/> |<span data-ttu-id="43fdb-109">PSETID_Task</span><span class="sxs-lookup"><span data-stu-id="43fdb-109">PSETID_Task</span></span>  <br/> |
|<span data-ttu-id="43fdb-110">ID long (LID) :</span><span class="sxs-lookup"><span data-stu-id="43fdb-110">Long ID (LID):</span></span>  <br/> |<span data-ttu-id="43fdb-111">0x00008122</span><span class="sxs-lookup"><span data-stu-id="43fdb-111">0x00008122</span></span>  <br/> |
|<span data-ttu-id="43fdb-112">Type de données :</span><span class="sxs-lookup"><span data-stu-id="43fdb-112">Data type:</span></span>  <br/> |<span data-ttu-id="43fdb-113">PT_UNICODE</span><span class="sxs-lookup"><span data-stu-id="43fdb-113">PT_UNICODE</span></span>  <br/> |
|<span data-ttu-id="43fdb-114">Domaine :</span><span class="sxs-lookup"><span data-stu-id="43fdb-114">Area:</span></span>  <br/> |<span data-ttu-id="43fdb-115">Tâche</span><span class="sxs-lookup"><span data-stu-id="43fdb-115">Task</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="43fdb-116">Remarques</span><span class="sxs-lookup"><span data-stu-id="43fdb-116">Remarks</span></span>

<span data-ttu-id="43fdb-117">Avant qu’un client envoie une demande de tâche, il définit cette propriété sur le nom de l’expéditeur de la tâche.</span><span class="sxs-lookup"><span data-stu-id="43fdb-117">Before a client sends a task request, it sets this property to the name of the task assigner.</span></span> <span data-ttu-id="43fdb-118">Avant qu’un client envoie une acceptation de tâche, il définit cette propriété sur le nom de la personne à qui la tâche a été assignée.</span><span class="sxs-lookup"><span data-stu-id="43fdb-118">Before a client sends a task acceptance, it sets this property to the name of the task assignee.</span></span> <span data-ttu-id="43fdb-119">Avant qu’un client envoie un rejet de tâche, il définit cette propriété sur le nom de l’assigneur de tâche.</span><span class="sxs-lookup"><span data-stu-id="43fdb-119">Before a client sends a task rejection, it sets this property to the name of the task assigner.</span></span>
  
## <a name="related-resources"></a><span data-ttu-id="43fdb-120">Ressources connexes</span><span class="sxs-lookup"><span data-stu-id="43fdb-120">Related resources</span></span>

### <a name="protocol-specifications"></a><span data-ttu-id="43fdb-121">Spécifications de protocole</span><span class="sxs-lookup"><span data-stu-id="43fdb-121">Protocol specifications</span></span>

<span data-ttu-id="43fdb-122">[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="43fdb-122">[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="43fdb-123">Fournit des définitions de jeu de propriétés et des références aux spécifications Exchange Server protocole.</span><span class="sxs-lookup"><span data-stu-id="43fdb-123">Provides property set definitions and references to related Exchange Server protocol specifications.</span></span>
    
<span data-ttu-id="43fdb-124">[[MS-OXOTASK]](https://msdn.microsoft.com/library/55600ec0-6195-4730-8436-59c7931ef27e%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="43fdb-124">[[MS-OXOTASK]](https://msdn.microsoft.com/library/55600ec0-6195-4730-8436-59c7931ef27e%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="43fdb-125">Définit plusieurs objets qui modélisent l’équivalent électronique des tâches, des affectations de tâches et des mises à jour de tâches.</span><span class="sxs-lookup"><span data-stu-id="43fdb-125">Defines several objects that model the electronic equivalent of tasks, task assignments, and task updates.</span></span>
    
### <a name="header-files"></a><span data-ttu-id="43fdb-126">Fichiers d’en-tête</span><span class="sxs-lookup"><span data-stu-id="43fdb-126">Header files</span></span>

<span data-ttu-id="43fdb-127">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="43fdb-127">Mapidefs.h</span></span>
  
> <span data-ttu-id="43fdb-128">Fournit des définitions de type de données.</span><span class="sxs-lookup"><span data-stu-id="43fdb-128">Provides data type definitions.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="43fdb-129">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="43fdb-129">See also</span></span>



[<span data-ttu-id="43fdb-130">Propriétés MAPI</span><span class="sxs-lookup"><span data-stu-id="43fdb-130">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="43fdb-131">Propriétés canoniques MAPI</span><span class="sxs-lookup"><span data-stu-id="43fdb-131">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="43fdb-132">Mappage des noms de propriétés canoniques aux noms MAPI</span><span class="sxs-lookup"><span data-stu-id="43fdb-132">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="43fdb-133">Mappage des noms MAPI aux noms de propriétés canoniques</span><span class="sxs-lookup"><span data-stu-id="43fdb-133">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

