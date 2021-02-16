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
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32356699"
---
# <a name="pidtagrecipientflags-canonical-property"></a><span data-ttu-id="7c68b-103">Propriété canonique PidTagRecipientFlags</span><span class="sxs-lookup"><span data-stu-id="7c68b-103">PidTagRecipientFlags Canonical Property</span></span>

  
  
<span data-ttu-id="7c68b-104">**S’applique à** : Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="7c68b-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="7c68b-105">Spécifie un champ de bits qui décrit l’état du destinataire.</span><span class="sxs-lookup"><span data-stu-id="7c68b-105">Specifies a bit field that describes the recipient status.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="7c68b-106">Propriétés associées :</span><span class="sxs-lookup"><span data-stu-id="7c68b-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="7c68b-107">PR_RECIPIENT_FLAGS</span><span class="sxs-lookup"><span data-stu-id="7c68b-107">PR_RECIPIENT_FLAGS</span></span>  <br/> |
|<span data-ttu-id="7c68b-108">Identificateur :</span><span class="sxs-lookup"><span data-stu-id="7c68b-108">Identifier:</span></span>  <br/> |<span data-ttu-id="7c68b-109">0x5FFD</span><span class="sxs-lookup"><span data-stu-id="7c68b-109">0x5FFD</span></span>  <br/> |
|<span data-ttu-id="7c68b-110">Type de données :</span><span class="sxs-lookup"><span data-stu-id="7c68b-110">Data type:</span></span>  <br/> |<span data-ttu-id="7c68b-111">PT_LONG</span><span class="sxs-lookup"><span data-stu-id="7c68b-111">PT_LONG</span></span>  <br/> |
|<span data-ttu-id="7c68b-112">Domaine :</span><span class="sxs-lookup"><span data-stu-id="7c68b-112">Area:</span></span>  <br/> |<span data-ttu-id="7c68b-113">Destinataire de transport</span><span class="sxs-lookup"><span data-stu-id="7c68b-113">Transport recipient</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="7c68b-114">Remarques</span><span class="sxs-lookup"><span data-stu-id="7c68b-114">Remarks</span></span>

<span data-ttu-id="7c68b-115">Cette propriété n’est pas obligatoire.</span><span class="sxs-lookup"><span data-stu-id="7c68b-115">This property is not required.</span></span> <span data-ttu-id="7c68b-116">Voici les indicateurs individuels qui peuvent être définies.</span><span class="sxs-lookup"><span data-stu-id="7c68b-116">The following are the individual flags that can be set.</span></span>
  
|<span data-ttu-id="7c68b-117">**Valeur**</span><span class="sxs-lookup"><span data-stu-id="7c68b-117">**Value**</span></span>|<span data-ttu-id="7c68b-118">**Description**</span><span class="sxs-lookup"><span data-stu-id="7c68b-118">**Description**</span></span>|
|:-----|:-----|
|<span data-ttu-id="7c68b-119">S (recipSendable, 0x00000001)</span><span class="sxs-lookup"><span data-stu-id="7c68b-119">S (recipSendable, 0x00000001)</span></span>  <br/> |<span data-ttu-id="7c68b-120">Le destinataire est un **participant à l’envoi.**</span><span class="sxs-lookup"><span data-stu-id="7c68b-120">The recipient is a **Sendable** Attendee.</span></span> <span data-ttu-id="7c68b-121">Cet indicateur est utilisé uniquement dans la propriété **dispidApptUnsendableRecips** ([PidLidAppointmentUnsendableRecipients](pidlidappointmentunsendablerecipients-canonical-property.md)).</span><span class="sxs-lookup"><span data-stu-id="7c68b-121">This flag is only used in the **dispidApptUnsendableRecips** ([PidLidAppointmentUnsendableRecipients](pidlidappointmentunsendablerecipients-canonical-property.md)) property.</span></span>  <br/> |
|<span data-ttu-id="7c68b-122">O (recipOrganizer, 0x0000002)</span><span class="sxs-lookup"><span data-stu-id="7c68b-122">O (recipOrganizer, 0x0000002)</span></span>  <br/> |<span data-ttu-id="7c68b-123">Le **RecipientRow** sur lequel cet indicateur est définie représente l’organisateur de la réunion.</span><span class="sxs-lookup"><span data-stu-id="7c68b-123">The **RecipientRow** on which this flag is set represents the meeting Organizer.</span></span>  <br/> |
|<span data-ttu-id="7c68b-124">ER (recipExceptionalResponse, 0x00000010)</span><span class="sxs-lookup"><span data-stu-id="7c68b-124">ER (recipExceptionalResponse, 0x00000010)</span></span>  <br/> |<span data-ttu-id="7c68b-125">Indique que le participant a donné une réponse pour l’exception sur laquelle réside **ce RecipientRow.**</span><span class="sxs-lookup"><span data-stu-id="7c68b-125">Indicates that the attendee gave a response for the exception on which this **RecipientRow** resides.</span></span> <span data-ttu-id="7c68b-126">Cet indicateur est utilisé uniquement dans **un RecipientRow** d’un objet message incorporé d’exception de l’objet de réunion de l’organisateur.</span><span class="sxs-lookup"><span data-stu-id="7c68b-126">This flag is only used in a **RecipientRow** of an exception embedded message object of the organizer's meeting object.</span></span>  <br/> |
|<span data-ttu-id="7c68b-127">ED (recipExceptionalDeleted, 0x00000020)</span><span class="sxs-lookup"><span data-stu-id="7c68b-127">ED (recipExceptionalDeleted, 0x00000020)</span></span>  <br/> |<span data-ttu-id="7c68b-128">Indique que bien que **recipientRow** existe, il doit être traité comme si le destinataire correspondant ne le fait pas.</span><span class="sxs-lookup"><span data-stu-id="7c68b-128">Indicates that although the **RecipientRow** exists, it should be treated as if the corresponding recipient does not.</span></span> <span data-ttu-id="7c68b-129">Cet indicateur est utilisé uniquement dans **un RecipientRow** d’un objet message incorporé d’exception de l’objet de réunion de l’organisateur.</span><span class="sxs-lookup"><span data-stu-id="7c68b-129">This flag is only used in a **RecipientRow** of an exception embedded message object of the organizer's meeting object.</span></span>  <br/> |
|<span data-ttu-id="7c68b-130">X (réservé, 0x00000040)</span><span class="sxs-lookup"><span data-stu-id="7c68b-130">X (reserved, 0x00000040)</span></span>  <br/> |<span data-ttu-id="7c68b-131">Ne doit pas être définie.</span><span class="sxs-lookup"><span data-stu-id="7c68b-131">Must not be set.</span></span>  <br/> |
|<span data-ttu-id="7c68b-132">X (réservé, 0x00000080)</span><span class="sxs-lookup"><span data-stu-id="7c68b-132">X (reserved, 0x00000080)</span></span>  <br/> |<span data-ttu-id="7c68b-133">Ne doit pas être définie.</span><span class="sxs-lookup"><span data-stu-id="7c68b-133">Must not be set.</span></span>  <br/> |
|<span data-ttu-id="7c68b-134">G (recipOriginal, 0x00000100)</span><span class="sxs-lookup"><span data-stu-id="7c68b-134">G (recipOriginal, 0x00000100)</span></span>  <br/> |<span data-ttu-id="7c68b-135">Indique que le destinataire est un participant d’origine.</span><span class="sxs-lookup"><span data-stu-id="7c68b-135">Indicates the recipient is an original attendee.</span></span> <span data-ttu-id="7c68b-136">Cet indicateur est utilisé uniquement dans la **propriété dispidApptUnsendableRecips.**</span><span class="sxs-lookup"><span data-stu-id="7c68b-136">This flag is only used in the **dispidApptUnsendableRecips** property.</span></span>  <br/> |
|<span data-ttu-id="7c68b-137">X (réservé, 0x00000200)</span><span class="sxs-lookup"><span data-stu-id="7c68b-137">X (reserved, 0x00000200)</span></span>  <br/> |<span data-ttu-id="7c68b-138">Réservé.</span><span class="sxs-lookup"><span data-stu-id="7c68b-138">Reserved.</span></span>  <br/> |
   
