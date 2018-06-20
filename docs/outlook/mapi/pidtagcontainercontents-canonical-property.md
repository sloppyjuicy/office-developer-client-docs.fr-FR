---
title: Propriété canonique PidTagContainerContents
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- PidTagContainerContents
api_type:
- HeaderDef
ms.assetid: 66dbe65a-b9fd-41d5-946f-ec8888363043
description: 'Derni�re modification�: lundi 9 mars 2015'
ms.openlocfilehash: c2979a0825ad6c62dbbb7931255501e90d8450a5
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19785839"
---
# <a name="pidtagcontainercontents-canonical-property"></a><span data-ttu-id="d4d51-103">Propriété canonique PidTagContainerContents</span><span class="sxs-lookup"><span data-stu-id="d4d51-103">PidTagContainerContents Canonical Property</span></span>

  
  
<span data-ttu-id="d4d51-104">**S’applique à**: Outlook</span><span class="sxs-lookup"><span data-stu-id="d4d51-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="d4d51-105">Contient un objet incorporé contenu tableau qui fournit des informations relatives à un conteneur.</span><span class="sxs-lookup"><span data-stu-id="d4d51-105">Contains an embedded contents table object that provides information about a container.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="d4d51-106">Propriétés associées :</span><span class="sxs-lookup"><span data-stu-id="d4d51-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="d4d51-107">PR_CONTAINER_CONTENTS</span><span class="sxs-lookup"><span data-stu-id="d4d51-107">PR_CONTAINER_CONTENTS</span></span>  <br/> |
|<span data-ttu-id="d4d51-108">Identificateur :</span><span class="sxs-lookup"><span data-stu-id="d4d51-108">Identifier:</span></span>  <br/> |<span data-ttu-id="d4d51-109">0x360F</span><span class="sxs-lookup"><span data-stu-id="d4d51-109">0x360F</span></span>  <br/> |
|<span data-ttu-id="d4d51-110">Type de données :</span><span class="sxs-lookup"><span data-stu-id="d4d51-110">Data type:</span></span>  <br/> |<span data-ttu-id="d4d51-111">PT_OBJECT</span><span class="sxs-lookup"><span data-stu-id="d4d51-111">PT_OBJECT</span></span>  <br/> |
|<span data-ttu-id="d4d51-112">Zone :</span><span class="sxs-lookup"><span data-stu-id="d4d51-112">Area:</span></span>  <br/> |<span data-ttu-id="d4d51-113">Container</span><span class="sxs-lookup"><span data-stu-id="d4d51-113">Container</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="d4d51-114">Remarques</span><span class="sxs-lookup"><span data-stu-id="d4d51-114">Remarks</span></span>

<span data-ttu-id="d4d51-115">Cette propriété peut être exclue dans les opérations [IMAPIProp::CopyTo](imapiprop-copyto.md) ou incluse dans les opérations de [IMAPIProp::CopyProps](imapiprop-copyprops.md) .</span><span class="sxs-lookup"><span data-stu-id="d4d51-115">This property can be excluded in [IMAPIProp::CopyTo](imapiprop-copyto.md) operations or included in [IMAPIProp::CopyProps](imapiprop-copyprops.md) operations.</span></span> <span data-ttu-id="d4d51-116">En tant que propriété de type PT_OBJECT, il ne peut pas être récupéré par la méthode [IMAPIProp::GetProps](imapiprop-getprops.md) ; son contenu doit être accessible par la méthode [IMAPIProp::OpenProperty](imapiprop-openproperty.md) , qui demande l’identificateur d’interface IID_IMAPITable.</span><span class="sxs-lookup"><span data-stu-id="d4d51-116">As a property of type PT_OBJECT, it cannot be successfully retrieved by the [IMAPIProp::GetProps](imapiprop-getprops.md) method; its contents should be accessed by the [IMAPIProp::OpenProperty](imapiprop-openproperty.md) method, requesting the IID_IMAPITable interface identifier.</span></span> <span data-ttu-id="d4d51-117">Fournisseurs de services doivent signaler à la méthode [IMAPIProp::GetPropList](imapiprop-getproplist.md) s’il est défini, mais peut le signaler ou pas si elle n’est pas définie.</span><span class="sxs-lookup"><span data-stu-id="d4d51-117">Service providers must report it to the [IMAPIProp::GetPropList](imapiprop-getproplist.md) method if it is set, but can optionally report it or not if it is not set.</span></span> 
  
