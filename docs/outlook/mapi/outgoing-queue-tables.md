---
title: Tables de file d'attente sortantes
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: 070377ca-ba9e-42ef-ac6b-ff7548b5ccf5
description: Dernière modification le 9 mars 2015
ms.openlocfilehash: 4bf935f58fb20460bbf6baf4b1434be1f3ab8156
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/28/2019
ms.locfileid: "33437573"
---
# <a name="outgoing-queue-tables"></a><span data-ttu-id="95fd3-103">Tables de file d'attente sortantes</span><span class="sxs-lookup"><span data-stu-id="95fd3-103">Outgoing Queue Tables</span></span>

  
  
<span data-ttu-id="95fd3-104">**S’applique à** : Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="95fd3-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="95fd3-105">Une table de file d'attente sortante contient des informations sur tous les messages sortants d'une banque de messages.</span><span class="sxs-lookup"><span data-stu-id="95fd3-105">An outgoing queue table contains information about all the outgoing messages for a message store.</span></span> <span data-ttu-id="95fd3-106">Les fournisseurs de banque de messages implémentent des tables de file d'attente sortantes que le spouleur MAPI doit utiliser.</span><span class="sxs-lookup"><span data-stu-id="95fd3-106">Message store providers implement outgoing queue tables for the MAPI spooler to use.</span></span> <span data-ttu-id="95fd3-107">Les banques qui ne prennent pas en charge l'envoi ou la réception de messages n'ont pas besoin d'implémenter ce tableau.</span><span class="sxs-lookup"><span data-stu-id="95fd3-107">Stores that do not support the sending or receiving of messages need not implement this table.</span></span> 
  
<span data-ttu-id="95fd3-108">Pour accéder à une table de file d'attente de messages sortants, le spouleur MAPI appelle la méthode [IMsgStore:: GetOutgoingQueue](imsgstore-getoutgoingqueue.md) .</span><span class="sxs-lookup"><span data-stu-id="95fd3-108">To access an outgoing queue table, the MAPI spooler calls the [IMsgStore::GetOutgoingQueue](imsgstore-getoutgoingqueue.md) method.</span></span> 
  
<span data-ttu-id="95fd3-109">Il est nécessaire que les messages soient prétraités et envoyés au fournisseur de transport dans l'ordre dans lequel ils ont été envoyés par l'application cliente.</span><span class="sxs-lookup"><span data-stu-id="95fd3-109">There is a requirement that messages be preprocessed and submitted to the transport provider in the same order as they were sent by the client application.</span></span> <span data-ttu-id="95fd3-110">Le spouleur MAPI est conçu pour accepter les messages de la Banque de messages dans l'ordre croissant de la durée de dépôt.</span><span class="sxs-lookup"><span data-stu-id="95fd3-110">The MAPI spooler is designed to accept messages from the message store in ascending order of submission time.</span></span> <span data-ttu-id="95fd3-111">En raison de cette exigence, un certain délai peut s'écouler avant que certains messages apparaissent dans la table de file d'attente sortante.</span><span class="sxs-lookup"><span data-stu-id="95fd3-111">Because of this requirement, there can be some delay before some messages appear in the outgoing queue table.</span></span> 
  
<span data-ttu-id="95fd3-112">Les banques de messages doivent autoriser le tri sur la table de file d'attente sortante afin que le spouleur MAPI puisse trier les messages par heure de dépôt ou que l'ordre de tri par défaut soit défini par ordre croissant.</span><span class="sxs-lookup"><span data-stu-id="95fd3-112">Message stores should either allow sorting on the outgoing queue table so that the MAPI spooler can sort the messages by submission time, or the default sort order should be by ascending submission time.</span></span> 
  
<span data-ttu-id="95fd3-113">La table de file d'attente sortante doit envoyer des notifications lorsque le contenu de la file d'attente est modifié.</span><span class="sxs-lookup"><span data-stu-id="95fd3-113">The outgoing queue table must send notifications when the contents of the queue changes.</span></span>
  
