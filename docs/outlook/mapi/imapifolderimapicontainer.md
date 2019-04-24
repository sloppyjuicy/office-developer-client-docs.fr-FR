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
description: 'Derni�re modification�: lundi 9 mars 2015'
ms.openlocfilehash: 5e31896354141999e02f2cba117ef9739340be61
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32329490"
---
# <a name="imapifolder--imapicontainer"></a><span data-ttu-id="ef2fe-103">IMAPIFolder : IMAPIContainer</span><span class="sxs-lookup"><span data-stu-id="ef2fe-103">IMAPIFolder : IMAPIContainer</span></span>

  
  
<span data-ttu-id="ef2fe-104">**S’applique à** : Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="ef2fe-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="ef2fe-105">Effectue des opérations sur les messages et les sous-dossiers d'un dossier.</span><span class="sxs-lookup"><span data-stu-id="ef2fe-105">Performs operations on the messages and subfolders in a folder.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="ef2fe-106">Fichier d’en-tête :</span><span class="sxs-lookup"><span data-stu-id="ef2fe-106">Header file:</span></span>  <br/> |<span data-ttu-id="ef2fe-107">Mapidefs. h</span><span class="sxs-lookup"><span data-stu-id="ef2fe-107">Mapidefs.h</span></span>  <br/> |
|<span data-ttu-id="ef2fe-108">Exposé par:</span><span class="sxs-lookup"><span data-stu-id="ef2fe-108">Exposed by:</span></span>  <br/> |<span data-ttu-id="ef2fe-109">Objets Folder</span><span class="sxs-lookup"><span data-stu-id="ef2fe-109">Folder objects</span></span>  <br/> |
|<span data-ttu-id="ef2fe-110">Implémenté par :</span><span class="sxs-lookup"><span data-stu-id="ef2fe-110">Implemented by:</span></span>  <br/> |<span data-ttu-id="ef2fe-111">Fournisseurs de banques de messages</span><span class="sxs-lookup"><span data-stu-id="ef2fe-111">Message store providers</span></span>  <br/> |
|<span data-ttu-id="ef2fe-112">Appelé par :</span><span class="sxs-lookup"><span data-stu-id="ef2fe-112">Called by:</span></span>  <br/> |<span data-ttu-id="ef2fe-113">Applications clientes et MAPI</span><span class="sxs-lookup"><span data-stu-id="ef2fe-113">Client applications and MAPI</span></span>  <br/> |
|<span data-ttu-id="ef2fe-114">Identificateur de l'interface:</span><span class="sxs-lookup"><span data-stu-id="ef2fe-114">Interface identifier:</span></span>  <br/> |<span data-ttu-id="ef2fe-115">IID_IMAPIFolder</span><span class="sxs-lookup"><span data-stu-id="ef2fe-115">IID_IMAPIFolder</span></span>  <br/> |
|<span data-ttu-id="ef2fe-116">Type de pointeur:</span><span class="sxs-lookup"><span data-stu-id="ef2fe-116">Pointer type:</span></span>  <br/> |<span data-ttu-id="ef2fe-117">LPMAPIFOLDER</span><span class="sxs-lookup"><span data-stu-id="ef2fe-117">LPMAPIFOLDER</span></span>  <br/> |
|<span data-ttu-id="ef2fe-118">Modèle de transaction:</span><span class="sxs-lookup"><span data-stu-id="ef2fe-118">Transaction model:</span></span>  <br/> |<span data-ttu-id="ef2fe-119">Pas de transaction</span><span class="sxs-lookup"><span data-stu-id="ef2fe-119">Nontransacted</span></span>  <br/> |
   
## <a name="vtable-order"></a><span data-ttu-id="ef2fe-120">Ordre vtable</span><span class="sxs-lookup"><span data-stu-id="ef2fe-120">Vtable order</span></span>

