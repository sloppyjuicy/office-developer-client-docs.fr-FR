---
title: Propriété canonique PidTagDeferredSendTime
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- PidTagDeferredSendTime
api_type:
- HeaderDef
ms.assetid: ee206c2d-8371-4d19-b42b-78f6479e13ca
description: 'Derni�re modification�: lundi 9 mars 2015'
ms.openlocfilehash: 3912c429f1aa932b4956d943579a4ed99634dca2
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19785903"
---
# <a name="pidtagdeferredsendtime-canonical-property"></a><span data-ttu-id="8d904-103">Propriété canonique PidTagDeferredSendTime</span><span class="sxs-lookup"><span data-stu-id="8d904-103">PidTagDeferredSendTime Canonical Property</span></span>

  
  
<span data-ttu-id="8d904-104">**S’applique à**: Outlook</span><span class="sxs-lookup"><span data-stu-id="8d904-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="8d904-105">Indique une heure lorsqu’un client souhaite différer l’envoi d’un message.</span><span class="sxs-lookup"><span data-stu-id="8d904-105">Indicates a time when a client would like to defer sending a message.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="8d904-106">Propriétés associées :</span><span class="sxs-lookup"><span data-stu-id="8d904-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="8d904-107">PR_DEFERRED_SEND_TIME</span><span class="sxs-lookup"><span data-stu-id="8d904-107">PR_DEFERRED_SEND_TIME</span></span>  <br/> |
|<span data-ttu-id="8d904-108">Identificateur :</span><span class="sxs-lookup"><span data-stu-id="8d904-108">Identifier:</span></span>  <br/> |<span data-ttu-id="8d904-109">0x3FEF</span><span class="sxs-lookup"><span data-stu-id="8d904-109">0x3FEF</span></span>  <br/> |
|<span data-ttu-id="8d904-110">Type de données :</span><span class="sxs-lookup"><span data-stu-id="8d904-110">Data type:</span></span>  <br/> |<span data-ttu-id="8d904-111">PT_SYSTIME</span><span class="sxs-lookup"><span data-stu-id="8d904-111">PT_SYSTIME</span></span>  <br/> |
|<span data-ttu-id="8d904-112">Zone :</span><span class="sxs-lookup"><span data-stu-id="8d904-112">Area:</span></span>  <br/> |<span data-ttu-id="8d904-113">État MAPI</span><span class="sxs-lookup"><span data-stu-id="8d904-113">MAPI status</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="8d904-114">Remarques</span><span class="sxs-lookup"><span data-stu-id="8d904-114">Remarks</span></span>

<span data-ttu-id="8d904-115">Si les **PR_DEFERRED_SEND_UNITS** ([PidTagDeferredSendUnits](pidtagdeferredsendunits-canonical-property.md)) et les propriétés de **PR_DEFERRED_SEND_NUMBER** ([PidTagDeferredSendNumber](pidtagdeferredsendnumber-canonical-property.md)) sont présentes, la valeur de cette propriété est recalculée à l’aide de la formule suivante et l’ancienne valeur est ignorée.</span><span class="sxs-lookup"><span data-stu-id="8d904-115">If the **PR_DEFERRED_SEND_UNITS** ([PidTagDeferredSendUnits](pidtagdeferredsendunits-canonical-property.md)) and **PR_DEFERRED_SEND_NUMBER** ([PidTagDeferredSendNumber](pidtagdeferredsendnumber-canonical-property.md)) properties are present, the value of this property is recomputed by using the following formula and the old value is ignored.</span></span>
  
 <span data-ttu-id="8d904-116">**PR_DEFERRED_SEND_TIME** = **PR_CLIENT_SUBMIT_TIME** ([PidTagClientSubmitTime](pidtagclientsubmittime-canonical-property.md)) + **PR_DEFERRED_SEND_NUMBER** \* heure (**PR_DEFERRED_SEND_UNITS**)</span><span class="sxs-lookup"><span data-stu-id="8d904-116">**PR_DEFERRED_SEND_TIME** = **PR_CLIENT_SUBMIT_TIME** ([PidTagClientSubmitTime](pidtagclientsubmittime-canonical-property.md)) + **PR_DEFERRED_SEND_NUMBER** \* TimeOf(**PR_DEFERRED_SEND_UNITS**)</span></span>
  
<span data-ttu-id="8d904-117">Si la valeur **PR_DEFERRED_SEND_TIME** est antérieure à l’heure actuelle (en UTC), le message est envoyé immédiatement.</span><span class="sxs-lookup"><span data-stu-id="8d904-117">If **PR_DEFERRED_SEND_TIME** value is earlier than the current time (in UTC), the message is sent immediately.</span></span> 
  
## <a name="related-resources"></a><span data-ttu-id="8d904-118">Ressources connexes</span><span class="sxs-lookup"><span data-stu-id="8d904-118">Related resources</span></span>

### <a name="protocol-specifications"></a><span data-ttu-id="8d904-119">Spécifications du protocole</span><span class="sxs-lookup"><span data-stu-id="8d904-119">Protocol specifications</span></span>

<span data-ttu-id="8d904-120">[[MS-OXOMSG]](http://msdn.microsoft.com/library/daa9120f-f325-4afb-a738-28f91049ab3c%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="8d904-120">[[MS-OXOMSG]](http://msdn.microsoft.com/library/daa9120f-f325-4afb-a738-28f91049ab3c%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="8d904-121">Spécifie les propriétés et les opérations qui sont autorisées pour les objets de message électronique.</span><span class="sxs-lookup"><span data-stu-id="8d904-121">Specifies the properties and operations that are permissible for email message objects.</span></span>
    
### <a name="header-files"></a><span data-ttu-id="8d904-122">Fichiers d’en-tête</span><span class="sxs-lookup"><span data-stu-id="8d904-122">Header files</span></span>

<span data-ttu-id="8d904-123">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="8d904-123">Mapidefs.h</span></span>
  
> <span data-ttu-id="8d904-124">Fournit des définitions de type de données.</span><span class="sxs-lookup"><span data-stu-id="8d904-124">Provides data type definitions.</span></span>
    
<span data-ttu-id="8d904-125">MAPITAGS.h</span><span class="sxs-lookup"><span data-stu-id="8d904-125">Mapitags.h</span></span>
  
> <span data-ttu-id="8d904-126">Contient les définitions des propriétés répertoriées en tant que d’autres noms.</span><span class="sxs-lookup"><span data-stu-id="8d904-126">Contains definitions of properties listed as alternate names.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="8d904-127">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="8d904-127">See also</span></span>



[<span data-ttu-id="8d904-128">Propriétés MAPI</span><span class="sxs-lookup"><span data-stu-id="8d904-128">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="8d904-129">Propriétés canoniques MAPI</span><span class="sxs-lookup"><span data-stu-id="8d904-129">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="8d904-130">Mappage de noms de propriété canonique aux noms MAPI</span><span class="sxs-lookup"><span data-stu-id="8d904-130">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="8d904-131">Mappage de noms MAPI pour les noms de propriété canonique</span><span class="sxs-lookup"><span data-stu-id="8d904-131">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

