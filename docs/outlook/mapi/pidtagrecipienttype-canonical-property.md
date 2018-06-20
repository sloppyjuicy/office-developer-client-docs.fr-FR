---
title: Propriété canonique PidTagRecipientType
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- MAPI.PidTagRecipientType
api_type:
- COM
ms.assetid: 67e31027-6bc2-4a40-9b00-d61baef4ab0f
description: 'Derni�re modification�: lundi 9 mars 2015'
ms.openlocfilehash: 0218ff558e9dfca2f73bbad2dc42cdb7bd7121fc
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19786563"
---
# <a name="pidtagrecipienttype-canonical-property"></a><span data-ttu-id="90be2-103">Propriété canonique PidTagRecipientType</span><span class="sxs-lookup"><span data-stu-id="90be2-103">PidTagRecipientType Canonical Property</span></span>

  
  
<span data-ttu-id="90be2-104">**S’applique à**: Outlook</span><span class="sxs-lookup"><span data-stu-id="90be2-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="90be2-105">Contient le type de destinataire pour un destinataire du message.</span><span class="sxs-lookup"><span data-stu-id="90be2-105">Contains the recipient type for a message recipient.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="90be2-106">Propriétés associées :</span><span class="sxs-lookup"><span data-stu-id="90be2-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="90be2-107">PR_RECIPIENT_TYPE</span><span class="sxs-lookup"><span data-stu-id="90be2-107">PR_RECIPIENT_TYPE</span></span>  <br/> |
|<span data-ttu-id="90be2-108">Identificateur :</span><span class="sxs-lookup"><span data-stu-id="90be2-108">Identifier:</span></span>  <br/> |<span data-ttu-id="90be2-109">0x0C15</span><span class="sxs-lookup"><span data-stu-id="90be2-109">0x0C15</span></span>  <br/> |
|<span data-ttu-id="90be2-110">Type de données :</span><span class="sxs-lookup"><span data-stu-id="90be2-110">Data type:</span></span>  <br/> |<span data-ttu-id="90be2-111">PT_LONG</span><span class="sxs-lookup"><span data-stu-id="90be2-111">PT_LONG</span></span>  <br/> |
|<span data-ttu-id="90be2-112">Zone :</span><span class="sxs-lookup"><span data-stu-id="90be2-112">Area:</span></span>  <br/> |<span data-ttu-id="90be2-113">Destinataire MAPI</span><span class="sxs-lookup"><span data-stu-id="90be2-113">MAPI recipient</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="90be2-114">Remarques</span><span class="sxs-lookup"><span data-stu-id="90be2-114">Remarks</span></span>

<span data-ttu-id="90be2-115">Le type de destinataire contenu dans cette propriété se compose d’une valeur obligatoire et un indicateur facultatif.</span><span class="sxs-lookup"><span data-stu-id="90be2-115">The recipient type contained in this property consists of one required value and one optional flag.</span></span>
  
<span data-ttu-id="90be2-116">Cette propriété doit contenir exactement une des valeurs suivantes :</span><span class="sxs-lookup"><span data-stu-id="90be2-116">This property must contain exactly one of the following values:</span></span>
  
<span data-ttu-id="90be2-117">MAPI_TO</span><span class="sxs-lookup"><span data-stu-id="90be2-117">MAPI_TO</span></span> 
  
> <span data-ttu-id="90be2-118">Le destinataire est un serveur principal (destinataire à).</span><span class="sxs-lookup"><span data-stu-id="90be2-118">The recipient is a primary (To) recipient.</span></span> <span data-ttu-id="90be2-119">Les clients doivent gérer les destinataires principaux.</span><span class="sxs-lookup"><span data-stu-id="90be2-119">Clients are required to handle primary recipients.</span></span> <span data-ttu-id="90be2-120">Tous les autres types sont facultatifs.</span><span class="sxs-lookup"><span data-stu-id="90be2-120">All other types are optional.</span></span>
    
