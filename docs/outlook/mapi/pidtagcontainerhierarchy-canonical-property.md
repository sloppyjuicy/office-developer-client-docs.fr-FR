---
title: Propriété canonique PidTagContainerHierarchy
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- PidTagContainerHierarchy
api_type:
- HeaderDef
ms.assetid: 6917510d-ca1e-4049-9eab-09313753ecf0
description: Dernière modification le 09 mars 2015
ms.openlocfilehash: 2c9598b583ba62adc42d6fb2b904dfe4981286ff
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/23/2018
ms.locfileid: "22578107"
---
# <a name="pidtagcontainerhierarchy-canonical-property"></a><span data-ttu-id="c67b1-103">Propriété canonique PidTagContainerHierarchy</span><span class="sxs-lookup"><span data-stu-id="c67b1-103">PidTagContainerHierarchy Canonical Property</span></span>

  
  
<span data-ttu-id="c67b1-104">**S’applique à**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="c67b1-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="c67b1-105">Contient un objet table hiérarchie incorporé qui fournit des informations sur l’enfant conteneurs.</span><span class="sxs-lookup"><span data-stu-id="c67b1-105">Contains an embedded hierarchy table object that provides information about the child containers.</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="c67b1-106">Propriétés associées :</span><span class="sxs-lookup"><span data-stu-id="c67b1-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="c67b1-107">PR_CONTAINER_HIERARCHY</span><span class="sxs-lookup"><span data-stu-id="c67b1-107">PR_CONTAINER_HIERARCHY</span></span>  <br/> |
|<span data-ttu-id="c67b1-108">Identificateur :</span><span class="sxs-lookup"><span data-stu-id="c67b1-108">Identifier:</span></span>  <br/> |<span data-ttu-id="c67b1-109">0x360E</span><span class="sxs-lookup"><span data-stu-id="c67b1-109">0x360E</span></span>  <br/> |
|<span data-ttu-id="c67b1-110">Type de données :</span><span class="sxs-lookup"><span data-stu-id="c67b1-110">Data type:</span></span>  <br/> |<span data-ttu-id="c67b1-111">PT_OBJECT</span><span class="sxs-lookup"><span data-stu-id="c67b1-111">PT_OBJECT</span></span>  <br/> |
|<span data-ttu-id="c67b1-112">Domaine :</span><span class="sxs-lookup"><span data-stu-id="c67b1-112">Area:</span></span>  <br/> |<span data-ttu-id="c67b1-113">Container</span><span class="sxs-lookup"><span data-stu-id="c67b1-113">Container</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="c67b1-114">Remarques</span><span class="sxs-lookup"><span data-stu-id="c67b1-114">Remarks</span></span>

<span data-ttu-id="c67b1-115">Cette propriété peut être exclue dans les opérations [IMAPIProp::CopyTo](imapiprop-copyto.md) ou incluse dans les opérations de [IMAPIProp::CopyProps](imapiprop-copyprops.md) .</span><span class="sxs-lookup"><span data-stu-id="c67b1-115">This property can be excluded in [IMAPIProp::CopyTo](imapiprop-copyto.md) operations or included in [IMAPIProp::CopyProps](imapiprop-copyprops.md) operations.</span></span> <span data-ttu-id="c67b1-116">En tant que propriété de type **PT_OBJECT**, il ne peut pas être récupéré par la méthode [IMAPIProp::GetProps](imapiprop-getprops.md) ; son contenu doit être accessible par la méthode [IMAPIProp::OpenProperty](imapiprop-openproperty.md) , qui demande l’identificateur d’interface IID_IMAPITable.</span><span class="sxs-lookup"><span data-stu-id="c67b1-116">As a property of type **PT_OBJECT**, it cannot be successfully retrieved by the [IMAPIProp::GetProps](imapiprop-getprops.md) method; its contents should be accessed by the [IMAPIProp::OpenProperty](imapiprop-openproperty.md) method, requesting the IID_IMAPITable interface identifier.</span></span> <span data-ttu-id="c67b1-117">Fournisseurs de services doivent signaler à la méthode [IMAPIProp::GetPropList](imapiprop-getproplist.md) s’il est défini, mais peut le signaler ou pas si elle n’est pas définie.</span><span class="sxs-lookup"><span data-stu-id="c67b1-117">Service providers must report it to the [IMAPIProp::GetPropList](imapiprop-getproplist.md) method if it is set, but can optionally report it or not if it is not set.</span></span> 
  
