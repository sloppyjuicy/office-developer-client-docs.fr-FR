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
description: Dernière modification le 9 mars 2015
ms.openlocfilehash: 7aef4c1d83672033662502ad0950b7bac9f58c52
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/28/2019
ms.locfileid: "33429501"
---
# <a name="pidtagparentdisplay-canonical-property"></a><span data-ttu-id="a7ba0-103">Propriété canonique PidTagParentDisplay</span><span class="sxs-lookup"><span data-stu-id="a7ba0-103">PidTagParentDisplay Canonical Property</span></span>

  
  
<span data-ttu-id="a7ba0-104">**S’applique à** : Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="a7ba0-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="a7ba0-105">Contient le nom complet du dossier dans lequel un message a été trouvé au cours d’une recherche.</span><span class="sxs-lookup"><span data-stu-id="a7ba0-105">Contains the display name of the folder where a message was found during a search.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="a7ba0-106">Propriétés associées :</span><span class="sxs-lookup"><span data-stu-id="a7ba0-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="a7ba0-107">PR_PARENT_DISPLAY, PR_PARENT_DISPLAY_A, PR_PARENT_DISPLAY_W</span><span class="sxs-lookup"><span data-stu-id="a7ba0-107">PR_PARENT_DISPLAY, PR_PARENT_DISPLAY_A, PR_PARENT_DISPLAY_W</span></span>  <br/> |
|<span data-ttu-id="a7ba0-108">Identificateur :</span><span class="sxs-lookup"><span data-stu-id="a7ba0-108">Identifier:</span></span>  <br/> |<span data-ttu-id="a7ba0-109">0x0E05</span><span class="sxs-lookup"><span data-stu-id="a7ba0-109">0x0E05</span></span>  <br/> |
|<span data-ttu-id="a7ba0-110">Type de données :</span><span class="sxs-lookup"><span data-stu-id="a7ba0-110">Data type:</span></span>  <br/> |<span data-ttu-id="a7ba0-111">PT_STRING8, PT_UNICODE</span><span class="sxs-lookup"><span data-stu-id="a7ba0-111">PT_STRING8, PT_UNICODE</span></span>  <br/> |
|<span data-ttu-id="a7ba0-112">Domaine :</span><span class="sxs-lookup"><span data-stu-id="a7ba0-112">Area:</span></span>  <br/> |<span data-ttu-id="a7ba0-113">MAPI non transmetteable</span><span class="sxs-lookup"><span data-stu-id="a7ba0-113">MAPI non-transmittable</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="a7ba0-114">Remarques</span><span class="sxs-lookup"><span data-stu-id="a7ba0-114">Remarks</span></span>

<span data-ttu-id="a7ba0-115">Ces propriétés ne se trouve sur aucun objet.</span><span class="sxs-lookup"><span data-stu-id="a7ba0-115">These properties is not on any object.</span></span> <span data-ttu-id="a7ba0-116">Elles peuvent uniquement apparaître dans la table des matières d’un dossier de résultats de recherche.</span><span class="sxs-lookup"><span data-stu-id="a7ba0-116">They can only appear in the contents table of a search-results folder.</span></span>
  
<span data-ttu-id="a7ba0-117">Ces propriétés **et PR_PARENT_ENTRYID** ([PidTagParentEntryId](pidtagparententryid-canonical-property.md)) ne sont pas liées les unes aux autres.</span><span class="sxs-lookup"><span data-stu-id="a7ba0-117">These properties and **PR_PARENT_ENTRYID** ([PidTagParentEntryId](pidtagparententryid-canonical-property.md)) properties are not related to each other.</span></span> <span data-ttu-id="a7ba0-118">Ils appartiennent à des contextes totalement différents.</span><span class="sxs-lookup"><span data-stu-id="a7ba0-118">They belong to entirely different contexts.</span></span>
  
## <a name="related-resources"></a><span data-ttu-id="a7ba0-119">Ressources connexes</span><span class="sxs-lookup"><span data-stu-id="a7ba0-119">Related resources</span></span>

### <a name="header-files"></a><span data-ttu-id="a7ba0-120">Fichiers d’en-tête</span><span class="sxs-lookup"><span data-stu-id="a7ba0-120">Header files</span></span>

<span data-ttu-id="a7ba0-121">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="a7ba0-121">Mapidefs.h</span></span>
  
> <span data-ttu-id="a7ba0-122">Fournit des définitions de type de données.</span><span class="sxs-lookup"><span data-stu-id="a7ba0-122">Provides data type definitions.</span></span>
    
<span data-ttu-id="a7ba0-123">Mapitags.h</span><span class="sxs-lookup"><span data-stu-id="a7ba0-123">Mapitags.h</span></span>
  
> <span data-ttu-id="a7ba0-124">Contient les définitions des propriétés répertoriées en tant que noms de remplacement.</span><span class="sxs-lookup"><span data-stu-id="a7ba0-124">Contains definitions of properties listed as alternate names.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="a7ba0-125">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="a7ba0-125">See also</span></span>



[<span data-ttu-id="a7ba0-126">Propriétés MAPI</span><span class="sxs-lookup"><span data-stu-id="a7ba0-126">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="a7ba0-127">Propriétés canoniques MAPI</span><span class="sxs-lookup"><span data-stu-id="a7ba0-127">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="a7ba0-128">Mappage des noms de propriétés canoniques aux noms MAPI</span><span class="sxs-lookup"><span data-stu-id="a7ba0-128">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="a7ba0-129">Mappage des noms MAPI aux noms de propriétés canoniques</span><span class="sxs-lookup"><span data-stu-id="a7ba0-129">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