<span data-ttu-id="95fd3-114">Les propriétés suivantes constituent le jeu de colonnes obligatoire dans les tables de file d'attente sortantes:</span><span class="sxs-lookup"><span data-stu-id="95fd3-114">The following properties make up the required column set in outgoing queue tables:</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="95fd3-115">**PR_CLIENT_SUBMIT_TIME** ([PidTagClientSubmitTime](pidtagclientsubmittime-canonical-property.md))</span><span class="sxs-lookup"><span data-stu-id="95fd3-115">**PR_CLIENT_SUBMIT_TIME** ([PidTagClientSubmitTime](pidtagclientsubmittime-canonical-property.md))</span></span>  <br/> |<span data-ttu-id="95fd3-116">**PR_DISPLAY_BCC** ([PidTagDisplayBcc](pidtagdisplaybcc-canonical-property.md))</span><span class="sxs-lookup"><span data-stu-id="95fd3-116">**PR_DISPLAY_BCC** ([PidTagDisplayBcc](pidtagdisplaybcc-canonical-property.md))</span></span>  <br/> |
|<span data-ttu-id="95fd3-117">**PR_DISPLAY_CC** ([PidTagDisplayCc](pidtagdisplaycc-canonical-property.md))</span><span class="sxs-lookup"><span data-stu-id="95fd3-117">**PR_DISPLAY_CC** ([PidTagDisplayCc](pidtagdisplaycc-canonical-property.md))</span></span>  <br/> |<span data-ttu-id="95fd3-118">**PR_DISPLAY_TO** ([PidTagDisplayTo](pidtagdisplayto-canonical-property.md))</span><span class="sxs-lookup"><span data-stu-id="95fd3-118">**PR_DISPLAY_TO** ([PidTagDisplayTo](pidtagdisplayto-canonical-property.md))</span></span>  <br/> |
|<span data-ttu-id="95fd3-119">**PR_ENTRYID** ([PidTagEntryId](pidtagentryid-canonical-property.md))</span><span class="sxs-lookup"><span data-stu-id="95fd3-119">**PR_ENTRYID** ([PidTagEntryId](pidtagentryid-canonical-property.md))</span></span>  <br/> |<span data-ttu-id="95fd3-120">**PR_MESSAGE_FLAGS** ([PidTagMessageFlags](pidtagmessageflags-canonical-property.md))</span><span class="sxs-lookup"><span data-stu-id="95fd3-120">**PR_MESSAGE_FLAGS** ([PidTagMessageFlags](pidtagmessageflags-canonical-property.md))</span></span>  <br/> |
|<span data-ttu-id="95fd3-121">**PR_MESSAGE_SIZE** ([PidTagMessageSize](pidtagmessagesize-canonical-property.md))</span><span class="sxs-lookup"><span data-stu-id="95fd3-121">**PR_MESSAGE_SIZE** ([PidTagMessageSize](pidtagmessagesize-canonical-property.md))</span></span>  <br/> |<span data-ttu-id="95fd3-122">**PR_PRIORITY** ([PidTagPriority](pidtagpriority-canonical-property.md))</span><span class="sxs-lookup"><span data-stu-id="95fd3-122">**PR_PRIORITY** ([PidTagPriority](pidtagpriority-canonical-property.md))</span></span>  <br/> |
|<span data-ttu-id="95fd3-123">**PR_SENDER_NAME** ([PidTagSenderName](pidtagsendername-canonical-property.md))</span><span class="sxs-lookup"><span data-stu-id="95fd3-123">**PR_SENDER_NAME** ([PidTagSenderName](pidtagsendername-canonical-property.md))</span></span>  <br/> |<span data-ttu-id="95fd3-124">**PR_SUBJECT** ([PidTagSubject](pidtagsubject-canonical-property.md))</span><span class="sxs-lookup"><span data-stu-id="95fd3-124">**PR_SUBJECT** ([PidTagSubject](pidtagsubject-canonical-property.md))</span></span>  <br/> |
|<span data-ttu-id="95fd3-125">**PR_SUBMIT_FLAGS** ([PidTagSubmitFlags](pidtagsubmitflags-canonical-property.md))</span><span class="sxs-lookup"><span data-stu-id="95fd3-125">**PR_SUBMIT_FLAGS** ([PidTagSubmitFlags](pidtagsubmitflags-canonical-property.md))</span></span>  <br/> | <br/> |
   
<span data-ttu-id="95fd3-126">Pour plus d'informations sur l'utilisation de la table de file d'attente de messages sortants, consultez la rubrique [envoi de messages à l'aide de fournisseurs de banques de messages](sending-messages-by-using-message-store-providers.md).</span><span class="sxs-lookup"><span data-stu-id="95fd3-126">For more information about how the outgoing queue table is used, see [Sending Messages by Using Message Store Providers](sending-messages-by-using-message-store-providers.md).</span></span>
  
## <a name="see-also"></a><span data-ttu-id="95fd3-127">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="95fd3-127">See also</span></span>



[<span data-ttu-id="95fd3-128">Tables MAPI</span><span class="sxs-lookup"><span data-stu-id="95fd3-128">MAPI Tables</span></span>](mapi-tables.md)

