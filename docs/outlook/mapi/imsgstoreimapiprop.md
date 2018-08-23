---
title: IMsgStore IMAPIProp
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- IMsgStore
api_type:
- COM
ms.assetid: 20090114-b183-4767-8971-a304a9aa47e6
description: Dernière modification le 09 mars 2015
ms.openlocfilehash: 4ed17fd7f826432da9460fe01e5aa76802726bad
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/23/2018
ms.locfileid: "22584631"
---
# <a name="imsgstore--imapiprop"></a><span data-ttu-id="cd9f3-103">IMsgStore : IMAPIProp</span><span class="sxs-lookup"><span data-stu-id="cd9f3-103">IMsgStore : IMAPIProp</span></span>

  
  
<span data-ttu-id="cd9f3-104">**S’applique à**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="cd9f3-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="cd9f3-105">Permet d’accéder aux informations de banque de messages et aux messages et des dossiers.</span><span class="sxs-lookup"><span data-stu-id="cd9f3-105">Provides access to message store information and to messages and folders.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="cd9f3-106">Fichier d’en-tête :</span><span class="sxs-lookup"><span data-stu-id="cd9f3-106">Header file:</span></span>  <br/> |<span data-ttu-id="cd9f3-107">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="cd9f3-107">Mapidefs.h</span></span>  <br/> |
|<span data-ttu-id="cd9f3-108">Exposés par :</span><span class="sxs-lookup"><span data-stu-id="cd9f3-108">Exposed by:</span></span>  <br/> |<span data-ttu-id="cd9f3-109">Objet store de message</span><span class="sxs-lookup"><span data-stu-id="cd9f3-109">Message store object</span></span>  <br/> |
|<span data-ttu-id="cd9f3-110">Implémentée par :</span><span class="sxs-lookup"><span data-stu-id="cd9f3-110">Implemented by:</span></span>  <br/> |<span data-ttu-id="cd9f3-111">Fournisseurs de banque de messages</span><span class="sxs-lookup"><span data-stu-id="cd9f3-111">Message store providers</span></span>  <br/> |
|<span data-ttu-id="cd9f3-112">Appelée par :</span><span class="sxs-lookup"><span data-stu-id="cd9f3-112">Called by:</span></span>  <br/> |<span data-ttu-id="cd9f3-113">Applications clientes, le spouleur MAPI et MAPI</span><span class="sxs-lookup"><span data-stu-id="cd9f3-113">Client applications, the MAPI spooler, and MAPI</span></span>  <br/> |
|<span data-ttu-id="cd9f3-114">Identificateur de l’interface :</span><span class="sxs-lookup"><span data-stu-id="cd9f3-114">Interface identifier:</span></span>  <br/> |<span data-ttu-id="cd9f3-115">IID_IMsgStore</span><span class="sxs-lookup"><span data-stu-id="cd9f3-115">IID_IMsgStore</span></span>  <br/> |
|<span data-ttu-id="cd9f3-116">Type de pointeur :</span><span class="sxs-lookup"><span data-stu-id="cd9f3-116">Pointer type:</span></span>  <br/> |<span data-ttu-id="cd9f3-117">IPMDB</span><span class="sxs-lookup"><span data-stu-id="cd9f3-117">LPMDB</span></span>  <br/> |
|<span data-ttu-id="cd9f3-118">Modèle de transaction :</span><span class="sxs-lookup"><span data-stu-id="cd9f3-118">Transaction model:</span></span>  <br/> |<span data-ttu-id="cd9f3-119">Nontransacted</span><span class="sxs-lookup"><span data-stu-id="cd9f3-119">Nontransacted</span></span>  <br/> |
   
## <a name="vtable-order"></a><span data-ttu-id="cd9f3-120">Ordre vtable</span><span class="sxs-lookup"><span data-stu-id="cd9f3-120">Vtable order</span></span>

