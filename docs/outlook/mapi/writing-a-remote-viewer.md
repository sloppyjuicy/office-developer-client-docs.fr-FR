---
title: Écriture d’une visionneuse à distance
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: f4d7d42f-688a-4199-b972-dd42528c0cdf
description: 'Derni�re modification�: lundi 9 mars 2015'
ms.openlocfilehash: 1d7fea7f92a315b9671d17c82a82d5d7d180f4bb
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32325661"
---
# <a name="writing-a-remote-viewer"></a>Écriture d’une visionneuse à distance

**S’applique à** : Outlook 2013 | Outlook 2016 
  
Une visionneuse à distance est une fenêtre dans une application cliente qui fournit un accès contrôlé aux messages stockés sur un autre ordinateur. Cet accès contrôlé peut fonctionner sur un lien de communication lent. Au lieu de récupérer une sélection complète des messages disponibles chaque fois qu'un utilisateur ouvre un dossier, la visionneuse à distance affiche uniquement les en-têtes. L'utilisateur sélectionne ensuite dans les en-têtes les messages à afficher de façon complète. Les clients de la visionneuse disTante peuvent permettre à leurs utilisateurs de supprimer des messages avant qu'ils ne soient jamais téléchargés. 
  
## <a name="to-retrieve-the-headers-of-messages-stored-remotely"></a>Pour récupérer les en-têtes des messages stockés à distance
  
1. Appelez [IMAPISession:: GetStatusTable](imapisession-getstatustable.md) pour accéder à la table d'État. 
    
2. Appeler [IMAPITable:: Restrict](imapitable-restrict.md) pour limiter la table d'État aux seules lignes dont la colonne de **type de ressource\_\_PR** ([PidTagResourceType](pidtagresourcetype-canonical-property.md)) est\_définie\_sur fournisseur de transport MAPI. 
    
3. Appelez la commande [IMAPITable:: SetColumns](imapitable-setcolumns.md) pour inclure les colonnes suivantes dans la table d'État: 
   - **ID\_** de la propriété PR ([PidTagEntryId](pidtagentryid-canonical-property.md))
   - **Méthodes\_de\_ressource PR** ([PidTagResourceMethods](pidtagresourcemethods-canonical-property.md))
   - **TYPE\_de\_ressource PR**, **\_PR\_Provider Display** ([PidTagProviderDisplay](pidtagproviderdisplay-canonical-property.md))
   - **PR\_status\_code** ([PidTagStatusCode](pidtagstatuscode-canonical-property.md)).
    
4. Appelez [HrQueryAllRows](hrqueryallrows.md) pour récupérer toutes les lignes dans la table d'État. 
    
5. TransMettez l'identificateur d'entrée pour chaque ligne de la table dans un appel à [IMAPISession:: OpenEntry](imapisession-openentry.md). Étant donné que cette interface est marshalée depuis le contexte du processus du spouleur MAPI vers le contexte du processus du client, contrairement aux interfaces généralement obtenues à partir de fournisseurs de carnet d'adresses ou de banque de messages, les problèmes liés au multithreading sont plus importants. 
    
