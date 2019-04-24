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
ms.openlocfilehash: 491381c771cae65e682acc8033b6558523847d3d
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32335594"
---
# <a name="contents-tables"></a>Tables des matières

  
  
**S’applique à** : Outlook 2013 | Outlook 2016 
  
Une table de contenu contient des informations sur les objets dans un conteneur MAPI. Les fournisseurs de carnet d'adresses implémentent les tables de contenu pour chacun de leurs conteneurs, ainsi que les banques de messages et les fournisseurs de transport distants implémentent les tables de contenu pour leurs dossiers. La table des matières d'un conteneur de carnet d'adresses répertorie les informations sur ses objets utilisateur de messagerie et de liste de distribution, tandis que la table des matières d'un dossier répertorie des informations sur ses messages. Les tables de contenu sont principalement utilisées par les applications clientes. 
  
Il existe deux types de tables de contenu de dossier:
  
- Les tables de contenu standard contiennent des messages standard, c'est-à-dire des messages qui peuvent être transmis et visibles par un utilisateur. 
    
- Les tables de contenu associées contiennent des informations masquées, non transmissibles, créées par un client à des fins spécifiques, par exemple pour stocker une représentation alternative d'un message standard. Les informations associées sont créées en transmettant l'indicateur MAPI_ASSOCIATED à l'appel [IMAPIFolder:: CreateMessage](imapifolder-createmessage.md) . 
    
Les tables de contenu de la plupart des conteneurs de carnet d'adresses et de nombreux dossiers ne prennent pas en charge le tri par catégorie. 
  
Il est possible d'accéder à une table des matières en appelant:
  
- [IMAPIContainer:: GetContentsTable](imapicontainer-getcontentstable.md).
    
    - Des
    
- [IMAPIProp:: OpenProperty](imapiprop-openproperty.md) avec **PR_CONTAINER_CONTENTS** ([PidTagContainerContents](pidtagcontainercontents-canonical-property.md)) ou **PR_FOLDER_ASSOCIATED_CONTENTS** ([PidTagFolderAssociatedContents](pidtagfolderassociatedcontents-canonical-property.md)) (dossiers uniquement) SPÉCIFIÉs en tant que balise de propriété et IID _IMAPITable en tant qu'identificateur d'interface.
    
Les fournisseurs de banques de messages et de carnets d'adresses doivent prendre en charge les deux techniques de récupération des propriétés de table. Il est inacceptable pour les fournisseurs de ne prendre en charge qu'un seul moyen d'accéder à ces tables, car les clients s'attendent à avoir le choix. 
  
 **GetContentsTable** accepte comme entrée plusieurs indicateurs qui spécifient des préférences. Lorsque ce paramètre est défini, l'indicateur MAPI_ASSOCIATED récupère une table de contenu associée. Étant donné que certains dossiers ne prennent pas en charge le contenu associé et qu'il n'existe aucun moyen pour les clients de le déterminer à l'avance, **GetContentsTable** renvoie parfois l'erreur MAPI_E_NO_SUPPORT lorsqu'une table de contenu associée est demandée. 
  
L'indicateur MAPI_DEFERRED_ERRORS indique à l'implémenteur du tableau que les erreurs rencontrées lors de l'appel n'ont pas besoin d'être signalées plus tard. 
  
L'appel à **IMAPIProp:: OpenProperty** implique l'accès à une table de contenu en ouvrant sa propriété correspondante, **PR_CONTAINER_CONTENTS** pour les tables de contenu de carnet d'adresses et de contenu de dossier standard, et **PR_FOLDER_ASSOCIATED_ CONTENU** des tables des matières associées. Bien que ces propriétés ne puissent pas être récupérées par le biais de la méthode [IMAPIProp:: GetProps](imapiprop-getprops.md) d'un dossier ou d'un conteneur, elles sont incluses dans le tableau des balises de propriété qui est renvoyé par la méthode [IMAPIProp:: GetPropList](imapiprop-getproplist.md) . 
  
 **PR_CONTAINER_CONTENTS** peut également être utilisé pour inclure ou exclure une table des matières d'une opération de copie. Si un client spécifie **PR_CONTAINER_CONTENTS** dans le paramètre *lpExcludeProps* pour **IMAPIProp:: CopyTo** dans une opération de copie, le nouveau dossier ou conteneur ne prend pas en charge la table des matières du dossier ou du conteneur d'origine. 
  
