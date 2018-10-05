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
description: Dernière modification le 9 mars 2015
ms.openlocfilehash: d30088ba7398669228a18be825323afa800ec536
ms.sourcegitcommit: ef717c65d8dd41ababffb01eafc443c79950aed4
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 10/04/2018
ms.locfileid: "25397841"
---
# <a name="pidtagmessagerecipients-canonical-property"></a><span data-ttu-id="e24c3-103">Propriété canonique PidTagMessageRecipients</span><span class="sxs-lookup"><span data-stu-id="e24c3-103">PidTagMessageRecipients Canonical Property</span></span>

  
  
<span data-ttu-id="e24c3-104">**S’applique à** : Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="e24c3-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="e24c3-105">Contient un tableau de restrictions qui peuvent être appliquées à une table des matières pour rechercher tous les messages qui contiennent des destinataires sous-objets répondant aux restrictions.</span><span class="sxs-lookup"><span data-stu-id="e24c3-105">Contains a table of restrictions that can be applied to a contents table to find all messages that contain recipient subobjects that meet the restrictions.</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="e24c3-106">Propriétés associées :</span><span class="sxs-lookup"><span data-stu-id="e24c3-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="e24c3-107">PR_MESSAGE_RECIPIENTS</span><span class="sxs-lookup"><span data-stu-id="e24c3-107">PR_MESSAGE_RECIPIENTS</span></span>  <br/> |
|<span data-ttu-id="e24c3-108">Identificateur :</span><span class="sxs-lookup"><span data-stu-id="e24c3-108">Identifier:</span></span>  <br/> |<span data-ttu-id="e24c3-109">0x0E12</span><span class="sxs-lookup"><span data-stu-id="e24c3-109">0x0E12</span></span>  <br/> |
|<span data-ttu-id="e24c3-110">Type de données :</span><span class="sxs-lookup"><span data-stu-id="e24c3-110">Data type:</span></span>  <br/> |<span data-ttu-id="e24c3-111">PT_OBJECT</span><span class="sxs-lookup"><span data-stu-id="e24c3-111">PT_OBJECT</span></span>  <br/> |
|<span data-ttu-id="e24c3-112">Domaine :</span><span class="sxs-lookup"><span data-stu-id="e24c3-112">Area:</span></span>  <br/> |<span data-ttu-id="e24c3-113">Général de messagerie</span><span class="sxs-lookup"><span data-stu-id="e24c3-113">General messaging</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="e24c3-114">Remarques</span><span class="sxs-lookup"><span data-stu-id="e24c3-114">Remarks</span></span>

<span data-ttu-id="e24c3-115">Cette propriété peut être exclue dans les opérations [IMAPIProp::CopyTo](imapiprop-copyto.md) ou incluse dans les opérations de [IMAPIProp::CopyProps](imapiprop-copyprops.md) .</span><span class="sxs-lookup"><span data-stu-id="e24c3-115">This property can be excluded in [IMAPIProp::CopyTo](imapiprop-copyto.md) operations or included in [IMAPIProp::CopyProps](imapiprop-copyprops.md) operations.</span></span> <span data-ttu-id="e24c3-116">En tant que propriété de type **PT_OBJECT**, il ne peut pas être récupéré par la méthode [IMAPIProp::GetProps](imapiprop-getprops.md) .</span><span class="sxs-lookup"><span data-stu-id="e24c3-116">As a property of type **PT_OBJECT**, it cannot be successfully retrieved by the [IMAPIProp::GetProps](imapiprop-getprops.md) method.</span></span> <span data-ttu-id="e24c3-117">Son contenu doit être accessible par la méthode [IMAPIProp::OpenProperty](imapiprop-openproperty.md) , qui demande l’identificateur d’interface **IID_IMAPITable** .</span><span class="sxs-lookup"><span data-stu-id="e24c3-117">Its contents should be accessed by the [IMAPIProp::OpenProperty](imapiprop-openproperty.md) method, requesting the **IID_IMAPITable** interface identifier.</span></span> <span data-ttu-id="e24c3-118">Fournisseurs de services doivent signaler à la méthode [IMAPIProp::GetPropList](imapiprop-getproplist.md) si elle est définie, mais peut le signaler ou pas si elle n’est pas définie.</span><span class="sxs-lookup"><span data-stu-id="e24c3-118">Service providers must report it to the [IMAPIProp::GetPropList](imapiprop-getproplist.md) method if it is set, but may optionally report it or not if it is not set.</span></span> 
  
<span data-ttu-id="e24c3-119">Pour récupérer le contenu du tableau, une application cliente doit appeler la méthode [IMessage::GetRecipientTable](imessage-getrecipienttable.md) .</span><span class="sxs-lookup"><span data-stu-id="e24c3-119">To retrieve table contents, a client application should call the [IMessage::GetRecipientTable](imessage-getrecipienttable.md) method.</span></span> 
  
