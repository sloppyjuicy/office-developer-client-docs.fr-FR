---
title: Propriété canonique PidLidTaskAccepted
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- PidLidTaskAccepted
api_type:
- COM
ms.assetid: 8e31f893-b639-43da-a535-662153c82d82
description: Dernière modification le 9 mars 2015
ms.openlocfilehash: 0172bf0d69c3f345b592364be754f58c9e7a4420
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32331282"
---
# <a name="pidlidtaskaccepted-canonical-property"></a><span data-ttu-id="c5b95-103">Propriété canonique PidLidTaskAccepted</span><span class="sxs-lookup"><span data-stu-id="c5b95-103">PidLidTaskAccepted Canonical Property</span></span>

  
  
<span data-ttu-id="c5b95-104">**S’applique à** : Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="c5b95-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="c5b95-105">Indique si une personne à la tâche a répondu à une demande de tâche.</span><span class="sxs-lookup"><span data-stu-id="c5b95-105">Indicates whether a task assignee has replied to a task request.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="c5b95-106">Propriétés associées :</span><span class="sxs-lookup"><span data-stu-id="c5b95-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="c5b95-107">dispidTaskAccepted</span><span class="sxs-lookup"><span data-stu-id="c5b95-107">dispidTaskAccepted</span></span>  <br/> |
|<span data-ttu-id="c5b95-108">Jeu de propriétés :</span><span class="sxs-lookup"><span data-stu-id="c5b95-108">Property set:</span></span>  <br/> |<span data-ttu-id="c5b95-109">PSETID_Task</span><span class="sxs-lookup"><span data-stu-id="c5b95-109">PSETID_Task</span></span>  <br/> |
|<span data-ttu-id="c5b95-110">ID long (LID) :</span><span class="sxs-lookup"><span data-stu-id="c5b95-110">Long ID (LID):</span></span>  <br/> |<span data-ttu-id="c5b95-111">0x00008108</span><span class="sxs-lookup"><span data-stu-id="c5b95-111">0x00008108</span></span>  <br/> |
|<span data-ttu-id="c5b95-112">Type de données :</span><span class="sxs-lookup"><span data-stu-id="c5b95-112">Data type:</span></span>  <br/> |<span data-ttu-id="c5b95-113">PT_BOOLEAN</span><span class="sxs-lookup"><span data-stu-id="c5b95-113">PT_BOOLEAN</span></span>  <br/> |
|<span data-ttu-id="c5b95-114">Domaine :</span><span class="sxs-lookup"><span data-stu-id="c5b95-114">Area:</span></span>  <br/> |<span data-ttu-id="c5b95-115">Tâche</span><span class="sxs-lookup"><span data-stu-id="c5b95-115">Task</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="c5b95-116">Remarques</span><span class="sxs-lookup"><span data-stu-id="c5b95-116">Remarks</span></span>

<span data-ttu-id="c5b95-117">Le client définit cette propriété sur FALSE pour une nouvelle tâche ou sur TRUE lorsqu’une tâche est acceptée ou rejetée.</span><span class="sxs-lookup"><span data-stu-id="c5b95-117">The client sets this property to FALSE for a new task, or the client sets this property to TRUE when a task is either accepted or rejected.</span></span> <span data-ttu-id="c5b95-118">Si la propriété n’est pas jeu, la valeur FALSE est supposée.</span><span class="sxs-lookup"><span data-stu-id="c5b95-118">If the property is left unset, a value of FALSE is assumed.</span></span>
  
## <a name="related-resources"></a><span data-ttu-id="c5b95-119">Ressources connexes</span><span class="sxs-lookup"><span data-stu-id="c5b95-119">Related resources</span></span>

### <a name="protocol-specifications"></a><span data-ttu-id="c5b95-120">Spécifications de protocole</span><span class="sxs-lookup"><span data-stu-id="c5b95-120">Protocol specifications</span></span>

<span data-ttu-id="c5b95-121">[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="c5b95-121">[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="c5b95-122">Fournit des définitions de jeu de propriétés et des références aux spécifications Exchange Server protocole.</span><span class="sxs-lookup"><span data-stu-id="c5b95-122">Provides property set definitions and references to related Exchange Server protocol specifications.</span></span>
    
<span data-ttu-id="c5b95-123">[[MS-OXOTASK]](https://msdn.microsoft.com/library/55600ec0-6195-4730-8436-59c7931ef27e%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="c5b95-123">[[MS-OXOTASK]](https://msdn.microsoft.com/library/55600ec0-6195-4730-8436-59c7931ef27e%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="c5b95-124">Spécifie les propriétés et opérations autorisées pour les contacts et les listes de distribution personnelles.</span><span class="sxs-lookup"><span data-stu-id="c5b95-124">Specifies the properties and operations that are permissible for contacts and personal distribution lists.</span></span>
    
### <a name="header-files"></a><span data-ttu-id="c5b95-125">Fichiers d’en-tête</span><span class="sxs-lookup"><span data-stu-id="c5b95-125">Header files</span></span>

<span data-ttu-id="c5b95-126">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="c5b95-126">Mapidefs.h</span></span>
  
> <span data-ttu-id="c5b95-127">Fournit des définitions de type de données.</span><span class="sxs-lookup"><span data-stu-id="c5b95-127">Provides data type definitions.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="c5b95-128">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="c5b95-128">See also</span></span>



[<span data-ttu-id="c5b95-129">Propriétés MAPI</span><span class="sxs-lookup"><span data-stu-id="c5b95-129">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="c5b95-130">Propriétés canoniques MAPI</span><span class="sxs-lookup"><span data-stu-id="c5b95-130">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="c5b95-131">Mappage des noms de propriétés canoniques aux noms MAPI</span><span class="sxs-lookup"><span data-stu-id="c5b95-131">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="c5b95-132">Mappage des noms MAPI aux noms de propriétés canoniques</span><span class="sxs-lookup"><span data-stu-id="c5b95-132">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

