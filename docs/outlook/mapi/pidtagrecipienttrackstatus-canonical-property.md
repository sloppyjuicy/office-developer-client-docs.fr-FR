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
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32355285"
---
# <a name="pidtagrecipienttrackstatus-canonical-property"></a><span data-ttu-id="88481-103">Propriété canonique PidTagRecipientTrackStatus</span><span class="sxs-lookup"><span data-stu-id="88481-103">PidTagRecipientTrackStatus Canonical Property</span></span>

  
  
<span data-ttu-id="88481-104">**S’applique à** : Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="88481-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="88481-105">Indique l’état de réponse renvoyé par le participant.</span><span class="sxs-lookup"><span data-stu-id="88481-105">Indicates the response status returned by the attendee.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="88481-106">Propriétés associées :</span><span class="sxs-lookup"><span data-stu-id="88481-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="88481-107">PR_RECIPIENT_TRACKSTATUS</span><span class="sxs-lookup"><span data-stu-id="88481-107">PR_RECIPIENT_TRACKSTATUS</span></span>  <br/> |
|<span data-ttu-id="88481-108">Identificateur :</span><span class="sxs-lookup"><span data-stu-id="88481-108">Identifier:</span></span>  <br/> |<span data-ttu-id="88481-109">0x5FFF</span><span class="sxs-lookup"><span data-stu-id="88481-109">0x5FFF</span></span>  <br/> |
|<span data-ttu-id="88481-110">Type de données :</span><span class="sxs-lookup"><span data-stu-id="88481-110">Data type:</span></span>  <br/> |<span data-ttu-id="88481-111">PT_LONG</span><span class="sxs-lookup"><span data-stu-id="88481-111">PT_LONG</span></span>  <br/> |
|<span data-ttu-id="88481-112">Domaine :</span><span class="sxs-lookup"><span data-stu-id="88481-112">Area:</span></span>  <br/> |<span data-ttu-id="88481-113">Destinataire de transport</span><span class="sxs-lookup"><span data-stu-id="88481-113">Transport recipient</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="88481-114">Remarques</span><span class="sxs-lookup"><span data-stu-id="88481-114">Remarks</span></span>

<span data-ttu-id="88481-115">Si cette valeur n’est pas définie, elle doit être supposée être respNone.</span><span class="sxs-lookup"><span data-stu-id="88481-115">If this value is not set, it must be assumed to be respNone.</span></span> <span data-ttu-id="88481-116">Dans le cas contraire, elle doit être l’une des suivantes :</span><span class="sxs-lookup"><span data-stu-id="88481-116">Otherwise, it must be one of the following:</span></span>
  
|<span data-ttu-id="88481-117">**État de la réponse**</span><span class="sxs-lookup"><span data-stu-id="88481-117">**Response status**</span></span>|<span data-ttu-id="88481-118">**Valeur**</span><span class="sxs-lookup"><span data-stu-id="88481-118">**Value**</span></span>|<span data-ttu-id="88481-119">**Description**</span><span class="sxs-lookup"><span data-stu-id="88481-119">**Description**</span></span>|
|:-----|:-----|:-----|
|<span data-ttu-id="88481-120">respNone</span><span class="sxs-lookup"><span data-stu-id="88481-120">respNone</span></span>  <br/> |<span data-ttu-id="88481-121">0x00000000</span><span class="sxs-lookup"><span data-stu-id="88481-121">0x00000000</span></span>  <br/> |<span data-ttu-id="88481-122">Aucune réponse n’est requise pour cet objet.</span><span class="sxs-lookup"><span data-stu-id="88481-122">No response is required for this object.</span></span> <span data-ttu-id="88481-123">C’est le cas pour les objets de rendez-vous et les objets de réponse de réunion.</span><span class="sxs-lookup"><span data-stu-id="88481-123">This is the case for appointment objects and meeting response objects.</span></span>  <br/> |
|<span data-ttu-id="88481-124">respTentative</span><span class="sxs-lookup"><span data-stu-id="88481-124">respTentative</span></span>  <br/> |<span data-ttu-id="88481-125">0x00000002</span><span class="sxs-lookup"><span data-stu-id="88481-125">0x00000002</span></span>  <br/> |<span data-ttu-id="88481-126">Cette valeur sur l’objet de réunion du participant indique que le participant a provisoirement accepté l’objet de demande de réunion.</span><span class="sxs-lookup"><span data-stu-id="88481-126">This value on the attendee's meeting object indicates that the attendee has tentatively accepted the meeting request object.</span></span>  <br/> |
|<span data-ttu-id="88481-127">respAccepted</span><span class="sxs-lookup"><span data-stu-id="88481-127">respAccepted</span></span>  <br/> |<span data-ttu-id="88481-128">0x00000003</span><span class="sxs-lookup"><span data-stu-id="88481-128">0x00000003</span></span>  <br/> |<span data-ttu-id="88481-129">Cette valeur sur l’objet de réunion du participant indique que le participant a accepté l’objet de demande de réunion.</span><span class="sxs-lookup"><span data-stu-id="88481-129">This value on the attendee's meeting object indicates that the attendee has accepted the meeting request object.</span></span>  <br/> |
|<span data-ttu-id="88481-130">respDeclined</span><span class="sxs-lookup"><span data-stu-id="88481-130">respDeclined</span></span>  <br/> |<span data-ttu-id="88481-131">0x00000004</span><span class="sxs-lookup"><span data-stu-id="88481-131">0x00000004</span></span>  <br/> |<span data-ttu-id="88481-132">Cette valeur sur l’objet de réunion du participant indique que le participant a refusé l’objet de demande de réunion.</span><span class="sxs-lookup"><span data-stu-id="88481-132">This value on the attendee's meeting object indicates that the attendee has declined the meeting request object.</span></span>  <br/> |
   
