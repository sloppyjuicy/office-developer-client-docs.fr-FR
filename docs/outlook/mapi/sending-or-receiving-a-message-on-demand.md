---
title: Envoyer ou recevoir un message à la demande
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: 479404c5-4926-402a-aa12-75dd23276d75
description: 'Derniére modification : samedi 23 juillet 2011'
ms.openlocfilehash: 668e1c57c59bf2356be808e0347e1bd5135478a2
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/23/2018
ms.locfileid: "22563890"
---
# <a name="sending-or-receiving-a-message-on-demand"></a>Envoyer ou recevoir un message à la demande
  
**S’applique à**: Outlook 2013 | Outlook 2016 
  
Clients comptent généralement sur le sous-système MAPI — le spouleur MAPI et les fournisseurs de services — pour gérer la synchronisation de la transmission de message et de réception. Toutefois, vous pouvez modifier ce délai à l’aide de l’objet d’état d’un fournisseur de transport ou le spouleur MAPI.
  
La méthode [IMAPIStatus::FlushQueues](imapistatus-flushqueues.md) supprime tous les messages des files d’attente entrant ou sortant un ou plusieurs du fournisseur de transport. Les procédures suivantes décrivent les deux techniques pour envoyer ou recevoir de messages à la demande. La première procédure utilise un objet de l’état du spouleur MAPI pour vider les files d’attente de chaque fournisseur de transport dans le profil ; la seconde procédure vide la file d’attente d’un fournisseur de transport unique. 
  
### <a name="to-flush-all-incoming-or-outgoing-queues-in-a-single-operation"></a>Pour vider toutes les files entrants ou sortants en une seule opération
  
1. Appelez [IMAPISession::GetStatusTable](imapisession-getstatustable.md) pour accéder à la table d’état. 
    
2. Appelez la méthode de [IMAPITable::SetColumns](imapitable-setcolumns.md) de la table d’état pour limiter la colonne valeur **PR_ENTRYID** ([PidTagEntryId](pidtagentryid-canonical-property.md)) et **PR_RESOURCE_TYPE** ([PidTagResourceType](pidtagresourcetype-canonical-property.md)).
    
3. Créer une restriction de propriété à l’aide d’une structure [SPropertyRestriction](spropertyrestriction.md) pour la correspondance de **PR_RESOURCE_TYPE** avec MAPI_SPOOLER. 
    
4. Appelez [HrQueryAllRows](hrqueryallrows.md), en passant la structure **SPropertyRestriction** , pour récupérer la ligne qui représente l’état du spouleur MAPI. 
    
5. Passez la colonne **PR_ENTRYID** à [IMAPISession::OpenEntry](imapisession-openentry.md) pour ouvrir statut objet du spouleur MAPI. 
    
6. Appelez [IMAPIStatus::FlushQueues](imapistatus-flushqueues.md) méthode du spouleur MAPI, en passant l’indicateur FLUSH_NO_UI pour supprimer l’interface utilisateur et indicateur FLUSH_UPLOAD ou FLUSH_DOWNLOAD pour vider les files d’attente entrants ou sortants. 
    
7. Version de l’objet de l’état et la table d’état, ainsi que la structure [SRowSet](srowset.md) qui est allouée à la table. 
    
### <a name="to-flush-incoming-or-outgoing-queues-individually-by-transport-provider"></a>Pour vider les files d’attente entrants ou sortants individuellement par le fournisseur de transport
  
1. Appelez [IMAPISession::GetStatusTable](imapisession-getstatustable.md) pour accéder à la table d’état. 
    
2. Appeler la méthode de [IMAPITable::SetColumns](imapitable-setcolumns.md) de la table d’état pour limiter la colonne valeur **PR_ENTRYID** et **PR_RESOURCE_TYPE**.
    
3. Créer une restriction de propriété à l’aide d’une structure [SPropertyRestriction](spropertyrestriction.md) pour la correspondance de **PR_RESOURCE_TYPE** avec MAPI_TRANSPORT_PROVIDER. 
    
4. Appelez [HrQueryAllRows](hrqueryallrows.md), en passant la structure **SPropertyRestriction** , pour récupérer les lignes qui sont fournis par des fournisseurs de transport. 
    
5. Pour chaque ligne renvoyée par **HrQueryAllRows**:
    
    1. Passez la colonne **PR_ENTRYID** à [IMAPISession::OpenEntry](imapisession-openentry.md) pour ouvrir l’objet de l’état du fournisseur de transport. 
        
    2. Vérifiez que l’objet d’état de transport prend en charge la méthode **FlushQueues** en vérifiant que sa propriété **PR_RESOURCE_METHODS** ([PidTagResourceMethods](pidtagresourcemethods-canonical-property.md)) a la STATUS_FLUSH_QUEUES l’indicateur est défini. 
        
    3. Si prise en charge, appelez [IMAPIStatus::FlushQueues](imapistatus-flushqueues.md). Si non pris en charge, appelez **IMAPIStatus::FlushQueues** méthode du spouleur MAPI, en passant l’identificateur d’entrée du transport dans le paramètre _lpTargetTransport_ . Voir la procédure précédente pour obtenir des instructions sur l’accès aux objet d’état du spouleur MAPI. Définir l’indicateur FLUSH_DOWNLOAD pour vider les files d’attente sortantes ou le FLUSH_UPLOAD à vider les files d’attente entrants. 
        
    4. Version de l’objet de l’état et la table d’état, ainsi que la structure [SRowSet](srowset.md) qui est allouée à la table. 
    
Le spouleur MAPI respecte l’indicateur FLUSH_NO_UI comme la plupart des fournisseurs de transport du réseau local. Toutefois, tous les fournisseurs de transport Honorer cet indicateur, notamment celles qui utilisent un modem explicitement et le Service d’accès à distance (RAS). RAS n’a pas été conçu pour permettre aux clients supprimer l’interface utilisateur. Il est possible pour un client à configurer afin qu’il peut se connecter sans nécessiter l’interaction d’un utilisateur, mais il est difficile et nécessite une connaissance approfondie des services de message du client.
  

