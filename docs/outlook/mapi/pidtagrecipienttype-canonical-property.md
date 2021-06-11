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
description: Dernière modification le 9 mars 2015
ms.openlocfilehash: 9d74fdb3acb6db94078d6090f0def050fb564cd9
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32355257"
---
# <a name="pidtagrecipienttype-canonical-property"></a><span data-ttu-id="c5fdf-103">Propriété canonique PidTagRecipientType</span><span class="sxs-lookup"><span data-stu-id="c5fdf-103">PidTagRecipientType Canonical Property</span></span>

  
  
<span data-ttu-id="c5fdf-104">**S’applique à** : Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="c5fdf-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="c5fdf-105">Contient le type de destinataire d’un destinataire de message.</span><span class="sxs-lookup"><span data-stu-id="c5fdf-105">Contains the recipient type for a message recipient.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="c5fdf-106">Propriétés associées :</span><span class="sxs-lookup"><span data-stu-id="c5fdf-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="c5fdf-107">PR_RECIPIENT_TYPE</span><span class="sxs-lookup"><span data-stu-id="c5fdf-107">PR_RECIPIENT_TYPE</span></span>  <br/> |
|<span data-ttu-id="c5fdf-108">Identificateur :</span><span class="sxs-lookup"><span data-stu-id="c5fdf-108">Identifier:</span></span>  <br/> |<span data-ttu-id="c5fdf-109">0x0C15</span><span class="sxs-lookup"><span data-stu-id="c5fdf-109">0x0C15</span></span>  <br/> |
|<span data-ttu-id="c5fdf-110">Type de données :</span><span class="sxs-lookup"><span data-stu-id="c5fdf-110">Data type:</span></span>  <br/> |<span data-ttu-id="c5fdf-111">PT_LONG</span><span class="sxs-lookup"><span data-stu-id="c5fdf-111">PT_LONG</span></span>  <br/> |
|<span data-ttu-id="c5fdf-112">Domaine :</span><span class="sxs-lookup"><span data-stu-id="c5fdf-112">Area:</span></span>  <br/> |<span data-ttu-id="c5fdf-113">Destinataire MAPI</span><span class="sxs-lookup"><span data-stu-id="c5fdf-113">MAPI recipient</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="c5fdf-114">Remarques</span><span class="sxs-lookup"><span data-stu-id="c5fdf-114">Remarks</span></span>

<span data-ttu-id="c5fdf-115">Le type de destinataire contenu dans cette propriété se compose d’une valeur requise et d’un indicateur facultatif.</span><span class="sxs-lookup"><span data-stu-id="c5fdf-115">The recipient type contained in this property consists of one required value and one optional flag.</span></span>
  
<span data-ttu-id="c5fdf-116">Cette propriété doit contenir exactement l’une des valeurs suivantes :</span><span class="sxs-lookup"><span data-stu-id="c5fdf-116">This property must contain exactly one of the following values:</span></span>
  
<span data-ttu-id="c5fdf-117">MAPI_TO</span><span class="sxs-lookup"><span data-stu-id="c5fdf-117">MAPI_TO</span></span> 
  
> <span data-ttu-id="c5fdf-118">Le destinataire est un destinataire principal (À).</span><span class="sxs-lookup"><span data-stu-id="c5fdf-118">The recipient is a primary (To) recipient.</span></span> <span data-ttu-id="c5fdf-119">Les clients sont tenus de gérer les destinataires principaux.</span><span class="sxs-lookup"><span data-stu-id="c5fdf-119">Clients are required to handle primary recipients.</span></span> <span data-ttu-id="c5fdf-120">Tous les autres types sont facultatifs.</span><span class="sxs-lookup"><span data-stu-id="c5fdf-120">All other types are optional.</span></span>
    
<span data-ttu-id="c5fdf-121">MAPI_CC</span><span class="sxs-lookup"><span data-stu-id="c5fdf-121">MAPI_CC</span></span> 
  