<span data-ttu-id="e24c3-120">Cette propriété peut être utilisée pour la restriction sous-objet en le définissant dans la structure [SSubRestriction](ssubrestriction.md) .</span><span class="sxs-lookup"><span data-stu-id="e24c3-120">This property can be used for subobject restriction by specifying it in the [SSubRestriction](ssubrestriction.md) structure.</span></span> <span data-ttu-id="e24c3-121">Cela permet à un client limiter l’affichage d’un conteneur pour les messages avec des destinataires de réunion critère donné.</span><span class="sxs-lookup"><span data-stu-id="e24c3-121">This enables a client to limit the view of a container to messages with recipients meeting given criteria.</span></span> <span data-ttu-id="e24c3-122">Un message satisfait aux conditions requises pour l’affichage si la restriction sous-objet satisfait au moins une ligne dans sa table destinataire, c'est-à-dire, un seul destinataire.</span><span class="sxs-lookup"><span data-stu-id="e24c3-122">A message qualifies for viewing if at least one row in its recipient table, that is, one recipient satisfies the subobject restriction.</span></span> 
  
 <span data-ttu-id="e24c3-123">**Remarque** Utilisation des résultats de restriction sous-objet est l’équivalent d’une [IMAPISession::OpenEntry](imapisession-openentry.md) des appels sur chaque message dans le tableau.</span><span class="sxs-lookup"><span data-stu-id="e24c3-123">**Note** Using subobject restriction results is the equivalent of an [IMAPISession::OpenEntry](imapisession-openentry.md) call on every message in the table.</span></span> <span data-ttu-id="e24c3-124">En fonction de l’application cliente et le nombre de messages à rechercher, il peut affecter les performances.</span><span class="sxs-lookup"><span data-stu-id="e24c3-124">Depending on the client application and the number of messages to be searched, it can affect performance.</span></span> 
  
<span data-ttu-id="e24c3-125">La propriété **PR_MESSAGE_ATTACHMENTS** ([PidTagMessageAttachments](pidtagmessageattachments-canonical-property.md)) et cette propriété sont similaires d’utilisation.</span><span class="sxs-lookup"><span data-stu-id="e24c3-125">The **PR_MESSAGE_ATTACHMENTS** ([PidTagMessageAttachments](pidtagmessageattachments-canonical-property.md)) property and this property are similar in usage.</span></span> <span data-ttu-id="e24c3-126">Plusieurs propriétés MAPI fournissent l’accès aux tables :</span><span class="sxs-lookup"><span data-stu-id="e24c3-126">Several MAPI properties provide access to tables:</span></span> 
  
|<span data-ttu-id="e24c3-127">**Propriété**</span><span class="sxs-lookup"><span data-stu-id="e24c3-127">**Property**</span></span>|<span data-ttu-id="e24c3-128">**Table**</span><span class="sxs-lookup"><span data-stu-id="e24c3-128">**Table**</span></span>|
|:-----|:-----|
|<span data-ttu-id="e24c3-129">**PR_CONTAINER_CONTENTS** ([PidTagContainerContents](pidtagcontainercontents-canonical-property.md))</span><span class="sxs-lookup"><span data-stu-id="e24c3-129">**PR_CONTAINER_CONTENTS** ([PidTagContainerContents](pidtagcontainercontents-canonical-property.md))</span></span>  <br/> |<span data-ttu-id="e24c3-130">Table des matières</span><span class="sxs-lookup"><span data-stu-id="e24c3-130">Contents table</span></span>  <br/> |
|<span data-ttu-id="e24c3-131">**PR_CONTAINER_HIERARCHY** ([PidTagContainerHierarchy](pidtagcontainerhierarchy-canonical-property.md))</span><span class="sxs-lookup"><span data-stu-id="e24c3-131">**PR_CONTAINER_HIERARCHY** ([PidTagContainerHierarchy](pidtagcontainerhierarchy-canonical-property.md))</span></span>  <br/> |<span data-ttu-id="e24c3-132">Table de hiérarchie</span><span class="sxs-lookup"><span data-stu-id="e24c3-132">Hierarchy table</span></span>  <br/> |
|<span data-ttu-id="e24c3-133">**PR_FOLDER_ASSOCIATED_CONTENTS** ([PidTagFolderAssociatedContents](pidtagfolderassociatedcontents-canonical-property.md))</span><span class="sxs-lookup"><span data-stu-id="e24c3-133">**PR_FOLDER_ASSOCIATED_CONTENTS** ([PidTagFolderAssociatedContents](pidtagfolderassociatedcontents-canonical-property.md))</span></span>  <br/> |<span data-ttu-id="e24c3-134">Tableau contenu associé</span><span class="sxs-lookup"><span data-stu-id="e24c3-134">Associated contents table</span></span>  <br/> |
|<span data-ttu-id="e24c3-135">**PR_MESSAGE_ATTACHMENTS** ([PidTagMessageAttachments](pidtagmessageattachments-canonical-property.md))</span><span class="sxs-lookup"><span data-stu-id="e24c3-135">**PR_MESSAGE_ATTACHMENTS** ([PidTagMessageAttachments](pidtagmessageattachments-canonical-property.md))</span></span>  <br/> |<span data-ttu-id="e24c3-136">Table des pièces jointes</span><span class="sxs-lookup"><span data-stu-id="e24c3-136">Attachment table</span></span>  <br/> |
|<span data-ttu-id="e24c3-137">PR_MESSAGE_RECIPIENTS</span><span class="sxs-lookup"><span data-stu-id="e24c3-137">PR_MESSAGE_RECIPIENTS</span></span>  <br/> |<span data-ttu-id="e24c3-138">Table des destinataires</span><span class="sxs-lookup"><span data-stu-id="e24c3-138">Recipient table</span></span>  <br/> |
   
