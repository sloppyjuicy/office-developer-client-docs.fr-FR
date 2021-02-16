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
ms.openlocfilehash: af4bf73b58f7723066bb8fad7c087ba0238ceec2
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/28/2019
ms.locfileid: "33422326"
---
# <a name="imsgstore--imapiprop"></a><span data-ttu-id="f2939-103">IMsgStore : IMAPIProp</span><span class="sxs-lookup"><span data-stu-id="f2939-103">IMsgStore : IMAPIProp</span></span>

  
  
<span data-ttu-id="f2939-104">**S’applique à** : Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="f2939-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="f2939-105">Permet d’accéder aux informations de la boutique de messages et aux messages et dossiers.</span><span class="sxs-lookup"><span data-stu-id="f2939-105">Provides access to message store information and to messages and folders.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="f2939-106">Fichier d’en-tête :</span><span class="sxs-lookup"><span data-stu-id="f2939-106">Header file:</span></span>  <br/> |<span data-ttu-id="f2939-107">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="f2939-107">Mapidefs.h</span></span>  <br/> |
|<span data-ttu-id="f2939-108">Exposé par :</span><span class="sxs-lookup"><span data-stu-id="f2939-108">Exposed by:</span></span>  <br/> |<span data-ttu-id="f2939-109">Objet de magasin de messages</span><span class="sxs-lookup"><span data-stu-id="f2939-109">Message store object</span></span>  <br/> |
|<span data-ttu-id="f2939-110">Implémenté par :</span><span class="sxs-lookup"><span data-stu-id="f2939-110">Implemented by:</span></span>  <br/> |<span data-ttu-id="f2939-111">Fournisseurs de magasins de messages</span><span class="sxs-lookup"><span data-stu-id="f2939-111">Message store providers</span></span>  <br/> |
|<span data-ttu-id="f2939-112">Appelé par :</span><span class="sxs-lookup"><span data-stu-id="f2939-112">Called by:</span></span>  <br/> |<span data-ttu-id="f2939-113">Applications clientes, lepooler MAPI et MAPI</span><span class="sxs-lookup"><span data-stu-id="f2939-113">Client applications, the MAPI spooler, and MAPI</span></span>  <br/> |
|<span data-ttu-id="f2939-114">Identificateur d’interface :</span><span class="sxs-lookup"><span data-stu-id="f2939-114">Interface identifier:</span></span>  <br/> |<span data-ttu-id="f2939-115">IID_IMsgStore</span><span class="sxs-lookup"><span data-stu-id="f2939-115">IID_IMsgStore</span></span>  <br/> |
|<span data-ttu-id="f2939-116">Type de pointeur :</span><span class="sxs-lookup"><span data-stu-id="f2939-116">Pointer type:</span></span>  <br/> |<span data-ttu-id="f2939-117">LPMDB</span><span class="sxs-lookup"><span data-stu-id="f2939-117">LPMDB</span></span>  <br/> |
|<span data-ttu-id="f2939-118">Modèle de transaction :</span><span class="sxs-lookup"><span data-stu-id="f2939-118">Transaction model:</span></span>  <br/> |<span data-ttu-id="f2939-119">Non traduit</span><span class="sxs-lookup"><span data-stu-id="f2939-119">Nontransacted</span></span>  <br/> |
   
## <a name="vtable-order"></a><span data-ttu-id="f2939-120">Ordre des vtables</span><span class="sxs-lookup"><span data-stu-id="f2939-120">Vtable order</span></span>

