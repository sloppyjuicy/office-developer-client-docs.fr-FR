---
title: Envoi ou réception d’un message à la demande
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: 479404c5-4926-402a-aa12-75dd23276d75
description: 'Dernière modification : 23 juillet 2011'
ms.openlocfilehash: 15b9c8c5a56b6f37464d2469bd1d7b3e24596502
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32356475"
---
# <a name="sending-or-receiving-a-message-on-demand"></a>Envoi ou réception d’un message à la demande
  
**S’applique à** : Outlook 2013 | Outlook 2016 
  
Les clients s'appuient généralement sur le sous-système MAPI, le spouleur MAPI et les fournisseurs de services, pour gérer le calendrier de transmission et de réception des messages. Toutefois, vous pouvez modifier ce délai à l'aide de l'objet Status du spouleur MAPI ou d'un fournisseur de transport.
  
La méthode [IMAPIStatus:: FlushQueues](imapistatus-flushqueues.md) supprime tous les messages d'une ou plusieurs files d'attente entrantes ou sortants d'un fournisseur de transport. Les procédures suivantes décrivent deux techniques pour l'envoi et la réception de messages à la demande. La première procédure utilise l'objet d'État du spouleur MAPI pour vider les files d'attente de chaque fournisseur de transport dans le profil; la deuxième procédure vide la file d'attente d'un fournisseur de transport unique. 
  
### <a name="to-flush-all-incoming-or-outgoing-queues-in-a-single-operation"></a>Pour vider toutes les files d'attente entrantes ou sortantes en une seule opération
  
1. Appelez [IMAPISession:: GetStatusTable](imapisession-getstatustable.md) pour accéder à la table d'État. 
    
2. Appelez la méthode [IMAPITable:: SetColumns](imapitable-setcolumns.md) de la table d'État pour limiter la valeur de la colonne à **PR_ENTRYID** ([PidTagEntryId](pidtagentryid-canonical-property.md)) et **PR_RESOURCE_TYPE** ([PidTagResourceType](pidtagresourcetype-canonical-property.md)).
    
3. Générez une restriction de propriété à l'aide d'une structure [SPropertyRestriction](spropertyrestriction.md) pour faire correspondre **PR_RESOURCE_TYPE** avec MAPI_SPOOLER. 
    
4. Appelez [HrQueryAllRows](hrqueryallrows.md), en transmettant la structure **SPropertyRestriction** , pour récupérer la ligne qui représente l'état du spouleur MAPI. 
    
5. TransMettez la colonne **PR_ENTRYID** à [IMAPISession:: OpenEntry](imapisession-openentry.md) pour ouvrir l'objet d'État du spouleur MAPI. 
    
6. Appelez la méthode [IMAPIStatus:: FlushQueues](imapistatus-flushqueues.md) du spouleur MAPI, en transmettant l'indicateur FLUSH_NO_UI pour supprimer l'interface utilisateur et l'indicateur FLUSH_DOWNLOAD ou FLUSH_UPLOAD pour vider les files d'attente sortantes ou entrantes. 
    
7. Libérez l'objet Status et la table Status, ainsi que la structure [SRowSet](srowset.md) allouée pour le tableau. 
    
### <a name="to-flush-incoming-or-outgoing-queues-individually-by-transport-provider"></a>Pour vider les files d'attente entrantes ou sortantes individuellement par fournisseur de transport
  
1. Appelez [IMAPISession:: GetStatusTable](imapisession-getstatustable.md) pour accéder à la table d'État. 
    
2. Appelez la méthode [IMAPITable:: SetColumns](imapitable-setcolumns.md) de la table d'État pour limiter la valeur de la colonne à **PR_ENTRYID** et **PR_RESOURCE_TYPE**.
    
3. Générez une restriction de propriété à l'aide d'une structure [SPropertyRestriction](spropertyrestriction.md) pour faire correspondre **PR_RESOURCE_TYPE** avec MAPI_TRANSPORT_PROVIDER. 
    
4. Appelez [HrQueryAllRows](hrqueryallrows.md)en transmettant la structure **SPropertyRestriction** pour récupérer les lignes fournies par les fournisseurs de transport. 
    
5. Pour chaque ligne renvoyée à partir de **HrQueryAllRows**:
    
    1. TransMettez la colonne **PR_ENTRYID** à [IMAPISession:: OpenEntry](imapisession-openentry.md) pour ouvrir l'objet d'État du fournisseur de transport. 
        
    2. Vérifiez que l'objet état de transport prend en charge la méthode **FlushQueues** en vérifiant que sa propriété **PR_RESOURCE_METHODS** ([PIDTAGRESOURCEMETHODS](pidtagresourcemethods-canonical-property.md)) a l'indicateur STATUS_FLUSH_QUEUES défini. 
        
    3. S'il est pris en charge, appelez [IMAPIStatus:: FlushQueues](imapistatus-flushqueues.md). Si ce n'est pas le cas, appelez la méthode **IMAPIStatus:: FlushQueues** du spouleur MAPI, en transmettant l'identificateur d'entrée du transport dans le paramètre _lpTargetTransport_ . Consultez la procédure précédente pour obtenir des instructions sur l'accès à l'objet d'État du spouleur MAPI. Définissez l'indicateur FLUSH_DOWNLOAD pour vider les files d'attente sortantes ou l'indicateur FLUSH_UPLOAD pour vider les files d'attente entrantes. 
        
    4. Libérez l'objet Status et la table Status, ainsi que la structure [SRowSet](srowset.md) allouée pour le tableau. 
    
Le spouleur MAPI honore l'indicateur FLUSH_NO_UI comme la plupart des fournisseurs de transport LAN. Toutefois, tous les fournisseurs de transport ne respectent pas cet indicateur, en particulier ceux qui utilisent un modem de manière explicite et le service d'accès à distance (RAS). RAS n'a pas été conçu pour permettre aux clients de supprimer l'interface utilisateur. Il est possible qu'un client soit configuré de sorte qu'il puisse se connecter sans nécessiter l'interaction d'un utilisateur, mais il est difficile et nécessite une connaissance approfondie des services de message du client.
  

