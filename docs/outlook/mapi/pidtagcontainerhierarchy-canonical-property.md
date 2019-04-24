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
description: 'Derni�re modification�: lundi 9 mars 2015'
ms.openlocfilehash: f009d7ce5cd1856ccff1e00953188c8edde7a6bc
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32332857"
---
# <a name="pidtagcontainerhierarchy-canonical-property"></a><span data-ttu-id="45193-103">Propriété canonique PidTagContainerHierarchy</span><span class="sxs-lookup"><span data-stu-id="45193-103">PidTagContainerHierarchy Canonical Property</span></span>

  
  
<span data-ttu-id="45193-104">**S’applique à** : Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="45193-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="45193-105">Contient un objet table de hiérarchie incorporé qui fournit des informations sur les conteneurs enfants.</span><span class="sxs-lookup"><span data-stu-id="45193-105">Contains an embedded hierarchy table object that provides information about the child containers.</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="45193-106">Propriétés associées :</span><span class="sxs-lookup"><span data-stu-id="45193-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="45193-107">PR_CONTAINER_HIERARCHY</span><span class="sxs-lookup"><span data-stu-id="45193-107">PR_CONTAINER_HIERARCHY</span></span>  <br/> |
|<span data-ttu-id="45193-108">Identificateur :</span><span class="sxs-lookup"><span data-stu-id="45193-108">Identifier:</span></span>  <br/> |<span data-ttu-id="45193-109">0x360E</span><span class="sxs-lookup"><span data-stu-id="45193-109">0x360E</span></span>  <br/> |
|<span data-ttu-id="45193-110">Type de données :</span><span class="sxs-lookup"><span data-stu-id="45193-110">Data type:</span></span>  <br/> |<span data-ttu-id="45193-111">PT_OBJECT</span><span class="sxs-lookup"><span data-stu-id="45193-111">PT_OBJECT</span></span>  <br/> |
|<span data-ttu-id="45193-112">Domaine :</span><span class="sxs-lookup"><span data-stu-id="45193-112">Area:</span></span>  <br/> |<span data-ttu-id="45193-113">Container</span><span class="sxs-lookup"><span data-stu-id="45193-113">Container</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="45193-114">Remarques</span><span class="sxs-lookup"><span data-stu-id="45193-114">Remarks</span></span>

<span data-ttu-id="45193-115">Cette propriété peut être exclue dans [IMAPIProp:: CopyTo](imapiprop-copyto.md) Operations ou incluse dans [IMAPIProp:: CopyProps](imapiprop-copyprops.md) Operations.</span><span class="sxs-lookup"><span data-stu-id="45193-115">This property can be excluded in [IMAPIProp::CopyTo](imapiprop-copyto.md) operations or included in [IMAPIProp::CopyProps](imapiprop-copyprops.md) operations.</span></span> <span data-ttu-id="45193-116">En tant que propriété de type **PT_OBJECT**, elle ne peut pas être récupérée avec succès par la méthode [IMAPIProp:: GetProps](imapiprop-getprops.md) ; son contenu doit être accessible à l'aide de la méthode [IMAPIProp:: OpenProperty](imapiprop-openproperty.md) , qui demande l'identificateur d'interface IID_IMAPITable.</span><span class="sxs-lookup"><span data-stu-id="45193-116">As a property of type **PT_OBJECT**, it cannot be successfully retrieved by the [IMAPIProp::GetProps](imapiprop-getprops.md) method; its contents should be accessed by the [IMAPIProp::OpenProperty](imapiprop-openproperty.md) method, requesting the IID_IMAPITable interface identifier.</span></span> <span data-ttu-id="45193-117">Les fournisseurs de services doivent le signaler à la méthode [IMAPIProp:: GetPropList](imapiprop-getproplist.md) s'il est défini, mais peuvent éventuellement le signaler ou non s'il n'est pas défini.</span><span class="sxs-lookup"><span data-stu-id="45193-117">Service providers must report it to the [IMAPIProp::GetPropList](imapiprop-getproplist.md) method if it is set, but can optionally report it or not if it is not set.</span></span> 
  