|||
|:-----|:-----|
|[<span data-ttu-id="f2939-121">Conseiller</span><span class="sxs-lookup"><span data-stu-id="f2939-121">Advise</span></span>](imsgstore-advise.md) <br/> |<span data-ttu-id="f2939-122">S’inscrit pour recevoir une notification des événements spécifiés qui affectent la boutique de messages.</span><span class="sxs-lookup"><span data-stu-id="f2939-122">Registers to receive notification of specified events that affect the message store.</span></span>  <br/> |
|[<span data-ttu-id="f2939-123">Unadvise</span><span class="sxs-lookup"><span data-stu-id="f2939-123">Unadvise</span></span>](imsgstore-unadvise.md) <br/> |<span data-ttu-id="f2939-124">Annule l’envoi de notifications précédemment définies avec un appel à la **méthode IMsgStore::Advise.**</span><span class="sxs-lookup"><span data-stu-id="f2939-124">Cancels the sending of notifications previously set up with a call to the **IMsgStore::Advise** method.</span></span>  <br/> |
|[<span data-ttu-id="f2939-125">CompareEntryIDs</span><span class="sxs-lookup"><span data-stu-id="f2939-125">CompareEntryIDs</span></span>](imsgstore-compareentryids.md) <br/> |<span data-ttu-id="f2939-126">Compare deux identificateurs d’entrée pour déterminer s’ils font référence à la même entrée dans une magasin de messages.</span><span class="sxs-lookup"><span data-stu-id="f2939-126">Compares two entry identifiers to determine whether they refer to the same entry in a message store.</span></span>  <br/> |
|[<span data-ttu-id="f2939-127">OpenEntry</span><span class="sxs-lookup"><span data-stu-id="f2939-127">OpenEntry</span></span>](imsgstore-openentry.md) <br/> |<span data-ttu-id="f2939-128">Ouvre un dossier ou un message et renvoie un pointeur d’interface pour un accès supplémentaire.</span><span class="sxs-lookup"><span data-stu-id="f2939-128">Opens a folder or message and returns an interface pointer for further access.</span></span>  <br/> |
|[<span data-ttu-id="f2939-129">SetReceiveFolder</span><span class="sxs-lookup"><span data-stu-id="f2939-129">SetReceiveFolder</span></span>](imsgstore-setreceivefolder.md) <br/> |<span data-ttu-id="f2939-130">Établit un dossier comme destination pour les messages entrants d’une classe de message particulière.</span><span class="sxs-lookup"><span data-stu-id="f2939-130">Establishes a folder as the destination for incoming messages of a particular message class.</span></span>  <br/> |
|[<span data-ttu-id="f2939-131">GetReceiveFolder</span><span class="sxs-lookup"><span data-stu-id="f2939-131">GetReceiveFolder</span></span>](imsgstore-getreceivefolder.md) <br/> |<span data-ttu-id="f2939-132">Obtient le dossier qui a été établi comme destination pour les messages entrants d’une classe de message spécifiée ou comme dossier de réception par défaut pour la magasin de messages.</span><span class="sxs-lookup"><span data-stu-id="f2939-132">Obtains the folder that was established as the destination for incoming messages of a specified message class or as the default receive folder for the message store.</span></span>  <br/> |
|[<span data-ttu-id="f2939-133">GetReceiveFolderTable</span><span class="sxs-lookup"><span data-stu-id="f2939-133">GetReceiveFolderTable</span></span>](imsgstore-getreceivefoldertable.md) <br/> |<span data-ttu-id="f2939-134">Permet d’accéder à la table des dossiers de réception, une table contenant des informations sur tous les dossiers de réception de la boutique de messages.</span><span class="sxs-lookup"><span data-stu-id="f2939-134">Provides access to the receive folder table, a table with information about all of the receive folders for the message store.</span></span>  <br/> |
|[<span data-ttu-id="f2939-135">StoreLogoff</span><span class="sxs-lookup"><span data-stu-id="f2939-135">StoreLogoff</span></span>](imsgstore-storelogoff.md) <br/> |<span data-ttu-id="f2939-136">Active la ff de logo dans l’ordre de la boutique de messages.</span><span class="sxs-lookup"><span data-stu-id="f2939-136">Enables the orderly logoff of the message store.</span></span>  <br/> |
|[<span data-ttu-id="f2939-137">AbortSubmit</span><span class="sxs-lookup"><span data-stu-id="f2939-137">AbortSubmit</span></span>](imsgstore-abortsubmit.md) <br/> |<span data-ttu-id="f2939-138">Tente de supprimer un message de la file d’attente sortante.</span><span class="sxs-lookup"><span data-stu-id="f2939-138">Attempts to remove a message from the outgoing queue.</span></span>  <br/> |
|[<span data-ttu-id="f2939-139">GetOutgoingQueue</span><span class="sxs-lookup"><span data-stu-id="f2939-139">GetOutgoingQueue</span></span>](imsgstore-getoutgoingqueue.md) <br/> |<span data-ttu-id="f2939-140">Permet d’accéder à la table de files d’attente sortante, une table qui contient des informations sur tous les messages de la file d’attente sortante de la boutique de messages.</span><span class="sxs-lookup"><span data-stu-id="f2939-140">Provides access to the outgoing queue table, a table that has information about all of the messages in the message store's outgoing queue.</span></span>  <br/> |
|[<span data-ttu-id="f2939-141">SetLockState</span><span class="sxs-lookup"><span data-stu-id="f2939-141">SetLockState</span></span>](imsgstore-setlockstate.md) <br/> |<span data-ttu-id="f2939-142">Verrouille ou déverrouille un message.</span><span class="sxs-lookup"><span data-stu-id="f2939-142">Locks or unlocks a message.</span></span>  <br/> |
|[<span data-ttu-id="f2939-143">FinishedMsg</span><span class="sxs-lookup"><span data-stu-id="f2939-143">FinishedMsg</span></span>](imsgstore-finishedmsg.md) <br/> |<span data-ttu-id="f2939-144">Permet au fournisseur de magasin de messages d’effectuer un traitement sur un message envoyé.</span><span class="sxs-lookup"><span data-stu-id="f2939-144">Enables the message store provider to perform processing on a sent message.</span></span>  <br/> |
|[<span data-ttu-id="f2939-145">NotifyNewMail</span><span class="sxs-lookup"><span data-stu-id="f2939-145">NotifyNewMail</span></span>](imsgstore-notifynewmail.md) <br/> |<span data-ttu-id="f2939-146">Informe la banque de messages un nouveau message est arriv�.</span><span class="sxs-lookup"><span data-stu-id="f2939-146">Informs the message store that a new message has arrived.</span></span>  <br/> |
   
