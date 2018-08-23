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
description: Dernière modification le 09 mars 2015
ms.openlocfilehash: f636c0a49d6ad96ab157d00780fa6ffc5c8f3236
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/23/2018
ms.locfileid: "22588271"
---
# <a name="pidtagdeferredsendtime-canonical-property"></a><span data-ttu-id="f58c3-103">Propriété canonique PidTagDeferredSendTime</span><span class="sxs-lookup"><span data-stu-id="f58c3-103">PidTagDeferredSendTime Canonical Property</span></span>

  
  
<span data-ttu-id="f58c3-104">**S’applique à**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="f58c3-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="f58c3-105">Indique une heure lorsqu’un client souhaite différer l’envoi d’un message.</span><span class="sxs-lookup"><span data-stu-id="f58c3-105">Indicates a time when a client would like to defer sending a message.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="f58c3-106">Propriétés associées :</span><span class="sxs-lookup"><span data-stu-id="f58c3-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="f58c3-107">PR_DEFERRED_SEND_TIME</span><span class="sxs-lookup"><span data-stu-id="f58c3-107">PR_DEFERRED_SEND_TIME</span></span>  <br/> |
|<span data-ttu-id="f58c3-108">Identificateur :</span><span class="sxs-lookup"><span data-stu-id="f58c3-108">Identifier:</span></span>  <br/> |<span data-ttu-id="f58c3-109">0x3FEF</span><span class="sxs-lookup"><span data-stu-id="f58c3-109">0x3FEF</span></span>  <br/> |
|<span data-ttu-id="f58c3-110">Type de données :</span><span class="sxs-lookup"><span data-stu-id="f58c3-110">Data type:</span></span>  <br/> |<span data-ttu-id="f58c3-111">PT_SYSTIME</span><span class="sxs-lookup"><span data-stu-id="f58c3-111">PT_SYSTIME</span></span>  <br/> |
|<span data-ttu-id="f58c3-112">Domaine :</span><span class="sxs-lookup"><span data-stu-id="f58c3-112">Area:</span></span>  <br/> |<span data-ttu-id="f58c3-113">État MAPI</span><span class="sxs-lookup"><span data-stu-id="f58c3-113">MAPI status</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="f58c3-114">Remarques</span><span class="sxs-lookup"><span data-stu-id="f58c3-114">Remarks</span></span>

<span data-ttu-id="f58c3-115">Si les **PR_DEFERRED_SEND_UNITS** ([PidTagDeferredSendUnits](pidtagdeferredsendunits-canonical-property.md)) et les propriétés de **PR_DEFERRED_SEND_NUMBER** ([PidTagDeferredSendNumber](pidtagdeferredsendnumber-canonical-property.md)) sont présentes, la valeur de cette propriété est recalculée à l’aide de la formule suivante et l’ancienne valeur est ignorée.</span><span class="sxs-lookup"><span data-stu-id="f58c3-115">If the **PR_DEFERRED_SEND_UNITS** ([PidTagDeferredSendUnits](pidtagdeferredsendunits-canonical-property.md)) and **PR_DEFERRED_SEND_NUMBER** ([PidTagDeferredSendNumber](pidtagdeferredsendnumber-canonical-property.md)) properties are present, the value of this property is recomputed by using the following formula and the old value is ignored.</span></span>
  
 <span data-ttu-id="f58c3-116">**PR_DEFERRED_SEND_TIME** = **PR_CLIENT_SUBMIT_TIME** ([PidTagClientSubmitTime](pidtagclientsubmittime-canonical-property.md)) + **PR_DEFERRED_SEND_NUMBER** \* heure (**PR_DEFERRED_SEND_UNITS**)</span><span class="sxs-lookup"><span data-stu-id="f58c3-116">**PR_DEFERRED_SEND_TIME** = **PR_CLIENT_SUBMIT_TIME** ([PidTagClientSubmitTime](pidtagclientsubmittime-canonical-property.md)) + **PR_DEFERRED_SEND_NUMBER** \* TimeOf(**PR_DEFERRED_SEND_UNITS**)</span></span>
  
<span data-ttu-id="f58c3-117">Si la valeur **PR_DEFERRED_SEND_TIME** est antérieure à l’heure actuelle (en UTC), le message est envoyé immédiatement.</span><span class="sxs-lookup"><span data-stu-id="f58c3-117">If **PR_DEFERRED_SEND_TIME** value is earlier than the current time (in UTC), the message is sent immediately.</span></span> 
  
## <a name="related-resources"></a><span data-ttu-id="f58c3-118">Ressources connexes</span><span class="sxs-lookup"><span data-stu-id="f58c3-118">Related resources</span></span>

### <a name="protocol-specifications"></a><span data-ttu-id="f58c3-119">Spécifications du protocole</span><span class="sxs-lookup"><span data-stu-id="f58c3-119">Protocol specifications</span></span>

<span data-ttu-id="f58c3-120">[[MS-OXOMSG]](http://msdn.microsoft.com/library/daa9120f-f325-4afb-a738-28f91049ab3c%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="f58c3-120">[[MS-OXOMSG]](http://msdn.microsoft.com/library/daa9120f-f325-4afb-a738-28f91049ab3c%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="f58c3-121">Spécifie les propriétés et les opérations qui sont autorisées pour les objets de message électronique.</span><span class="sxs-lookup"><span data-stu-id="f58c3-121">Specifies the properties and operations that are permissible for email message objects.</span></span>
    
### <a name="header-files"></a><span data-ttu-id="f58c3-122">Fichiers d’en-tête</span><span class="sxs-lookup"><span data-stu-id="f58c3-122">Header files</span></span>

<span data-ttu-id="f58c3-123">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="f58c3-123">Mapidefs.h</span></span>
  
> <span data-ttu-id="f58c3-124">Fournit des définitions de type de données.</span><span class="sxs-lookup"><span data-stu-id="f58c3-124">Provides data type definitions.</span></span>
    
<span data-ttu-id="f58c3-125">MAPITAGS.h</span><span class="sxs-lookup"><span data-stu-id="f58c3-125">Mapitags.h</span></span>
  
> <span data-ttu-id="f58c3-126">Contient les définitions des propriétés répertoriées en tant que d’autres noms.</span><span class="sxs-lookup"><span data-stu-id="f58c3-126">Contains definitions of properties listed as alternate names.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="f58c3-127">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="f58c3-127">See also</span></span>



[<span data-ttu-id="f58c3-128">Propriétés MAPI</span><span class="sxs-lookup"><span data-stu-id="f58c3-128">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="f58c3-129">Propriétés canoniques MAPI</span><span class="sxs-lookup"><span data-stu-id="f58c3-129">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="f58c3-130">Mappage des noms de propriétés canoniques aux noms MAPI</span><span class="sxs-lookup"><span data-stu-id="f58c3-130">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="f58c3-131">Mappage des noms MAPI aux noms de propriétés canoniques</span><span class="sxs-lookup"><span data-stu-id="f58c3-131">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

