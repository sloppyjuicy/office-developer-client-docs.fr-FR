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
description: 'Derni�re modification�: lundi 9 mars 2015'
ms.openlocfilehash: a93e5a44768cd99512189f800bf98ab6e30b575d
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19786517"
---
# <a name="pidtagrecipientflags-canonical-property"></a><span data-ttu-id="7426e-103">Propriété canonique PidTagRecipientFlags</span><span class="sxs-lookup"><span data-stu-id="7426e-103">PidTagRecipientFlags Canonical Property</span></span>

  
  
<span data-ttu-id="7426e-104">**S’applique à**: Outlook</span><span class="sxs-lookup"><span data-stu-id="7426e-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="7426e-105">Spécifie un champ de bits qui décrit l’état du destinataire.</span><span class="sxs-lookup"><span data-stu-id="7426e-105">Specifies a bit field that describes the recipient status.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="7426e-106">Propriétés associées :</span><span class="sxs-lookup"><span data-stu-id="7426e-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="7426e-107">PR_RECIPIENT_FLAGS</span><span class="sxs-lookup"><span data-stu-id="7426e-107">PR_RECIPIENT_FLAGS</span></span>  <br/> |
|<span data-ttu-id="7426e-108">Identificateur :</span><span class="sxs-lookup"><span data-stu-id="7426e-108">Identifier:</span></span>  <br/> |<span data-ttu-id="7426e-109">0x5FFD</span><span class="sxs-lookup"><span data-stu-id="7426e-109">0x5FFD</span></span>  <br/> |
|<span data-ttu-id="7426e-110">Type de données :</span><span class="sxs-lookup"><span data-stu-id="7426e-110">Data type:</span></span>  <br/> |<span data-ttu-id="7426e-111">PT_LONG</span><span class="sxs-lookup"><span data-stu-id="7426e-111">PT_LONG</span></span>  <br/> |
|<span data-ttu-id="7426e-112">Zone :</span><span class="sxs-lookup"><span data-stu-id="7426e-112">Area:</span></span>  <br/> |<span data-ttu-id="7426e-113">Destinataire de transport</span><span class="sxs-lookup"><span data-stu-id="7426e-113">Transport recipient</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="7426e-114">Remarques</span><span class="sxs-lookup"><span data-stu-id="7426e-114">Remarks</span></span>

<span data-ttu-id="7426e-115">Cette propriété n’est pas requise.</span><span class="sxs-lookup"><span data-stu-id="7426e-115">This property is not required.</span></span> <span data-ttu-id="7426e-116">Voici les indicateurs individuels qui peuvent être définies.</span><span class="sxs-lookup"><span data-stu-id="7426e-116">The following are the individual flags that can be set.</span></span>
  
|<span data-ttu-id="7426e-117">**Valeur**</span><span class="sxs-lookup"><span data-stu-id="7426e-117">**Value**</span></span>|<span data-ttu-id="7426e-118">**Description**</span><span class="sxs-lookup"><span data-stu-id="7426e-118">**Description**</span></span>|
|:-----|:-----|
|<span data-ttu-id="7426e-119">S (recipSendable, 0 x 00000001)</span><span class="sxs-lookup"><span data-stu-id="7426e-119">S (recipSendable, 0x00000001)</span></span>  <br/> |<span data-ttu-id="7426e-120">Le destinataire est un participant **Sendable** .</span><span class="sxs-lookup"><span data-stu-id="7426e-120">The recipient is a **Sendable** Attendee.</span></span> <span data-ttu-id="7426e-121">Cet indicateur est utilisé uniquement dans la propriété **dispidApptUnsendableRecips** ([PidLidAppointmentUnsendableRecipients](pidlidappointmentunsendablerecipients-canonical-property.md)).</span><span class="sxs-lookup"><span data-stu-id="7426e-121">This flag is only used in the **dispidApptUnsendableRecips** ([PidLidAppointmentUnsendableRecipients](pidlidappointmentunsendablerecipients-canonical-property.md)) property.</span></span>  <br/> |
|<span data-ttu-id="7426e-122">O (recipOrganizer, 0x0000002)</span><span class="sxs-lookup"><span data-stu-id="7426e-122">O (recipOrganizer, 0x0000002)</span></span>  <br/> |<span data-ttu-id="7426e-123">Le **RecipientRow** sur lequel il est défini représente l’organisateur de la réunion.</span><span class="sxs-lookup"><span data-stu-id="7426e-123">The **RecipientRow** on which this flag is set represents the meeting Organizer.</span></span>  <br/> |
|<span data-ttu-id="7426e-124">Restauration d’urgence (recipExceptionalResponse, 0 x 00000010)</span><span class="sxs-lookup"><span data-stu-id="7426e-124">ER (recipExceptionalResponse, 0x00000010)</span></span>  <br/> |<span data-ttu-id="7426e-125">Indique que le participant a donné une réponse de l’exception sur lequel réside cette **RecipientRow** .</span><span class="sxs-lookup"><span data-stu-id="7426e-125">Indicates that the attendee gave a response for the exception on which this **RecipientRow** resides.</span></span> <span data-ttu-id="7426e-126">Cet indicateur est utilisé uniquement dans un **RecipientRow** d’un objet de messages incorporés d’exception de l’objet de réunion de l’organisateur.</span><span class="sxs-lookup"><span data-stu-id="7426e-126">This flag is only used in a **RecipientRow** of an exception embedded message object of the organizer's meeting object.</span></span>  <br/> |
|<span data-ttu-id="7426e-127">ED (recipExceptionalDeleted, 0 x 00000020)</span><span class="sxs-lookup"><span data-stu-id="7426e-127">ED (recipExceptionalDeleted, 0x00000020)</span></span>  <br/> |<span data-ttu-id="7426e-128">Indique que bien que l' **RecipientRow** existe, il doit être traitée comme si le destinataire n’a pas.</span><span class="sxs-lookup"><span data-stu-id="7426e-128">Indicates that although the **RecipientRow** exists, it should be treated as if the corresponding recipient does not.</span></span> <span data-ttu-id="7426e-129">Cet indicateur est utilisé uniquement dans un **RecipientRow** d’un objet de messages incorporés d’exception de l’objet de réunion de l’organisateur.</span><span class="sxs-lookup"><span data-stu-id="7426e-129">This flag is only used in a **RecipientRow** of an exception embedded message object of the organizer's meeting object.</span></span>  <br/> |
|<span data-ttu-id="7426e-130">X (0 x 00000040 réservés,)</span><span class="sxs-lookup"><span data-stu-id="7426e-130">X (reserved, 0x00000040)</span></span>  <br/> |<span data-ttu-id="7426e-131">Ne doit pas être définie.</span><span class="sxs-lookup"><span data-stu-id="7426e-131">Must not be set.</span></span>  <br/> |
|<span data-ttu-id="7426e-132">X (0x00000080 réservés,)</span><span class="sxs-lookup"><span data-stu-id="7426e-132">X (reserved, 0x00000080)</span></span>  <br/> |<span data-ttu-id="7426e-133">Ne doit pas être définie.</span><span class="sxs-lookup"><span data-stu-id="7426e-133">Must not be set.</span></span>  <br/> |
|<span data-ttu-id="7426e-134">G (recipOriginal, 0 x 00000100)</span><span class="sxs-lookup"><span data-stu-id="7426e-134">G (recipOriginal, 0x00000100)</span></span>  <br/> |<span data-ttu-id="7426e-135">Indique que le destinataire est un participant d’origine.</span><span class="sxs-lookup"><span data-stu-id="7426e-135">Indicates the recipient is an original attendee.</span></span> <span data-ttu-id="7426e-136">Cet indicateur est utilisé uniquement dans la propriété **dispidApptUnsendableRecips** .</span><span class="sxs-lookup"><span data-stu-id="7426e-136">This flag is only used in the **dispidApptUnsendableRecips** property.</span></span>  <br/> |
|<span data-ttu-id="7426e-137">X (0 x 00000200 réservés,)</span><span class="sxs-lookup"><span data-stu-id="7426e-137">X (reserved, 0x00000200)</span></span>  <br/> |<span data-ttu-id="7426e-138">Réservé.</span><span class="sxs-lookup"><span data-stu-id="7426e-138">Reserved.</span></span>  <br/> |
   
