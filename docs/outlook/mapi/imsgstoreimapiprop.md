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
description: Dernière modification le 9 mars 2015
ms.openlocfilehash: 4ed17fd7f826432da9460fe01e5aa76802726bad
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/23/2018
ms.locfileid: "22584631"
---
# <a name="imsgstore--imapiprop"></a><span data-ttu-id="7a8de-103">IMsgStore : IMAPIProp</span><span class="sxs-lookup"><span data-stu-id="7a8de-103">IMsgStore : IMAPIProp</span></span>

  
  
<span data-ttu-id="7a8de-104">**S’applique à** : Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="7a8de-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="7a8de-105">Permet d’accéder aux informations de banque de messages et aux messages et des dossiers.</span><span class="sxs-lookup"><span data-stu-id="7a8de-105">Provides access to message store information and to messages and folders.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="7a8de-106">Fichier d’en-tête :</span><span class="sxs-lookup"><span data-stu-id="7a8de-106">Header file:</span></span>  <br/> |<span data-ttu-id="7a8de-107">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="7a8de-107">Mapidefs.h</span></span>  <br/> |
|<span data-ttu-id="7a8de-108">Exposés par :</span><span class="sxs-lookup"><span data-stu-id="7a8de-108">Exposed by:</span></span>  <br/> |<span data-ttu-id="7a8de-109">Objet store de message</span><span class="sxs-lookup"><span data-stu-id="7a8de-109">Message store object</span></span>  <br/> |
|<span data-ttu-id="7a8de-110">Implémenté par :</span><span class="sxs-lookup"><span data-stu-id="7a8de-110">Implemented by:</span></span>  <br/> |<span data-ttu-id="7a8de-111">Fournisseurs de banque de messages</span><span class="sxs-lookup"><span data-stu-id="7a8de-111">Message store providers</span></span>  <br/> |
|<span data-ttu-id="7a8de-112">Appelé par :</span><span class="sxs-lookup"><span data-stu-id="7a8de-112">Called by:</span></span>  <br/> |<span data-ttu-id="7a8de-113">Applications clientes, le spouleur MAPI et MAPI</span><span class="sxs-lookup"><span data-stu-id="7a8de-113">Client applications, the MAPI spooler, and MAPI</span></span>  <br/> |
|<span data-ttu-id="7a8de-114">Identificateur de l’interface :</span><span class="sxs-lookup"><span data-stu-id="7a8de-114">Interface identifier:</span></span>  <br/> |<span data-ttu-id="7a8de-115">IID_IMsgStore</span><span class="sxs-lookup"><span data-stu-id="7a8de-115">IID_IMsgStore</span></span>  <br/> |
|<span data-ttu-id="7a8de-116">Type de pointeur :</span><span class="sxs-lookup"><span data-stu-id="7a8de-116">Pointer type:</span></span>  <br/> |<span data-ttu-id="7a8de-117">IPMDB</span><span class="sxs-lookup"><span data-stu-id="7a8de-117">LPMDB</span></span>  <br/> |
|<span data-ttu-id="7a8de-118">Modèle de transaction :</span><span class="sxs-lookup"><span data-stu-id="7a8de-118">Transaction model:</span></span>  <br/> |<span data-ttu-id="7a8de-119">Nontransacted</span><span class="sxs-lookup"><span data-stu-id="7a8de-119">Nontransacted</span></span>  <br/> |
   
## <a name="vtable-order"></a><span data-ttu-id="7a8de-120">Ordre vtable</span><span class="sxs-lookup"><span data-stu-id="7a8de-120">Vtable order</span></span>

