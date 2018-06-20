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
ms.openlocfilehash: ae09723c78fe4e333fb5c46e8c79da4b77c0b331
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19786912"
---
# <a name="pidtagvalidfoldermask-canonical-property"></a><span data-ttu-id="8fbe7-103">Propriété canonique PidTagValidFolderMask</span><span class="sxs-lookup"><span data-stu-id="8fbe7-103">PidTagValidFolderMask Canonical Property</span></span>

  
  
<span data-ttu-id="8fbe7-104">**S’applique à**: Outlook</span><span class="sxs-lookup"><span data-stu-id="8fbe7-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="8fbe7-105">Contient un masque binaire composé des indicateurs qui influencent la validité des identificateurs d’entrée des dossiers dans une banque de messages.</span><span class="sxs-lookup"><span data-stu-id="8fbe7-105">Contains a bitmask of flags that indicate the validity of the entry identifiers of the folders in a message store.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="8fbe7-106">Propriétés associées :</span><span class="sxs-lookup"><span data-stu-id="8fbe7-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="8fbe7-107">PR_VALID_FOLDER_MASK</span><span class="sxs-lookup"><span data-stu-id="8fbe7-107">PR_VALID_FOLDER_MASK</span></span>  <br/> |
|<span data-ttu-id="8fbe7-108">Identificateur :</span><span class="sxs-lookup"><span data-stu-id="8fbe7-108">Identifier:</span></span>  <br/> |<span data-ttu-id="8fbe7-109">0x35DF</span><span class="sxs-lookup"><span data-stu-id="8fbe7-109">0x35DF</span></span>  <br/> |
|<span data-ttu-id="8fbe7-110">Type de données :</span><span class="sxs-lookup"><span data-stu-id="8fbe7-110">Data type:</span></span>  <br/> |<span data-ttu-id="8fbe7-111">PT_LONG</span><span class="sxs-lookup"><span data-stu-id="8fbe7-111">PT_LONG</span></span>  <br/> |
|<span data-ttu-id="8fbe7-112">Zone :</span><span class="sxs-lookup"><span data-stu-id="8fbe7-112">Area:</span></span>  <br/> |<span data-ttu-id="8fbe7-113">Banque de messages MAPI</span><span class="sxs-lookup"><span data-stu-id="8fbe7-113">MAPI message store</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="8fbe7-114">Remarques</span><span class="sxs-lookup"><span data-stu-id="8fbe7-114">Remarks</span></span>

<span data-ttu-id="8fbe7-115">Identificateur d’entrée d’un dossier peut devenir non valide si un utilisateur supprime le dossier ou si la banque de messages est corrompue.</span><span class="sxs-lookup"><span data-stu-id="8fbe7-115">A folder's entry identifier can become invalid if a user deletes the folder or if the message store becomes corrupted.</span></span>
  
<span data-ttu-id="8fbe7-116">Un ou plusieurs des indicateurs suivants peuvent être définies pour le masque de bits :</span><span class="sxs-lookup"><span data-stu-id="8fbe7-116">One or more of the following flags can be set for the bitmask:</span></span> 
  
<span data-ttu-id="8fbe7-117">FOLDER_COMMON_VIEWS_VALID</span><span class="sxs-lookup"><span data-stu-id="8fbe7-117">FOLDER_COMMON_VIEWS_VALID</span></span> 
  
> <span data-ttu-id="8fbe7-118">Le dossier views courantes possède un identificateur d’entrée valide.</span><span class="sxs-lookup"><span data-stu-id="8fbe7-118">The common views folder has a valid entry identifier.</span></span> <span data-ttu-id="8fbe7-119">Voir **PR_COMMON_VIEWS_ENTRYID** ([PidTagCommonViewsEntryId](pidtagcommonviewsentryid-canonical-property.md)).</span><span class="sxs-lookup"><span data-stu-id="8fbe7-119">See **PR_COMMON_VIEWS_ENTRYID** ([PidTagCommonViewsEntryId](pidtagcommonviewsentryid-canonical-property.md)).</span></span>
    
