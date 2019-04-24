---
title: Propriété canonique PidTagMessageRecipients
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- PidTagMessageRecipients
api_type:
- HeaderDef
ms.assetid: 7f8b0d96-99d6-4f1c-8ac4-4dbb83626382
description: 'Derni�re modification�: lundi 9 mars 2015'
ms.openlocfilehash: d30088ba7398669228a18be825323afa800ec536
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32355684"
---
# <a name="pidtagmessagerecipients-canonical-property"></a><span data-ttu-id="5eeca-103">Propriété canonique PidTagMessageRecipients</span><span class="sxs-lookup"><span data-stu-id="5eeca-103">PidTagMessageRecipients Canonical Property</span></span>

  
  
<span data-ttu-id="5eeca-104">**S’applique à** : Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="5eeca-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="5eeca-105">Contient un tableau de restrictions qui peuvent être appliquées à une table de contenu pour rechercher tous les messages qui contiennent des sous-objets de destinataire qui répondent aux restrictions.</span><span class="sxs-lookup"><span data-stu-id="5eeca-105">Contains a table of restrictions that can be applied to a contents table to find all messages that contain recipient subobjects that meet the restrictions.</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="5eeca-106">Propriétés associées :</span><span class="sxs-lookup"><span data-stu-id="5eeca-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="5eeca-107">PR_MESSAGE_RECIPIENTS</span><span class="sxs-lookup"><span data-stu-id="5eeca-107">PR_MESSAGE_RECIPIENTS</span></span>  <br/> |
|<span data-ttu-id="5eeca-108">Identificateur :</span><span class="sxs-lookup"><span data-stu-id="5eeca-108">Identifier:</span></span>  <br/> |<span data-ttu-id="5eeca-109">0x0E12</span><span class="sxs-lookup"><span data-stu-id="5eeca-109">0x0E12</span></span>  <br/> |
|<span data-ttu-id="5eeca-110">Type de données :</span><span class="sxs-lookup"><span data-stu-id="5eeca-110">Data type:</span></span>  <br/> |<span data-ttu-id="5eeca-111">PT_OBJECT</span><span class="sxs-lookup"><span data-stu-id="5eeca-111">PT_OBJECT</span></span>  <br/> |
|<span data-ttu-id="5eeca-112">Domaine :</span><span class="sxs-lookup"><span data-stu-id="5eeca-112">Area:</span></span>  <br/> |<span data-ttu-id="5eeca-113">Messagerie générale</span><span class="sxs-lookup"><span data-stu-id="5eeca-113">General messaging</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="5eeca-114">Remarques</span><span class="sxs-lookup"><span data-stu-id="5eeca-114">Remarks</span></span>

<span data-ttu-id="5eeca-115">Cette propriété peut être exclue dans [IMAPIProp:: CopyTo](imapiprop-copyto.md) Operations ou incluse dans [IMAPIProp:: CopyProps](imapiprop-copyprops.md) Operations.</span><span class="sxs-lookup"><span data-stu-id="5eeca-115">This property can be excluded in [IMAPIProp::CopyTo](imapiprop-copyto.md) operations or included in [IMAPIProp::CopyProps](imapiprop-copyprops.md) operations.</span></span> <span data-ttu-id="5eeca-116">En tant que propriété de type **PT_OBJECT**, elle ne peut pas être récupérée avec succès par la méthode [IMAPIProp:: GetProps](imapiprop-getprops.md) .</span><span class="sxs-lookup"><span data-stu-id="5eeca-116">As a property of type **PT_OBJECT**, it cannot be successfully retrieved by the [IMAPIProp::GetProps](imapiprop-getprops.md) method.</span></span> <span data-ttu-id="5eeca-117">Son contenu doit être accessible à l'aide de la méthode [IMAPIProp:: OpenProperty](imapiprop-openproperty.md) , qui demande l'identificateur d'interface **IID_IMAPITable** .</span><span class="sxs-lookup"><span data-stu-id="5eeca-117">Its contents should be accessed by the [IMAPIProp::OpenProperty](imapiprop-openproperty.md) method, requesting the **IID_IMAPITable** interface identifier.</span></span> <span data-ttu-id="5eeca-118">Les fournisseurs de services doivent le signaler à la méthode [IMAPIProp:: GetPropList](imapiprop-getproplist.md) s'il est défini, mais éventuellement le signaler ou non s'il n'est pas défini.</span><span class="sxs-lookup"><span data-stu-id="5eeca-118">Service providers must report it to the [IMAPIProp::GetPropList](imapiprop-getproplist.md) method if it is set, but may optionally report it or not if it is not set.</span></span> 
  
