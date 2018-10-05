---
title: Propriété canonique PidTagRecipientFlags
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- MAPI.PidTagRecipientFlags
api_type:
- COM
ms.assetid: 9fbe537f-b5fe-48a2-803c-653c50c82efd
description: Dernière modification le 9 mars 2015
ms.openlocfilehash: 7b791d75c2a76ea1a504c0d8862dd20f5365b475
ms.sourcegitcommit: ef717c65d8dd41ababffb01eafc443c79950aed4
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 10/04/2018
ms.locfileid: "25394040"
---
# <a name="pidtagrecipientflags-canonical-property"></a><span data-ttu-id="f9200-103">Propriété canonique PidTagRecipientFlags</span><span class="sxs-lookup"><span data-stu-id="f9200-103">PidTagRecipientFlags Canonical Property</span></span>

  
  
<span data-ttu-id="f9200-104">**S’applique à** : Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="f9200-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="f9200-105">Spécifie un champ de bits qui décrit l’état du destinataire.</span><span class="sxs-lookup"><span data-stu-id="f9200-105">Specifies a bit field that describes the recipient status.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="f9200-106">Propriétés associées :</span><span class="sxs-lookup"><span data-stu-id="f9200-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="f9200-107">PR_RECIPIENT_FLAGS</span><span class="sxs-lookup"><span data-stu-id="f9200-107">PR_RECIPIENT_FLAGS</span></span>  <br/> |
|<span data-ttu-id="f9200-108">Identificateur :</span><span class="sxs-lookup"><span data-stu-id="f9200-108">Identifier:</span></span>  <br/> |<span data-ttu-id="f9200-109">0x5FFD</span><span class="sxs-lookup"><span data-stu-id="f9200-109">0x5FFD</span></span>  <br/> |
|<span data-ttu-id="f9200-110">Type de données :</span><span class="sxs-lookup"><span data-stu-id="f9200-110">Data type:</span></span>  <br/> |<span data-ttu-id="f9200-111">PT_LONG</span><span class="sxs-lookup"><span data-stu-id="f9200-111">PT_LONG</span></span>  <br/> |
|<span data-ttu-id="f9200-112">Domaine :</span><span class="sxs-lookup"><span data-stu-id="f9200-112">Area:</span></span>  <br/> |<span data-ttu-id="f9200-113">Destinataire de transport</span><span class="sxs-lookup"><span data-stu-id="f9200-113">Transport recipient</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="f9200-114">Remarques</span><span class="sxs-lookup"><span data-stu-id="f9200-114">Remarks</span></span>

<span data-ttu-id="f9200-115">Cette propriété n’est pas requise.</span><span class="sxs-lookup"><span data-stu-id="f9200-115">This property is not required.</span></span> <span data-ttu-id="f9200-116">Voici les indicateurs individuels qui peuvent être définies.</span><span class="sxs-lookup"><span data-stu-id="f9200-116">The following are the individual flags that can be set.</span></span>
  