<span data-ttu-id="c67b1-118">Pour récupérer le contenu du tableau, une application cliente doit appeler la méthode [IMAPIContainer::GetHierarchyTable](imapicontainer-gethierarchytable.md) .</span><span class="sxs-lookup"><span data-stu-id="c67b1-118">To retrieve table contents, a client application should call the [IMAPIContainer::GetHierarchyTable](imapicontainer-gethierarchytable.md) method.</span></span> <span data-ttu-id="c67b1-119">Pour plus d’informations, voir les [Tables de hiérarchie](hierarchy-tables.md).</span><span class="sxs-lookup"><span data-stu-id="c67b1-119">For more information, see [Hierarchy Tables](hierarchy-tables.md).</span></span> 
  
 <span data-ttu-id="c67b1-120">**PR_CONTAINER_CONTENTS** ([PidTagContainerContents](pidtagcontainercontents-canonical-property.md)), **PR_FOLDER_ASSOCIATED_CONTENTS** ([PidTagFolderAssociatedContents](pidtagfolderassociatedcontents-canonical-property.md)) et cette propriété sont similaires dans l’utilisation.</span><span class="sxs-lookup"><span data-stu-id="c67b1-120">**PR_CONTAINER_CONTENTS** ([PidTagContainerContents](pidtagcontainercontents-canonical-property.md)), **PR_FOLDER_ASSOCIATED_CONTENTS** ([PidTagFolderAssociatedContents](pidtagfolderassociatedcontents-canonical-property.md)), and this property are similar in usage.</span></span> <span data-ttu-id="c67b1-121">Plusieurs propriétés MAPI fournissent l’accès aux tables :</span><span class="sxs-lookup"><span data-stu-id="c67b1-121">Several MAPI properties provide access to tables:</span></span> 
  
|<span data-ttu-id="c67b1-122">**Propriété**</span><span class="sxs-lookup"><span data-stu-id="c67b1-122">**Property**</span></span>|<span data-ttu-id="c67b1-123">**Table**</span><span class="sxs-lookup"><span data-stu-id="c67b1-123">**Table**</span></span>|
|:-----|:-----|
|<span data-ttu-id="c67b1-124">**PR_CONTAINER_CONTENTS** ([PidTagContainerContents](pidtagcontainercontents-canonical-property.md))</span><span class="sxs-lookup"><span data-stu-id="c67b1-124">**PR_CONTAINER_CONTENTS** ([PidTagContainerContents](pidtagcontainercontents-canonical-property.md))</span></span>  <br/> |<span data-ttu-id="c67b1-125">Table des matières</span><span class="sxs-lookup"><span data-stu-id="c67b1-125">Contents table</span></span>  <br/> |
|<span data-ttu-id="c67b1-126">**PR_CONTAINER_HIERARCHY**</span><span class="sxs-lookup"><span data-stu-id="c67b1-126">**PR_CONTAINER_HIERARCHY**</span></span> <br/> |<span data-ttu-id="c67b1-127">Table de hiérarchie</span><span class="sxs-lookup"><span data-stu-id="c67b1-127">Hierarchy table</span></span>  <br/> |
|<span data-ttu-id="c67b1-128">**PR_FOLDER_ASSOCIATED_CONTENTS** ([PidTagFolderAssociatedContents](pidtagfolderassociatedcontents-canonical-property.md))</span><span class="sxs-lookup"><span data-stu-id="c67b1-128">**PR_FOLDER_ASSOCIATED_CONTENTS** ([PidTagFolderAssociatedContents](pidtagfolderassociatedcontents-canonical-property.md))</span></span>  <br/> |<span data-ttu-id="c67b1-129">Tableau contenu associé</span><span class="sxs-lookup"><span data-stu-id="c67b1-129">Associated contents table</span></span>  <br/> |
|<span data-ttu-id="c67b1-130">**PR_MESSAGE_ATTACHMENTS** ([PidTagMessageAttachments](pidtagmessageattachments-canonical-property.md))</span><span class="sxs-lookup"><span data-stu-id="c67b1-130">**PR_MESSAGE_ATTACHMENTS** ([PidTagMessageAttachments](pidtagmessageattachments-canonical-property.md))</span></span>  <br/> |<span data-ttu-id="c67b1-131">Table des pièces jointes</span><span class="sxs-lookup"><span data-stu-id="c67b1-131">Attachment table</span></span>  <br/> |
|<span data-ttu-id="c67b1-132">**PR_MESSAGE_RECIPIENTS** ([PidTagMessageRecipients](pidtagmessagerecipients-canonical-property.md))</span><span class="sxs-lookup"><span data-stu-id="c67b1-132">**PR_MESSAGE_RECIPIENTS** ([PidTagMessageRecipients](pidtagmessagerecipients-canonical-property.md))</span></span>  <br/> |<span data-ttu-id="c67b1-133">Table des destinataires</span><span class="sxs-lookup"><span data-stu-id="c67b1-133">Recipient table</span></span>  <br/> |
   
