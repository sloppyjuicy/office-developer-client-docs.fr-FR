---
title: IMAPIFolder IMAPIContainer
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- IMAPIFolder
api_type:
- COM
ms.assetid: bc2e8d17-7687-43c2-8f01-b677703f7288
description: Dernière modification le 09 mars 2015
ms.openlocfilehash: 1886987515f3cafe38418960baa4b6fd89e3b6f2
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/23/2018
ms.locfileid: "22590798"
---
# <a name="imapifolder--imapicontainer"></a><span data-ttu-id="ac9f8-103">IMAPIFolder : IMAPIContainer</span><span class="sxs-lookup"><span data-stu-id="ac9f8-103">IMAPIFolder : IMAPIContainer</span></span>

  
  
<span data-ttu-id="ac9f8-104">**S’applique à**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="ac9f8-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="ac9f8-105">Effectue des opérations sur les messages et les sous-dossiers dans un dossier.</span><span class="sxs-lookup"><span data-stu-id="ac9f8-105">Performs operations on the messages and subfolders in a folder.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="ac9f8-106">Fichier d’en-tête :</span><span class="sxs-lookup"><span data-stu-id="ac9f8-106">Header file:</span></span>  <br/> |<span data-ttu-id="ac9f8-107">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="ac9f8-107">Mapidefs.h</span></span>  <br/> |
|<span data-ttu-id="ac9f8-108">Exposés par :</span><span class="sxs-lookup"><span data-stu-id="ac9f8-108">Exposed by:</span></span>  <br/> |<span data-ttu-id="ac9f8-109">Objets de dossier</span><span class="sxs-lookup"><span data-stu-id="ac9f8-109">Folder objects</span></span>  <br/> |
|<span data-ttu-id="ac9f8-110">Implémentée par :</span><span class="sxs-lookup"><span data-stu-id="ac9f8-110">Implemented by:</span></span>  <br/> |<span data-ttu-id="ac9f8-111">Fournisseurs de banque de messages</span><span class="sxs-lookup"><span data-stu-id="ac9f8-111">Message store providers</span></span>  <br/> |
|<span data-ttu-id="ac9f8-112">Appelée par :</span><span class="sxs-lookup"><span data-stu-id="ac9f8-112">Called by:</span></span>  <br/> |<span data-ttu-id="ac9f8-113">Les applications clientes et MAPI</span><span class="sxs-lookup"><span data-stu-id="ac9f8-113">Client applications and MAPI</span></span>  <br/> |
|<span data-ttu-id="ac9f8-114">Identificateur de l’interface :</span><span class="sxs-lookup"><span data-stu-id="ac9f8-114">Interface identifier:</span></span>  <br/> |<span data-ttu-id="ac9f8-115">IID_IMAPIFolder</span><span class="sxs-lookup"><span data-stu-id="ac9f8-115">IID_IMAPIFolder</span></span>  <br/> |
|<span data-ttu-id="ac9f8-116">Type de pointeur :</span><span class="sxs-lookup"><span data-stu-id="ac9f8-116">Pointer type:</span></span>  <br/> |<span data-ttu-id="ac9f8-117">LPMAPIFOLDER</span><span class="sxs-lookup"><span data-stu-id="ac9f8-117">LPMAPIFOLDER</span></span>  <br/> |
|<span data-ttu-id="ac9f8-118">Modèle de transaction :</span><span class="sxs-lookup"><span data-stu-id="ac9f8-118">Transaction model:</span></span>  <br/> |<span data-ttu-id="ac9f8-119">Nontransacted</span><span class="sxs-lookup"><span data-stu-id="ac9f8-119">Nontransacted</span></span>  <br/> |
   
## <a name="vtable-order"></a><span data-ttu-id="ac9f8-120">Ordre vtable</span><span class="sxs-lookup"><span data-stu-id="ac9f8-120">Vtable order</span></span>

