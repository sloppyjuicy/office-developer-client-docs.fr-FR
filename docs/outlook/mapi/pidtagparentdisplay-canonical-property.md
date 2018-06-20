---
title: Propriété canonique PidTagParentDisplay
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- MAPI.PidTagParentDisplay
api_type:
- COM
ms.assetid: 6a36f4fb-17c0-4271-87d4-a92895f35f23
description: 'Derni�re modification�: lundi 9 mars 2015'
ms.openlocfilehash: ce9fea80a2dfed25002e5500dd4defaf5ff04421
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19786407"
---
# <a name="pidtagparentdisplay-canonical-property"></a><span data-ttu-id="fb3c7-103">Propriété canonique PidTagParentDisplay</span><span class="sxs-lookup"><span data-stu-id="fb3c7-103">PidTagParentDisplay Canonical Property</span></span>

  
  
<span data-ttu-id="fb3c7-104">**S’applique à**: Outlook</span><span class="sxs-lookup"><span data-stu-id="fb3c7-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="fb3c7-105">Contient le nom complet du dossier dans lequel un message a été trouvé pendant une recherche.</span><span class="sxs-lookup"><span data-stu-id="fb3c7-105">Contains the display name of the folder where a message was found during a search.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="fb3c7-106">Propriétés associées :</span><span class="sxs-lookup"><span data-stu-id="fb3c7-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="fb3c7-107">PR_PARENT_DISPLAY, PR_PARENT_DISPLAY_A, PR_PARENT_DISPLAY_W</span><span class="sxs-lookup"><span data-stu-id="fb3c7-107">PR_PARENT_DISPLAY, PR_PARENT_DISPLAY_A, PR_PARENT_DISPLAY_W</span></span>  <br/> |
|<span data-ttu-id="fb3c7-108">Identificateur :</span><span class="sxs-lookup"><span data-stu-id="fb3c7-108">Identifier:</span></span>  <br/> |<span data-ttu-id="fb3c7-109">0x0E05</span><span class="sxs-lookup"><span data-stu-id="fb3c7-109">0x0E05</span></span>  <br/> |
|<span data-ttu-id="fb3c7-110">Type de données :</span><span class="sxs-lookup"><span data-stu-id="fb3c7-110">Data type:</span></span>  <br/> |<span data-ttu-id="fb3c7-111">PT_STRING8, PT_UNICODE</span><span class="sxs-lookup"><span data-stu-id="fb3c7-111">PT_STRING8, PT_UNICODE</span></span>  <br/> |
|<span data-ttu-id="fb3c7-112">Zone :</span><span class="sxs-lookup"><span data-stu-id="fb3c7-112">Area:</span></span>  <br/> |<span data-ttu-id="fb3c7-113">MAPI non transmissible</span><span class="sxs-lookup"><span data-stu-id="fb3c7-113">MAPI non-transmittable</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="fb3c7-114">Remarques</span><span class="sxs-lookup"><span data-stu-id="fb3c7-114">Remarks</span></span>

<span data-ttu-id="fb3c7-115">Ces propriétés n’est pas sur tous les objets.</span><span class="sxs-lookup"><span data-stu-id="fb3c7-115">These properties is not on any object.</span></span> <span data-ttu-id="fb3c7-116">Ils peuvent uniquement apparaître dans la table des matières d’un dossier de résultats de recherche.</span><span class="sxs-lookup"><span data-stu-id="fb3c7-116">They can only appear in the contents table of a search-results folder.</span></span>
  
<span data-ttu-id="fb3c7-117">Ces propriétés et les propriétés **PR_PARENT_ENTRYID** ([PidTagParentEntryId](pidtagparententryid-canonical-property.md)) ne sont pas liées à l’autre.</span><span class="sxs-lookup"><span data-stu-id="fb3c7-117">These properties and **PR_PARENT_ENTRYID** ([PidTagParentEntryId](pidtagparententryid-canonical-property.md)) properties are not related to each other.</span></span> <span data-ttu-id="fb3c7-118">Ils appartiennent aux contextes totalement différents.</span><span class="sxs-lookup"><span data-stu-id="fb3c7-118">They belong to entirely different contexts.</span></span>
  
## <a name="related-resources"></a><span data-ttu-id="fb3c7-119">Ressources connexes</span><span class="sxs-lookup"><span data-stu-id="fb3c7-119">Related resources</span></span>

### <a name="header-files"></a><span data-ttu-id="fb3c7-120">Fichiers d’en-tête</span><span class="sxs-lookup"><span data-stu-id="fb3c7-120">Header files</span></span>

<span data-ttu-id="fb3c7-121">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="fb3c7-121">Mapidefs.h</span></span>
  
> <span data-ttu-id="fb3c7-122">Fournit des définitions de type de données.</span><span class="sxs-lookup"><span data-stu-id="fb3c7-122">Provides data type definitions.</span></span>
    
<span data-ttu-id="fb3c7-123">MAPITAGS.h</span><span class="sxs-lookup"><span data-stu-id="fb3c7-123">Mapitags.h</span></span>
  
> <span data-ttu-id="fb3c7-124">Contient les définitions des propriétés répertoriées en tant que d’autres noms.</span><span class="sxs-lookup"><span data-stu-id="fb3c7-124">Contains definitions of properties listed as alternate names.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="fb3c7-125">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="fb3c7-125">See also</span></span>



[<span data-ttu-id="fb3c7-126">Propriétés MAPI</span><span class="sxs-lookup"><span data-stu-id="fb3c7-126">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="fb3c7-127">Propriétés canoniques MAPI</span><span class="sxs-lookup"><span data-stu-id="fb3c7-127">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="fb3c7-128">Mappage de noms de propriété canonique aux noms MAPI</span><span class="sxs-lookup"><span data-stu-id="fb3c7-128">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="fb3c7-129">Mappage de noms MAPI pour les noms de propriété canonique</span><span class="sxs-lookup"><span data-stu-id="fb3c7-129">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