Les tables conteneur du carnet d'adresses et contenu du dossier contiennent une longue liste de colonnes obligatoires (colonnes que les clients peuvent s'attendre à être disponibles après avoir récupéré la table à partir de **GetContentsTable** ou **OpenProperty**. Les fournisseurs peuvent ajouter à cet ensemble obligatoire si nécessaire et les clients, via la méthode **SetColumns** , peuvent également demander des modifications. 
  
Les colonnes requises pour chaque type de table de contenu sont les suivantes:
  
|**Colonne obligatoire**|**Type de table des matières**|
|:-----|:-----|
|**PR_ADDRTYPE** ([PidTagAddressType](pidtagaddresstype-canonical-property.md))  <br/> |Tables de conteneurs du carnet d'adresses  <br/> |
|**PR_DISPLAY_NAME** ([PidTagDisplayName](pidtagdisplayname-canonical-property.md))  <br/> |Tables de conteneurs du carnet d'adresses  <br/> |
|**PR_DISPLAY_CC** ([PidTagDisplayCc](pidtagdisplaycc-canonical-property.md))  <br/> |Tables de dossiers de banque de messages  <br/> |
|**PR_DISPLAY_TO** ([PidTagDisplayTo](pidtagdisplayto-canonical-property.md))  <br/> |Tous les tableaux de contenu de dossier  <br/> |
|**PR_DISPLAY_TYPE** ([PidTagDisplayType](pidtagdisplaytype-canonical-property.md))  <br/> |Tables de conteneurs du carnet d'adresses  <br/> |
|**PR_ENTRYID** ([PidTagEntryId](pidtagentryid-canonical-property.md))  <br/> |Toutes les tables de contenu  <br/> |
|**PR_HASATTACH** ([PidTagHasAttachments](pidtaghasattachments-canonical-property.md))  <br/> |Tous les tableaux de contenu de dossier  <br/> |
|**PR_INSTANCE_KEY** ([PidTagInstanceKey](pidtaginstancekey-canonical-property.md))  <br/> |Toutes les tables de contenu  <br/> |
|**PR_LAST_MODIFICATION_TIME** ([PidTagLastModificationTime](pidtaglastmodificationtime-canonical-property.md))  <br/> |Tables de dossiers de banque de messages  <br/> |
|**PR_MAPPING_SIGNATURE** ([PidTagMappingSignature](pidtagmappingsignature-canonical-property.md))  <br/> |Tables de dossiers de banque de messages  <br/> |
|**PR_MESSAGE_CLASS** ([PidTagMessageClass](pidtagmessageclass-canonical-property.md))  <br/> |Tous les tableaux de contenu de dossier  <br/> |
|**PR_MESSAGE_DOWNLOAD_TIME** ([PidTagMessageDownloadTime](pidtagmessagedownloadtime-canonical-property.md))  <br/> |Tables de dossiers de transport à distance  <br/> |
|**PR_MESSAGE_FLAGS** ([PidTagMessageFlags](pidtagmessageflags-canonical-property.md))  <br/> |Tous les tableaux de contenu de dossier  <br/> |
|**PR_MESSAGE_SIZE** ([PidTagMessageSize](pidtagmessagesize-canonical-property.md))  <br/> |Tous les tableaux de contenu de dossier  <br/> |
|**PR_MSG_STATUS** ([PidTagMessageStatus](pidtagmessagestatus-canonical-property.md))  <br/> |Tous les tableaux de contenu de dossier  <br/> |
|**PR_OBJECT_TYPE** ([PidTagObjectType](pidtagobjecttype-canonical-property.md))  <br/> |Toutes les tables de contenu  <br/> |
|**PR_PARENT_ENTRYID** ([PidTagParentEntryId](pidtagparententryid-canonical-property.md))  <br/> |Tables de dossiers de banque de messages  <br/> |
|**PR_RECORD_KEY** ([PidTagRecordKey](pidtagrecordkey-canonical-property.md))  <br/> |Conteneur de carnet d'adresses et tables de dossiers de banque de messages  <br/> |
|**PR_SENT_REPRESENTING_NAME** ([PidTagSentRepresentingName](pidtagsentrepresentingname-canonical-property.md))  <br/> |Tables de dossiers de transport à distance  <br/> |
|**PR_STORE_ENTRYID** ([PidTagStoreEntryId](pidtagstoreentryid-canonical-property.md))  <br/> |Tables de dossiers de banque de messages  <br/> |
|**PR_STORE_RECORD_KEY** ([PidTagStoreRecordKey](pidtagstorerecordkey-canonical-property.md))  <br/> |Tables de dossiers de banque de messages  <br/> |
   
