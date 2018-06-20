---
title: Tables des matières
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: 7b8efb4e-b5be-41b8-81bb-9aa1da421433
description: 'Derni�re modification�: lundi 9 mars 2015'
ms.openlocfilehash: 0dd79d9630837b5ec8a709d386ccc0db987dfb5b
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19783058"
---
# <a name="contents-tables"></a>Tables des matières

  
  
**S’applique à**: Outlook 
  
Une table des matières contient des informations sur les objets dans un conteneur MAPI. Fournisseurs de carnet d’adresses implémentent des tables des matières pour chacun de leurs conteneurs et banque de messages et des fournisseurs de transport à distance implémentent des tables de contenu pour leurs dossiers. La table des matières d’un conteneur de carnet d’adresses répertorie les informations sur ses objets messages utilisateur et de distribution liste, tandis que la table des matières d’un dossier répertorie les informations sur ses messages. Tables de contenu sont utilisées par les applications clientes. 
  
Il existe deux types de tables de contenu de dossier :
  
- Tables des matières standard contiennent des messages standards — les messages qui peuvent être transmises et rendus visible à un utilisateur. 
    
- Tables de contenu associé contiennent des informations masquées, non transmissible créées par un client pour un usage spécifique, par exemple pour stocker une autre représentation d’un message standard. Informations associées sont créées en transmettant l’indicateur MAPI_ASSOCIATED à l’appel de [IMAPIFolder::CreateMessage](imapifolder-createmessage.md) . 
    
Le contenu de tables de la plupart des conteneurs de carnet d’adresses et le nombre de dossiers ne prennent pas charge classés tri. 
  
Une table des matières est accessible en appelant :
  
- [IMAPIContainer::GetContentsTable](imapicontainer-getcontentstable.md).
    
    - Ou -
    
- [IMAPIProp::OpenProperty](imapiprop-openproperty.md) avec **PR_CONTAINER_CONTENTS** ([PidTagContainerContents](pidtagcontainercontents-canonical-property.md)) ou **PR_FOLDER_ASSOCIATED_CONTENTS** ([PidTagFolderAssociatedContents](pidtagfolderassociatedcontents-canonical-property.md)) (uniquement pour les dossiers) spécifié en tant que propriété tag et IID _IMAPITable en tant que l’identificateur d’interface.
    
Banque de messages et adresses fournisseurs de carnet de doivent prendre en charge les deux méthodes pour récupérer les propriétés du tableau. N’est pas acceptable pour les fournisseurs prendre en charge qu’un moyen pour accéder à ces tables, car les clients s’attendent à avoir le choix. 
  
 **GetContentsTable** accepte comme entrée plusieurs indicateurs qui spécifient les préférences. Lorsque la valeur, l’indicateur MAPI_ASSOCIATED récupère un tableau de contenu associée. Étant donné que certains dossiers ne prennent pas en charge contenu associé, et il n’existe aucun moyen pour les clients déterminer à l’avance, **GetContentsTable** renvoie parfois l’erreur MAPI_E_NO_SUPPORT lors d’une demande d’un tableau de contenu associée. 
  
L’indicateur MAPI_DEFERRED_ERRORS indique à l’implémentation de la table qui les erreurs rencontrées lors de l’appel ne doivent pas être signalé jusqu'à une date ultérieure. 
  
L’appel vers **IMAPIProp::OpenProperty** implique l’accès à une table des matières en ouvrant sa propriété correspondante, **PR_CONTAINER_CONTENTS** **PR_FOLDER_ASSOCIATED_ tables de contenu téléchargeable adresse et tables de contenu de dossier standard CONTENU** pour associé tables des matières. Bien que ni ou ces propriétés peuvent être récupérées à un dossier ou du conteneur [IMAPIProp::GetProps](imapiprop-getprops.md) , ils sont inclus dans le tableau de balise de propriété qui est retourné par la méthode [IMAPIProp::GetPropList](imapiprop-getproplist.md) . 
  
 **PR_CONTAINER_CONTENTS** peut également servir à inclure ou exclure un tableau contenu dans une opération de copie. Si un client spécifie **PR_CONTAINER_CONTENTS** dans le paramètre *lpExcludeProps* pour **IMAPIProp::CopyTo** dans une opération de copie, le nouveau dossier ou le conteneur ne prendra pas en charge la table des matières du dossier d’origine ou du conteneur. 
  
