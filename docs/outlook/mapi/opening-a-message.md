---
title: Ouverture d’un message
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: 142c4975-08df-4501-9996-557aa44eafb3
description: 'Derniére modification : samedi 23 juillet 2011'
ms.openlocfilehash: bf633a971f7e3077ce2f418021ef183a36db8cc8
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/28/2019
ms.locfileid: "33411091"
---
# <a name="opening-a-message"></a><span data-ttu-id="c6936-103">Ouverture d’un message</span><span class="sxs-lookup"><span data-stu-id="c6936-103">Opening a message</span></span>
 
<span data-ttu-id="c6936-104">**S’applique à** : Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="c6936-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
### <a name="to-open-a-message"></a><span data-ttu-id="c6936-105">Pour ouvrir un message</span><span class="sxs-lookup"><span data-stu-id="c6936-105">To open a message</span></span>
  
1. <span data-ttu-id="c6936-106">Récupérez l'identificateur d'entrée du message à partir de l'une des sources suivantes:</span><span class="sxs-lookup"><span data-stu-id="c6936-106">Retrieve the message's entry identifier from one of the following sources:</span></span>
    
   - <span data-ttu-id="c6936-107">La ligne qui représente le message dans la table des matières de son dossier parent.</span><span class="sxs-lookup"><span data-stu-id="c6936-107">The row that represents the message in the contents table of its parent folder.</span></span> <span data-ttu-id="c6936-108">Pour plus d'informations sur l'utilisation d'une table de contenu de dossier, voir [content tables](contents-tables.md).</span><span class="sxs-lookup"><span data-stu-id="c6936-108">For more information about working with a folder contents table, see [Contents Tables](contents-tables.md).</span></span>
    
   - <span data-ttu-id="c6936-109">Membre **lpEntryID** de la structure [NEWMAIL_NOTIFICATION](newmail_notification.md) qui est envoyé avec un nouveau message de notification.</span><span class="sxs-lookup"><span data-stu-id="c6936-109">The **lpEntryID** member of the [NEWMAIL_NOTIFICATION](newmail_notification.md) structure that is sent with a new mail notification.</span></span> <span data-ttu-id="c6936-110">Pour plus d'informations sur la réception et la gestion des notifications, consultez la rubrique [gestion](handling-notifications.md)des notifications.</span><span class="sxs-lookup"><span data-stu-id="c6936-110">For more information about receiving and handling notifications, see [Handling Notifications](handling-notifications.md).</span></span>
    
   - <span data-ttu-id="c6936-111">Un appel à la méthode [IMAPIProp:: GetProps](imapiprop-getprops.md) du message qui demande la propriété **PR_ENTRYID** ([PidTagEntryId](pidtagentryid-canonical-property.md)).</span><span class="sxs-lookup"><span data-stu-id="c6936-111">A call to the message's [IMAPIProp::GetProps](imapiprop-getprops.md) method requesting the **PR_ENTRYID** ([PidTagEntryId](pidtagentryid-canonical-property.md)) property.</span></span> 
    
2. <span data-ttu-id="c6936-112">Appelez l'une des méthodes **OpenEntry** suivantes pour ouvrir le message, en définissant _lpEntryID_ sur l'identificateur d'entrée du message:</span><span class="sxs-lookup"><span data-stu-id="c6936-112">Call one of the following **OpenEntry** methods to open the message, setting  _lpEntryID_ to the message's entry identifier:</span></span> 
    
   - [<span data-ttu-id="c6936-113">IMAPIContainer::OpenEntry</span><span class="sxs-lookup"><span data-stu-id="c6936-113">IMAPIContainer::OpenEntry</span></span>](imapicontainer-openentry.md)
    
   - [<span data-ttu-id="c6936-114">IMsgStore::OpenEntry</span><span class="sxs-lookup"><span data-stu-id="c6936-114">IMsgStore::OpenEntry</span></span>](imsgstore-openentry.md)
    
   - [<span data-ttu-id="c6936-115">IMAPISession::OpenEntry</span><span class="sxs-lookup"><span data-stu-id="c6936-115">IMAPISession::OpenEntry</span></span>](imapisession-openentry.md)
    
  <span data-ttu-id="c6936-116">La méthode la plus rapide est utilisable uniquement pour les messages entrants et implique l'appel de la méthode **IMAPIFolder:: OpenEntry** du dossier de réception.</span><span class="sxs-lookup"><span data-stu-id="c6936-116">The fastest method is usable only for incoming messages and involves calling the receive folder's **IMAPIFolder::OpenEntry** method.</span></span> <span data-ttu-id="c6936-117">La méthode la plus rapide, qui appelle la méthode **IMsgStore:: OpenEntry** de la Banque de messages, peut être utilisée pour tous les messages comme la méthode la plus lente, en appelant **IMAPISession:: OpenEntry**.</span><span class="sxs-lookup"><span data-stu-id="c6936-117">The next fastest method, calling the message store's **IMsgStore::OpenEntry** method, is usable for all messages as is the slowest method, calling **IMAPISession::OpenEntry**.</span></span>
    
> [!NOTE]
> <span data-ttu-id="c6936-118">Les dossiers et leurs tables de contenu peuvent être fermés à tout moment sans affecter de façon négative les messages qui ont été ouverts à partir de ces derniers.</span><span class="sxs-lookup"><span data-stu-id="c6936-118">Folders and their contents tables can be closed at any time without adversely affecting any of the messages that were opened from within them.</span></span> 
  
### <a name="to-open-a-message-that-has-been-saved-on-disk"></a><span data-ttu-id="c6936-119">Pour ouvrir un message qui a été enregistré sur le disque</span><span class="sxs-lookup"><span data-stu-id="c6936-119">To open a message that has been saved on disk</span></span>
  
1. <span data-ttu-id="c6936-120">Appelez **StgOpenStorage** pour récupérer un pointeur d'interface **IStorage** , en transmettant le nom du fichier de message pour le paramètre _pwcsName_ .</span><span class="sxs-lookup"><span data-stu-id="c6936-120">Call **StgOpenStorage** to retrieve an **IStorage** interface pointer, passing the name of the message file for the  _pwcsName_ parameter.</span></span> 
    
   ```cpp
    LPSTORAGE pStorage = NULL;
    HRESULT hr = StgOpenStorage (L"MESSAGE.MSG", NULL,
                                STGM_TRANSACTED |
                                STGM_READWRITE |
                                STGM_SHARE_EXCLUSIVE,
                                NULL, 0, &pStorage);
    
   ```

2. <span data-ttu-id="c6936-121">Appelez **OpenIMsgOnIStg** pour récupérer un pointeur d'interface **IMessage** permettant d'accéder au message.</span><span class="sxs-lookup"><span data-stu-id="c6936-121">Call **OpenIMsgOnIStg** to retrieve an **IMessage** interface pointer to access the message.</span></span> 
    
   ```cpp
    LPMESSAGE pMessage = NULL;
    LPMALLOC pMalloc = MAPIGetDefaultMalloc();
    hr = OpenIMsgOnIStg (NULL, MAPIAllocateBuffer, MAPIAllocateMore,
                        MAPIFreeBuffer, pMalloc, NULL, pStorage,
                        NULL, 0, 0, &pMessage);
    
   ```