|||
|:-----|:-----|
|[<span data-ttu-id="cd9f3-121">Conseiller</span><span class="sxs-lookup"><span data-stu-id="cd9f3-121">Advise</span></span>](imsgstore-advise.md) <br/> |<span data-ttu-id="cd9f3-122">Inscrit pour recevoir des notifications d’événements spécifiques qui affectent la banque de messages.</span><span class="sxs-lookup"><span data-stu-id="cd9f3-122">Registers to receive notification of specified events that affect the message store.</span></span>  <br/> |
|[<span data-ttu-id="cd9f3-123">L’avertissement</span><span class="sxs-lookup"><span data-stu-id="cd9f3-123">Unadvise</span></span>](imsgstore-unadvise.md) <br/> |<span data-ttu-id="cd9f3-124">Annule l’envoi de notifications précédemment configurées avec un appel à la méthode **IMsgStore::Advise** .</span><span class="sxs-lookup"><span data-stu-id="cd9f3-124">Cancels the sending of notifications previously set up with a call to the **IMsgStore::Advise** method.</span></span>  <br/> |
|[<span data-ttu-id="cd9f3-125">CompareEntryIDs</span><span class="sxs-lookup"><span data-stu-id="cd9f3-125">CompareEntryIDs</span></span>](imsgstore-compareentryids.md) <br/> |<span data-ttu-id="cd9f3-126">Compare deux identificateurs d’entrée pour déterminer si elles font référence à la même entrée dans une banque de messages.</span><span class="sxs-lookup"><span data-stu-id="cd9f3-126">Compares two entry identifiers to determine whether they refer to the same entry in a message store.</span></span>  <br/> |
|[<span data-ttu-id="cd9f3-127">OpenEntry</span><span class="sxs-lookup"><span data-stu-id="cd9f3-127">OpenEntry</span></span>](imsgstore-openentry.md) <br/> |<span data-ttu-id="cd9f3-128">Ouvre un dossier ou un message et retourne un pointeur d’interface pour l’accès des autres.</span><span class="sxs-lookup"><span data-stu-id="cd9f3-128">Opens a folder or message and returns an interface pointer for further access.</span></span>  <br/> |
|[<span data-ttu-id="cd9f3-129">SetReceiveFolder</span><span class="sxs-lookup"><span data-stu-id="cd9f3-129">SetReceiveFolder</span></span>](imsgstore-setreceivefolder.md) <br/> |<span data-ttu-id="cd9f3-130">Établissement d’un dossier comme destination pour les messages entrants d’une classe de message particulier.</span><span class="sxs-lookup"><span data-stu-id="cd9f3-130">Establishes a folder as the destination for incoming messages of a particular message class.</span></span>  <br/> |
|[<span data-ttu-id="cd9f3-131">GetReceiveFolder</span><span class="sxs-lookup"><span data-stu-id="cd9f3-131">GetReceiveFolder</span></span>](imsgstore-getreceivefolder.md) <br/> |<span data-ttu-id="cd9f3-132">Obtient le dossier qui a été établi comme dossier pour la banque de messages de réception de la destination pour les messages entrants d’une classe de message spécifié ou en tant que la valeur par défaut.</span><span class="sxs-lookup"><span data-stu-id="cd9f3-132">Obtains the folder that was established as the destination for incoming messages of a specified message class or as the default receive folder for the message store.</span></span>  <br/> |
|[<span data-ttu-id="cd9f3-133">GetReceiveFolderTable</span><span class="sxs-lookup"><span data-stu-id="cd9f3-133">GetReceiveFolderTable</span></span>](imsgstore-getreceivefoldertable.md) <br/> |<span data-ttu-id="cd9f3-134">Permet d’accéder à la table de dossier de réception, un tableau avec des informations sur tous les dossiers de réception de la banque de messages.</span><span class="sxs-lookup"><span data-stu-id="cd9f3-134">Provides access to the receive folder table, a table with information about all of the receive folders for the message store.</span></span>  <br/> |
|[<span data-ttu-id="cd9f3-135">StoreLogoff</span><span class="sxs-lookup"><span data-stu-id="cd9f3-135">StoreLogoff</span></span>](imsgstore-storelogoff.md) <br/> |<span data-ttu-id="cd9f3-136">Permet la déconnexion ordonnée de la banque de messages.</span><span class="sxs-lookup"><span data-stu-id="cd9f3-136">Enables the orderly logoff of the message store.</span></span>  <br/> |
|[<span data-ttu-id="cd9f3-137">AbortSubmit</span><span class="sxs-lookup"><span data-stu-id="cd9f3-137">AbortSubmit</span></span>](imsgstore-abortsubmit.md) <br/> |<span data-ttu-id="cd9f3-138">Tente de supprimer un message de la file d’attente sortante.</span><span class="sxs-lookup"><span data-stu-id="cd9f3-138">Attempts to remove a message from the outgoing queue.</span></span>  <br/> |
|[<span data-ttu-id="cd9f3-139">GetOutgoingQueue</span><span class="sxs-lookup"><span data-stu-id="cd9f3-139">GetOutgoingQueue</span></span>](imsgstore-getoutgoingqueue.md) <br/> |<span data-ttu-id="cd9f3-140">Permet d’accéder à la table sortant de la file d’attente, une table qui comporte des informations sur tous les messages en file d’attente sortante de la banque de messages.</span><span class="sxs-lookup"><span data-stu-id="cd9f3-140">Provides access to the outgoing queue table, a table that has information about all of the messages in the message store's outgoing queue.</span></span>  <br/> |
|[<span data-ttu-id="cd9f3-141">SetLockState</span><span class="sxs-lookup"><span data-stu-id="cd9f3-141">SetLockState</span></span>](imsgstore-setlockstate.md) <br/> |<span data-ttu-id="cd9f3-142">Verrouiller ou déverrouiller un message.</span><span class="sxs-lookup"><span data-stu-id="cd9f3-142">Locks or unlocks a message.</span></span>  <br/> |
|[<span data-ttu-id="cd9f3-143">FinishedMsg</span><span class="sxs-lookup"><span data-stu-id="cd9f3-143">FinishedMsg</span></span>](imsgstore-finishedmsg.md) <br/> |<span data-ttu-id="cd9f3-144">Active le fournisseur de banque de messages effectuer le traitement sur un message envoyé.</span><span class="sxs-lookup"><span data-stu-id="cd9f3-144">Enables the message store provider to perform processing on a sent message.</span></span>  <br/> |
|[<span data-ttu-id="cd9f3-145">NotifyNewMail</span><span class="sxs-lookup"><span data-stu-id="cd9f3-145">NotifyNewMail</span></span>](imsgstore-notifynewmail.md) <br/> |<span data-ttu-id="cd9f3-146">Informe la banque de messages un nouveau message est arriv�.</span><span class="sxs-lookup"><span data-stu-id="cd9f3-146">Informs the message store that a new message has arrived.</span></span>  <br/> |
   
