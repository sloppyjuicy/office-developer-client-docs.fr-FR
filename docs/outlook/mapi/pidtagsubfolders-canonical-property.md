---
title: Propriété canonique PidTagSubfolders
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- MAPI.PidTagSubfolders
api_type:
- COM
ms.assetid: b456b07b-4d83-46bf-a305-4f322ea7dbd1
description: Dernière modification le 09 mars 2015
ms.openlocfilehash: 93e5510802fe5ff0327d7ed3fc702fa61cd3c1c4
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/23/2018
ms.locfileid: "22565577"
---
# <a name="pidtagsubfolders-canonical-property"></a><span data-ttu-id="744e4-103">Propriété canonique PidTagSubfolders</span><span class="sxs-lookup"><span data-stu-id="744e4-103">PidTagSubfolders Canonical Property</span></span>

  
  
<span data-ttu-id="744e4-104">**S’applique à**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="744e4-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="744e4-105">Contient la valeur TRUE si un dossier contient des sous-dossiers.</span><span class="sxs-lookup"><span data-stu-id="744e4-105">Contains TRUE if a folder contains subfolders.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="744e4-106">Propriétés associées :</span><span class="sxs-lookup"><span data-stu-id="744e4-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="744e4-107">PR_SUBFOLDERS</span><span class="sxs-lookup"><span data-stu-id="744e4-107">PR_SUBFOLDERS</span></span>  <br/> |
|<span data-ttu-id="744e4-108">Identificateur :</span><span class="sxs-lookup"><span data-stu-id="744e4-108">Identifier:</span></span>  <br/> |<span data-ttu-id="744e4-109">0x360A</span><span class="sxs-lookup"><span data-stu-id="744e4-109">0x360A</span></span>  <br/> |
|<span data-ttu-id="744e4-110">Type de données :</span><span class="sxs-lookup"><span data-stu-id="744e4-110">Data type:</span></span>  <br/> |<span data-ttu-id="744e4-111">PT_BOOLEAN</span><span class="sxs-lookup"><span data-stu-id="744e4-111">PT_BOOLEAN</span></span>  <br/> |
|<span data-ttu-id="744e4-112">Domaine :</span><span class="sxs-lookup"><span data-stu-id="744e4-112">Area:</span></span>  <br/> |<span data-ttu-id="744e4-113">Conteneur MAPI</span><span class="sxs-lookup"><span data-stu-id="744e4-113">MAPI container</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="744e4-114">Remarques</span><span class="sxs-lookup"><span data-stu-id="744e4-114">Remarks</span></span>

<span data-ttu-id="744e4-115">Banques de messages doivent fournir cette propriété pour tous les dossiers.</span><span class="sxs-lookup"><span data-stu-id="744e4-115">Message stores must supply this property for all folders.</span></span>
  
## <a name="related-resources"></a><span data-ttu-id="744e4-116">Ressources connexes</span><span class="sxs-lookup"><span data-stu-id="744e4-116">Related resources</span></span>

### <a name="protocol-specifications"></a><span data-ttu-id="744e4-117">Spécifications du protocole</span><span class="sxs-lookup"><span data-stu-id="744e4-117">Protocol specifications</span></span>

<span data-ttu-id="744e4-118">[[MS-OXPROPS]](http://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="744e4-118">[[MS-OXPROPS]](http://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="744e4-119">Fournit des références aux spécifications du protocole Exchange Server associées.</span><span class="sxs-lookup"><span data-stu-id="744e4-119">Provides references to related Exchange Server protocol specifications.</span></span>
    
<span data-ttu-id="744e4-120">[[MS-OXCFOLD]](http://msdn.microsoft.com/library/c0f31b95-c07f-486c-98d9-535ed9705fbf%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="744e4-120">[[MS-OXCFOLD]](http://msdn.microsoft.com/library/c0f31b95-c07f-486c-98d9-535ed9705fbf%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="744e4-121">Gère les opérations de dossier.</span><span class="sxs-lookup"><span data-stu-id="744e4-121">Handles folder operations.</span></span>
    
### <a name="header-files"></a><span data-ttu-id="744e4-122">Fichiers d’en-tête</span><span class="sxs-lookup"><span data-stu-id="744e4-122">Header files</span></span>

<span data-ttu-id="744e4-123">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="744e4-123">Mapidefs.h</span></span>
  
> <span data-ttu-id="744e4-124">Fournit des définitions de type de données.</span><span class="sxs-lookup"><span data-stu-id="744e4-124">Provides data type definitions.</span></span>
    
<span data-ttu-id="744e4-125">MAPITAGS.h</span><span class="sxs-lookup"><span data-stu-id="744e4-125">Mapitags.h</span></span>
  
> <span data-ttu-id="744e4-126">Contient les définitions des propriétés répertoriées en tant que d’autres noms.</span><span class="sxs-lookup"><span data-stu-id="744e4-126">Contains definitions of properties listed as alternate names.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="744e4-127">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="744e4-127">See also</span></span>



[<span data-ttu-id="744e4-128">Propriétés MAPI</span><span class="sxs-lookup"><span data-stu-id="744e4-128">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="744e4-129">Propriétés canoniques MAPI</span><span class="sxs-lookup"><span data-stu-id="744e4-129">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="744e4-130">Mappage des noms de propriétés canoniques aux noms MAPI</span><span class="sxs-lookup"><span data-stu-id="744e4-130">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="744e4-131">Mappage des noms MAPI aux noms de propriétés canoniques</span><span class="sxs-lookup"><span data-stu-id="744e4-131">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

