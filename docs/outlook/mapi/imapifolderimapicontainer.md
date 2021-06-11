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
description: Dernière modification le 9 mars 2015
ms.openlocfilehash: 5e31896354141999e02f2cba117ef9739340be61
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/28/2019
ms.locfileid: "33424237"
---
# <a name="imapifolder--imapicontainer"></a><span data-ttu-id="3d4c9-103">IMAPIFolder : IMAPIContainer</span><span class="sxs-lookup"><span data-stu-id="3d4c9-103">IMAPIFolder : IMAPIContainer</span></span>

  
  
<span data-ttu-id="3d4c9-104">**S’applique à** : Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="3d4c9-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="3d4c9-105">Effectue des opérations sur les messages et sous-dossiers d’un dossier.</span><span class="sxs-lookup"><span data-stu-id="3d4c9-105">Performs operations on the messages and subfolders in a folder.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="3d4c9-106">Fichier d’en-tête :</span><span class="sxs-lookup"><span data-stu-id="3d4c9-106">Header file:</span></span>  <br/> |<span data-ttu-id="3d4c9-107">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="3d4c9-107">Mapidefs.h</span></span>  <br/> |
|<span data-ttu-id="3d4c9-108">Exposé par :</span><span class="sxs-lookup"><span data-stu-id="3d4c9-108">Exposed by:</span></span>  <br/> |<span data-ttu-id="3d4c9-109">Objets Folder</span><span class="sxs-lookup"><span data-stu-id="3d4c9-109">Folder objects</span></span>  <br/> |
|<span data-ttu-id="3d4c9-110">Implémenté par :</span><span class="sxs-lookup"><span data-stu-id="3d4c9-110">Implemented by:</span></span>  <br/> |<span data-ttu-id="3d4c9-111">Fournisseurs de magasins de messages</span><span class="sxs-lookup"><span data-stu-id="3d4c9-111">Message store providers</span></span>  <br/> |
|<span data-ttu-id="3d4c9-112">Appelé par :</span><span class="sxs-lookup"><span data-stu-id="3d4c9-112">Called by:</span></span>  <br/> |<span data-ttu-id="3d4c9-113">Applications clientes et MAPI</span><span class="sxs-lookup"><span data-stu-id="3d4c9-113">Client applications and MAPI</span></span>  <br/> |
|<span data-ttu-id="3d4c9-114">Identificateur d’interface :</span><span class="sxs-lookup"><span data-stu-id="3d4c9-114">Interface identifier:</span></span>  <br/> |<span data-ttu-id="3d4c9-115">IID_IMAPIFolder</span><span class="sxs-lookup"><span data-stu-id="3d4c9-115">IID_IMAPIFolder</span></span>  <br/> |
|<span data-ttu-id="3d4c9-116">Type de pointeur :</span><span class="sxs-lookup"><span data-stu-id="3d4c9-116">Pointer type:</span></span>  <br/> |<span data-ttu-id="3d4c9-117">LPMAPIFOLDER</span><span class="sxs-lookup"><span data-stu-id="3d4c9-117">LPMAPIFOLDER</span></span>  <br/> |
|<span data-ttu-id="3d4c9-118">Modèle de transaction :</span><span class="sxs-lookup"><span data-stu-id="3d4c9-118">Transaction model:</span></span>  <br/> |<span data-ttu-id="3d4c9-119">Non traduit</span><span class="sxs-lookup"><span data-stu-id="3d4c9-119">Nontransacted</span></span>  <br/> |
   
## <a name="vtable-order"></a><span data-ttu-id="3d4c9-120">Ordre des vtables</span><span class="sxs-lookup"><span data-stu-id="3d4c9-120">Vtable order</span></span>

