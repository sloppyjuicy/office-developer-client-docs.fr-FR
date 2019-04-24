---
title: Propriété canonique PidLidTaskVersion
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- PidLidTaskVersion
api_type:
- COM
ms.assetid: 3ab77f25-ad11-4501-8d35-ef560c07e2f2
description: 'Derni�re modification�: lundi 9 mars 2015'
ms.openlocfilehash: 3daf8a04afc9cf47d808b46f2cee010e15a33cf9
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32356491"
---
# <a name="pidlidtaskversion-canonical-property"></a><span data-ttu-id="63c8f-103">Propriété canonique PidLidTaskVersion</span><span class="sxs-lookup"><span data-stu-id="63c8f-103">PidLidTaskVersion Canonical Property</span></span>

  
  
<span data-ttu-id="63c8f-104">**S’applique à** : Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="63c8f-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="63c8f-105">Indique quelle copie est la dernière mise à jour d'une tâche.</span><span class="sxs-lookup"><span data-stu-id="63c8f-105">Indicates which copy is the latest update of a task.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="63c8f-106">Propriétés associées :</span><span class="sxs-lookup"><span data-stu-id="63c8f-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="63c8f-107">dispidTaskVersion</span><span class="sxs-lookup"><span data-stu-id="63c8f-107">dispidTaskVersion</span></span>  <br/> |
|<span data-ttu-id="63c8f-108">Jeu de propriétés:</span><span class="sxs-lookup"><span data-stu-id="63c8f-108">Property set:</span></span>  <br/> |<span data-ttu-id="63c8f-109">PSETID_Task</span><span class="sxs-lookup"><span data-stu-id="63c8f-109">PSETID_Task</span></span>  <br/> |
|<span data-ttu-id="63c8f-110">ID long (couvercle):</span><span class="sxs-lookup"><span data-stu-id="63c8f-110">Long ID (LID):</span></span>  <br/> |<span data-ttu-id="63c8f-111">0x00008112</span><span class="sxs-lookup"><span data-stu-id="63c8f-111">0x00008112</span></span>  <br/> |
|<span data-ttu-id="63c8f-112">Type de données :</span><span class="sxs-lookup"><span data-stu-id="63c8f-112">Data type:</span></span>  <br/> |<span data-ttu-id="63c8f-113">PT_LONG</span><span class="sxs-lookup"><span data-stu-id="63c8f-113">PT_LONG</span></span>  <br/> |
|<span data-ttu-id="63c8f-114">Domaine :</span><span class="sxs-lookup"><span data-stu-id="63c8f-114">Area:</span></span>  <br/> |<span data-ttu-id="63c8f-115">Tâche</span><span class="sxs-lookup"><span data-stu-id="63c8f-115">Task</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="63c8f-116">Remarques</span><span class="sxs-lookup"><span data-stu-id="63c8f-116">Remarks</span></span>

<span data-ttu-id="63c8f-117">Les mises à jour dont les versions sont inférieures à la tâche sont ignorées.</span><span class="sxs-lookup"><span data-stu-id="63c8f-117">Updates with lower versions than the task are ignored.</span></span> 
  
<span data-ttu-id="63c8f-118">Lors de l'incorporation d'une tâche dans une communication de tâches, le client définit également la version actuelle de la tâche incorporée sur la communication de tâche.</span><span class="sxs-lookup"><span data-stu-id="63c8f-118">When embedding a task in a task communication, the client sets the current version of the embedded task on the task communication as well.</span></span>
  
## <a name="related-resources"></a><span data-ttu-id="63c8f-119">Ressources associées</span><span class="sxs-lookup"><span data-stu-id="63c8f-119">Related resources</span></span>

### <a name="protocol-specifications"></a><span data-ttu-id="63c8f-120">Spécifications de protocole</span><span class="sxs-lookup"><span data-stu-id="63c8f-120">Protocol specifications</span></span>

<span data-ttu-id="63c8f-121">[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="63c8f-121">[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="63c8f-122">Fournit des définitions de jeu de propriétés et des références à des spécifications de protocole Exchange Server connexes.</span><span class="sxs-lookup"><span data-stu-id="63c8f-122">Provides property set definitions and references to related Exchange Server protocol specifications.</span></span>
    
<span data-ttu-id="63c8f-123">[[MS-OXOTASK]](https://msdn.microsoft.com/library/55600ec0-6195-4730-8436-59c7931ef27e%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="63c8f-123">[[MS-OXOTASK]](https://msdn.microsoft.com/library/55600ec0-6195-4730-8436-59c7931ef27e%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="63c8f-124">Définit plusieurs objets qui modélisent l'équivalent électronique des tâches, des affectations de tâches et des mises à jour de tâches.</span><span class="sxs-lookup"><span data-stu-id="63c8f-124">Defines several objects that model the electronic equivalent of tasks, task assignments, and task updates.</span></span>
    
### <a name="header-files"></a><span data-ttu-id="63c8f-125">Fichiers d'en-tête</span><span class="sxs-lookup"><span data-stu-id="63c8f-125">Header files</span></span>

<span data-ttu-id="63c8f-126">Mapidefs. h</span><span class="sxs-lookup"><span data-stu-id="63c8f-126">Mapidefs.h</span></span>
  
> <span data-ttu-id="63c8f-127">Fournit des définitions de type de données.</span><span class="sxs-lookup"><span data-stu-id="63c8f-127">Provides data type definitions.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="63c8f-128">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="63c8f-128">See also</span></span>



[<span data-ttu-id="63c8f-129">Propriétés MAPI</span><span class="sxs-lookup"><span data-stu-id="63c8f-129">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="63c8f-130">Propriétés canoniques MAPI</span><span class="sxs-lookup"><span data-stu-id="63c8f-130">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="63c8f-131">Mappage des noms de propriétés canoniques aux noms MAPI</span><span class="sxs-lookup"><span data-stu-id="63c8f-131">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="63c8f-132">Mappage des noms MAPI aux noms de propriétés canoniques</span><span class="sxs-lookup"><span data-stu-id="63c8f-132">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

