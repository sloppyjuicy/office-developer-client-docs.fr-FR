---
title: Propriété canonique PidTagFolderAssociatedContents
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- PidTagFolderAssociatedContents
api_type:
- HeaderDef
ms.assetid: d1f3f589-dc2d-4538-a13f-278dad29bcc7
description: 'Derni�re modification�: lundi 9 mars 2015'
ms.openlocfilehash: fe6395029e312a19bce6252e73b4616bb0aa0851
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19785996"
---
# <a name="pidtagfolderassociatedcontents-canonical-property"></a><span data-ttu-id="84035-103">Propriété canonique PidTagFolderAssociatedContents</span><span class="sxs-lookup"><span data-stu-id="84035-103">PidTagFolderAssociatedContents Canonical Property</span></span>

  
  
<span data-ttu-id="84035-104">**S’applique à**: Outlook</span><span class="sxs-lookup"><span data-stu-id="84035-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="84035-105">Contient un objet incorporé contenu tableau qui fournit des informations sur la table de contenu associée.</span><span class="sxs-lookup"><span data-stu-id="84035-105">Contains an embedded contents table object that provides information about the associated contents table.</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="84035-106">Propriétés associées :</span><span class="sxs-lookup"><span data-stu-id="84035-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="84035-107">PR_FOLDER_ASSOCIATED_CONTENTS</span><span class="sxs-lookup"><span data-stu-id="84035-107">PR_FOLDER_ASSOCIATED_CONTENTS</span></span>  <br/> |
|<span data-ttu-id="84035-108">Identificateur :</span><span class="sxs-lookup"><span data-stu-id="84035-108">Identifier:</span></span>  <br/> |<span data-ttu-id="84035-109">0x3610</span><span class="sxs-lookup"><span data-stu-id="84035-109">0x3610</span></span>  <br/> |
|<span data-ttu-id="84035-110">Type de données :</span><span class="sxs-lookup"><span data-stu-id="84035-110">Data type:</span></span>  <br/> |<span data-ttu-id="84035-111">PT_OBJECT</span><span class="sxs-lookup"><span data-stu-id="84035-111">PT_OBJECT</span></span>  <br/> |
|<span data-ttu-id="84035-112">Zone :</span><span class="sxs-lookup"><span data-stu-id="84035-112">Area:</span></span>  <br/> |<span data-ttu-id="84035-113">Conteneur MAPI</span><span class="sxs-lookup"><span data-stu-id="84035-113">MAPI container</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="84035-114">Remarques</span><span class="sxs-lookup"><span data-stu-id="84035-114">Remarks</span></span>

<span data-ttu-id="84035-115">Le tableau contenu associé représente un sous-dossier qui n’apparaît pas dans la table des matières standard.</span><span class="sxs-lookup"><span data-stu-id="84035-115">The associated contents table represents a subfolder that does not appear in the standard contents table.</span></span> <span data-ttu-id="84035-116">Il contient les messages associés ou masqué, du dossier.</span><span class="sxs-lookup"><span data-stu-id="84035-116">It contains the folder's associated, or hidden, messages.</span></span> 
  
<span data-ttu-id="84035-117">Cette propriété peut être exclue dans les opérations [IMAPIProp::CopyTo](imapiprop-copyto.md) ou incluse dans les opérations de [IMAPIProp::CopyProps](imapiprop-copyprops.md) .</span><span class="sxs-lookup"><span data-stu-id="84035-117">This property can be excluded in [IMAPIProp::CopyTo](imapiprop-copyto.md) operations or included in [IMAPIProp::CopyProps](imapiprop-copyprops.md) operations.</span></span> <span data-ttu-id="84035-118">En tant que propriété de type **PT_OBJECT**, il ne peut pas être récupéré par la méthode [IMAPIProp::GetProps](imapiprop-getprops.md) ; son contenu doit être accessible par la méthode [IMAPIProp::OpenProperty](imapiprop-openproperty.md) , qui demande l’identificateur d’interface **IID_IMAPITable** .</span><span class="sxs-lookup"><span data-stu-id="84035-118">As a property of type **PT_OBJECT**, it cannot be successfully retrieved by the [IMAPIProp::GetProps](imapiprop-getprops.md) method; its contents should be accessed by the [IMAPIProp::OpenProperty](imapiprop-openproperty.md) method, requesting the **IID_IMAPITable** interface identifier.</span></span> <span data-ttu-id="84035-119">Fournisseurs de services doivent signaler à la méthode [IMAPIProp::GetPropList](imapiprop-getproplist.md) si elle est définie, mais peut le signaler ou pas si elle n’est pas définie.</span><span class="sxs-lookup"><span data-stu-id="84035-119">Service providers must report it to the [IMAPIProp::GetPropList](imapiprop-getproplist.md) method if it is set, but may optionally report it or not if it is not set.</span></span> 
  
