---
title: Propriété canonique PidTagContentCount
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- PidTagContentCount
api_type:
- HeaderDef
ms.assetid: 27c75031-a968-4636-98a6-4a5b7422f57c
description: Dernière modification le 09 mars 2015
ms.openlocfilehash: b489e73f9453e5d2ae6657969c2bc18fc9a4620e
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/23/2018
ms.locfileid: "22562938"
---
# <a name="pidtagcontentcount-canonical-property"></a><span data-ttu-id="680f7-103">Propriété canonique PidTagContentCount</span><span class="sxs-lookup"><span data-stu-id="680f7-103">PidTagContentCount Canonical Property</span></span>

  
  
<span data-ttu-id="680f7-104">**S’applique à**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="680f7-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="680f7-105">Contient le nombre de messages dans un dossier, calculé par la banque de messages.</span><span class="sxs-lookup"><span data-stu-id="680f7-105">Contains the number of messages in a folder, as computed by the message store.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="680f7-106">Propriétés associées :</span><span class="sxs-lookup"><span data-stu-id="680f7-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="680f7-107">PR_CONTENT_COUNT</span><span class="sxs-lookup"><span data-stu-id="680f7-107">PR_CONTENT_COUNT</span></span>  <br/> |
|<span data-ttu-id="680f7-108">Identificateur :</span><span class="sxs-lookup"><span data-stu-id="680f7-108">Identifier:</span></span>  <br/> |<span data-ttu-id="680f7-109">0x3602</span><span class="sxs-lookup"><span data-stu-id="680f7-109">0x3602</span></span>  <br/> |
|<span data-ttu-id="680f7-110">Type de données :</span><span class="sxs-lookup"><span data-stu-id="680f7-110">Data type:</span></span>  <br/> |<span data-ttu-id="680f7-111">PT_LONG</span><span class="sxs-lookup"><span data-stu-id="680f7-111">PT_LONG</span></span>  <br/> |
|<span data-ttu-id="680f7-112">Domaine :</span><span class="sxs-lookup"><span data-stu-id="680f7-112">Area:</span></span>  <br/> |<span data-ttu-id="680f7-113">Folder</span><span class="sxs-lookup"><span data-stu-id="680f7-113">Folder</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="680f7-114">Remarques</span><span class="sxs-lookup"><span data-stu-id="680f7-114">Remarks</span></span>

<span data-ttu-id="680f7-115">Cette propriété calculée par la banque de messages est utilisée pour les deux, même si associées, à des fins.</span><span class="sxs-lookup"><span data-stu-id="680f7-115">This property computed by the message store is used for two different, though related, purposes.</span></span> <span data-ttu-id="680f7-116">Dans un objet MapiFolder, il contient le nombre de messages dans un dossier.</span><span class="sxs-lookup"><span data-stu-id="680f7-116">On a MapiFolder object, it contains the number of messages in a folder.</span></span> <span data-ttu-id="680f7-117">Dans une ligne d’en-tête dans les tableaux MAPI par catégorie, il contient le nombre de messages non associés dans les catégories correspondant à cette ligne d’en-tête.</span><span class="sxs-lookup"><span data-stu-id="680f7-117">In a heading row in categorized MAPI tables, it contains the number of non-associated messages in the category corresponding to that heading row.</span></span>
  
<span data-ttu-id="680f7-118">Nombre figurant dans cette propriété n’inclut pas les entrées associées dans le dossier.</span><span class="sxs-lookup"><span data-stu-id="680f7-118">The number contained in this property does not include associated entries in the folder.</span></span> <span data-ttu-id="680f7-119">**PR_CONTENT_UNREAD** ([PidTagContentUnreadCount](pidtagcontentunreadcount-canonical-property.md)) contient le nombre de messages non lus du dossier.</span><span class="sxs-lookup"><span data-stu-id="680f7-119">**PR_CONTENT_UNREAD** ([PidTagContentUnreadCount](pidtagcontentunreadcount-canonical-property.md)) contains the count of unread messages for the folder.</span></span> <span data-ttu-id="680f7-120">Une application cliente peut lire mais pas modifier cette propriété et la **PR_CONTENT_UNREAD**.</span><span class="sxs-lookup"><span data-stu-id="680f7-120">A client application can read but not change this property and **PR_CONTENT_UNREAD**.</span></span> 
  
## <a name="related-resources"></a><span data-ttu-id="680f7-121">Ressources connexes</span><span class="sxs-lookup"><span data-stu-id="680f7-121">Related resources</span></span>

### <a name="protocol-specifications"></a><span data-ttu-id="680f7-122">Spécifications du protocole</span><span class="sxs-lookup"><span data-stu-id="680f7-122">Protocol specifications</span></span>

<span data-ttu-id="680f7-123">[[MS-OXPROPS]](http://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="680f7-123">[[MS-OXPROPS]](http://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="680f7-124">Fournit des références aux spécifications du protocole connexes Microsoft Exchange Server.</span><span class="sxs-lookup"><span data-stu-id="680f7-124">Provides references to related Microsoft Exchange Server protocol specifications.</span></span>
    
<span data-ttu-id="680f7-125">[[MS-OXCFOLD]](http://msdn.microsoft.com/library/c0f31b95-c07f-486c-98d9-535ed9705fbf%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="680f7-125">[[MS-OXCFOLD]](http://msdn.microsoft.com/library/c0f31b95-c07f-486c-98d9-535ed9705fbf%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="680f7-126">Gère les opérations de dossier.</span><span class="sxs-lookup"><span data-stu-id="680f7-126">Handles folder operations.</span></span>
    
<span data-ttu-id="680f7-127">[[MS-OXCTABL]](http://msdn.microsoft.com/library/d33612dc-36a8-4623-8a26-c156cf8aae4b%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="680f7-127">[[MS-OXCTABL]](http://msdn.microsoft.com/library/d33612dc-36a8-4623-8a26-c156cf8aae4b%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="680f7-128">Inclut les opérations autorisées pour les objets de la table principale.</span><span class="sxs-lookup"><span data-stu-id="680f7-128">Includes permissible operations for the core table objects.</span></span>
    
### <a name="header-files"></a><span data-ttu-id="680f7-129">Fichiers d’en-tête</span><span class="sxs-lookup"><span data-stu-id="680f7-129">Header files</span></span>

<span data-ttu-id="680f7-130">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="680f7-130">Mapidefs.h</span></span>
  
> <span data-ttu-id="680f7-131">Fournit des définitions de type de données.</span><span class="sxs-lookup"><span data-stu-id="680f7-131">Provides data type definitions.</span></span>
    
<span data-ttu-id="680f7-132">MAPITAGS.h</span><span class="sxs-lookup"><span data-stu-id="680f7-132">Mapitags.h</span></span>
  
> <span data-ttu-id="680f7-133">Contient les définitions des propriétés répertoriées en tant que d’autres noms.</span><span class="sxs-lookup"><span data-stu-id="680f7-133">Contains definitions of properties listed as alternate names.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="680f7-134">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="680f7-134">See also</span></span>



[<span data-ttu-id="680f7-135">Propriétés MAPI</span><span class="sxs-lookup"><span data-stu-id="680f7-135">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="680f7-136">Propriétés canoniques MAPI</span><span class="sxs-lookup"><span data-stu-id="680f7-136">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="680f7-137">Mappage des noms de propriétés canoniques aux noms MAPI</span><span class="sxs-lookup"><span data-stu-id="680f7-137">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="680f7-138">Mappage des noms MAPI aux noms de propriétés canoniques</span><span class="sxs-lookup"><span data-stu-id="680f7-138">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