|||
|:-----|:-----|
|[<span data-ttu-id="3d4c9-121">CreateMessage</span><span class="sxs-lookup"><span data-stu-id="3d4c9-121">CreateMessage</span></span>](imapifolder-createmessage.md) <br/> |<span data-ttu-id="3d4c9-122">Crée un message.</span><span class="sxs-lookup"><span data-stu-id="3d4c9-122">Creates a new message.</span></span>  <br/> |
|[<span data-ttu-id="3d4c9-123">CopyMessages</span><span class="sxs-lookup"><span data-stu-id="3d4c9-123">CopyMessages</span></span>](imapifolder-copymessages.md) <br/> |<span data-ttu-id="3d4c9-124">Copie ou déplace un ou plusieurs messages.</span><span class="sxs-lookup"><span data-stu-id="3d4c9-124">Copies or moves one or more messages.</span></span>  <br/> |
|[<span data-ttu-id="3d4c9-125">DeleteMessages</span><span class="sxs-lookup"><span data-stu-id="3d4c9-125">DeleteMessages</span></span>](imapifolder-deletemessages.md) <br/> |<span data-ttu-id="3d4c9-126">Supprime un ou plusieurs messages.</span><span class="sxs-lookup"><span data-stu-id="3d4c9-126">Deletes one or more messages.</span></span>  <br/> |
|[<span data-ttu-id="3d4c9-127">CreateFolder</span><span class="sxs-lookup"><span data-stu-id="3d4c9-127">CreateFolder</span></span>](imapifolder-createfolder.md) <br/> |<span data-ttu-id="3d4c9-128">Crée un sous-ensemble.</span><span class="sxs-lookup"><span data-stu-id="3d4c9-128">Creates a new subfolder.</span></span>  <br/> |
|[<span data-ttu-id="3d4c9-129">CopyFolder</span><span class="sxs-lookup"><span data-stu-id="3d4c9-129">CopyFolder</span></span>](imapifolder-copyfolder.md) <br/> |<span data-ttu-id="3d4c9-130">Copie ou déplace un sous-folder.</span><span class="sxs-lookup"><span data-stu-id="3d4c9-130">Copies or moves a subfolder.</span></span>  <br/> |
|[<span data-ttu-id="3d4c9-131">DeleteFolder</span><span class="sxs-lookup"><span data-stu-id="3d4c9-131">DeleteFolder</span></span>](imapifolder-deletefolder.md) <br/> |<span data-ttu-id="3d4c9-132">Supprime un sous-foldeur.</span><span class="sxs-lookup"><span data-stu-id="3d4c9-132">Deletes a subfolder.</span></span>  <br/> |
|[<span data-ttu-id="3d4c9-133">SetReadFlags</span><span class="sxs-lookup"><span data-stu-id="3d4c9-133">SetReadFlags</span></span>](imapifolder-setreadflags.md) <br/> |<span data-ttu-id="3d4c9-134">Définit ou désine l’indicateur MSGFLAG_READ dans la propriété **PR_MESSAGE_FLAGS** ([PidTagMessageFlags](pidtagmessageflags-canonical-property.md)) d’un ou plusieurs messages du dossier et gère l’envoi de rapports de lecture.</span><span class="sxs-lookup"><span data-stu-id="3d4c9-134">Sets or clears the MSGFLAG_READ flag in the **PR_MESSAGE_FLAGS** ([PidTagMessageFlags](pidtagmessageflags-canonical-property.md)) property of one or more of the folder's messages, and manages the sending of read reports.</span></span>  <br/> |
|[<span data-ttu-id="3d4c9-135">GetMessageStatus</span><span class="sxs-lookup"><span data-stu-id="3d4c9-135">GetMessageStatus</span></span>](imapifolder-getmessagestatus.md) <br/> |<span data-ttu-id="3d4c9-136">Obtient l’état associé à un message dans un dossier particulier.</span><span class="sxs-lookup"><span data-stu-id="3d4c9-136">Obtains the status associated with a message in a particular folder.</span></span>  <br/> |
|[<span data-ttu-id="3d4c9-137">SetMessageStatus</span><span class="sxs-lookup"><span data-stu-id="3d4c9-137">SetMessageStatus</span></span>](imapifolder-setmessagestatus.md) <br/> |<span data-ttu-id="3d4c9-138">Définit l’état associé à un message.</span><span class="sxs-lookup"><span data-stu-id="3d4c9-138">Sets the status associated with a message.</span></span>  <br/> |
|[<span data-ttu-id="3d4c9-139">SaveContentsSort</span><span class="sxs-lookup"><span data-stu-id="3d4c9-139">SaveContentsSort</span></span>](imapifolder-savecontentssort.md) <br/> |<span data-ttu-id="3d4c9-140">Définit l’ordre de tri par défaut pour la table des matières d’un dossier.</span><span class="sxs-lookup"><span data-stu-id="3d4c9-140">Sets the default sort order for a folder's contents table.</span></span>  <br/> |
|[<span data-ttu-id="3d4c9-141">EmptyFolder</span><span class="sxs-lookup"><span data-stu-id="3d4c9-141">EmptyFolder</span></span>](imapifolder-emptyfolder.md) <br/> |<span data-ttu-id="3d4c9-142">Supprime tous les messages et sous-dossiers d’un dossier sans supprimer le dossier lui-même.</span><span class="sxs-lookup"><span data-stu-id="3d4c9-142">Deletes all messages and subfolders from a folder without deleting the folder itself.</span></span>  <br/> |
   
