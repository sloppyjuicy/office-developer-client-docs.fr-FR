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
description: 'Derni�re modification�: lundi 9 mars 2015'
ms.openlocfilehash: 6dc2bcf2003ee16fa4a6c66689b6af79653e2d04
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19785465"
---
# <a name="pidlidtasklastuser-canonical-property"></a><span data-ttu-id="9bcfd-103">Propriété canonique PidLidTaskLastUser</span><span class="sxs-lookup"><span data-stu-id="9bcfd-103">PidLidTaskLastUser Canonical Property</span></span>

  
  
<span data-ttu-id="9bcfd-104">**S’applique à**: Outlook</span><span class="sxs-lookup"><span data-stu-id="9bcfd-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="9bcfd-105">Autres noms du dernier utilisateur qui a été propriétaire de la tâche.</span><span class="sxs-lookup"><span data-stu-id="9bcfd-105">Names the most recent user who was the task owner.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="9bcfd-106">Propriétés associées :</span><span class="sxs-lookup"><span data-stu-id="9bcfd-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="9bcfd-107">dispidTaskLastUser</span><span class="sxs-lookup"><span data-stu-id="9bcfd-107">dispidTaskLastUser</span></span>  <br/> |
|<span data-ttu-id="9bcfd-108">Jeu de propriétés :</span><span class="sxs-lookup"><span data-stu-id="9bcfd-108">Property set:</span></span>  <br/> |<span data-ttu-id="9bcfd-109">PSETID_Task</span><span class="sxs-lookup"><span data-stu-id="9bcfd-109">PSETID_Task</span></span>  <br/> |
|<span data-ttu-id="9bcfd-110">ID de type long (capot) :</span><span class="sxs-lookup"><span data-stu-id="9bcfd-110">Long ID (LID):</span></span>  <br/> |<span data-ttu-id="9bcfd-111">0x00008122</span><span class="sxs-lookup"><span data-stu-id="9bcfd-111">0x00008122</span></span>  <br/> |
|<span data-ttu-id="9bcfd-112">Type de données :</span><span class="sxs-lookup"><span data-stu-id="9bcfd-112">Data type:</span></span>  <br/> |<span data-ttu-id="9bcfd-113">PT_UNICODE</span><span class="sxs-lookup"><span data-stu-id="9bcfd-113">PT_UNICODE</span></span>  <br/> |
|<span data-ttu-id="9bcfd-114">Zone :</span><span class="sxs-lookup"><span data-stu-id="9bcfd-114">Area:</span></span>  <br/> |<span data-ttu-id="9bcfd-115">Tâche</span><span class="sxs-lookup"><span data-stu-id="9bcfd-115">Task</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="9bcfd-116">Remarques</span><span class="sxs-lookup"><span data-stu-id="9bcfd-116">Remarks</span></span>

<span data-ttu-id="9bcfd-117">Avant qu’un client envoie une demande de tâche, elle définit cette propriété sur le nom de l’assigne de tâche.</span><span class="sxs-lookup"><span data-stu-id="9bcfd-117">Before a client sends a task request, it sets this property to the name of the task assigner.</span></span> <span data-ttu-id="9bcfd-118">Avant qu’un client envoie une acceptation de la tâche, elle définit cette propriété sur le nom du destinataire de la tâche.</span><span class="sxs-lookup"><span data-stu-id="9bcfd-118">Before a client sends a task acceptance, it sets this property to the name of the task assignee.</span></span> <span data-ttu-id="9bcfd-119">Avant qu’un client envoie un refus de la tâche, il définit cette propriété sur le nom de l’assigne de tâche.</span><span class="sxs-lookup"><span data-stu-id="9bcfd-119">Before a client sends a task rejection, it sets this property to the name of the task assigner.</span></span>
  
## <a name="related-resources"></a><span data-ttu-id="9bcfd-120">Ressources connexes</span><span class="sxs-lookup"><span data-stu-id="9bcfd-120">Related resources</span></span>

### <a name="protocol-specifications"></a><span data-ttu-id="9bcfd-121">Spécifications du protocole</span><span class="sxs-lookup"><span data-stu-id="9bcfd-121">Protocol specifications</span></span>

<span data-ttu-id="9bcfd-122">[[MS-OXPROPS]](http://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="9bcfd-122">[[MS-OXPROPS]](http://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="9bcfd-123">Fournit des définitions de jeu de propriétés et des références aux spécifications du protocole Exchange Server connexes.</span><span class="sxs-lookup"><span data-stu-id="9bcfd-123">Provides property set definitions and references to related Exchange Server protocol specifications.</span></span>
    
<span data-ttu-id="9bcfd-124">[[MS-OXOTASK]](http://msdn.microsoft.com/library/55600ec0-6195-4730-8436-59c7931ef27e%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="9bcfd-124">[[MS-OXOTASK]](http://msdn.microsoft.com/library/55600ec0-6195-4730-8436-59c7931ef27e%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="9bcfd-125">Définit plusieurs objets qui représentent l’équivalent électronique des tâches, les affectations de tâches et les mises à jour de tâche.</span><span class="sxs-lookup"><span data-stu-id="9bcfd-125">Defines several objects that model the electronic equivalent of tasks, task assignments, and task updates.</span></span>
    
### <a name="header-files"></a><span data-ttu-id="9bcfd-126">Fichiers d’en-tête</span><span class="sxs-lookup"><span data-stu-id="9bcfd-126">Header files</span></span>

<span data-ttu-id="9bcfd-127">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="9bcfd-127">Mapidefs.h</span></span>
  
> <span data-ttu-id="9bcfd-128">Fournit des définitions de type de données.</span><span class="sxs-lookup"><span data-stu-id="9bcfd-128">Provides data type definitions.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="9bcfd-129">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="9bcfd-129">See also</span></span>



[<span data-ttu-id="9bcfd-130">Propriétés MAPI</span><span class="sxs-lookup"><span data-stu-id="9bcfd-130">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="9bcfd-131">Propriétés canoniques MAPI</span><span class="sxs-lookup"><span data-stu-id="9bcfd-131">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="9bcfd-132">Mappage de noms de propriété canonique aux noms MAPI</span><span class="sxs-lookup"><span data-stu-id="9bcfd-132">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="9bcfd-133">Mappage de noms MAPI pour les noms de propriété canonique</span><span class="sxs-lookup"><span data-stu-id="9bcfd-133">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

