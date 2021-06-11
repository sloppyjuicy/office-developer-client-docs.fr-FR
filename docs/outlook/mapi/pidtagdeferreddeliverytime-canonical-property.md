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
description: Dernière modification le 9 mars 2015
ms.openlocfilehash: 7197159fd55016454de3fa806fc30d0700ef5f3d
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32359926"
---
# <a name="pidtagdeferreddeliverytime-canonical-property"></a><span data-ttu-id="a054f-103">Propriété canonique PidTagDeferredDeliveryTime</span><span class="sxs-lookup"><span data-stu-id="a054f-103">PidTagDeferredDeliveryTime Canonical Property</span></span>

  
  
<span data-ttu-id="a054f-104">**S’applique à** : Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="a054f-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="a054f-105">Contient la date et l’heure à laquelle un expéditeur de message souhaite remettre un message.</span><span class="sxs-lookup"><span data-stu-id="a054f-105">Contains the date and time when a message sender wants a message delivered.</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="a054f-106">Propriétés associées :</span><span class="sxs-lookup"><span data-stu-id="a054f-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="a054f-107">PR_DEFERRED_DELIVERY_TIME</span><span class="sxs-lookup"><span data-stu-id="a054f-107">PR_DEFERRED_DELIVERY_TIME</span></span>  <br/> |
|<span data-ttu-id="a054f-108">Identificateur :</span><span class="sxs-lookup"><span data-stu-id="a054f-108">Identifier:</span></span>  <br/> |<span data-ttu-id="a054f-109">0x000F</span><span class="sxs-lookup"><span data-stu-id="a054f-109">0x000F</span></span>  <br/> |
|<span data-ttu-id="a054f-110">Type de données :</span><span class="sxs-lookup"><span data-stu-id="a054f-110">Data type:</span></span>  <br/> |<span data-ttu-id="a054f-111">PT_SYSTIME</span><span class="sxs-lookup"><span data-stu-id="a054f-111">PT_SYSTIME</span></span>  <br/> |
|<span data-ttu-id="a054f-112">Domaine :</span><span class="sxs-lookup"><span data-stu-id="a054f-112">Area:</span></span>  <br/> |<span data-ttu-id="a054f-113">Enveloppe MAPI</span><span class="sxs-lookup"><span data-stu-id="a054f-113">MAPI envelope</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="a054f-114">Remarques</span><span class="sxs-lookup"><span data-stu-id="a054f-114">Remarks</span></span>

<span data-ttu-id="a054f-115">MAPI n’effectue pas la remise différée ; il s’agit d’une option du système de messagerie sous-jacent pour gérer la remise différée.</span><span class="sxs-lookup"><span data-stu-id="a054f-115">MAPI does not perform the deferred delivery; it is an option of the underlying messaging system to handle deferred delivery.</span></span>
  
## <a name="related-resources"></a><span data-ttu-id="a054f-116">Ressources connexes</span><span class="sxs-lookup"><span data-stu-id="a054f-116">Related resources</span></span>

### <a name="protocol-specifications"></a><span data-ttu-id="a054f-117">Spécifications de protocole</span><span class="sxs-lookup"><span data-stu-id="a054f-117">Protocol specifications</span></span>

<span data-ttu-id="a054f-118">[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="a054f-118">[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="a054f-119">Fournit des références aux spécifications Exchange Server protocole.</span><span class="sxs-lookup"><span data-stu-id="a054f-119">Provides references to related Exchange Server protocol specifications.</span></span>
    
<span data-ttu-id="a054f-120">[[MS-OXOMSG]](https://msdn.microsoft.com/library/daa9120f-f325-4afb-a738-28f91049ab3c%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="a054f-120">[[MS-OXOMSG]](https://msdn.microsoft.com/library/daa9120f-f325-4afb-a738-28f91049ab3c%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="a054f-121">Spécifie les propriétés et opérations autorisées sur les messages électroniques.</span><span class="sxs-lookup"><span data-stu-id="a054f-121">Specifies the properties and operations that are permissible on email messages.</span></span>
    
### <a name="header-files"></a><span data-ttu-id="a054f-122">Fichiers d’en-tête</span><span class="sxs-lookup"><span data-stu-id="a054f-122">Header files</span></span>

<span data-ttu-id="a054f-123">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="a054f-123">Mapidefs.h</span></span>
  
> <span data-ttu-id="a054f-124">Fournit des définitions de type de données.</span><span class="sxs-lookup"><span data-stu-id="a054f-124">Provides data type definitions.</span></span>
    
<span data-ttu-id="a054f-125">Mapitags.h</span><span class="sxs-lookup"><span data-stu-id="a054f-125">Mapitags.h</span></span>
  
> <span data-ttu-id="a054f-126">Contient les définitions des propriétés répertoriées en tant que noms de remplacement.</span><span class="sxs-lookup"><span data-stu-id="a054f-126">Contains definitions of properties listed as alternate names.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="a054f-127">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="a054f-127">See also</span></span>



[<span data-ttu-id="a054f-128">Propriétés MAPI</span><span class="sxs-lookup"><span data-stu-id="a054f-128">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="a054f-129">Propriétés canoniques MAPI</span><span class="sxs-lookup"><span data-stu-id="a054f-129">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="a054f-130">Mappage des noms de propriétés canoniques aux noms MAPI</span><span class="sxs-lookup"><span data-stu-id="a054f-130">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="a054f-131">Mappage des noms MAPI aux noms de propriétés canoniques</span><span class="sxs-lookup"><span data-stu-id="a054f-131">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

