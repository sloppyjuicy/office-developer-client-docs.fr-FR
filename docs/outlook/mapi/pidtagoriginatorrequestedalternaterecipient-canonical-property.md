---
title: Propriété canonique PidTagOriginatorRequestedAlternateRecipient
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- MAPI.PidTagOriginatorRequestedAlternateRecipient
api_type:
- COM
ms.assetid: c85b7862-18bc-4e17-94db-9097e0ac4a02
description: 'Derni�re modification�: lundi 9 mars 2015'
ms.openlocfilehash: c7abd0ae93c5b38c756ec0915dda6a4cdfcebaa5
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19786370"
---
# <a name="pidtagoriginatorrequestedalternaterecipient-canonical-property"></a><span data-ttu-id="ba290-103">Propriété canonique PidTagOriginatorRequestedAlternateRecipient</span><span class="sxs-lookup"><span data-stu-id="ba290-103">PidTagOriginatorRequestedAlternateRecipient Canonical Property</span></span>

  
  
<span data-ttu-id="ba290-104">**S’applique à**: Outlook</span><span class="sxs-lookup"><span data-stu-id="ba290-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="ba290-105">Contient un identificateur d’entrée pour un autre destinataire désigné par l’expéditeur.</span><span class="sxs-lookup"><span data-stu-id="ba290-105">Contains an entry identifier for an alternate recipient designated by the sender.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="ba290-106">Propriétés associées :</span><span class="sxs-lookup"><span data-stu-id="ba290-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="ba290-107">PR_ORIGINATOR_REQUESTED_ALTERNATE_RECIPIENT</span><span class="sxs-lookup"><span data-stu-id="ba290-107">PR_ORIGINATOR_REQUESTED_ALTERNATE_RECIPIENT</span></span>  <br/> |
|<span data-ttu-id="ba290-108">Identificateur :</span><span class="sxs-lookup"><span data-stu-id="ba290-108">Identifier:</span></span>  <br/> |<span data-ttu-id="ba290-109">0x0C09</span><span class="sxs-lookup"><span data-stu-id="ba290-109">0x0C09</span></span>  <br/> |
|<span data-ttu-id="ba290-110">Type de données :</span><span class="sxs-lookup"><span data-stu-id="ba290-110">Data type:</span></span>  <br/> |<span data-ttu-id="ba290-111">PT_BINARY</span><span class="sxs-lookup"><span data-stu-id="ba290-111">PT_BINARY</span></span>  <br/> |
|<span data-ttu-id="ba290-112">Zone :</span><span class="sxs-lookup"><span data-stu-id="ba290-112">Area:</span></span>  <br/> |<span data-ttu-id="ba290-113">MIME</span><span class="sxs-lookup"><span data-stu-id="ba290-113">MIME</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="ba290-114">Remarques</span><span class="sxs-lookup"><span data-stu-id="ba290-114">Remarks</span></span>

<span data-ttu-id="ba290-115">Cette propriété est utilisée dans les messages transféré automatiquement.</span><span class="sxs-lookup"><span data-stu-id="ba290-115">This property is used in autoforwarded messages.</span></span> <span data-ttu-id="ba290-116">Si le transfert automatique n’est pas autorisée ou si aucune autre destinataire n’a été désigné, un rapport de non-remise doit être généré.</span><span class="sxs-lookup"><span data-stu-id="ba290-116">If autoforwarding is not permitted or if no alternate recipient has been designated, a nondelivery report should be generated.</span></span>
  
## <a name="related-resources"></a><span data-ttu-id="ba290-117">Ressources connexes</span><span class="sxs-lookup"><span data-stu-id="ba290-117">Related resources</span></span>

### <a name="header-files"></a><span data-ttu-id="ba290-118">Fichiers d’en-tête</span><span class="sxs-lookup"><span data-stu-id="ba290-118">Header files</span></span>

<span data-ttu-id="ba290-119">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="ba290-119">Mapidefs.h</span></span>
  
> <span data-ttu-id="ba290-120">Fournit des définitions de type de données.</span><span class="sxs-lookup"><span data-stu-id="ba290-120">Provides data type definitions.</span></span>
    
<span data-ttu-id="ba290-121">MAPITAGS.h</span><span class="sxs-lookup"><span data-stu-id="ba290-121">Mapitags.h</span></span>
  
> <span data-ttu-id="ba290-122">Contient les définitions des propriétés répertoriées en tant que d’autres noms.</span><span class="sxs-lookup"><span data-stu-id="ba290-122">Contains definitions of properties listed as alternate names.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="ba290-123">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="ba290-123">See also</span></span>



[<span data-ttu-id="ba290-124">Propriétés MAPI</span><span class="sxs-lookup"><span data-stu-id="ba290-124">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="ba290-125">Propriétés canoniques MAPI</span><span class="sxs-lookup"><span data-stu-id="ba290-125">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="ba290-126">Mappage de noms de propriété canonique aux noms MAPI</span><span class="sxs-lookup"><span data-stu-id="ba290-126">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="ba290-127">Mappage de noms MAPI pour les noms de propriété canonique</span><span class="sxs-lookup"><span data-stu-id="ba290-127">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

