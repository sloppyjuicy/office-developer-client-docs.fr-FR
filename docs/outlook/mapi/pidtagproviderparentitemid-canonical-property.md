---
title: Propriété canonique PidTagProviderParentItemId
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- MAPI.PidTagProviderParentItemId
api_type:
- COM
ms.assetid: 6adb8e85-ae56-4542-8b19-ed3cfe7fe522
description: Dernière modification le 09 mars 2015
ms.openlocfilehash: d0ec4e793a5b7940802ee159c2e869695166ce93
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/23/2018
ms.locfileid: "22563281"
---
# <a name="pidtagproviderparentitemid-canonical-property"></a><span data-ttu-id="cf466-103">Propriété canonique PidTagProviderParentItemId</span><span class="sxs-lookup"><span data-stu-id="cf466-103">PidTagProviderParentItemId Canonical Property</span></span>

  
  
<span data-ttu-id="cf466-104">**S’applique à**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="cf466-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="cf466-105">Spécifie un identificateur pour l’objet parent d’un dossier ou un élément dans une banque.</span><span class="sxs-lookup"><span data-stu-id="cf466-105">Specifies an identifier for the parent of a folder or an item in a store.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="cf466-106">Propriétés associées :</span><span class="sxs-lookup"><span data-stu-id="cf466-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="cf466-107">PR_PROVIDER_PARENT_ITEMID</span><span class="sxs-lookup"><span data-stu-id="cf466-107">PR_PROVIDER_PARENT_ITEMID</span></span>  <br/> |
|<span data-ttu-id="cf466-108">Identificateur :</span><span class="sxs-lookup"><span data-stu-id="cf466-108">Identifier:</span></span>  <br/> |<span data-ttu-id="cf466-109">0x0EA4</span><span class="sxs-lookup"><span data-stu-id="cf466-109">0x0EA4</span></span>  <br/> |
|<span data-ttu-id="cf466-110">Type de données :</span><span class="sxs-lookup"><span data-stu-id="cf466-110">Data type:</span></span>  <br/> |<span data-ttu-id="cf466-111">PT_BINARY</span><span class="sxs-lookup"><span data-stu-id="cf466-111">PT_BINARY</span></span>  <br/> |
|<span data-ttu-id="cf466-112">Domaine :</span><span class="sxs-lookup"><span data-stu-id="cf466-112">Area:</span></span>  <br/> |<span data-ttu-id="cf466-113">MAPI non transmissible</span><span class="sxs-lookup"><span data-stu-id="cf466-113">MAPI non-transmittable</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="cf466-114">Remarques</span><span class="sxs-lookup"><span data-stu-id="cf466-114">Remarks</span></span>

<span data-ttu-id="cf466-115">Fournisseurs de magasins peuvent spécifier une valeur pour cette propriété pour un parent d’un dossier ou un élément, mais doivent conserver la valeur de la même session.</span><span class="sxs-lookup"><span data-stu-id="cf466-115">Store providers can specify a value for this property for a parent of a folder or an item, but should keep the value the same between sessions.</span></span> <span data-ttu-id="cf466-116">Fournisseurs de magasins d’utilisent cette propriété pour identifier des résultats de recherche renvoyés à partir d’un moteur de recherche.</span><span class="sxs-lookup"><span data-stu-id="cf466-116">Store providers use this property to identify search results returned from a search engine.</span></span>
  
## <a name="related-resources"></a><span data-ttu-id="cf466-117">Ressources connexes</span><span class="sxs-lookup"><span data-stu-id="cf466-117">Related resources</span></span>

### <a name="header-files"></a><span data-ttu-id="cf466-118">Fichiers d’en-tête</span><span class="sxs-lookup"><span data-stu-id="cf466-118">Header files</span></span>

<span data-ttu-id="cf466-119">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="cf466-119">Mapidefs.h</span></span>
  
> <span data-ttu-id="cf466-120">Fournit des définitions de type de données.</span><span class="sxs-lookup"><span data-stu-id="cf466-120">Provides data type definitions.</span></span>
    
<span data-ttu-id="cf466-121">MAPITAGS.h</span><span class="sxs-lookup"><span data-stu-id="cf466-121">Mapitags.h</span></span>
  
> <span data-ttu-id="cf466-122">Contient les définitions des propriétés répertoriées en tant que d’autres noms.</span><span class="sxs-lookup"><span data-stu-id="cf466-122">Contains definitions of properties listed as alternate names.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="cf466-123">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="cf466-123">See also</span></span>



[<span data-ttu-id="cf466-124">Propriétés MAPI</span><span class="sxs-lookup"><span data-stu-id="cf466-124">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="cf466-125">Propriétés canoniques MAPI</span><span class="sxs-lookup"><span data-stu-id="cf466-125">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="cf466-126">Mappage des noms de propriétés canoniques aux noms MAPI</span><span class="sxs-lookup"><span data-stu-id="cf466-126">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="cf466-127">Mappage des noms MAPI aux noms de propriétés canoniques</span><span class="sxs-lookup"><span data-stu-id="cf466-127">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

