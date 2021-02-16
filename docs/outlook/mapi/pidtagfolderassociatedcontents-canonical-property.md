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
description: Dernière modification le 9 mars 2015
ms.openlocfilehash: c85c5d7c3e80508c4d328f69ac4ad15f0f2c355a
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32316302"
---
# <a name="pidtagfolderassociatedcontents-canonical-property"></a><span data-ttu-id="a3196-103">Propriété canonique PidTagFolderAssociatedContents</span><span class="sxs-lookup"><span data-stu-id="a3196-103">PidTagFolderAssociatedContents Canonical Property</span></span>

  
  
<span data-ttu-id="a3196-104">**S’applique à** : Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="a3196-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="a3196-105">Contient un objet de table des matières incorporé qui fournit des informations sur la table des matières associée.</span><span class="sxs-lookup"><span data-stu-id="a3196-105">Contains an embedded contents table object that provides information about the associated contents table.</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="a3196-106">Propriétés associées :</span><span class="sxs-lookup"><span data-stu-id="a3196-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="a3196-107">PR_FOLDER_ASSOCIATED_CONTENTS</span><span class="sxs-lookup"><span data-stu-id="a3196-107">PR_FOLDER_ASSOCIATED_CONTENTS</span></span>  <br/> |
|<span data-ttu-id="a3196-108">Identificateur :</span><span class="sxs-lookup"><span data-stu-id="a3196-108">Identifier:</span></span>  <br/> |<span data-ttu-id="a3196-109">0x3610</span><span class="sxs-lookup"><span data-stu-id="a3196-109">0x3610</span></span>  <br/> |
|<span data-ttu-id="a3196-110">Type de données :</span><span class="sxs-lookup"><span data-stu-id="a3196-110">Data type:</span></span>  <br/> |<span data-ttu-id="a3196-111">PT_OBJECT</span><span class="sxs-lookup"><span data-stu-id="a3196-111">PT_OBJECT</span></span>  <br/> |
|<span data-ttu-id="a3196-112">Domaine :</span><span class="sxs-lookup"><span data-stu-id="a3196-112">Area:</span></span>  <br/> |<span data-ttu-id="a3196-113">Conteneur MAPI</span><span class="sxs-lookup"><span data-stu-id="a3196-113">MAPI container</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="a3196-114">Remarques</span><span class="sxs-lookup"><span data-stu-id="a3196-114">Remarks</span></span>

<span data-ttu-id="a3196-115">La table des matières associée représente un sous-foldeur qui n’apparaît pas dans la table des matières standard.</span><span class="sxs-lookup"><span data-stu-id="a3196-115">The associated contents table represents a subfolder that does not appear in the standard contents table.</span></span> <span data-ttu-id="a3196-116">Il contient les messages associés ou masqués du dossier.</span><span class="sxs-lookup"><span data-stu-id="a3196-116">It contains the folder's associated, or hidden, messages.</span></span> 
  
<span data-ttu-id="a3196-117">Cette propriété peut être exclue dans les opérations [IMAPIProp::CopyTo](imapiprop-copyto.md) ou incluse dans les opérations [IMAPIProp::CopyProps.](imapiprop-copyprops.md)</span><span class="sxs-lookup"><span data-stu-id="a3196-117">This property can be excluded in [IMAPIProp::CopyTo](imapiprop-copyto.md) operations or included in [IMAPIProp::CopyProps](imapiprop-copyprops.md) operations.</span></span> <span data-ttu-id="a3196-118">En tant que propriété de type **PT_OBJECT**, elle ne peut pas être récupérée avec succès par la méthode [IMAPIProp::GetProps](imapiprop-getprops.md) ; Son contenu doit être accessible par la méthode [IMAPIProp::OpenProperty,](imapiprop-openproperty.md) en demandant l’identificateur **IID_IMAPITable’interface.**</span><span class="sxs-lookup"><span data-stu-id="a3196-118">As a property of type **PT_OBJECT**, it cannot be successfully retrieved by the [IMAPIProp::GetProps](imapiprop-getprops.md) method; its contents should be accessed by the [IMAPIProp::OpenProperty](imapiprop-openproperty.md) method, requesting the **IID_IMAPITable** interface identifier.</span></span> <span data-ttu-id="a3196-119">Les fournisseurs de services doivent le signaler à la méthode [IMAPIProp::GetPropList](imapiprop-getproplist.md) si elle est définie, mais peuvent éventuellement la signaler ou non si elle n’est pas définie.</span><span class="sxs-lookup"><span data-stu-id="a3196-119">Service providers must report it to the [IMAPIProp::GetPropList](imapiprop-getproplist.md) method if it is set, but may optionally report it or not if it is not set.</span></span> 
  