## <a name="related-resources"></a><span data-ttu-id="e24c3-139">Ressources connexes</span><span class="sxs-lookup"><span data-stu-id="e24c3-139">Related resources</span></span>

### <a name="protocol-specifications"></a><span data-ttu-id="e24c3-140">Spécifications du protocole</span><span class="sxs-lookup"><span data-stu-id="e24c3-140">Protocol specifications</span></span>

<span data-ttu-id="e24c3-141">[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="e24c3-141">[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="e24c3-142">Fournit des références aux spécifications du protocole Exchange Server associées.</span><span class="sxs-lookup"><span data-stu-id="e24c3-142">Provides references to related Exchange Server protocol specifications.</span></span>
    
<span data-ttu-id="e24c3-143">[[MS-OXCFXICS]](https://msdn.microsoft.com/library/b9752f3d-d50d-44b8-9e6b-608a117c8532%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="e24c3-143">[[MS-OXCFXICS]](https://msdn.microsoft.com/library/b9752f3d-d50d-44b8-9e6b-608a117c8532%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="e24c3-144">Gère l’ordre et le flux pour les transferts de données entre un client et le serveur.</span><span class="sxs-lookup"><span data-stu-id="e24c3-144">Handles the order and flow for data transfers between a client and server.</span></span>
    
<span data-ttu-id="e24c3-145">[[MS-OXCICAL]](https://msdn.microsoft.com/library/a685a040-5b69-4c84-b084-795113fb4012%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="e24c3-145">[[MS-OXCICAL]](https://msdn.microsoft.com/library/a685a040-5b69-4c84-b084-795113fb4012%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="e24c3-146">La conversion entre IETF RFC2445, RFC2446, RFC2447 et rendez-vous et des objets de la conférence.</span><span class="sxs-lookup"><span data-stu-id="e24c3-146">Converts between IETF RFC2445, RFC2446, and RFC2447, and appointment and meeting objects.</span></span>
    
<span data-ttu-id="e24c3-147">[[MS-OXCSPAM]](https://msdn.microsoft.com/library/522f8587-4aed-4cd6-831b-40bd87862189%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="e24c3-147">[[MS-OXCSPAM]](https://msdn.microsoft.com/library/522f8587-4aed-4cd6-831b-40bd87862189%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="e24c3-148">Permet la gestion des listes autoriser/bloquer et la détermination des messages de courrier indésirable.</span><span class="sxs-lookup"><span data-stu-id="e24c3-148">Enables the handling of allow/block lists and the determination of junk email messages.</span></span>
    
<span data-ttu-id="e24c3-149">[[MS-OXTNEF]](https://msdn.microsoft.com/library/1f0544d7-30b7-4194-b58f-adc82f3763bb%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="e24c3-149">[[MS-OXTNEF]](https://msdn.microsoft.com/library/1f0544d7-30b7-4194-b58f-adc82f3763bb%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="e24c3-150">Code et décode des objets message et la pièce jointe à une représentation sous forme de flux efficace.</span><span class="sxs-lookup"><span data-stu-id="e24c3-150">Encodes and decodes message and attachment objects to an efficient stream representation.</span></span>
    
### <a name="header-files"></a><span data-ttu-id="e24c3-151">Fichiers d’en-tête</span><span class="sxs-lookup"><span data-stu-id="e24c3-151">Header files</span></span>

<span data-ttu-id="e24c3-152">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="e24c3-152">Mapidefs.h</span></span>
  
> <span data-ttu-id="e24c3-153">Fournit des définitions de type de données.</span><span class="sxs-lookup"><span data-stu-id="e24c3-153">Provides data type definitions.</span></span>
    
<span data-ttu-id="e24c3-154">MAPITAGS.h</span><span class="sxs-lookup"><span data-stu-id="e24c3-154">Mapitags.h</span></span>
  
> <span data-ttu-id="e24c3-155">Contient les définitions des propriétés répertoriées en tant que d’autres noms.</span><span class="sxs-lookup"><span data-stu-id="e24c3-155">Contains definitions of properties listed as alternate names.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="e24c3-156">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="e24c3-156">See also</span></span>



[<span data-ttu-id="e24c3-157">Propriétés MAPI</span><span class="sxs-lookup"><span data-stu-id="e24c3-157">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="e24c3-158">Propriétés canoniques MAPI</span><span class="sxs-lookup"><span data-stu-id="e24c3-158">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="e24c3-159">Mappage des noms de propriétés canoniques aux noms MAPI</span><span class="sxs-lookup"><span data-stu-id="e24c3-159">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="e24c3-160">Mappage des noms MAPI aux noms de propriétés canoniques</span><span class="sxs-lookup"><span data-stu-id="e24c3-160">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

