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
ms.openlocfilehash: a31e2862aa3a6265f1dd9f8036abe329cf556276
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19785491"
---
# <a name="pidlidtaskversion-canonical-property"></a><span data-ttu-id="8106b-103">Propriété canonique PidLidTaskVersion</span><span class="sxs-lookup"><span data-stu-id="8106b-103">PidLidTaskVersion Canonical Property</span></span>

  
  
<span data-ttu-id="8106b-104">**S’applique à**: Outlook</span><span class="sxs-lookup"><span data-stu-id="8106b-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="8106b-105">Indique la copie est la dernière mise à jour d’une tâche.</span><span class="sxs-lookup"><span data-stu-id="8106b-105">Indicates which copy is the latest update of a task.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="8106b-106">Propriétés associées :</span><span class="sxs-lookup"><span data-stu-id="8106b-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="8106b-107">dispidTaskVersion</span><span class="sxs-lookup"><span data-stu-id="8106b-107">dispidTaskVersion</span></span>  <br/> |
|<span data-ttu-id="8106b-108">Jeu de propriétés :</span><span class="sxs-lookup"><span data-stu-id="8106b-108">Property set:</span></span>  <br/> |<span data-ttu-id="8106b-109">PSETID_Task</span><span class="sxs-lookup"><span data-stu-id="8106b-109">PSETID_Task</span></span>  <br/> |
|<span data-ttu-id="8106b-110">ID de type long (capot) :</span><span class="sxs-lookup"><span data-stu-id="8106b-110">Long ID (LID):</span></span>  <br/> |<span data-ttu-id="8106b-111">0x00008112</span><span class="sxs-lookup"><span data-stu-id="8106b-111">0x00008112</span></span>  <br/> |
|<span data-ttu-id="8106b-112">Type de données :</span><span class="sxs-lookup"><span data-stu-id="8106b-112">Data type:</span></span>  <br/> |<span data-ttu-id="8106b-113">PT_LONG</span><span class="sxs-lookup"><span data-stu-id="8106b-113">PT_LONG</span></span>  <br/> |
|<span data-ttu-id="8106b-114">Zone :</span><span class="sxs-lookup"><span data-stu-id="8106b-114">Area:</span></span>  <br/> |<span data-ttu-id="8106b-115">Tâche</span><span class="sxs-lookup"><span data-stu-id="8106b-115">Task</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="8106b-116">Remarques</span><span class="sxs-lookup"><span data-stu-id="8106b-116">Remarks</span></span>

<span data-ttu-id="8106b-117">Mises à jour avec des versions inférieures à la tâche sont ignorés.</span><span class="sxs-lookup"><span data-stu-id="8106b-117">Updates with lower versions than the task are ignored.</span></span> 
  
<span data-ttu-id="8106b-118">Lors de l’incorporation d’une tâche dans une communication de la tâche, le client définit la version actuelle de la tâche incorporée sur ainsi que la communication de la tâche.</span><span class="sxs-lookup"><span data-stu-id="8106b-118">When embedding a task in a task communication, the client sets the current version of the embedded task on the task communication as well.</span></span>
  
## <a name="related-resources"></a><span data-ttu-id="8106b-119">Ressources connexes</span><span class="sxs-lookup"><span data-stu-id="8106b-119">Related resources</span></span>

### <a name="protocol-specifications"></a><span data-ttu-id="8106b-120">Spécifications du protocole</span><span class="sxs-lookup"><span data-stu-id="8106b-120">Protocol specifications</span></span>

<span data-ttu-id="8106b-121">[[MS-OXPROPS]](http://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="8106b-121">[[MS-OXPROPS]](http://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="8106b-122">Fournit des définitions de jeu de propriétés et des références aux spécifications du protocole Exchange Server connexes.</span><span class="sxs-lookup"><span data-stu-id="8106b-122">Provides property set definitions and references to related Exchange Server protocol specifications.</span></span>
    
<span data-ttu-id="8106b-123">[[MS-OXOTASK]](http://msdn.microsoft.com/library/55600ec0-6195-4730-8436-59c7931ef27e%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="8106b-123">[[MS-OXOTASK]](http://msdn.microsoft.com/library/55600ec0-6195-4730-8436-59c7931ef27e%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="8106b-124">Définit plusieurs objets qui représentent l’équivalent électronique des tâches, les affectations de tâches et les mises à jour de tâche.</span><span class="sxs-lookup"><span data-stu-id="8106b-124">Defines several objects that model the electronic equivalent of tasks, task assignments, and task updates.</span></span>
    
### <a name="header-files"></a><span data-ttu-id="8106b-125">Fichiers d’en-tête</span><span class="sxs-lookup"><span data-stu-id="8106b-125">Header files</span></span>

<span data-ttu-id="8106b-126">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="8106b-126">Mapidefs.h</span></span>
  
> <span data-ttu-id="8106b-127">Fournit des définitions de type de données.</span><span class="sxs-lookup"><span data-stu-id="8106b-127">Provides data type definitions.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="8106b-128">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="8106b-128">See also</span></span>



[<span data-ttu-id="8106b-129">Propriétés MAPI</span><span class="sxs-lookup"><span data-stu-id="8106b-129">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="8106b-130">Propriétés canoniques MAPI</span><span class="sxs-lookup"><span data-stu-id="8106b-130">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="8106b-131">Mappage de noms de propriété canonique aux noms MAPI</span><span class="sxs-lookup"><span data-stu-id="8106b-131">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="8106b-132">Mappage de noms MAPI pour les noms de propriété canonique</span><span class="sxs-lookup"><span data-stu-id="8106b-132">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

