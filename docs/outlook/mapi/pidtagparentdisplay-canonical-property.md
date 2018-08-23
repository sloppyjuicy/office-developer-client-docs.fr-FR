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
description: Dernière modification le 09 mars 2015
ms.openlocfilehash: 910a62a660ea17992aa391d7453919d9fbb53c86
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/23/2018
ms.locfileid: "22580431"
---
# <a name="pidtagparentdisplay-canonical-property"></a><span data-ttu-id="6819e-103">Propriété canonique PidTagParentDisplay</span><span class="sxs-lookup"><span data-stu-id="6819e-103">PidTagParentDisplay Canonical Property</span></span>

  
  
<span data-ttu-id="6819e-104">**S’applique à**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="6819e-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="6819e-105">Contient le nom complet du dossier dans lequel un message a été trouvé pendant une recherche.</span><span class="sxs-lookup"><span data-stu-id="6819e-105">Contains the display name of the folder where a message was found during a search.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="6819e-106">Propriétés associées :</span><span class="sxs-lookup"><span data-stu-id="6819e-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="6819e-107">PR_PARENT_DISPLAY, PR_PARENT_DISPLAY_A, PR_PARENT_DISPLAY_W</span><span class="sxs-lookup"><span data-stu-id="6819e-107">PR_PARENT_DISPLAY, PR_PARENT_DISPLAY_A, PR_PARENT_DISPLAY_W</span></span>  <br/> |
|<span data-ttu-id="6819e-108">Identificateur :</span><span class="sxs-lookup"><span data-stu-id="6819e-108">Identifier:</span></span>  <br/> |<span data-ttu-id="6819e-109">0x0E05</span><span class="sxs-lookup"><span data-stu-id="6819e-109">0x0E05</span></span>  <br/> |
|<span data-ttu-id="6819e-110">Type de données :</span><span class="sxs-lookup"><span data-stu-id="6819e-110">Data type:</span></span>  <br/> |<span data-ttu-id="6819e-111">PT_STRING8, PT_UNICODE</span><span class="sxs-lookup"><span data-stu-id="6819e-111">PT_STRING8, PT_UNICODE</span></span>  <br/> |
|<span data-ttu-id="6819e-112">Domaine :</span><span class="sxs-lookup"><span data-stu-id="6819e-112">Area:</span></span>  <br/> |<span data-ttu-id="6819e-113">MAPI non transmissible</span><span class="sxs-lookup"><span data-stu-id="6819e-113">MAPI non-transmittable</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="6819e-114">Remarques</span><span class="sxs-lookup"><span data-stu-id="6819e-114">Remarks</span></span>

<span data-ttu-id="6819e-115">Ces propriétés n’est pas sur tous les objets.</span><span class="sxs-lookup"><span data-stu-id="6819e-115">These properties is not on any object.</span></span> <span data-ttu-id="6819e-116">Ils peuvent uniquement apparaître dans la table des matières d’un dossier de résultats de recherche.</span><span class="sxs-lookup"><span data-stu-id="6819e-116">They can only appear in the contents table of a search-results folder.</span></span>
  
<span data-ttu-id="6819e-117">Ces propriétés et les propriétés **PR_PARENT_ENTRYID** ([PidTagParentEntryId](pidtagparententryid-canonical-property.md)) ne sont pas liées à l’autre.</span><span class="sxs-lookup"><span data-stu-id="6819e-117">These properties and **PR_PARENT_ENTRYID** ([PidTagParentEntryId](pidtagparententryid-canonical-property.md)) properties are not related to each other.</span></span> <span data-ttu-id="6819e-118">Ils appartiennent aux contextes totalement différents.</span><span class="sxs-lookup"><span data-stu-id="6819e-118">They belong to entirely different contexts.</span></span>
  
## <a name="related-resources"></a><span data-ttu-id="6819e-119">Ressources connexes</span><span class="sxs-lookup"><span data-stu-id="6819e-119">Related resources</span></span>

### <a name="header-files"></a><span data-ttu-id="6819e-120">Fichiers d’en-tête</span><span class="sxs-lookup"><span data-stu-id="6819e-120">Header files</span></span>

<span data-ttu-id="6819e-121">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="6819e-121">Mapidefs.h</span></span>
  
> <span data-ttu-id="6819e-122">Fournit des définitions de type de données.</span><span class="sxs-lookup"><span data-stu-id="6819e-122">Provides data type definitions.</span></span>
    
<span data-ttu-id="6819e-123">MAPITAGS.h</span><span class="sxs-lookup"><span data-stu-id="6819e-123">Mapitags.h</span></span>
  
> <span data-ttu-id="6819e-124">Contient les définitions des propriétés répertoriées en tant que d’autres noms.</span><span class="sxs-lookup"><span data-stu-id="6819e-124">Contains definitions of properties listed as alternate names.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="6819e-125">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="6819e-125">See also</span></span>



[<span data-ttu-id="6819e-126">Propriétés MAPI</span><span class="sxs-lookup"><span data-stu-id="6819e-126">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="6819e-127">Propriétés canoniques MAPI</span><span class="sxs-lookup"><span data-stu-id="6819e-127">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="6819e-128">Mappage des noms de propriétés canoniques aux noms MAPI</span><span class="sxs-lookup"><span data-stu-id="6819e-128">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="6819e-129">Mappage des noms MAPI aux noms de propriétés canoniques</span><span class="sxs-lookup"><span data-stu-id="6819e-129">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