|<span data-ttu-id="f9200-117">**Valeur**</span><span class="sxs-lookup"><span data-stu-id="f9200-117">**Value**</span></span>|<span data-ttu-id="f9200-118">**Description**</span><span class="sxs-lookup"><span data-stu-id="f9200-118">**Description**</span></span>|
|:-----|:-----|
|<span data-ttu-id="f9200-119">S (recipSendable, 0 x 00000001)</span><span class="sxs-lookup"><span data-stu-id="f9200-119">S (recipSendable, 0x00000001)</span></span>  <br/> |<span data-ttu-id="f9200-120">Le destinataire est un participant **Sendable** .</span><span class="sxs-lookup"><span data-stu-id="f9200-120">The recipient is a **Sendable** Attendee.</span></span> <span data-ttu-id="f9200-121">Cet indicateur est utilisé uniquement dans la propriété **dispidApptUnsendableRecips** ([PidLidAppointmentUnsendableRecipients](pidlidappointmentunsendablerecipients-canonical-property.md)).</span><span class="sxs-lookup"><span data-stu-id="f9200-121">This flag is only used in the **dispidApptUnsendableRecips** ([PidLidAppointmentUnsendableRecipients](pidlidappointmentunsendablerecipients-canonical-property.md)) property.</span></span>  <br/> |
|<span data-ttu-id="f9200-122">O (recipOrganizer, 0x0000002)</span><span class="sxs-lookup"><span data-stu-id="f9200-122">O (recipOrganizer, 0x0000002)</span></span>  <br/> |<span data-ttu-id="f9200-123">Le **RecipientRow** sur lequel il est défini représente l’organisateur de la réunion.</span><span class="sxs-lookup"><span data-stu-id="f9200-123">The **RecipientRow** on which this flag is set represents the meeting Organizer.</span></span>  <br/> |
|<span data-ttu-id="f9200-124">Restauration d’urgence (recipExceptionalResponse, 0 x 00000010)</span><span class="sxs-lookup"><span data-stu-id="f9200-124">ER (recipExceptionalResponse, 0x00000010)</span></span>  <br/> |<span data-ttu-id="f9200-125">Indique que le participant a donné une réponse de l’exception sur lequel réside cette **RecipientRow** .</span><span class="sxs-lookup"><span data-stu-id="f9200-125">Indicates that the attendee gave a response for the exception on which this **RecipientRow** resides.</span></span> <span data-ttu-id="f9200-126">Cet indicateur est utilisé uniquement dans un **RecipientRow** d’un objet de messages incorporés d’exception de l’objet de réunion de l’organisateur.</span><span class="sxs-lookup"><span data-stu-id="f9200-126">This flag is only used in a **RecipientRow** of an exception embedded message object of the organizer's meeting object.</span></span>  <br/> |
|<span data-ttu-id="f9200-127">ED (recipExceptionalDeleted, 0 x 00000020)</span><span class="sxs-lookup"><span data-stu-id="f9200-127">ED (recipExceptionalDeleted, 0x00000020)</span></span>  <br/> |<span data-ttu-id="f9200-128">Indique que bien que l' **RecipientRow** existe, il doit être traitée comme si le destinataire n’a pas.</span><span class="sxs-lookup"><span data-stu-id="f9200-128">Indicates that although the **RecipientRow** exists, it should be treated as if the corresponding recipient does not.</span></span> <span data-ttu-id="f9200-129">Cet indicateur est utilisé uniquement dans un **RecipientRow** d’un objet de messages incorporés d’exception de l’objet de réunion de l’organisateur.</span><span class="sxs-lookup"><span data-stu-id="f9200-129">This flag is only used in a **RecipientRow** of an exception embedded message object of the organizer's meeting object.</span></span>  <br/> |
|<span data-ttu-id="f9200-130">X (0 x 00000040 réservés,)</span><span class="sxs-lookup"><span data-stu-id="f9200-130">X (reserved, 0x00000040)</span></span>  <br/> |<span data-ttu-id="f9200-131">Ne doit pas être définie.</span><span class="sxs-lookup"><span data-stu-id="f9200-131">Must not be set.</span></span>  <br/> |
|<span data-ttu-id="f9200-132">X (0x00000080 réservés,)</span><span class="sxs-lookup"><span data-stu-id="f9200-132">X (reserved, 0x00000080)</span></span>  <br/> |<span data-ttu-id="f9200-133">Ne doit pas être définie.</span><span class="sxs-lookup"><span data-stu-id="f9200-133">Must not be set.</span></span>  <br/> |
|<span data-ttu-id="f9200-134">G (recipOriginal, 0 x 00000100)</span><span class="sxs-lookup"><span data-stu-id="f9200-134">G (recipOriginal, 0x00000100)</span></span>  <br/> |<span data-ttu-id="f9200-135">Indique que le destinataire est un participant d’origine.</span><span class="sxs-lookup"><span data-stu-id="f9200-135">Indicates the recipient is an original attendee.</span></span> <span data-ttu-id="f9200-136">Cet indicateur est utilisé uniquement dans la propriété **dispidApptUnsendableRecips** .</span><span class="sxs-lookup"><span data-stu-id="f9200-136">This flag is only used in the **dispidApptUnsendableRecips** property.</span></span>  <br/> |
|<span data-ttu-id="f9200-137">X (0 x 00000200 réservés,)</span><span class="sxs-lookup"><span data-stu-id="f9200-137">X (reserved, 0x00000200)</span></span>  <br/> |<span data-ttu-id="f9200-138">Réservé.</span><span class="sxs-lookup"><span data-stu-id="f9200-138">Reserved.</span></span>  <br/> |
   
## <a name="related-resources"></a><span data-ttu-id="f9200-139">Ressources connexes</span><span class="sxs-lookup"><span data-stu-id="f9200-139">Related resources</span></span>

### <a name="protocol-specifications"></a><span data-ttu-id="f9200-140">Spécifications du protocole</span><span class="sxs-lookup"><span data-stu-id="f9200-140">Protocol specifications</span></span>

<span data-ttu-id="f9200-141">[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="f9200-141">[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="f9200-142">Fournit des références aux spécifications du protocole Exchange Server associées.</span><span class="sxs-lookup"><span data-stu-id="f9200-142">Provides references to related Exchange Server protocol specifications.</span></span>
    
<span data-ttu-id="f9200-143">[[MS-OXOCAL]](https://msdn.microsoft.com/library/09861fde-c8e4-4028-9346-e7c214cfdba1%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="f9200-143">[[MS-OXOCAL]](https://msdn.microsoft.com/library/09861fde-c8e4-4028-9346-e7c214cfdba1%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="f9200-144">Spécifie les propriétés et opérations pour un rendez-vous, une demande de réunion et les messages de réponse.</span><span class="sxs-lookup"><span data-stu-id="f9200-144">Specifies the properties and operations for appointment, meeting request, and response messages.</span></span>
    
### <a name="header-files"></a><span data-ttu-id="f9200-145">Fichiers d’en-tête</span><span class="sxs-lookup"><span data-stu-id="f9200-145">Header files</span></span>

<span data-ttu-id="f9200-146">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="f9200-146">Mapidefs.h</span></span>
  
> <span data-ttu-id="f9200-147">Fournit des définitions de type de données.</span><span class="sxs-lookup"><span data-stu-id="f9200-147">Provides data type definitions.</span></span>
    
<span data-ttu-id="f9200-148">MAPITAGS.h</span><span class="sxs-lookup"><span data-stu-id="f9200-148">Mapitags.h</span></span>
  
> <span data-ttu-id="f9200-149">Contient les définitions des propriétés répertoriées en tant que d’autres noms.</span><span class="sxs-lookup"><span data-stu-id="f9200-149">Contains definitions of properties listed as alternate names.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="f9200-150">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="f9200-150">See also</span></span>



[<span data-ttu-id="f9200-151">Propriétés MAPI</span><span class="sxs-lookup"><span data-stu-id="f9200-151">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="f9200-152">Propriétés canoniques MAPI</span><span class="sxs-lookup"><span data-stu-id="f9200-152">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="f9200-153">Mappage des noms de propriétés canoniques aux noms MAPI</span><span class="sxs-lookup"><span data-stu-id="f9200-153">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="f9200-154">Mappage des noms MAPI aux noms de propriétés canoniques</span><span class="sxs-lookup"><span data-stu-id="f9200-154">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

