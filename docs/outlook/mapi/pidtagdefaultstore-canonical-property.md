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
description: Dernière modification le 09 mars 2015
ms.openlocfilehash: d544c741685d401aaf36fe19be50ab402c9e5604
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/23/2018
ms.locfileid: "22592681"
---
# <a name="pidtagdefaultstore-canonical-property"></a><span data-ttu-id="97166-103">Propriété canonique PidTagDefaultStore</span><span class="sxs-lookup"><span data-stu-id="97166-103">PidTagDefaultStore Canonical Property</span></span>

  
  
<span data-ttu-id="97166-104">**S’applique à**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="97166-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="97166-105">Contient la valeur TRUE si une banque de messages est la banque de messages par défaut dans la table.</span><span class="sxs-lookup"><span data-stu-id="97166-105">Contains TRUE if a message store is the default message store in the message store table.</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="97166-106">Propriétés associées :</span><span class="sxs-lookup"><span data-stu-id="97166-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="97166-107">PR_DEFAULT_STORE</span><span class="sxs-lookup"><span data-stu-id="97166-107">PR_DEFAULT_STORE</span></span>  <br/> |
|<span data-ttu-id="97166-108">Identificateur :</span><span class="sxs-lookup"><span data-stu-id="97166-108">Identifier:</span></span>  <br/> |<span data-ttu-id="97166-109">0x3400</span><span class="sxs-lookup"><span data-stu-id="97166-109">0x3400</span></span>  <br/> |
|<span data-ttu-id="97166-110">Type de données :</span><span class="sxs-lookup"><span data-stu-id="97166-110">Data type:</span></span>  <br/> |<span data-ttu-id="97166-111">PT_BOOLEAN</span><span class="sxs-lookup"><span data-stu-id="97166-111">PT_BOOLEAN</span></span>  <br/> |
|<span data-ttu-id="97166-112">Domaine :</span><span class="sxs-lookup"><span data-stu-id="97166-112">Area:</span></span>  <br/> |<span data-ttu-id="97166-113">Banque de messages MAPI</span><span class="sxs-lookup"><span data-stu-id="97166-113">MAPI message store</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="97166-114">Remarques</span><span class="sxs-lookup"><span data-stu-id="97166-114">Remarks</span></span>

<span data-ttu-id="97166-115">Cette propriété s’affiche en tant que colonne dans la table.</span><span class="sxs-lookup"><span data-stu-id="97166-115">This property appears as a column in the message store table.</span></span> <span data-ttu-id="97166-116">La valeur est basée sur **PR_RESOURCE_FLAGS** ([PidTagResourceFlags](pidtagresourceflags-canonical-property.md)).</span><span class="sxs-lookup"><span data-stu-id="97166-116">The value is based on **PR_RESOURCE_FLAGS** ([PidTagResourceFlags](pidtagresourceflags-canonical-property.md)).</span></span> 
  
## <a name="related-resources"></a><span data-ttu-id="97166-117">Ressources connexes</span><span class="sxs-lookup"><span data-stu-id="97166-117">Related resources</span></span>

### <a name="protocol-specifications"></a><span data-ttu-id="97166-118">Spécifications du protocole</span><span class="sxs-lookup"><span data-stu-id="97166-118">Protocol specifications</span></span>

<span data-ttu-id="97166-119">[[MS-OXPROPS]](http://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="97166-119">[[MS-OXPROPS]](http://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="97166-120">Fournit des références aux spécifications du protocole Exchange Server associées.</span><span class="sxs-lookup"><span data-stu-id="97166-120">Provides references to related Exchange Server protocol specifications.</span></span>
    
### <a name="header-files"></a><span data-ttu-id="97166-121">Fichiers d’en-tête</span><span class="sxs-lookup"><span data-stu-id="97166-121">Header files</span></span>

<span data-ttu-id="97166-122">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="97166-122">Mapidefs.h</span></span>
  
> <span data-ttu-id="97166-123">Fournit des définitions de type de données.</span><span class="sxs-lookup"><span data-stu-id="97166-123">Provides data type definitions.</span></span>
    
<span data-ttu-id="97166-124">MAPITAGS.h</span><span class="sxs-lookup"><span data-stu-id="97166-124">Mapitags.h</span></span>
  
> <span data-ttu-id="97166-125">Contient les définitions des propriétés répertoriées en tant que d’autres noms.</span><span class="sxs-lookup"><span data-stu-id="97166-125">Contains definitions of properties listed as alternate names.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="97166-126">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="97166-126">See also</span></span>



[<span data-ttu-id="97166-127">Propriétés MAPI</span><span class="sxs-lookup"><span data-stu-id="97166-127">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="97166-128">Propriétés canoniques MAPI</span><span class="sxs-lookup"><span data-stu-id="97166-128">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="97166-129">Mappage des noms de propriétés canoniques aux noms MAPI</span><span class="sxs-lookup"><span data-stu-id="97166-129">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="97166-130">Mappage des noms MAPI aux noms de propriétés canoniques</span><span class="sxs-lookup"><span data-stu-id="97166-130">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

