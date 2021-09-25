---
title: Tables des matières
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.localizationpriority: medium
api_type:
- COM
ms.assetid: 7b8efb4e-b5be-41b8-81bb-9aa1da421433
description: Dernière modification le 9 mars 2015
ms.openlocfilehash: 8114190a263ffbcc72344cd3a051a427238ecb0f
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/24/2021
ms.locfileid: "59556825"
---
# <a name="contents-tables"></a>Tables des matières

  
  
**S’applique à** : Outlook 2013 | Outlook 2016 
  
Une table des matières contient des informations sur les objets dans un conteneur MAPI. Les fournisseurs de carnets d’adresses implémentent des tables de contenu pour chacun de leurs conteneurs, et les fournisseurs de magasins de messages et de transport distants implémentent des tables de contenu pour leurs dossiers. La table des matières d’un conteneur de carnet d’adresses répertorie les informations sur ses objets d’utilisateur de messagerie et de liste de distribution, tandis que la table des matières d’un dossier répertorie les informations sur ses messages. Les tables des matières sont principalement utilisées par les applications clientes. 
  
Il existe deux types de tables de contenu de dossier :
  
- Les tables de contenu standard contiennent des messages standard qui peuvent être transmis et visibles à un utilisateur. 
    
- Les tables de contenu associées contiennent des informations masquées non transmises créées par un client à des fins spécifiques, telles que le magasin d’une représentation alternative d’un message standard. Les informations associées sont créées en passant l’indicateur MAPI_ASSOCIATED à l’appel [IMAPIFolder::CreateMessage.](imapifolder-createmessage.md) 
    
Les tables de contenu de la plupart des conteneurs de carnet d’adresses et de nombreux dossiers ne peuvent pas prendre en charge le tri classé. 
  
Une table des matières est accessible en appelant :
  
- [IMAPIContainer::GetContentsTable](imapicontainer-getcontentstable.md).
    
    - Ou -
    
- [IMAPIProp::OpenProperty](imapiprop-openproperty.md) avec **PR_CONTAINER_CONTENTS** ([PidTagContainerContents](pidtagcontainercontents-canonical-property.md)) ou **PR_FOLDER_ASSOCIATED_CONTENTS** ([PidTagFolderAssociatedContents](pidtagfolderassociatedcontents-canonical-property.md)) (dossiers uniquement) spécifié en tant que balise de propriété et IID_IMAPITable comme identificateur d’interface.
    
Les fournisseurs de magasins de messages et de carnets d’adresses doivent prendre en charge les deux techniques d’extraction des propriétés de table. Il est inacceptable pour les fournisseurs de prendre en charge une seule façon d’accéder à ces tables, car les clients s’attendent à avoir le choix. 
  
 **GetContentsTable** accepte comme entrée plusieurs indicateurs qui spécifient des préférences. Lorsqu’il est MAPI_ASSOCIATED, l’indicateur récupère une table des matières associée. Étant donné que certains dossiers ne peuvent pas prendre en charge le contenu associé et qu’il n’existe aucun moyen pour les clients de le déterminer à l’avance, **GetContentsTable** renvoie parfois la MAPI_E_NO_SUPPORT d’erreur lorsqu’une table des matières associée est demandée. 
  
L MAPI_DEFERRED_ERRORS indique à l’implémenteur de la table que les erreurs rencontrées pendant l’appel n’ont pas besoin d’être signalées avant un certain temps. 
  
L’appel à **IMAPIProp::OpenProperty** implique d’accéder à une table des matières en ouvrant sa propriété correspondante, **des PR_CONTAINER_CONTENTS** pour les tables de contenu du carnet d’adresses et des tables de contenu de dossier standard et **des PR_FOLDER_ASSOCIATED_CONTENTS** pour les tables de contenu associées. Bien qu’aucune de ces propriétés ne puisse être récupérée par le biais de la méthode [IMAPIProp::GetProps](imapiprop-getprops.md) d’un dossier ou d’un conteneur, elles sont incluses dans le tableau de balises de propriétés renvoyé par la méthode [IMAPIProp::GetPropList.](imapiprop-getproplist.md) 
  
 **PR_CONTAINER_CONTENTS** permet également d’inclure ou d’exclure une table des matières d’une opération de copie. Si un client spécifie **PR_CONTAINER_CONTENTS** dans le paramètre  *lpExcludeProps*  pour **IMAPIProp::CopyTo** dans une opération de copie, le nouveau dossier ou conteneur ne prendra pas en charge la table des matières du dossier ou conteneur d’origine. 
  
