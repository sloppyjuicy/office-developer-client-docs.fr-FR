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
# <a name="opening-a-message"></a>Ouverture d’un message
 
**S’applique à** : Outlook 2013 | Outlook 2016 
  
### <a name="to-open-a-message"></a>Pour ouvrir un message
  
1. Récupérez l'identificateur d'entrée du message à partir de l'une des sources suivantes:
    
   - La ligne qui représente le message dans la table des matières de son dossier parent. Pour plus d'informations sur l'utilisation d'une table de contenu de dossier, voir [content tables](contents-tables.md).
    
   - Membre **lpEntryID** de la structure [NEWMAIL_NOTIFICATION](newmail_notification.md) qui est envoyé avec un nouveau message de notification. Pour plus d'informations sur la réception et la gestion des notifications, consultez la rubrique [gestion](handling-notifications.md)des notifications.
    
   - Un appel à la méthode [IMAPIProp:: GetProps](imapiprop-getprops.md) du message qui demande la propriété **PR_ENTRYID** ([PidTagEntryId](pidtagentryid-canonical-property.md)). 
    
2. Appelez l'une des méthodes **OpenEntry** suivantes pour ouvrir le message, en définissant _lpEntryID_ sur l'identificateur d'entrée du message: 
    
   - [IMAPIContainer::OpenEntry](imapicontainer-openentry.md)
    
   - [IMsgStore::OpenEntry](imsgstore-openentry.md)
    
   - [IMAPISession::OpenEntry](imapisession-openentry.md)
    
  La méthode la plus rapide est utilisable uniquement pour les messages entrants et implique l'appel de la méthode **IMAPIFolder:: OpenEntry** du dossier de réception. La méthode la plus rapide, qui appelle la méthode **IMsgStore:: OpenEntry** de la Banque de messages, peut être utilisée pour tous les messages comme la méthode la plus lente, en appelant **IMAPISession:: OpenEntry**.
    
> [!NOTE]
> Les dossiers et leurs tables de contenu peuvent être fermés à tout moment sans affecter de façon négative les messages qui ont été ouverts à partir de ces derniers. 
  
### <a name="to-open-a-message-that-has-been-saved-on-disk"></a>Pour ouvrir un message qui a été enregistré sur le disque
  
1. Appelez **StgOpenStorage** pour récupérer un pointeur d'interface **IStorage** , en transmettant le nom du fichier de message pour le paramètre _pwcsName_ . 
    
   ```cpp
    LPSTORAGE pStorage = NULL;
    HRESULT hr = StgOpenStorage (L"MESSAGE.MSG", NULL,
                                STGM_TRANSACTED |
                                STGM_READWRITE |
                                STGM_SHARE_EXCLUSIVE,
                                NULL, 0, &pStorage);
    
   ```

2. Appelez **OpenIMsgOnIStg** pour récupérer un pointeur d'interface **IMessage** permettant d'accéder au message. 
    
   ```cpp
    LPMESSAGE pMessage = NULL;
    LPMALLOC pMalloc = MAPIGetDefaultMalloc();
    hr = OpenIMsgOnIStg (NULL, MAPIAllocateBuffer, MAPIAllocateMore,
                        MAPIFreeBuffer, pMalloc, NULL, pStorage,
                        NULL, 0, 0, &pMessage);
    
   ```