|<span data-ttu-id="cd9f3-147">**Propriétés requises**</span><span class="sxs-lookup"><span data-stu-id="cd9f3-147">**Required properties**</span></span>|<span data-ttu-id="cd9f3-148">**Niveau d’accès**</span><span class="sxs-lookup"><span data-stu-id="cd9f3-148">**Access level**</span></span>|
|:-----|:-----|
|<span data-ttu-id="cd9f3-149">**PR_DISPLAY_NAME** ([PidTagDisplayName](pidtagdisplayname-canonical-property.md))</span><span class="sxs-lookup"><span data-stu-id="cd9f3-149">**PR_DISPLAY_NAME** ([PidTagDisplayName](pidtagdisplayname-canonical-property.md))</span></span>  <br/> |<span data-ttu-id="cd9f3-150">En lecture-écriture.</span><span class="sxs-lookup"><span data-stu-id="cd9f3-150">Read/write</span></span>  <br/> |
|<span data-ttu-id="cd9f3-151">**PR_ENTRYID** ([PidTagEntryId](pidtagentryid-canonical-property.md))</span><span class="sxs-lookup"><span data-stu-id="cd9f3-151">**PR_ENTRYID** ([PidTagEntryId](pidtagentryid-canonical-property.md))</span></span>  <br/> |<span data-ttu-id="cd9f3-152">Lecture seule</span><span class="sxs-lookup"><span data-stu-id="cd9f3-152">Read-only</span></span>  <br/> |
|<span data-ttu-id="cd9f3-153">**PR_OBJECT_TYPE** ([PidTagObjectType](pidtagobjecttype-canonical-property.md))</span><span class="sxs-lookup"><span data-stu-id="cd9f3-153">**PR_OBJECT_TYPE** ([PidTagObjectType](pidtagobjecttype-canonical-property.md))</span></span>  <br/> |<span data-ttu-id="cd9f3-154">Lecture seule</span><span class="sxs-lookup"><span data-stu-id="cd9f3-154">Read-only</span></span>  <br/> |
|<span data-ttu-id="cd9f3-155">**PR_RECORD_KEY** ([PidTagRecordKey](pidtagrecordkey-canonical-property.md))</span><span class="sxs-lookup"><span data-stu-id="cd9f3-155">**PR_RECORD_KEY** ([PidTagRecordKey](pidtagrecordkey-canonical-property.md))</span></span>  <br/> |<span data-ttu-id="cd9f3-156">Lecture seule</span><span class="sxs-lookup"><span data-stu-id="cd9f3-156">Read-only</span></span>  <br/> |
|<span data-ttu-id="cd9f3-157">**PR_STORE_ENTRYID** ([PidTagStoreEntryId](pidtagstoreentryid-canonical-property.md))</span><span class="sxs-lookup"><span data-stu-id="cd9f3-157">**PR_STORE_ENTRYID** ([PidTagStoreEntryId](pidtagstoreentryid-canonical-property.md))</span></span>  <br/> |<span data-ttu-id="cd9f3-158">Lecture seule</span><span class="sxs-lookup"><span data-stu-id="cd9f3-158">Read-only</span></span>  <br/> |
|<span data-ttu-id="cd9f3-159">**PR_STORE_RECORD_KEY** ([PidTagStoreRecordKey](pidtagstorerecordkey-canonical-property.md))</span><span class="sxs-lookup"><span data-stu-id="cd9f3-159">**PR_STORE_RECORD_KEY** ([PidTagStoreRecordKey](pidtagstorerecordkey-canonical-property.md))</span></span>  <br/> |<span data-ttu-id="cd9f3-160">Lecture seule</span><span class="sxs-lookup"><span data-stu-id="cd9f3-160">Read-only</span></span>  <br/> |
|<span data-ttu-id="cd9f3-161">**PR_MDB_PROVIDER** ([PidTagStoreProvider](pidtagstoreprovider-canonical-property.md))</span><span class="sxs-lookup"><span data-stu-id="cd9f3-161">**PR_MDB_PROVIDER** ([PidTagStoreProvider](pidtagstoreprovider-canonical-property.md))</span></span>  <br/> |<span data-ttu-id="cd9f3-162">Lecture seule</span><span class="sxs-lookup"><span data-stu-id="cd9f3-162">Read-only</span></span>  <br/> |
|<span data-ttu-id="cd9f3-163">**PR_STORE_SUPPORT_MASK** ([PidTagStoreSupportMask](pidtagstoresupportmask-canonical-property.md))</span><span class="sxs-lookup"><span data-stu-id="cd9f3-163">**PR_STORE_SUPPORT_MASK** ([PidTagStoreSupportMask](pidtagstoresupportmask-canonical-property.md))</span></span>  <br/> |<span data-ttu-id="cd9f3-164">Lecture seule</span><span class="sxs-lookup"><span data-stu-id="cd9f3-164">Read-only</span></span>  <br/> |
   