Livre adresse conteneur et le dossier tables de contenu ont une longue liste de colonnes requises : colonnes clients pourront être disponibles une fois extrait le tableau **GetContentsTable** ou **OpenProperty**. Fournisseurs peuvent ajouter à cet ensemble requis si nécessaire et les clients, par le biais de la méthode **SetColumns** , peuvent également demander des modifications. 
  
Les colonnes requises pour chacun des types de tables de contenu sont les suivants :
  
|**Colonne requise**|**Type de table des matières**|
|:-----|:-----|
|**TYPEADR_PR** ([PidTagAddressType](pidtagaddresstype-canonical-property.md))  <br/> |Tables de conteneur de carnet d’adresses  <br/> |
|**PR_DISPLAY_NAME** ([PidTagDisplayName](pidtagdisplayname-canonical-property.md))  <br/> |Tables de conteneur de carnet d’adresses  <br/> |
|**PR_DISPLAY_CC** ([PidTagDisplayCc](pidtagdisplaycc-canonical-property.md))  <br/> |Tables de dossier de banque de messages  <br/> |
|**PR_DISPLAY_TO** ([PidTagDisplayTo](pidtagdisplayto-canonical-property.md))  <br/> |Toutes les tables de contenu de dossier  <br/> |
|**PR_DISPLAY_TYPE** ([PidTagDisplayType](pidtagdisplaytype-canonical-property.md))  <br/> |Tables de conteneur de carnet d’adresses  <br/> |
|**PR_ENTRYID** ([PidTagEntryId](pidtagentryid-canonical-property.md))  <br/> |Toutes les tables de contenu  <br/> |
|**PR_HASATTACH** ([PidTagHasAttachments](pidtaghasattachments-canonical-property.md))  <br/> |Toutes les tables de contenu de dossier  <br/> |
|**PR_INSTANCE_KEY** ([PidTagInstanceKey](pidtaginstancekey-canonical-property.md))  <br/> |Toutes les tables de contenu  <br/> |
|**PR_LAST_MODIFICATION_TIME** ([PidTagLastModificationTime](pidtaglastmodificationtime-canonical-property.md))  <br/> |Tables de dossier de banque de messages  <br/> |
|**PR_MAPPING_SIGNATURE** ([PidTagMappingSignature](pidtagmappingsignature-canonical-property.md))  <br/> |Tables de dossier de banque de messages  <br/> |
|**PR_MESSAGE_CLASS** ([PidTagMessageClass](pidtagmessageclass-canonical-property.md))  <br/> |Toutes les tables de contenu de dossier  <br/> |
|**PR_MESSAGE_DOWNLOAD_TIME** ([PidTagMessageDownloadTime](pidtagmessagedownloadtime-canonical-property.md))  <br/> |Tables de dossier de transport à distance  <br/> |
|**PR_MESSAGE_FLAGS** ([PidTagMessageFlags](pidtagmessageflags-canonical-property.md))  <br/> |Toutes les tables de contenu de dossier  <br/> |
|**PR_MESSAGE_SIZE** ([PidTagMessageSize](pidtagmessagesize-canonical-property.md))  <br/> |Toutes les tables de contenu de dossier  <br/> |
|**PR_MSG_STATUS** ([PidTagMessageStatus](pidtagmessagestatus-canonical-property.md))  <br/> |Toutes les tables de contenu de dossier  <br/> |
|**PR_OBJECT_TYPE** ([PidTagObjectType](pidtagobjecttype-canonical-property.md))  <br/> |Toutes les tables de contenu  <br/> |
|**PR_PARENT_ENTRYID** ([PidTagParentEntryId](pidtagparententryid-canonical-property.md))  <br/> |Tables de dossier de banque de messages  <br/> |
|**PR_RECORD_KEY** ([PidTagRecordKey](pidtagrecordkey-canonical-property.md))  <br/> |Tables de dossier de banque de messages et de conteneur de carnets d’adresses  <br/> |
|**PR_SENT_REPRESENTING_NAME** ([PidTagSentRepresentingName](pidtagsentrepresentingname-canonical-property.md))  <br/> |Tables de dossier de transport à distance  <br/> |
|**PR_STORE_ENTRYID** ([PidTagStoreEntryId](pidtagstoreentryid-canonical-property.md))  <br/> |Tables de dossier de banque de messages  <br/> |
|**PR_STORE_RECORD_KEY** ([PidTagStoreRecordKey](pidtagstorerecordkey-canonical-property.md))  <br/> |Tables de dossier de banque de messages  <br/> |
   
