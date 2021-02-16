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
description: Dernière modification le 9 mars 2015
ms.openlocfilehash: 5f0717c2a6def6f99f1e53217764e8820125b79d
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32283127"
---
# <a name="pidtagcontainercontents-canonical-property"></a><span data-ttu-id="253ca-103">Propriété canonique PidTagContainerContents</span><span class="sxs-lookup"><span data-stu-id="253ca-103">PidTagContainerContents Canonical Property</span></span>

  
  
<span data-ttu-id="253ca-104">**S’applique à** : Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="253ca-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="253ca-105">Contient un objet de table des matières incorporé qui fournit des informations sur un conteneur.</span><span class="sxs-lookup"><span data-stu-id="253ca-105">Contains an embedded contents table object that provides information about a container.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="253ca-106">Propriétés associées :</span><span class="sxs-lookup"><span data-stu-id="253ca-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="253ca-107">PR_CONTAINER_CONTENTS</span><span class="sxs-lookup"><span data-stu-id="253ca-107">PR_CONTAINER_CONTENTS</span></span>  <br/> |
|<span data-ttu-id="253ca-108">Identificateur :</span><span class="sxs-lookup"><span data-stu-id="253ca-108">Identifier:</span></span>  <br/> |<span data-ttu-id="253ca-109">0x360F</span><span class="sxs-lookup"><span data-stu-id="253ca-109">0x360F</span></span>  <br/> |
|<span data-ttu-id="253ca-110">Type de données :</span><span class="sxs-lookup"><span data-stu-id="253ca-110">Data type:</span></span>  <br/> |<span data-ttu-id="253ca-111">PT_OBJECT</span><span class="sxs-lookup"><span data-stu-id="253ca-111">PT_OBJECT</span></span>  <br/> |
|<span data-ttu-id="253ca-112">Domaine :</span><span class="sxs-lookup"><span data-stu-id="253ca-112">Area:</span></span>  <br/> |<span data-ttu-id="253ca-113">Container</span><span class="sxs-lookup"><span data-stu-id="253ca-113">Container</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="253ca-114">Remarques</span><span class="sxs-lookup"><span data-stu-id="253ca-114">Remarks</span></span>

<span data-ttu-id="253ca-115">Cette propriété peut être exclue dans les opérations [IMAPIProp::CopyTo](imapiprop-copyto.md) ou incluse dans les opérations [IMAPIProp::CopyProps.](imapiprop-copyprops.md)</span><span class="sxs-lookup"><span data-stu-id="253ca-115">This property can be excluded in [IMAPIProp::CopyTo](imapiprop-copyto.md) operations or included in [IMAPIProp::CopyProps](imapiprop-copyprops.md) operations.</span></span> <span data-ttu-id="253ca-116">En tant que propriété de type PT_OBJECT, elle ne peut pas être récupérée avec succès par la méthode [IMAPIProp::GetProps](imapiprop-getprops.md) ; Son contenu doit être accessible par la méthode [IMAPIProp::OpenProperty,](imapiprop-openproperty.md) en demandant l’identificateur IID_IMAPITable’interface.</span><span class="sxs-lookup"><span data-stu-id="253ca-116">As a property of type PT_OBJECT, it cannot be successfully retrieved by the [IMAPIProp::GetProps](imapiprop-getprops.md) method; its contents should be accessed by the [IMAPIProp::OpenProperty](imapiprop-openproperty.md) method, requesting the IID_IMAPITable interface identifier.</span></span> <span data-ttu-id="253ca-117">Les fournisseurs de services doivent le signaler à la méthode [IMAPIProp::GetPropList](imapiprop-getproplist.md) si elle est définie, mais peuvent éventuellement la signaler ou non si elle n’est pas définie.</span><span class="sxs-lookup"><span data-stu-id="253ca-117">Service providers must report it to the [IMAPIProp::GetPropList](imapiprop-getproplist.md) method if it is set, but can optionally report it or not if it is not set.</span></span> 
  
