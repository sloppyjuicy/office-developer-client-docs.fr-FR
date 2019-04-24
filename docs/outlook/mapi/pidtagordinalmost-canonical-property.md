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
description: 'Derni�re modification�: lundi 9 mars 2015'
ms.openlocfilehash: 31f39cfbd0e993bfc28003fd64e8af97e7e76818
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32329186"
---
# <a name="pidtagordinalmost-canonical-property"></a><span data-ttu-id="f105a-103">Propriété canonique PidTagOrdinalMost</span><span class="sxs-lookup"><span data-stu-id="f105a-103">PidTagOrdinalMost Canonical Property</span></span>

  
  
<span data-ttu-id="f105a-104">**S’applique à** : Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="f105a-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="f105a-105">Contient un nombre positif dont la valeur négative est inférieure ou égale à la valeur de la propriété **dispidTaskOrdinal** ([PidLidTaskOrdinal](pidlidtaskordinal-canonical-property.md)) de toutes les tâches dans le dossier.</span><span class="sxs-lookup"><span data-stu-id="f105a-105">Contains a positive number whose negative is less than or equal to the value of the **dispidTaskOrdinal** ([PidLidTaskOrdinal](pidlidtaskordinal-canonical-property.md)) property of all tasks in the folder.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="f105a-106">Propriétés associées :</span><span class="sxs-lookup"><span data-stu-id="f105a-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="f105a-107">PR_ORDINAL_MOST</span><span class="sxs-lookup"><span data-stu-id="f105a-107">PR_ORDINAL_MOST</span></span>  <br/> |
|<span data-ttu-id="f105a-108">Identificateur :</span><span class="sxs-lookup"><span data-stu-id="f105a-108">Identifier:</span></span>  <br/> |<span data-ttu-id="f105a-109">0x36E2</span><span class="sxs-lookup"><span data-stu-id="f105a-109">0x36E2</span></span>  <br/> |
|<span data-ttu-id="f105a-110">Type de données :</span><span class="sxs-lookup"><span data-stu-id="f105a-110">Data type:</span></span>  <br/> |<span data-ttu-id="f105a-111">PT_LONG</span><span class="sxs-lookup"><span data-stu-id="f105a-111">PT_LONG</span></span>  <br/> |
|<span data-ttu-id="f105a-112">Domaine :</span><span class="sxs-lookup"><span data-stu-id="f105a-112">Area:</span></span>  <br/> |<span data-ttu-id="f105a-113">Tâche</span><span class="sxs-lookup"><span data-stu-id="f105a-113">Task</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="f105a-114">Remarques</span><span class="sxs-lookup"><span data-stu-id="f105a-114">Remarks</span></span>

<span data-ttu-id="f105a-115">Cette propriété doit être mise à jour pour maintenir cette condition dès que la propriété **dispidTaskOrdinal** de n'importe quel objet Task du dossier change de manière à violer la condition.</span><span class="sxs-lookup"><span data-stu-id="f105a-115">This property must be updated to maintain this condition whenever the **dispidTaskOrdinal** property of any task object in the folder changes in a way that would violate the condition.</span></span> 
  
## <a name="related-resources"></a><span data-ttu-id="f105a-116">Ressources associées</span><span class="sxs-lookup"><span data-stu-id="f105a-116">Related resources</span></span>

### <a name="protocol-specifications"></a><span data-ttu-id="f105a-117">Spécifications de protocole</span><span class="sxs-lookup"><span data-stu-id="f105a-117">Protocol specifications</span></span>

<span data-ttu-id="f105a-118">[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="f105a-118">[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="f105a-119">Fournit des références à des spécifications de protocole Exchange Server connexes.</span><span class="sxs-lookup"><span data-stu-id="f105a-119">Provides references to related Exchange Server protocol specifications.</span></span>
    
<span data-ttu-id="f105a-120">[[MS-OXOTASK]](https://msdn.microsoft.com/library/55600ec0-6195-4730-8436-59c7931ef27e%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="f105a-120">[[MS-OXOTASK]](https://msdn.microsoft.com/library/55600ec0-6195-4730-8436-59c7931ef27e%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="f105a-121">Spécifie les propriétés et les opérations qui sont autorisées pour les contacts et les listes de distribution personnelle.</span><span class="sxs-lookup"><span data-stu-id="f105a-121">Specifies the properties and operations that are permissible for contacts and personal distribution lists.</span></span>
  
### <a name="header-files"></a><span data-ttu-id="f105a-122">Fichiers d'en-tête</span><span class="sxs-lookup"><span data-stu-id="f105a-122">Header files</span></span>

<span data-ttu-id="f105a-123">Mapidefs. h</span><span class="sxs-lookup"><span data-stu-id="f105a-123">Mapidefs.h</span></span>
  
> <span data-ttu-id="f105a-124">Fournit des définitions de type de données.</span><span class="sxs-lookup"><span data-stu-id="f105a-124">Provides data type definitions.</span></span>
    
<span data-ttu-id="f105a-125">Mapitags. h</span><span class="sxs-lookup"><span data-stu-id="f105a-125">Mapitags.h</span></span>
  
> <span data-ttu-id="f105a-126">Contient les définitions des propriétés figurant en tant que noms de substitution.</span><span class="sxs-lookup"><span data-stu-id="f105a-126">Contains definitions of properties listed as alternate names.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="f105a-127">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="f105a-127">See also</span></span>



[<span data-ttu-id="f105a-128">Propriétés MAPI</span><span class="sxs-lookup"><span data-stu-id="f105a-128">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="f105a-129">Propriétés canoniques MAPI</span><span class="sxs-lookup"><span data-stu-id="f105a-129">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="f105a-130">Mappage des noms de propriétés canoniques aux noms MAPI</span><span class="sxs-lookup"><span data-stu-id="f105a-130">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="f105a-131">Mappage des noms MAPI aux noms de propriétés canoniques</span><span class="sxs-lookup"><span data-stu-id="f105a-131">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