Les tables de contenu de conteneur et de dossier de carnet d’adresses disposent d’une longue liste de colonnes requises , colonnes que les clients peuvent s’attendre à être disponibles après avoir récupéré la table à partir de **GetContentsTable** ou **OpenProperty**. Les fournisseurs peuvent s’ajouter à cet ensemble requis si nécessaire et les clients, via la méthode **SetColumns,** peuvent également demander des modifications. 
  
Les colonnes requises pour chacun des types de tables des matières sont les suivants :
  
|**Colonne requise**|**Type de table des matières**|
|:-----|:-----|
|**PR_ADDRTYPE** ([PidTagAddressType](pidtagaddresstype-canonical-property.md))  <br/> |Tables de conteneur de carnet d’adresses  <br/> |
|**PR_DISPLAY_NAME** ([PidTagDisplayName](pidtagdisplayname-canonical-property.md))  <br/> |Tables de conteneur de carnet d’adresses  <br/> |
|**PR_DISPLAY_CC** ([PidTagDisplayCc](pidtagdisplaycc-canonical-property.md))  <br/> |Tables des dossiers de la boutique de messages  <br/> |
|**PR_DISPLAY_TO** ([PidTagDisplayTo](pidtagdisplayto-canonical-property.md))  <br/> |Toutes les tables de contenu de dossier  <br/> |
|**PR_DISPLAY_TYPE** ([PidTagDisplayType](pidtagdisplaytype-canonical-property.md))  <br/> |Tables de conteneur de carnet d’adresses  <br/> |
|**PR_ENTRYID** ([PidTagEntryId](pidtagentryid-canonical-property.md))  <br/> |Toutes les tables des matières  <br/> |
|**PR_HASATTACH** ([PidTagHasAttachments](pidtaghasattachments-canonical-property.md))  <br/> |Toutes les tables de contenu de dossier  <br/> |
|**PR_INSTANCE_KEY** ([PidTagInstanceKey](pidtaginstancekey-canonical-property.md))  <br/> |Toutes les tables des matières  <br/> |
|**PR_LAST_MODIFICATION_TIME** ([PidTagLastModificationTime](pidtaglastmodificationtime-canonical-property.md))  <br/> |Tables des dossiers de la boutique de messages  <br/> |
|**PR_MAPPING_SIGNATURE** ([PidTagMappingSignature](pidtagmappingsignature-canonical-property.md))  <br/> |Tables des dossiers de la boutique de messages  <br/> |
|**PR_MESSAGE_CLASS** ([PidTagMessageClass](pidtagmessageclass-canonical-property.md))  <br/> |Toutes les tables de contenu de dossier  <br/> |
|**PR_MESSAGE_DOWNLOAD_TIME** ([PidTagMessageDownloadTime](pidtagmessagedownloadtime-canonical-property.md))  <br/> |Tables des dossiers de transport à distance  <br/> |
|**PR_MESSAGE_FLAGS** ([PidTagMessageFlags](pidtagmessageflags-canonical-property.md))  <br/> |Toutes les tables de contenu de dossier  <br/> |
|**PR_MESSAGE_SIZE** ([PidTagMessageSize](pidtagmessagesize-canonical-property.md))  <br/> |Toutes les tables de contenu de dossier  <br/> |
|**PR_MSG_STATUS** ([PidTagMessageStatus](pidtagmessagestatus-canonical-property.md))  <br/> |Toutes les tables de contenu de dossier  <br/> |
|**PR_OBJECT_TYPE** ([PidTagObjectType](pidtagobjecttype-canonical-property.md))  <br/> |Toutes les tables des matières  <br/> |
|**PR_PARENT_ENTRYID** ([PidTagParentEntryId](pidtagparententryid-canonical-property.md))  <br/> |Tables des dossiers de la boutique de messages  <br/> |
|**PR_RECORD_KEY** ([PidTagRecordKey](pidtagrecordkey-canonical-property.md))  <br/> |Tables des dossiers de conteneur de carnet d’adresses et de magasin de messages  <br/> |
|**PR_SENT_REPRESENTING_NAME** ([PidTagSentRepresentingName](pidtagsentrepresentingname-canonical-property.md))  <br/> |Tables des dossiers de transport à distance  <br/> |
|**PR_STORE_ENTRYID** ([PidTagStoreEntryId](pidtagstoreentryid-canonical-property.md))  <br/> |Tables des dossiers de la boutique de messages  <br/> |
|**PR_STORE_RECORD_KEY** ([PidTagStoreRecordKey](pidtagstorerecordkey-canonical-property.md))  <br/> |Tables des dossiers de la boutique de messages  <br/> |
   
