---
title: Tables de files d’attente sortantes
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: 070377ca-ba9e-42ef-ac6b-ff7548b5ccf5
description: Dernière modification le 09 mars 2015
ms.openlocfilehash: c5f136a0d26b7519bc1b7b3d8f448f5f382767ad
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/23/2018
ms.locfileid: "22591253"
---
# <a name="outgoing-queue-tables"></a><span data-ttu-id="d05ba-103">Tables de files d’attente sortantes</span><span class="sxs-lookup"><span data-stu-id="d05ba-103">Outgoing Queue Tables</span></span>

  
  
<span data-ttu-id="d05ba-104">**S’applique à**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="d05ba-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="d05ba-105">Une table sortant de la file d’attente contient des informations sur tous les messages sortants pour une banque de messages.</span><span class="sxs-lookup"><span data-stu-id="d05ba-105">An outgoing queue table contains information about all the outgoing messages for a message store.</span></span> <span data-ttu-id="d05ba-106">Implémentés par les fournisseurs de banque de message sortant tables de file d’attente pour le spouleur MAPI à utiliser.</span><span class="sxs-lookup"><span data-stu-id="d05ba-106">Message store providers implement outgoing queue tables for the MAPI spooler to use.</span></span> <span data-ttu-id="d05ba-107">Magasins qui ne prennent pas en charge l’envoi ou la réception de messages ne doit pas mettre ce tableau.</span><span class="sxs-lookup"><span data-stu-id="d05ba-107">Stores that do not support the sending or receiving of messages need not implement this table.</span></span> 
  
<span data-ttu-id="d05ba-108">Pour accéder à une table de file d’attente sortante, le spouleur MAPI appelle la méthode [IMsgStore::GetOutgoingQueue](imsgstore-getoutgoingqueue.md) .</span><span class="sxs-lookup"><span data-stu-id="d05ba-108">To access an outgoing queue table, the MAPI spooler calls the [IMsgStore::GetOutgoingQueue](imsgstore-getoutgoingqueue.md) method.</span></span> 
  
<span data-ttu-id="d05ba-109">Il est nécessaire que les messages prétraités et soumises au fournisseur de transport dans le même ordre qu’ils ont été envoyés par l’application cliente.</span><span class="sxs-lookup"><span data-stu-id="d05ba-109">There is a requirement that messages be preprocessed and submitted to the transport provider in the same order as they were sent by the client application.</span></span> <span data-ttu-id="d05ba-110">Le spouleur MAPI est conçu pour accepter les messages de la banque de messages dans l’ordre croissant de l’heure de soumission.</span><span class="sxs-lookup"><span data-stu-id="d05ba-110">The MAPI spooler is designed to accept messages from the message store in ascending order of submission time.</span></span> <span data-ttu-id="d05ba-111">En raison de cette exigence, il peut être quelque temps avant que certains messages s’affichent dans le tableau sortant de la file d’attente.</span><span class="sxs-lookup"><span data-stu-id="d05ba-111">Because of this requirement, there can be some delay before some messages appear in the outgoing queue table.</span></span> 
  
<span data-ttu-id="d05ba-112">Banques de messages doivent soit autoriser le tri de la table de file d’attente sortante afin que le spouleur MAPI permettre trier les messages par heure de soumission ou l’ordre de tri par défaut doit être par ordre croissant heure de soumission.</span><span class="sxs-lookup"><span data-stu-id="d05ba-112">Message stores should either allow sorting on the outgoing queue table so that the MAPI spooler can sort the messages by submission time, or the default sort order should be by ascending submission time.</span></span> 
  
<span data-ttu-id="d05ba-113">Le tableau sortant de la file d’attente doit envoyer des notifications lorsque le contenu de la file d’attente est modifié.</span><span class="sxs-lookup"><span data-stu-id="d05ba-113">The outgoing queue table must send notifications when the contents of the queue changes.</span></span>
  
