---
title: Propriété canonique PidTagRecipientTrackStatus
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- MAPI.PidTagRecipientTrackStatus
api_type:
- COM
ms.assetid: d619b5e7-2867-44fc-9b42-123bb1bf7bde
description: Dernière modification le 9 mars 2015
ms.openlocfilehash: 074bcf7c051b78bc32caf66502747e7fb1ab6b79
ms.sourcegitcommit: ef717c65d8dd41ababffb01eafc443c79950aed4
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 10/04/2018
ms.locfileid: "25389889"
---
# <a name="pidtagrecipienttrackstatus-canonical-property"></a><span data-ttu-id="07962-103">Propriété canonique PidTagRecipientTrackStatus</span><span class="sxs-lookup"><span data-stu-id="07962-103">PidTagRecipientTrackStatus Canonical Property</span></span>

  
  
<span data-ttu-id="07962-104">**S’applique à** : Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="07962-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="07962-105">Indique l’état de la réponse renvoyée par le participant.</span><span class="sxs-lookup"><span data-stu-id="07962-105">Indicates the response status returned by the attendee.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="07962-106">Propriétés associées :</span><span class="sxs-lookup"><span data-stu-id="07962-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="07962-107">PR_RECIPIENT_TRACKSTATUS</span><span class="sxs-lookup"><span data-stu-id="07962-107">PR_RECIPIENT_TRACKSTATUS</span></span>  <br/> |
|<span data-ttu-id="07962-108">Identificateur :</span><span class="sxs-lookup"><span data-stu-id="07962-108">Identifier:</span></span>  <br/> |<span data-ttu-id="07962-109">0x5FFF</span><span class="sxs-lookup"><span data-stu-id="07962-109">0x5FFF</span></span>  <br/> |
|<span data-ttu-id="07962-110">Type de données :</span><span class="sxs-lookup"><span data-stu-id="07962-110">Data type:</span></span>  <br/> |<span data-ttu-id="07962-111">PT_LONG</span><span class="sxs-lookup"><span data-stu-id="07962-111">PT_LONG</span></span>  <br/> |
|<span data-ttu-id="07962-112">Domaine :</span><span class="sxs-lookup"><span data-stu-id="07962-112">Area:</span></span>  <br/> |<span data-ttu-id="07962-113">Destinataire de transport</span><span class="sxs-lookup"><span data-stu-id="07962-113">Transport recipient</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="07962-114">Remarques</span><span class="sxs-lookup"><span data-stu-id="07962-114">Remarks</span></span>

<span data-ttu-id="07962-115">Si cette valeur n’est pas définie, il doit être supposé pour être respNone.</span><span class="sxs-lookup"><span data-stu-id="07962-115">If this value is not set, it must be assumed to be respNone.</span></span> <span data-ttu-id="07962-116">Dans le cas contraire, il doit être une des options suivantes :</span><span class="sxs-lookup"><span data-stu-id="07962-116">Otherwise, it must be one of the following:</span></span>
  
|<span data-ttu-id="07962-117">**État de réponse**</span><span class="sxs-lookup"><span data-stu-id="07962-117">**Response status**</span></span>|<span data-ttu-id="07962-118">**Valeur**</span><span class="sxs-lookup"><span data-stu-id="07962-118">**Value**</span></span>|<span data-ttu-id="07962-119">**Description**</span><span class="sxs-lookup"><span data-stu-id="07962-119">**Description**</span></span>|
|:-----|:-----|:-----|
|<span data-ttu-id="07962-120">respNone</span><span class="sxs-lookup"><span data-stu-id="07962-120">respNone</span></span>  <br/> |<span data-ttu-id="07962-121">0x00000000</span><span class="sxs-lookup"><span data-stu-id="07962-121">0x00000000</span></span>  <br/> |<span data-ttu-id="07962-122">Aucune réponse n’est requise pour cet objet.</span><span class="sxs-lookup"><span data-stu-id="07962-122">No response is required for this object.</span></span> <span data-ttu-id="07962-123">C’est le cas pour les objets de rendez-vous et des objets de réponse de réunion.</span><span class="sxs-lookup"><span data-stu-id="07962-123">This is the case for appointment objects and meeting response objects.</span></span>  <br/> |
|<span data-ttu-id="07962-124">respTentative</span><span class="sxs-lookup"><span data-stu-id="07962-124">respTentative</span></span>  <br/> |<span data-ttu-id="07962-125">0x00000002</span><span class="sxs-lookup"><span data-stu-id="07962-125">0x00000002</span></span>  <br/> |<span data-ttu-id="07962-126">Cette valeur sur l’objet de réunion du participant indique que le participant a accepté provisoirement la réunion objet de requête.</span><span class="sxs-lookup"><span data-stu-id="07962-126">This value on the attendee's meeting object indicates that the attendee has tentatively accepted the meeting request object.</span></span>  <br/> |
|<span data-ttu-id="07962-127">respAccepted</span><span class="sxs-lookup"><span data-stu-id="07962-127">respAccepted</span></span>  <br/> |<span data-ttu-id="07962-128">0 x 00000003</span><span class="sxs-lookup"><span data-stu-id="07962-128">0x00000003</span></span>  <br/> |<span data-ttu-id="07962-129">Cette valeur sur l’objet de réunion du participant indique que le participant a accepté la réunion objet de requête.</span><span class="sxs-lookup"><span data-stu-id="07962-129">This value on the attendee's meeting object indicates that the attendee has accepted the meeting request object.</span></span>  <br/> |
|<span data-ttu-id="07962-130">respDeclined</span><span class="sxs-lookup"><span data-stu-id="07962-130">respDeclined</span></span>  <br/> |<span data-ttu-id="07962-131">0 x 00000004</span><span class="sxs-lookup"><span data-stu-id="07962-131">0x00000004</span></span>  <br/> |<span data-ttu-id="07962-132">Cette valeur sur l’objet de réunion du participant indique que le participant a refusé la réunion objet de requête.</span><span class="sxs-lookup"><span data-stu-id="07962-132">This value on the attendee's meeting object indicates that the attendee has declined the meeting request object.</span></span>  <br/> |
   