<span data-ttu-id="d4d51-118">Pour récupérer le contenu du tableau, une application cliente doit appeler la méthode [IMAPIContainer::GetContentsTable](imapicontainer-getcontentstable.md) .</span><span class="sxs-lookup"><span data-stu-id="d4d51-118">To retrieve table contents, a client application should call the [IMAPIContainer::GetContentsTable](imapicontainer-getcontentstable.md) method.</span></span> <span data-ttu-id="d4d51-119">For more information, see [Tables des mati�res](contents-tables.md).</span><span class="sxs-lookup"><span data-stu-id="d4d51-119">For more information, see [Contents Tables](contents-tables.md).</span></span> 
  
<span data-ttu-id="d4d51-120">Cette propriété, **PR_CONTAINER_HIERARCHY** ([PidTagContainerHierarchy](pidtagcontainerhierarchy-canonical-property.md)) et **PR_FOLDER_ASSOCIATED_CONTENTS** ([PidTagFolderAssociatedContents](pidtagfolderassociatedcontents-canonical-property.md)) sont similaires d’utilisation.</span><span class="sxs-lookup"><span data-stu-id="d4d51-120">This property, **PR_CONTAINER_HIERARCHY** ([PidTagContainerHierarchy](pidtagcontainerhierarchy-canonical-property.md)) , and **PR_FOLDER_ASSOCIATED_CONTENTS** ([PidTagFolderAssociatedContents](pidtagfolderassociatedcontents-canonical-property.md)) are similar in usage.</span></span> <span data-ttu-id="d4d51-121">Plusieurs propriétés MAPI fournissent l’accès aux tables :</span><span class="sxs-lookup"><span data-stu-id="d4d51-121">Several MAPI properties provide access to tables:</span></span> 
  
|<span data-ttu-id="d4d51-122">**Propriété**</span><span class="sxs-lookup"><span data-stu-id="d4d51-122">**Property**</span></span>|<span data-ttu-id="d4d51-123">**Table**</span><span class="sxs-lookup"><span data-stu-id="d4d51-123">**Table**</span></span>|
|:-----|:-----|
|<span data-ttu-id="d4d51-124">PidTagContainerContents</span><span class="sxs-lookup"><span data-stu-id="d4d51-124">PidTagContainerContents</span></span>  <br/> |<span data-ttu-id="d4d51-125">Table des matières</span><span class="sxs-lookup"><span data-stu-id="d4d51-125">Contents table</span></span>  <br/> |
|<span data-ttu-id="d4d51-126">**PR_CONTAINER_HIERARCHY** ([PidTagContainerHierarchy](pidtagcontainerhierarchy-canonical-property.md))</span><span class="sxs-lookup"><span data-stu-id="d4d51-126">**PR_CONTAINER_HIERARCHY** ([PidTagContainerHierarchy](pidtagcontainerhierarchy-canonical-property.md))</span></span>  <br/> |<span data-ttu-id="d4d51-127">Table de hiérarchie</span><span class="sxs-lookup"><span data-stu-id="d4d51-127">Hierarchy table</span></span>  <br/> |
|<span data-ttu-id="d4d51-128">**PR_FOLDER_ASSOCIATED_CONTENTS** ([PidTagFolderAssociatedContents](pidtagfolderassociatedcontents-canonical-property.md))</span><span class="sxs-lookup"><span data-stu-id="d4d51-128">**PR_FOLDER_ASSOCIATED_CONTENTS** ([PidTagFolderAssociatedContents](pidtagfolderassociatedcontents-canonical-property.md))</span></span>  <br/> |<span data-ttu-id="d4d51-129">Tableau contenu associé</span><span class="sxs-lookup"><span data-stu-id="d4d51-129">Associated contents table</span></span>  <br/> |
|<span data-ttu-id="d4d51-130">**PR_MESSAGE_ATTACHMENTS** ([PidTagMessageAttachments](pidtagmessageattachments-canonical-property.md))</span><span class="sxs-lookup"><span data-stu-id="d4d51-130">**PR_MESSAGE_ATTACHMENTS** ([PidTagMessageAttachments](pidtagmessageattachments-canonical-property.md))</span></span>  <br/> |<span data-ttu-id="d4d51-131">Table des pièces jointes</span><span class="sxs-lookup"><span data-stu-id="d4d51-131">Attachment table</span></span>  <br/> |
|<span data-ttu-id="d4d51-132">**PR_MESSAGE_RECIPIENTS** ([PidTagMessageRecipients](pidtagmessagerecipients-canonical-property.md))</span><span class="sxs-lookup"><span data-stu-id="d4d51-132">**PR_MESSAGE_RECIPIENTS** ([PidTagMessageRecipients](pidtagmessagerecipients-canonical-property.md))</span></span>  <br/> |<span data-ttu-id="d4d51-133">Table des destinataires</span><span class="sxs-lookup"><span data-stu-id="d4d51-133">Recipient table</span></span>  <br/> |
   
