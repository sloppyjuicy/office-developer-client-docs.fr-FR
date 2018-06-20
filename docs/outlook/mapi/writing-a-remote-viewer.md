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
ms.openlocfilehash: 554f98f7bda8c6616ce06b86142213c18bff1f69
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19787488"
---
# <a name="writing-a-remote-viewer"></a>Écriture d’une visionneuse à distance

**S’applique à**: Outlook 
  
Une visionneuse à distance est une fenêtre dans une application cliente qui fournit un accès contrôlé aux messages stockés sur un autre ordinateur. Ce contrôle d’accès peut fonctionner sur une liaison lente. Au lieu d’extraire une sélection de messages disponibles chaque fois qu’un utilisateur ouvre un dossier, la visionneuse à distance affiche uniquement les en-têtes. L’utilisateur sélectionne ensuite les en-têtes à partir de laquelle des messages pour afficher entièrement. Clients distants visionneuse permettent à leurs utilisateurs de supprimer des messages avant de les télécharger jamais. 
  
## <a name="to-retrieve-the-headers-of-messages-stored-remotely"></a>Pour récupérer les en-têtes des messages stockés à distance
  
1. Appelez [IMAPISession::GetStatusTable](imapisession-getstatustable.md) pour accéder à la table d’état. 
    
2. Appelez [IMAPITable](imapitable-restrict.md) pour limiter la table d’état uniquement aux lignes qui ont leur **PR\_ressources\_TYPE** ([PidTagResourceType](pidtagresourcetype-canonical-property.md)) colonne valeur MAPI\_TRANSPORT\_fournisseur. 
    
3. Appelez [IMAPITable::SetColumns](imapitable-setcolumns.md) pour inclure les colonnes suivantes dans la table d’état : 
   - **PR\_ENTRYID** ([PidTagEntryId](pidtagentryid-canonical-property.md))
   - **PR\_ressources\_méthodes** ([PidTagResourceMethods](pidtagresourcemethods-canonical-property.md))
   - **PR\_ressources\_TYPE**, **PR\_fournisseur\_affichage** ([PidTagProviderDisplay](pidtagproviderdisplay-canonical-property.md))
   - **PR\_état\_CODE** ([PidTagStatusCode](pidtagstatuscode-canonical-property.md)).
    
4. Appelez [HrQueryAllRows](hrqueryallrows.md) pour récupérer toutes les lignes dans la table d’état. 
    
5. Passez l’identificateur d’entrée pour chaque ligne du tableau dans un appel à [IMAPISession::OpenEntry](imapisession-openentry.md). Parce que cette interface est assemblée à partir du contexte de processus du spouleur MAPI au contexte de processus du client, contrairement aux interfaces généralement obtenus à partir du carnet d’adresses ou message stocker les fournisseurs — problèmes concernant le multithreading sont de plus d’importance. 
    
