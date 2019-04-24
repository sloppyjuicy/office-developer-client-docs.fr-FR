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
description: 'Derni�re modification�: lundi 9 mars 2015'
ms.openlocfilehash: 0f99cf38e65c75ce1ba74bf72d88e19f4fbfa03a
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32286445"
---
# <a name="pidtagproviderparentitemid-canonical-property"></a><span data-ttu-id="ac095-103">Propriété canonique PidTagProviderParentItemId</span><span class="sxs-lookup"><span data-stu-id="ac095-103">PidTagProviderParentItemId Canonical Property</span></span>

  
  
<span data-ttu-id="ac095-104">**S’applique à** : Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="ac095-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="ac095-105">Spécifie un identificateur pour le parent d'un dossier ou d'un élément dans un magasin.</span><span class="sxs-lookup"><span data-stu-id="ac095-105">Specifies an identifier for the parent of a folder or an item in a store.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="ac095-106">Propriétés associées :</span><span class="sxs-lookup"><span data-stu-id="ac095-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="ac095-107">PR_PROVIDER_PARENT_ITEMID</span><span class="sxs-lookup"><span data-stu-id="ac095-107">PR_PROVIDER_PARENT_ITEMID</span></span>  <br/> |
|<span data-ttu-id="ac095-108">Identificateur :</span><span class="sxs-lookup"><span data-stu-id="ac095-108">Identifier:</span></span>  <br/> |<span data-ttu-id="ac095-109">0x0EA4</span><span class="sxs-lookup"><span data-stu-id="ac095-109">0x0EA4</span></span>  <br/> |
|<span data-ttu-id="ac095-110">Type de données :</span><span class="sxs-lookup"><span data-stu-id="ac095-110">Data type:</span></span>  <br/> |<span data-ttu-id="ac095-111">PT_BINARY</span><span class="sxs-lookup"><span data-stu-id="ac095-111">PT_BINARY</span></span>  <br/> |
|<span data-ttu-id="ac095-112">Domaine :</span><span class="sxs-lookup"><span data-stu-id="ac095-112">Area:</span></span>  <br/> |<span data-ttu-id="ac095-113">MAPI non transmissible</span><span class="sxs-lookup"><span data-stu-id="ac095-113">MAPI non-transmittable</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="ac095-114">Remarques</span><span class="sxs-lookup"><span data-stu-id="ac095-114">Remarks</span></span>

<span data-ttu-id="ac095-115">Les fournisseurs de magasins peuvent spécifier une valeur pour cette propriété pour un parent d'un dossier ou d'un élément, tout en conservant la même valeur entre les sessions.</span><span class="sxs-lookup"><span data-stu-id="ac095-115">Store providers can specify a value for this property for a parent of a folder or an item, but should keep the value the same between sessions.</span></span> <span data-ttu-id="ac095-116">Les fournisseurs de magasin utilisent cette propriété pour identifier les résultats de recherche renvoyés par un moteur de recherche.</span><span class="sxs-lookup"><span data-stu-id="ac095-116">Store providers use this property to identify search results returned from a search engine.</span></span>
  
## <a name="related-resources"></a><span data-ttu-id="ac095-117">Ressources associées</span><span class="sxs-lookup"><span data-stu-id="ac095-117">Related resources</span></span>

### <a name="header-files"></a><span data-ttu-id="ac095-118">Fichiers d'en-tête</span><span class="sxs-lookup"><span data-stu-id="ac095-118">Header files</span></span>

<span data-ttu-id="ac095-119">Mapidefs. h</span><span class="sxs-lookup"><span data-stu-id="ac095-119">Mapidefs.h</span></span>
  
> <span data-ttu-id="ac095-120">Fournit des définitions de type de données.</span><span class="sxs-lookup"><span data-stu-id="ac095-120">Provides data type definitions.</span></span>
    
<span data-ttu-id="ac095-121">Mapitags. h</span><span class="sxs-lookup"><span data-stu-id="ac095-121">Mapitags.h</span></span>
  
> <span data-ttu-id="ac095-122">Contient les définitions des propriétés figurant en tant que noms de substitution.</span><span class="sxs-lookup"><span data-stu-id="ac095-122">Contains definitions of properties listed as alternate names.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="ac095-123">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="ac095-123">See also</span></span>



[<span data-ttu-id="ac095-124">Propriétés MAPI</span><span class="sxs-lookup"><span data-stu-id="ac095-124">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="ac095-125">Propriétés canoniques MAPI</span><span class="sxs-lookup"><span data-stu-id="ac095-125">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="ac095-126">Mappage des noms de propriétés canoniques aux noms MAPI</span><span class="sxs-lookup"><span data-stu-id="ac095-126">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="ac095-127">Mappage des noms MAPI aux noms de propriétés canoniques</span><span class="sxs-lookup"><span data-stu-id="ac095-127">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

