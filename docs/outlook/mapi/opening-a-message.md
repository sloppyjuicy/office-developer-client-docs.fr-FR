---
title: Ouverture d’un message
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.localizationpriority: medium
api_type:
- COM
ms.assetid: 142c4975-08df-4501-9996-557aa44eafb3
description: 'Derniére modification : samedi 23 juillet 2011'
ms.openlocfilehash: d74e26f2968758f31a410a428bd75b70803e5141
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/24/2021
ms.locfileid: "59555950"
---
# <a name="opening-a-message"></a>Ouverture d’un message
 
**S’applique à** : Outlook 2013 | Outlook 2016 
  
### <a name="to-open-a-message"></a>Pour ouvrir un message
  
1. Récupérez l’identificateur d’entrée du message à partir de l’une des sources suivantes :
    
   - Ligne qui représente le message dans la table des matières de son dossier parent. Pour plus d’informations sur l’working with a folder contents table, see [Contents Tables](contents-tables.md).
    
   - Membre **lpEntryID** de la structure [NEWMAIL_NOTIFICATION](newmail_notification.md) envoyée avec une nouvelle notification par courrier électronique. Pour plus d’informations sur la réception et la gestion des notifications, voir [Gestion des notifications.](handling-notifications.md)
    
   - Appel à la méthode [IMAPIProp::GetProps](imapiprop-getprops.md) du message demandant la propriété **PR_ENTRYID** ([PidTagEntryId](pidtagentryid-canonical-property.md)). 
    
2. Appelez l’une des méthodes **OpenEntry** suivantes pour ouvrir le message, en fixant  _lpEntryID_ sur l’identificateur d’entrée du message : 
    
   - [IMAPIContainer::OpenEntry](imapicontainer-openentry.md)
    
   - [IMsgStore::OpenEntry](imsgstore-openentry.md)
    
   - [IMAPISession::OpenEntry](imapisession-openentry.md)
    
  La méthode la plus rapide est utilisable uniquement pour les messages entrants et implique l’appel de la méthode **IMAPIFolder::OpenEntry** du dossier de réception. La méthode la plus rapide suivante, en appelant la méthode **IMsgStore::OpenEntry** de la boutique de messages, est utilisable pour tous les messages, tout comme la méthode la plus lente, en appelant **IMAPISession::OpenEntry**.
    
> [!NOTE]
> Les dossiers et leurs tables de contenu peuvent être fermés à tout moment sans affecter les messages qui ont été ouverts à partir de ces derniers. 
  
### <a name="to-open-a-message-that-has-been-saved-on-disk"></a>Pour ouvrir un message qui a été enregistré sur disque
  
1. Appelez **StgOpenStorage** pour récupérer un pointeur d’interface **IStorage,** en passant le nom du fichier de message pour le paramètre _pwcsName._ 
    
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