|||
|:-----|:-----|
|[<span data-ttu-id="ac9f8-121">CreateMessage</span><span class="sxs-lookup"><span data-stu-id="ac9f8-121">CreateMessage</span></span>](imapifolder-createmessage.md) <br/> |<span data-ttu-id="ac9f8-122">Crée un nouveau message.</span><span class="sxs-lookup"><span data-stu-id="ac9f8-122">Creates a new message.</span></span>  <br/> |
|[<span data-ttu-id="ac9f8-123">CopyMessages</span><span class="sxs-lookup"><span data-stu-id="ac9f8-123">CopyMessages</span></span>](imapifolder-copymessages.md) <br/> |<span data-ttu-id="ac9f8-124">Copie ou déplace un ou plusieurs messages.</span><span class="sxs-lookup"><span data-stu-id="ac9f8-124">Copies or moves one or more messages.</span></span>  <br/> |
|[<span data-ttu-id="ac9f8-125">DeleteMessages</span><span class="sxs-lookup"><span data-stu-id="ac9f8-125">DeleteMessages</span></span>](imapifolder-deletemessages.md) <br/> |<span data-ttu-id="ac9f8-126">Supprime un ou plusieurs messages.</span><span class="sxs-lookup"><span data-stu-id="ac9f8-126">Deletes one or more messages.</span></span>  <br/> |
|[<span data-ttu-id="ac9f8-127">CreateFolder</span><span class="sxs-lookup"><span data-stu-id="ac9f8-127">CreateFolder</span></span>](imapifolder-createfolder.md) <br/> |<span data-ttu-id="ac9f8-128">Crée un sous-dossier.</span><span class="sxs-lookup"><span data-stu-id="ac9f8-128">Creates a new subfolder.</span></span>  <br/> |
|[<span data-ttu-id="ac9f8-129">CopyFolder</span><span class="sxs-lookup"><span data-stu-id="ac9f8-129">CopyFolder</span></span>](imapifolder-copyfolder.md) <br/> |<span data-ttu-id="ac9f8-130">Copie ou déplace un sous-dossier.</span><span class="sxs-lookup"><span data-stu-id="ac9f8-130">Copies or moves a subfolder.</span></span>  <br/> |
|[<span data-ttu-id="ac9f8-131">DeleteFolder</span><span class="sxs-lookup"><span data-stu-id="ac9f8-131">DeleteFolder</span></span>](imapifolder-deletefolder.md) <br/> |<span data-ttu-id="ac9f8-132">Supprime un sous-dossier.</span><span class="sxs-lookup"><span data-stu-id="ac9f8-132">Deletes a subfolder.</span></span>  <br/> |
|[<span data-ttu-id="ac9f8-133">SetReadFlags</span><span class="sxs-lookup"><span data-stu-id="ac9f8-133">SetReadFlags</span></span>](imapifolder-setreadflags.md) <br/> |<span data-ttu-id="ac9f8-134">Définit ou supprime l’indicateur MSGFLAG_READ dans la propriété **PR_MESSAGE_FLAGS** ([PidTagMessageFlags](pidtagmessageflags-canonical-property.md)) d’un ou plusieurs des messages du dossier et gère l’envoi de rapports de lecture.</span><span class="sxs-lookup"><span data-stu-id="ac9f8-134">Sets or clears the MSGFLAG_READ flag in the **PR_MESSAGE_FLAGS** ([PidTagMessageFlags](pidtagmessageflags-canonical-property.md)) property of one or more of the folder's messages, and manages the sending of read reports.</span></span>  <br/> |
|[<span data-ttu-id="ac9f8-135">GetMessageStatus</span><span class="sxs-lookup"><span data-stu-id="ac9f8-135">GetMessageStatus</span></span>](imapifolder-getmessagestatus.md) <br/> |<span data-ttu-id="ac9f8-136">Obtient l’état d’un message dans un dossier spécifique.</span><span class="sxs-lookup"><span data-stu-id="ac9f8-136">Obtains the status associated with a message in a particular folder.</span></span>  <br/> |
|[<span data-ttu-id="ac9f8-137">SetMessageStatus</span><span class="sxs-lookup"><span data-stu-id="ac9f8-137">SetMessageStatus</span></span>](imapifolder-setmessagestatus.md) <br/> |<span data-ttu-id="ac9f8-138">Définit l’état d’un message.</span><span class="sxs-lookup"><span data-stu-id="ac9f8-138">Sets the status associated with a message.</span></span>  <br/> |
|[<span data-ttu-id="ac9f8-139">SaveContentsSort</span><span class="sxs-lookup"><span data-stu-id="ac9f8-139">SaveContentsSort</span></span>](imapifolder-savecontentssort.md) <br/> |<span data-ttu-id="ac9f8-140">Définit l’ordre de tri par défaut pour la table des matières d’un dossier.</span><span class="sxs-lookup"><span data-stu-id="ac9f8-140">Sets the default sort order for a folder's contents table.</span></span>  <br/> |
|[<span data-ttu-id="ac9f8-141">EmptyFolder</span><span class="sxs-lookup"><span data-stu-id="ac9f8-141">EmptyFolder</span></span>](imapifolder-emptyfolder.md) <br/> |<span data-ttu-id="ac9f8-142">Supprime tous les messages et les sous-dossiers d’un dossier sans supprimer le dossier proprement dit.</span><span class="sxs-lookup"><span data-stu-id="ac9f8-142">Deletes all messages and subfolders from a folder without deleting the folder itself.</span></span>  <br/> |
   