> <span data-ttu-id="c5fdf-122">Le destinataire est un destinataire en copie carbone (CC), un destinataire qui reçoit un message en plus des destinataires principaux.</span><span class="sxs-lookup"><span data-stu-id="c5fdf-122">The recipient is a carbon copy (CC) recipient, a recipient that receives a message in addition to the primary recipients.</span></span>
    
<span data-ttu-id="c5fdf-123">MAPI_BCC</span><span class="sxs-lookup"><span data-stu-id="c5fdf-123">MAPI_BCC</span></span> 
  
> <span data-ttu-id="c5fdf-124">Le destinataire est un destinataire en copie carbone non voyante (Bc).</span><span class="sxs-lookup"><span data-stu-id="c5fdf-124">The recipient is a blind carbon copy (BCC) recipient.</span></span> <span data-ttu-id="c5fdf-125">Les destinataires de copie principale et carbone ignorent l’existence de destinataires BcC.</span><span class="sxs-lookup"><span data-stu-id="c5fdf-125">Primary and carbon copy recipients are unaware of the existence of BCC recipients.</span></span> 
    
<span data-ttu-id="c5fdf-126">MAPI_P1</span><span class="sxs-lookup"><span data-stu-id="c5fdf-126">MAPI_P1</span></span> 
  
> <span data-ttu-id="c5fdf-127">Le destinataire n’a pas reçu le message lors de la tentative précédente.</span><span class="sxs-lookup"><span data-stu-id="c5fdf-127">The recipient did not successfully receive the message on the previous attempt.</span></span> <span data-ttu-id="c5fdf-128">Il s’agit d’un renvoyer d’une transmission antérieure.</span><span class="sxs-lookup"><span data-stu-id="c5fdf-128">This is a resend of an earlier transmission.</span></span>
    
<span data-ttu-id="c5fdf-129">En outre, l’indicateur suivant peut être définie :</span><span class="sxs-lookup"><span data-stu-id="c5fdf-129">In addition, the following flag can be set:</span></span>
  
<span data-ttu-id="c5fdf-130">MAPI_SUBMITTED</span><span class="sxs-lookup"><span data-stu-id="c5fdf-130">MAPI_SUBMITTED</span></span> 
  
> <span data-ttu-id="c5fdf-131">Le destinataire a déjà reçu le message et n’a pas besoin de le recevoir à nouveau.</span><span class="sxs-lookup"><span data-stu-id="c5fdf-131">The recipient has already received the message and does not need to receive it again.</span></span> <span data-ttu-id="c5fdf-132">Il s’agit d’un renvoyer d’une transmission antérieure.</span><span class="sxs-lookup"><span data-stu-id="c5fdf-132">This is a resend of an earlier transmission.</span></span> <span data-ttu-id="c5fdf-133">Cet indicateur est associé aux valeurs **MAPI_TO,** **MAPI_CC** et **MAPI_BCC** valeurs.</span><span class="sxs-lookup"><span data-stu-id="c5fdf-133">This flag is set in conjunction with the **MAPI_TO**, **MAPI_CC**, and **MAPI_BCC** values.</span></span> 
    