|||
|:-----|:-----|
|[<span data-ttu-id="7a8de-121">Conseiller</span><span class="sxs-lookup"><span data-stu-id="7a8de-121">Advise</span></span>](imsgstore-advise.md) <br/> |<span data-ttu-id="7a8de-122">Inscrit pour recevoir des notifications d’événements spécifiques qui affectent la banque de messages.</span><span class="sxs-lookup"><span data-stu-id="7a8de-122">Registers to receive notification of specified events that affect the message store.</span></span>  <br/> |
|[<span data-ttu-id="7a8de-123">L’avertissement</span><span class="sxs-lookup"><span data-stu-id="7a8de-123">Unadvise</span></span>](imsgstore-unadvise.md) <br/> |<span data-ttu-id="7a8de-124">Annule l’envoi de notifications précédemment configurées avec un appel à la méthode **IMsgStore::Advise** .</span><span class="sxs-lookup"><span data-stu-id="7a8de-124">Cancels the sending of notifications previously set up with a call to the **IMsgStore::Advise** method.</span></span>  <br/> |
|[<span data-ttu-id="7a8de-125">CompareEntryIDs</span><span class="sxs-lookup"><span data-stu-id="7a8de-125">CompareEntryIDs</span></span>](imsgstore-compareentryids.md) <br/> |<span data-ttu-id="7a8de-126">Compare deux identificateurs d’entrée pour déterminer si elles font référence à la même entrée dans une banque de messages.</span><span class="sxs-lookup"><span data-stu-id="7a8de-126">Compares two entry identifiers to determine whether they refer to the same entry in a message store.</span></span>  <br/> |
|[<span data-ttu-id="7a8de-127">OpenEntry</span><span class="sxs-lookup"><span data-stu-id="7a8de-127">OpenEntry</span></span>](imsgstore-openentry.md) <br/> |<span data-ttu-id="7a8de-128">Ouvre un dossier ou un message et retourne un pointeur d’interface pour l’accès des autres.</span><span class="sxs-lookup"><span data-stu-id="7a8de-128">Opens a folder or message and returns an interface pointer for further access.</span></span>  <br/> |
|[<span data-ttu-id="7a8de-129">SetReceiveFolder</span><span class="sxs-lookup"><span data-stu-id="7a8de-129">SetReceiveFolder</span></span>](imsgstore-setreceivefolder.md) <br/> |<span data-ttu-id="7a8de-130">Établissement d’un dossier comme destination pour les messages entrants d’une classe de message particulier.</span><span class="sxs-lookup"><span data-stu-id="7a8de-130">Establishes a folder as the destination for incoming messages of a particular message class.</span></span>  <br/> |
|[<span data-ttu-id="7a8de-131">GetReceiveFolder</span><span class="sxs-lookup"><span data-stu-id="7a8de-131">GetReceiveFolder</span></span>](imsgstore-getreceivefolder.md) <br/> |<span data-ttu-id="7a8de-132">Obtient le dossier qui a été établi comme dossier pour la banque de messages de réception de la destination pour les messages entrants d’une classe de message spécifié ou en tant que la valeur par défaut.</span><span class="sxs-lookup"><span data-stu-id="7a8de-132">Obtains the folder that was established as the destination for incoming messages of a specified message class or as the default receive folder for the message store.</span></span>  <br/> |
|[<span data-ttu-id="7a8de-133">GetReceiveFolderTable</span><span class="sxs-lookup"><span data-stu-id="7a8de-133">GetReceiveFolderTable</span></span>](imsgstore-getreceivefoldertable.md) <br/> |<span data-ttu-id="7a8de-134">Permet d’accéder à la table de dossier de réception, un tableau avec des informations sur tous les dossiers de réception de la banque de messages.</span><span class="sxs-lookup"><span data-stu-id="7a8de-134">Provides access to the receive folder table, a table with information about all of the receive folders for the message store.</span></span>  <br/> |
|[<span data-ttu-id="7a8de-135">StoreLogoff</span><span class="sxs-lookup"><span data-stu-id="7a8de-135">StoreLogoff</span></span>](imsgstore-storelogoff.md) <br/> |<span data-ttu-id="7a8de-136">Permet la déconnexion ordonnée de la banque de messages.</span><span class="sxs-lookup"><span data-stu-id="7a8de-136">Enables the orderly logoff of the message store.</span></span>  <br/> |
|[<span data-ttu-id="7a8de-137">AbortSubmit</span><span class="sxs-lookup"><span data-stu-id="7a8de-137">AbortSubmit</span></span>](imsgstore-abortsubmit.md) <br/> |<span data-ttu-id="7a8de-138">Tente de supprimer un message de la file d’attente sortante.</span><span class="sxs-lookup"><span data-stu-id="7a8de-138">Attempts to remove a message from the outgoing queue.</span></span>  <br/> |
|[<span data-ttu-id="7a8de-139">GetOutgoingQueue</span><span class="sxs-lookup"><span data-stu-id="7a8de-139">GetOutgoingQueue</span></span>](imsgstore-getoutgoingqueue.md) <br/> |<span data-ttu-id="7a8de-140">Permet d’accéder à la table sortant de la file d’attente, une table qui comporte des informations sur tous les messages en file d’attente sortante de la banque de messages.</span><span class="sxs-lookup"><span data-stu-id="7a8de-140">Provides access to the outgoing queue table, a table that has information about all of the messages in the message store's outgoing queue.</span></span>  <br/> |
|[<span data-ttu-id="7a8de-141">SetLockState</span><span class="sxs-lookup"><span data-stu-id="7a8de-141">SetLockState</span></span>](imsgstore-setlockstate.md) <br/> |<span data-ttu-id="7a8de-142">Verrouiller ou déverrouiller un message.</span><span class="sxs-lookup"><span data-stu-id="7a8de-142">Locks or unlocks a message.</span></span>  <br/> |
|[<span data-ttu-id="7a8de-143">FinishedMsg</span><span class="sxs-lookup"><span data-stu-id="7a8de-143">FinishedMsg</span></span>](imsgstore-finishedmsg.md) <br/> |<span data-ttu-id="7a8de-144">Active le fournisseur de banque de messages effectuer le traitement sur un message envoyé.</span><span class="sxs-lookup"><span data-stu-id="7a8de-144">Enables the message store provider to perform processing on a sent message.</span></span>  <br/> |
|[<span data-ttu-id="7a8de-145">NotifyNewMail</span><span class="sxs-lookup"><span data-stu-id="7a8de-145">NotifyNewMail</span></span>](imsgstore-notifynewmail.md) <br/> |<span data-ttu-id="7a8de-146">Informe la banque de messages un nouveau message est arriv�.</span><span class="sxs-lookup"><span data-stu-id="7a8de-146">Informs the message store that a new message has arrived.</span></span>  <br/> |
   