## <a name="related-resources"></a><span data-ttu-id="7c68b-139">Ressources connexes</span><span class="sxs-lookup"><span data-stu-id="7c68b-139">Related resources</span></span>

### <a name="protocol-specifications"></a><span data-ttu-id="7c68b-140">Spécifications de protocole</span><span class="sxs-lookup"><span data-stu-id="7c68b-140">Protocol specifications</span></span>

<span data-ttu-id="7c68b-141">[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="7c68b-141">[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="7c68b-142">Fournit des références aux spécifications Exchange Server de protocole associées.</span><span class="sxs-lookup"><span data-stu-id="7c68b-142">Provides references to related Exchange Server protocol specifications.</span></span>
    
<span data-ttu-id="7c68b-143">[[MS-OXOCAL]](https://msdn.microsoft.com/library/09861fde-c8e4-4028-9346-e7c214cfdba1%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="7c68b-143">[[MS-OXOCAL]](https://msdn.microsoft.com/library/09861fde-c8e4-4028-9346-e7c214cfdba1%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="7c68b-144">Spécifie les propriétés et les opérations pour les messages de rendez-vous, de demande de réunion et de réponse.</span><span class="sxs-lookup"><span data-stu-id="7c68b-144">Specifies the properties and operations for appointment, meeting request, and response messages.</span></span>
    
### <a name="header-files"></a><span data-ttu-id="7c68b-145">Fichiers d’en-tête</span><span class="sxs-lookup"><span data-stu-id="7c68b-145">Header files</span></span>

<span data-ttu-id="7c68b-146">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="7c68b-146">Mapidefs.h</span></span>
  
> <span data-ttu-id="7c68b-147">Fournit des définitions de type de données.</span><span class="sxs-lookup"><span data-stu-id="7c68b-147">Provides data type definitions.</span></span>
    
<span data-ttu-id="7c68b-148">Mapitags.h</span><span class="sxs-lookup"><span data-stu-id="7c68b-148">Mapitags.h</span></span>
  
> <span data-ttu-id="7c68b-149">Contient les définitions des propriétés répertoriées en tant que noms de remplacement.</span><span class="sxs-lookup"><span data-stu-id="7c68b-149">Contains definitions of properties listed as alternate names.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="7c68b-150">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="7c68b-150">See also</span></span>



[<span data-ttu-id="7c68b-151">Propriétés MAPI</span><span class="sxs-lookup"><span data-stu-id="7c68b-151">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="7c68b-152">Propriétés canoniques MAPI</span><span class="sxs-lookup"><span data-stu-id="7c68b-152">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="7c68b-153">Mappage des noms de propriétés canoniques aux noms MAPI</span><span class="sxs-lookup"><span data-stu-id="7c68b-153">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="7c68b-154">Mappage des noms MAPI aux noms de propriétés canoniques</span><span class="sxs-lookup"><span data-stu-id="7c68b-154">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