<span data-ttu-id="d05ba-114">Les propriétés suivantes constituent la colonne requise définie dans les tableaux de file d’attente sortant :</span><span class="sxs-lookup"><span data-stu-id="d05ba-114">The following properties make up the required column set in outgoing queue tables:</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="d05ba-115">**PR_CLIENT_SUBMIT_TIME** ([PidTagClientSubmitTime](pidtagclientsubmittime-canonical-property.md))</span><span class="sxs-lookup"><span data-stu-id="d05ba-115">**PR_CLIENT_SUBMIT_TIME** ([PidTagClientSubmitTime](pidtagclientsubmittime-canonical-property.md))</span></span>  <br/> |<span data-ttu-id="d05ba-116">**PR_DISPLAY_BCC** ([PidTagDisplayBcc](pidtagdisplaybcc-canonical-property.md))</span><span class="sxs-lookup"><span data-stu-id="d05ba-116">**PR_DISPLAY_BCC** ([PidTagDisplayBcc](pidtagdisplaybcc-canonical-property.md))</span></span>  <br/> |
|<span data-ttu-id="d05ba-117">**PR_DISPLAY_CC** ([PidTagDisplayCc](pidtagdisplaycc-canonical-property.md))</span><span class="sxs-lookup"><span data-stu-id="d05ba-117">**PR_DISPLAY_CC** ([PidTagDisplayCc](pidtagdisplaycc-canonical-property.md))</span></span>  <br/> |<span data-ttu-id="d05ba-118">**PR_DISPLAY_TO** ([PidTagDisplayTo](pidtagdisplayto-canonical-property.md))</span><span class="sxs-lookup"><span data-stu-id="d05ba-118">**PR_DISPLAY_TO** ([PidTagDisplayTo](pidtagdisplayto-canonical-property.md))</span></span>  <br/> |
|<span data-ttu-id="d05ba-119">**PR_ENTRYID** ([PidTagEntryId](pidtagentryid-canonical-property.md))</span><span class="sxs-lookup"><span data-stu-id="d05ba-119">**PR_ENTRYID** ([PidTagEntryId](pidtagentryid-canonical-property.md))</span></span>  <br/> |<span data-ttu-id="d05ba-120">**PR_MESSAGE_FLAGS** ([PidTagMessageFlags](pidtagmessageflags-canonical-property.md))</span><span class="sxs-lookup"><span data-stu-id="d05ba-120">**PR_MESSAGE_FLAGS** ([PidTagMessageFlags](pidtagmessageflags-canonical-property.md))</span></span>  <br/> |
|<span data-ttu-id="d05ba-121">**PR_MESSAGE_SIZE** ([PidTagMessageSize](pidtagmessagesize-canonical-property.md))</span><span class="sxs-lookup"><span data-stu-id="d05ba-121">**PR_MESSAGE_SIZE** ([PidTagMessageSize](pidtagmessagesize-canonical-property.md))</span></span>  <br/> |<span data-ttu-id="d05ba-122">**PR_PRIORITY** ([PidTagPriority](pidtagpriority-canonical-property.md))</span><span class="sxs-lookup"><span data-stu-id="d05ba-122">**PR_PRIORITY** ([PidTagPriority](pidtagpriority-canonical-property.md))</span></span>  <br/> |
|<span data-ttu-id="d05ba-123">**PR_SENDER_NAME** ([PidTagSenderName](pidtagsendername-canonical-property.md))</span><span class="sxs-lookup"><span data-stu-id="d05ba-123">**PR_SENDER_NAME** ([PidTagSenderName](pidtagsendername-canonical-property.md))</span></span>  <br/> |<span data-ttu-id="d05ba-124">**PR_SUBJECT** ([PidTagSubject](pidtagsubject-canonical-property.md))</span><span class="sxs-lookup"><span data-stu-id="d05ba-124">**PR_SUBJECT** ([PidTagSubject](pidtagsubject-canonical-property.md))</span></span>  <br/> |
|<span data-ttu-id="d05ba-125">**PR_SUBMIT_FLAGS** ([PidTagSubmitFlags](pidtagsubmitflags-canonical-property.md))</span><span class="sxs-lookup"><span data-stu-id="d05ba-125">**PR_SUBMIT_FLAGS** ([PidTagSubmitFlags](pidtagsubmitflags-canonical-property.md))</span></span>  <br/> | <br/> |
   
<span data-ttu-id="d05ba-126">Pour plus d’informations sur l’utilisation de la table sortant de la file d’attente, consultez [Envoi de Messages par les fournisseurs de banque de Message à l’aide](sending-messages-by-using-message-store-providers.md).</span><span class="sxs-lookup"><span data-stu-id="d05ba-126">For more information about how the outgoing queue table is used, see [Sending Messages by Using Message Store Providers](sending-messages-by-using-message-store-providers.md).</span></span>
  
## <a name="see-also"></a><span data-ttu-id="d05ba-127">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="d05ba-127">See also</span></span>



[<span data-ttu-id="d05ba-128">Tables MAPI</span><span class="sxs-lookup"><span data-stu-id="d05ba-128">MAPI Tables</span></span>](mapi-tables.md)

