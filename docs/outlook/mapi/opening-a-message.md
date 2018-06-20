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
# <a name="opening-a-message"></a>Ouverture d’un message
 
**S’applique à**: Outlook 
  
### <a name="to-open-a-message"></a>Pour ouvrir un message
  
1. Récupérer l’identificateur d’entrée du message d’une des sources suivantes :
    
   - La ligne qui représente le message dans la table des matières de son dossier parent. Pour plus d’informations sur l’utilisation d’un tableau contenu de dossier, voir les [Tables des matières](contents-tables.md).
    
   - Le membre **lpEntryID** de la structure [NEWMAIL_NOTIFICATION](newmail_notification.md) qui est envoyé avec une notification de nouveau courrier. Pour plus d’informations sur la réception et la gestion des notifications, voir [Gestion des Notifications](handling-notifications.md).
    
   - Un appel de méthode de [IMAPIProp::GetProps](imapiprop-getprops.md) du message demandant la propriété **PR_ENTRYID** ([PidTagEntryId](pidtagentryid-canonical-property.md)). 
    
2. Appelez l’une des méthodes suivantes **OpenEntry** pour ouvrir le message, le paramètre _lpEntryID_ à l’identificateur d’entrée du message : 
    
   - [IMAPIContainer::OpenEntry](imapicontainer-openentry.md)
    
   - [IMsgStore::OpenEntry](imsgstore-openentry.md)
    
   - [IMAPISession::OpenEntry](imapisession-openentry.md)
    
  La méthode la plus rapide est utilisable uniquement pour les messages entrants et implique l’appel de méthode **d’IMAPIFolder::OpenEntry** du dossier de réception. La méthode plus rapide, l’appel de méthode de **IMsgStore::OpenEntry** de la banque de messages, est utilisable pour tous les messages, ainsi que la méthode la plus lente, l’appel **IMAPISession::OpenEntry**.
    
> [!NOTE]
> Dossiers et les tables de contenu peuvent être fermés à tout moment sans affecter un des messages qui ont été ouverts à partir de leur. 
  
### <a name="to-open-a-message-that-has-been-saved-on-disk"></a>Pour ouvrir un message qui a été enregistré sur le disque
  
1. Appelez **StgOpenStorage** pour récupérer un pointeur d’interface **IStorage** , en passant le nom du fichier de message pour le paramètre _pwcsName_ . 
    
   ```cpp
    LPSTORAGE pStorage = NULL;
    HRESULT hr = StgOpenStorage (L"MESSAGE.MSG", NULL,
                                STGM_TRANSACTED |
                                STGM_READWRITE |
                                STGM_SHARE_EXCLUSIVE,
                                NULL, 0, &pStorage);
    
   ```

2. Appelez **OpenIMsgOnIStg** pour récupérer un pointeur d’interface **IMessage** pour accéder au message. 
    
   ```cpp
    LPMESSAGE pMessage = NULL;
    LPMALLOC pMalloc = MAPIGetDefaultMalloc();
    hr = OpenIMsgOnIStg (NULL, MAPIAllocateBuffer, MAPIAllocateMore,
                        MAPIFreeBuffer, pMalloc, NULL, pStorage,
                        NULL, 0, 0, &pMessage);
    
   ```