L’identificateur d’entrée disponible avec chaque ligne peut être un identificateur d’entrée à court ou long terme, en fonction de l’implémentation de la table. Les identificateurs d’entrée à court terme sont généralement utilisés dans les situations où les performances sont un problème. Les deux types d’identificateur d’entrée peuvent être utilisés pour accéder à l’objet correspondant. 
  
Les tables de contenu ont également un ensemble de colonnes facultatives, mais couramment incluses par les fournisseurs de services dans leurs implémentations. Ces colonnes facultatives sont :
  
|**Colonne facultative**|**Type de table des matières**|
|:-----|:-----|
|**PR_CLIENT_SUBMIT_TIME** ([PidTagClientSubmitTime](pidtagclientsubmittime-canonical-property.md))  <br/> |Tables des dossiers de la boutique de messages  <br/> |
|**PR_CONTENT_COUNT** ([PidTagContentCount](pidtagcontentcount-canonical-property.md))  <br/> |Tables de contenu de dossier standard  <br/> |
|**PR_CONTENT_UNREAD** ([PidTagContentUnreadCount](pidtagcontentunreadcount-canonical-property.md))  <br/> |Tables de contenu de dossier standard  <br/> |
|**PR_CONVERSATION_INDEX** ([PidTagConversationIndex](pidtagconversationindex-canonical-property.md))  <br/> |Tables des dossiers de la boutique de messages  <br/> |
|**PR_EMAIL_ADDRESS** ([PidTagEmailAddress](pidtagemailaddress-canonical-property.md))  <br/> |Tables de conteneur de carnet d’adresses  <br/> |
|**PR_IMPORTANCE** ([PidTagImportance](pidtagimportance-canonical-property.md))  <br/> |Toutes les tables de contenu de dossier  <br/> |
|**PR_MESSAGE_DELIVERY_TIME** ([PidTagMessageDeliveryTime](pidtagmessagedeliverytime-canonical-property.md))  <br/> |Toutes les tables de contenu de dossier  <br/> |
|**PR_NORMALIZED_SUBJECT** ([PidTagNormalizedSubject](pidtagnormalizedsubject-canonical-property.md))  <br/> |Toutes les tables de contenu de dossier  <br/> |
|**PR_PRIORITY** ([PidTagPriority](pidtagpriority-canonical-property.md))  <br/> |Toutes les tables de contenu de dossier  <br/> |
|**PR_SEARCH_KEY** ([PidTagSearchKey](pidtagsearchkey-canonical-property.md))  <br/> |Tables de conteneur de carnet d’adresses  <br/> |
|**PR_SEND_RICH_INFO** ([PidTagSendRichInfo](pidtagsendrichinfo-canonical-property.md))  <br/> |Tables de conteneur de carnet d’adresses  <br/> |
|**PR_SENDER_NAME** ([PidTagSenderName](pidtagsendername-canonical-property.md))  <br/> |Toutes les tables de contenu de dossier  <br/> |
|**PR_SENSITIVITY** ([PidTagSensitivity](pidtagsensitivity-canonical-property.md))  <br/> |Toutes les tables de contenu de dossier  <br/> |
|**PR_SUBJECT** ([PidTagSubject](pidtagsubject-canonical-property.md))  <br/> |Toutes les tables de contenu de dossier  <br/> |
|**PR_TRANSMITABLE_DISPLAY_NAME** ([PidTagTransmittableDisplayName](pidtagtransmittabledisplayname-canonical-property.md))  <br/> |Tables de conteneur de carnet d’adresses  <br/> |
   
Les fournisseurs de magasins de messages doivent également inclure **PR_PARENT_DISPLAY** ([PidTagParentDisplay](pidtagparentdisplay-canonical-property.md)) pour les tables de contenu des dossiers de résultats de recherche uniquement.
  
Les propriétés nommées peuvent être ajoutées à l’ensemble de colonnes d’une table de contenu de dossier uniquement si tous les messages du dossier ont la même signature de mappage, c’est-à-dire le même mappage des noms de propriétés aux identificateurs de propriété. Les tables de contenu de dossier doivent prendre en charge l’ajout de propriétés spécifiques à la classe de message au jeu de colonnes, s’ils la prise en charge de la création de messages arbitraires dans le dossier.
  
Les clients peuvent enregistrer l’ordre de tri par défaut d’une table de contenu de dossier en appelant sa méthode [IMAPIFolder::SaveContentsSort.](imapifolder-savecontentssort.md) Si l RECURSIVE_SORT est spécifié lors de l’appel, l’ordre de tri peut être appliqué à tous les sous-dossiers du dossier. 
  
## <a name="see-also"></a>Voir aussi



[MAPI Tables](mapi-tables.md)

