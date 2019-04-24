---
title: Propriété canonique PidTagValidFolderMask
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- MAPI.PidTagValidFolderMask
api_type:
- COM
ms.assetid: 83a44aee-5269-42a8-8078-4bc063bb6e29
description: 'Derni�re modification�: lundi 9 mars 2015'
ms.openlocfilehash: 925e0eb60d55349ded114b827b6ca67e3b5ac1ce
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32360745"
---
# <a name="pidtagvalidfoldermask-canonical-property"></a><span data-ttu-id="64b7e-103">Propriété canonique PidTagValidFolderMask</span><span class="sxs-lookup"><span data-stu-id="64b7e-103">PidTagValidFolderMask Canonical Property</span></span>

  
  
<span data-ttu-id="64b7e-104">**S’applique à** : Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="64b7e-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="64b7e-105">Contient un masque de réindicateur des indicateurs qui indiquent la validité des identificateurs d'entrée des dossiers dans une banque de messages.</span><span class="sxs-lookup"><span data-stu-id="64b7e-105">Contains a bitmask of flags that indicate the validity of the entry identifiers of the folders in a message store.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="64b7e-106">Propriétés associées :</span><span class="sxs-lookup"><span data-stu-id="64b7e-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="64b7e-107">PR_VALID_FOLDER_MASK</span><span class="sxs-lookup"><span data-stu-id="64b7e-107">PR_VALID_FOLDER_MASK</span></span>  <br/> |
|<span data-ttu-id="64b7e-108">Identificateur :</span><span class="sxs-lookup"><span data-stu-id="64b7e-108">Identifier:</span></span>  <br/> |<span data-ttu-id="64b7e-109">0x35DF</span><span class="sxs-lookup"><span data-stu-id="64b7e-109">0x35DF</span></span>  <br/> |
|<span data-ttu-id="64b7e-110">Type de données :</span><span class="sxs-lookup"><span data-stu-id="64b7e-110">Data type:</span></span>  <br/> |<span data-ttu-id="64b7e-111">PT_LONG</span><span class="sxs-lookup"><span data-stu-id="64b7e-111">PT_LONG</span></span>  <br/> |
|<span data-ttu-id="64b7e-112">Domaine :</span><span class="sxs-lookup"><span data-stu-id="64b7e-112">Area:</span></span>  <br/> |<span data-ttu-id="64b7e-113">Banque de messages MAPI</span><span class="sxs-lookup"><span data-stu-id="64b7e-113">MAPI message store</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="64b7e-114">Remarques</span><span class="sxs-lookup"><span data-stu-id="64b7e-114">Remarks</span></span>

<span data-ttu-id="64b7e-115">L'identificateur d'entrée d'un dossier peut devenir non valide si un utilisateur supprime le dossier ou si la Banque de messages est endommagée.</span><span class="sxs-lookup"><span data-stu-id="64b7e-115">A folder's entry identifier can become invalid if a user deletes the folder or if the message store becomes corrupted.</span></span>
  
<span data-ttu-id="64b7e-116">Un ou plusieurs des indicateurs suivants peuvent être définis pour le masque de masques:</span><span class="sxs-lookup"><span data-stu-id="64b7e-116">One or more of the following flags can be set for the bitmask:</span></span> 
  
<span data-ttu-id="64b7e-117">FOLDER_COMMON_VIEWS_VALID</span><span class="sxs-lookup"><span data-stu-id="64b7e-117">FOLDER_COMMON_VIEWS_VALID</span></span> 
  
> <span data-ttu-id="64b7e-118">Le dossier des affichages communs a un identificateur d'entrée valide.</span><span class="sxs-lookup"><span data-stu-id="64b7e-118">The common views folder has a valid entry identifier.</span></span> <span data-ttu-id="64b7e-119">Voir **PR_COMMON_VIEWS_ENTRYID** ([PidTagCommonViewsEntryId](pidtagcommonviewsentryid-canonical-property.md)).</span><span class="sxs-lookup"><span data-stu-id="64b7e-119">See **PR_COMMON_VIEWS_ENTRYID** ([PidTagCommonViewsEntryId](pidtagcommonviewsentryid-canonical-property.md)).</span></span>
    