<span data-ttu-id="8fbe7-120">FOLDER_FINDER_VALID</span><span class="sxs-lookup"><span data-stu-id="8fbe7-120">FOLDER_FINDER_VALID</span></span> 
  
> <span data-ttu-id="8fbe7-121">Le dossier de recherche a un identificateur d’entrée valide.</span><span class="sxs-lookup"><span data-stu-id="8fbe7-121">The finder folder has a valid entry identifier.</span></span> <span data-ttu-id="8fbe7-122">Voir **PR_FINDER_ENTRYID** ([PidTagFinderEntryId](pidtagfinderentryid-canonical-property.md)).</span><span class="sxs-lookup"><span data-stu-id="8fbe7-122">See **PR_FINDER_ENTRYID** ([PidTagFinderEntryId](pidtagfinderentryid-canonical-property.md)).</span></span> 
    
<span data-ttu-id="8fbe7-123">FOLDER_IPM_INBOX_VALID</span><span class="sxs-lookup"><span data-stu-id="8fbe7-123">FOLDER_IPM_INBOX_VALID</span></span> 
  
> <span data-ttu-id="8fbe7-124">Recevoir le message interpersonnel (IPM) dossier possède un identificateur d’entrée valide.</span><span class="sxs-lookup"><span data-stu-id="8fbe7-124">The interpersonal message (IPM) receive folder has a valid entry identifier.</span></span> <span data-ttu-id="8fbe7-125">Voir [IMsgStore::GetReceiveFolder](imsgstore-getreceivefolder.md).</span><span class="sxs-lookup"><span data-stu-id="8fbe7-125">See [IMsgStore::GetReceiveFolder](imsgstore-getreceivefolder.md).</span></span> 
    
<span data-ttu-id="8fbe7-126">FOLDER_IPM_OUTBOX_VALID</span><span class="sxs-lookup"><span data-stu-id="8fbe7-126">FOLDER_IPM_OUTBOX_VALID</span></span> 
  
> <span data-ttu-id="8fbe7-127">Le dossier boîte d’envoi de l’IPM possède un identificateur d’entrée valide.</span><span class="sxs-lookup"><span data-stu-id="8fbe7-127">The IPM Outbox folder has a valid entry identifier.</span></span> <span data-ttu-id="8fbe7-128">Voir **PR_IPM_OUTBOX_ENTRYID** ([PidTagIpmOutboxEntryId](pidtagipmoutboxentryid-canonical-property.md)).</span><span class="sxs-lookup"><span data-stu-id="8fbe7-128">See **PR_IPM_OUTBOX_ENTRYID** ([PidTagIpmOutboxEntryId](pidtagipmoutboxentryid-canonical-property.md)).</span></span> 
    
<span data-ttu-id="8fbe7-129">FOLDER_IPM_SENTMAIL_VALID</span><span class="sxs-lookup"><span data-stu-id="8fbe7-129">FOLDER_IPM_SENTMAIL_VALID</span></span> 
  
> <span data-ttu-id="8fbe7-130">Le dossier éléments envoyés de IPM possède un identificateur d’entrée valide.</span><span class="sxs-lookup"><span data-stu-id="8fbe7-130">The IPM Sent Items folder has a valid entry identifier.</span></span> <span data-ttu-id="8fbe7-131">Voir **PR_IPM_SENTMAIL_ENTRYID** ([PidTagIpmSentMailEntryId](pidtagipmsentmailentryid-canonical-property.md)).</span><span class="sxs-lookup"><span data-stu-id="8fbe7-131">See **PR_IPM_SENTMAIL_ENTRYID** ([PidTagIpmSentMailEntryId](pidtagipmsentmailentryid-canonical-property.md)).</span></span>
    
<span data-ttu-id="8fbe7-132">FOLDER_IPM_SUBTREE_VALID</span><span class="sxs-lookup"><span data-stu-id="8fbe7-132">FOLDER_IPM_SUBTREE_VALID</span></span> 
  
