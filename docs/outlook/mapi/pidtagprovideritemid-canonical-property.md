---
title: Propriété canonique PidTagProviderItemId
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- MAPI.PidTagProviderItemId
api_type:
- COM
ms.assetid: fadbf1af-32c2-43ea-8475-15b31b2a9e68
description: Dernière modification le 09 mars 2015
ms.openlocfilehash: e0f13b0b8d2f7eb6fd7ba60e9e351b62251aa13d
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/23/2018
ms.locfileid: "22572836"
---
# <a name="pidtagprovideritemid-canonical-property"></a><span data-ttu-id="6f2b7-103">Propriété canonique PidTagProviderItemId</span><span class="sxs-lookup"><span data-stu-id="6f2b7-103">PidTagProviderItemId Canonical Property</span></span>

  
  
<span data-ttu-id="6f2b7-104">**S’applique à**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="6f2b7-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="6f2b7-105">Spécifie un identificateur pour un dossier ou un élément dans une banque.</span><span class="sxs-lookup"><span data-stu-id="6f2b7-105">Specifies an identifier for a folder or an item in a store.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="6f2b7-106">Propriétés associées :</span><span class="sxs-lookup"><span data-stu-id="6f2b7-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="6f2b7-107">PR_PROVIDER_ITEMID</span><span class="sxs-lookup"><span data-stu-id="6f2b7-107">PR_PROVIDER_ITEMID</span></span>  <br/> |
|<span data-ttu-id="6f2b7-108">Identificateur :</span><span class="sxs-lookup"><span data-stu-id="6f2b7-108">Identifier:</span></span>  <br/> |<span data-ttu-id="6f2b7-109">0x0EA3</span><span class="sxs-lookup"><span data-stu-id="6f2b7-109">0x0EA3</span></span>  <br/> |
|<span data-ttu-id="6f2b7-110">Type de données :</span><span class="sxs-lookup"><span data-stu-id="6f2b7-110">Data type:</span></span>  <br/> |<span data-ttu-id="6f2b7-111">PT_BINARY</span><span class="sxs-lookup"><span data-stu-id="6f2b7-111">PT_BINARY</span></span>  <br/> |
|<span data-ttu-id="6f2b7-112">Domaine :</span><span class="sxs-lookup"><span data-stu-id="6f2b7-112">Area:</span></span>  <br/> |<span data-ttu-id="6f2b7-113">MapiNonTransmittable</span><span class="sxs-lookup"><span data-stu-id="6f2b7-113">MapiNonTransmittable</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="6f2b7-114">Remarques</span><span class="sxs-lookup"><span data-stu-id="6f2b7-114">Remarks</span></span>

<span data-ttu-id="6f2b7-115">Fournisseurs de magasins peuvent spécifier une valeur pour cette propriété pour un dossier ou un élément, mais doivent conserver la valeur de la même session.</span><span class="sxs-lookup"><span data-stu-id="6f2b7-115">Store providers can specify a value for this property for a folder or an item, but should keep the value the same between sessions.</span></span> <span data-ttu-id="6f2b7-116">Fournisseurs de magasins d’utilisent cette propriété pour identifier des résultats de recherche renvoyés à partir d’un moteur de recherche.</span><span class="sxs-lookup"><span data-stu-id="6f2b7-116">Store providers use this property to identify search results returned from a search engine.</span></span>
  
## <a name="related-resources"></a><span data-ttu-id="6f2b7-117">Ressources connexes</span><span class="sxs-lookup"><span data-stu-id="6f2b7-117">Related resources</span></span>

### <a name="header-files"></a><span data-ttu-id="6f2b7-118">Fichiers d’en-tête</span><span class="sxs-lookup"><span data-stu-id="6f2b7-118">Header files</span></span>

<span data-ttu-id="6f2b7-119">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="6f2b7-119">Mapidefs.h</span></span>
  
> <span data-ttu-id="6f2b7-120">Fournit des définitions de type de données.</span><span class="sxs-lookup"><span data-stu-id="6f2b7-120">Provides data type definitions.</span></span>
    
<span data-ttu-id="6f2b7-121">MAPITAGS.h</span><span class="sxs-lookup"><span data-stu-id="6f2b7-121">Mapitags.h</span></span>
  
> <span data-ttu-id="6f2b7-122">Contient les définitions des propriétés répertoriées en tant que d’autres noms.</span><span class="sxs-lookup"><span data-stu-id="6f2b7-122">Contains definitions of properties listed as alternate names.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="6f2b7-123">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="6f2b7-123">See also</span></span>



[<span data-ttu-id="6f2b7-124">Propriétés MAPI</span><span class="sxs-lookup"><span data-stu-id="6f2b7-124">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="6f2b7-125">Propriétés canoniques MAPI</span><span class="sxs-lookup"><span data-stu-id="6f2b7-125">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="6f2b7-126">Mappage des noms de propriétés canoniques aux noms MAPI</span><span class="sxs-lookup"><span data-stu-id="6f2b7-126">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="6f2b7-127">Mappage des noms MAPI aux noms de propriétés canoniques</span><span class="sxs-lookup"><span data-stu-id="6f2b7-127">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