<span data-ttu-id="64b7e-120">FOLDER_FINDER_VALID</span><span class="sxs-lookup"><span data-stu-id="64b7e-120">FOLDER_FINDER_VALID</span></span> 
  
> <span data-ttu-id="64b7e-121">Le dossier Finder a un identificateur d'entrée valide.</span><span class="sxs-lookup"><span data-stu-id="64b7e-121">The finder folder has a valid entry identifier.</span></span> <span data-ttu-id="64b7e-122">Voir **PR_FINDER_ENTRYID** ([PidTagFinderEntryId](pidtagfinderentryid-canonical-property.md)).</span><span class="sxs-lookup"><span data-stu-id="64b7e-122">See **PR_FINDER_ENTRYID** ([PidTagFinderEntryId](pidtagfinderentryid-canonical-property.md)).</span></span> 
    
<span data-ttu-id="64b7e-123">FOLDER_IPM_INBOX_VALID</span><span class="sxs-lookup"><span data-stu-id="64b7e-123">FOLDER_IPM_INBOX_VALID</span></span> 
  
> <span data-ttu-id="64b7e-124">Le dossier de réception de message interpersonnes (IPM) a un identificateur d'entrée valide.</span><span class="sxs-lookup"><span data-stu-id="64b7e-124">The interpersonal message (IPM) receive folder has a valid entry identifier.</span></span> <span data-ttu-id="64b7e-125">Voir [IMsgStore:: GetReceiveFolder](imsgstore-getreceivefolder.md).</span><span class="sxs-lookup"><span data-stu-id="64b7e-125">See [IMsgStore::GetReceiveFolder](imsgstore-getreceivefolder.md).</span></span> 
    
<span data-ttu-id="64b7e-126">FOLDER_IPM_OUTBOX_VALID</span><span class="sxs-lookup"><span data-stu-id="64b7e-126">FOLDER_IPM_OUTBOX_VALID</span></span> 
  
> <span data-ttu-id="64b7e-127">Le dossier boîte d'envoi IPM a un identificateur d'entrée valide.</span><span class="sxs-lookup"><span data-stu-id="64b7e-127">The IPM Outbox folder has a valid entry identifier.</span></span> <span data-ttu-id="64b7e-128">Voir **PR_IPM_OUTBOX_ENTRYID** ([PidTagIpmOutboxEntryId](pidtagipmoutboxentryid-canonical-property.md)).</span><span class="sxs-lookup"><span data-stu-id="64b7e-128">See **PR_IPM_OUTBOX_ENTRYID** ([PidTagIpmOutboxEntryId](pidtagipmoutboxentryid-canonical-property.md)).</span></span> 
    
<span data-ttu-id="64b7e-129">FOLDER_IPM_SENTMAIL_VALID</span><span class="sxs-lookup"><span data-stu-id="64b7e-129">FOLDER_IPM_SENTMAIL_VALID</span></span> 
  
> <span data-ttu-id="64b7e-130">Le dossier éléments envoyés par IPM a un identificateur d'entrée valide.</span><span class="sxs-lookup"><span data-stu-id="64b7e-130">The IPM Sent Items folder has a valid entry identifier.</span></span> <span data-ttu-id="64b7e-131">Voir **PR_IPM_SENTMAIL_ENTRYID** ([PidTagIpmSentMailEntryId](pidtagipmsentmailentryid-canonical-property.md)).</span><span class="sxs-lookup"><span data-stu-id="64b7e-131">See **PR_IPM_SENTMAIL_ENTRYID** ([PidTagIpmSentMailEntryId](pidtagipmsentmailentryid-canonical-property.md)).</span></span>
    
<span data-ttu-id="64b7e-132">FOLDER_IPM_SUBTREE_VALID</span><span class="sxs-lookup"><span data-stu-id="64b7e-132">FOLDER_IPM_SUBTREE_VALID</span></span> 
  