L'identificateur d'entrée disponible avec chaque ligne peut être un identificateur d'entrée à court ou long terme, en fonction de l'implémentation de la table. Les identificateurs d'entrée à court terme sont généralement utilisés dans les situations où les performances sont un problème. Les deux types d'identificateurs d'entrée peuvent être utilisés pour accéder à l'objet correspondant. 
  
Les tables de contenu ont également un ensemble de colonnes qui sont facultatives, mais généralement incluses par les fournisseurs de services dans leurs implémentations. Ces colonnes facultatives sont les suivantes:
  
|**Colonne facultative**|**Type de table des matières**|
|:-----|:-----|
|**PR_CLIENT_SUBMIT_TIME** ([PidTagClientSubmitTime](pidtagclientsubmittime-canonical-property.md))  <br/> |Tables de dossiers de banque de messages  <br/> |
|**PR_CONTENT_COUNT** ([PidTagContentCount](pidtagcontentcount-canonical-property.md))  <br/> |Tables de contenu de dossier standard  <br/> |
|**PR_CONTENT_UNREAD** ([PidTagContentUnreadCount](pidtagcontentunreadcount-canonical-property.md))  <br/> |Tables de contenu de dossier standard  <br/> |
|**PR_CONVERSATION_INDEX** ([PidTagConversationIndex](pidtagconversationindex-canonical-property.md))  <br/> |Tables de dossiers de banque de messages  <br/> |
|**PR_EMAIL_ADDRESS** ([PidTagEmailAddress](pidtagemailaddress-canonical-property.md))  <br/> |Tables de conteneurs du carnet d'adresses  <br/> |
|**PR_IMPORTANCE** ([PidTagImportance](pidtagimportance-canonical-property.md))  <br/> |Tous les tableaux de contenu de dossier  <br/> |
|**PR_MESSAGE_DELIVERY_TIME** ([PidTagMessageDeliveryTime](pidtagmessagedeliverytime-canonical-property.md))  <br/> |Tous les tableaux de contenu de dossier  <br/> |
|**PR_NORMALIZED_SUBJECT** ([PidTagNormalizedSubject](pidtagnormalizedsubject-canonical-property.md))  <br/> |Tous les tableaux de contenu de dossier  <br/> |
|**PR_PRIORITY** ([PidTagPriority](pidtagpriority-canonical-property.md))  <br/> |Tous les tableaux de contenu de dossier  <br/> |
|**PR_SEARCH_KEY** ([PidTagSearchKey](pidtagsearchkey-canonical-property.md))  <br/> |Tables de conteneurs du carnet d'adresses  <br/> |
|**PR_SEND_RICH_INFO** ([PidTagSendRichInfo](pidtagsendrichinfo-canonical-property.md))  <br/> |Tables de conteneurs du carnet d'adresses  <br/> |
|**PR_SENDER_NAME** ([PidTagSenderName](pidtagsendername-canonical-property.md))  <br/> |Tous les tableaux de contenu de dossier  <br/> |
|**PR_SENSITIVITY** ([PidTagSensitivity](pidtagsensitivity-canonical-property.md))  <br/> |Tous les tableaux de contenu de dossier  <br/> |
|**PR_SUBJECT** ([PidTagSubject](pidtagsubject-canonical-property.md))  <br/> |Tous les tableaux de contenu de dossier  <br/> |
|**PR_TRANSMITABLE_DISPLAY_NAME** ([PidTagTransmittableDisplayName](pidtagtransmittabledisplayname-canonical-property.md))  <br/> |Tables de conteneurs du carnet d'adresses  <br/> |
   
Les fournisseurs de banques de messages doivent également inclure **PR_PARENT_DISPLAY** ([PidTagParentDisplay](pidtagparentdisplay-canonical-property.md)) pour les tables de contenu des dossiers de résultats de recherche uniquement.
  
Les propriétés nommées peuvent être ajoutées à l'ensemble de colonnes d'une table de contenu de dossier uniquement si tous les messages dans le dossier ont la même signature de mappage, c'est-à-dire le même mappage des noms de propriétés aux identificateurs de propriétés. Les tables de contenu de dossier doivent prendre en charge l'ajout de propriétés spécifiques à la classe de message dans le jeu de colonnes, s'ils prennent en charge la création de messages arbitraires dans le dossier.
  
Les clients peuvent enregistrer l'ordre de tri par défaut pour une table de contenu de dossier en appelant la méthode [IMAPIFolder:: SaveContentsSort](imapifolder-savecontentssort.md) . Si l'indicateur RECURSIVE_SORT est spécifié sur l'appel, l'ordre de tri peut être appliqué à tous les sous-dossiers dans le dossier. 
  
## <a name="see-also"></a>Voir aussi



[Tables MAPI](mapi-tables.md)