## <a name="related-resources"></a><span data-ttu-id="c67b1-134">Ressources connexes</span><span class="sxs-lookup"><span data-stu-id="c67b1-134">Related resources</span></span>

### <a name="protocol-specifications"></a><span data-ttu-id="c67b1-135">Spécifications du protocole</span><span class="sxs-lookup"><span data-stu-id="c67b1-135">Protocol specifications</span></span>

<span data-ttu-id="c67b1-136">[[MS-OXPROPS]](http://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="c67b1-136">[[MS-OXPROPS]](http://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="c67b1-137">Fournit des références aux spécifications du protocole Exchange Server associées.</span><span class="sxs-lookup"><span data-stu-id="c67b1-137">Provides references to related Exchange Server protocol specifications.</span></span>
    
<span data-ttu-id="c67b1-138">[[MS-OXCFXICS]](http://msdn.microsoft.com/library/b9752f3d-d50d-44b8-9e6b-608a117c8532%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="c67b1-138">[[MS-OXCFXICS]](http://msdn.microsoft.com/library/b9752f3d-d50d-44b8-9e6b-608a117c8532%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="c67b1-139">Gère l’ordre et le flux pour les transferts de données entre un client et le serveur.</span><span class="sxs-lookup"><span data-stu-id="c67b1-139">Handles the order and flow for data transfers between a client and server.</span></span>
    
<span data-ttu-id="c67b1-140">[[MS-OXCICAL]](http://msdn.microsoft.com/library/a685a040-5b69-4c84-b084-795113fb4012%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="c67b1-140">[[MS-OXCICAL]](http://msdn.microsoft.com/library/a685a040-5b69-4c84-b084-795113fb4012%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="c67b1-141">La conversion entre IETF RFC2445, RFC2446, RFC2447 et rendez-vous et des objets de la conférence.</span><span class="sxs-lookup"><span data-stu-id="c67b1-141">Converts between IETF RFC2445, RFC2446, and RFC2447, and appointment and meeting objects.</span></span>
    
### <a name="header-files"></a><span data-ttu-id="c67b1-142">Fichiers d’en-tête</span><span class="sxs-lookup"><span data-stu-id="c67b1-142">Header files</span></span>

<span data-ttu-id="c67b1-143">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="c67b1-143">Mapidefs.h</span></span>
  
> <span data-ttu-id="c67b1-144">Fournit des définitions de type de données.</span><span class="sxs-lookup"><span data-stu-id="c67b1-144">Provides data type definitions.</span></span>
    
<span data-ttu-id="c67b1-145">MAPITAGS.h</span><span class="sxs-lookup"><span data-stu-id="c67b1-145">Mapitags.h</span></span>
  
> <span data-ttu-id="c67b1-146">Contient les définitions des propriétés répertoriées en tant que d’autres noms.</span><span class="sxs-lookup"><span data-stu-id="c67b1-146">Contains definitions of properties listed as alternate names.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="c67b1-147">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="c67b1-147">See also</span></span>



[<span data-ttu-id="c67b1-148">Propriétés MAPI</span><span class="sxs-lookup"><span data-stu-id="c67b1-148">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="c67b1-149">Propriétés canoniques MAPI</span><span class="sxs-lookup"><span data-stu-id="c67b1-149">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="c67b1-150">Mappage des noms de propriétés canoniques aux noms MAPI</span><span class="sxs-lookup"><span data-stu-id="c67b1-150">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="c67b1-151">Mappage des noms MAPI aux noms de propriétés canoniques</span><span class="sxs-lookup"><span data-stu-id="c67b1-151">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