## <a name="related-resources"></a><span data-ttu-id="d4d51-134">Ressources connexes</span><span class="sxs-lookup"><span data-stu-id="d4d51-134">Related resources</span></span>

### <a name="protocol-specifications"></a><span data-ttu-id="d4d51-135">Spécifications du protocole</span><span class="sxs-lookup"><span data-stu-id="d4d51-135">Protocol specifications</span></span>

<span data-ttu-id="d4d51-136">[[MS-OXPROPS]](http://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="d4d51-136">[[MS-OXPROPS]](http://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="d4d51-137">Fournit des références aux spécifications du protocole Exchange Server associées.</span><span class="sxs-lookup"><span data-stu-id="d4d51-137">Provides references to related Exchange Server protocol specifications.</span></span>
    
<span data-ttu-id="d4d51-138">[[MS-OXOABK]](http://msdn.microsoft.com/library/f4cf9b4c-9232-4506-9e71-2270de217614%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="d4d51-138">[[MS-OXOABK]](http://msdn.microsoft.com/library/f4cf9b4c-9232-4506-9e71-2270de217614%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="d4d51-139">Spécifie les propriétés et opérations pour les listes des utilisateurs, des contacts, des groupes et des ressources.</span><span class="sxs-lookup"><span data-stu-id="d4d51-139">Specifies the properties and operations for lists of users, contacts, groups, and resources.</span></span>
    
### <a name="header-files"></a><span data-ttu-id="d4d51-140">Fichiers d’en-tête</span><span class="sxs-lookup"><span data-stu-id="d4d51-140">Header files</span></span>

<span data-ttu-id="d4d51-141">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="d4d51-141">Mapidefs.h</span></span>
  
> <span data-ttu-id="d4d51-142">Fournit des définitions de type de données.</span><span class="sxs-lookup"><span data-stu-id="d4d51-142">Provides data type definitions.</span></span>
    
<span data-ttu-id="d4d51-143">MAPITAGS.h</span><span class="sxs-lookup"><span data-stu-id="d4d51-143">Mapitags.h</span></span>
  
> <span data-ttu-id="d4d51-144">Contient les définitions des propriétés répertoriées en tant que d’autres noms.</span><span class="sxs-lookup"><span data-stu-id="d4d51-144">Contains definitions of properties listed as alternate names.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="d4d51-145">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="d4d51-145">See also</span></span>



[<span data-ttu-id="d4d51-146">Propriétés MAPI</span><span class="sxs-lookup"><span data-stu-id="d4d51-146">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="d4d51-147">Propriétés canoniques MAPI</span><span class="sxs-lookup"><span data-stu-id="d4d51-147">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="d4d51-148">Mappage de noms de propriété canonique aux noms MAPI</span><span class="sxs-lookup"><span data-stu-id="d4d51-148">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="d4d51-149">Mappage de noms MAPI pour les noms de propriété canonique</span><span class="sxs-lookup"><span data-stu-id="d4d51-149">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