<span data-ttu-id="5eeca-119">Pour récupérer le contenu de la table, une application cliente doit appeler la méthode [IMessage:: GetRecipientTable](imessage-getrecipienttable.md) .</span><span class="sxs-lookup"><span data-stu-id="5eeca-119">To retrieve table contents, a client application should call the [IMessage::GetRecipientTable](imessage-getrecipienttable.md) method.</span></span> 
  
<span data-ttu-id="5eeca-120">Cette propriété peut être utilisée pour la restriction de sous-objet en la spécifiant dans la structure [SSubRestriction](ssubrestriction.md) .</span><span class="sxs-lookup"><span data-stu-id="5eeca-120">This property can be used for subobject restriction by specifying it in the [SSubRestriction](ssubrestriction.md) structure.</span></span> <span data-ttu-id="5eeca-121">Cela permet à un client de limiter l'affichage d'un conteneur aux messages pour lesquels les destinataires répondent à des critères.</span><span class="sxs-lookup"><span data-stu-id="5eeca-121">This enables a client to limit the view of a container to messages with recipients meeting given criteria.</span></span> <span data-ttu-id="5eeca-122">Un message qualifie pour l'affichage si au moins une ligne dans sa table de destinataires, c'est-à-dire un destinataire répond à la restriction de sous-objet.</span><span class="sxs-lookup"><span data-stu-id="5eeca-122">A message qualifies for viewing if at least one row in its recipient table, that is, one recipient satisfies the subobject restriction.</span></span> 
  
 <span data-ttu-id="5eeca-123">**Note** L'utilisation de résultats de restriction de sous-objet équivaut à un appel [IMAPISession:: OpenEntry](imapisession-openentry.md) sur chaque message du tableau.</span><span class="sxs-lookup"><span data-stu-id="5eeca-123">**Note** Using subobject restriction results is the equivalent of an [IMAPISession::OpenEntry](imapisession-openentry.md) call on every message in the table.</span></span> <span data-ttu-id="5eeca-124">En fonction de l'application cliente et du nombre de messages à rechercher, cela peut affecter les performances.</span><span class="sxs-lookup"><span data-stu-id="5eeca-124">Depending on the client application and the number of messages to be searched, it can affect performance.</span></span> 
  
<span data-ttu-id="5eeca-125">La propriété **PR_MESSAGE_ATTACHMENTS** ([PidTagMessageAttachments](pidtagmessageattachments-canonical-property.md)) et cette propriété sont similaires en matière d'utilisation.</span><span class="sxs-lookup"><span data-stu-id="5eeca-125">The **PR_MESSAGE_ATTACHMENTS** ([PidTagMessageAttachments](pidtagmessageattachments-canonical-property.md)) property and this property are similar in usage.</span></span> <span data-ttu-id="5eeca-126">Plusieurs propriétés MAPI permettent d'accéder à des tables:</span><span class="sxs-lookup"><span data-stu-id="5eeca-126">Several MAPI properties provide access to tables:</span></span> 
  