<span data-ttu-id="c5fdf-134">La MAPI_P1 et l’indicateur **MAPI_SUBMITTED** sont utilisés lorsqu’un message est retransmis en raison d’une non-remise à un ou plusieurs des destinataires prévus.</span><span class="sxs-lookup"><span data-stu-id="c5fdf-134">The MAPI_P1 value and the **MAPI_SUBMITTED** flag are used when a message is being retransmitted due to nondelivery to one or more of the intended recipients.</span></span> <span data-ttu-id="c5fdf-135">Pour cette retransmission, le client définit **MAPI_SUBMITTED** sur chaque destinataire qui n’a pas besoin de nouveau du message, mais qui doit être affiché dans la liste des destinataires.</span><span class="sxs-lookup"><span data-stu-id="c5fdf-135">For this retransmission, the client sets **MAPI_SUBMITTED** on every recipient that does not need the message again but should be displayed in the recipient list.</span></span> <span data-ttu-id="c5fdf-136">Pour chaque destinataire qui **n’a** pas reçu le message précédemment, le client conserve le destinataire d’origine avec sa valeur PR_RECIPIENT_TYPE inchangée, mais envoie en outre une copie du destinataire avec MAPI_P1 à la place de la valeur d’origine.</span><span class="sxs-lookup"><span data-stu-id="c5fdf-136">For every recipient that did not receive the message previously, the client retains the original recipient with its **PR_RECIPIENT_TYPE** value unchanged, but additionally submits a copy of the recipient with MAPI_P1 in place of the original value.</span></span> <span data-ttu-id="c5fdf-137">Cette copie, qui est ignorée avant la remise réelle, force le destinataire dans l’enveloppe P1 et garantit la retransmission physique à ce destinataire.</span><span class="sxs-lookup"><span data-stu-id="c5fdf-137">This copy, which is discarded before actual delivery, forces the recipient into the P1 envelope and guarantees physical retransmission to that recipient.</span></span> <span data-ttu-id="c5fdf-138">La **propriété PR_RESPONSIBILITY** ([PidTagResponsibility](pidtagresponsibility-canonical-property.md)) est définie sur FALSE pour MAPI_P1 destinataires.</span><span class="sxs-lookup"><span data-stu-id="c5fdf-138">The **PR_RESPONSIBILITY** ([PidTagResponsibility](pidtagresponsibility-canonical-property.md)) property is set to FALSE for MAPI_P1 recipients.</span></span>
  
<span data-ttu-id="c5fdf-139">Lorsqu’un client affiche un formulaire de renvoyer, seuls les destinataires MAPI_P1 sont visibles.</span><span class="sxs-lookup"><span data-stu-id="c5fdf-139">When a client displays a resend form, only the MAPI_P1 recipients are visible.</span></span> <span data-ttu-id="c5fdf-140">Sauf si l’utilisateur entre des destinataires supplémentaires, lorsque le message est remis, la liste des destinataires s’affiche exactement comme lors de la première envoi du message.</span><span class="sxs-lookup"><span data-stu-id="c5fdf-140">Unless the user enters additional recipients, when the message is delivered, the recipient list appears exactly as it did when the message was sent for the first time.</span></span> 
  
<span data-ttu-id="c5fdf-141">Les **propriétés PR_DISPLAY_TO** ([PidTagDisplayTo](pidtagdisplayto-canonical-property.md)), **PR_DISPLAY_CC** ([PidTagDisplayCc](pidtagdisplaycc-canonical-property.md)) et **PR_DISPLAY_BCC** ([PidTagDisplayBcc](pidtagdisplaybcc-canonical-property.md)) sont liées au type de destinataire.</span><span class="sxs-lookup"><span data-stu-id="c5fdf-141">The **PR_DISPLAY_TO** ([PidTagDisplayTo](pidtagdisplayto-canonical-property.md)), **PR_DISPLAY_CC** ([PidTagDisplayCc](pidtagdisplaycc-canonical-property.md)) and **PR_DISPLAY_BCC** ([PidTagDisplayBcc](pidtagdisplaybcc-canonical-property.md)) properties are related to recipient type.</span></span> <span data-ttu-id="c5fdf-142">Lorsqu’un client appelle **IMAPIProp::SaveChanges** d’un message et qu’il y a au moins un destinataire dans la liste des destinataires, le fournisseur de magasin de messages définit ces propriétés comme suit :</span><span class="sxs-lookup"><span data-stu-id="c5fdf-142">When a client calls a message's **IMAPIProp::SaveChanges** and there is at least one recipient in the recipient list, the message store provider sets these properties as follows:</span></span> 
  
