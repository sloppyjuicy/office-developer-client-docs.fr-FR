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
description: Dernière modification le 9 mars 2015
ms.openlocfilehash: 8de14542c0d2a4e6d95fb4258697b827f82b8d06
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32339248"
---
# <a name="pidtagsubfolders-canonical-property"></a><span data-ttu-id="48b78-103">Propriété canonique PidTagSubfolders</span><span class="sxs-lookup"><span data-stu-id="48b78-103">PidTagSubfolders Canonical Property</span></span>

  
  
<span data-ttu-id="48b78-104">**S’applique à** : Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="48b78-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="48b78-105">Contient TRUE si un dossier contient des sous-dossiers.</span><span class="sxs-lookup"><span data-stu-id="48b78-105">Contains TRUE if a folder contains subfolders.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="48b78-106">Propriétés associées :</span><span class="sxs-lookup"><span data-stu-id="48b78-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="48b78-107">PR_SUBFOLDERS</span><span class="sxs-lookup"><span data-stu-id="48b78-107">PR_SUBFOLDERS</span></span>  <br/> |
|<span data-ttu-id="48b78-108">Identificateur :</span><span class="sxs-lookup"><span data-stu-id="48b78-108">Identifier:</span></span>  <br/> |<span data-ttu-id="48b78-109">0x360A</span><span class="sxs-lookup"><span data-stu-id="48b78-109">0x360A</span></span>  <br/> |
|<span data-ttu-id="48b78-110">Type de données :</span><span class="sxs-lookup"><span data-stu-id="48b78-110">Data type:</span></span>  <br/> |<span data-ttu-id="48b78-111">PT_BOOLEAN</span><span class="sxs-lookup"><span data-stu-id="48b78-111">PT_BOOLEAN</span></span>  <br/> |
|<span data-ttu-id="48b78-112">Domaine :</span><span class="sxs-lookup"><span data-stu-id="48b78-112">Area:</span></span>  <br/> |<span data-ttu-id="48b78-113">Conteneur MAPI</span><span class="sxs-lookup"><span data-stu-id="48b78-113">MAPI container</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="48b78-114">Remarques</span><span class="sxs-lookup"><span data-stu-id="48b78-114">Remarks</span></span>

<span data-ttu-id="48b78-115">Les magasins de messages doivent fournir cette propriété pour tous les dossiers.</span><span class="sxs-lookup"><span data-stu-id="48b78-115">Message stores must supply this property for all folders.</span></span>
  
## <a name="related-resources"></a><span data-ttu-id="48b78-116">Ressources connexes</span><span class="sxs-lookup"><span data-stu-id="48b78-116">Related resources</span></span>

### <a name="protocol-specifications"></a><span data-ttu-id="48b78-117">Spécifications de protocole</span><span class="sxs-lookup"><span data-stu-id="48b78-117">Protocol specifications</span></span>

<span data-ttu-id="48b78-118">[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="48b78-118">[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="48b78-119">Fournit des références aux spécifications Exchange Server de protocole associées.</span><span class="sxs-lookup"><span data-stu-id="48b78-119">Provides references to related Exchange Server protocol specifications.</span></span>
    
<span data-ttu-id="48b78-120">[[MS-OXCFOLD]](https://msdn.microsoft.com/library/c0f31b95-c07f-486c-98d9-535ed9705fbf%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="48b78-120">[[MS-OXCFOLD]](https://msdn.microsoft.com/library/c0f31b95-c07f-486c-98d9-535ed9705fbf%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="48b78-121">Gère les opérations de dossier.</span><span class="sxs-lookup"><span data-stu-id="48b78-121">Handles folder operations.</span></span>
    
### <a name="header-files"></a><span data-ttu-id="48b78-122">Fichiers d’en-tête</span><span class="sxs-lookup"><span data-stu-id="48b78-122">Header files</span></span>

<span data-ttu-id="48b78-123">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="48b78-123">Mapidefs.h</span></span>
  
> <span data-ttu-id="48b78-124">Fournit des définitions de type de données.</span><span class="sxs-lookup"><span data-stu-id="48b78-124">Provides data type definitions.</span></span>
    
<span data-ttu-id="48b78-125">Mapitags.h</span><span class="sxs-lookup"><span data-stu-id="48b78-125">Mapitags.h</span></span>
  
> <span data-ttu-id="48b78-126">Contient les définitions des propriétés répertoriées en tant que noms de remplacement.</span><span class="sxs-lookup"><span data-stu-id="48b78-126">Contains definitions of properties listed as alternate names.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="48b78-127">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="48b78-127">See also</span></span>



[<span data-ttu-id="48b78-128">Propriétés MAPI</span><span class="sxs-lookup"><span data-stu-id="48b78-128">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="48b78-129">Propriétés canoniques MAPI</span><span class="sxs-lookup"><span data-stu-id="48b78-129">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="48b78-130">Mappage des noms de propriétés canoniques aux noms MAPI</span><span class="sxs-lookup"><span data-stu-id="48b78-130">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="48b78-131">Mappage des noms MAPI aux noms de propriétés canoniques</span><span class="sxs-lookup"><span data-stu-id="48b78-131">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