|<span data-ttu-id="5eeca-127">**Property**</span><span class="sxs-lookup"><span data-stu-id="5eeca-127">**Property**</span></span>|<span data-ttu-id="5eeca-128">**Table**</span><span class="sxs-lookup"><span data-stu-id="5eeca-128">**Table**</span></span>|
|:-----|:-----|
|<span data-ttu-id="5eeca-129">**PR_CONTAINER_CONTENTS** ([PidTagContainerContents](pidtagcontainercontents-canonical-property.md))</span><span class="sxs-lookup"><span data-stu-id="5eeca-129">**PR_CONTAINER_CONTENTS** ([PidTagContainerContents](pidtagcontainercontents-canonical-property.md))</span></span>  <br/> |<span data-ttu-id="5eeca-130">Table des matières</span><span class="sxs-lookup"><span data-stu-id="5eeca-130">Contents table</span></span>  <br/> |
|<span data-ttu-id="5eeca-131">**PR_CONTAINER_HIERARCHY** ([PidTagContainerHierarchy](pidtagcontainerhierarchy-canonical-property.md))</span><span class="sxs-lookup"><span data-stu-id="5eeca-131">**PR_CONTAINER_HIERARCHY** ([PidTagContainerHierarchy](pidtagcontainerhierarchy-canonical-property.md))</span></span>  <br/> |<span data-ttu-id="5eeca-132">Table Hierarchy</span><span class="sxs-lookup"><span data-stu-id="5eeca-132">Hierarchy table</span></span>  <br/> |
|<span data-ttu-id="5eeca-133">**PR_FOLDER_ASSOCIATED_CONTENTS** ([PidTagFolderAssociatedContents](pidtagfolderassociatedcontents-canonical-property.md))</span><span class="sxs-lookup"><span data-stu-id="5eeca-133">**PR_FOLDER_ASSOCIATED_CONTENTS** ([PidTagFolderAssociatedContents](pidtagfolderassociatedcontents-canonical-property.md))</span></span>  <br/> |<span data-ttu-id="5eeca-134">Table des matières associées</span><span class="sxs-lookup"><span data-stu-id="5eeca-134">Associated contents table</span></span>  <br/> |
|<span data-ttu-id="5eeca-135">**PR_MESSAGE_ATTACHMENTS** ([PidTagMessageAttachments](pidtagmessageattachments-canonical-property.md))</span><span class="sxs-lookup"><span data-stu-id="5eeca-135">**PR_MESSAGE_ATTACHMENTS** ([PidTagMessageAttachments](pidtagmessageattachments-canonical-property.md))</span></span>  <br/> |<span data-ttu-id="5eeca-136">Table des pièces jointes</span><span class="sxs-lookup"><span data-stu-id="5eeca-136">Attachment table</span></span>  <br/> |
|<span data-ttu-id="5eeca-137">PR_MESSAGE_RECIPIENTS</span><span class="sxs-lookup"><span data-stu-id="5eeca-137">PR_MESSAGE_RECIPIENTS</span></span>  <br/> |<span data-ttu-id="5eeca-138">Table de destinataires</span><span class="sxs-lookup"><span data-stu-id="5eeca-138">Recipient table</span></span>  <br/> |
   
## <a name="related-resources"></a><span data-ttu-id="5eeca-139">Ressources associées</span><span class="sxs-lookup"><span data-stu-id="5eeca-139">Related resources</span></span>

### <a name="protocol-specifications"></a><span data-ttu-id="5eeca-140">Spécifications de protocole</span><span class="sxs-lookup"><span data-stu-id="5eeca-140">Protocol specifications</span></span>

