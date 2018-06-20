---
title: Propriété canonique PidTagDeliverTime
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- PidTagDeliverTime
api_type:
- HeaderDef
ms.assetid: da0ad17b-08ac-4c50-ac1d-13062b890dfd
description: 'Derni�re modification�: lundi 9 mars 2015'
ms.openlocfilehash: 40839e34a61b5e5fdd3d7b69d8c553d7e469cd22
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19785921"
---
# <a name="pidtagdelivertime-canonical-property"></a><span data-ttu-id="9e0f8-103">Propriété canonique PidTagDeliverTime</span><span class="sxs-lookup"><span data-stu-id="9e0f8-103">PidTagDeliverTime Canonical Property</span></span>

  
  
<span data-ttu-id="9e0f8-104">**S’applique à**: Outlook</span><span class="sxs-lookup"><span data-stu-id="9e0f8-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="9e0f8-105">Contient la date et l’heure lorsque le message d’origine a été remis.</span><span class="sxs-lookup"><span data-stu-id="9e0f8-105">Contains the date and time when the original message was delivered.</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="9e0f8-106">Propriétés associées :</span><span class="sxs-lookup"><span data-stu-id="9e0f8-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="9e0f8-107">PR_DELIVER_TIME</span><span class="sxs-lookup"><span data-stu-id="9e0f8-107">PR_DELIVER_TIME</span></span>  <br/> |
|<span data-ttu-id="9e0f8-108">Identificateur :</span><span class="sxs-lookup"><span data-stu-id="9e0f8-108">Identifier:</span></span>  <br/> |<span data-ttu-id="9e0f8-109">0x0010</span><span class="sxs-lookup"><span data-stu-id="9e0f8-109">0x0010</span></span>  <br/> |
|<span data-ttu-id="9e0f8-110">Type de données :</span><span class="sxs-lookup"><span data-stu-id="9e0f8-110">Data type:</span></span>  <br/> |<span data-ttu-id="9e0f8-111">PT_SYSTIME</span><span class="sxs-lookup"><span data-stu-id="9e0f8-111">PT_SYSTIME</span></span>  <br/> |
|<span data-ttu-id="9e0f8-112">Zone :</span><span class="sxs-lookup"><span data-stu-id="9e0f8-112">Area:</span></span>  <br/> |<span data-ttu-id="9e0f8-113">Enveloppe MAPI</span><span class="sxs-lookup"><span data-stu-id="9e0f8-113">MAPI envelope</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="9e0f8-114">Remarques</span><span class="sxs-lookup"><span data-stu-id="9e0f8-114">Remarks</span></span>

<span data-ttu-id="9e0f8-115">Cette propriété est une propriété par destinataire sur un rapport de remise qui indique le temps que le message d’origine a été remis à l’utilisateur de messagerie pour lequel le rapport de remise est généré.</span><span class="sxs-lookup"><span data-stu-id="9e0f8-115">This property is a per-recipient property on a delivery report that indicates the time the original message was delivered to the messaging user for which the delivery report is being generated.</span></span>
  
## <a name="related-resources"></a><span data-ttu-id="9e0f8-116">Ressources connexes</span><span class="sxs-lookup"><span data-stu-id="9e0f8-116">Related resources</span></span>

### <a name="header-files"></a><span data-ttu-id="9e0f8-117">Fichiers d’en-tête</span><span class="sxs-lookup"><span data-stu-id="9e0f8-117">Header files</span></span>

<span data-ttu-id="9e0f8-118">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="9e0f8-118">Mapidefs.h</span></span>
  
> <span data-ttu-id="9e0f8-119">Fournit des définitions de type de données.</span><span class="sxs-lookup"><span data-stu-id="9e0f8-119">Provides data type definitions.</span></span>
    
<span data-ttu-id="9e0f8-120">MAPITAGS.h</span><span class="sxs-lookup"><span data-stu-id="9e0f8-120">Mapitags.h</span></span>
  
> <span data-ttu-id="9e0f8-121">Contient les définitions des propriétés répertoriées en tant que d’autres noms.</span><span class="sxs-lookup"><span data-stu-id="9e0f8-121">Contains definitions of properties listed as alternate names.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="9e0f8-122">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="9e0f8-122">See also</span></span>



[<span data-ttu-id="9e0f8-123">IMAPISupport::StatusRecips</span><span class="sxs-lookup"><span data-stu-id="9e0f8-123">IMAPISupport::StatusRecips</span></span>](imapisupport-statusrecips.md)


[<span data-ttu-id="9e0f8-124">Propriétés MAPI</span><span class="sxs-lookup"><span data-stu-id="9e0f8-124">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="9e0f8-125">Propriétés canoniques MAPI</span><span class="sxs-lookup"><span data-stu-id="9e0f8-125">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="9e0f8-126">Mappage de noms de propriété canonique aux noms MAPI</span><span class="sxs-lookup"><span data-stu-id="9e0f8-126">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="9e0f8-127">Mappage de noms MAPI pour les noms de propriété canonique</span><span class="sxs-lookup"><span data-stu-id="9e0f8-127">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