|||
|:-----|:-----|
|[<span data-ttu-id="ef2fe-121">CreateMessage</span><span class="sxs-lookup"><span data-stu-id="ef2fe-121">CreateMessage</span></span>](imapifolder-createmessage.md) <br/> |<span data-ttu-id="ef2fe-122">Crée un message.</span><span class="sxs-lookup"><span data-stu-id="ef2fe-122">Creates a new message.</span></span>  <br/> |
|[<span data-ttu-id="ef2fe-123">CopyMessages</span><span class="sxs-lookup"><span data-stu-id="ef2fe-123">CopyMessages</span></span>](imapifolder-copymessages.md) <br/> |<span data-ttu-id="ef2fe-124">Copie ou déplace un ou plusieurs messages.</span><span class="sxs-lookup"><span data-stu-id="ef2fe-124">Copies or moves one or more messages.</span></span>  <br/> |
|[<span data-ttu-id="ef2fe-125">DeleteMessages</span><span class="sxs-lookup"><span data-stu-id="ef2fe-125">DeleteMessages</span></span>](imapifolder-deletemessages.md) <br/> |<span data-ttu-id="ef2fe-126">Supprime un ou plusieurs messages.</span><span class="sxs-lookup"><span data-stu-id="ef2fe-126">Deletes one or more messages.</span></span>  <br/> |
|[<span data-ttu-id="ef2fe-127">CreateFolder</span><span class="sxs-lookup"><span data-stu-id="ef2fe-127">CreateFolder</span></span>](imapifolder-createfolder.md) <br/> |<span data-ttu-id="ef2fe-128">Crée un sous-dossier.</span><span class="sxs-lookup"><span data-stu-id="ef2fe-128">Creates a new subfolder.</span></span>  <br/> |
|[<span data-ttu-id="ef2fe-129">CopyFolder</span><span class="sxs-lookup"><span data-stu-id="ef2fe-129">CopyFolder</span></span>](imapifolder-copyfolder.md) <br/> |<span data-ttu-id="ef2fe-130">Copie ou déplace un sous-dossier.</span><span class="sxs-lookup"><span data-stu-id="ef2fe-130">Copies or moves a subfolder.</span></span>  <br/> |
|[<span data-ttu-id="ef2fe-131">DeleteFolder</span><span class="sxs-lookup"><span data-stu-id="ef2fe-131">DeleteFolder</span></span>](imapifolder-deletefolder.md) <br/> |<span data-ttu-id="ef2fe-132">Supprime un sous-dossier.</span><span class="sxs-lookup"><span data-stu-id="ef2fe-132">Deletes a subfolder.</span></span>  <br/> |
|[<span data-ttu-id="ef2fe-133">SetReadFlags</span><span class="sxs-lookup"><span data-stu-id="ef2fe-133">SetReadFlags</span></span>](imapifolder-setreadflags.md) <br/> |<span data-ttu-id="ef2fe-134">Définit ou efface l'indicateur MSGFLAG_READ dans la propriété **PR_MESSAGE_FLAGS** ([PidTagMessageFlags](pidtagmessageflags-canonical-property.md)) d'un ou plusieurs des messages du dossier, et gère l'envoi des rapports de lecture.</span><span class="sxs-lookup"><span data-stu-id="ef2fe-134">Sets or clears the MSGFLAG_READ flag in the **PR_MESSAGE_FLAGS** ([PidTagMessageFlags](pidtagmessageflags-canonical-property.md)) property of one or more of the folder's messages, and manages the sending of read reports.</span></span>  <br/> |
|[<span data-ttu-id="ef2fe-135">GetMessageStatus</span><span class="sxs-lookup"><span data-stu-id="ef2fe-135">GetMessageStatus</span></span>](imapifolder-getmessagestatus.md) <br/> |<span data-ttu-id="ef2fe-136">Obtient l'état associé à un message dans un dossier particulier.</span><span class="sxs-lookup"><span data-stu-id="ef2fe-136">Obtains the status associated with a message in a particular folder.</span></span>  <br/> |
|[<span data-ttu-id="ef2fe-137">SetMessageStatus</span><span class="sxs-lookup"><span data-stu-id="ef2fe-137">SetMessageStatus</span></span>](imapifolder-setmessagestatus.md) <br/> |<span data-ttu-id="ef2fe-138">Définit l'état associé à un message.</span><span class="sxs-lookup"><span data-stu-id="ef2fe-138">Sets the status associated with a message.</span></span>  <br/> |
|[<span data-ttu-id="ef2fe-139">SaveContentsSort</span><span class="sxs-lookup"><span data-stu-id="ef2fe-139">SaveContentsSort</span></span>](imapifolder-savecontentssort.md) <br/> |<span data-ttu-id="ef2fe-140">Définit l'ordre de tri par défaut pour la table des matières d'un dossier.</span><span class="sxs-lookup"><span data-stu-id="ef2fe-140">Sets the default sort order for a folder's contents table.</span></span>  <br/> |
|[<span data-ttu-id="ef2fe-141">EmptyFolder</span><span class="sxs-lookup"><span data-stu-id="ef2fe-141">EmptyFolder</span></span>](imapifolder-emptyfolder.md) <br/> |<span data-ttu-id="ef2fe-142">Supprime tous les messages et sous-dossiers d'un dossier sans supprimer le dossier lui-même.</span><span class="sxs-lookup"><span data-stu-id="ef2fe-142">Deletes all messages and subfolders from a folder without deleting the folder itself.</span></span>  <br/> |
   
