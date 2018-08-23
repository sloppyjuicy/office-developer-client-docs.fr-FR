---
title: Propriété canonique PidTagFreeBusyRangeTimestamp
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- PidTagFreeBusyRangeTimestamp
api_type:
- HeaderDef
ms.assetid: 142d955f-f92d-485a-80c9-9c72e82af0f2
description: Dernière modification le 09 mars 2015
ms.openlocfilehash: 6c7dbbaf9d3d8cc09eef8a6ac193e786092bb8cf
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/23/2018
ms.locfileid: "22571450"
---
# <a name="pidtagfreebusyrangetimestamp-canonical-property"></a><span data-ttu-id="db355-103">Propriété canonique PidTagFreeBusyRangeTimestamp</span><span class="sxs-lookup"><span data-stu-id="db355-103">PidTagFreeBusyRangeTimestamp Canonical Property</span></span>

  
  
<span data-ttu-id="db355-104">**S’applique à**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="db355-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="db355-105">Contient l’heure lorsque les données a été publiées.</span><span class="sxs-lookup"><span data-stu-id="db355-105">Contains the time when the data was published.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="db355-106">Propriétés associées :</span><span class="sxs-lookup"><span data-stu-id="db355-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="db355-107">PR_FREEBUSY_RANGE_TIMESTAMP</span><span class="sxs-lookup"><span data-stu-id="db355-107">PR_FREEBUSY_RANGE_TIMESTAMP</span></span>  <br/> |
|<span data-ttu-id="db355-108">Identificateur :</span><span class="sxs-lookup"><span data-stu-id="db355-108">Identifier:</span></span>  <br/> |<span data-ttu-id="db355-109">0x6868</span><span class="sxs-lookup"><span data-stu-id="db355-109">0x6868</span></span>  <br/> |
|<span data-ttu-id="db355-110">Type de données :</span><span class="sxs-lookup"><span data-stu-id="db355-110">Data type:</span></span>  <br/> |<span data-ttu-id="db355-111">PT_SYSTIME</span><span class="sxs-lookup"><span data-stu-id="db355-111">PT_SYSTIME</span></span>  <br/> |
|<span data-ttu-id="db355-112">Domaine :</span><span class="sxs-lookup"><span data-stu-id="db355-112">Area:</span></span>  <br/> |<span data-ttu-id="db355-113">Informations de disponibilité</span><span class="sxs-lookup"><span data-stu-id="db355-113">Free/Busy</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="db355-114">Remarques</span><span class="sxs-lookup"><span data-stu-id="db355-114">Remarks</span></span>

<span data-ttu-id="db355-115">Cette propriété est le nombre de minutes depuis minuit, 1er janvier 1601 en temps universel coordonné (UTC).</span><span class="sxs-lookup"><span data-stu-id="db355-115">This property is the number of minutes since midnight, January 1, 1601 in Coordinated Universal Time (UTC).</span></span>
  
## <a name="related-resources"></a><span data-ttu-id="db355-116">Ressources connexes</span><span class="sxs-lookup"><span data-stu-id="db355-116">Related resources</span></span>

### <a name="protocol-specifications"></a><span data-ttu-id="db355-117">Spécifications du protocole</span><span class="sxs-lookup"><span data-stu-id="db355-117">Protocol specifications</span></span>

<span data-ttu-id="db355-118">[[MS-OXPROPS]](http://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="db355-118">[[MS-OXPROPS]](http://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="db355-119">Fournit des références aux spécifications du protocole Exchange Server associées.</span><span class="sxs-lookup"><span data-stu-id="db355-119">Provides references to related Exchange Server protocol specifications.</span></span>
    
<span data-ttu-id="db355-120">[[MS-OXOPFFB]](http://msdn.microsoft.com/library/1a527299-7211-4d27-a74c-b69bd0746320%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="db355-120">[[MS-OXOPFFB]](http://msdn.microsoft.com/library/1a527299-7211-4d27-a74c-b69bd0746320%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="db355-121">Publie la disponibilité d’un utilisateur ou une ressource.</span><span class="sxs-lookup"><span data-stu-id="db355-121">Publishes the availability of a user or resource.</span></span>
    
### <a name="header-files"></a><span data-ttu-id="db355-122">Fichiers d’en-tête</span><span class="sxs-lookup"><span data-stu-id="db355-122">Header files</span></span>

<span data-ttu-id="db355-123">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="db355-123">Mapidefs.h</span></span>
  
> <span data-ttu-id="db355-124">Fournit des définitions de type de données.</span><span class="sxs-lookup"><span data-stu-id="db355-124">Provides data type definitions.</span></span>
    
<span data-ttu-id="db355-125">MAPITAGS.h</span><span class="sxs-lookup"><span data-stu-id="db355-125">Mapitags.h</span></span>
  
> <span data-ttu-id="db355-126">Contient les définitions des propriétés répertoriées en tant que d’autres noms.</span><span class="sxs-lookup"><span data-stu-id="db355-126">Contains definitions of properties listed as alternate names.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="db355-127">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="db355-127">See also</span></span>



[<span data-ttu-id="db355-128">Propriétés MAPI</span><span class="sxs-lookup"><span data-stu-id="db355-128">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="db355-129">Propriétés canoniques MAPI</span><span class="sxs-lookup"><span data-stu-id="db355-129">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="db355-130">Mappage des noms de propriétés canoniques aux noms MAPI</span><span class="sxs-lookup"><span data-stu-id="db355-130">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="db355-131">Mappage des noms MAPI aux noms de propriétés canoniques</span><span class="sxs-lookup"><span data-stu-id="db355-131">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

