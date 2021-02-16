---
title: À propos de l’API de gestion des comptes
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: overview
localization_priority: Normal
ms.assetid: eb6b921d-ecf8-3ce5-87ba-ac1632416b05
description: 'L’API de gestion des comptes permet d’accéder aux informations de compte et prend en charge les notifications de modifications de compte. En tant que clients de cette API, les fournisseurs de messagerie font les choses suivantes :'
ms.openlocfilehash: 76520b7cc7f28ede28257729e4e4fbe2d5096290
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/28/2019
ms.locfileid: "33426248"
---
# <a name="about-the-account-management-api"></a>À propos de l’API de gestion des comptes

L’API de gestion des comptes permet d’accéder aux informations de compte et prend en charge les notifications de modifications de compte. En tant que clients de cette API, les fournisseurs de messagerie font les choses suivantes :
  
1. Utilisez [IOlkAccountManager pour](iolkaccountmanager.md) gérer l’accès aux comptes et configurer des notifications concernant les modifications de compte. 
    
2. Implémentez [et utilisez IOlkAccountNotify](iolkaccountnotify.md) pour envoyer des notifications concernant les modifications de compte. 
    
3. Utilisez [IOlkEnum pour](iolkenum.md) éumer les comptes. 
    
4. Utilisez [IOlkAccount pour](iolkaccount.md) obtenir et définir des propriétés et d’autres informations sur un compte. Les clients obtiennent cette interface via [IOlkAccountManager::FindAccount](iolkaccountmanager-findaccount.md) ou [IOlkEnum::GetNext](iolkenum-getnext.md) pour accéder à un compte individuel. 
    
5. Implémentez et utilisez [IOlkAccountHelper](iolkaccounthelper.md) pour fournir la fonctionnalité d’aide du gestionnaire de comptes, y compris l’obtention du nom de profil d’un compte et de la session MAPI actuelle. 
    
6. Implémentez et utilisez [IOlkErrorUnknown](iolkerrorunknown.md) pour fournir des informations supplémentaires sur une erreur dans **IOlkAccountManager,** **IOlkAccountNotify** et **IOlkAccount**. 

##  <a name="account-management-api-components"></a>Composants de l’API de gestion des comptes

L’API de gestion des comptes fournit les définitions, les types de données, les interfaces, les propriétés nommées et les propriétés suivantes.
  
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
    

