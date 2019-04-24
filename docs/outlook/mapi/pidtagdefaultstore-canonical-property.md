---
title: Propriété canonique PidTagDefaultStore
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- PidTagDefaultStore
api_type:
- HeaderDef
ms.assetid: 6314d91c-4948-4fd1-bacc-932d4bb2c22f
description: 'Derni�re modification�: lundi 9 mars 2015'
ms.openlocfilehash: 0cbcc8185f6f46a1bfceb2dd6d0aaf9c5d7cab2e
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32270104"
---
# <a name="pidtagdefaultstore-canonical-property"></a><span data-ttu-id="bf981-103">Propriété canonique PidTagDefaultStore</span><span class="sxs-lookup"><span data-stu-id="bf981-103">PidTagDefaultStore Canonical Property</span></span>

  
  
<span data-ttu-id="bf981-104">**S’applique à** : Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="bf981-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="bf981-105">Contient la valeur TRUE si une banque de messages est la Banque de messages par défaut dans la table de banque de messages.</span><span class="sxs-lookup"><span data-stu-id="bf981-105">Contains TRUE if a message store is the default message store in the message store table.</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="bf981-106">Propriétés associées :</span><span class="sxs-lookup"><span data-stu-id="bf981-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="bf981-107">PR_DEFAULT_STORE</span><span class="sxs-lookup"><span data-stu-id="bf981-107">PR_DEFAULT_STORE</span></span>  <br/> |
|<span data-ttu-id="bf981-108">Identificateur :</span><span class="sxs-lookup"><span data-stu-id="bf981-108">Identifier:</span></span>  <br/> |<span data-ttu-id="bf981-109">0x3400</span><span class="sxs-lookup"><span data-stu-id="bf981-109">0x3400</span></span>  <br/> |
|<span data-ttu-id="bf981-110">Type de données :</span><span class="sxs-lookup"><span data-stu-id="bf981-110">Data type:</span></span>  <br/> |<span data-ttu-id="bf981-111">PT_BOOLEAN</span><span class="sxs-lookup"><span data-stu-id="bf981-111">PT_BOOLEAN</span></span>  <br/> |
|<span data-ttu-id="bf981-112">Domaine :</span><span class="sxs-lookup"><span data-stu-id="bf981-112">Area:</span></span>  <br/> |<span data-ttu-id="bf981-113">Banque de messages MAPI</span><span class="sxs-lookup"><span data-stu-id="bf981-113">MAPI message store</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="bf981-114">Remarques</span><span class="sxs-lookup"><span data-stu-id="bf981-114">Remarks</span></span>

<span data-ttu-id="bf981-115">Cette propriété apparaît sous la forme d'une colonne dans la table de banque de messages.</span><span class="sxs-lookup"><span data-stu-id="bf981-115">This property appears as a column in the message store table.</span></span> <span data-ttu-id="bf981-116">La valeur est basée sur **PR_RESOURCE_FLAGS** ([PidTagResourceFlags](pidtagresourceflags-canonical-property.md)).</span><span class="sxs-lookup"><span data-stu-id="bf981-116">The value is based on **PR_RESOURCE_FLAGS** ([PidTagResourceFlags](pidtagresourceflags-canonical-property.md)).</span></span> 
  
## <a name="related-resources"></a><span data-ttu-id="bf981-117">Ressources associées</span><span class="sxs-lookup"><span data-stu-id="bf981-117">Related resources</span></span>

### <a name="protocol-specifications"></a><span data-ttu-id="bf981-118">Spécifications de protocole</span><span class="sxs-lookup"><span data-stu-id="bf981-118">Protocol specifications</span></span>

<span data-ttu-id="bf981-119">[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="bf981-119">[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="bf981-120">Fournit des références à des spécifications de protocole Exchange Server connexes.</span><span class="sxs-lookup"><span data-stu-id="bf981-120">Provides references to related Exchange Server protocol specifications.</span></span>
    
### <a name="header-files"></a><span data-ttu-id="bf981-121">Fichiers d'en-tête</span><span class="sxs-lookup"><span data-stu-id="bf981-121">Header files</span></span>

<span data-ttu-id="bf981-122">Mapidefs. h</span><span class="sxs-lookup"><span data-stu-id="bf981-122">Mapidefs.h</span></span>
  
> <span data-ttu-id="bf981-123">Fournit des définitions de type de données.</span><span class="sxs-lookup"><span data-stu-id="bf981-123">Provides data type definitions.</span></span>
    
<span data-ttu-id="bf981-124">Mapitags. h</span><span class="sxs-lookup"><span data-stu-id="bf981-124">Mapitags.h</span></span>
  
> <span data-ttu-id="bf981-125">Contient les définitions des propriétés figurant en tant que noms de substitution.</span><span class="sxs-lookup"><span data-stu-id="bf981-125">Contains definitions of properties listed as alternate names.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="bf981-126">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="bf981-126">See also</span></span>



[<span data-ttu-id="bf981-127">Propriétés MAPI</span><span class="sxs-lookup"><span data-stu-id="bf981-127">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="bf981-128">Propriétés canoniques MAPI</span><span class="sxs-lookup"><span data-stu-id="bf981-128">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="bf981-129">Mappage des noms de propriétés canoniques aux noms MAPI</span><span class="sxs-lookup"><span data-stu-id="bf981-129">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="bf981-130">Mappage des noms MAPI aux noms de propriétés canoniques</span><span class="sxs-lookup"><span data-stu-id="bf981-130">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