|<span data-ttu-id="ef2fe-143">**Propriétés requises**</span><span class="sxs-lookup"><span data-stu-id="ef2fe-143">**Required properties**</span></span>|<span data-ttu-id="ef2fe-144">**Access**</span><span class="sxs-lookup"><span data-stu-id="ef2fe-144">**Access**</span></span>|
|:-----|:-----|
|<span data-ttu-id="ef2fe-145">**PR_DISPLAY_NAME** ([PidTagDisplayNamePrefix](pidtagdisplaynameprefix-canonical-property.md))</span><span class="sxs-lookup"><span data-stu-id="ef2fe-145">**PR_DISPLAY_NAME** ([PidTagDisplayNamePrefix](pidtagdisplaynameprefix-canonical-property.md))</span></span>  <br/> |<span data-ttu-id="ef2fe-146">En lecture-écriture.</span><span class="sxs-lookup"><span data-stu-id="ef2fe-146">Read/write</span></span>  <br/> |
|<span data-ttu-id="ef2fe-147">**PR_ENTRYID** ([PidTagEntryId](pidtagentryid-canonical-property.md))</span><span class="sxs-lookup"><span data-stu-id="ef2fe-147">**PR_ENTRYID** ([PidTagEntryId](pidtagentryid-canonical-property.md))</span></span>  <br/> |<span data-ttu-id="ef2fe-148">Lecture seule</span><span class="sxs-lookup"><span data-stu-id="ef2fe-148">Read-only</span></span>  <br/> |
|<span data-ttu-id="ef2fe-149">**PR_FOLDER_TYPE** ([PidTagFolderType](pidtagfoldertype-canonical-property.md))</span><span class="sxs-lookup"><span data-stu-id="ef2fe-149">**PR_FOLDER_TYPE** ([PidTagFolderType](pidtagfoldertype-canonical-property.md))</span></span>  <br/> |<span data-ttu-id="ef2fe-150">En lecture-écriture.</span><span class="sxs-lookup"><span data-stu-id="ef2fe-150">Read/write</span></span>  <br/> |
|<span data-ttu-id="ef2fe-151">**PR_OBJECT_TYPE** ([PidTagObjectType](pidtagobjecttype-canonical-property.md))</span><span class="sxs-lookup"><span data-stu-id="ef2fe-151">**PR_OBJECT_TYPE** ([PidTagObjectType](pidtagobjecttype-canonical-property.md))</span></span>  <br/> |<span data-ttu-id="ef2fe-152">Lecture seule</span><span class="sxs-lookup"><span data-stu-id="ef2fe-152">Read-only</span></span>  <br/> |
|<span data-ttu-id="ef2fe-153">**PR_PARENT_ENTRYID** ([PidTagParentEntryId](pidtagparententryid-canonical-property.md))</span><span class="sxs-lookup"><span data-stu-id="ef2fe-153">**PR_PARENT_ENTRYID** ([PidTagParentEntryId](pidtagparententryid-canonical-property.md))</span></span>  <br/> |<span data-ttu-id="ef2fe-154">Lecture seule</span><span class="sxs-lookup"><span data-stu-id="ef2fe-154">Read-only</span></span>  <br/> |
|<span data-ttu-id="ef2fe-155">**PR_RECORD_KEY** ([PidTagRecordKey](pidtagrecordkey-canonical-property.md))</span><span class="sxs-lookup"><span data-stu-id="ef2fe-155">**PR_RECORD_KEY** ([PidTagRecordKey](pidtagrecordkey-canonical-property.md))</span></span>  <br/> |<span data-ttu-id="ef2fe-156">Lecture seule</span><span class="sxs-lookup"><span data-stu-id="ef2fe-156">Read-only</span></span>  <br/> |
|<span data-ttu-id="ef2fe-157">**PR_STORE_ENTRYID** ([PidTagStoreEntryId](pidtagstoreentryid-canonical-property.md))</span><span class="sxs-lookup"><span data-stu-id="ef2fe-157">**PR_STORE_ENTRYID** ([PidTagStoreEntryId](pidtagstoreentryid-canonical-property.md))</span></span>  <br/> |<span data-ttu-id="ef2fe-158">Lecture seule</span><span class="sxs-lookup"><span data-stu-id="ef2fe-158">Read-only</span></span>  <br/> |
|<span data-ttu-id="ef2fe-159">**PR_STORE_RECORD_KEY** ([PidTagStoreRecordKey](pidtagstorerecordkey-canonical-property.md))</span><span class="sxs-lookup"><span data-stu-id="ef2fe-159">**PR_STORE_RECORD_KEY** ([PidTagStoreRecordKey](pidtagstorerecordkey-canonical-property.md))</span></span>  <br/> |<span data-ttu-id="ef2fe-160">Lecture seule</span><span class="sxs-lookup"><span data-stu-id="ef2fe-160">Read-only</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="ef2fe-161">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="ef2fe-161">See also</span></span>



[<span data-ttu-id="ef2fe-162">Interfaces MAPI</span><span class="sxs-lookup"><span data-stu-id="ef2fe-162">MAPI Interfaces</span></span>](mapi-interfaces.md)