|<span data-ttu-id="f2939-147">**Propriétés requises**</span><span class="sxs-lookup"><span data-stu-id="f2939-147">**Required properties**</span></span>|<span data-ttu-id="f2939-148">**Niveau d’accès**</span><span class="sxs-lookup"><span data-stu-id="f2939-148">**Access level**</span></span>|
|:-----|:-----|
|<span data-ttu-id="f2939-149">**PR_DISPLAY_NAME** ([PidTagDisplayName](pidtagdisplayname-canonical-property.md))</span><span class="sxs-lookup"><span data-stu-id="f2939-149">**PR_DISPLAY_NAME** ([PidTagDisplayName](pidtagdisplayname-canonical-property.md))</span></span>  <br/> |<span data-ttu-id="f2939-150">Lecture/écriture</span><span class="sxs-lookup"><span data-stu-id="f2939-150">Read/write</span></span>  <br/> |
|<span data-ttu-id="f2939-151">**PR_ENTRYID** ([PidTagEntryId](pidtagentryid-canonical-property.md))</span><span class="sxs-lookup"><span data-stu-id="f2939-151">**PR_ENTRYID** ([PidTagEntryId](pidtagentryid-canonical-property.md))</span></span>  <br/> |<span data-ttu-id="f2939-152">Lecture seule</span><span class="sxs-lookup"><span data-stu-id="f2939-152">Read-only</span></span>  <br/> |
|<span data-ttu-id="f2939-153">**PR_OBJECT_TYPE** ([PidTagObjectType](pidtagobjecttype-canonical-property.md))</span><span class="sxs-lookup"><span data-stu-id="f2939-153">**PR_OBJECT_TYPE** ([PidTagObjectType](pidtagobjecttype-canonical-property.md))</span></span>  <br/> |<span data-ttu-id="f2939-154">Lecture seule</span><span class="sxs-lookup"><span data-stu-id="f2939-154">Read-only</span></span>  <br/> |
|<span data-ttu-id="f2939-155">**PR_RECORD_KEY** ([PidTagRecordKey](pidtagrecordkey-canonical-property.md))</span><span class="sxs-lookup"><span data-stu-id="f2939-155">**PR_RECORD_KEY** ([PidTagRecordKey](pidtagrecordkey-canonical-property.md))</span></span>  <br/> |<span data-ttu-id="f2939-156">Lecture seule</span><span class="sxs-lookup"><span data-stu-id="f2939-156">Read-only</span></span>  <br/> |
|<span data-ttu-id="f2939-157">**PR_STORE_ENTRYID** ([PidTagStoreEntryId](pidtagstoreentryid-canonical-property.md))</span><span class="sxs-lookup"><span data-stu-id="f2939-157">**PR_STORE_ENTRYID** ([PidTagStoreEntryId](pidtagstoreentryid-canonical-property.md))</span></span>  <br/> |<span data-ttu-id="f2939-158">Lecture seule</span><span class="sxs-lookup"><span data-stu-id="f2939-158">Read-only</span></span>  <br/> |
|<span data-ttu-id="f2939-159">**PR_STORE_RECORD_KEY** ([PidTagStoreRecordKey](pidtagstorerecordkey-canonical-property.md))</span><span class="sxs-lookup"><span data-stu-id="f2939-159">**PR_STORE_RECORD_KEY** ([PidTagStoreRecordKey](pidtagstorerecordkey-canonical-property.md))</span></span>  <br/> |<span data-ttu-id="f2939-160">Lecture seule</span><span class="sxs-lookup"><span data-stu-id="f2939-160">Read-only</span></span>  <br/> |
|<span data-ttu-id="f2939-161">**PR_MDB_PROVIDER** ([PidTagStoreProvider](pidtagstoreprovider-canonical-property.md))</span><span class="sxs-lookup"><span data-stu-id="f2939-161">**PR_MDB_PROVIDER** ([PidTagStoreProvider](pidtagstoreprovider-canonical-property.md))</span></span>  <br/> |<span data-ttu-id="f2939-162">Lecture seule</span><span class="sxs-lookup"><span data-stu-id="f2939-162">Read-only</span></span>  <br/> |
|<span data-ttu-id="f2939-163">**PR_STORE_SUPPORT_MASK** ([PidTagStoreSupportMask](pidtagstoresupportmask-canonical-property.md))</span><span class="sxs-lookup"><span data-stu-id="f2939-163">**PR_STORE_SUPPORT_MASK** ([PidTagStoreSupportMask](pidtagstoresupportmask-canonical-property.md))</span></span>  <br/> |<span data-ttu-id="f2939-164">Lecture seule</span><span class="sxs-lookup"><span data-stu-id="f2939-164">Read-only</span></span>  <br/> |
   
