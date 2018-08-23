---
title: Propriété canonique PidTagOrdinalMost
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- MAPI.PidTagOrdinalMost
api_type:
- COM
ms.assetid: c18de08b-8c28-4cdf-bd2e-b9c650cd6da6
description: Dernière modification le 09 mars 2015
ms.openlocfilehash: 60704464beb162a614d6619b5e74d362b4af4488
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/23/2018
ms.locfileid: "22585107"
---
# <a name="pidtagordinalmost-canonical-property"></a><span data-ttu-id="1c4c1-103">Propriété canonique PidTagOrdinalMost</span><span class="sxs-lookup"><span data-stu-id="1c4c1-103">PidTagOrdinalMost Canonical Property</span></span>

  
  
<span data-ttu-id="1c4c1-104">**S’applique à**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="1c4c1-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="1c4c1-105">Contient un nombre positif dont négatif est inférieure ou égale à la valeur de la propriété **dispidTaskOrdinal** ([PidLidTaskOrdinal](pidlidtaskordinal-canonical-property.md)) de toutes les tâches dans le dossier.</span><span class="sxs-lookup"><span data-stu-id="1c4c1-105">Contains a positive number whose negative is less than or equal to the value of the **dispidTaskOrdinal** ([PidLidTaskOrdinal](pidlidtaskordinal-canonical-property.md)) property of all tasks in the folder.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="1c4c1-106">Propriétés associées :</span><span class="sxs-lookup"><span data-stu-id="1c4c1-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="1c4c1-107">PR_ORDINAL_MOST</span><span class="sxs-lookup"><span data-stu-id="1c4c1-107">PR_ORDINAL_MOST</span></span>  <br/> |
|<span data-ttu-id="1c4c1-108">Identificateur :</span><span class="sxs-lookup"><span data-stu-id="1c4c1-108">Identifier:</span></span>  <br/> |<span data-ttu-id="1c4c1-109">0x36E2</span><span class="sxs-lookup"><span data-stu-id="1c4c1-109">0x36E2</span></span>  <br/> |
|<span data-ttu-id="1c4c1-110">Type de données :</span><span class="sxs-lookup"><span data-stu-id="1c4c1-110">Data type:</span></span>  <br/> |<span data-ttu-id="1c4c1-111">PT_LONG</span><span class="sxs-lookup"><span data-stu-id="1c4c1-111">PT_LONG</span></span>  <br/> |
|<span data-ttu-id="1c4c1-112">Domaine :</span><span class="sxs-lookup"><span data-stu-id="1c4c1-112">Area:</span></span>  <br/> |<span data-ttu-id="1c4c1-113">Task</span><span class="sxs-lookup"><span data-stu-id="1c4c1-113">Task</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="1c4c1-114">Remarques</span><span class="sxs-lookup"><span data-stu-id="1c4c1-114">Remarks</span></span>

<span data-ttu-id="1c4c1-115">Cette propriété doit être mis à jour pour maintenir cette condition à chaque modification de la propriété **dispidTaskOrdinal** de tout objet de tâche dans le dossier d’une manière qui ne respecte pas la condition.</span><span class="sxs-lookup"><span data-stu-id="1c4c1-115">This property must be updated to maintain this condition whenever the **dispidTaskOrdinal** property of any task object in the folder changes in a way that would violate the condition.</span></span> 
  
## <a name="related-resources"></a><span data-ttu-id="1c4c1-116">Ressources connexes</span><span class="sxs-lookup"><span data-stu-id="1c4c1-116">Related resources</span></span>

### <a name="protocol-specifications"></a><span data-ttu-id="1c4c1-117">Spécifications du protocole</span><span class="sxs-lookup"><span data-stu-id="1c4c1-117">Protocol specifications</span></span>

<span data-ttu-id="1c4c1-118">[[MS-OXPROPS]](http://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="1c4c1-118">[[MS-OXPROPS]](http://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="1c4c1-119">Fournit des références aux spécifications du protocole Exchange Server associées.</span><span class="sxs-lookup"><span data-stu-id="1c4c1-119">Provides references to related Exchange Server protocol specifications.</span></span>
    
<span data-ttu-id="1c4c1-120">[[MS-OXOTASK]](http://msdn.microsoft.com/library/55600ec0-6195-4730-8436-59c7931ef27e%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="1c4c1-120">[[MS-OXOTASK]](http://msdn.microsoft.com/library/55600ec0-6195-4730-8436-59c7931ef27e%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="1c4c1-121">Spécifie les propriétés et les opérations qui sont autorisées pour les contacts et les listes de distribution personnelles.</span><span class="sxs-lookup"><span data-stu-id="1c4c1-121">Specifies the properties and operations that are permissible for contacts and personal distribution lists.</span></span>
  
### <a name="header-files"></a><span data-ttu-id="1c4c1-122">Fichiers d’en-tête</span><span class="sxs-lookup"><span data-stu-id="1c4c1-122">Header files</span></span>

<span data-ttu-id="1c4c1-123">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="1c4c1-123">Mapidefs.h</span></span>
  
> <span data-ttu-id="1c4c1-124">Fournit des définitions de type de données.</span><span class="sxs-lookup"><span data-stu-id="1c4c1-124">Provides data type definitions.</span></span>
    
<span data-ttu-id="1c4c1-125">MAPITAGS.h</span><span class="sxs-lookup"><span data-stu-id="1c4c1-125">Mapitags.h</span></span>
  
> <span data-ttu-id="1c4c1-126">Contient les définitions des propriétés répertoriées en tant que d’autres noms.</span><span class="sxs-lookup"><span data-stu-id="1c4c1-126">Contains definitions of properties listed as alternate names.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="1c4c1-127">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="1c4c1-127">See also</span></span>



[<span data-ttu-id="1c4c1-128">Propriétés MAPI</span><span class="sxs-lookup"><span data-stu-id="1c4c1-128">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="1c4c1-129">Propriétés canoniques MAPI</span><span class="sxs-lookup"><span data-stu-id="1c4c1-129">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="1c4c1-130">Mappage des noms de propriétés canoniques aux noms MAPI</span><span class="sxs-lookup"><span data-stu-id="1c4c1-130">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="1c4c1-131">Mappage des noms MAPI aux noms de propriétés canoniques</span><span class="sxs-lookup"><span data-stu-id="1c4c1-131">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