<span data-ttu-id="a3196-120">Pour récupérer le contenu de la table, les applications clientes doivent appeler la méthode [IMAPIContainer::GetContentsTable.](imapicontainer-getcontentstable.md)</span><span class="sxs-lookup"><span data-stu-id="a3196-120">To retrieve table contents, client applications should call the [IMAPIContainer::GetContentsTable](imapicontainer-getcontentstable.md) method.</span></span> <span data-ttu-id="a3196-121">Pour plus d’informations sur les tables de contenu de dossier, voir Tables des [matières](contents-tables.md) et [Affichage d’une table des matières des dossiers.](displaying-a-folder-contents-table.md)</span><span class="sxs-lookup"><span data-stu-id="a3196-121">For more information on folder contents tables, see [Contents Tables](contents-tables.md) and [Displaying a Folder Contents Table](displaying-a-folder-contents-table.md).</span></span> 
  
<span data-ttu-id="a3196-122">Les **PR_CONTAINER_CONTENTS** ([PidTagContainerContents](pidtagcontainercontents-canonical-property.md)), **PR_CONTAINER_HIERARCHY** ([PidTagContainerHierarchy](pidtagcontainerhierarchy-canonical-property.md)) et cette propriété sont similaires dans l’utilisation.</span><span class="sxs-lookup"><span data-stu-id="a3196-122">The **PR_CONTAINER_CONTENTS** ([PidTagContainerContents](pidtagcontainercontents-canonical-property.md)), **PR_CONTAINER_HIERARCHY** ([PidTagContainerHierarchy](pidtagcontainerhierarchy-canonical-property.md)), and this property are similar in usage.</span></span> <span data-ttu-id="a3196-123">Plusieurs propriétés MAPI permettent d’accéder aux tables :</span><span class="sxs-lookup"><span data-stu-id="a3196-123">Several MAPI properties provide access to tables:</span></span> 
  
|<span data-ttu-id="a3196-124">**Propriété**</span><span class="sxs-lookup"><span data-stu-id="a3196-124">**Property**</span></span>|<span data-ttu-id="a3196-125">**Tableau**</span><span class="sxs-lookup"><span data-stu-id="a3196-125">**Table**</span></span>|
|:-----|:-----|
|<span data-ttu-id="a3196-126">**PR_CONTAINER_CONTENTS** ([PidTagContainerContents](pidtagcontainercontents-canonical-property.md))</span><span class="sxs-lookup"><span data-stu-id="a3196-126">**PR_CONTAINER_CONTENTS** ([PidTagContainerContents](pidtagcontainercontents-canonical-property.md))</span></span>  <br/> |<span data-ttu-id="a3196-127">Table Contents</span><span class="sxs-lookup"><span data-stu-id="a3196-127">Contents table</span></span>  <br/> |
|<span data-ttu-id="a3196-128">**PR_CONTAINER_HIERARCHY** ([PidTagContainerHierarchy](pidtagcontainerhierarchy-canonical-property.md))</span><span class="sxs-lookup"><span data-stu-id="a3196-128">**PR_CONTAINER_HIERARCHY** ([PidTagContainerHierarchy](pidtagcontainerhierarchy-canonical-property.md))</span></span>  <br/> |<span data-ttu-id="a3196-129">Table Hierarchy</span><span class="sxs-lookup"><span data-stu-id="a3196-129">Hierarchy table</span></span>  <br/> |
|<span data-ttu-id="a3196-130">**PR_FOLDER_ASSOCIATED_CONTENTS**</span><span class="sxs-lookup"><span data-stu-id="a3196-130">**PR_FOLDER_ASSOCIATED_CONTENTS**</span></span> <br/> |<span data-ttu-id="a3196-131">Table des matières associée</span><span class="sxs-lookup"><span data-stu-id="a3196-131">Associated contents table</span></span>  <br/> |
|<span data-ttu-id="a3196-132">**PR_MESSAGE_ATTACHMENTS** ([PidTagMessageAttachments](pidtagmessageattachments-canonical-property.md))</span><span class="sxs-lookup"><span data-stu-id="a3196-132">**PR_MESSAGE_ATTACHMENTS** ([PidTagMessageAttachments](pidtagmessageattachments-canonical-property.md))</span></span>  <br/> |<span data-ttu-id="a3196-133">Table Attachment</span><span class="sxs-lookup"><span data-stu-id="a3196-133">Attachment table</span></span>  <br/> |
|<span data-ttu-id="a3196-134">**PR_MESSAGE_RECIPIENTS** ([PidTagMessageRecipients](pidtagmessagerecipients-canonical-property.md))</span><span class="sxs-lookup"><span data-stu-id="a3196-134">**PR_MESSAGE_RECIPIENTS** ([PidTagMessageRecipients](pidtagmessagerecipients-canonical-property.md))</span></span>  <br/> |<span data-ttu-id="a3196-135">Table Recipient</span><span class="sxs-lookup"><span data-stu-id="a3196-135">Recipient table</span></span>  <br/> |
   