## <a name="related-resources"></a><span data-ttu-id="07962-133">Ressources connexes</span><span class="sxs-lookup"><span data-stu-id="07962-133">Related resources</span></span>

### <a name="protocol-specifications"></a><span data-ttu-id="07962-134">Spécifications du protocole</span><span class="sxs-lookup"><span data-stu-id="07962-134">Protocol specifications</span></span>

<span data-ttu-id="07962-135">[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="07962-135">[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="07962-136">Fournit des références aux spécifications du protocole Exchange Server associées.</span><span class="sxs-lookup"><span data-stu-id="07962-136">Provides references to related Exchange Server protocol specifications.</span></span>
    
<span data-ttu-id="07962-137">[[MS-OXOCAL]](https://msdn.microsoft.com/library/09861fde-c8e4-4028-9346-e7c214cfdba1%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="07962-137">[[MS-OXOCAL]](https://msdn.microsoft.com/library/09861fde-c8e4-4028-9346-e7c214cfdba1%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="07962-138">Spécifie les propriétés et opérations pour un rendez-vous, une demande de réunion et les messages de réponse.</span><span class="sxs-lookup"><span data-stu-id="07962-138">Specifies the properties and operations for appointment, meeting request, and response messages.</span></span>
    
<span data-ttu-id="07962-139">[[MS-OXCMSG]](https://msdn.microsoft.com/library/7fd7ec40-deec-4c06-9493-1bc06b349682%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="07962-139">[[MS-OXCMSG]](https://msdn.microsoft.com/library/7fd7ec40-deec-4c06-9493-1bc06b349682%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="07962-140">Gère les objets de message et la pièce jointe.</span><span class="sxs-lookup"><span data-stu-id="07962-140">Handles message and attachment objects.</span></span>
    
### <a name="header-files"></a><span data-ttu-id="07962-141">Fichiers d’en-tête</span><span class="sxs-lookup"><span data-stu-id="07962-141">Header files</span></span>

<span data-ttu-id="07962-142">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="07962-142">Mapidefs.h</span></span>
  
> <span data-ttu-id="07962-143">Fournit des définitions de type de données.</span><span class="sxs-lookup"><span data-stu-id="07962-143">Provides data type definitions.</span></span>
    
<span data-ttu-id="07962-144">MAPITAGS.h</span><span class="sxs-lookup"><span data-stu-id="07962-144">Mapitags.h</span></span>
  
> <span data-ttu-id="07962-145">Contient les définitions des propriétés répertoriées en tant que d’autres noms.</span><span class="sxs-lookup"><span data-stu-id="07962-145">Contains definitions of properties listed as alternate names.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="07962-146">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="07962-146">See also</span></span>



[<span data-ttu-id="07962-147">Propriétés MAPI</span><span class="sxs-lookup"><span data-stu-id="07962-147">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="07962-148">Propriétés canoniques MAPI</span><span class="sxs-lookup"><span data-stu-id="07962-148">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="07962-149">Mappage des noms de propriétés canoniques aux noms MAPI</span><span class="sxs-lookup"><span data-stu-id="07962-149">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="07962-150">Mappage des noms MAPI aux noms de propriétés canoniques</span><span class="sxs-lookup"><span data-stu-id="07962-150">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

