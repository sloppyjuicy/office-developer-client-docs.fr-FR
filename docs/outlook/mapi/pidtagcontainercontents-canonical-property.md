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
ms.openlocfilehash: 5f0717c2a6def6f99f1e53217764e8820125b79d
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32283127"
---
# <a name="pidtagcontainercontents-canonical-property"></a><span data-ttu-id="b030e-103">Propriété canonique PidTagContainerContents</span><span class="sxs-lookup"><span data-stu-id="b030e-103">PidTagContainerContents Canonical Property</span></span>

  
  
<span data-ttu-id="b030e-104">**S’applique à** : Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="b030e-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="b030e-105">Contient un objet table de contenu incorporé qui fournit des informations sur un conteneur.</span><span class="sxs-lookup"><span data-stu-id="b030e-105">Contains an embedded contents table object that provides information about a container.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="b030e-106">Propriétés associées :</span><span class="sxs-lookup"><span data-stu-id="b030e-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="b030e-107">PR_CONTAINER_CONTENTS</span><span class="sxs-lookup"><span data-stu-id="b030e-107">PR_CONTAINER_CONTENTS</span></span>  <br/> |
|<span data-ttu-id="b030e-108">Identificateur :</span><span class="sxs-lookup"><span data-stu-id="b030e-108">Identifier:</span></span>  <br/> |<span data-ttu-id="b030e-109">0x360F</span><span class="sxs-lookup"><span data-stu-id="b030e-109">0x360F</span></span>  <br/> |
|<span data-ttu-id="b030e-110">Type de données :</span><span class="sxs-lookup"><span data-stu-id="b030e-110">Data type:</span></span>  <br/> |<span data-ttu-id="b030e-111">PT_OBJECT</span><span class="sxs-lookup"><span data-stu-id="b030e-111">PT_OBJECT</span></span>  <br/> |
|<span data-ttu-id="b030e-112">Domaine :</span><span class="sxs-lookup"><span data-stu-id="b030e-112">Area:</span></span>  <br/> |<span data-ttu-id="b030e-113">Container</span><span class="sxs-lookup"><span data-stu-id="b030e-113">Container</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="b030e-114">Remarques</span><span class="sxs-lookup"><span data-stu-id="b030e-114">Remarks</span></span>

<span data-ttu-id="b030e-115">Cette propriété peut être exclue dans [IMAPIProp:: CopyTo](imapiprop-copyto.md) Operations ou incluse dans [IMAPIProp:: CopyProps](imapiprop-copyprops.md) Operations.</span><span class="sxs-lookup"><span data-stu-id="b030e-115">This property can be excluded in [IMAPIProp::CopyTo](imapiprop-copyto.md) operations or included in [IMAPIProp::CopyProps](imapiprop-copyprops.md) operations.</span></span> <span data-ttu-id="b030e-116">En tant que propriété de type PT_OBJECT, elle ne peut pas être récupérée avec succès par la méthode [IMAPIProp:: GetProps](imapiprop-getprops.md) ; son contenu doit être accessible à l'aide de la méthode [IMAPIProp:: OpenProperty](imapiprop-openproperty.md) , qui demande l'identificateur d'interface IID_IMAPITable.</span><span class="sxs-lookup"><span data-stu-id="b030e-116">As a property of type PT_OBJECT, it cannot be successfully retrieved by the [IMAPIProp::GetProps](imapiprop-getprops.md) method; its contents should be accessed by the [IMAPIProp::OpenProperty](imapiprop-openproperty.md) method, requesting the IID_IMAPITable interface identifier.</span></span> <span data-ttu-id="b030e-117">Les fournisseurs de services doivent le signaler à la méthode [IMAPIProp:: GetPropList](imapiprop-getproplist.md) s'il est défini, mais peuvent éventuellement le signaler ou non s'il n'est pas défini.</span><span class="sxs-lookup"><span data-stu-id="b030e-117">Service providers must report it to the [IMAPIProp::GetPropList](imapiprop-getproplist.md) method if it is set, but can optionally report it or not if it is not set.</span></span> 
  