L’identificateur d’entrée disponible avec chaque ligne peut être un court ou à long terme identificateur d’entrée, en fonction de l’implémentation de la table. Identificateurs d’entrée à court terme sont généralement utilisés dans les situations où les performances sont un problème. Un type d’identificateur d’entrée peut être utilisé pour accéder à l’objet correspondant. 
  
Tables des matières ont également un ensemble de colonnes qui sont facultatifs, mais généralement inclus par les fournisseurs de service dans leurs implémentations. Ces colonnes facultatives sont les suivants :
  
|**Colonne facultative**|**Type de table des matières**|
|:-----|:-----|
|**PR_CLIENT_SUBMIT_TIME** ([PidTagClientSubmitTime](pidtagclientsubmittime-canonical-property.md))  <br/> |Tables de dossier de banque de messages  <br/> |
|**PR_CONTENT_COUNT** ([PidTagContentCount](pidtagcontentcount-canonical-property.md))  <br/> |Tables de contenu de dossier standard  <br/> |
|**PR_CONTENT_UNREAD** ([PidTagContentUnreadCount](pidtagcontentunreadcount-canonical-property.md))  <br/> |Tables de contenu de dossier standard  <br/> |
|**PR_CONVERSATION_INDEX** ([PidTagConversationIndex](pidtagconversationindex-canonical-property.md))  <br/> |Tables de dossier de banque de messages  <br/> |
|**ADRESSE_EMAIL_PR** ([PidTagEmailAddress](pidtagemailaddress-canonical-property.md))  <br/> |Tables de conteneur de carnet d’adresses  <br/> |
|**PR_IMPORTANCE** ([PidTagImportance](pidtagimportance-canonical-property.md))  <br/> |Toutes les tables de contenu de dossier  <br/> |
|**PR_MESSAGE_DELIVERY_TIME** ([PidTagMessageDeliveryTime](pidtagmessagedeliverytime-canonical-property.md))  <br/> |Toutes les tables de contenu de dossier  <br/> |
|**PR_NORMALIZED_SUBJECT** ([PidTagNormalizedSubject](pidtagnormalizedsubject-canonical-property.md))  <br/> |Toutes les tables de contenu de dossier  <br/> |
|**PR_PRIORITY** ([PidTagPriority](pidtagpriority-canonical-property.md))  <br/> |Toutes les tables de contenu de dossier  <br/> |
|**Clé PR_SEARCH_KEY** ([PidTagSearchKey](pidtagsearchkey-canonical-property.md))  <br/> |Tables de conteneur de carnet d’adresses  <br/> |
|**PR_SEND_RICH_INFO** ([PidTagSendRichInfo](pidtagsendrichinfo-canonical-property.md))  <br/> |Tables de conteneur de carnet d’adresses  <br/> |
|**PR_SENDER_NAME** ([PidTagSenderName](pidtagsendername-canonical-property.md))  <br/> |Toutes les tables de contenu de dossier  <br/> |
|**PR_SENSITIVITY** ([PidTagSensitivity](pidtagsensitivity-canonical-property.md))  <br/> |Toutes les tables de contenu de dossier  <br/> |
|**PR_SUBJECT** ([PidTagSubject](pidtagsubject-canonical-property.md))  <br/> |Toutes les tables de contenu de dossier  <br/> |
|**PR_TRANSMITABLE_DISPLAY_NAME** ([PidTagTransmittableDisplayName](pidtagtransmittabledisplayname-canonical-property.md))  <br/> |Tables de conteneur de carnet d’adresses  <br/> |
   
Fournisseurs de magasins de message doivent également inclure **PR_PARENT_DISPLAY** ([PidTagParentDisplay](pidtagparentdisplay-canonical-property.md)) pour les tables de contenu des dossiers de résultats de recherche uniquement.
  
Propriétés nommées peuvent être ajoutées à l’ensemble de colonnes d’une table de contenu du dossier uniquement si tous les messages dans le dossier ont la même mappage signature, autrement dit, le même mappage de noms de propriété pour les identificateurs de propriété. Tables de contenu de dossier doivent prendre en charge des propriétés spécifiques à la colonne valeur, ajout classe de message si elles prennent en charge la création de messages arbitraires dans le dossier.
  
Les clients peuvent enregistrer l’ordre de tri par défaut pour un tableau contenu de dossier en appelant la méthode [IMAPIFolder::SaveContentsSort](imapifolder-savecontentssort.md) . Si l’indicateur RECURSIVE_SORT est spécifié lors de l’appel, l’ordre de tri peut être établie à appliquer à tous les sous-dossiers du dossier. 
  
## <a name="see-also"></a>Voir aussi



[Tables MAPI](mapi-tables.md)