6. Appelez la méthode [IUnknown:: QueryInterface](https://msdn.microsoft.com/library/54d5ff80-18db-43f2-b636-f93ac053146d.aspx) de l'objet d'État, en transmettant IID_IMAPIFolder comme identificateur d'interface, pour récupérer le dossier distant. Le dossier distant n'est pas une implémentation de dossier complète; Il prend en charge uniquement un sous-ensemble de méthodes et de propriétés de dossier. L'une des méthodes requises, [IMAPIProp:: GetProps](imapiprop-getprops.md), prend en charge la récupération des propriétés suivantes:
    
    |||
    |:-----|:-----|
    |**Accès\_PR** ([PidTagAccess](pidtagaccess-canonical-property.md))  <br/> |**PR_ACCESS_LEVEL** ([PidTagAccessLevel](pidtagaccesslevel-canonical-property.md))  <br/> |
    |**PR_CONTENT_COUNT** ([PidTagContentCount](pidtagcontentcount-canonical-property.md))  <br/> |**PR_ASSOC_CONTENT_COUNT** ([PidTagAssociatedContentCount](pidtagassociatedcontentcount-canonical-property.md))  <br/> |
    |**PR_FOLDER_TYPE** ([PidTagFolderType](pidtagfoldertype-canonical-property.md))  <br/> |**PR_OBJECT_TYPE** ([PidTagObjectType](pidtagobjecttype-canonical-property.md))  <br/> |
    |**SOUS\_-dossiers PR** ([PidTagSubfolders](pidtagsubfolders-canonical-property.md))  <br/> |**PR_CREATION_TIME** ([PidTagCreationTime](pidtagcreationtime-canonical-property.md))  <br/> |
    |**PR_DISPLAY_NAME** ([PidTagDisplayName](pidtagdisplayname-canonical-property.md))  <br/> |**PR_DISPLAY_TYPE** ([PidTagDisplayType](pidtagdisplaytype-canonical-property.md))  <br/> |
    
    Les dossiers disTants doivent également prendre en charge les méthodes [IMAPIProp:: GetPropList](imapiprop-getproplist.md), [IMAPIContainer:: GetContentsTable](imapicontainer-getcontentstable.md)et [IMAPIFolder:: SetMessageStatus](imapifolder-setmessagestatus.md) . Les tables de contenu de dossier distant prennent généralement en charge les colonnes suivantes: 
        
    |||
    |:-----|:-----|
    |**PR\_Display\_to** ([PidTagDisplayTo](pidtagdisplayto-canonical-property.md))  <br/> |**\_ID de la propriété** <br/> |
    |**PR\_HASATTACH** ([PidTagHasAttachments](pidtaghasattachments-canonical-property.md))  <br/> |**PR_IMPORTANCE** ([PidTagImportance](pidtagimportance-canonical-property.md))  <br/> |
    |**PR_INSTANCE_KEY** ([PidTagInstanceKey](pidtaginstancekey-canonical-property.md))  <br/> |**PR_MESSAGE_CLASS** ([PidTagMessageClass](pidtagmessageclass-canonical-property.md))  <br/> |
    |**PR\_MESSAGE_DELIVERY_TIME** ([PidTagMessageDeliveryTime](pidtagmessagedeliverytime-canonical-property.md))  <br/> |**PR_MESSAGE_FLAGS** ([PidTagMessageFlags](pidtagmessageflags-canonical-property.md))  <br/> |
    |**PR\_MESSAGE_DOWNLOAD_TIME** ([PidTagMessageDownloadTime](pidtagmessagedownloadtime-canonical-property.md))  <br/> |**PR_MESSAGE_SIZE** ([PidTagMessageSize](pidtagmessagesize-canonical-property.md))  <br/> |
    |**PR_MSG_STATUS** ([PidTagMessageStatus](pidtagmessagestatus-canonical-property.md))  <br/> |**PR_OBJECT_TYPE** <br/> |
    |**PR_NORMALIZED_SUBJECT** ([PidTagNormalizedSubject](pidtagnormalizedsubject-canonical-property.md))  <br/> |**PR_PRIORITY** ([PidTagPriority](pidtagpriority-canonical-property.md))  <br/> |
    |**PR_SENDER_NAME** ([PidTagSenderName](pidtagsendername-canonical-property.md))  <br/> |**PR_SENSITIVITY** ([PidTagSensitivity](pidtagsensitivity-canonical-property.md))  <br/> |
    |**PR\_SENT_REPRESENTING_NAME** ([PidTagSentRepresentingName](pidtagsentrepresentingname-canonical-property.md))  <br/> |**PR_SUBJECT** ([PidTagSubject](pidtagsubject-canonical-property.md))  <br/> |
   
7. Appelez la méthode [IMAPIStatus:: ValidateState](imapistatus-validatestate.md) du fournisseur de transport la première fois que l'une des options de transfert est prélevée. L'indicateur de processus REFRESH_XP_HEADER_CACHE ou PROCESS_XP_HEADER_CACHE doit être défini ainsi que l'indicateur SHOW_XP_SSESSION_UI pour permettre l'affichage de l'interface utilisateur. 
    
   > [!NOTE]
   > Pour marquer un en-tête de message particulier en vue d'un téléchargement ou d'une suppression, un client appelle [IMAPIFolder:: SetMessageStatus](imapifolder-setmessagestatus.md) et définit l'indicateur MSGSTATUS_REMOTE_DOWNLOAD ou MSGSTATUS_REMOTE_DELETE. 
  

