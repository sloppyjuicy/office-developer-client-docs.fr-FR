---
title: Propriété canonique PidTagOriginalDisplayCc
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- MAPI.PidTagOriginalDisplayCc
api_type:
- COM
ms.assetid: f48d723c-3ad8-4617-952a-ba5216b2129c
description: 'Derni�re modification�: lundi 9 mars 2015'
ms.openlocfilehash: c4fc8ef6dd67eb5187bbc0bac8c4f4f9bee13826
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19786313"
---
# <a name="pidtagoriginaldisplaycc-canonical-property"></a><span data-ttu-id="f7e2c-103">Propriété canonique PidTagOriginalDisplayCc</span><span class="sxs-lookup"><span data-stu-id="f7e2c-103">PidTagOriginalDisplayCc Canonical Property</span></span>

  
  
<span data-ttu-id="f7e2c-104">**S’applique à**: Outlook</span><span class="sxs-lookup"><span data-stu-id="f7e2c-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="f7e2c-105">Contient les noms complets des destinataires en copie carbone (CC) du message d’origine.</span><span class="sxs-lookup"><span data-stu-id="f7e2c-105">Contains the display names of any carbon copy (CC) recipients of the original message.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="f7e2c-106">Propriétés associées :</span><span class="sxs-lookup"><span data-stu-id="f7e2c-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="f7e2c-107">PR_ORIGINAL_DISPLAY_CC, PR_ORIGINAL_DISPLAY_CC_A, PR_ORIGINAL_DISPLAY_CC_W</span><span class="sxs-lookup"><span data-stu-id="f7e2c-107">PR_ORIGINAL_DISPLAY_CC, PR_ORIGINAL_DISPLAY_CC_A, PR_ORIGINAL_DISPLAY_CC_W</span></span>  <br/> |
|<span data-ttu-id="f7e2c-108">Identificateur :</span><span class="sxs-lookup"><span data-stu-id="f7e2c-108">Identifier:</span></span>  <br/> |<span data-ttu-id="f7e2c-109">0x0073</span><span class="sxs-lookup"><span data-stu-id="f7e2c-109">0x0073</span></span>  <br/> |
|<span data-ttu-id="f7e2c-110">Type de données :</span><span class="sxs-lookup"><span data-stu-id="f7e2c-110">Data type:</span></span>  <br/> |<span data-ttu-id="f7e2c-111">PT_STRING8, PT_UNICODE</span><span class="sxs-lookup"><span data-stu-id="f7e2c-111">PT_STRING8, PT_UNICODE</span></span>  <br/> |
|<span data-ttu-id="f7e2c-112">Zone :</span><span class="sxs-lookup"><span data-stu-id="f7e2c-112">Area:</span></span>  <br/> |<span data-ttu-id="f7e2c-113">Général de messagerie</span><span class="sxs-lookup"><span data-stu-id="f7e2c-113">General messaging</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="f7e2c-114">Remarques</span><span class="sxs-lookup"><span data-stu-id="f7e2c-114">Remarks</span></span>

<span data-ttu-id="f7e2c-115">Ces propriétés contiennent une liste séparée par des points-virgules.</span><span class="sxs-lookup"><span data-stu-id="f7e2c-115">These properties contain a list separated by semicolons.</span></span> <span data-ttu-id="f7e2c-116">Il est fourni par MAPI et est copié directement à partir de **PR_DISPLAY_CC** ([PidTagDisplayCc](pidtagdisplaycc-canonical-property.md)) lorsqu’une remise ou rapport de non-remise ou en lecture ou nonread rapport est généré.</span><span class="sxs-lookup"><span data-stu-id="f7e2c-116">It is furnished by MAPI and is copied directly from **PR_DISPLAY_CC** ([PidTagDisplayCc](pidtagdisplaycc-canonical-property.md)) when a delivery or nondelivery report or a read or nonread report is generated.</span></span> <span data-ttu-id="f7e2c-117">Cette propriété peut être présente sur les autres messages tel que défini par les classes de message.</span><span class="sxs-lookup"><span data-stu-id="f7e2c-117">This property may be present on other messages as defined by their message classes.</span></span>
  
## <a name="related-resources"></a><span data-ttu-id="f7e2c-118">Ressources connexes</span><span class="sxs-lookup"><span data-stu-id="f7e2c-118">Related resources</span></span>

### <a name="protocol-specifications"></a><span data-ttu-id="f7e2c-119">Spécifications du protocole</span><span class="sxs-lookup"><span data-stu-id="f7e2c-119">Protocol specifications</span></span>

<span data-ttu-id="f7e2c-120">[[MS-OXPROPS]](http://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="f7e2c-120">[[MS-OXPROPS]](http://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="f7e2c-121">Fournit des références aux spécifications du protocole Exchange Server associées.</span><span class="sxs-lookup"><span data-stu-id="f7e2c-121">Provides references to related Exchange Server protocol specifications.</span></span>
    
<span data-ttu-id="f7e2c-122">[[MS-OXOMSG]](http://msdn.microsoft.com/library/daa9120f-f325-4afb-a738-28f91049ab3c%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="f7e2c-122">[[MS-OXOMSG]](http://msdn.microsoft.com/library/daa9120f-f325-4afb-a738-28f91049ab3c%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="f7e2c-123">Spécifie les propriétés et les opérations qui sont autorisées sur les objets de message électronique.</span><span class="sxs-lookup"><span data-stu-id="f7e2c-123">Specifies the properties and operations that are permissible on email message objects.</span></span>
    
### <a name="header-files"></a><span data-ttu-id="f7e2c-124">Fichiers d’en-tête</span><span class="sxs-lookup"><span data-stu-id="f7e2c-124">Header files</span></span>

<span data-ttu-id="f7e2c-125">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="f7e2c-125">Mapidefs.h</span></span>
  
> <span data-ttu-id="f7e2c-126">Fournit des définitions de type de données.</span><span class="sxs-lookup"><span data-stu-id="f7e2c-126">Provides data type definitions.</span></span>
    
<span data-ttu-id="f7e2c-127">MAPITAGS.h</span><span class="sxs-lookup"><span data-stu-id="f7e2c-127">Mapitags.h</span></span>
  
> <span data-ttu-id="f7e2c-128">Contient les définitions des propriétés répertoriées en tant que d’autres noms.</span><span class="sxs-lookup"><span data-stu-id="f7e2c-128">Contains definitions of properties listed as alternate names.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="f7e2c-129">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="f7e2c-129">See also</span></span>



[<span data-ttu-id="f7e2c-130">Propriétés MAPI</span><span class="sxs-lookup"><span data-stu-id="f7e2c-130">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="f7e2c-131">Propriétés canoniques MAPI</span><span class="sxs-lookup"><span data-stu-id="f7e2c-131">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="f7e2c-132">Mappage de noms de propriété canonique aux noms MAPI</span><span class="sxs-lookup"><span data-stu-id="f7e2c-132">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="f7e2c-133">Mappage de noms MAPI pour les noms de propriété canonique</span><span class="sxs-lookup"><span data-stu-id="f7e2c-133">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