|<span data-ttu-id="3d4c9-143">**Propriétés requises**</span><span class="sxs-lookup"><span data-stu-id="3d4c9-143">**Required properties**</span></span>|<span data-ttu-id="3d4c9-144">**Access**</span><span class="sxs-lookup"><span data-stu-id="3d4c9-144">**Access**</span></span>|
|:-----|:-----|
|<span data-ttu-id="3d4c9-145">**PR_DISPLAY_NAME** ([PidTagDisplayNamePrefix](pidtagdisplaynameprefix-canonical-property.md))</span><span class="sxs-lookup"><span data-stu-id="3d4c9-145">**PR_DISPLAY_NAME** ([PidTagDisplayNamePrefix](pidtagdisplaynameprefix-canonical-property.md))</span></span>  <br/> |<span data-ttu-id="3d4c9-146">Lecture/écriture</span><span class="sxs-lookup"><span data-stu-id="3d4c9-146">Read/write</span></span>  <br/> |
|<span data-ttu-id="3d4c9-147">**PR_ENTRYID** ([PidTagEntryId](pidtagentryid-canonical-property.md))</span><span class="sxs-lookup"><span data-stu-id="3d4c9-147">**PR_ENTRYID** ([PidTagEntryId](pidtagentryid-canonical-property.md))</span></span>  <br/> |<span data-ttu-id="3d4c9-148">Lecture seule</span><span class="sxs-lookup"><span data-stu-id="3d4c9-148">Read-only</span></span>  <br/> |
|<span data-ttu-id="3d4c9-149">**PR_FOLDER_TYPE** ([PidTagFolderType](pidtagfoldertype-canonical-property.md))</span><span class="sxs-lookup"><span data-stu-id="3d4c9-149">**PR_FOLDER_TYPE** ([PidTagFolderType](pidtagfoldertype-canonical-property.md))</span></span>  <br/> |<span data-ttu-id="3d4c9-150">Lecture/écriture</span><span class="sxs-lookup"><span data-stu-id="3d4c9-150">Read/write</span></span>  <br/> |
|<span data-ttu-id="3d4c9-151">**PR_OBJECT_TYPE** ([PidTagObjectType](pidtagobjecttype-canonical-property.md))</span><span class="sxs-lookup"><span data-stu-id="3d4c9-151">**PR_OBJECT_TYPE** ([PidTagObjectType](pidtagobjecttype-canonical-property.md))</span></span>  <br/> |<span data-ttu-id="3d4c9-152">Lecture seule</span><span class="sxs-lookup"><span data-stu-id="3d4c9-152">Read-only</span></span>  <br/> |
|<span data-ttu-id="3d4c9-153">**PR_PARENT_ENTRYID** ([PidTagParentEntryId](pidtagparententryid-canonical-property.md))</span><span class="sxs-lookup"><span data-stu-id="3d4c9-153">**PR_PARENT_ENTRYID** ([PidTagParentEntryId](pidtagparententryid-canonical-property.md))</span></span>  <br/> |<span data-ttu-id="3d4c9-154">Lecture seule</span><span class="sxs-lookup"><span data-stu-id="3d4c9-154">Read-only</span></span>  <br/> |
|<span data-ttu-id="3d4c9-155">**PR_RECORD_KEY** ([PidTagRecordKey](pidtagrecordkey-canonical-property.md))</span><span class="sxs-lookup"><span data-stu-id="3d4c9-155">**PR_RECORD_KEY** ([PidTagRecordKey](pidtagrecordkey-canonical-property.md))</span></span>  <br/> |<span data-ttu-id="3d4c9-156">Lecture seule</span><span class="sxs-lookup"><span data-stu-id="3d4c9-156">Read-only</span></span>  <br/> |
|<span data-ttu-id="3d4c9-157">**PR_STORE_ENTRYID** ([PidTagStoreEntryId](pidtagstoreentryid-canonical-property.md))</span><span class="sxs-lookup"><span data-stu-id="3d4c9-157">**PR_STORE_ENTRYID** ([PidTagStoreEntryId](pidtagstoreentryid-canonical-property.md))</span></span>  <br/> |<span data-ttu-id="3d4c9-158">Lecture seule</span><span class="sxs-lookup"><span data-stu-id="3d4c9-158">Read-only</span></span>  <br/> |
|<span data-ttu-id="3d4c9-159">**PR_STORE_RECORD_KEY** ([PidTagStoreRecordKey](pidtagstorerecordkey-canonical-property.md))</span><span class="sxs-lookup"><span data-stu-id="3d4c9-159">**PR_STORE_RECORD_KEY** ([PidTagStoreRecordKey](pidtagstorerecordkey-canonical-property.md))</span></span>  <br/> |<span data-ttu-id="3d4c9-160">Lecture seule</span><span class="sxs-lookup"><span data-stu-id="3d4c9-160">Read-only</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="3d4c9-161">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="3d4c9-161">See also</span></span>



[<span data-ttu-id="3d4c9-162">Interfaces MAPI</span><span class="sxs-lookup"><span data-stu-id="3d4c9-162">MAPI Interfaces</span></span>](mapi-interfaces.md)