|<span data-ttu-id="ac9f8-143">**Propriétés requises**</span><span class="sxs-lookup"><span data-stu-id="ac9f8-143">**Required properties**</span></span>|<span data-ttu-id="ac9f8-144">**Access**</span><span class="sxs-lookup"><span data-stu-id="ac9f8-144">**Access**</span></span>|
|:-----|:-----|
|<span data-ttu-id="ac9f8-145">**PR_DISPLAY_NAME** ([PidTagDisplayNamePrefix](pidtagdisplaynameprefix-canonical-property.md))</span><span class="sxs-lookup"><span data-stu-id="ac9f8-145">**PR_DISPLAY_NAME** ([PidTagDisplayNamePrefix](pidtagdisplaynameprefix-canonical-property.md))</span></span>  <br/> |<span data-ttu-id="ac9f8-146">En lecture-écriture.</span><span class="sxs-lookup"><span data-stu-id="ac9f8-146">Read/write</span></span>  <br/> |
|<span data-ttu-id="ac9f8-147">**PR_ENTRYID** ([PidTagEntryId](pidtagentryid-canonical-property.md))</span><span class="sxs-lookup"><span data-stu-id="ac9f8-147">**PR_ENTRYID** ([PidTagEntryId](pidtagentryid-canonical-property.md))</span></span>  <br/> |<span data-ttu-id="ac9f8-148">Lecture seule</span><span class="sxs-lookup"><span data-stu-id="ac9f8-148">Read-only</span></span>  <br/> |
|<span data-ttu-id="ac9f8-149">**PR_FOLDER_TYPE** ([PidTagFolderType](pidtagfoldertype-canonical-property.md))</span><span class="sxs-lookup"><span data-stu-id="ac9f8-149">**PR_FOLDER_TYPE** ([PidTagFolderType](pidtagfoldertype-canonical-property.md))</span></span>  <br/> |<span data-ttu-id="ac9f8-150">En lecture-écriture.</span><span class="sxs-lookup"><span data-stu-id="ac9f8-150">Read/write</span></span>  <br/> |
|<span data-ttu-id="ac9f8-151">**PR_OBJECT_TYPE** ([PidTagObjectType](pidtagobjecttype-canonical-property.md))</span><span class="sxs-lookup"><span data-stu-id="ac9f8-151">**PR_OBJECT_TYPE** ([PidTagObjectType](pidtagobjecttype-canonical-property.md))</span></span>  <br/> |<span data-ttu-id="ac9f8-152">Lecture seule</span><span class="sxs-lookup"><span data-stu-id="ac9f8-152">Read-only</span></span>  <br/> |
|<span data-ttu-id="ac9f8-153">**PR_PARENT_ENTRYID** ([PidTagParentEntryId](pidtagparententryid-canonical-property.md))</span><span class="sxs-lookup"><span data-stu-id="ac9f8-153">**PR_PARENT_ENTRYID** ([PidTagParentEntryId](pidtagparententryid-canonical-property.md))</span></span>  <br/> |<span data-ttu-id="ac9f8-154">Lecture seule</span><span class="sxs-lookup"><span data-stu-id="ac9f8-154">Read-only</span></span>  <br/> |
|<span data-ttu-id="ac9f8-155">**PR_RECORD_KEY** ([PidTagRecordKey](pidtagrecordkey-canonical-property.md))</span><span class="sxs-lookup"><span data-stu-id="ac9f8-155">**PR_RECORD_KEY** ([PidTagRecordKey](pidtagrecordkey-canonical-property.md))</span></span>  <br/> |<span data-ttu-id="ac9f8-156">Lecture seule</span><span class="sxs-lookup"><span data-stu-id="ac9f8-156">Read-only</span></span>  <br/> |
|<span data-ttu-id="ac9f8-157">**PR_STORE_ENTRYID** ([PidTagStoreEntryId](pidtagstoreentryid-canonical-property.md))</span><span class="sxs-lookup"><span data-stu-id="ac9f8-157">**PR_STORE_ENTRYID** ([PidTagStoreEntryId](pidtagstoreentryid-canonical-property.md))</span></span>  <br/> |<span data-ttu-id="ac9f8-158">Lecture seule</span><span class="sxs-lookup"><span data-stu-id="ac9f8-158">Read-only</span></span>  <br/> |
|<span data-ttu-id="ac9f8-159">**PR_STORE_RECORD_KEY** ([PidTagStoreRecordKey](pidtagstorerecordkey-canonical-property.md))</span><span class="sxs-lookup"><span data-stu-id="ac9f8-159">**PR_STORE_RECORD_KEY** ([PidTagStoreRecordKey](pidtagstorerecordkey-canonical-property.md))</span></span>  <br/> |<span data-ttu-id="ac9f8-160">Lecture seule</span><span class="sxs-lookup"><span data-stu-id="ac9f8-160">Read-only</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="ac9f8-161">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="ac9f8-161">See also</span></span>



[<span data-ttu-id="ac9f8-162">Interfaces MAPI</span><span class="sxs-lookup"><span data-stu-id="ac9f8-162">MAPI Interfaces</span></span>](mapi-interfaces.md)