<span data-ttu-id="253ca-118">Pour récupérer le contenu de la table, une application cliente doit appeler la méthode [IMAPIContainer::GetContentsTable.](imapicontainer-getcontentstable.md)</span><span class="sxs-lookup"><span data-stu-id="253ca-118">To retrieve table contents, a client application should call the [IMAPIContainer::GetContentsTable](imapicontainer-getcontentstable.md) method.</span></span> <span data-ttu-id="253ca-119">For more information, see [Tables des mati�res](contents-tables.md).</span><span class="sxs-lookup"><span data-stu-id="253ca-119">For more information, see [Contents Tables](contents-tables.md).</span></span> 
  
<span data-ttu-id="253ca-120">Cette propriété, **PR_CONTAINER_HIERARCHY** ([PidTagContainerHierarchy](pidtagcontainerhierarchy-canonical-property.md)) et **PR_FOLDER_ASSOCIATED_CONTENTS** ([PidTagFolderAssociatedContents](pidtagfolderassociatedcontents-canonical-property.md)) sont similaires dans l’utilisation.</span><span class="sxs-lookup"><span data-stu-id="253ca-120">This property, **PR_CONTAINER_HIERARCHY** ([PidTagContainerHierarchy](pidtagcontainerhierarchy-canonical-property.md)) , and **PR_FOLDER_ASSOCIATED_CONTENTS** ([PidTagFolderAssociatedContents](pidtagfolderassociatedcontents-canonical-property.md)) are similar in usage.</span></span> <span data-ttu-id="253ca-121">Plusieurs propriétés MAPI permettent d’accéder aux tables :</span><span class="sxs-lookup"><span data-stu-id="253ca-121">Several MAPI properties provide access to tables:</span></span> 
  
|<span data-ttu-id="253ca-122">**Propriété**</span><span class="sxs-lookup"><span data-stu-id="253ca-122">**Property**</span></span>|<span data-ttu-id="253ca-123">**Tableau**</span><span class="sxs-lookup"><span data-stu-id="253ca-123">**Table**</span></span>|
|:-----|:-----|
|<span data-ttu-id="253ca-124">PidTagContainerContents</span><span class="sxs-lookup"><span data-stu-id="253ca-124">PidTagContainerContents</span></span>  <br/> |<span data-ttu-id="253ca-125">Table Contents</span><span class="sxs-lookup"><span data-stu-id="253ca-125">Contents table</span></span>  <br/> |
|<span data-ttu-id="253ca-126">**PR_CONTAINER_HIERARCHY** ([PidTagContainerHierarchy](pidtagcontainerhierarchy-canonical-property.md))</span><span class="sxs-lookup"><span data-stu-id="253ca-126">**PR_CONTAINER_HIERARCHY** ([PidTagContainerHierarchy](pidtagcontainerhierarchy-canonical-property.md))</span></span>  <br/> |<span data-ttu-id="253ca-127">Table Hierarchy</span><span class="sxs-lookup"><span data-stu-id="253ca-127">Hierarchy table</span></span>  <br/> |
|<span data-ttu-id="253ca-128">**PR_FOLDER_ASSOCIATED_CONTENTS** ([PidTagFolderAssociatedContents](pidtagfolderassociatedcontents-canonical-property.md))</span><span class="sxs-lookup"><span data-stu-id="253ca-128">**PR_FOLDER_ASSOCIATED_CONTENTS** ([PidTagFolderAssociatedContents](pidtagfolderassociatedcontents-canonical-property.md))</span></span>  <br/> |<span data-ttu-id="253ca-129">Table des matières associée</span><span class="sxs-lookup"><span data-stu-id="253ca-129">Associated contents table</span></span>  <br/> |
|<span data-ttu-id="253ca-130">**PR_MESSAGE_ATTACHMENTS** ([PidTagMessageAttachments](pidtagmessageattachments-canonical-property.md))</span><span class="sxs-lookup"><span data-stu-id="253ca-130">**PR_MESSAGE_ATTACHMENTS** ([PidTagMessageAttachments](pidtagmessageattachments-canonical-property.md))</span></span>  <br/> |<span data-ttu-id="253ca-131">Table Attachment</span><span class="sxs-lookup"><span data-stu-id="253ca-131">Attachment table</span></span>  <br/> |
|<span data-ttu-id="253ca-132">**PR_MESSAGE_RECIPIENTS** ([PidTagMessageRecipients](pidtagmessagerecipients-canonical-property.md))</span><span class="sxs-lookup"><span data-stu-id="253ca-132">**PR_MESSAGE_RECIPIENTS** ([PidTagMessageRecipients](pidtagmessagerecipients-canonical-property.md))</span></span>  <br/> |<span data-ttu-id="253ca-133">Table Recipient</span><span class="sxs-lookup"><span data-stu-id="253ca-133">Recipient table</span></span>  <br/> |
   