<span data-ttu-id="b030e-118">Pour récupérer le contenu de la table, une application cliente doit appeler la méthode [IMAPIContainer:: GetContentsTable](imapicontainer-getcontentstable.md) .</span><span class="sxs-lookup"><span data-stu-id="b030e-118">To retrieve table contents, a client application should call the [IMAPIContainer::GetContentsTable](imapicontainer-getcontentstable.md) method.</span></span> <span data-ttu-id="b030e-119">For more information, see [Tables des mati�res](contents-tables.md).</span><span class="sxs-lookup"><span data-stu-id="b030e-119">For more information, see [Contents Tables](contents-tables.md).</span></span> 
  
<span data-ttu-id="b030e-120">Cette propriété, **PR_CONTAINER_HIERARCHY** ([PidTagContainerHierarchy](pidtagcontainerhierarchy-canonical-property.md)) et **PR_FOLDER_ASSOCIATED_CONTENTS** ([PidTagFolderAssociatedContents](pidtagfolderassociatedcontents-canonical-property.md)) sont similaires en matière d'utilisation.</span><span class="sxs-lookup"><span data-stu-id="b030e-120">This property, **PR_CONTAINER_HIERARCHY** ([PidTagContainerHierarchy](pidtagcontainerhierarchy-canonical-property.md)) , and **PR_FOLDER_ASSOCIATED_CONTENTS** ([PidTagFolderAssociatedContents](pidtagfolderassociatedcontents-canonical-property.md)) are similar in usage.</span></span> <span data-ttu-id="b030e-121">Plusieurs propriétés MAPI permettent d'accéder à des tables:</span><span class="sxs-lookup"><span data-stu-id="b030e-121">Several MAPI properties provide access to tables:</span></span> 
  
|<span data-ttu-id="b030e-122">**Property**</span><span class="sxs-lookup"><span data-stu-id="b030e-122">**Property**</span></span>|<span data-ttu-id="b030e-123">**Table**</span><span class="sxs-lookup"><span data-stu-id="b030e-123">**Table**</span></span>|
|:-----|:-----|
|<span data-ttu-id="b030e-124">PidTagContainerContents</span><span class="sxs-lookup"><span data-stu-id="b030e-124">PidTagContainerContents</span></span>  <br/> |<span data-ttu-id="b030e-125">Table des matières</span><span class="sxs-lookup"><span data-stu-id="b030e-125">Contents table</span></span>  <br/> |
|<span data-ttu-id="b030e-126">**PR_CONTAINER_HIERARCHY** ([PidTagContainerHierarchy](pidtagcontainerhierarchy-canonical-property.md))</span><span class="sxs-lookup"><span data-stu-id="b030e-126">**PR_CONTAINER_HIERARCHY** ([PidTagContainerHierarchy](pidtagcontainerhierarchy-canonical-property.md))</span></span>  <br/> |<span data-ttu-id="b030e-127">Table Hierarchy</span><span class="sxs-lookup"><span data-stu-id="b030e-127">Hierarchy table</span></span>  <br/> |
|<span data-ttu-id="b030e-128">**PR_FOLDER_ASSOCIATED_CONTENTS** ([PidTagFolderAssociatedContents](pidtagfolderassociatedcontents-canonical-property.md))</span><span class="sxs-lookup"><span data-stu-id="b030e-128">**PR_FOLDER_ASSOCIATED_CONTENTS** ([PidTagFolderAssociatedContents](pidtagfolderassociatedcontents-canonical-property.md))</span></span>  <br/> |<span data-ttu-id="b030e-129">Table des matières associées</span><span class="sxs-lookup"><span data-stu-id="b030e-129">Associated contents table</span></span>  <br/> |
|<span data-ttu-id="b030e-130">**PR_MESSAGE_ATTACHMENTS** ([PidTagMessageAttachments](pidtagmessageattachments-canonical-property.md))</span><span class="sxs-lookup"><span data-stu-id="b030e-130">**PR_MESSAGE_ATTACHMENTS** ([PidTagMessageAttachments](pidtagmessageattachments-canonical-property.md))</span></span>  <br/> |<span data-ttu-id="b030e-131">Table des pièces jointes</span><span class="sxs-lookup"><span data-stu-id="b030e-131">Attachment table</span></span>  <br/> |
|<span data-ttu-id="b030e-132">**PR_MESSAGE_RECIPIENTS** ([PidTagMessageRecipients](pidtagmessagerecipients-canonical-property.md))</span><span class="sxs-lookup"><span data-stu-id="b030e-132">**PR_MESSAGE_RECIPIENTS** ([PidTagMessageRecipients](pidtagmessagerecipients-canonical-property.md))</span></span>  <br/> |<span data-ttu-id="b030e-133">Table de destinataires</span><span class="sxs-lookup"><span data-stu-id="b030e-133">Recipient table</span></span>  <br/> |
   