<span data-ttu-id="45193-118">Pour récupérer le contenu de la table, une application cliente doit appeler la méthode [IMAPIContainer:: GetHierarchyTable](imapicontainer-gethierarchytable.md) .</span><span class="sxs-lookup"><span data-stu-id="45193-118">To retrieve table contents, a client application should call the [IMAPIContainer::GetHierarchyTable](imapicontainer-gethierarchytable.md) method.</span></span> <span data-ttu-id="45193-119">Pour plus d'informations, consultez la rubrique [Hierarchy tables](hierarchy-tables.md).</span><span class="sxs-lookup"><span data-stu-id="45193-119">For more information, see [Hierarchy Tables](hierarchy-tables.md).</span></span> 
  
 <span data-ttu-id="45193-120">**PR_CONTAINER_CONTENTS** ([PidTagContainerContents](pidtagcontainercontents-canonical-property.md)), **PR_FOLDER_ASSOCIATED_CONTENTS** ([PidTagFolderAssociatedContents](pidtagfolderassociatedcontents-canonical-property.md)) et cette propriété sont similaires dans l'utilisation.</span><span class="sxs-lookup"><span data-stu-id="45193-120">**PR_CONTAINER_CONTENTS** ([PidTagContainerContents](pidtagcontainercontents-canonical-property.md)), **PR_FOLDER_ASSOCIATED_CONTENTS** ([PidTagFolderAssociatedContents](pidtagfolderassociatedcontents-canonical-property.md)), and this property are similar in usage.</span></span> <span data-ttu-id="45193-121">Plusieurs propriétés MAPI permettent d'accéder à des tables:</span><span class="sxs-lookup"><span data-stu-id="45193-121">Several MAPI properties provide access to tables:</span></span> 
  
|<span data-ttu-id="45193-122">**Property**</span><span class="sxs-lookup"><span data-stu-id="45193-122">**Property**</span></span>|<span data-ttu-id="45193-123">**Table**</span><span class="sxs-lookup"><span data-stu-id="45193-123">**Table**</span></span>|
|:-----|:-----|
|<span data-ttu-id="45193-124">**PR_CONTAINER_CONTENTS** ([PidTagContainerContents](pidtagcontainercontents-canonical-property.md))</span><span class="sxs-lookup"><span data-stu-id="45193-124">**PR_CONTAINER_CONTENTS** ([PidTagContainerContents](pidtagcontainercontents-canonical-property.md))</span></span>  <br/> |<span data-ttu-id="45193-125">Table des matières</span><span class="sxs-lookup"><span data-stu-id="45193-125">Contents table</span></span>  <br/> |
|<span data-ttu-id="45193-126">**PR_CONTAINER_HIERARCHY**</span><span class="sxs-lookup"><span data-stu-id="45193-126">**PR_CONTAINER_HIERARCHY**</span></span> <br/> |<span data-ttu-id="45193-127">Table Hierarchy</span><span class="sxs-lookup"><span data-stu-id="45193-127">Hierarchy table</span></span>  <br/> |
|<span data-ttu-id="45193-128">**PR_FOLDER_ASSOCIATED_CONTENTS** ([PidTagFolderAssociatedContents](pidtagfolderassociatedcontents-canonical-property.md))</span><span class="sxs-lookup"><span data-stu-id="45193-128">**PR_FOLDER_ASSOCIATED_CONTENTS** ([PidTagFolderAssociatedContents](pidtagfolderassociatedcontents-canonical-property.md))</span></span>  <br/> |<span data-ttu-id="45193-129">Table des matières associées</span><span class="sxs-lookup"><span data-stu-id="45193-129">Associated contents table</span></span>  <br/> |
|<span data-ttu-id="45193-130">**PR_MESSAGE_ATTACHMENTS** ([PidTagMessageAttachments](pidtagmessageattachments-canonical-property.md))</span><span class="sxs-lookup"><span data-stu-id="45193-130">**PR_MESSAGE_ATTACHMENTS** ([PidTagMessageAttachments](pidtagmessageattachments-canonical-property.md))</span></span>  <br/> |<span data-ttu-id="45193-131">Table des pièces jointes</span><span class="sxs-lookup"><span data-stu-id="45193-131">Attachment table</span></span>  <br/> |
|<span data-ttu-id="45193-132">**PR_MESSAGE_RECIPIENTS** ([PidTagMessageRecipients](pidtagmessagerecipients-canonical-property.md))</span><span class="sxs-lookup"><span data-stu-id="45193-132">**PR_MESSAGE_RECIPIENTS** ([PidTagMessageRecipients](pidtagmessagerecipients-canonical-property.md))</span></span>  <br/> |<span data-ttu-id="45193-133">Table de destinataires</span><span class="sxs-lookup"><span data-stu-id="45193-133">Recipient table</span></span>  <br/> |
   