<span data-ttu-id="90be2-121">NI</span><span class="sxs-lookup"><span data-stu-id="90be2-121">MAPI_CC</span></span> 
  
> <span data-ttu-id="90be2-122">Le destinataire est un destinataire en copie carbone (CC), un destinataire qui reçoit un message en plus des destinataires principaux.</span><span class="sxs-lookup"><span data-stu-id="90be2-122">The recipient is a carbon copy (CC) recipient, a recipient that receives a message in addition to the primary recipients.</span></span>
    
<span data-ttu-id="90be2-123">MAPI_BCC</span><span class="sxs-lookup"><span data-stu-id="90be2-123">MAPI_BCC</span></span> 
  
> <span data-ttu-id="90be2-124">Le destinataire est un destinataire de copie carbone invisible (Cci).</span><span class="sxs-lookup"><span data-stu-id="90be2-124">The recipient is a blind carbon copy (BCC) recipient.</span></span> <span data-ttu-id="90be2-125">Destinataires principal et de copie carbone connaissent l’existence des destinataires Cci.</span><span class="sxs-lookup"><span data-stu-id="90be2-125">Primary and carbon copy recipients are unaware of the existence of BCC recipients.</span></span> 
    
<span data-ttu-id="90be2-126">MAPI_P1</span><span class="sxs-lookup"><span data-stu-id="90be2-126">MAPI_P1</span></span> 
  
> <span data-ttu-id="90be2-127">Le destinataire s’est pas correctement le message lors de la tentative précédente.</span><span class="sxs-lookup"><span data-stu-id="90be2-127">The recipient did not successfully receive the message on the previous attempt.</span></span> <span data-ttu-id="90be2-128">Il s’agit d’un renvoi d’une transmission antérieure.</span><span class="sxs-lookup"><span data-stu-id="90be2-128">This is a resend of an earlier transmission.</span></span>
    
<span data-ttu-id="90be2-129">En outre, l’indicateur suivant peut être définie :</span><span class="sxs-lookup"><span data-stu-id="90be2-129">In addition, the following flag can be set:</span></span>
  
<span data-ttu-id="90be2-130">MAPI_SUBMITTED</span><span class="sxs-lookup"><span data-stu-id="90be2-130">MAPI_SUBMITTED</span></span> 
  
> <span data-ttu-id="90be2-131">Le destinataire a déjà reçu le message et ne doit pas recevoir de nouveau.</span><span class="sxs-lookup"><span data-stu-id="90be2-131">The recipient has already received the message and does not need to receive it again.</span></span> <span data-ttu-id="90be2-132">Il s’agit d’un renvoi d’une transmission antérieure.</span><span class="sxs-lookup"><span data-stu-id="90be2-132">This is a resend of an earlier transmission.</span></span> <span data-ttu-id="90be2-133">Cet indicateur est défini en association avec les valeurs **MAPI_TO**, **ni**et **MAPI_BCC** .</span><span class="sxs-lookup"><span data-stu-id="90be2-133">This flag is set in conjunction with the **MAPI_TO**, **MAPI_CC**, and **MAPI_BCC** values.</span></span> 
    
