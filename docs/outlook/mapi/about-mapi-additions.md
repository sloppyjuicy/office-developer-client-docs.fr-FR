---
title: Ajouts MAPI
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.localizationpriority: medium
ms.assetid: 78e2806d-bb6f-cd96-21f1-b7c667c73c33
description: 'Derniére modification : samedi 23 juillet 2011'
ms.openlocfilehash: 033053c41988ad9b63f88def7652d1a37dae5f1e
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/24/2021
ms.locfileid: "59588307"
---
# <a name="about-mapi-additions"></a>Ajouts MAPI

**S’applique à** : Outlook 2013 | Outlook 2016 
  
Les ajouts MAPI sont des API qui appartiennent à l’interface MAPI (Messaging Application Programming Interface), telles que les types de données, les fonctions et les propriétés, qui n’ont pas été précédemment exposées et documentées dans le cadre de la Référence du programmeur MAPI. Elles incluent les définitions et propriétés suivantes.
  
## <a name="constant-definitions"></a>Définitions des constantes

- **[Constantes MAPI supplémentaires](mapi-constants.md)**
  
## <a name="data-types"></a>Types de données

- **[EXCHANGE_STORE_VERSION_NUM](exchange_store_version_num.md)**
    
- **[FollowUpStatus](followupstatus.md)**
    
- **[Gender](gender.md)**
    
- **[OlFlagIcon](olflagicon.md)**
    
## <a name="functions"></a>Fonctions

- **[FixMAPI](fixmapi.md)**
    
## <a name="properties"></a>Propriétés

Les propriétés suivantes sont généralement exposées par les objets de message.
  
- **[PR_BODY_W](pidtagbody-canonical-property.md)**
    
- **[PR_CONFLICT_ITEMS](pidtagconflictitems-canonical-property.md)**
    
- **[PR_DISPLAY_BCC_W](pidtagdisplaybcc-canonical-property.md)**
    
- **[PR_DISPLAY_CC_W](pidtagdisplaycc-canonical-property.md)**
    
- **[PR_DISPLAY_TO_W](pidtagdisplayto-canonical-property.md)**
    
- **[PR_FLAG_STATUS](pidtagflagstatus-canonical-property.md)**
    
- **[PR_FOLLOWUP_ICON](pidtagfollowupicon-canonical-property.md)**
    
- **[PR_INETMAIL_OVERRIDE_FORMAT](pidtaginternetmailoverrideformat-canonical-property.md)**
    
- **[PR_MESSAGE_CLASS_W](pidtagmessageclass-canonical-property.md)**
    
- **[PR_MSG_EDITOR_FORMAT](pidtagmessageeditorformat-canonical-property.md)**
    
- **[PR_NORMALIZED_SUBJECT_W](pidtagnormalizedsubject-canonical-property.md)**
    
- **[PR_SENDER_ADDRTYPE_W](pidtagsenderaddresstype-canonical-property.md)**
    
- **[PR_SENDER_EMAIL_ADDRESS_W](pidtagsenderemailaddress-canonical-property.md)**
    
- **[PR_SENDER_NAME_W](pidtagsendername-canonical-property.md)**
    
- **[PR_SENT_REPRESENTING_ADDRTYPE_W](pidtagsentrepresentingaddresstype-canonical-property.md)**
    
- **[PR_SENT_REPRESENTING_EMAIL_ADDRESS_W](pidtagsentrepresentingemailaddress-canonical-property.md)**
    
- **[PR_SENT_REPRESENTING_NAME_W](pidtagsentrepresentingname-canonical-property.md)**
    
- **[PR_SUBJECT_PREFIX_W](pidtagsubjectprefix-canonical-property.md)**
    
- **[PR_SUBJECT_W](pidtagsubject-canonical-property.md)**
    
Les propriétés suivantes sont exposées par des objets de table de contenu de carnet d’adresses.
  
- **[PR_DISPLAY_TYPE_EX](pidtagdisplaytypeex-canonical-property.md)**
    
Les propriétés suivantes sont exposées par des objets conteneur de carnet d’adresses.
  
- **[PR_EMS_AB_SERVER](pidtagemsabserver-canonical-property.md)**
    
- **[PR_EMS_AB_SERVER_A](pidtagemsabserver-canonical-property.md)**
    
- **[PR_EMS_AB_SERVER_W](pidtagemsabserver-canonical-property.md)**
    
Les propriétés suivantes sont exposées par des objets de dossier.
  