## <a name="related-resources"></a><span data-ttu-id="45193-134">Ressources associées</span><span class="sxs-lookup"><span data-stu-id="45193-134">Related resources</span></span>

### <a name="protocol-specifications"></a><span data-ttu-id="45193-135">Spécifications de protocole</span><span class="sxs-lookup"><span data-stu-id="45193-135">Protocol specifications</span></span>

<span data-ttu-id="45193-136">[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="45193-136">[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="45193-137">Fournit des références à des spécifications de protocole Exchange Server connexes.</span><span class="sxs-lookup"><span data-stu-id="45193-137">Provides references to related Exchange Server protocol specifications.</span></span>
    
<span data-ttu-id="45193-138">[[MS-OXCFXICS]](https://msdn.microsoft.com/library/b9752f3d-d50d-44b8-9e6b-608a117c8532%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="45193-138">[[MS-OXCFXICS]](https://msdn.microsoft.com/library/b9752f3d-d50d-44b8-9e6b-608a117c8532%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="45193-139">Gère l'ordre et le flux de transfert de données entre un client et un serveur.</span><span class="sxs-lookup"><span data-stu-id="45193-139">Handles the order and flow for data transfers between a client and server.</span></span>
    
<span data-ttu-id="45193-140">[[MS-OXCICAL]](https://msdn.microsoft.com/library/a685a040-5b69-4c84-b084-795113fb4012%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="45193-140">[[MS-OXCICAL]](https://msdn.microsoft.com/library/a685a040-5b69-4c84-b084-795113fb4012%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="45193-141">Effectue une conversion entre l'IETF RFC2445, RFC2446 et RFC2447, et les objets de rendez-vous et de réunion.</span><span class="sxs-lookup"><span data-stu-id="45193-141">Converts between IETF RFC2445, RFC2446, and RFC2447, and appointment and meeting objects.</span></span>
    
### <a name="header-files"></a><span data-ttu-id="45193-142">Fichiers d'en-tête</span><span class="sxs-lookup"><span data-stu-id="45193-142">Header files</span></span>

<span data-ttu-id="45193-143">Mapidefs. h</span><span class="sxs-lookup"><span data-stu-id="45193-143">Mapidefs.h</span></span>
  
> <span data-ttu-id="45193-144">Fournit des définitions de type de données.</span><span class="sxs-lookup"><span data-stu-id="45193-144">Provides data type definitions.</span></span>
    
<span data-ttu-id="45193-145">Mapitags. h</span><span class="sxs-lookup"><span data-stu-id="45193-145">Mapitags.h</span></span>
  
> <span data-ttu-id="45193-146">Contient les définitions des propriétés figurant en tant que noms de substitution.</span><span class="sxs-lookup"><span data-stu-id="45193-146">Contains definitions of properties listed as alternate names.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="45193-147">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="45193-147">See also</span></span>



[<span data-ttu-id="45193-148">Propriétés MAPI</span><span class="sxs-lookup"><span data-stu-id="45193-148">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="45193-149">Propriétés canoniques MAPI</span><span class="sxs-lookup"><span data-stu-id="45193-149">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="45193-150">Mappage des noms de propriétés canoniques aux noms MAPI</span><span class="sxs-lookup"><span data-stu-id="45193-150">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="45193-151">Mappage des noms MAPI aux noms de propriétés canoniques</span><span class="sxs-lookup"><span data-stu-id="45193-151">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