<span data-ttu-id="f2939-165">Les propriétés suivantes sont pour les magasins de messages interpersonnels (IPM) :</span><span class="sxs-lookup"><span data-stu-id="f2939-165">The following properties are for interpersonal message (IPM) message stores:</span></span>
  
- <span data-ttu-id="f2939-166">**PR_IPM_OUTBOX_ENTRYID** ([PidTagIpmOutboxEntryId](pidtagipmoutboxentryid-canonical-property.md))</span><span class="sxs-lookup"><span data-stu-id="f2939-166">**PR_IPM_OUTBOX_ENTRYID** ([PidTagIpmOutboxEntryId](pidtagipmoutboxentryid-canonical-property.md))</span></span>
    
- <span data-ttu-id="f2939-167">**PR_IPM_SENTMAIL_ENTRYID** ([PidTagIpmSentMailEntryId](pidtagipmsentmailentryid-canonical-property.md))</span><span class="sxs-lookup"><span data-stu-id="f2939-167">**PR_IPM_SENTMAIL_ENTRYID** ([PidTagIpmSentMailEntryId](pidtagipmsentmailentryid-canonical-property.md))</span></span>
    
- <span data-ttu-id="f2939-168">**PR_IPM_SUBTREE_ENTRYID** ([PidTagIpmSubtreeEntryId](pidtagipmsubtreeentryid-canonical-property.md))</span><span class="sxs-lookup"><span data-stu-id="f2939-168">**PR_IPM_SUBTREE_ENTRYID** ([PidTagIpmSubtreeEntryId](pidtagipmsubtreeentryid-canonical-property.md))</span></span>
    
- <span data-ttu-id="f2939-169">**PR_IPM_WASTEBASKET_ENTRYID** ([PidTagIpmWastebasketEntryId](pidtagipmwastebasketentryid-canonical-property.md))</span><span class="sxs-lookup"><span data-stu-id="f2939-169">**PR_IPM_WASTEBASKET_ENTRYID** ([PidTagIpmWastebasketEntryId](pidtagipmwastebasketentryid-canonical-property.md))</span></span>
    
- <span data-ttu-id="f2939-170">**PR_MDB_PROVIDER**</span><span class="sxs-lookup"><span data-stu-id="f2939-170">**PR_MDB_PROVIDER**</span></span>
    
- <span data-ttu-id="f2939-171">**PR_STORE_SUPPORT_MASK**</span><span class="sxs-lookup"><span data-stu-id="f2939-171">**PR_STORE_SUPPORT_MASK**</span></span>
    
## <a name="see-also"></a><span data-ttu-id="f2939-172">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="f2939-172">See also</span></span>



[<span data-ttu-id="f2939-173">Propriétés MAPI</span><span class="sxs-lookup"><span data-stu-id="f2939-173">MAPI Properties</span></span>](mapi-properties.md)