> <span data-ttu-id="8fbe7-133">La sous-arborescence de dossier IPM possède un identificateur d’entrée valide.</span><span class="sxs-lookup"><span data-stu-id="8fbe7-133">The IPM folder subtree has a valid entry identifier.</span></span> <span data-ttu-id="8fbe7-134">Voir **PR_IPM_SUBTREE_ENTRYID** ([PidTagIpmSubtreeEntryId](pidtagipmsubtreeentryid-canonical-property.md)).</span><span class="sxs-lookup"><span data-stu-id="8fbe7-134">See **PR_IPM_SUBTREE_ENTRYID** ([PidTagIpmSubtreeEntryId](pidtagipmsubtreeentryid-canonical-property.md)).</span></span>
    
<span data-ttu-id="8fbe7-135">FOLDER_IPM_WASTEBASKET_VALID</span><span class="sxs-lookup"><span data-stu-id="8fbe7-135">FOLDER_IPM_WASTEBASKET_VALID</span></span> 
  
> <span data-ttu-id="8fbe7-136">Le dossier éléments supprimés de IPM possède un identificateur d’entrée valide.</span><span class="sxs-lookup"><span data-stu-id="8fbe7-136">The IPM Deleted Items folder has a valid entry identifier.</span></span> <span data-ttu-id="8fbe7-137">Voir **PR_IPM_WASTEBASKET_ENTRYID** ([PidTagIpmWastebasketEntryId](pidtagipmwastebasketentryid-canonical-property.md)).</span><span class="sxs-lookup"><span data-stu-id="8fbe7-137">See **PR_IPM_WASTEBASKET_ENTRYID** ([PidTagIpmWastebasketEntryId](pidtagipmwastebasketentryid-canonical-property.md)).</span></span>
    
<span data-ttu-id="8fbe7-138">FOLDER_VIEWS_VALID</span><span class="sxs-lookup"><span data-stu-id="8fbe7-138">FOLDER_VIEWS_VALID</span></span> 
  
> <span data-ttu-id="8fbe7-139">Le dossier views possède un identificateur d’entrée valide.</span><span class="sxs-lookup"><span data-stu-id="8fbe7-139">The views folder has a valid entry identifier.</span></span> <span data-ttu-id="8fbe7-140">Voir **PR_VIEWS_ENTRYID** ([PidTagViewsEntryId](pidtagviewsentryid-canonical-property.md)).</span><span class="sxs-lookup"><span data-stu-id="8fbe7-140">See **PR_VIEWS_ENTRYID** ([PidTagViewsEntryId](pidtagviewsentryid-canonical-property.md)).</span></span>
    
## <a name="related-resources"></a><span data-ttu-id="8fbe7-141">Ressources connexes</span><span class="sxs-lookup"><span data-stu-id="8fbe7-141">Related resources</span></span>

### <a name="header-files"></a><span data-ttu-id="8fbe7-142">Fichiers d’en-tête</span><span class="sxs-lookup"><span data-stu-id="8fbe7-142">Header files</span></span>

<span data-ttu-id="8fbe7-143">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="8fbe7-143">Mapidefs.h</span></span>
  
> <span data-ttu-id="8fbe7-144">Fournit des définitions de type de données.</span><span class="sxs-lookup"><span data-stu-id="8fbe7-144">Provides data type definitions.</span></span>
    
<span data-ttu-id="8fbe7-145">MAPITAGS.h</span><span class="sxs-lookup"><span data-stu-id="8fbe7-145">Mapitags.h</span></span>
  
> <span data-ttu-id="8fbe7-146">Contient les définitions des propriétés répertoriées en tant que d’autres noms.</span><span class="sxs-lookup"><span data-stu-id="8fbe7-146">Contains definitions of properties listed as alternate names.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="8fbe7-147">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="8fbe7-147">See also</span></span>



[<span data-ttu-id="8fbe7-148">Propriétés MAPI</span><span class="sxs-lookup"><span data-stu-id="8fbe7-148">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="8fbe7-149">Propriétés canoniques MAPI</span><span class="sxs-lookup"><span data-stu-id="8fbe7-149">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="8fbe7-150">Mappage de noms de propriété canonique aux noms MAPI</span><span class="sxs-lookup"><span data-stu-id="8fbe7-150">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="8fbe7-151">Mappage de noms MAPI pour les noms de propriété canonique</span><span class="sxs-lookup"><span data-stu-id="8fbe7-151">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