|<span data-ttu-id="c5fdf-143">**Propriété**</span><span class="sxs-lookup"><span data-stu-id="c5fdf-143">**Property**</span></span>|<span data-ttu-id="c5fdf-144">**Description**</span><span class="sxs-lookup"><span data-stu-id="c5fdf-144">**Description**</span></span>|
|:-----|:-----|
|<span data-ttu-id="c5fdf-145">PR_DISPLAY_TO</span><span class="sxs-lookup"><span data-stu-id="c5fdf-145">PR_DISPLAY_TO</span></span>  <br/> |<span data-ttu-id="c5fdf-146">Définissez cette valeur sur TRUE si un ou plusieurs destinataires sont **MAPI_TO** destinataires.</span><span class="sxs-lookup"><span data-stu-id="c5fdf-146">Set to TRUE if one or more of the recipients are **MAPI_TO** recipients.</span></span>  <br/> |
|<span data-ttu-id="c5fdf-147">PR_DISPLAY_CC</span><span class="sxs-lookup"><span data-stu-id="c5fdf-147">PR_DISPLAY_CC</span></span>  <br/> |<span data-ttu-id="c5fdf-148">Définissez cette valeur sur TRUE si un ou plusieurs destinataires sont **MAPI_CC** destinataires.</span><span class="sxs-lookup"><span data-stu-id="c5fdf-148">Set to TRUE if one or more of the recipients are **MAPI_CC** recipients.</span></span>  <br/> |
| <span data-ttu-id="c5fdf-149">PR_DISPLAY_BCC</span><span class="sxs-lookup"><span data-stu-id="c5fdf-149">PR_DISPLAY_BCC</span></span>  <br/> |<span data-ttu-id="c5fdf-150">Définissez cette valeur sur TRUE si un ou plusieurs destinataires sont **MAPI_BCC** destinataires.</span><span class="sxs-lookup"><span data-stu-id="c5fdf-150">Set to TRUE if one or more of the recipients are **MAPI_BCC** recipients.</span></span>  <br/> |
   
<span data-ttu-id="c5fdf-151">Dans X.400, l’enveloppe P1 ou de remise est les informations nécessaires pour remettre un message, y compris les propriétés d’adresse du destinataire et les indicateurs d’option contrôlant la remise et les réponses.</span><span class="sxs-lookup"><span data-stu-id="c5fdf-151">In X.400, the P1 or delivery envelope is the information needed to deliver a message, including the recipient's address properties and any option flags controlling delivery and replies.</span></span> <span data-ttu-id="c5fdf-152">L’enveloppe P2 ou d’affichage est les informations généralement affichées pour chaque destinataire autre que le texte du message lui-même.</span><span class="sxs-lookup"><span data-stu-id="c5fdf-152">The P2 or display envelope is the information usually displayed to each recipient other than the message text itself.</span></span> <span data-ttu-id="c5fdf-153">Il inclut généralement l’objet, l’importance, la priorité, la sensibilité et l’heure d’envoi, ainsi que les noms des destinataires principaux et copiés.</span><span class="sxs-lookup"><span data-stu-id="c5fdf-153">It typically includes the subject, importance, priority, sensitivity, and submission time, as well as the primary and copied recipient names.</span></span> 
  
## <a name="related-resources"></a><span data-ttu-id="c5fdf-154">Ressources connexes</span><span class="sxs-lookup"><span data-stu-id="c5fdf-154">Related resources</span></span>

### <a name="protocol-specifications"></a><span data-ttu-id="c5fdf-155">Spécifications de protocole</span><span class="sxs-lookup"><span data-stu-id="c5fdf-155">Protocol specifications</span></span>