## <a name="related-resources"></a><span data-ttu-id="a3196-136">Ressources connexes</span><span class="sxs-lookup"><span data-stu-id="a3196-136">Related resources</span></span>

### <a name="protocol-specifications"></a><span data-ttu-id="a3196-137">Spécifications de protocole</span><span class="sxs-lookup"><span data-stu-id="a3196-137">Protocol specifications</span></span>

<span data-ttu-id="a3196-138">[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="a3196-138">[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="a3196-139">Fournit des références aux spécifications Exchange Server de protocole associées.</span><span class="sxs-lookup"><span data-stu-id="a3196-139">Provides references to related Exchange Server protocol specifications.</span></span>
    
<span data-ttu-id="a3196-140">[[MS-OXCFXICS]](https://msdn.microsoft.com/library/b9752f3d-d50d-44b8-9e6b-608a117c8532%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="a3196-140">[[MS-OXCFXICS]](https://msdn.microsoft.com/library/b9752f3d-d50d-44b8-9e6b-608a117c8532%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="a3196-141">Gère l’ordre et le flux des transferts de données entre un client et un serveur.</span><span class="sxs-lookup"><span data-stu-id="a3196-141">Handles the order and flow for data transfers between a client and server.</span></span>
    
<span data-ttu-id="a3196-142">[[MS-OXCICAL]](https://msdn.microsoft.com/library/a685a040-5b69-4c84-b084-795113fb4012%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="a3196-142">[[MS-OXCICAL]](https://msdn.microsoft.com/library/a685a040-5b69-4c84-b084-795113fb4012%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="a3196-143">Convertit les éléments RFC2445, RFC2446 et RFC2447 de l’IETF, ainsi que les éléments de rendez-vous et de réunion.</span><span class="sxs-lookup"><span data-stu-id="a3196-143">Converts between IETF RFC2445, RFC2446, and RFC2447, and appointment and meeting items.</span></span>
    
### <a name="header-files"></a><span data-ttu-id="a3196-144">Fichiers d’en-tête</span><span class="sxs-lookup"><span data-stu-id="a3196-144">Header files</span></span>

<span data-ttu-id="a3196-145">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="a3196-145">Mapidefs.h</span></span>
  
> <span data-ttu-id="a3196-146">Fournit des définitions de type de données.</span><span class="sxs-lookup"><span data-stu-id="a3196-146">Provides data type definitions.</span></span>
    
<span data-ttu-id="a3196-147">Mapitags.h</span><span class="sxs-lookup"><span data-stu-id="a3196-147">Mapitags.h</span></span>
  
> <span data-ttu-id="a3196-148">Contient les définitions des propriétés répertoriées en tant que noms de remplacement.</span><span class="sxs-lookup"><span data-stu-id="a3196-148">Contains definitions of properties listed as alternate names.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="a3196-149">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="a3196-149">See also</span></span>



[<span data-ttu-id="a3196-150">Propriété canonique PidTagAssociatedContentCount</span><span class="sxs-lookup"><span data-stu-id="a3196-150">PidTagAssociatedContentCount Canonical Property</span></span>](pidtagassociatedcontentcount-canonical-property.md)


[<span data-ttu-id="a3196-151">Propriétés MAPI</span><span class="sxs-lookup"><span data-stu-id="a3196-151">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="a3196-152">Propriétés canoniques MAPI</span><span class="sxs-lookup"><span data-stu-id="a3196-152">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="a3196-153">Mappage des noms de propriétés canoniques aux noms MAPI</span><span class="sxs-lookup"><span data-stu-id="a3196-153">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="a3196-154">Mappage des noms MAPI aux noms de propriétés canoniques</span><span class="sxs-lookup"><span data-stu-id="a3196-154">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

