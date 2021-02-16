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
# <a name="imapifolder--imapicontainer"></a><span data-ttu-id="c32bc-103">IMAPIFolder : IMAPIContainer</span><span class="sxs-lookup"><span data-stu-id="c32bc-103">IMAPIFolder : IMAPIContainer</span></span>

  
  
<span data-ttu-id="c32bc-104">**S’applique à** : Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="c32bc-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="c32bc-105">Effectue des opérations sur les messages et sous-dossiers d’un dossier.</span><span class="sxs-lookup"><span data-stu-id="c32bc-105">Performs operations on the messages and subfolders in a folder.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="c32bc-106">Fichier d’en-tête :</span><span class="sxs-lookup"><span data-stu-id="c32bc-106">Header file:</span></span>  <br/> |<span data-ttu-id="c32bc-107">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="c32bc-107">Mapidefs.h</span></span>  <br/> |
|<span data-ttu-id="c32bc-108">Exposé par :</span><span class="sxs-lookup"><span data-stu-id="c32bc-108">Exposed by:</span></span>  <br/> |<span data-ttu-id="c32bc-109">Objets Folder</span><span class="sxs-lookup"><span data-stu-id="c32bc-109">Folder objects</span></span>  <br/> |
|<span data-ttu-id="c32bc-110">Implémenté par :</span><span class="sxs-lookup"><span data-stu-id="c32bc-110">Implemented by:</span></span>  <br/> |<span data-ttu-id="c32bc-111">Fournisseurs de magasins de messages</span><span class="sxs-lookup"><span data-stu-id="c32bc-111">Message store providers</span></span>  <br/> |
|<span data-ttu-id="c32bc-112">Appelé par :</span><span class="sxs-lookup"><span data-stu-id="c32bc-112">Called by:</span></span>  <br/> |<span data-ttu-id="c32bc-113">Applications clientes et MAPI</span><span class="sxs-lookup"><span data-stu-id="c32bc-113">Client applications and MAPI</span></span>  <br/> |
|<span data-ttu-id="c32bc-114">Identificateur d’interface :</span><span class="sxs-lookup"><span data-stu-id="c32bc-114">Interface identifier:</span></span>  <br/> |<span data-ttu-id="c32bc-115">IID_IMAPIFolder</span><span class="sxs-lookup"><span data-stu-id="c32bc-115">IID_IMAPIFolder</span></span>  <br/> |
|<span data-ttu-id="c32bc-116">Type de pointeur :</span><span class="sxs-lookup"><span data-stu-id="c32bc-116">Pointer type:</span></span>  <br/> |<span data-ttu-id="c32bc-117">LPMAPIFOLDER</span><span class="sxs-lookup"><span data-stu-id="c32bc-117">LPMAPIFOLDER</span></span>  <br/> |
|<span data-ttu-id="c32bc-118">Modèle de transaction :</span><span class="sxs-lookup"><span data-stu-id="c32bc-118">Transaction model:</span></span>  <br/> |<span data-ttu-id="c32bc-119">Non traduit</span><span class="sxs-lookup"><span data-stu-id="c32bc-119">Nontransacted</span></span>  <br/> |
   
## <a name="vtable-order"></a><span data-ttu-id="c32bc-120">Ordre des vtables</span><span class="sxs-lookup"><span data-stu-id="c32bc-120">Vtable order</span></span>

