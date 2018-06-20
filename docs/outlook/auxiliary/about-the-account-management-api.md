---
title: À propos de l’API de gestion de compte
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: overview
localization_priority: Normal
ms.assetid: eb6b921d-ecf8-3ce5-87ba-ac1632416b05
description: 'L’API de gestion de compte permet d’accéder aux informations de compte et prend en charge les notifications des modifications de compte. Comme des clients de cette API, les fournisseurs de messagerie procédez comme suit :'
ms.openlocfilehash: 678143def25395c47f1c17cc99dcdcd1fb145e1c
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19782543"
---
# <a name="about-the-account-management-api"></a>À propos de l’API de gestion de compte

L’API de gestion de compte permet d’accéder aux informations de compte et prend en charge les notifications des modifications de compte. Comme des clients de cette API, les fournisseurs de messagerie procédez comme suit :
  
1. Utilisez [IOlkAccountManager](iolkaccountmanager.md) pour gérer l’accès aux comptes et configurer des notifications sur les modifications de compte. 
    
2. Mettre en œuvre et [IOlkAccountNotify](iolkaccountnotify.md) permet d’envoyer des notifications sur les modifications de compte. 
    
3. Utilisez [IOlkEnum](iolkenum.md) pour énumérer les comptes. 
    
4. Utilisez [IOlkAccount](iolkaccount.md) pour obtenir et définir des propriétés et autres informations sur un compte. Les clients obtiennent cette interface via [IOlkAccountManager::FindAccount](iolkaccountmanager-findaccount.md) ou [IOlkEnum::GetNext](iolkenum-getnext.md) pour accéder à un compte individuel. 
    
5. Mettre en œuvre et utiliser [IOlkAccountHelper](iolkaccounthelper.md) pour fournir les fonctionnalités d’assistance de gestionnaire de compte, y compris pour obtenir le nom du profil d’un compte et la session MAPI en cours. 
    
6. Mettre en œuvre et permet de fournir des informations supplémentaires sur une erreur dans **IOlkAccountManager**, **IOlkAccountNotify**et **IOlkAccount** [IOlkErrorUnknown](iolkerrorunknown.md) . 

##  <a name="account-management-api-components"></a>Composants d’API de gestion de compte

L’API de gestion de compte fournit les définitions suivantes, les types de données, des interfaces, nommé les propriétés et les propriétés.
  
### <a name="definitions"></a>Définitions
  
- [Constantes (API de gestion des comptes)](constants-account-management-api.md)
    
### <a name="data-types"></a>Types de données
  
- [ACCT_BIN](acct_bin.md)
    
- [ACCT_VARIANT](acct_variant.md)
    
### <a name="interfaces"></a>Interfaces
  
- [IOlkAccount](iolkaccount.md)
    
- [IOlkAccountHelper](iolkaccounthelper.md)
    
- [IOlkAccountManager](iolkaccountmanager.md)
    
- [IOlkAccountNotify](iolkaccountnotify.md)
    
- [IOlkEnum](iolkenum.md)
    
- [IOlkErrorUnknown](iolkerrorunknown.md)
    
### <a name="named-properties"></a>Propriétés nommées
  
- [PidLidInternetAccountName](pidlidinternetaccountname.md)
    
- [PidLidInternetAccountStamp](pidlidinternetaccountstamp.md)
    
### <a name="properties"></a>Propriétés
  
- [PidTagNextSendAcct](pidtagnextsendacct.md)
    
- [PidTagPrimarySendAccount](pidtagprimarysendaccount.md)
    
- [PROP_ACCT_DELIVERY_FOLDER](prop_acct_delivery_folder.md)
    
- [PROP_ACCT_DELIVERY_STORE](prop_acct_delivery_store.md)
    
- [PROP_ACCT_ID](prop_acct_id.md)
    
- [PROP_ACCT_IS_EXCH](prop_acct_is_exch.md)
    
- [PROP_ACCT_NAME](prop_acct_name.md)
    
- [PROP_ACCT_PREFERENCES_UID](prop_acct_preferences_uid.md)
    
- [PROP_ACCT_SEND_STAMP](prop_acct_send_stamp.md)
    
- [PROP_ACCT_SENTITEMS_EID](prop_acct_sentitems_eid.md)
    
- [PROP_ACCT_STAMP](prop_acct_stamp.md)
    
- [PROP_ACCT_USER_EMAIL_ADDR](prop_acct_user_email_addr.md)
    
- [PROP_ACCT_USER_DISPLAY_NAME](prop_acct_user_display_name.md)
    
- [PROP_MAPI_EMSMDB_UID](prop_mapi_emsmdb_uid.md)
    
- [PROP_MAPI_IDENTITY_ENTRYID](prop_mapi_identity_entryid.md)
    
- [PROP_MAPI_TRANSPORT_FLAGS](prop_mapi_transport_flags.md)
    

