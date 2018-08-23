---
title: Propriété canonique PidLidResponseStatus
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- PidLidResponseStatus
api_type:
- COM
ms.assetid: e56142fd-204b-497e-83b9-59f9acda6cb4
description: Dernière modification le 09 mars 2015
ms.openlocfilehash: 2e6aa8407459fef5fd9657e9d2887f0ae78ff9c9
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/23/2018
ms.locfileid: "22585464"
---
# <a name="pidlidresponsestatus-canonical-property"></a><span data-ttu-id="f4db5-103">Propriété canonique PidLidResponseStatus</span><span class="sxs-lookup"><span data-stu-id="f4db5-103">PidLidResponseStatus Canonical Property</span></span>

  
  
<span data-ttu-id="f4db5-104">**S’applique à**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="f4db5-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="f4db5-105">Spécifie l’état de la réponse d’un participant.</span><span class="sxs-lookup"><span data-stu-id="f4db5-105">Specifies the response status of an attendee.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="f4db5-106">Propriétés associées :</span><span class="sxs-lookup"><span data-stu-id="f4db5-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="f4db5-107">dispidResponseStatus</span><span class="sxs-lookup"><span data-stu-id="f4db5-107">dispidResponseStatus</span></span>  <br/> |
|<span data-ttu-id="f4db5-108">Jeu de propriétés :</span><span class="sxs-lookup"><span data-stu-id="f4db5-108">Property set:</span></span>  <br/> |<span data-ttu-id="f4db5-109">PSETID_Appointment</span><span class="sxs-lookup"><span data-stu-id="f4db5-109">PSETID_Appointment</span></span>  <br/> |
|<span data-ttu-id="f4db5-110">ID de type long (capot) :</span><span class="sxs-lookup"><span data-stu-id="f4db5-110">Long ID (LID):</span></span>  <br/> |<span data-ttu-id="f4db5-111">0x00008218</span><span class="sxs-lookup"><span data-stu-id="f4db5-111">0x00008218</span></span>  <br/> |
|<span data-ttu-id="f4db5-112">Type de données :</span><span class="sxs-lookup"><span data-stu-id="f4db5-112">Data type:</span></span>  <br/> |<span data-ttu-id="f4db5-113">PT_LONG</span><span class="sxs-lookup"><span data-stu-id="f4db5-113">PT_LONG</span></span>  <br/> |
|<span data-ttu-id="f4db5-114">Domaine :</span><span class="sxs-lookup"><span data-stu-id="f4db5-114">Area:</span></span>  <br/> |<span data-ttu-id="f4db5-115">Réunions</span><span class="sxs-lookup"><span data-stu-id="f4db5-115">Meetings</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="f4db5-116">Remarques</span><span class="sxs-lookup"><span data-stu-id="f4db5-116">Remarks</span></span>

<span data-ttu-id="f4db5-117">L’état de réponse doit être une des valeurs dans le tableau ci-dessous.</span><span class="sxs-lookup"><span data-stu-id="f4db5-117">The response status must be one of the values in the table below.</span></span>
  