> <span data-ttu-id="64b7e-133">La sous-arborescence du dossier IPM a un identificateur d'entrée valide.</span><span class="sxs-lookup"><span data-stu-id="64b7e-133">The IPM folder subtree has a valid entry identifier.</span></span> <span data-ttu-id="64b7e-134">Voir **PR_IPM_SUBTREE_ENTRYID** ([PidTagIpmSubtreeEntryId](pidtagipmsubtreeentryid-canonical-property.md)).</span><span class="sxs-lookup"><span data-stu-id="64b7e-134">See **PR_IPM_SUBTREE_ENTRYID** ([PidTagIpmSubtreeEntryId](pidtagipmsubtreeentryid-canonical-property.md)).</span></span>
    
<span data-ttu-id="64b7e-135">FOLDER_IPM_WASTEBASKET_VALID</span><span class="sxs-lookup"><span data-stu-id="64b7e-135">FOLDER_IPM_WASTEBASKET_VALID</span></span> 
  
> <span data-ttu-id="64b7e-136">Le dossier éléments supprimés IPM a un identificateur d'entrée valide.</span><span class="sxs-lookup"><span data-stu-id="64b7e-136">The IPM Deleted Items folder has a valid entry identifier.</span></span> <span data-ttu-id="64b7e-137">Voir **PR_IPM_WASTEBASKET_ENTRYID** ([PidTagIpmWastebasketEntryId](pidtagipmwastebasketentryid-canonical-property.md)).</span><span class="sxs-lookup"><span data-stu-id="64b7e-137">See **PR_IPM_WASTEBASKET_ENTRYID** ([PidTagIpmWastebasketEntryId](pidtagipmwastebasketentryid-canonical-property.md)).</span></span>
    
<span data-ttu-id="64b7e-138">FOLDER_VIEWS_VALID</span><span class="sxs-lookup"><span data-stu-id="64b7e-138">FOLDER_VIEWS_VALID</span></span> 
  
> <span data-ttu-id="64b7e-139">Le dossier views a un identificateur d'entrée valide.</span><span class="sxs-lookup"><span data-stu-id="64b7e-139">The views folder has a valid entry identifier.</span></span> <span data-ttu-id="64b7e-140">Voir **PR_VIEWS_ENTRYID** ([PidTagViewsEntryId](pidtagviewsentryid-canonical-property.md)).</span><span class="sxs-lookup"><span data-stu-id="64b7e-140">See **PR_VIEWS_ENTRYID** ([PidTagViewsEntryId](pidtagviewsentryid-canonical-property.md)).</span></span>
    
## <a name="related-resources"></a><span data-ttu-id="64b7e-141">Ressources associées</span><span class="sxs-lookup"><span data-stu-id="64b7e-141">Related resources</span></span>

### <a name="header-files"></a><span data-ttu-id="64b7e-142">Fichiers d'en-tête</span><span class="sxs-lookup"><span data-stu-id="64b7e-142">Header files</span></span>

<span data-ttu-id="64b7e-143">Mapidefs. h</span><span class="sxs-lookup"><span data-stu-id="64b7e-143">Mapidefs.h</span></span>
  
> <span data-ttu-id="64b7e-144">Fournit des définitions de type de données.</span><span class="sxs-lookup"><span data-stu-id="64b7e-144">Provides data type definitions.</span></span>
    
<span data-ttu-id="64b7e-145">Mapitags. h</span><span class="sxs-lookup"><span data-stu-id="64b7e-145">Mapitags.h</span></span>
  
> <span data-ttu-id="64b7e-146">Contient les définitions des propriétés figurant en tant que noms de substitution.</span><span class="sxs-lookup"><span data-stu-id="64b7e-146">Contains definitions of properties listed as alternate names.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="64b7e-147">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="64b7e-147">See also</span></span>



[<span data-ttu-id="64b7e-148">Propriétés MAPI</span><span class="sxs-lookup"><span data-stu-id="64b7e-148">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="64b7e-149">Propriétés canoniques MAPI</span><span class="sxs-lookup"><span data-stu-id="64b7e-149">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="64b7e-150">Mappage des noms de propriétés canoniques aux noms MAPI</span><span class="sxs-lookup"><span data-stu-id="64b7e-150">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="64b7e-151">Mappage des noms MAPI aux noms de propriétés canoniques</span><span class="sxs-lookup"><span data-stu-id="64b7e-151">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

