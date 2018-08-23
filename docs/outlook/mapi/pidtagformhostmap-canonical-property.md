---
title: Propriété canonique PidTagFormHostMap
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- PidTagFormHostMap
api_type:
- HeaderDef
ms.assetid: 92742747-cce0-4c54-9ece-1fcf652ac498
description: Dernière modification le 09 mars 2015
ms.openlocfilehash: 8c024f71279fac5dbb3d771442d9fbfb8a50e0f5
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/23/2018
ms.locfileid: "22578870"
---
# <a name="pidtagformhostmap-canonical-property"></a><span data-ttu-id="e91f9-103">Propriété canonique PidTagFormHostMap</span><span class="sxs-lookup"><span data-stu-id="e91f9-103">PidTagFormHostMap Canonical Property</span></span>

  
  
<span data-ttu-id="e91f9-104">**S’applique à**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="e91f9-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="e91f9-105">Contient un mappage de l’hôte des formulaires disponibles.</span><span class="sxs-lookup"><span data-stu-id="e91f9-105">Contains a host map of available forms.</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="e91f9-106">Propriétés associées :</span><span class="sxs-lookup"><span data-stu-id="e91f9-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="e91f9-107">PR_FORM_HOST_MAP</span><span class="sxs-lookup"><span data-stu-id="e91f9-107">PR_FORM_HOST_MAP</span></span>  <br/> |
|<span data-ttu-id="e91f9-108">Identificateur :</span><span class="sxs-lookup"><span data-stu-id="e91f9-108">Identifier:</span></span>  <br/> |<span data-ttu-id="e91f9-109">0x3306</span><span class="sxs-lookup"><span data-stu-id="e91f9-109">0x3306</span></span>  <br/> |
|<span data-ttu-id="e91f9-110">Type de données :</span><span class="sxs-lookup"><span data-stu-id="e91f9-110">Data type:</span></span>  <br/> |<span data-ttu-id="e91f9-111">PT_MV_LONG</span><span class="sxs-lookup"><span data-stu-id="e91f9-111">PT_MV_LONG</span></span>  <br/> |
|<span data-ttu-id="e91f9-112">Domaine :</span><span class="sxs-lookup"><span data-stu-id="e91f9-112">Area:</span></span>  <br/> |<span data-ttu-id="e91f9-113">MAPI courantes</span><span class="sxs-lookup"><span data-stu-id="e91f9-113">MAPI common</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="e91f9-114">Remarques</span><span class="sxs-lookup"><span data-stu-id="e91f9-114">Remarks</span></span>

<span data-ttu-id="e91f9-115">Une application cliente doit mettre à jour cette propriété, ainsi que la propriété **PR_DISPLAY_NAME** ([PidTagDisplayName](pidtagdisplayname-canonical-property.md)), lorsque vous modifiez la structure sous-jacente de l’interface **IMAPIFormProp** .</span><span class="sxs-lookup"><span data-stu-id="e91f9-115">A client application should update this property, along with the **PR_DISPLAY_NAME** ([PidTagDisplayName](pidtagdisplayname-canonical-property.md)) property, when changing the underlying structure in the **IMAPIFormProp** interface.</span></span> 
  
## <a name="related-resources"></a><span data-ttu-id="e91f9-116">Ressources connexes</span><span class="sxs-lookup"><span data-stu-id="e91f9-116">Related resources</span></span>

### <a name="header-files"></a><span data-ttu-id="e91f9-117">Fichiers d’en-tête</span><span class="sxs-lookup"><span data-stu-id="e91f9-117">Header files</span></span>

<span data-ttu-id="e91f9-118">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="e91f9-118">Mapidefs.h</span></span>
  
> <span data-ttu-id="e91f9-119">Fournit des définitions de type de données.</span><span class="sxs-lookup"><span data-stu-id="e91f9-119">Provides data type definitions.</span></span>
    
<span data-ttu-id="e91f9-120">MAPITAGS.h</span><span class="sxs-lookup"><span data-stu-id="e91f9-120">Mapitags.h</span></span>
  
> <span data-ttu-id="e91f9-121">Contient les définitions des propriétés répertoriées en tant que d’autres noms.</span><span class="sxs-lookup"><span data-stu-id="e91f9-121">Contains definitions of properties listed as alternate names.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="e91f9-122">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="e91f9-122">See also</span></span>



[<span data-ttu-id="e91f9-123">Propriétés MAPI</span><span class="sxs-lookup"><span data-stu-id="e91f9-123">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="e91f9-124">Propriétés canoniques MAPI</span><span class="sxs-lookup"><span data-stu-id="e91f9-124">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="e91f9-125">Mappage des noms de propriétés canoniques aux noms MAPI</span><span class="sxs-lookup"><span data-stu-id="e91f9-125">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="e91f9-126">Mappage des noms MAPI aux noms de propriétés canoniques</span><span class="sxs-lookup"><span data-stu-id="e91f9-126">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