|<span data-ttu-id="f4db5-118">**État de réponse**</span><span class="sxs-lookup"><span data-stu-id="f4db5-118">**Response status**</span></span>|<span data-ttu-id="f4db5-119">**Valeur**</span><span class="sxs-lookup"><span data-stu-id="f4db5-119">**Value**</span></span>|<span data-ttu-id="f4db5-120">**Description**</span><span class="sxs-lookup"><span data-stu-id="f4db5-120">**Description**</span></span>|
|:-----|:-----|:-----|
|<span data-ttu-id="f4db5-121">respNone</span><span class="sxs-lookup"><span data-stu-id="f4db5-121">respNone</span></span>  <br/> |<span data-ttu-id="f4db5-122">0x00000000</span><span class="sxs-lookup"><span data-stu-id="f4db5-122">0x00000000</span></span>  <br/> |<span data-ttu-id="f4db5-123">Aucune réponse n’est requise pour cet objet.</span><span class="sxs-lookup"><span data-stu-id="f4db5-123">No response is required for this object.</span></span> <span data-ttu-id="f4db5-124">C’est le cas pour les objets de rendez-vous et des objets de réponse de réunion.</span><span class="sxs-lookup"><span data-stu-id="f4db5-124">This is the case for appointment objects and meeting response objects.</span></span>  <br/> |
|<span data-ttu-id="f4db5-125">respOrganized</span><span class="sxs-lookup"><span data-stu-id="f4db5-125">respOrganized</span></span>  <br/> |<span data-ttu-id="f4db5-126">0x00000001</span><span class="sxs-lookup"><span data-stu-id="f4db5-126">0x00000001</span></span>  <br/> |<span data-ttu-id="f4db5-127">Cette réunion appartient à l’organisateur.</span><span class="sxs-lookup"><span data-stu-id="f4db5-127">This meeting belongs to the organizer.</span></span>  <br/> |
|<span data-ttu-id="f4db5-128">respTentative</span><span class="sxs-lookup"><span data-stu-id="f4db5-128">respTentative</span></span>  <br/> |<span data-ttu-id="f4db5-129">0x00000002</span><span class="sxs-lookup"><span data-stu-id="f4db5-129">0x00000002</span></span>  <br/> |<span data-ttu-id="f4db5-130">Cette valeur sur la réunion du participant indique que le participant a provisoirement accepté la demande de réunion.</span><span class="sxs-lookup"><span data-stu-id="f4db5-130">This value on the attendee's meeting indicates that the attendee has tentatively accepted the meeting request.</span></span>  <br/> |
|<span data-ttu-id="f4db5-131">respAccepted</span><span class="sxs-lookup"><span data-stu-id="f4db5-131">respAccepted</span></span>  <br/> |<span data-ttu-id="f4db5-132">0 x 00000003</span><span class="sxs-lookup"><span data-stu-id="f4db5-132">0x00000003</span></span>  <br/> |<span data-ttu-id="f4db5-133">Cette valeur t de réunion du participant indique que le participant a accepté la demande de réunion.</span><span class="sxs-lookup"><span data-stu-id="f4db5-133">This value on the attendee's meeting t indicates that the attendee has accepted the meeting request.</span></span>  <br/> |
|<span data-ttu-id="f4db5-134">respDeclined</span><span class="sxs-lookup"><span data-stu-id="f4db5-134">respDeclined</span></span>  <br/> |<span data-ttu-id="f4db5-135">0 x 00000004</span><span class="sxs-lookup"><span data-stu-id="f4db5-135">0x00000004</span></span>  <br/> |<span data-ttu-id="f4db5-136">Cette valeur sur la réunion du participant indique que le participant a refusé la demande de réunion.</span><span class="sxs-lookup"><span data-stu-id="f4db5-136">This value on the attendee's meeting indicates that the attendee has declined the meeting request.</span></span>  <br/> |
|<span data-ttu-id="f4db5-137">respNotResponded</span><span class="sxs-lookup"><span data-stu-id="f4db5-137">respNotResponded</span></span>  <br/> |<span data-ttu-id="f4db5-138">0 x 00000005</span><span class="sxs-lookup"><span data-stu-id="f4db5-138">0x00000005</span></span>  <br/> |<span data-ttu-id="f4db5-139">Cette valeur sur la réunion du participant indique que le participant n’a pas encore répondu.</span><span class="sxs-lookup"><span data-stu-id="f4db5-139">This value on the attendee's meeting indicates the attendee has not yet responded.</span></span> <span data-ttu-id="f4db5-140">Cette valeur est dans la demande de réunion, mise à jour de la réunion, l’annulation de réunion.</span><span class="sxs-lookup"><span data-stu-id="f4db5-140">This value is on the meeting request, meeting update, and meeting cancelation.</span></span>  <br/> |
   
## <a name="related-resources"></a><span data-ttu-id="f4db5-141">Ressources connexes</span><span class="sxs-lookup"><span data-stu-id="f4db5-141">Related resources</span></span>

### <a name="protocol-specifications"></a><span data-ttu-id="f4db5-142">Spécifications du protocole</span><span class="sxs-lookup"><span data-stu-id="f4db5-142">Protocol specifications</span></span>

<span data-ttu-id="f4db5-143">[[MS-OXPROPS]](http://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="f4db5-143">[[MS-OXPROPS]](http://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="f4db5-144">Fournit des définitions de jeu de propriétés et des références aux spécifications du protocole Exchange Server connexes.</span><span class="sxs-lookup"><span data-stu-id="f4db5-144">Provides property set definitions and references to related Exchange Server protocol specifications.</span></span>
    
<span data-ttu-id="f4db5-145">[[MS-OXOCAL]](http://msdn.microsoft.com/library/09861fde-c8e4-4028-9346-e7c214cfdba1%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="f4db5-145">[[MS-OXOCAL]](http://msdn.microsoft.com/library/09861fde-c8e4-4028-9346-e7c214cfdba1%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="f4db5-146">Spécifie les propriétés et opérations pour un rendez-vous, une demande de réunion et les messages de réponse.</span><span class="sxs-lookup"><span data-stu-id="f4db5-146">Specifies the properties and operations for appointment, meeting request, and response messages.</span></span>
    
### <a name="header-files"></a><span data-ttu-id="f4db5-147">Fichiers d’en-tête</span><span class="sxs-lookup"><span data-stu-id="f4db5-147">Header files</span></span>

<span data-ttu-id="f4db5-148">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="f4db5-148">Mapidefs.h</span></span>
  
> <span data-ttu-id="f4db5-149">Fournit des définitions de type de données.</span><span class="sxs-lookup"><span data-stu-id="f4db5-149">Provides data type definitions.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="f4db5-150">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="f4db5-150">See also</span></span>



[<span data-ttu-id="f4db5-151">Propriétés MAPI</span><span class="sxs-lookup"><span data-stu-id="f4db5-151">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="f4db5-152">Propriétés canoniques MAPI</span><span class="sxs-lookup"><span data-stu-id="f4db5-152">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="f4db5-153">Mappage des noms de propriétés canoniques aux noms MAPI</span><span class="sxs-lookup"><span data-stu-id="f4db5-153">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="f4db5-154">Mappage des noms MAPI aux noms de propriétés canoniques</span><span class="sxs-lookup"><span data-stu-id="f4db5-154">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

