---
title: IMAPIFolder IMAPIContainer
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
ms.localizationpriority: medium
api_name:
- IMAPIFolder
api_type:
- COM
ms.assetid: bc2e8d17-7687-43c2-8f01-b677703f7288
description: Dernière modification le 9 mars 2015
ms.openlocfilehash: 8da401207ba3e6341ffbe85de2b474103ff986bc
ms.sourcegitcommit: c0fae34cd3a9c75a7cffcf9ae8e417ddde07a989
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 02/12/2022
ms.locfileid: "62773578"
---
# <a name="imapifolder--imapicontainer"></a>IMAPIFolder : IMAPIContainer

  
  
**S’applique à** : Outlook 2013 | Outlook 2016 
  
Effectue des opérations sur les messages et sous-dossiers d’un dossier.
  
|||
|:-----|:-----|
|Fichier d’en-tête :  <br/> |Mapidefs.h  <br/> |
|Exposé par :  <br/> |Objets Folder  <br/> |
|Implémenté par :  <br/> |Fournisseurs de magasins de messages  <br/> |
|Appelé par :  <br/> |Applications clientes et MAPI  <br/> |
|Identificateur d’interface :  <br/> |IID_IMAPIFolder  <br/> |
|Type de pointeur :  <br/> |LPMAPIFOLDER  <br/> |
|Modèle de transaction :  <br/> |Non traduit  <br/> |
   
## <a name="vtable-order"></a>Ordre des vtables

|||
|:-----|:-----|
|[CreateMessage](imapifolder-createmessage.md) <br/> |Crée un message. |
|[CopyMessages](imapifolder-copymessages.md) <br/> |Copie ou déplace un ou plusieurs messages. |
|[DeleteMessages](imapifolder-deletemessages.md) <br/> |Supprime un ou plusieurs messages. |
|[CreateFolder](imapifolder-createfolder.md) <br/> |Crée un sous-ensemble. |
|[CopyFolder](imapifolder-copyfolder.md) <br/> |Copie ou déplace un sous-folder. |
|[DeleteFolder](imapifolder-deletefolder.md) <br/> |Supprime un sous-folder. |
|[SetReadFlags](imapifolder-setreadflags.md) <br/> |Définit ou désine l’indicateur MSGFLAG_READ dans la propriété **PR_MESSAGE_FLAGS** ([PidTagMessageFlags](pidtagmessageflags-canonical-property.md)) d’un ou plusieurs messages du dossier et gère l’envoi de rapports de lecture. |
|[GetMessageStatus](imapifolder-getmessagestatus.md) <br/> |Obtient l’état associé à un message dans un dossier particulier. |
|[SetMessageStatus](imapifolder-setmessagestatus.md) <br/> |Définit l’état associé à un message. |
|[SaveContentsSort](imapifolder-savecontentssort.md) <br/> |Définit l’ordre de tri par défaut pour la table des matières d’un dossier. |
|[EmptyFolder](imapifolder-emptyfolder.md) <br/> |Supprime tous les messages et sous-dossiers d’un dossier sans supprimer le dossier lui-même. |
   
|**Propriétés requises**|**Access**|
|:-----|:-----|
|**PR_DISPLAY_NAME** ([PidTagDisplayNamePrefix](pidtagdisplaynameprefix-canonical-property.md))  <br/> |Lecture/écriture  <br/> |
|**PR_ENTRYID** ([PidTagEntryId](pidtagentryid-canonical-property.md))  <br/> |Lecture seule  <br/> |
|**PR_FOLDER_TYPE** ([PidTagFolderType](pidtagfoldertype-canonical-property.md))  <br/> |Lecture/écriture  <br/> |
|**PR_OBJECT_TYPE** ([PidTagObjectType](pidtagobjecttype-canonical-property.md))  <br/> |Lecture seule  <br/> |
|**PR_PARENT_ENTRYID** ([PidTagParentEntryId](pidtagparententryid-canonical-property.md))  <br/> |Lecture seule  <br/> |
|**PR_RECORD_KEY** ([PidTagRecordKey](pidtagrecordkey-canonical-property.md))  <br/> |Lecture seule  <br/> |
|**PR_STORE_ENTRYID** ([PidTagStoreEntryId](pidtagstoreentryid-canonical-property.md))  <br/> |Lecture seule  <br/> |
|**PR_STORE_RECORD_KEY** ([PidTagStoreRecordKey](pidtagstorerecordkey-canonical-property.md))  <br/> |Lecture seule  <br/> |
   
## <a name="see-also"></a>Voir aussi



[Interfaces MAPI](mapi-interfaces.md)