<span data-ttu-id="5eeca-141">[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="5eeca-141">[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="5eeca-142">Fournit des références à des spécifications de protocole Exchange Server connexes.</span><span class="sxs-lookup"><span data-stu-id="5eeca-142">Provides references to related Exchange Server protocol specifications.</span></span>
    
<span data-ttu-id="5eeca-143">[[MS-OXCFXICS]](https://msdn.microsoft.com/library/b9752f3d-d50d-44b8-9e6b-608a117c8532%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="5eeca-143">[[MS-OXCFXICS]](https://msdn.microsoft.com/library/b9752f3d-d50d-44b8-9e6b-608a117c8532%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="5eeca-144">Gère l'ordre et le flux de transfert de données entre un client et un serveur.</span><span class="sxs-lookup"><span data-stu-id="5eeca-144">Handles the order and flow for data transfers between a client and server.</span></span>
    
<span data-ttu-id="5eeca-145">[[MS-OXCICAL]](https://msdn.microsoft.com/library/a685a040-5b69-4c84-b084-795113fb4012%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="5eeca-145">[[MS-OXCICAL]](https://msdn.microsoft.com/library/a685a040-5b69-4c84-b084-795113fb4012%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="5eeca-146">Effectue une conversion entre l'IETF RFC2445, RFC2446 et RFC2447, et les objets de rendez-vous et de réunion.</span><span class="sxs-lookup"><span data-stu-id="5eeca-146">Converts between IETF RFC2445, RFC2446, and RFC2447, and appointment and meeting objects.</span></span>
    
<span data-ttu-id="5eeca-147">[[MS-OXCSPAM]](https://msdn.microsoft.com/library/522f8587-4aed-4cd6-831b-40bd87862189%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="5eeca-147">[[MS-OXCSPAM]](https://msdn.microsoft.com/library/522f8587-4aed-4cd6-831b-40bd87862189%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="5eeca-148">Active la gestion des listes d'autorisation/de blocage et la détermination des messages électroniques indésirables.</span><span class="sxs-lookup"><span data-stu-id="5eeca-148">Enables the handling of allow/block lists and the determination of junk email messages.</span></span>
    
<span data-ttu-id="5eeca-149">[[MS-OXTNEF]](https://msdn.microsoft.com/library/1f0544d7-30b7-4194-b58f-adc82f3763bb%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="5eeca-149">[[MS-OXTNEF]](https://msdn.microsoft.com/library/1f0544d7-30b7-4194-b58f-adc82f3763bb%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="5eeca-150">Encode et décode les objets message et Attachment en une représentation de flux efficace.</span><span class="sxs-lookup"><span data-stu-id="5eeca-150">Encodes and decodes message and attachment objects to an efficient stream representation.</span></span>
    
### <a name="header-files"></a><span data-ttu-id="5eeca-151">Fichiers d'en-tête</span><span class="sxs-lookup"><span data-stu-id="5eeca-151">Header files</span></span>

<span data-ttu-id="5eeca-152">Mapidefs. h</span><span class="sxs-lookup"><span data-stu-id="5eeca-152">Mapidefs.h</span></span>
  
> <span data-ttu-id="5eeca-153">Fournit des définitions de type de données.</span><span class="sxs-lookup"><span data-stu-id="5eeca-153">Provides data type definitions.</span></span>
    
<span data-ttu-id="5eeca-154">Mapitags. h</span><span class="sxs-lookup"><span data-stu-id="5eeca-154">Mapitags.h</span></span>
  
> <span data-ttu-id="5eeca-155">Contient les définitions des propriétés figurant en tant que noms de substitution.</span><span class="sxs-lookup"><span data-stu-id="5eeca-155">Contains definitions of properties listed as alternate names.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="5eeca-156">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="5eeca-156">See also</span></span>



[<span data-ttu-id="5eeca-157">Propriétés MAPI</span><span class="sxs-lookup"><span data-stu-id="5eeca-157">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="5eeca-158">Propriétés canoniques MAPI</span><span class="sxs-lookup"><span data-stu-id="5eeca-158">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="5eeca-159">Mappage des noms de propriétés canoniques aux noms MAPI</span><span class="sxs-lookup"><span data-stu-id="5eeca-159">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="5eeca-160">Mappage des noms MAPI aux noms de propriétés canoniques</span><span class="sxs-lookup"><span data-stu-id="5eeca-160">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