## <a name="related-resources"></a><span data-ttu-id="88481-133">Ressources connexes</span><span class="sxs-lookup"><span data-stu-id="88481-133">Related resources</span></span>

### <a name="protocol-specifications"></a><span data-ttu-id="88481-134">Spécifications de protocole</span><span class="sxs-lookup"><span data-stu-id="88481-134">Protocol specifications</span></span>

<span data-ttu-id="88481-135">[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="88481-135">[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="88481-136">Fournit des références aux spécifications Exchange Server protocole.</span><span class="sxs-lookup"><span data-stu-id="88481-136">Provides references to related Exchange Server protocol specifications.</span></span>
    
<span data-ttu-id="88481-137">[[MS-OXOCAL]](https://msdn.microsoft.com/library/09861fde-c8e4-4028-9346-e7c214cfdba1%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="88481-137">[[MS-OXOCAL]](https://msdn.microsoft.com/library/09861fde-c8e4-4028-9346-e7c214cfdba1%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="88481-138">Spécifie les propriétés et les opérations pour les messages de rendez-vous, de demande de réunion et de réponse.</span><span class="sxs-lookup"><span data-stu-id="88481-138">Specifies the properties and operations for appointment, meeting request, and response messages.</span></span>
    
<span data-ttu-id="88481-139">[[MS-OXCMSG]](https://msdn.microsoft.com/library/7fd7ec40-deec-4c06-9493-1bc06b349682%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="88481-139">[[MS-OXCMSG]](https://msdn.microsoft.com/library/7fd7ec40-deec-4c06-9493-1bc06b349682%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="88481-140">Gère les objets message et pièce jointe.</span><span class="sxs-lookup"><span data-stu-id="88481-140">Handles message and attachment objects.</span></span>
    
### <a name="header-files"></a><span data-ttu-id="88481-141">Fichiers d’en-tête</span><span class="sxs-lookup"><span data-stu-id="88481-141">Header files</span></span>

<span data-ttu-id="88481-142">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="88481-142">Mapidefs.h</span></span>
  
> <span data-ttu-id="88481-143">Fournit des définitions de type de données.</span><span class="sxs-lookup"><span data-stu-id="88481-143">Provides data type definitions.</span></span>
    
<span data-ttu-id="88481-144">Mapitags.h</span><span class="sxs-lookup"><span data-stu-id="88481-144">Mapitags.h</span></span>
  
> <span data-ttu-id="88481-145">Contient les définitions des propriétés répertoriées en tant que noms de remplacement.</span><span class="sxs-lookup"><span data-stu-id="88481-145">Contains definitions of properties listed as alternate names.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="88481-146">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="88481-146">See also</span></span>



[<span data-ttu-id="88481-147">Propriétés MAPI</span><span class="sxs-lookup"><span data-stu-id="88481-147">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="88481-148">Propriétés canoniques MAPI</span><span class="sxs-lookup"><span data-stu-id="88481-148">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="88481-149">Mappage des noms de propriétés canoniques aux noms MAPI</span><span class="sxs-lookup"><span data-stu-id="88481-149">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="88481-150">Mappage des noms MAPI aux noms de propriétés canoniques</span><span class="sxs-lookup"><span data-stu-id="88481-150">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

