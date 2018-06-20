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
description: 'Derni�re modification�: lundi 9 mars 2015'
ms.openlocfilehash: 20bb23690a0d0833960ba3d1f104585c857c825b
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19786038"
---
# <a name="pidtagfreebusyrangetimestamp-canonical-property"></a><span data-ttu-id="41635-103">Propriété canonique PidTagFreeBusyRangeTimestamp</span><span class="sxs-lookup"><span data-stu-id="41635-103">PidTagFreeBusyRangeTimestamp Canonical Property</span></span>

  
  
<span data-ttu-id="41635-104">**S’applique à**: Outlook</span><span class="sxs-lookup"><span data-stu-id="41635-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="41635-105">Contient l’heure lorsque les données a été publiées.</span><span class="sxs-lookup"><span data-stu-id="41635-105">Contains the time when the data was published.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="41635-106">Propriétés associées :</span><span class="sxs-lookup"><span data-stu-id="41635-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="41635-107">PR_FREEBUSY_RANGE_TIMESTAMP</span><span class="sxs-lookup"><span data-stu-id="41635-107">PR_FREEBUSY_RANGE_TIMESTAMP</span></span>  <br/> |
|<span data-ttu-id="41635-108">Identificateur :</span><span class="sxs-lookup"><span data-stu-id="41635-108">Identifier:</span></span>  <br/> |<span data-ttu-id="41635-109">0x6868</span><span class="sxs-lookup"><span data-stu-id="41635-109">0x6868</span></span>  <br/> |
|<span data-ttu-id="41635-110">Type de données :</span><span class="sxs-lookup"><span data-stu-id="41635-110">Data type:</span></span>  <br/> |<span data-ttu-id="41635-111">PT_SYSTIME</span><span class="sxs-lookup"><span data-stu-id="41635-111">PT_SYSTIME</span></span>  <br/> |
|<span data-ttu-id="41635-112">Zone :</span><span class="sxs-lookup"><span data-stu-id="41635-112">Area:</span></span>  <br/> |<span data-ttu-id="41635-113">Informations de disponibilité</span><span class="sxs-lookup"><span data-stu-id="41635-113">Free/Busy</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="41635-114">Remarques</span><span class="sxs-lookup"><span data-stu-id="41635-114">Remarks</span></span>

<span data-ttu-id="41635-115">Cette propriété est le nombre de minutes depuis minuit, 1er janvier 1601 en temps universel coordonné (UTC).</span><span class="sxs-lookup"><span data-stu-id="41635-115">This property is the number of minutes since midnight, January 1, 1601 in Coordinated Universal Time (UTC).</span></span>
  
## <a name="related-resources"></a><span data-ttu-id="41635-116">Ressources connexes</span><span class="sxs-lookup"><span data-stu-id="41635-116">Related resources</span></span>

### <a name="protocol-specifications"></a><span data-ttu-id="41635-117">Spécifications du protocole</span><span class="sxs-lookup"><span data-stu-id="41635-117">Protocol specifications</span></span>

<span data-ttu-id="41635-118">[[MS-OXPROPS]](http://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="41635-118">[[MS-OXPROPS]](http://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="41635-119">Fournit des références aux spécifications du protocole Exchange Server associées.</span><span class="sxs-lookup"><span data-stu-id="41635-119">Provides references to related Exchange Server protocol specifications.</span></span>
    
<span data-ttu-id="41635-120">[[MS-OXOPFFB]](http://msdn.microsoft.com/library/1a527299-7211-4d27-a74c-b69bd0746320%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="41635-120">[[MS-OXOPFFB]](http://msdn.microsoft.com/library/1a527299-7211-4d27-a74c-b69bd0746320%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="41635-121">Publie la disponibilité d’un utilisateur ou une ressource.</span><span class="sxs-lookup"><span data-stu-id="41635-121">Publishes the availability of a user or resource.</span></span>
    
### <a name="header-files"></a><span data-ttu-id="41635-122">Fichiers d’en-tête</span><span class="sxs-lookup"><span data-stu-id="41635-122">Header files</span></span>

<span data-ttu-id="41635-123">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="41635-123">Mapidefs.h</span></span>
  
> <span data-ttu-id="41635-124">Fournit des définitions de type de données.</span><span class="sxs-lookup"><span data-stu-id="41635-124">Provides data type definitions.</span></span>
    
<span data-ttu-id="41635-125">MAPITAGS.h</span><span class="sxs-lookup"><span data-stu-id="41635-125">Mapitags.h</span></span>
  
> <span data-ttu-id="41635-126">Contient les définitions des propriétés répertoriées en tant que d’autres noms.</span><span class="sxs-lookup"><span data-stu-id="41635-126">Contains definitions of properties listed as alternate names.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="41635-127">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="41635-127">See also</span></span>



[<span data-ttu-id="41635-128">Propriétés MAPI</span><span class="sxs-lookup"><span data-stu-id="41635-128">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="41635-129">Propriétés canoniques MAPI</span><span class="sxs-lookup"><span data-stu-id="41635-129">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="41635-130">Mappage de noms de propriété canonique aux noms MAPI</span><span class="sxs-lookup"><span data-stu-id="41635-130">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="41635-131">Mappage de noms MAPI pour les noms de propriété canonique</span><span class="sxs-lookup"><span data-stu-id="41635-131">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

