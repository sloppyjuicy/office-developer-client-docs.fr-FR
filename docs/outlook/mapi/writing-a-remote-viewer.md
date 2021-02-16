---
title: Écriture d’une visionneuse à distance
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: f4d7d42f-688a-4199-b972-dd42528c0cdf
description: Dernière modification le 9 mars 2015
ms.openlocfilehash: 1d7fea7f92a315b9671d17c82a82d5d7d180f4bb
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32325661"
---
# <a name="writing-a-remote-viewer"></a>Écriture d’une visionneuse à distance

**S’applique à** : Outlook 2013 | Outlook 2016 
  
Une visionneuse à distance est une fenêtre d’une application cliente qui fournit un accès contrôlé aux messages stockés sur un autre ordinateur. Cet accès contrôlé peut fonctionner sur une liaison de communication lente. Au lieu de récupérer une sélection complète des messages disponibles chaque fois qu’un utilisateur ouvre un dossier, la visionneuse distante affiche d’abord uniquement les en-têtes. L’utilisateur sélectionne ensuite dans les en-têtes les messages à afficher en intégralité. Les clients de visionneuse distante peuvent autoriser leurs utilisateurs à supprimer des messages avant qu’ils ne soient téléchargés. 
  
## <a name="to-retrieve-the-headers-of-messages-stored-remotely"></a>Pour récupérer les en-têtes des messages stockés à distance
  
1. Appelez [IMAPISession::GetStatusTable](imapisession-getstatustable.md) pour accéder à la table d’état. 
    
2. Appelez [IMAPITable::Restrict](imapitable-restrict.md) pour limiter la table d’état aux seules lignes dont la colonne **PR RESOURCE \_ \_ TYPE** ([PidTagResourceType](pidtagresourcetype-canonical-property.md)) est définie sur MAPI \_ TRANSPORT \_ PROVIDER. 
    
3. Appelez [IMAPITable::SetColumns](imapitable-setcolumns.md) pour inclure les colonnes suivantes dans le tableau d’état : 
   - **PR \_ ENTRYID** ([PidTagEntryId](pidtagentryid-canonical-property.md))
   - **PR \_ RESOURCE \_ METHODS** ([PidTagResourceMethods](pidtagresourcemethods-canonical-property.md))
   - **PR \_ TYPE \_ DE RESSOURCE**, PR PROVIDER **\_ \_ DISPLAY** ([PidTagProviderDisplay](pidtagproviderdisplay-canonical-property.md))
   - **PR \_ CODE \_ D’ÉTAT** ([PidTagStatusCode](pidtagstatuscode-canonical-property.md)).
    
4. Appelez [HrQueryAllRows](hrqueryallrows.md) pour récupérer toutes les lignes de la table d’état. 
    
5. Passez l’identificateur d’entrée pour chaque ligne de la table dans un appel à [IMAPISession::OpenEntry](imapisession-openentry.md). Étant donné que cette interface est marshalée du contexte de processus dupooler MAPI au contexte de processus du client , contrairement aux interfaces généralement obtenues à partir de fournisseurs de carnet d’adresses ou de magasins de messages, les problèmes concernant le multithreading sont plus importants. 
    