|<span data-ttu-id="7a8de-147">**Propriétés requises**</span><span class="sxs-lookup"><span data-stu-id="7a8de-147">**Required properties**</span></span>|<span data-ttu-id="7a8de-148">**Niveau d’accès**</span><span class="sxs-lookup"><span data-stu-id="7a8de-148">**Access level**</span></span>|
|:-----|:-----|
|<span data-ttu-id="7a8de-149">**PR_DISPLAY_NAME** ([PidTagDisplayName](pidtagdisplayname-canonical-property.md))</span><span class="sxs-lookup"><span data-stu-id="7a8de-149">**PR_DISPLAY_NAME** ([PidTagDisplayName](pidtagdisplayname-canonical-property.md))</span></span>  <br/> |<span data-ttu-id="7a8de-150">En lecture-écriture.</span><span class="sxs-lookup"><span data-stu-id="7a8de-150">Read/write</span></span>  <br/> |
|<span data-ttu-id="7a8de-151">**PR_ENTRYID** ([PidTagEntryId](pidtagentryid-canonical-property.md))</span><span class="sxs-lookup"><span data-stu-id="7a8de-151">**PR_ENTRYID** ([PidTagEntryId](pidtagentryid-canonical-property.md))</span></span>  <br/> |<span data-ttu-id="7a8de-152">Lecture seule</span><span class="sxs-lookup"><span data-stu-id="7a8de-152">Read-only</span></span>  <br/> |
|<span data-ttu-id="7a8de-153">**PR_OBJECT_TYPE** ([PidTagObjectType](pidtagobjecttype-canonical-property.md))</span><span class="sxs-lookup"><span data-stu-id="7a8de-153">**PR_OBJECT_TYPE** ([PidTagObjectType](pidtagobjecttype-canonical-property.md))</span></span>  <br/> |<span data-ttu-id="7a8de-154">Lecture seule</span><span class="sxs-lookup"><span data-stu-id="7a8de-154">Read-only</span></span>  <br/> |
|<span data-ttu-id="7a8de-155">**PR_RECORD_KEY** ([PidTagRecordKey](pidtagrecordkey-canonical-property.md))</span><span class="sxs-lookup"><span data-stu-id="7a8de-155">**PR_RECORD_KEY** ([PidTagRecordKey](pidtagrecordkey-canonical-property.md))</span></span>  <br/> |<span data-ttu-id="7a8de-156">Lecture seule</span><span class="sxs-lookup"><span data-stu-id="7a8de-156">Read-only</span></span>  <br/> |
|<span data-ttu-id="7a8de-157">**PR_STORE_ENTRYID** ([PidTagStoreEntryId](pidtagstoreentryid-canonical-property.md))</span><span class="sxs-lookup"><span data-stu-id="7a8de-157">**PR_STORE_ENTRYID** ([PidTagStoreEntryId](pidtagstoreentryid-canonical-property.md))</span></span>  <br/> |<span data-ttu-id="7a8de-158">Lecture seule</span><span class="sxs-lookup"><span data-stu-id="7a8de-158">Read-only</span></span>  <br/> |
|<span data-ttu-id="7a8de-159">**PR_STORE_RECORD_KEY** ([PidTagStoreRecordKey](pidtagstorerecordkey-canonical-property.md))</span><span class="sxs-lookup"><span data-stu-id="7a8de-159">**PR_STORE_RECORD_KEY** ([PidTagStoreRecordKey](pidtagstorerecordkey-canonical-property.md))</span></span>  <br/> |<span data-ttu-id="7a8de-160">Lecture seule</span><span class="sxs-lookup"><span data-stu-id="7a8de-160">Read-only</span></span>  <br/> |
|<span data-ttu-id="7a8de-161">**PR_MDB_PROVIDER** ([PidTagStoreProvider](pidtagstoreprovider-canonical-property.md))</span><span class="sxs-lookup"><span data-stu-id="7a8de-161">**PR_MDB_PROVIDER** ([PidTagStoreProvider](pidtagstoreprovider-canonical-property.md))</span></span>  <br/> |<span data-ttu-id="7a8de-162">Lecture seule</span><span class="sxs-lookup"><span data-stu-id="7a8de-162">Read-only</span></span>  <br/> |
|<span data-ttu-id="7a8de-163">**PR_STORE_SUPPORT_MASK** ([PidTagStoreSupportMask](pidtagstoresupportmask-canonical-property.md))</span><span class="sxs-lookup"><span data-stu-id="7a8de-163">**PR_STORE_SUPPORT_MASK** ([PidTagStoreSupportMask](pidtagstoresupportmask-canonical-property.md))</span></span>  <br/> |<span data-ttu-id="7a8de-164">Lecture seule</span><span class="sxs-lookup"><span data-stu-id="7a8de-164">Read-only</span></span>  <br/> |
   
