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
description: Dernière modification le 09 mars 2015
ms.openlocfilehash: 0e84f1361e9ca3d95b4297c01801e649a9f86ced
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/23/2018
ms.locfileid: "22569231"
---
# <a name="pidtagrecipientflags-canonical-property"></a><span data-ttu-id="4cda6-103">Propriété canonique PidTagRecipientFlags</span><span class="sxs-lookup"><span data-stu-id="4cda6-103">PidTagRecipientFlags Canonical Property</span></span>

  
  
<span data-ttu-id="4cda6-104">**S’applique à**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="4cda6-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="4cda6-105">Spécifie un champ de bits qui décrit l’état du destinataire.</span><span class="sxs-lookup"><span data-stu-id="4cda6-105">Specifies a bit field that describes the recipient status.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="4cda6-106">Propriétés associées :</span><span class="sxs-lookup"><span data-stu-id="4cda6-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="4cda6-107">PR_RECIPIENT_FLAGS</span><span class="sxs-lookup"><span data-stu-id="4cda6-107">PR_RECIPIENT_FLAGS</span></span>  <br/> |
|<span data-ttu-id="4cda6-108">Identificateur :</span><span class="sxs-lookup"><span data-stu-id="4cda6-108">Identifier:</span></span>  <br/> |<span data-ttu-id="4cda6-109">0x5FFD</span><span class="sxs-lookup"><span data-stu-id="4cda6-109">0x5FFD</span></span>  <br/> |
|<span data-ttu-id="4cda6-110">Type de données :</span><span class="sxs-lookup"><span data-stu-id="4cda6-110">Data type:</span></span>  <br/> |<span data-ttu-id="4cda6-111">PT_LONG</span><span class="sxs-lookup"><span data-stu-id="4cda6-111">PT_LONG</span></span>  <br/> |
|<span data-ttu-id="4cda6-112">Domaine :</span><span class="sxs-lookup"><span data-stu-id="4cda6-112">Area:</span></span>  <br/> |<span data-ttu-id="4cda6-113">Destinataire de transport</span><span class="sxs-lookup"><span data-stu-id="4cda6-113">Transport recipient</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="4cda6-114">Remarques</span><span class="sxs-lookup"><span data-stu-id="4cda6-114">Remarks</span></span>

<span data-ttu-id="4cda6-115">Cette propriété n’est pas requise.</span><span class="sxs-lookup"><span data-stu-id="4cda6-115">This property is not required.</span></span> <span data-ttu-id="4cda6-116">Voici les indicateurs individuels qui peuvent être définies.</span><span class="sxs-lookup"><span data-stu-id="4cda6-116">The following are the individual flags that can be set.</span></span>
  
|<span data-ttu-id="4cda6-117">**Valeur**</span><span class="sxs-lookup"><span data-stu-id="4cda6-117">**Value**</span></span>|<span data-ttu-id="4cda6-118">**Description**</span><span class="sxs-lookup"><span data-stu-id="4cda6-118">**Description**</span></span>|
|:-----|:-----|
|<span data-ttu-id="4cda6-119">S (recipSendable, 0 x 00000001)</span><span class="sxs-lookup"><span data-stu-id="4cda6-119">S (recipSendable, 0x00000001)</span></span>  <br/> |<span data-ttu-id="4cda6-120">Le destinataire est un participant **Sendable** .</span><span class="sxs-lookup"><span data-stu-id="4cda6-120">The recipient is a **Sendable** Attendee.</span></span> <span data-ttu-id="4cda6-121">Cet indicateur est utilisé uniquement dans la propriété **dispidApptUnsendableRecips** ([PidLidAppointmentUnsendableRecipients](pidlidappointmentunsendablerecipients-canonical-property.md)).</span><span class="sxs-lookup"><span data-stu-id="4cda6-121">This flag is only used in the **dispidApptUnsendableRecips** ([PidLidAppointmentUnsendableRecipients](pidlidappointmentunsendablerecipients-canonical-property.md)) property.</span></span>  <br/> |
|<span data-ttu-id="4cda6-122">O (recipOrganizer, 0x0000002)</span><span class="sxs-lookup"><span data-stu-id="4cda6-122">O (recipOrganizer, 0x0000002)</span></span>  <br/> |<span data-ttu-id="4cda6-123">Le **RecipientRow** sur lequel il est défini représente l’organisateur de la réunion.</span><span class="sxs-lookup"><span data-stu-id="4cda6-123">The **RecipientRow** on which this flag is set represents the meeting Organizer.</span></span>  <br/> |
|<span data-ttu-id="4cda6-124">Restauration d’urgence (recipExceptionalResponse, 0 x 00000010)</span><span class="sxs-lookup"><span data-stu-id="4cda6-124">ER (recipExceptionalResponse, 0x00000010)</span></span>  <br/> |<span data-ttu-id="4cda6-125">Indique que le participant a donné une réponse de l’exception sur lequel réside cette **RecipientRow** .</span><span class="sxs-lookup"><span data-stu-id="4cda6-125">Indicates that the attendee gave a response for the exception on which this **RecipientRow** resides.</span></span> <span data-ttu-id="4cda6-126">Cet indicateur est utilisé uniquement dans un **RecipientRow** d’un objet de messages incorporés d’exception de l’objet de réunion de l’organisateur.</span><span class="sxs-lookup"><span data-stu-id="4cda6-126">This flag is only used in a **RecipientRow** of an exception embedded message object of the organizer's meeting object.</span></span>  <br/> |
|<span data-ttu-id="4cda6-127">ED (recipExceptionalDeleted, 0 x 00000020)</span><span class="sxs-lookup"><span data-stu-id="4cda6-127">ED (recipExceptionalDeleted, 0x00000020)</span></span>  <br/> |<span data-ttu-id="4cda6-128">Indique que bien que l' **RecipientRow** existe, il doit être traitée comme si le destinataire n’a pas.</span><span class="sxs-lookup"><span data-stu-id="4cda6-128">Indicates that although the **RecipientRow** exists, it should be treated as if the corresponding recipient does not.</span></span> <span data-ttu-id="4cda6-129">Cet indicateur est utilisé uniquement dans un **RecipientRow** d’un objet de messages incorporés d’exception de l’objet de réunion de l’organisateur.</span><span class="sxs-lookup"><span data-stu-id="4cda6-129">This flag is only used in a **RecipientRow** of an exception embedded message object of the organizer's meeting object.</span></span>  <br/> |
|<span data-ttu-id="4cda6-130">X (0 x 00000040 réservés,)</span><span class="sxs-lookup"><span data-stu-id="4cda6-130">X (reserved, 0x00000040)</span></span>  <br/> |<span data-ttu-id="4cda6-131">Ne doit pas être définie.</span><span class="sxs-lookup"><span data-stu-id="4cda6-131">Must not be set.</span></span>  <br/> |
|<span data-ttu-id="4cda6-132">X (0x00000080 réservés,)</span><span class="sxs-lookup"><span data-stu-id="4cda6-132">X (reserved, 0x00000080)</span></span>  <br/> |<span data-ttu-id="4cda6-133">Ne doit pas être définie.</span><span class="sxs-lookup"><span data-stu-id="4cda6-133">Must not be set.</span></span>  <br/> |
|<span data-ttu-id="4cda6-134">G (recipOriginal, 0 x 00000100)</span><span class="sxs-lookup"><span data-stu-id="4cda6-134">G (recipOriginal, 0x00000100)</span></span>  <br/> |<span data-ttu-id="4cda6-135">Indique que le destinataire est un participant d’origine.</span><span class="sxs-lookup"><span data-stu-id="4cda6-135">Indicates the recipient is an original attendee.</span></span> <span data-ttu-id="4cda6-136">Cet indicateur est utilisé uniquement dans la propriété **dispidApptUnsendableRecips** .</span><span class="sxs-lookup"><span data-stu-id="4cda6-136">This flag is only used in the **dispidApptUnsendableRecips** property.</span></span>  <br/> |
|<span data-ttu-id="4cda6-137">X (0 x 00000200 réservés,)</span><span class="sxs-lookup"><span data-stu-id="4cda6-137">X (reserved, 0x00000200)</span></span>  <br/> |<span data-ttu-id="4cda6-138">Réservé.</span><span class="sxs-lookup"><span data-stu-id="4cda6-138">Reserved.</span></span>  <br/> |
   
