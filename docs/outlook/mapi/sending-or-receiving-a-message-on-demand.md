---
title: Envoi ou réception d’un message à la demande
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.localizationpriority: medium
api_type:
- COM
ms.assetid: 479404c5-4926-402a-aa12-75dd23276d75
ms.openlocfilehash: 84c796bbf9dae082ae32137a26f2695f298da0b3
ms.sourcegitcommit: 518845d053a009b11c8d907a33822161c0b6bc96
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/08/2022
ms.locfileid: "63373646"
---
# <a name="sending-or-receiving-a-message-on-demand"></a>Envoi ou réception d’un message à la demande
  
**S’applique à** : Outlook 2013 | Outlook 2016 
  
Les clients s’appuient généralement sur le sous-système MAPI (lepooler MAPI et les fournisseurs de services) pour gérer le minutage de la transmission et de la réception des messages. Toutefois, vous pouvez modifier ce minutage à l’aide de l’objet d’état dupooler MAPI ou d’un fournisseur de transport.
  
La [méthode IMAPIStatus::FlushQueues](imapistatus-flushqueues.md) supprime tous les messages des files d’attente entrantes ou sortantes d’un ou de plusieurs fournisseurs de transport. Les procédures suivantes décrivent deux techniques d’envoi ou de réception de messages à la demande. La première procédure utilise l’objet d’état dupooler MAPI pour vider les files d’attente de chaque fournisseur de transport dans le profil . La deuxième procédure vide la file d’attente d’un fournisseur de transport unique. 
  
### <a name="to-flush-all-incoming-or-outgoing-queues-in-a-single-operation"></a>Pour vider toutes les files d’attente entrantes ou sortantes en une seule opération
  
1. [Appelez IMAPISession::GetStatusTable](imapisession-getstatustable.md) pour accéder à la table d’état. 
    
2. Appelez la méthode [IMAPITable::SetColumns](imapitable-setcolumns.md) de la table d’état pour limiter le jeu de colonnes à **PR_ENTRYID** ([PidTagEntryId](pidtagentryid-canonical-property.md)) et **PR_RESOURCE_TYPE** ([PidTagResourceType](pidtagresourcetype-canonical-property.md)).
    
3. Créez une restriction de propriété à l’aide d’une structure [SPropertyRestriction](spropertyrestriction.md) pour **PR_RESOURCE_TYPE avec MAPI_SPOOLER** . 
    
4. [Appelez HrQueryAllRows](hrqueryallrows.md), en passant la structure **SPropertyRestriction**, pour récupérer la ligne qui représente l’état dupooler MAPI. 
    
5. Passez la **PR_ENTRYID** à [IMAPISession::OpenEntry](imapisession-openentry.md) pour ouvrir l’objet d’état dupooler MAPI. 
    
6. Appelez la méthode [IMAPIStatus::FlushQueues](imapistatus-flushqueues.md) dupooler MAPI, en passant l’indicateur FLUSH_NO_UI pour supprimer l’interface utilisateur et l’indicateur FLUSH_DOWNLOAD ou FLUSH_UPLOAD pour vider les files d’attente sortantes ou entrantes. 
    
7. Release the status object and the status table, as well as the [SRowSet](srowset.md) structure that is allocated for the table. 
    
### <a name="to-flush-incoming-or-outgoing-queues-individually-by-transport-provider"></a>Pour vider les files d’attente entrantes ou sortantes individuellement par fournisseur de transport
  
1. [Appelez IMAPISession::GetStatusTable](imapisession-getstatustable.md) pour accéder à la table d’état. 
    
2. Appelez la méthode [IMAPITable::SetColumns](imapitable-setcolumns.md) de la table d’état pour limiter le jeu de colonnes **PR_ENTRYID** et **PR_RESOURCE_TYPE**.
    
3. Créez une restriction de propriété à l’aide d’une structure [SPropertyRestriction](spropertyrestriction.md) pour **PR_RESOURCE_TYPE avec MAPI_TRANSPORT_PROVIDER** . 
    
4. [Appelez HrQueryAllRows](hrqueryallrows.md), en passant la structure **SPropertyRestriction**, pour récupérer les lignes fournies par les fournisseurs de transport. 
    
5. Pour chaque ligne renvoyée **par HrQueryAllRows** :
    
    1. Passez la **PR_ENTRYID** à [IMAPISession::OpenEntry](imapisession-openentry.md) pour ouvrir l’objet d’état du fournisseur de transport. 
        
    2. Vérifiez que l’objet d’état de transport prend en charge la méthode **FlushQueues** en vérifiant que sa propriété **PR_RESOURCE_METHODS** ([PidTagResourceMethods](pidtagresourcemethods-canonical-property.md)) possède l’indicateur STATUS_FLUSH_QUEUES définie. 
        
    3. Si pris en charge, appelez [IMAPIStatus::FlushQueues](imapistatus-flushqueues.md). Si ce paramètre n’est pas pris en compte, appelez la méthode **IMAPIStatus::FlushQueues** dupooler MAPI, en passant l’identificateur d’entrée du transport dans le paramètre _lpTargetTransport_ . Consultez la procédure précédente pour obtenir des instructions sur l’accès à l’objet d’état dupooler MAPI. Définissez l FLUSH_DOWNLOAD pour vider les files d’attente sortantes ou l’indicateur FLUSH_UPLOAD pour vider les files d’attente entrantes. 
        
    4. Release the status object and the status table, as well as the [SRowSet](srowset.md) structure that is allocated for the table. 
    
Lepooler MAPI honore l’FLUSH_NO_UI comme la plupart des fournisseurs de transport LAN. Toutefois, tous les fournisseurs de transport ne respectent pas cet indicateur, en particulier ceux qui utilisent un modem explicitement et le service d’accès à distance (RAS). Ras n’a pas été conçu pour permettre aux clients de supprimer l’interface utilisateur. Il est possible pour un client d’être configuré de sorte qu’il puisse se connecter sans nécessiter l’interaction d’un utilisateur, mais il est difficile et nécessite une connaissance approfondie des services de message du client.
  