## <a name="related-resources"></a><span data-ttu-id="7426e-139">Ressources connexes</span><span class="sxs-lookup"><span data-stu-id="7426e-139">Related resources</span></span>

### <a name="protocol-specifications"></a><span data-ttu-id="7426e-140">Spécifications du protocole</span><span class="sxs-lookup"><span data-stu-id="7426e-140">Protocol specifications</span></span>

<span data-ttu-id="7426e-141">[[MS-OXPROPS]](http://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="7426e-141">[[MS-OXPROPS]](http://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="7426e-142">Fournit des références aux spécifications du protocole Exchange Server associées.</span><span class="sxs-lookup"><span data-stu-id="7426e-142">Provides references to related Exchange Server protocol specifications.</span></span>
    
<span data-ttu-id="7426e-143">[[MS-OXOCAL]](http://msdn.microsoft.com/library/09861fde-c8e4-4028-9346-e7c214cfdba1%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="7426e-143">[[MS-OXOCAL]](http://msdn.microsoft.com/library/09861fde-c8e4-4028-9346-e7c214cfdba1%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="7426e-144">Spécifie les propriétés et opérations pour un rendez-vous, une demande de réunion et les messages de réponse.</span><span class="sxs-lookup"><span data-stu-id="7426e-144">Specifies the properties and operations for appointment, meeting request, and response messages.</span></span>
    
### <a name="header-files"></a><span data-ttu-id="7426e-145">Fichiers d’en-tête</span><span class="sxs-lookup"><span data-stu-id="7426e-145">Header files</span></span>

<span data-ttu-id="7426e-146">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="7426e-146">Mapidefs.h</span></span>
  
> <span data-ttu-id="7426e-147">Fournit des définitions de type de données.</span><span class="sxs-lookup"><span data-stu-id="7426e-147">Provides data type definitions.</span></span>
    
<span data-ttu-id="7426e-148">MAPITAGS.h</span><span class="sxs-lookup"><span data-stu-id="7426e-148">Mapitags.h</span></span>
  
> <span data-ttu-id="7426e-149">Contient les définitions des propriétés répertoriées en tant que d’autres noms.</span><span class="sxs-lookup"><span data-stu-id="7426e-149">Contains definitions of properties listed as alternate names.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="7426e-150">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="7426e-150">See also</span></span>



[<span data-ttu-id="7426e-151">Propriétés MAPI</span><span class="sxs-lookup"><span data-stu-id="7426e-151">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="7426e-152">Propriétés canoniques MAPI</span><span class="sxs-lookup"><span data-stu-id="7426e-152">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="7426e-153">Mappage de noms de propriété canonique aux noms MAPI</span><span class="sxs-lookup"><span data-stu-id="7426e-153">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="7426e-154">Mappage de noms MAPI pour les noms de propriété canonique</span><span class="sxs-lookup"><span data-stu-id="7426e-154">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