## <a name="related-resources"></a><span data-ttu-id="b030e-134">Ressources associées</span><span class="sxs-lookup"><span data-stu-id="b030e-134">Related resources</span></span>

### <a name="protocol-specifications"></a><span data-ttu-id="b030e-135">Spécifications de protocole</span><span class="sxs-lookup"><span data-stu-id="b030e-135">Protocol specifications</span></span>

<span data-ttu-id="b030e-136">[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="b030e-136">[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="b030e-137">Fournit des références à des spécifications de protocole Exchange Server connexes.</span><span class="sxs-lookup"><span data-stu-id="b030e-137">Provides references to related Exchange Server protocol specifications.</span></span>
    
<span data-ttu-id="b030e-138">[[MS-OXOABK]](https://msdn.microsoft.com/library/f4cf9b4c-9232-4506-9e71-2270de217614%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="b030e-138">[[MS-OXOABK]](https://msdn.microsoft.com/library/f4cf9b4c-9232-4506-9e71-2270de217614%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="b030e-139">Spécifie les propriétés et les opérations pour les listes d'utilisateurs, de contacts, de groupes et de ressources.</span><span class="sxs-lookup"><span data-stu-id="b030e-139">Specifies the properties and operations for lists of users, contacts, groups, and resources.</span></span>
    
### <a name="header-files"></a><span data-ttu-id="b030e-140">Fichiers d'en-tête</span><span class="sxs-lookup"><span data-stu-id="b030e-140">Header files</span></span>

<span data-ttu-id="b030e-141">Mapidefs. h</span><span class="sxs-lookup"><span data-stu-id="b030e-141">Mapidefs.h</span></span>
  
> <span data-ttu-id="b030e-142">Fournit des définitions de type de données.</span><span class="sxs-lookup"><span data-stu-id="b030e-142">Provides data type definitions.</span></span>
    
<span data-ttu-id="b030e-143">Mapitags. h</span><span class="sxs-lookup"><span data-stu-id="b030e-143">Mapitags.h</span></span>
  
> <span data-ttu-id="b030e-144">Contient les définitions des propriétés figurant en tant que noms de substitution.</span><span class="sxs-lookup"><span data-stu-id="b030e-144">Contains definitions of properties listed as alternate names.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="b030e-145">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="b030e-145">See also</span></span>



[<span data-ttu-id="b030e-146">Propriétés MAPI</span><span class="sxs-lookup"><span data-stu-id="b030e-146">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="b030e-147">Propriétés canoniques MAPI</span><span class="sxs-lookup"><span data-stu-id="b030e-147">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="b030e-148">Mappage des noms de propriétés canoniques aux noms MAPI</span><span class="sxs-lookup"><span data-stu-id="b030e-148">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="b030e-149">Mappage des noms MAPI aux noms de propriétés canoniques</span><span class="sxs-lookup"><span data-stu-id="b030e-149">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

