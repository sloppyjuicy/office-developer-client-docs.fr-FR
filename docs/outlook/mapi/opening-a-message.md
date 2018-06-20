---
title: Ouverture d’un message
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: 142c4975-08df-4501-9996-557aa44eafb3
description: 'Derni�re modification�: samedi 23 juillet 2011'
ms.openlocfilehash: 4ea75f723a2fcb242d8b9a516498855aa20cfdd4
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19784926"
---
# <a name="opening-a-message"></a><span data-ttu-id="1aa2e-103">Ouverture d’un message</span><span class="sxs-lookup"><span data-stu-id="1aa2e-103">Opening a message</span></span>
 
<span data-ttu-id="1aa2e-104">**S’applique à**: Outlook</span><span class="sxs-lookup"><span data-stu-id="1aa2e-104">**Applies to**: Outlook</span></span> 
  
### <a name="to-open-a-message"></a><span data-ttu-id="1aa2e-105">Pour ouvrir un message</span><span class="sxs-lookup"><span data-stu-id="1aa2e-105">To open a message</span></span>
  
1. <span data-ttu-id="1aa2e-106">Récupérer l’identificateur d’entrée du message d’une des sources suivantes :</span><span class="sxs-lookup"><span data-stu-id="1aa2e-106">Retrieve the message's entry identifier from one of the following sources:</span></span>
    
   - <span data-ttu-id="1aa2e-107">La ligne qui représente le message dans la table des matières de son dossier parent.</span><span class="sxs-lookup"><span data-stu-id="1aa2e-107">The row that represents the message in the contents table of its parent folder.</span></span> <span data-ttu-id="1aa2e-108">Pour plus d’informations sur l’utilisation d’un tableau contenu de dossier, voir les [Tables des matières](contents-tables.md).</span><span class="sxs-lookup"><span data-stu-id="1aa2e-108">For more information about working with a folder contents table, see [Contents Tables](contents-tables.md).</span></span>
    
   - <span data-ttu-id="1aa2e-109">Le membre **lpEntryID** de la structure [NEWMAIL_NOTIFICATION](newmail_notification.md) qui est envoyé avec une notification de nouveau courrier.</span><span class="sxs-lookup"><span data-stu-id="1aa2e-109">The **lpEntryID** member of the [NEWMAIL_NOTIFICATION](newmail_notification.md) structure that is sent with a new mail notification.</span></span> <span data-ttu-id="1aa2e-110">Pour plus d’informations sur la réception et la gestion des notifications, voir [Gestion des Notifications](handling-notifications.md).</span><span class="sxs-lookup"><span data-stu-id="1aa2e-110">For more information about receiving and handling notifications, see [Handling Notifications](handling-notifications.md).</span></span>
    
   - <span data-ttu-id="1aa2e-111">Un appel de méthode de [IMAPIProp::GetProps](imapiprop-getprops.md) du message demandant la propriété **PR_ENTRYID** ([PidTagEntryId](pidtagentryid-canonical-property.md)).</span><span class="sxs-lookup"><span data-stu-id="1aa2e-111">A call to the message's [IMAPIProp::GetProps](imapiprop-getprops.md) method requesting the **PR_ENTRYID** ([PidTagEntryId](pidtagentryid-canonical-property.md)) property.</span></span> 
    
2. <span data-ttu-id="1aa2e-112">Appelez l’une des méthodes suivantes **OpenEntry** pour ouvrir le message, le paramètre _lpEntryID_ à l’identificateur d’entrée du message :</span><span class="sxs-lookup"><span data-stu-id="1aa2e-112">Call one of the following **OpenEntry** methods to open the message, setting  _lpEntryID_ to the message's entry identifier:</span></span> 
    
   - [<span data-ttu-id="1aa2e-113">IMAPIContainer::OpenEntry</span><span class="sxs-lookup"><span data-stu-id="1aa2e-113">IMAPIContainer::OpenEntry</span></span>](imapicontainer-openentry.md)
    
   - [<span data-ttu-id="1aa2e-114">IMsgStore::OpenEntry</span><span class="sxs-lookup"><span data-stu-id="1aa2e-114">IMsgStore::OpenEntry</span></span>](imsgstore-openentry.md)
    
   - [<span data-ttu-id="1aa2e-115">IMAPISession::OpenEntry</span><span class="sxs-lookup"><span data-stu-id="1aa2e-115">IMAPISession::OpenEntry</span></span>](imapisession-openentry.md)
    
  <span data-ttu-id="1aa2e-116">La méthode la plus rapide est utilisable uniquement pour les messages entrants et implique l’appel de méthode **d’IMAPIFolder::OpenEntry** du dossier de réception.</span><span class="sxs-lookup"><span data-stu-id="1aa2e-116">The fastest method is usable only for incoming messages and involves calling the receive folder's **IMAPIFolder::OpenEntry** method.</span></span> <span data-ttu-id="1aa2e-117">La méthode plus rapide, l’appel de méthode de **IMsgStore::OpenEntry** de la banque de messages, est utilisable pour tous les messages, ainsi que la méthode la plus lente, l’appel **IMAPISession::OpenEntry**.</span><span class="sxs-lookup"><span data-stu-id="1aa2e-117">The next fastest method, calling the message store's **IMsgStore::OpenEntry** method, is usable for all messages as is the slowest method, calling **IMAPISession::OpenEntry**.</span></span>
    
> [!NOTE]
> <span data-ttu-id="1aa2e-118">Dossiers et les tables de contenu peuvent être fermés à tout moment sans affecter un des messages qui ont été ouverts à partir de leur.</span><span class="sxs-lookup"><span data-stu-id="1aa2e-118">Folders and their contents tables can be closed at any time without adversely affecting any of the messages that were opened from within them.</span></span> 
  
### <a name="to-open-a-message-that-has-been-saved-on-disk"></a><span data-ttu-id="1aa2e-119">Pour ouvrir un message qui a été enregistré sur le disque</span><span class="sxs-lookup"><span data-stu-id="1aa2e-119">To open a message that has been saved on disk</span></span>
  
1. <span data-ttu-id="1aa2e-120">Appelez **StgOpenStorage** pour récupérer un pointeur d’interface **IStorage** , en passant le nom du fichier de message pour le paramètre _pwcsName_ .</span><span class="sxs-lookup"><span data-stu-id="1aa2e-120">Call **StgOpenStorage** to retrieve an **IStorage** interface pointer, passing the name of the message file for the  _pwcsName_ parameter.</span></span> 
    
   ```cpp
    LPSTORAGE pStorage = NULL;
    HRESULT hr = StgOpenStorage (L"MESSAGE.MSG", NULL,
                                STGM_TRANSACTED |
                                STGM_READWRITE |
                                STGM_SHARE_EXCLUSIVE,
                                NULL, 0, &pStorage);
    
   ```

2. <span data-ttu-id="1aa2e-121">Appelez **OpenIMsgOnIStg** pour récupérer un pointeur d’interface **IMessage** pour accéder au message.</span><span class="sxs-lookup"><span data-stu-id="1aa2e-121">Call **OpenIMsgOnIStg** to retrieve an **IMessage** interface pointer to access the message.</span></span> 
    
   ```cpp
    LPMESSAGE pMessage = NULL;
    LPMALLOC pMalloc = MAPIGetDefaultMalloc();
    hr = OpenIMsgOnIStg (NULL, MAPIAllocateBuffer, MAPIAllocateMore,
                        MAPIFreeBuffer, pMalloc, NULL, pStorage,
                        NULL, 0, 0, &pMessage);
    
   ```