<span data-ttu-id="90be2-134">La valeur MAPI_P1 et l’indicateur **MAPI_SUBMITTED** est utilisés lors de la retransmission d’un message en raison de non-remise à une ou plusieurs des destinataires.</span><span class="sxs-lookup"><span data-stu-id="90be2-134">The MAPI_P1 value and the **MAPI_SUBMITTED** flag are used when a message is being retransmitted due to nondelivery to one or more of the intended recipients.</span></span> <span data-ttu-id="90be2-135">Pour cette retransmission, le client définit **MAPI_SUBMITTED** sur chaque destinataire n'a pas besoin du message, mais doit être affiché dans la liste des destinataires.</span><span class="sxs-lookup"><span data-stu-id="90be2-135">For this retransmission, the client sets **MAPI_SUBMITTED** on every recipient that does not need the message again but should be displayed in the recipient list.</span></span> <span data-ttu-id="90be2-136">Pour chaque destinataire n’ayant pas reçu le message précédemment, le client conserve le destinataire d’origine dont la valeur est inchangée **PR_RECIPIENT_TYPE** , mais en outre envoie une copie du destinataire avec MAPI_P1 à la place de la valeur d’origine.</span><span class="sxs-lookup"><span data-stu-id="90be2-136">For every recipient that did not receive the message previously, the client retains the original recipient with its **PR_RECIPIENT_TYPE** value unchanged, but additionally submits a copy of the recipient with MAPI_P1 in place of the original value.</span></span> <span data-ttu-id="90be2-137">Cette copie, qui est ignorée avant remise réelle, force le destinataire dans l’enveloppe P1 et garantit retransmission physique à ce destinataire.</span><span class="sxs-lookup"><span data-stu-id="90be2-137">This copy, which is discarded before actual delivery, forces the recipient into the P1 envelope and guarantees physical retransmission to that recipient.</span></span> <span data-ttu-id="90be2-138">La propriété **PR_RESPONSIBILITY** ([PidTagResponsibility](pidtagresponsibility-canonical-property.md)) est définie sur FALSE pour MAPI_P1 destinataires.</span><span class="sxs-lookup"><span data-stu-id="90be2-138">The **PR_RESPONSIBILITY** ([PidTagResponsibility](pidtagresponsibility-canonical-property.md)) property is set to FALSE for MAPI_P1 recipients.</span></span>
  
<span data-ttu-id="90be2-139">Lorsqu’un client affiche un formulaire de renvoi, seuls les destinataires MAPI_P1 sont visibles.</span><span class="sxs-lookup"><span data-stu-id="90be2-139">When a client displays a resend form, only the MAPI_P1 recipients are visible.</span></span> <span data-ttu-id="90be2-140">À moins que l’utilisateur entre des destinataires supplémentaires, lorsque le message est remis, la liste des destinataires s’affiche exactement comme lorsque le message a été envoyé pour la première fois.</span><span class="sxs-lookup"><span data-stu-id="90be2-140">Unless the user enters additional recipients, when the message is delivered, the recipient list appears exactly as it did when the message was sent for the first time.</span></span> 
  
<span data-ttu-id="90be2-141">Le **PR_DISPLAY_TO** ([PidTagDisplayTo](pidtagdisplayto-canonical-property.md)), **PR_DISPLAY_CC** ([PidTagDisplayCc](pidtagdisplaycc-canonical-property.md)) et propriétés **PR_DISPLAY_BCC** ([PidTagDisplayBcc](pidtagdisplaybcc-canonical-property.md)) sont liées à un type de destinataire.</span><span class="sxs-lookup"><span data-stu-id="90be2-141">The **PR_DISPLAY_TO** ([PidTagDisplayTo](pidtagdisplayto-canonical-property.md)), **PR_DISPLAY_CC** ([PidTagDisplayCc](pidtagdisplaycc-canonical-property.md)) and **PR_DISPLAY_BCC** ([PidTagDisplayBcc](pidtagdisplaybcc-canonical-property.md)) properties are related to recipient type.</span></span> <span data-ttu-id="90be2-142">Lorsqu’un client appelle **IMAPIProp::SaveChanges d’un message** et il existe au moins un destinataire dans la liste des destinataires, le fournisseur de banque de messages définit ces propriétés comme suit :</span><span class="sxs-lookup"><span data-stu-id="90be2-142">When a client calls a message's **IMAPIProp::SaveChanges** and there is at least one recipient in the recipient list, the message store provider sets these properties as follows:</span></span> 
  
