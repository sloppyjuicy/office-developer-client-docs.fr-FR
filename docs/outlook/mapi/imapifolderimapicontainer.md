---
title: IMAPIFolder IMAPIContainer
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- IMAPIFolder
api_type:
- COM
ms.assetid: bc2e8d17-7687-43c2-8f01-b677703f7288
description: Dernière modification le 09 mars 2015
ms.openlocfilehash: 1886987515f3cafe38418960baa4b6fd89e3b6f2
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/23/2018
ms.locfileid: "22590798"
---
# <a name="imapifolder--imapicontainer"></a>IMAPIFolder : IMAPIContainer

  
  
**S’applique à**: Outlook 2013 | Outlook 2016 
  
Effectue des opérations sur les messages et les sous-dossiers dans un dossier.
  
|||
|:-----|:-----|
|Fichier d’en-tête :  <br/> |Mapidefs.h  <br/> |
|Exposés par :  <br/> |Objets de dossier  <br/> |
|Implémentée par :  <br/> |Fournisseurs de banque de messages  <br/> |
|Appelée par :  <br/> |Les applications clientes et MAPI  <br/> |
|Identificateur de l’interface :  <br/> |IID_IMAPIFolder  <br/> |
|Type de pointeur :  <br/> |LPMAPIFOLDER  <br/> |
|Modèle de transaction :  <br/> |Nontransacted  <br/> |
   
## <a name="vtable-order"></a>Ordre vtable

|||
|:-----|:-----|
|[CreateMessage](imapifolder-createmessage.md) <br/> |Crée un nouveau message.  <br/> |
|[CopyMessages](imapifolder-copymessages.md) <br/> |Copie ou déplace un ou plusieurs messages.  <br/> |
|[DeleteMessages](imapifolder-deletemessages.md) <br/> |Supprime un ou plusieurs messages.  <br/> |
|[CreateFolder](imapifolder-createfolder.md) <br/> |Crée un sous-dossier.  <br/> |
|[CopyFolder](imapifolder-copyfolder.md) <br/> |Copie ou déplace un sous-dossier.  <br/> |
|[DeleteFolder](imapifolder-deletefolder.md) <br/> |Supprime un sous-dossier.  <br/> |
|[SetReadFlags](imapifolder-setreadflags.md) <br/> |Définit ou supprime l’indicateur MSGFLAG_READ dans la propriété **PR_MESSAGE_FLAGS** ([PidTagMessageFlags](pidtagmessageflags-canonical-property.md)) d’un ou plusieurs des messages du dossier et gère l’envoi de rapports de lecture.  <br/> |
|[GetMessageStatus](imapifolder-getmessagestatus.md) <br/> |Obtient l’état d’un message dans un dossier spécifique.  <br/> |
|[SetMessageStatus](imapifolder-setmessagestatus.md) <br/> |Définit l’état d’un message.  <br/> |
|[SaveContentsSort](imapifolder-savecontentssort.md) <br/> |Définit l’ordre de tri par défaut pour la table des matières d’un dossier.  <br/> |
|[EmptyFolder](imapifolder-emptyfolder.md) <br/> |Supprime tous les messages et les sous-dossiers d’un dossier sans supprimer le dossier proprement dit.  <br/> |
   
|**Propriétés requises**|**Access**|
|:-----|:-----|
|**PR_DISPLAY_NAME** ([PidTagDisplayNamePrefix](pidtagdisplaynameprefix-canonical-property.md))  <br/> |En lecture-écriture.  <br/> |
|**PR_ENTRYID** ([PidTagEntryId](pidtagentryid-canonical-property.md))  <br/> |Lecture seule  <br/> |
|**PR_FOLDER_TYPE** ([PidTagFolderType](pidtagfoldertype-canonical-property.md))  <br/> |En lecture-écriture.  <br/> |
|**PR_OBJECT_TYPE** ([PidTagObjectType](pidtagobjecttype-canonical-property.md))  <br/> |Lecture seule  <br/> |
|**PR_PARENT_ENTRYID** ([PidTagParentEntryId](pidtagparententryid-canonical-property.md))  <br/> |Lecture seule  <br/> |
|**PR_RECORD_KEY** ([PidTagRecordKey](pidtagrecordkey-canonical-property.md))  <br/> |Lecture seule  <br/> |
|**PR_STORE_ENTRYID** ([PidTagStoreEntryId](pidtagstoreentryid-canonical-property.md))  <br/> |Lecture seule  <br/> |
|**PR_STORE_RECORD_KEY** ([PidTagStoreRecordKey](pidtagstorerecordkey-canonical-property.md))  <br/> |Lecture seule  <br/> |
   
## <a name="see-also"></a>Voir aussi



[Interfaces MAPI](mapi-interfaces.md)