|||
|:-----|:-----|
|[<span data-ttu-id="c32bc-121">CreateMessage</span><span class="sxs-lookup"><span data-stu-id="c32bc-121">CreateMessage</span></span>](imapifolder-createmessage.md) <br/> |<span data-ttu-id="c32bc-122">Crée un message.</span><span class="sxs-lookup"><span data-stu-id="c32bc-122">Creates a new message.</span></span>  <br/> |
|[<span data-ttu-id="c32bc-123">CopyMessages</span><span class="sxs-lookup"><span data-stu-id="c32bc-123">CopyMessages</span></span>](imapifolder-copymessages.md) <br/> |<span data-ttu-id="c32bc-124">Copie ou déplace un ou plusieurs messages.</span><span class="sxs-lookup"><span data-stu-id="c32bc-124">Copies or moves one or more messages.</span></span>  <br/> |
|[<span data-ttu-id="c32bc-125">DeleteMessages</span><span class="sxs-lookup"><span data-stu-id="c32bc-125">DeleteMessages</span></span>](imapifolder-deletemessages.md) <br/> |<span data-ttu-id="c32bc-126">Supprime un ou plusieurs messages.</span><span class="sxs-lookup"><span data-stu-id="c32bc-126">Deletes one or more messages.</span></span>  <br/> |
|[<span data-ttu-id="c32bc-127">CreateFolder</span><span class="sxs-lookup"><span data-stu-id="c32bc-127">CreateFolder</span></span>](imapifolder-createfolder.md) <br/> |<span data-ttu-id="c32bc-128">Crée un sous-ensemble.</span><span class="sxs-lookup"><span data-stu-id="c32bc-128">Creates a new subfolder.</span></span>  <br/> |
|[<span data-ttu-id="c32bc-129">CopyFolder</span><span class="sxs-lookup"><span data-stu-id="c32bc-129">CopyFolder</span></span>](imapifolder-copyfolder.md) <br/> |<span data-ttu-id="c32bc-130">Copie ou déplace un sous-folder.</span><span class="sxs-lookup"><span data-stu-id="c32bc-130">Copies or moves a subfolder.</span></span>  <br/> |
|[<span data-ttu-id="c32bc-131">DeleteFolder</span><span class="sxs-lookup"><span data-stu-id="c32bc-131">DeleteFolder</span></span>](imapifolder-deletefolder.md) <br/> |<span data-ttu-id="c32bc-132">Supprime un sous-folder.</span><span class="sxs-lookup"><span data-stu-id="c32bc-132">Deletes a subfolder.</span></span>  <br/> |
|[<span data-ttu-id="c32bc-133">SetReadFlags</span><span class="sxs-lookup"><span data-stu-id="c32bc-133">SetReadFlags</span></span>](imapifolder-setreadflags.md) <br/> |<span data-ttu-id="c32bc-134">Définit ou désine l’indicateur MSGFLAG_READ dans la propriété **PR_MESSAGE_FLAGS** ([PidTagMessageFlags](pidtagmessageflags-canonical-property.md)) d’un ou plusieurs messages du dossier et gère l’envoi de rapports de lecture.</span><span class="sxs-lookup"><span data-stu-id="c32bc-134">Sets or clears the MSGFLAG_READ flag in the **PR_MESSAGE_FLAGS** ([PidTagMessageFlags](pidtagmessageflags-canonical-property.md)) property of one or more of the folder's messages, and manages the sending of read reports.</span></span>  <br/> |
|[<span data-ttu-id="c32bc-135">GetMessageStatus</span><span class="sxs-lookup"><span data-stu-id="c32bc-135">GetMessageStatus</span></span>](imapifolder-getmessagestatus.md) <br/> |<span data-ttu-id="c32bc-136">Obtient l’état associé à un message dans un dossier particulier.</span><span class="sxs-lookup"><span data-stu-id="c32bc-136">Obtains the status associated with a message in a particular folder.</span></span>  <br/> |
|[<span data-ttu-id="c32bc-137">SetMessageStatus</span><span class="sxs-lookup"><span data-stu-id="c32bc-137">SetMessageStatus</span></span>](imapifolder-setmessagestatus.md) <br/> |<span data-ttu-id="c32bc-138">Définit l’état associé à un message.</span><span class="sxs-lookup"><span data-stu-id="c32bc-138">Sets the status associated with a message.</span></span>  <br/> |
|[<span data-ttu-id="c32bc-139">SaveContentsSort</span><span class="sxs-lookup"><span data-stu-id="c32bc-139">SaveContentsSort</span></span>](imapifolder-savecontentssort.md) <br/> |<span data-ttu-id="c32bc-140">Définit l’ordre de tri par défaut pour la table des matières d’un dossier.</span><span class="sxs-lookup"><span data-stu-id="c32bc-140">Sets the default sort order for a folder's contents table.</span></span>  <br/> |
|[<span data-ttu-id="c32bc-141">EmptyFolder</span><span class="sxs-lookup"><span data-stu-id="c32bc-141">EmptyFolder</span></span>](imapifolder-emptyfolder.md) <br/> |<span data-ttu-id="c32bc-142">Supprime tous les messages et sous-dossiers d’un dossier sans supprimer le dossier lui-même.</span><span class="sxs-lookup"><span data-stu-id="c32bc-142">Deletes all messages and subfolders from a folder without deleting the folder itself.</span></span>  <br/> |
   