<span data-ttu-id="c5fdf-156">[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="c5fdf-156">[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="c5fdf-157">Fournit des références aux spécifications Exchange Server protocole.</span><span class="sxs-lookup"><span data-stu-id="c5fdf-157">Provides references to related Exchange Server protocol specifications.</span></span>
    
<span data-ttu-id="c5fdf-158">[[MS-OXCMSG]](https://msdn.microsoft.com/library/7fd7ec40-deec-4c06-9493-1bc06b349682%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="c5fdf-158">[[MS-OXCMSG]](https://msdn.microsoft.com/library/7fd7ec40-deec-4c06-9493-1bc06b349682%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="c5fdf-159">Gère les objets message et pièce jointe.</span><span class="sxs-lookup"><span data-stu-id="c5fdf-159">Handles message and attachment objects.</span></span>
    
<span data-ttu-id="c5fdf-160">[[MS-OXOMSG]](https://msdn.microsoft.com/library/daa9120f-f325-4afb-a738-28f91049ab3c%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="c5fdf-160">[[MS-OXOMSG]](https://msdn.microsoft.com/library/daa9120f-f325-4afb-a738-28f91049ab3c%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="c5fdf-161">Spécifie les propriétés et opérations autorisées pour les objets de message électronique.</span><span class="sxs-lookup"><span data-stu-id="c5fdf-161">Specifies the properties and operations that are permissible for email message objects.</span></span>
    
<span data-ttu-id="c5fdf-162">[[MS-OXOCAL]](https://msdn.microsoft.com/library/09861fde-c8e4-4028-9346-e7c214cfdba1%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="c5fdf-162">[[MS-OXOCAL]](https://msdn.microsoft.com/library/09861fde-c8e4-4028-9346-e7c214cfdba1%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="c5fdf-163">Spécifie les propriétés et les opérations pour les messages de rendez-vous, de demande de réunion et de réponse.</span><span class="sxs-lookup"><span data-stu-id="c5fdf-163">Specifies the properties and operations for appointment, meeting request, and response messages.</span></span>
    
### <a name="header-files"></a><span data-ttu-id="c5fdf-164">Fichiers d’en-tête</span><span class="sxs-lookup"><span data-stu-id="c5fdf-164">Header files</span></span>

<span data-ttu-id="c5fdf-165">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="c5fdf-165">Mapidefs.h</span></span>
  
> <span data-ttu-id="c5fdf-166">Fournit des définitions de type de données.</span><span class="sxs-lookup"><span data-stu-id="c5fdf-166">Provides data type definitions.</span></span>
    
<span data-ttu-id="c5fdf-167">Mapitags.h</span><span class="sxs-lookup"><span data-stu-id="c5fdf-167">Mapitags.h</span></span>
  
> <span data-ttu-id="c5fdf-168">Contient les définitions des propriétés répertoriées en tant que noms de remplacement.</span><span class="sxs-lookup"><span data-stu-id="c5fdf-168">Contains definitions of properties listed as alternate names.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="c5fdf-169">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="c5fdf-169">See also</span></span>



[<span data-ttu-id="c5fdf-170">Propriété canonique PidTagRecipientStatus</span><span class="sxs-lookup"><span data-stu-id="c5fdf-170">PidTagRecipientStatus Canonical Property</span></span>](pidtagrecipientstatus-canonical-property.md)
  
[<span data-ttu-id="c5fdf-171">Propriété canonique PidTagDisplayTo</span><span class="sxs-lookup"><span data-stu-id="c5fdf-171">PidTagDisplayTo Canonical Property</span></span>](pidtagdisplayto-canonical-property.md)
  
[<span data-ttu-id="c5fdf-172">Propriété canonique PidTagDisplayBcc</span><span class="sxs-lookup"><span data-stu-id="c5fdf-172">PidTagDisplayBcc Canonical Property</span></span>](pidtagdisplaybcc-canonical-property.md)
  
[<span data-ttu-id="c5fdf-173">Propriété canonique PidTagDisplayCc</span><span class="sxs-lookup"><span data-stu-id="c5fdf-173">PidTagDisplayCc Canonical Property</span></span>](pidtagdisplaycc-canonical-property.md)


[<span data-ttu-id="c5fdf-174">Propriétés MAPI</span><span class="sxs-lookup"><span data-stu-id="c5fdf-174">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="c5fdf-175">Propriétés canoniques MAPI</span><span class="sxs-lookup"><span data-stu-id="c5fdf-175">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="c5fdf-176">Mappage des noms de propriétés canoniques aux noms MAPI</span><span class="sxs-lookup"><span data-stu-id="c5fdf-176">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="c5fdf-177">Mappage des noms MAPI aux noms de propriétés canoniques</span><span class="sxs-lookup"><span data-stu-id="c5fdf-177">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

