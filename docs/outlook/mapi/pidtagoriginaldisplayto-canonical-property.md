---
title: Propriété canonique PidTagOriginalDisplayTo
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- MAPI.PidTagOriginalDisplayTo
api_type:
- COM
ms.assetid: 8c1cf14c-0339-4ced-8f68-4bfaa1e4d3e9
description: Dernière modification le 9 mars 2015
ms.openlocfilehash: 5a2f60051e5cb0717926a5c3e2f878a49919b04c
ms.sourcegitcommit: ef717c65d8dd41ababffb01eafc443c79950aed4
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 10/04/2018
ms.locfileid: "25385066"
---
# <a name="pidtagoriginaldisplayto-canonical-property"></a><span data-ttu-id="0afb2-103">Propriété canonique PidTagOriginalDisplayTo</span><span class="sxs-lookup"><span data-stu-id="0afb2-103">PidTagOriginalDisplayTo Canonical Property</span></span>

  
  
<span data-ttu-id="0afb2-104">**S’applique à** : Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="0afb2-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="0afb2-105">Contient les noms complets des (destinataires du message d’origine à) principale.</span><span class="sxs-lookup"><span data-stu-id="0afb2-105">Contains the display names of the primary (To) recipients of the original message.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="0afb2-106">Propriétés associées :</span><span class="sxs-lookup"><span data-stu-id="0afb2-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="0afb2-107">PR_ORIGINAL_DISPLAY_TO, PR_ORIGINAL_DISPLAY_TO_A, PR_ORIGINAL_DISPLAY_TO_W</span><span class="sxs-lookup"><span data-stu-id="0afb2-107">PR_ORIGINAL_DISPLAY_TO, PR_ORIGINAL_DISPLAY_TO_A, PR_ORIGINAL_DISPLAY_TO_W</span></span>  <br/> |
|<span data-ttu-id="0afb2-108">Identificateur :</span><span class="sxs-lookup"><span data-stu-id="0afb2-108">Identifier:</span></span>  <br/> |<span data-ttu-id="0afb2-109">0x0074</span><span class="sxs-lookup"><span data-stu-id="0afb2-109">0x0074</span></span>  <br/> |
|<span data-ttu-id="0afb2-110">Type de données :</span><span class="sxs-lookup"><span data-stu-id="0afb2-110">Data type:</span></span>  <br/> |<span data-ttu-id="0afb2-111">PT_STRING8, PT_UNICODE</span><span class="sxs-lookup"><span data-stu-id="0afb2-111">PT_STRING8, PT_UNICODE</span></span>  <br/> |
|<span data-ttu-id="0afb2-112">Domaine :</span><span class="sxs-lookup"><span data-stu-id="0afb2-112">Area:</span></span>  <br/> |<span data-ttu-id="0afb2-113">Général de messagerie</span><span class="sxs-lookup"><span data-stu-id="0afb2-113">General messaging</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="0afb2-114">Remarques</span><span class="sxs-lookup"><span data-stu-id="0afb2-114">Remarks</span></span>

<span data-ttu-id="0afb2-115">Ces propriétés contiennent une liste ASCII séparée par des points-virgules.</span><span class="sxs-lookup"><span data-stu-id="0afb2-115">These properties contain an ASCII list separated by semicolons.</span></span> <span data-ttu-id="0afb2-116">Il est fourni par MAPI et est copié directement à partir de **PR_DISPLAY_TO** ([PidTagDisplayTo](pidtagdisplayto-canonical-property.md)) lorsqu’une remise ou rapport de non-remise ou en lecture ou nonread rapport est généré.</span><span class="sxs-lookup"><span data-stu-id="0afb2-116">It is furnished by MAPI and is copied directly from **PR_DISPLAY_TO** ([PidTagDisplayTo](pidtagdisplayto-canonical-property.md)) when a delivery or nondelivery report or a read or nonread report is generated.</span></span> <span data-ttu-id="0afb2-117">Cette propriété peut être présente sur les autres messages tel que défini par les classes de message.</span><span class="sxs-lookup"><span data-stu-id="0afb2-117">This property may be present on other messages as defined by their message classes.</span></span>
  
## <a name="related-resources"></a><span data-ttu-id="0afb2-118">Ressources connexes</span><span class="sxs-lookup"><span data-stu-id="0afb2-118">Related resources</span></span>

### <a name="protocol-specifications"></a><span data-ttu-id="0afb2-119">Spécifications du protocole</span><span class="sxs-lookup"><span data-stu-id="0afb2-119">Protocol specifications</span></span>

<span data-ttu-id="0afb2-120">[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="0afb2-120">[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="0afb2-121">Fournit des références aux spécifications du protocole Exchange Server associées.</span><span class="sxs-lookup"><span data-stu-id="0afb2-121">Provides references to related Exchange Server protocol specifications.</span></span>
    
<span data-ttu-id="0afb2-122">[[MS-OXOMSG]](https://msdn.microsoft.com/library/daa9120f-f325-4afb-a738-28f91049ab3c%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="0afb2-122">[[MS-OXOMSG]](https://msdn.microsoft.com/library/daa9120f-f325-4afb-a738-28f91049ab3c%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="0afb2-123">Spécifie les propriétés et les opérations qui sont autorisées sur les objets de message électronique.</span><span class="sxs-lookup"><span data-stu-id="0afb2-123">Specifies the properties and operations that are permissible on email message objects.</span></span>
    
### <a name="header-files"></a><span data-ttu-id="0afb2-124">Fichiers d’en-tête</span><span class="sxs-lookup"><span data-stu-id="0afb2-124">Header files</span></span>

<span data-ttu-id="0afb2-125">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="0afb2-125">Mapidefs.h</span></span>
  
> <span data-ttu-id="0afb2-126">Fournit des définitions de type de données.</span><span class="sxs-lookup"><span data-stu-id="0afb2-126">Provides data type definitions.</span></span>
    
<span data-ttu-id="0afb2-127">MAPITAGS.h</span><span class="sxs-lookup"><span data-stu-id="0afb2-127">Mapitags.h</span></span>
  
> <span data-ttu-id="0afb2-128">Contient les définitions des propriétés répertoriées en tant que d’autres noms.</span><span class="sxs-lookup"><span data-stu-id="0afb2-128">Contains definitions of properties listed as alternate names.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="0afb2-129">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="0afb2-129">See also</span></span>



[<span data-ttu-id="0afb2-130">Propriétés MAPI</span><span class="sxs-lookup"><span data-stu-id="0afb2-130">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="0afb2-131">Propriétés canoniques MAPI</span><span class="sxs-lookup"><span data-stu-id="0afb2-131">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="0afb2-132">Mappage des noms de propriétés canoniques aux noms MAPI</span><span class="sxs-lookup"><span data-stu-id="0afb2-132">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="0afb2-133">Mappage des noms MAPI aux noms de propriétés canoniques</span><span class="sxs-lookup"><span data-stu-id="0afb2-133">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

