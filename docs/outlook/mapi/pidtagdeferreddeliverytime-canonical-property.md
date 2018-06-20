---
title: Propriété canonique PidTagDeferredDeliveryTime
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- PidTagDeferredDeliveryTime
api_type:
- HeaderDef
ms.assetid: 263ac923-692f-40d4-bdd5-116dc5c49766
description: 'Derni�re modification�: lundi 9 mars 2015'
ms.openlocfilehash: b6b5f5aa5c595fb0c19ca9b8a9f8aeb94a2c2725
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19785932"
---
# <a name="pidtagdeferreddeliverytime-canonical-property"></a><span data-ttu-id="58bbe-103">Propriété canonique PidTagDeferredDeliveryTime</span><span class="sxs-lookup"><span data-stu-id="58bbe-103">PidTagDeferredDeliveryTime Canonical Property</span></span>

  
  
<span data-ttu-id="58bbe-104">**S’applique à**: Outlook</span><span class="sxs-lookup"><span data-stu-id="58bbe-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="58bbe-105">Contient la date et l’heure quand un expéditeur du message souhaite un message envoyé.</span><span class="sxs-lookup"><span data-stu-id="58bbe-105">Contains the date and time when a message sender wants a message delivered.</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="58bbe-106">Propriétés associées :</span><span class="sxs-lookup"><span data-stu-id="58bbe-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="58bbe-107">PR_DEFERRED_DELIVERY_TIME</span><span class="sxs-lookup"><span data-stu-id="58bbe-107">PR_DEFERRED_DELIVERY_TIME</span></span>  <br/> |
|<span data-ttu-id="58bbe-108">Identificateur :</span><span class="sxs-lookup"><span data-stu-id="58bbe-108">Identifier:</span></span>  <br/> |<span data-ttu-id="58bbe-109">0x000F</span><span class="sxs-lookup"><span data-stu-id="58bbe-109">0x000F</span></span>  <br/> |
|<span data-ttu-id="58bbe-110">Type de données :</span><span class="sxs-lookup"><span data-stu-id="58bbe-110">Data type:</span></span>  <br/> |<span data-ttu-id="58bbe-111">PT_SYSTIME</span><span class="sxs-lookup"><span data-stu-id="58bbe-111">PT_SYSTIME</span></span>  <br/> |
|<span data-ttu-id="58bbe-112">Zone :</span><span class="sxs-lookup"><span data-stu-id="58bbe-112">Area:</span></span>  <br/> |<span data-ttu-id="58bbe-113">Enveloppe MAPI</span><span class="sxs-lookup"><span data-stu-id="58bbe-113">MAPI envelope</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="58bbe-114">Remarques</span><span class="sxs-lookup"><span data-stu-id="58bbe-114">Remarks</span></span>

<span data-ttu-id="58bbe-115">MAPI n’effectue pas la remise différée ; Il est une option du système de messagerie sous-jacent pour gérer la remise différée.</span><span class="sxs-lookup"><span data-stu-id="58bbe-115">MAPI does not perform the deferred delivery; it is an option of the underlying messaging system to handle deferred delivery.</span></span>
  
## <a name="related-resources"></a><span data-ttu-id="58bbe-116">Ressources connexes</span><span class="sxs-lookup"><span data-stu-id="58bbe-116">Related resources</span></span>

### <a name="protocol-specifications"></a><span data-ttu-id="58bbe-117">Spécifications du protocole</span><span class="sxs-lookup"><span data-stu-id="58bbe-117">Protocol specifications</span></span>

<span data-ttu-id="58bbe-118">[[MS-OXPROPS]](http://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="58bbe-118">[[MS-OXPROPS]](http://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="58bbe-119">Fournit des références aux spécifications du protocole Exchange Server associées.</span><span class="sxs-lookup"><span data-stu-id="58bbe-119">Provides references to related Exchange Server protocol specifications.</span></span>
    
<span data-ttu-id="58bbe-120">[[MS-OXOMSG]](http://msdn.microsoft.com/library/daa9120f-f325-4afb-a738-28f91049ab3c%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="58bbe-120">[[MS-OXOMSG]](http://msdn.microsoft.com/library/daa9120f-f325-4afb-a738-28f91049ab3c%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="58bbe-121">Spécifie les propriétés et les opérations qui sont autorisées sur les messages électroniques.</span><span class="sxs-lookup"><span data-stu-id="58bbe-121">Specifies the properties and operations that are permissible on email messages.</span></span>
    
### <a name="header-files"></a><span data-ttu-id="58bbe-122">Fichiers d’en-tête</span><span class="sxs-lookup"><span data-stu-id="58bbe-122">Header files</span></span>

<span data-ttu-id="58bbe-123">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="58bbe-123">Mapidefs.h</span></span>
  
> <span data-ttu-id="58bbe-124">Fournit des définitions de type de données.</span><span class="sxs-lookup"><span data-stu-id="58bbe-124">Provides data type definitions.</span></span>
    
<span data-ttu-id="58bbe-125">MAPITAGS.h</span><span class="sxs-lookup"><span data-stu-id="58bbe-125">Mapitags.h</span></span>
  
> <span data-ttu-id="58bbe-126">Contient les définitions des propriétés répertoriées en tant que d’autres noms.</span><span class="sxs-lookup"><span data-stu-id="58bbe-126">Contains definitions of properties listed as alternate names.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="58bbe-127">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="58bbe-127">See also</span></span>



[<span data-ttu-id="58bbe-128">Propriétés MAPI</span><span class="sxs-lookup"><span data-stu-id="58bbe-128">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="58bbe-129">Propriétés canoniques MAPI</span><span class="sxs-lookup"><span data-stu-id="58bbe-129">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="58bbe-130">Mappage de noms de propriété canonique aux noms MAPI</span><span class="sxs-lookup"><span data-stu-id="58bbe-130">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="58bbe-131">Mappage de noms MAPI pour les noms de propriété canonique</span><span class="sxs-lookup"><span data-stu-id="58bbe-131">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

