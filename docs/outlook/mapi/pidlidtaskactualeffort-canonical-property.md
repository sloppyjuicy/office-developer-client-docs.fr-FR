---
title: Propriété canonique PidLidTaskActualEffort
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- PidLidTaskActualEffort
api_type:
- COM
ms.assetid: 8e9a9432-bf50-4333-82ec-fba19dff8006
description: Dernière modification le 09 mars 2015
ms.openlocfilehash: a145a103620d23dae4f6a48c225251e8aecc278e
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/23/2018
ms.locfileid: "22593668"
---
# <a name="pidlidtaskactualeffort-canonical-property"></a><span data-ttu-id="68f65-103">Propriété canonique PidLidTaskActualEffort</span><span class="sxs-lookup"><span data-stu-id="68f65-103">PidLidTaskActualEffort Canonical Property</span></span>

  
  
<span data-ttu-id="68f65-104">**S’applique à**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="68f65-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="68f65-105">Indique le nombre de minutes que l’utilisateur a effectué une tâche.</span><span class="sxs-lookup"><span data-stu-id="68f65-105">Indicates the number of minutes that the user performed a task.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="68f65-106">Propriétés associées :</span><span class="sxs-lookup"><span data-stu-id="68f65-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="68f65-107">dispidTaskActualEffort</span><span class="sxs-lookup"><span data-stu-id="68f65-107">dispidTaskActualEffort</span></span>  <br/> |
|<span data-ttu-id="68f65-108">Jeu de propriétés :</span><span class="sxs-lookup"><span data-stu-id="68f65-108">Property set:</span></span>  <br/> |<span data-ttu-id="68f65-109">PSETID_Task</span><span class="sxs-lookup"><span data-stu-id="68f65-109">PSETID_Task</span></span>  <br/> |
|<span data-ttu-id="68f65-110">ID de type long (capot) :</span><span class="sxs-lookup"><span data-stu-id="68f65-110">Long ID (LID):</span></span>  <br/> |<span data-ttu-id="68f65-111">0x00008110</span><span class="sxs-lookup"><span data-stu-id="68f65-111">0x00008110</span></span>  <br/> |
|<span data-ttu-id="68f65-112">Type de données :</span><span class="sxs-lookup"><span data-stu-id="68f65-112">Data type:</span></span>  <br/> |<span data-ttu-id="68f65-113">PT_LONG</span><span class="sxs-lookup"><span data-stu-id="68f65-113">PT_LONG</span></span>  <br/> |
|<span data-ttu-id="68f65-114">Domaine :</span><span class="sxs-lookup"><span data-stu-id="68f65-114">Area:</span></span>  <br/> |<span data-ttu-id="68f65-115">Task</span><span class="sxs-lookup"><span data-stu-id="68f65-115">Task</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="68f65-116">Remarques</span><span class="sxs-lookup"><span data-stu-id="68f65-116">Remarks</span></span>

<span data-ttu-id="68f65-117">La valeur doit être supérieure ou égale à 0 et inférieur à 0x5AE980DF (1,525,252,319), où 480 minutes égal à un jour et 2 400 minutes égale une semaine (huit heures dans une journée de travail et cinq jours dans une semaine de travail).</span><span class="sxs-lookup"><span data-stu-id="68f65-117">The value must be greater than or equal to 0 and less than 0x5AE980DF (1,525,252,319), where 480 minutes equal one day and 2400 minutes equal one week (eight hours in a work day and five days in a work week).</span></span>
  
## <a name="related-resources"></a><span data-ttu-id="68f65-118">Ressources connexes</span><span class="sxs-lookup"><span data-stu-id="68f65-118">Related resources</span></span>

### <a name="protocol-specifications"></a><span data-ttu-id="68f65-119">Spécifications du protocole</span><span class="sxs-lookup"><span data-stu-id="68f65-119">Protocol specifications</span></span>

<span data-ttu-id="68f65-120">[[MS-OXPROPS]](http://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="68f65-120">[[MS-OXPROPS]](http://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="68f65-121">Fournit des définitions de jeu de propriétés et des références aux spécifications du protocole Exchange Server connexes.</span><span class="sxs-lookup"><span data-stu-id="68f65-121">Provides property set definitions and references to related Exchange Server protocol specifications.</span></span>
    
<span data-ttu-id="68f65-122">[[MS-OXOTASK]](http://msdn.microsoft.com/library/55600ec0-6195-4730-8436-59c7931ef27e%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="68f65-122">[[MS-OXOTASK]](http://msdn.microsoft.com/library/55600ec0-6195-4730-8436-59c7931ef27e%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="68f65-123">Spécifie les propriétés et les opérations qui sont autorisées pour les contacts et les objets de liste de distribution personnelle.</span><span class="sxs-lookup"><span data-stu-id="68f65-123">Specifies the properties and operations that are permissible for contact and personal distribution list objects.</span></span>
    
### <a name="header-files"></a><span data-ttu-id="68f65-124">Fichiers d’en-tête</span><span class="sxs-lookup"><span data-stu-id="68f65-124">Header files</span></span>

<span data-ttu-id="68f65-125">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="68f65-125">Mapidefs.h</span></span>
  
> <span data-ttu-id="68f65-126">Fournit des définitions de type de données.</span><span class="sxs-lookup"><span data-stu-id="68f65-126">Provides data type definitions.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="68f65-127">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="68f65-127">See also</span></span>



[<span data-ttu-id="68f65-128">Propriétés MAPI</span><span class="sxs-lookup"><span data-stu-id="68f65-128">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="68f65-129">Propriétés canoniques MAPI</span><span class="sxs-lookup"><span data-stu-id="68f65-129">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="68f65-130">Mappage des noms de propriétés canoniques aux noms MAPI</span><span class="sxs-lookup"><span data-stu-id="68f65-130">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="68f65-131">Mappage des noms MAPI aux noms de propriétés canoniques</span><span class="sxs-lookup"><span data-stu-id="68f65-131">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