|<span data-ttu-id="90be2-143">**Propriété**</span><span class="sxs-lookup"><span data-stu-id="90be2-143">**Property**</span></span>|<span data-ttu-id="90be2-144">**Description**</span><span class="sxs-lookup"><span data-stu-id="90be2-144">**Description**</span></span>|
|:-----|:-----|
|<span data-ttu-id="90be2-145">PR_DISPLAY_TO</span><span class="sxs-lookup"><span data-stu-id="90be2-145">PR_DISPLAY_TO</span></span>  <br/> |<span data-ttu-id="90be2-146">La valeur TRUE si un ou plusieurs destinataires sont **MAPI_TO** destinataires.</span><span class="sxs-lookup"><span data-stu-id="90be2-146">Set to TRUE if one or more of the recipients are **MAPI_TO** recipients.</span></span>  <br/> |
|<span data-ttu-id="90be2-147">PR_DISPLAY_CC</span><span class="sxs-lookup"><span data-stu-id="90be2-147">PR_DISPLAY_CC</span></span>  <br/> |<span data-ttu-id="90be2-148">La valeur TRUE si un ou plusieurs destinataires sont **ni** destinataires.</span><span class="sxs-lookup"><span data-stu-id="90be2-148">Set to TRUE if one or more of the recipients are **MAPI_CC** recipients.</span></span>  <br/> |
| <span data-ttu-id="90be2-149">PR_DISPLAY_BCC</span><span class="sxs-lookup"><span data-stu-id="90be2-149">PR_DISPLAY_BCC</span></span>  <br/> |<span data-ttu-id="90be2-150">La valeur TRUE si un ou plusieurs destinataires sont **MAPI_BCC** destinataires.</span><span class="sxs-lookup"><span data-stu-id="90be2-150">Set to TRUE if one or more of the recipients are **MAPI_BCC** recipients.</span></span>  <br/> |
   
<span data-ttu-id="90be2-151">L’enveloppe P1 ou de remise est X.400, les informations nécessaires pour envoyer un message, y compris les propriétés de l’adresse du destinataire et les indicateurs d’option de contrôle de remise et réponses.</span><span class="sxs-lookup"><span data-stu-id="90be2-151">In X.400, the P1 or delivery envelope is the information needed to deliver a message, including the recipient's address properties and any option flags controlling delivery and replies.</span></span> <span data-ttu-id="90be2-152">L’enveloppe P2 ou affichage est les informations généralement affichées pour chaque destinataire autre que le texte du message.</span><span class="sxs-lookup"><span data-stu-id="90be2-152">The P2 or display envelope is the information usually displayed to each recipient other than the message text itself.</span></span> <span data-ttu-id="90be2-153">Il inclut généralement l’objet, importance, priorité, sensibilité et heure d’envoi, comme ainsi que les noms des destinataires principaux et copiés.</span><span class="sxs-lookup"><span data-stu-id="90be2-153">It typically includes the subject, importance, priority, sensitivity, and submission time, as well as the primary and copied recipient names.</span></span> 
  
## <a name="related-resources"></a><span data-ttu-id="90be2-154">Ressources connexes</span><span class="sxs-lookup"><span data-stu-id="90be2-154">Related resources</span></span>

### <a name="protocol-specifications"></a><span data-ttu-id="90be2-155">Spécifications du protocole</span><span class="sxs-lookup"><span data-stu-id="90be2-155">Protocol specifications</span></span>