|<span data-ttu-id="c32bc-143">**Propriétés requises**</span><span class="sxs-lookup"><span data-stu-id="c32bc-143">**Required properties**</span></span>|<span data-ttu-id="c32bc-144">**Access**</span><span class="sxs-lookup"><span data-stu-id="c32bc-144">**Access**</span></span>|
|:-----|:-----|
|<span data-ttu-id="c32bc-145">**PR_DISPLAY_NAME** ([PidTagDisplayNamePrefix](pidtagdisplaynameprefix-canonical-property.md))</span><span class="sxs-lookup"><span data-stu-id="c32bc-145">**PR_DISPLAY_NAME** ([PidTagDisplayNamePrefix](pidtagdisplaynameprefix-canonical-property.md))</span></span>  <br/> |<span data-ttu-id="c32bc-146">Lecture/écriture</span><span class="sxs-lookup"><span data-stu-id="c32bc-146">Read/write</span></span>  <br/> |
|<span data-ttu-id="c32bc-147">**PR_ENTRYID** ([PidTagEntryId](pidtagentryid-canonical-property.md))</span><span class="sxs-lookup"><span data-stu-id="c32bc-147">**PR_ENTRYID** ([PidTagEntryId](pidtagentryid-canonical-property.md))</span></span>  <br/> |<span data-ttu-id="c32bc-148">Lecture seule</span><span class="sxs-lookup"><span data-stu-id="c32bc-148">Read-only</span></span>  <br/> |
|<span data-ttu-id="c32bc-149">**PR_FOLDER_TYPE** ([PidTagFolderType](pidtagfoldertype-canonical-property.md))</span><span class="sxs-lookup"><span data-stu-id="c32bc-149">**PR_FOLDER_TYPE** ([PidTagFolderType](pidtagfoldertype-canonical-property.md))</span></span>  <br/> |<span data-ttu-id="c32bc-150">Lecture/écriture</span><span class="sxs-lookup"><span data-stu-id="c32bc-150">Read/write</span></span>  <br/> |
|<span data-ttu-id="c32bc-151">**PR_OBJECT_TYPE** ([PidTagObjectType](pidtagobjecttype-canonical-property.md))</span><span class="sxs-lookup"><span data-stu-id="c32bc-151">**PR_OBJECT_TYPE** ([PidTagObjectType](pidtagobjecttype-canonical-property.md))</span></span>  <br/> |<span data-ttu-id="c32bc-152">Lecture seule</span><span class="sxs-lookup"><span data-stu-id="c32bc-152">Read-only</span></span>  <br/> |
|<span data-ttu-id="c32bc-153">**PR_PARENT_ENTRYID** ([PidTagParentEntryId](pidtagparententryid-canonical-property.md))</span><span class="sxs-lookup"><span data-stu-id="c32bc-153">**PR_PARENT_ENTRYID** ([PidTagParentEntryId](pidtagparententryid-canonical-property.md))</span></span>  <br/> |<span data-ttu-id="c32bc-154">Lecture seule</span><span class="sxs-lookup"><span data-stu-id="c32bc-154">Read-only</span></span>  <br/> |
|<span data-ttu-id="c32bc-155">**PR_RECORD_KEY** ([PidTagRecordKey](pidtagrecordkey-canonical-property.md))</span><span class="sxs-lookup"><span data-stu-id="c32bc-155">**PR_RECORD_KEY** ([PidTagRecordKey](pidtagrecordkey-canonical-property.md))</span></span>  <br/> |<span data-ttu-id="c32bc-156">Lecture seule</span><span class="sxs-lookup"><span data-stu-id="c32bc-156">Read-only</span></span>  <br/> |
|<span data-ttu-id="c32bc-157">**PR_STORE_ENTRYID** ([PidTagStoreEntryId](pidtagstoreentryid-canonical-property.md))</span><span class="sxs-lookup"><span data-stu-id="c32bc-157">**PR_STORE_ENTRYID** ([PidTagStoreEntryId](pidtagstoreentryid-canonical-property.md))</span></span>  <br/> |<span data-ttu-id="c32bc-158">Lecture seule</span><span class="sxs-lookup"><span data-stu-id="c32bc-158">Read-only</span></span>  <br/> |
|<span data-ttu-id="c32bc-159">**PR_STORE_RECORD_KEY** ([PidTagStoreRecordKey](pidtagstorerecordkey-canonical-property.md))</span><span class="sxs-lookup"><span data-stu-id="c32bc-159">**PR_STORE_RECORD_KEY** ([PidTagStoreRecordKey](pidtagstorerecordkey-canonical-property.md))</span></span>  <br/> |<span data-ttu-id="c32bc-160">Lecture seule</span><span class="sxs-lookup"><span data-stu-id="c32bc-160">Read-only</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="c32bc-161">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="c32bc-161">See also</span></span>



[<span data-ttu-id="c32bc-162">Interfaces MAPI</span><span class="sxs-lookup"><span data-stu-id="c32bc-162">MAPI Interfaces</span></span>](mapi-interfaces.md)