<span data-ttu-id="cd9f3-165">Les propriétés suivantes sont des magasins de message message interpersonnel (IPM) :</span><span class="sxs-lookup"><span data-stu-id="cd9f3-165">The following properties are for interpersonal message (IPM) message stores:</span></span>
  
- <span data-ttu-id="cd9f3-166">**PR_IPM_OUTBOX_ENTRYID** ([PidTagIpmOutboxEntryId](pidtagipmoutboxentryid-canonical-property.md))</span><span class="sxs-lookup"><span data-stu-id="cd9f3-166">**PR_IPM_OUTBOX_ENTRYID** ([PidTagIpmOutboxEntryId](pidtagipmoutboxentryid-canonical-property.md))</span></span>
    
- <span data-ttu-id="cd9f3-167">**PR_IPM_SENTMAIL_ENTRYID** ([PidTagIpmSentMailEntryId](pidtagipmsentmailentryid-canonical-property.md))</span><span class="sxs-lookup"><span data-stu-id="cd9f3-167">**PR_IPM_SENTMAIL_ENTRYID** ([PidTagIpmSentMailEntryId](pidtagipmsentmailentryid-canonical-property.md))</span></span>
    
- <span data-ttu-id="cd9f3-168">**PR_IPM_SUBTREE_ENTRYID** ([PidTagIpmSubtreeEntryId](pidtagipmsubtreeentryid-canonical-property.md))</span><span class="sxs-lookup"><span data-stu-id="cd9f3-168">**PR_IPM_SUBTREE_ENTRYID** ([PidTagIpmSubtreeEntryId](pidtagipmsubtreeentryid-canonical-property.md))</span></span>
    
- <span data-ttu-id="cd9f3-169">**PR_IPM_WASTEBASKET_ENTRYID** ([PidTagIpmWastebasketEntryId](pidtagipmwastebasketentryid-canonical-property.md))</span><span class="sxs-lookup"><span data-stu-id="cd9f3-169">**PR_IPM_WASTEBASKET_ENTRYID** ([PidTagIpmWastebasketEntryId](pidtagipmwastebasketentryid-canonical-property.md))</span></span>
    
- <span data-ttu-id="cd9f3-170">**PR_MDB_PROVIDER**</span><span class="sxs-lookup"><span data-stu-id="cd9f3-170">**PR_MDB_PROVIDER**</span></span>
    
- <span data-ttu-id="cd9f3-171">**PR_STORE_SUPPORT_MASK**</span><span class="sxs-lookup"><span data-stu-id="cd9f3-171">**PR_STORE_SUPPORT_MASK**</span></span>
    
## <a name="see-also"></a><span data-ttu-id="cd9f3-172">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="cd9f3-172">See also</span></span>



[<span data-ttu-id="cd9f3-173">Propriétés MAPI</span><span class="sxs-lookup"><span data-stu-id="cd9f3-173">MAPI Properties</span></span>](mapi-properties.md)