<span data-ttu-id="90be2-156">[[MS-OXPROPS]](http://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="90be2-156">[[MS-OXPROPS]](http://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="90be2-157">Fournit des références aux spécifications du protocole Exchange Server associées.</span><span class="sxs-lookup"><span data-stu-id="90be2-157">Provides references to related Exchange Server protocol specifications.</span></span>
    
<span data-ttu-id="90be2-158">[[MS-OXCMSG]](http://msdn.microsoft.com/library/7fd7ec40-deec-4c06-9493-1bc06b349682%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="90be2-158">[[MS-OXCMSG]](http://msdn.microsoft.com/library/7fd7ec40-deec-4c06-9493-1bc06b349682%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="90be2-159">Gère les objets de message et la pièce jointe.</span><span class="sxs-lookup"><span data-stu-id="90be2-159">Handles message and attachment objects.</span></span>
    
<span data-ttu-id="90be2-160">[[MS-OXOMSG]](http://msdn.microsoft.com/library/daa9120f-f325-4afb-a738-28f91049ab3c%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="90be2-160">[[MS-OXOMSG]](http://msdn.microsoft.com/library/daa9120f-f325-4afb-a738-28f91049ab3c%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="90be2-161">Spécifie les propriétés et les opérations qui sont autorisées pour les objets de message électronique.</span><span class="sxs-lookup"><span data-stu-id="90be2-161">Specifies the properties and operations that are permissible for email message objects.</span></span>
    
<span data-ttu-id="90be2-162">[[MS-OXOCAL]](http://msdn.microsoft.com/library/09861fde-c8e4-4028-9346-e7c214cfdba1%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="90be2-162">[[MS-OXOCAL]](http://msdn.microsoft.com/library/09861fde-c8e4-4028-9346-e7c214cfdba1%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="90be2-163">Spécifie les propriétés et opérations pour un rendez-vous, une demande de réunion et les messages de réponse.</span><span class="sxs-lookup"><span data-stu-id="90be2-163">Specifies the properties and operations for appointment, meeting request, and response messages.</span></span>
    
### <a name="header-files"></a><span data-ttu-id="90be2-164">Fichiers d’en-tête</span><span class="sxs-lookup"><span data-stu-id="90be2-164">Header files</span></span>

<span data-ttu-id="90be2-165">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="90be2-165">Mapidefs.h</span></span>
  
> <span data-ttu-id="90be2-166">Fournit des définitions de type de données.</span><span class="sxs-lookup"><span data-stu-id="90be2-166">Provides data type definitions.</span></span>
    
<span data-ttu-id="90be2-167">MAPITAGS.h</span><span class="sxs-lookup"><span data-stu-id="90be2-167">Mapitags.h</span></span>
  
> <span data-ttu-id="90be2-168">Contient les définitions des propriétés répertoriées en tant que d’autres noms.</span><span class="sxs-lookup"><span data-stu-id="90be2-168">Contains definitions of properties listed as alternate names.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="90be2-169">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="90be2-169">See also</span></span>



[<span data-ttu-id="90be2-170">Propriété canonique PidTagRecipientStatus</span><span class="sxs-lookup"><span data-stu-id="90be2-170">PidTagRecipientStatus Canonical Property</span></span>](pidtagrecipientstatus-canonical-property.md)
  
[<span data-ttu-id="90be2-171">Propriété canonique PidTagDisplayTo</span><span class="sxs-lookup"><span data-stu-id="90be2-171">PidTagDisplayTo Canonical Property</span></span>](pidtagdisplayto-canonical-property.md)
  
[<span data-ttu-id="90be2-172">Propriété canonique PidTagDisplayBcc</span><span class="sxs-lookup"><span data-stu-id="90be2-172">PidTagDisplayBcc Canonical Property</span></span>](pidtagdisplaybcc-canonical-property.md)
  
[<span data-ttu-id="90be2-173">Propriété canonique PidTagDisplayCc</span><span class="sxs-lookup"><span data-stu-id="90be2-173">PidTagDisplayCc Canonical Property</span></span>](pidtagdisplaycc-canonical-property.md)


[<span data-ttu-id="90be2-174">Propriétés MAPI</span><span class="sxs-lookup"><span data-stu-id="90be2-174">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="90be2-175">Propriétés canoniques MAPI</span><span class="sxs-lookup"><span data-stu-id="90be2-175">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="90be2-176">Mappage de noms de propriété canonique aux noms MAPI</span><span class="sxs-lookup"><span data-stu-id="90be2-176">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="90be2-177">Mappage de noms MAPI pour les noms de propriété canonique</span><span class="sxs-lookup"><span data-stu-id="90be2-177">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