<span data-ttu-id="84035-120">Pour récupérer le contenu du tableau, les applications clientes doivent appeler la méthode [IMAPIContainer::GetContentsTable](imapicontainer-getcontentstable.md) .</span><span class="sxs-lookup"><span data-stu-id="84035-120">To retrieve table contents, client applications should call the [IMAPIContainer::GetContentsTable](imapicontainer-getcontentstable.md) method.</span></span> <span data-ttu-id="84035-121">Pour plus d’informations sur les tables de contenu de dossier, voir [Tableaux de contenu](contents-tables.md) et [d’Afficher un tableau contenu de dossier](displaying-a-folder-contents-table.md).</span><span class="sxs-lookup"><span data-stu-id="84035-121">For more information on folder contents tables, see [Contents Tables](contents-tables.md) and [Displaying a Folder Contents Table](displaying-a-folder-contents-table.md).</span></span> 
  
<span data-ttu-id="84035-122">Cette propriété, la **PR_CONTAINER_CONTENTS** ([PidTagContainerContents](pidtagcontainercontents-canonical-property.md)) et **PR_CONTAINER_HIERARCHY** ([PidTagContainerHierarchy](pidtagcontainerhierarchy-canonical-property.md)) sont similaires dans l’utilisation.</span><span class="sxs-lookup"><span data-stu-id="84035-122">The **PR_CONTAINER_CONTENTS** ([PidTagContainerContents](pidtagcontainercontents-canonical-property.md)), **PR_CONTAINER_HIERARCHY** ([PidTagContainerHierarchy](pidtagcontainerhierarchy-canonical-property.md)), and this property are similar in usage.</span></span> <span data-ttu-id="84035-123">Plusieurs propriétés MAPI fournissent l’accès aux tables :</span><span class="sxs-lookup"><span data-stu-id="84035-123">Several MAPI properties provide access to tables:</span></span> 
  
|<span data-ttu-id="84035-124">**Propriété**</span><span class="sxs-lookup"><span data-stu-id="84035-124">**Property**</span></span>|<span data-ttu-id="84035-125">**Table**</span><span class="sxs-lookup"><span data-stu-id="84035-125">**Table**</span></span>|
|:-----|:-----|
|<span data-ttu-id="84035-126">**PR_CONTAINER_CONTENTS** ([PidTagContainerContents](pidtagcontainercontents-canonical-property.md))</span><span class="sxs-lookup"><span data-stu-id="84035-126">**PR_CONTAINER_CONTENTS** ([PidTagContainerContents](pidtagcontainercontents-canonical-property.md))</span></span>  <br/> |<span data-ttu-id="84035-127">Table des matières</span><span class="sxs-lookup"><span data-stu-id="84035-127">Contents table</span></span>  <br/> |
|<span data-ttu-id="84035-128">**PR_CONTAINER_HIERARCHY** ([PidTagContainerHierarchy](pidtagcontainerhierarchy-canonical-property.md))</span><span class="sxs-lookup"><span data-stu-id="84035-128">**PR_CONTAINER_HIERARCHY** ([PidTagContainerHierarchy](pidtagcontainerhierarchy-canonical-property.md))</span></span>  <br/> |<span data-ttu-id="84035-129">Table de hiérarchie</span><span class="sxs-lookup"><span data-stu-id="84035-129">Hierarchy table</span></span>  <br/> |
|<span data-ttu-id="84035-130">**PR_FOLDER_ASSOCIATED_CONTENTS**</span><span class="sxs-lookup"><span data-stu-id="84035-130">**PR_FOLDER_ASSOCIATED_CONTENTS**</span></span> <br/> |<span data-ttu-id="84035-131">Tableau contenu associé</span><span class="sxs-lookup"><span data-stu-id="84035-131">Associated contents table</span></span>  <br/> |
|<span data-ttu-id="84035-132">**PR_MESSAGE_ATTACHMENTS** ([PidTagMessageAttachments](pidtagmessageattachments-canonical-property.md))</span><span class="sxs-lookup"><span data-stu-id="84035-132">**PR_MESSAGE_ATTACHMENTS** ([PidTagMessageAttachments](pidtagmessageattachments-canonical-property.md))</span></span>  <br/> |<span data-ttu-id="84035-133">Table des pièces jointes</span><span class="sxs-lookup"><span data-stu-id="84035-133">Attachment table</span></span>  <br/> |
|<span data-ttu-id="84035-134">**PR_MESSAGE_RECIPIENTS** ([PidTagMessageRecipients](pidtagmessagerecipients-canonical-property.md))</span><span class="sxs-lookup"><span data-stu-id="84035-134">**PR_MESSAGE_RECIPIENTS** ([PidTagMessageRecipients](pidtagmessagerecipients-canonical-property.md))</span></span>  <br/> |<span data-ttu-id="84035-135">Table des destinataires</span><span class="sxs-lookup"><span data-stu-id="84035-135">Recipient table</span></span>  <br/> |
   
