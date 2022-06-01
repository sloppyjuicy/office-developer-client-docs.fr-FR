---
title: IMAPIFolder IMAPIContainer
description: IMAPIFolderIMAPIContainer effectue des opérations sur les messages et les sous-dossiers d’un dossier. Cet article décrit les propriétés et les membres associés.
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
ms.openlocfilehash: 79b640fbca43ef0454d63c9984d6f49d04e5c0f9
ms.sourcegitcommit: f872848fbeb5b2353179ad4bf4eab23f61f87666
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/01/2022
ms.locfileid: "65816163"
---
# <a name="imapifolder--imapicontainer"></a>IMAPIFolder : IMAPIContainer

  
  
**S’applique à** : Outlook 2013 | Outlook 2016 
  
Effectue des opérations sur les messages et les sous-dossiers d’un dossier.
  
|Propriété |Valeur |
|:-----|:-----|
|Fichier d’en-tête :  <br/> |Mapidefs.h  <br/> |
|Exposé par :  <br/> |Objets de dossier  <br/> |
|Implémenté par :  <br/> |Fournisseurs de magasins de messages  <br/> |
|Appelé par :  <br/> |Applications clientes et MAPI  <br/> |
|Identificateur d’interface :  <br/> |IID_IMAPIFolder  <br/> |
|Type de pointeur :  <br/> |LPMAPIFOLDER  <br/> |
|Modèle de transaction :  <br/> |Non transactionnel  <br/> |
   
## <a name="vtable-order"></a>Ordre des tables virtuelles

|Member |Description |
|:-----|:-----|
|[CreateMessage](imapifolder-createmessage.md) <br/> |Crée un message. |
|[CopyMessages](imapifolder-copymessages.md) <br/> |Copie ou déplace un ou plusieurs messages. |
|[DeleteMessages](imapifolder-deletemessages.md) <br/> |Supprime un ou plusieurs messages. |
|[CreateFolder](imapifolder-createfolder.md) <br/> |Crée un sous-dossier. |
|[CopyFolder](imapifolder-copyfolder.md) <br/> |Copie ou déplace un sous-dossier. |
|[DeleteFolder](imapifolder-deletefolder.md) <br/> |Supprime un sous-dossier. |
|[SetReadFlags](imapifolder-setreadflags.md) <br/> |Définit ou efface l’indicateur MSGFLAG_READ dans la propriété **PR_MESSAGE_FLAGS** ([PidTagMessageFlags](pidtagmessageflags-canonical-property.md)) d’un ou plusieurs messages du dossier, et gère l’envoi de rapports de lecture. |
|[GetMessageStatus](imapifolder-getmessagestatus.md) <br/> |Obtient l’état associé à un message dans un dossier particulier. |
|[SetMessageStatus](imapifolder-setmessagestatus.md) <br/> |Définit l’état associé à un message. |
|[SaveContentsSort](imapifolder-savecontentssort.md) <br/> |Définit l’ordre de tri par défaut pour la table du contenu d’un dossier. |
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