6. Appelez la méthode [IUnknown::QueryInterface](https://msdn.microsoft.com/library/54d5ff80-18db-43f2-b636-f93ac053146d.aspx) de l’objet d’état, IID_IMAPIFolder comme identificateur d’interface, pour récupérer le dossier distant. Le dossier distant n’est pas une implémentation de dossier complète ; il ne prend en charge qu’un sous-ensemble de méthodes et de propriétés de dossier. L’une des méthodes requises, [IMAPIProp::GetProps,](imapiprop-getprops.md)prend en charge la récupération des propriétés suivantes :
    
    |||
    |:-----|:-----|
    |**PR \_ ACCESS** ([PidTagAccess](pidtagaccess-canonical-property.md))  <br/> |**PR_ACCESS_LEVEL** ([PidTagAccessLevel](pidtagaccesslevel-canonical-property.md))  <br/> |
    |**PR_CONTENT_COUNT** ([PidTagContentCount](pidtagcontentcount-canonical-property.md))  <br/> |**PR_ASSOC_CONTENT_COUNT** ([PidTagAssociatedContentCount](pidtagassociatedcontentcount-canonical-property.md))  <br/> |
    |**PR_FOLDER_TYPE** ([PidTagFolderType](pidtagfoldertype-canonical-property.md))  <br/> |**PR_OBJECT_TYPE** ([PidTagObjectType](pidtagobjecttype-canonical-property.md))  <br/> |
    |**PR \_ SUBFOLDERS** ([PidTagSubfolders](pidtagsubfolders-canonical-property.md))  <br/> |**PR_CREATION_TIME** ([PidTagCreationTime](pidtagcreationtime-canonical-property.md))  <br/> |
    |**PR_DISPLAY_NAME** ([PidTagDisplayName](pidtagdisplayname-canonical-property.md))  <br/> |**PR_DISPLAY_TYPE** ([PidTagDisplayType](pidtagdisplaytype-canonical-property.md))  <br/> |
    
    Les dossiers distants doivent également prendre en charge les méthodes [IMAPIProp::GetPropList,](imapiprop-getproplist.md) [IMAPIContainer::GetContentsTable](imapicontainer-getcontentstable.md)et [IMAPIFolder::SetMessageStatus.](imapifolder-setmessagestatus.md) Les tables de contenu des dossiers distants prend généralement en charge les colonnes suivantes : 
        
    |||
    |:-----|:-----|
    |**PR \_ DISPLAY \_ TO** ([PidTagDisplayTo](pidtagdisplayto-canonical-property.md))  <br/> |**PR \_ ENTRYID** <br/> |
    |**PR \_ HASATTACH** ([PidTagHasAttachments](pidtaghasattachments-canonical-property.md))  <br/> |**PR_IMPORTANCE** ([PidTagImportance](pidtagimportance-canonical-property.md))  <br/> |
    |**PR_INSTANCE_KEY** ([PidTagInstanceKey](pidtaginstancekey-canonical-property.md))  <br/> |**PR_MESSAGE_CLASS** ([PidTagMessageClass](pidtagmessageclass-canonical-property.md))  <br/> |
    |**PR \_ MESSAGE_DELIVERY_TIME** ([PidTagMessageDeliveryTime](pidtagmessagedeliverytime-canonical-property.md))  <br/> |**PR_MESSAGE_FLAGS** ([PidTagMessageFlags](pidtagmessageflags-canonical-property.md))  <br/> |
    |**PR \_ MESSAGE_DOWNLOAD_TIME** ([PidTagMessageDownloadTime](pidtagmessagedownloadtime-canonical-property.md))  <br/> |**PR_MESSAGE_SIZE** ([PidTagMessageSize](pidtagmessagesize-canonical-property.md))  <br/> |
    |**PR_MSG_STATUS** ([PidTagMessageStatus](pidtagmessagestatus-canonical-property.md))  <br/> |**PR_OBJECT_TYPE** <br/> |
    |**PR_NORMALIZED_SUBJECT** ([PidTagNormalizedSubject](pidtagnormalizedsubject-canonical-property.md))  <br/> |**PR_PRIORITY** ([PidTagPriority](pidtagpriority-canonical-property.md))  <br/> |
    |**PR_SENDER_NAME** ([PidTagSenderName](pidtagsendername-canonical-property.md))  <br/> |**PR_SENSITIVITY** ([PidTagSensitivity](pidtagsensitivity-canonical-property.md))  <br/> |
    |**PR \_ SENT_REPRESENTING_NAME** ([PidTagSentRepresentingName](pidtagsentrepresentingname-canonical-property.md))  <br/> |**PR_SUBJECT** ([PidTagSubject](pidtagsubject-canonical-property.md))  <br/> |
   
7. Appelez la méthode [IMAPIStatus::ValidateState](imapistatus-validatestate.md) du fournisseur de transport lors de la première sélection de l’une des options de transfert. L’REFRESH_XP_HEADER_CACHE ou PROCESS_XP_HEADER_CACHE de processus doit être définie, ainsi que l’indicateur SHOW_XP_SSESSION_UI pour permettre à l’interface utilisateur d’être affichée. 
    
   > [!NOTE]
   > Pour marquer un en-tête de message particulier pour le téléchargement ou la suppression, un client appelle [IMAPIFolder::SetMessageStatus](imapifolder-setmessagestatus.md) et définit l’indicateur MSGSTATUS_REMOTE_DOWNLOAD ou MSGSTATUS_REMOTE_DELETE. 
  