## <a name="related-resources"></a><span data-ttu-id="84035-136">Ressources connexes</span><span class="sxs-lookup"><span data-stu-id="84035-136">Related resources</span></span>

### <a name="protocol-specifications"></a><span data-ttu-id="84035-137">Spécifications du protocole</span><span class="sxs-lookup"><span data-stu-id="84035-137">Protocol specifications</span></span>

<span data-ttu-id="84035-138">[[MS-OXPROPS]](http://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="84035-138">[[MS-OXPROPS]](http://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="84035-139">Fournit des références aux spécifications du protocole Exchange Server associées.</span><span class="sxs-lookup"><span data-stu-id="84035-139">Provides references to related Exchange Server protocol specifications.</span></span>
    
<span data-ttu-id="84035-140">[[MS-OXCFXICS]](http://msdn.microsoft.com/library/b9752f3d-d50d-44b8-9e6b-608a117c8532%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="84035-140">[[MS-OXCFXICS]](http://msdn.microsoft.com/library/b9752f3d-d50d-44b8-9e6b-608a117c8532%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="84035-141">Gère l’ordre et le flux pour les transferts de données entre un client et le serveur.</span><span class="sxs-lookup"><span data-stu-id="84035-141">Handles the order and flow for data transfers between a client and server.</span></span>
    
<span data-ttu-id="84035-142">[[MS-OXCICAL]](http://msdn.microsoft.com/library/a685a040-5b69-4c84-b084-795113fb4012%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="84035-142">[[MS-OXCICAL]](http://msdn.microsoft.com/library/a685a040-5b69-4c84-b084-795113fb4012%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="84035-143">La conversion entre IETF RFC2445, RFC2446, RFC2447 et rendez-vous et des éléments de réunion.</span><span class="sxs-lookup"><span data-stu-id="84035-143">Converts between IETF RFC2445, RFC2446, and RFC2447, and appointment and meeting items.</span></span>
    
### <a name="header-files"></a><span data-ttu-id="84035-144">Fichiers d’en-tête</span><span class="sxs-lookup"><span data-stu-id="84035-144">Header files</span></span>

<span data-ttu-id="84035-145">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="84035-145">Mapidefs.h</span></span>
  
> <span data-ttu-id="84035-146">Fournit des définitions de type de données.</span><span class="sxs-lookup"><span data-stu-id="84035-146">Provides data type definitions.</span></span>
    
<span data-ttu-id="84035-147">MAPITAGS.h</span><span class="sxs-lookup"><span data-stu-id="84035-147">Mapitags.h</span></span>
  
> <span data-ttu-id="84035-148">Contient les définitions des propriétés répertoriées en tant que d’autres noms.</span><span class="sxs-lookup"><span data-stu-id="84035-148">Contains definitions of properties listed as alternate names.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="84035-149">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="84035-149">See also</span></span>



[<span data-ttu-id="84035-150">Propriété canonique PidTagAssociatedContentCount</span><span class="sxs-lookup"><span data-stu-id="84035-150">PidTagAssociatedContentCount Canonical Property</span></span>](pidtagassociatedcontentcount-canonical-property.md)


[<span data-ttu-id="84035-151">Propriétés MAPI</span><span class="sxs-lookup"><span data-stu-id="84035-151">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="84035-152">Propriétés canoniques MAPI</span><span class="sxs-lookup"><span data-stu-id="84035-152">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="84035-153">Mappage de noms de propriété canonique aux noms MAPI</span><span class="sxs-lookup"><span data-stu-id="84035-153">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="84035-154">Mappage de noms MAPI pour les noms de propriété canonique</span><span class="sxs-lookup"><span data-stu-id="84035-154">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

