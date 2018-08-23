---
title: Recherche de messages envoyés ou enregistrés
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: 6b6714a5-7f36-4a72-9a2a-0d7fdf0e21b7
description: 'Derniére modification : samedi 23 juillet 2011'
ms.openlocfilehash: 5a2e4f4b248cb8eefd5ee37c0c90d5ef9c0d0cac
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/23/2018
ms.locfileid: "22565017"
---
# <a name="finding-sent-or-saved-messages"></a><span data-ttu-id="765ff-103">Recherche de messages envoyés ou enregistrés</span><span class="sxs-lookup"><span data-stu-id="765ff-103">Finding Sent or Saved Messages</span></span>

  
  
<span data-ttu-id="765ff-104">**S’applique à**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="765ff-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
 <span data-ttu-id="765ff-105">**Pour rechercher tous les messages sortants que vous avez enregistré ou envoyé**</span><span class="sxs-lookup"><span data-stu-id="765ff-105">**To locate all the outgoing messages that you have saved or sent**</span></span>
  
1. <span data-ttu-id="765ff-106">Appelez [IMsgStore::CompareEntryIDs](imsgstore-compareentryids.md) pour comparer le dossier qui contient vos messages envoyés par le dossier qui contient les messages entrants.</span><span class="sxs-lookup"><span data-stu-id="765ff-106">Call [IMsgStore::CompareEntryIDs](imsgstore-compareentryids.md) to compare the folder that contains your sent messages with the folder that contains your incoming messages.</span></span> 
    
2. <span data-ttu-id="765ff-107">Définissez le paramètre _lpEntryID1_ pour pointer vers **PR_IPM_SENTMAIL_ENTRYID** ([PidTagIpmSentMailEntryId](pidtagipmsentmailentryid-canonical-property.md)) et le paramètre _lpEntryID2_ pour pointer vers **PR_PARENT_ENTRYID** ([PidTagParentEntryId](pidtagparententryid-canonical-property.md)).</span><span class="sxs-lookup"><span data-stu-id="765ff-107">Set the  _lpEntryID1_ parameter to point to **PR_IPM_SENTMAIL_ENTRYID** ([PidTagIpmSentMailEntryId](pidtagipmsentmailentryid-canonical-property.md)) and the  _lpEntryID2_ parameter to point to **PR_PARENT_ENTRYID** ([PidTagParentEntryId](pidtagparententryid-canonical-property.md)).</span></span>
    
<span data-ttu-id="765ff-108">Sachez que si vous supprimer les messages après leur sont envoyés ou que vous ont déplacé des messages envoyés vers un autre dossier, cette stratégie ne fonctionne pas.</span><span class="sxs-lookup"><span data-stu-id="765ff-108">Be aware that if you either delete messages after they are sent or have moved any of the sent messages to another folder, this strategy will not work.</span></span> 
  
<span data-ttu-id="765ff-109">Si en examinant un message entrant, vous constatez que les propriétés qui sont généralement définies par un fournisseur de transport sont manquantes, vous pouvez supposer que le message a été jamais géré par un fournisseur de transport.</span><span class="sxs-lookup"><span data-stu-id="765ff-109">If in examining an incoming message you notice that the properties that are typically set by a transport provider are missing, you can assume that the message was never handled by a transport provider.</span></span> <span data-ttu-id="765ff-110">Ces propriétés sont les suivantes :</span><span class="sxs-lookup"><span data-stu-id="765ff-110">These properties include:</span></span>
  
- <span data-ttu-id="765ff-111">Propriétés **PR_RECEIVED_BY**</span><span class="sxs-lookup"><span data-stu-id="765ff-111">**PR_RECEIVED_BY** properties</span></span> 
    
- <span data-ttu-id="765ff-112">**PR_MESSAGE_DOWNLOAD_TIME** ([PidTagMessageDownloadTime](pidtagmessagedownloadtime-canonical-property.md))</span><span class="sxs-lookup"><span data-stu-id="765ff-112">**PR_MESSAGE_DOWNLOAD_TIME** ([PidTagMessageDownloadTime](pidtagmessagedownloadtime-canonical-property.md))</span></span>
    
- <span data-ttu-id="765ff-113">**PR_TRANSPORT_MESSAGE_HEADERS** ([PidTagTransportMessageHeaders](pidtagtransportmessageheaders-canonical-property.md))</span><span class="sxs-lookup"><span data-stu-id="765ff-113">**PR_TRANSPORT_MESSAGE_HEADERS** ([PidTagTransportMessageHeaders](pidtagtransportmessageheaders-canonical-property.md))</span></span>
    
- <span data-ttu-id="765ff-114">**PR_MESSAGE_TO_ME** ([PidTagMessageToMe](pidtagmessagetome-canonical-property.md))</span><span class="sxs-lookup"><span data-stu-id="765ff-114">**PR_MESSAGE_TO_ME** ([PidTagMessageToMe](pidtagmessagetome-canonical-property.md))</span></span>
    
- <span data-ttu-id="765ff-115">**PR_MESSAGE_CC_ME** ([PidTagMessageCcMe](pidtagmessageccme-canonical-property.md))</span><span class="sxs-lookup"><span data-stu-id="765ff-115">**PR_MESSAGE_CC_ME** ([PidTagMessageCcMe](pidtagmessageccme-canonical-property.md))</span></span>
    
- <span data-ttu-id="765ff-116">**PR_MESSAGE_RECIP_ME** ([PidTagMessageRecipientMe](pidtagmessagerecipientme-canonical-property.md))</span><span class="sxs-lookup"><span data-stu-id="765ff-116">**PR_MESSAGE_RECIP_ME** ([PidTagMessageRecipientMe](pidtagmessagerecipientme-canonical-property.md))</span></span>
    