6. Appelez la méthode [IUnknown::QueryInterface](http://msdn.microsoft.com/library/54d5ff80-18db-43f2-b636-f93ac053146d.aspx) de l’objet de l’état, en passant IID_IMAPIFolder comme l’identificateur d’interface permet de récupérer le dossier à distance. Le dossier distant n’est pas une implémentation de dossier complet ; Il prend en charge uniquement un sous-ensemble des propriétés et méthodes de dossier. Une des méthodes requis, [IMAPIProp::GetProps](imapiprop-getprops.md), prend en charge l’extraction des propriétés suivantes :
    
    |||
    |:-----|:-----|
    |**PR\_ACCESS** ([PidTagAccess](pidtagaccess-canonical-property.md))  <br/> |**PR_ACCESS_LEVEL** ([PidTagAccessLevel](pidtagaccesslevel-canonical-property.md))  <br/> |
    |**PR_CONTENT_COUNT** ([PidTagContentCount](pidtagcontentcount-canonical-property.md))  <br/> |**PR_ASSOC_CONTENT_COUNT** ([PidTagAssociatedContentCount](pidtagassociatedcontentcount-canonical-property.md))  <br/> |
    |**PR_FOLDER_TYPE** ([PidTagFolderType](pidtagfoldertype-canonical-property.md))  <br/> |**PR_OBJECT_TYPE** ([PidTagObjectType](pidtagobjecttype-canonical-property.md))  <br/> |
    |**PR\_sous-dossiers** ([PidTagSubfolders](pidtagsubfolders-canonical-property.md))  <br/> |**PR_CREATION_TIME** ([PidTagCreationTime](pidtagcreationtime-canonical-property.md))  <br/> |
    |**PR_DISPLAY_NAME** ([PidTagDisplayName](pidtagdisplayname-canonical-property.md))  <br/> |**PR_DISPLAY_TYPE** ([PidTagDisplayType](pidtagdisplaytype-canonical-property.md))  <br/> |
    
    Dossiers distants doivent également en charge les méthodes [IMAPIProp::GetPropList](imapiprop-getproplist.md), [IMAPIContainer::GetContentsTable](imapicontainer-getcontentstable.md)et [IMAPIFolder::SetMessageStatus](imapifolder-setmessagestatus.md) . Tables de contenu de dossier distant prennent généralement en charge les colonnes suivantes : 
        
    |||
    |:-----|:-----|
    |**PR\_affichage\_à** ([PidTagDisplayTo](pidtagdisplayto-canonical-property.md))  <br/> |**PR\_ENTRYID** <br/> |
    |**PR\_HASATTACH** ([PidTagHasAttachments](pidtaghasattachments-canonical-property.md))  <br/> |**PR_IMPORTANCE** ([PidTagImportance](pidtagimportance-canonical-property.md))  <br/> |
    |**PR_INSTANCE_KEY** ([PidTagInstanceKey](pidtaginstancekey-canonical-property.md))  <br/> |**PR_MESSAGE_CLASS** ([PidTagMessageClass](pidtagmessageclass-canonical-property.md))  <br/> |
    |**PR\_MESSAGE_DELIVERY_TIME** ([PidTagMessageDeliveryTime](pidtagmessagedeliverytime-canonical-property.md))  <br/> |**PR_MESSAGE_FLAGS** ([PidTagMessageFlags](pidtagmessageflags-canonical-property.md))  <br/> |
    |**PR\_MESSAGE_DOWNLOAD_TIME** ([PidTagMessageDownloadTime](pidtagmessagedownloadtime-canonical-property.md))  <br/> |**PR_MESSAGE_SIZE** ([PidTagMessageSize](pidtagmessagesize-canonical-property.md))  <br/> |
    |**PR_MSG_STATUS** ([PidTagMessageStatus](pidtagmessagestatus-canonical-property.md))  <br/> |**PR_OBJECT_TYPE** <br/> |
    |**PR_NORMALIZED_SUBJECT** ([PidTagNormalizedSubject](pidtagnormalizedsubject-canonical-property.md))  <br/> |**PR_PRIORITY** ([PidTagPriority](pidtagpriority-canonical-property.md))  <br/> |
    |**PR_SENDER_NAME** ([PidTagSenderName](pidtagsendername-canonical-property.md))  <br/> |**PR_SENSITIVITY** ([PidTagSensitivity](pidtagsensitivity-canonical-property.md))  <br/> |
    |**PR\_SENT_REPRESENTING_NAME** ([PidTagSentRepresentingName](pidtagsentrepresentingname-canonical-property.md))  <br/> |**PR_SUBJECT** ([PidTagSubject](pidtagsubject-canonical-property.md))  <br/> |
   
7. Appel [IMAPIStatus::ValidateState](imapistatus-validatestate.md) méthode la première fois du fournisseur de transport qu’une des options de transfert est sélectionnée. Indicateur de processus PROCESS_XP_HEADER_CACHE ou REFRESH_XP_HEADER_CACHE doit être défini ainsi que l’indicateur SHOW_XP_SSESSION_UI pour autoriser l’interface utilisateur à afficher. 
    
   > [!NOTE]
   > Pour marquer un en-tête de message particulier pour le téléchargement ou la suppression, un client appelle [IMAPIFolder::SetMessageStatus](imapifolder-setmessagestatus.md) et définit l’indicateur MSGSTATUS_REMOTE_DELETE ou MSGSTATUS_REMOTE_DOWNLOAD. 
  