- **[PR_AGING_GRANULARITY](pidtagaginggranularity-canonical-property.md)**
    
- **[PR_AGING_PERIOD](pidtagagingperiod-canonical-property.md)**
    
Les propriétés suivantes sont exposées par les objets utilisateur de messagerie.
  
- **[PR_ASSISTANT_TELEPHONE_NUMBER_W](pidtagassistanttelephonenumber-canonical-property.md)**
    
- **[PR_ASSISTANT_W](pidtagassistant-canonical-property.md)**
    
- **[PR_ATTACHMENT_CONTACTPHOTO](pidtagattachmentcontactphoto-canonical-property.md)**
    
- **[PR_BIRTHDAY](pidtagbirthday-canonical-property.md)**
    
- **[PR_BUSINESS_FAX_NUMBER_W](pidtagbusinessfaxnumber-canonical-property.md)**
    
- **[PR_BUSINESS_HOME_PAGE_W](pidtagbusinesshomepage-canonical-property.md)**
    
- **[PR_CALLBACK_TELEPHONE_NUMBER_W](pidtagcallbacktelephonenumber-canonical-property.md)**
    
- **[PR_CAR_TELEPHONE_NUMBER_W](pidtagcartelephonenumber-canonical-property.md)**
    
- **[PR_CELLULAR_TELEPHONE_NUMBER_W](pidtagmobiletelephonenumber-canonical-property.md)**
    
- **[PR_CHILDRENS_NAMES_W](pidtagchildrensnames-canonical-property.md)**
    
- **[PR_DEPARTMENT_NAME_W](pidtagdepartmentname-canonical-property.md)**
    
- **[PR_DISPLAY_NAME_PREFIX_W](pidtagdisplaynameprefix-canonical-property.md)**
    
- **[PR_GENDER](pidtaggender-canonical-property.md)**
    
- **[PR_GENERATION_W](pidtaggeneration-canonical-property.md)**
    
- **[PR_GIVEN_NAME_W](pidtaggivenname-canonical-property.md)**
    
- **[PR_HOBBIES_W](pidtaghobbies-canonical-property.md)**
    
- **[PR_HOME_ADDRESS_CITY_W](pidtaghomeaddresscity-canonical-property.md)**
    
- **[PR_HOME_ADDRESS_COUNTRY_W](pidtaghomeaddresscountry-canonical-property.md)**
    
- **[PR_HOME_ADDRESS_POST_OFFICE_BOX_W](pidtaghomeaddresspostofficebox-canonical-property.md)**
    
- **[PR_HOME_ADDRESS_POSTAL_CODE_W](pidtaghomeaddresspostalcode-canonical-property.md)**
    
- **[PR_HOME_ADDRESS_STATE_OR_PROVINCE_W](pidtaghomeaddressstateorprovince-canonical-property.md)**
    
- **[PR_HOME_ADDRESS_STREET_W](pidtaghomeaddressstreet-canonical-property.md)**
    
- **[PR_HOME_FAX_NUMBER_W](pidtaghomefaxnumber-canonical-property.md)**
    
- **[PR_HOME_TELEPHONE_NUMBER_W](pidtaghometelephonenumber-canonical-property.md)**
    
- **[PR_KEYWORD_W](pidtagkeyword-canonical-property.md)**
    
- **[PR_MANAGER_NAME_W](pidtagmanagername-canonical-property.md)**
    
- **[PR_MIDDLE_NAME_W](pidtagmiddlename-canonical-property.md)**
    
- **[PR_NICKNAME_W](pidtagnickname-canonical-property.md)**
    
- **[PR_OFFICE_LOCATION_W](pidtagofficelocation-canonical-property.md)**
    
- **[PR_OFFICE_TELEPHONE_NUMBER_W](pidtagbusinesstelephonenumber-canonical-property.md)**
    
- **[PR_OTHER_ADDRESS_CITY_W](pidtagotheraddresscity-canonical-property.md)**
    
- **[PR_OTHER_ADDRESS_COUNTRY_W](pidtagotheraddresscountry-canonical-property.md)**
    
- **[PR_OTHER_ADDRESS_POST_OFFICE_BOX_W](pidtagotheraddresspostofficebox-canonical-property.md)**
    
- **[PR_OTHER_ADDRESS_POSTAL_CODE_W](pidtagotheraddresspostalcode-canonical-property.md)**
    
- **[PR_OTHER_ADDRESS_STATE_OR_PROVINCE_W](pidtagotheraddressstateorprovince-canonical-property.md)**
    