## <a name="related-resources"></a><span data-ttu-id="253ca-134">Ressources connexes</span><span class="sxs-lookup"><span data-stu-id="253ca-134">Related resources</span></span>

### <a name="protocol-specifications"></a><span data-ttu-id="253ca-135">Spécifications de protocole</span><span class="sxs-lookup"><span data-stu-id="253ca-135">Protocol specifications</span></span>

<span data-ttu-id="253ca-136">[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="253ca-136">[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="253ca-137">Fournit des références aux spécifications Exchange Server de protocole associées.</span><span class="sxs-lookup"><span data-stu-id="253ca-137">Provides references to related Exchange Server protocol specifications.</span></span>
    
<span data-ttu-id="253ca-138">[[MS-OXOABK]](https://msdn.microsoft.com/library/f4cf9b4c-9232-4506-9e71-2270de217614%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="253ca-138">[[MS-OXOABK]](https://msdn.microsoft.com/library/f4cf9b4c-9232-4506-9e71-2270de217614%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="253ca-139">Spécifie les propriétés et les opérations des listes d’utilisateurs, de contacts, de groupes et de ressources.</span><span class="sxs-lookup"><span data-stu-id="253ca-139">Specifies the properties and operations for lists of users, contacts, groups, and resources.</span></span>
    
### <a name="header-files"></a><span data-ttu-id="253ca-140">Fichiers d’en-tête</span><span class="sxs-lookup"><span data-stu-id="253ca-140">Header files</span></span>

<span data-ttu-id="253ca-141">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="253ca-141">Mapidefs.h</span></span>
  
> <span data-ttu-id="253ca-142">Fournit des définitions de type de données.</span><span class="sxs-lookup"><span data-stu-id="253ca-142">Provides data type definitions.</span></span>
    
<span data-ttu-id="253ca-143">Mapitags.h</span><span class="sxs-lookup"><span data-stu-id="253ca-143">Mapitags.h</span></span>
  
> <span data-ttu-id="253ca-144">Contient les définitions des propriétés répertoriées en tant que noms de remplacement.</span><span class="sxs-lookup"><span data-stu-id="253ca-144">Contains definitions of properties listed as alternate names.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="253ca-145">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="253ca-145">See also</span></span>



[<span data-ttu-id="253ca-146">Propriétés MAPI</span><span class="sxs-lookup"><span data-stu-id="253ca-146">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="253ca-147">Propriétés canoniques MAPI</span><span class="sxs-lookup"><span data-stu-id="253ca-147">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="253ca-148">Mappage des noms de propriétés canoniques aux noms MAPI</span><span class="sxs-lookup"><span data-stu-id="253ca-148">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="253ca-149">Mappage des noms MAPI aux noms de propriétés canoniques</span><span class="sxs-lookup"><span data-stu-id="253ca-149">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