## <a name="related-resources"></a><span data-ttu-id="4cda6-139">Ressources connexes</span><span class="sxs-lookup"><span data-stu-id="4cda6-139">Related resources</span></span>

### <a name="protocol-specifications"></a><span data-ttu-id="4cda6-140">Spécifications du protocole</span><span class="sxs-lookup"><span data-stu-id="4cda6-140">Protocol specifications</span></span>

<span data-ttu-id="4cda6-141">[[MS-OXPROPS]](http://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="4cda6-141">[[MS-OXPROPS]](http://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="4cda6-142">Fournit des références aux spécifications du protocole Exchange Server associées.</span><span class="sxs-lookup"><span data-stu-id="4cda6-142">Provides references to related Exchange Server protocol specifications.</span></span>
    
<span data-ttu-id="4cda6-143">[[MS-OXOCAL]](http://msdn.microsoft.com/library/09861fde-c8e4-4028-9346-e7c214cfdba1%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="4cda6-143">[[MS-OXOCAL]](http://msdn.microsoft.com/library/09861fde-c8e4-4028-9346-e7c214cfdba1%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="4cda6-144">Spécifie les propriétés et opérations pour un rendez-vous, une demande de réunion et les messages de réponse.</span><span class="sxs-lookup"><span data-stu-id="4cda6-144">Specifies the properties and operations for appointment, meeting request, and response messages.</span></span>
    
### <a name="header-files"></a><span data-ttu-id="4cda6-145">Fichiers d’en-tête</span><span class="sxs-lookup"><span data-stu-id="4cda6-145">Header files</span></span>

<span data-ttu-id="4cda6-146">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="4cda6-146">Mapidefs.h</span></span>
  
> <span data-ttu-id="4cda6-147">Fournit des définitions de type de données.</span><span class="sxs-lookup"><span data-stu-id="4cda6-147">Provides data type definitions.</span></span>
    
<span data-ttu-id="4cda6-148">MAPITAGS.h</span><span class="sxs-lookup"><span data-stu-id="4cda6-148">Mapitags.h</span></span>
  
> <span data-ttu-id="4cda6-149">Contient les définitions des propriétés répertoriées en tant que d’autres noms.</span><span class="sxs-lookup"><span data-stu-id="4cda6-149">Contains definitions of properties listed as alternate names.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="4cda6-150">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="4cda6-150">See also</span></span>



[<span data-ttu-id="4cda6-151">Propriétés MAPI</span><span class="sxs-lookup"><span data-stu-id="4cda6-151">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="4cda6-152">Propriétés canoniques MAPI</span><span class="sxs-lookup"><span data-stu-id="4cda6-152">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="4cda6-153">Mappage des noms de propriétés canoniques aux noms MAPI</span><span class="sxs-lookup"><span data-stu-id="4cda6-153">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="4cda6-154">Mappage des noms MAPI aux noms de propriétés canoniques</span><span class="sxs-lookup"><span data-stu-id="4cda6-154">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