<span data-ttu-id="7a8de-165">Les propriétés suivantes sont des magasins de message message interpersonnel (IPM) :</span><span class="sxs-lookup"><span data-stu-id="7a8de-165">The following properties are for interpersonal message (IPM) message stores:</span></span>
  
- <span data-ttu-id="7a8de-166">**PR_IPM_OUTBOX_ENTRYID** ([PidTagIpmOutboxEntryId](pidtagipmoutboxentryid-canonical-property.md))</span><span class="sxs-lookup"><span data-stu-id="7a8de-166">**PR_IPM_OUTBOX_ENTRYID** ([PidTagIpmOutboxEntryId](pidtagipmoutboxentryid-canonical-property.md))</span></span>
    
- <span data-ttu-id="7a8de-167">**PR_IPM_SENTMAIL_ENTRYID** ([PidTagIpmSentMailEntryId](pidtagipmsentmailentryid-canonical-property.md))</span><span class="sxs-lookup"><span data-stu-id="7a8de-167">**PR_IPM_SENTMAIL_ENTRYID** ([PidTagIpmSentMailEntryId](pidtagipmsentmailentryid-canonical-property.md))</span></span>
    
- <span data-ttu-id="7a8de-168">**PR_IPM_SUBTREE_ENTRYID** ([PidTagIpmSubtreeEntryId](pidtagipmsubtreeentryid-canonical-property.md))</span><span class="sxs-lookup"><span data-stu-id="7a8de-168">**PR_IPM_SUBTREE_ENTRYID** ([PidTagIpmSubtreeEntryId](pidtagipmsubtreeentryid-canonical-property.md))</span></span>
    
- <span data-ttu-id="7a8de-169">**PR_IPM_WASTEBASKET_ENTRYID** ([PidTagIpmWastebasketEntryId](pidtagipmwastebasketentryid-canonical-property.md))</span><span class="sxs-lookup"><span data-stu-id="7a8de-169">**PR_IPM_WASTEBASKET_ENTRYID** ([PidTagIpmWastebasketEntryId](pidtagipmwastebasketentryid-canonical-property.md))</span></span>
    
- <span data-ttu-id="7a8de-170">**PR_MDB_PROVIDER**</span><span class="sxs-lookup"><span data-stu-id="7a8de-170">**PR_MDB_PROVIDER**</span></span>
    
- <span data-ttu-id="7a8de-171">**PR_STORE_SUPPORT_MASK**</span><span class="sxs-lookup"><span data-stu-id="7a8de-171">**PR_STORE_SUPPORT_MASK**</span></span>
    
## <a name="see-also"></a><span data-ttu-id="7a8de-172">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="7a8de-172">See also</span></span>



[<span data-ttu-id="7a8de-173">Propriétés MAPI</span><span class="sxs-lookup"><span data-stu-id="7a8de-173">MAPI Properties</span></span>](mapi-properties.md)

