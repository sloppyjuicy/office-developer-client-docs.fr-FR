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
description: 'Derni�re modification�: lundi 9 mars 2015'
ms.openlocfilehash: 9e0316ead2adf00619bd87c57946ba72ed01f4b0
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19786039"
---
# <a name="pidtagformhostmap-canonical-property"></a><span data-ttu-id="16584-103">Propriété canonique PidTagFormHostMap</span><span class="sxs-lookup"><span data-stu-id="16584-103">PidTagFormHostMap Canonical Property</span></span>

  
  
<span data-ttu-id="16584-104">**S’applique à**: Outlook</span><span class="sxs-lookup"><span data-stu-id="16584-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="16584-105">Contient un mappage de l’hôte des formulaires disponibles.</span><span class="sxs-lookup"><span data-stu-id="16584-105">Contains a host map of available forms.</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="16584-106">Propriétés associées :</span><span class="sxs-lookup"><span data-stu-id="16584-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="16584-107">PR_FORM_HOST_MAP</span><span class="sxs-lookup"><span data-stu-id="16584-107">PR_FORM_HOST_MAP</span></span>  <br/> |
|<span data-ttu-id="16584-108">Identificateur :</span><span class="sxs-lookup"><span data-stu-id="16584-108">Identifier:</span></span>  <br/> |<span data-ttu-id="16584-109">0x3306</span><span class="sxs-lookup"><span data-stu-id="16584-109">0x3306</span></span>  <br/> |
|<span data-ttu-id="16584-110">Type de données :</span><span class="sxs-lookup"><span data-stu-id="16584-110">Data type:</span></span>  <br/> |<span data-ttu-id="16584-111">PT_MV_LONG</span><span class="sxs-lookup"><span data-stu-id="16584-111">PT_MV_LONG</span></span>  <br/> |
|<span data-ttu-id="16584-112">Zone :</span><span class="sxs-lookup"><span data-stu-id="16584-112">Area:</span></span>  <br/> |<span data-ttu-id="16584-113">MAPI courantes</span><span class="sxs-lookup"><span data-stu-id="16584-113">MAPI common</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="16584-114">Remarques</span><span class="sxs-lookup"><span data-stu-id="16584-114">Remarks</span></span>

<span data-ttu-id="16584-115">Une application cliente doit mettre à jour cette propriété, ainsi que la propriété **PR_DISPLAY_NAME** ([PidTagDisplayName](pidtagdisplayname-canonical-property.md)), lorsque vous modifiez la structure sous-jacente de l’interface **IMAPIFormProp** .</span><span class="sxs-lookup"><span data-stu-id="16584-115">A client application should update this property, along with the **PR_DISPLAY_NAME** ([PidTagDisplayName](pidtagdisplayname-canonical-property.md)) property, when changing the underlying structure in the **IMAPIFormProp** interface.</span></span> 
  
## <a name="related-resources"></a><span data-ttu-id="16584-116">Ressources connexes</span><span class="sxs-lookup"><span data-stu-id="16584-116">Related resources</span></span>

### <a name="header-files"></a><span data-ttu-id="16584-117">Fichiers d’en-tête</span><span class="sxs-lookup"><span data-stu-id="16584-117">Header files</span></span>

<span data-ttu-id="16584-118">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="16584-118">Mapidefs.h</span></span>
  
> <span data-ttu-id="16584-119">Fournit des définitions de type de données.</span><span class="sxs-lookup"><span data-stu-id="16584-119">Provides data type definitions.</span></span>
    
<span data-ttu-id="16584-120">MAPITAGS.h</span><span class="sxs-lookup"><span data-stu-id="16584-120">Mapitags.h</span></span>
  
> <span data-ttu-id="16584-121">Contient les définitions des propriétés répertoriées en tant que d’autres noms.</span><span class="sxs-lookup"><span data-stu-id="16584-121">Contains definitions of properties listed as alternate names.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="16584-122">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="16584-122">See also</span></span>



[<span data-ttu-id="16584-123">Propriétés MAPI</span><span class="sxs-lookup"><span data-stu-id="16584-123">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="16584-124">Propriétés canoniques MAPI</span><span class="sxs-lookup"><span data-stu-id="16584-124">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="16584-125">Mappage de noms de propriété canonique aux noms MAPI</span><span class="sxs-lookup"><span data-stu-id="16584-125">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="16584-126">Mappage de noms MAPI pour les noms de propriété canonique</span><span class="sxs-lookup"><span data-stu-id="16584-126">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