- **[PR_OTHER_ADDRESS_STREET_W](pidtagotheraddressstreet-canonical-property.md)**
    
- **[PR_PAGER_TELEPHONE_NUMBER_W](pidtagpagertelephonenumber-canonical-property.md)**
    
- **[PR_PERSONAL_HOME_PAGE_W](pidtagpersonalhomepage-canonical-property.md)**
    
- **[PR_PRIMARY_TELEPHONE_NUMBER_W](pidtagprimarytelephonenumber-canonical-property.md)**
    
- **[PR_PROFESSION_W](pidtagprofession-canonical-property.md)**
    
- **[PR_SPOUSE_NAME_W](pidtagspousename-canonical-property.md)**
    
- **[PR_SURNAME_W](pidtagsurname-canonical-property.md)**
    
- **[PR_TITLE_W](pidtagtitle-canonical-property.md)**
    
- **[PR_TTYTDD_PHONE_NUMBER_W](pidtagttytddphonenumber-canonical-property.md)**
    
- **[PR_WEDDING_ANNIVERSARY](pidtagweddinganniversary-canonical-property.md)**
    
Les propriétés suivantes sont exposées par des objets de section de profil.
  
- **[PR_PROFILE_SERVER_FULL_VERSION](pidtagprofileserverfullversion-canonical-property.md)**
    
- **[PR_PROFILE_SERVER_VERSION](pidtagprofileserverversion-canonical-property.md)**
    
- **[PR_PROVIDER_DISPLAY_NAME_W](pidtagproviderdisplayname-canonical-property.md)**
    
- **[PR_PROVIDER_ICON_W](pidtagprovidericon-canonical-property.md)**
    
- **[PR_ROH_FLAGS](pidtagrpcoverhttpflags-canonical-property.md)**
    
- **[PR_ROH_PROXY_AUTH_SCHEME](pidtagrpcoverhttpproxyauthscheme-canonical-property.md)**
    
- **[PR_ROH_PROXY_PRINCIPAL_NAME](pidtagrpcoverhttpproxyprincipalname-canonical-property.md)**
    
- **[PR_ROH_PROXY_SERVER](pidtagrpcoverhttpproxyserver-canonical-property.md)**
    
Les propriétés suivantes sont exposées par les objets store.
  
- **[PR_IPM_APPOINTMENT_ENTRYID](pidtagipmappointmententryid-canonical-property.md)**
    
- **[PR_IPM_CONTACT_ENTRYID](pidtagipmcontactentryid-canonical-property.md)**
    
- **[PR_IPM_DRAFTS_ENTRYID](pidtagipmdraftsentryid-canonical-property.md)**
    
- **[PR_IPM_JOURNAL_ENTRYID](pidtagipmjournalentryid-canonical-property.md)**
    
- **[PR_IPM_NOTE_ENTRYID](pidtagipmnoteentryid-canonical-property.md)**
    
- **[PR_IPM_TASK_ENTRYID](pidtagipmtaskentryid-canonical-property.md)**
    
Les propriétés suivantes sont exposées par les objets store et sont utilisées pour rechercher des éléments spécifiques d’un e-mail dans la boutique.
  
- **[PR_SEARCH_ATTACHMENTS_W](pidtagsearchattachments-canonical-property.md)**
    
- **[PR_SEARCH_RECIP_EMAIL_BCC_W](pidtagsearchrecipientemailbcc-canonical-property.md)**
    
- **[PR_SEARCH_RECIP_EMAIL_CC_W](pidtagsearchrecipientemailcc-canonical-property.md)**
    
- **[PR_SEARCH_RECIP_EMAIL_TO_W](pidtagsearchrecipientemailto-canonical-property.md)**
    
## <a name="see-also"></a>Voir aussi

- [Accès à une banque sur le serveur distant lorsqu’Outlook est en mode Exchange mis en cache](how-to-access-store-on-remote-server-in-cached-exchange-mode.md)  
- [Détecter la version d’Exchange Server dans un profil Outlook client](how-to-detect-the-version-of-exchange-server-in-an-outlook-profile.md)
- [Ouvrir une banque sur le serveur distant lorsqu’Outlook est en mode Exchange mis en cache](how-to-open-store-on-remote-server-in-cached-exchange-mode.md)
- [Gérer un message dans un fichier OST sans appeler de synchronisation en mode Exchange mis en cache](how-to-manage-a-message-in-an-ost-without-invoking-a-synchronization.md)

