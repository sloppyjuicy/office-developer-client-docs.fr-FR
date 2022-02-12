---
title: IOlkAccount
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.localizationpriority: medium
ms.assetid: 7b7cb295-fc77-a8b9-aac9-e548f3b4afcb
ms.openlocfilehash: c36db2d700d5c36804f771218376c403c6eadc6c
ms.sourcegitcommit: c0fae34cd3a9c75a7cffcf9ae8e417ddde07a989
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 02/12/2022
ms.locfileid: "62784369"
---
# <a name="iolkaccount"></a>IOlkAccount

Prend en charge l’obtention et la définition de propriétés et d’autres informations sur un compte.
  
## <a name="quick-info"></a>Informations rapides

|||
|:-----|:-----|
|Hérite de :  <br/> |[IOlkErrorUnknown](iolkerrorunknown.md) <br/> |
|Implémenté par :  <br/> |Outlook  <br/> |
|Fourni par :  <br/> |[IOlkAccountManager::FindAccount](iolkaccountmanager-findaccount.md) and [IOlkEnum::GetNext](iolkenum-getnext.md) <br/> |
|Appelé par :  <br/> |Client  <br/> |
|Identificateur d’interface :  <br/> |IID_IOlkAccount  <br/> |
   
## <a name="vtable-order"></a>Ordre des vtables

|||
|:-----|:-----|
| *Membre d’espace réservé*  <br/> | *Non pris en charge ou documenté.*  <br/> |
| *Membre d’espace réservé*  <br/> | *Non pris en charge ou documenté.*  <br/> |
| *Membre d’espace réservé*  <br/> | *Non pris en charge ou documenté.*  <br/> |
| *Membre d’espace réservé*  <br/> | *Non pris en charge ou documenté.*  <br/> |
| *Membre d’espace réservé*  <br/> | *Non pris en charge ou documenté.*  <br/> |
| *Membre d’espace réservé*  <br/> | *Non pris en charge ou documenté.*  <br/> |
|[GetAccountInfo](iolkaccount-getaccountinfo.md) <br/> |Obtient le type et les catégories du compte spécifié. |
|[GetProp](iolkaccount-getprop.md) <br/> |Obtient la valeur de la propriété de compte spécifiée. Voir le tableau Propriétés ci-dessous. |
|[SetProp](iolkaccount-setprop.md) <br/> |Définit la valeur de la propriété de compte spécifiée. Voir le tableau Propriétés ci-dessous. |
| *Membre d’espace réservé*  <br/> | *Non pris en charge ou documenté.*  <br/> |
| *Membre d’espace réservé*  <br/> | *Non pris en charge ou documenté.*  <br/> |
| *Membre d’espace réservé*  <br/> | *Non pris en charge ou documenté.*  <br/> |
|[FreeMemory](iolkaccount-freememory.md) <br/> |Libère la mémoire allouée par **l’interface IOlkAccount** . |
| *Membre d’espace réservé*  <br/> | *Non pris en charge ou documenté.*  <br/> |
|[SaveChanges](iolkaccount-savechanges.md) <br/> |Valider les modifications apportées à l’objet de compte en écrivant dans le magasin du Registre. |
   
## <a name="properties"></a>Propriétés

|||
|:-----|:-----|
|[PROP_ACCT_DELIVERY_FOLDER](prop_acct_delivery_folder.md) <br/> |Représente l’ID d’entrée du dossier de remise par défaut du compte. |
|[PROP_ACCT_DELIVERY_STORE](prop_acct_delivery_store.md) <br/> |Représente l’ID d’entrée de la banque de remise par défaut pour le compte. |
|[PROP_ACCT_ID](prop_acct_id.md) <br/> |Renvoie l’identificateur de compte Outlook 2000 et versions antérieures de Outlook. |
|[PROP_ACCT_IS_EXCH](prop_acct_is_exch.md) <br/> |Cette valeur a la valeur True si le compte est un Exchange Microsoft. |
|[PROP_ACCT_MINI_UID](prop_acct_mini_uid.md) <br/> |Renvoie l’identificateur de compte dans les versions Outlook depuis Outlook 2002. |
|[PROP_ACCT_NAME](prop_acct_name.md) <br/> |Renvoie le nom du compte. |
|[PROP_ACCT_PREFERENCES_UID](prop_acct_preferences_uid.md) <br/> |Récupère l’identificateur unique (UID) de la section de profil qui stocke les préférences de compte. |
|[PROP_ACCT_SEND_STAMP](prop_acct_send_stamp.md) <br/> |Renvoie le cachet « envoyer » du compte. |
|[PROP_ACCT_SENTITEMS_EID](prop_acct_sentitems_eid.md) <br/> |Représente l’ID d’entrée du dossier par défaut pour les éléments envoyés pour le compte. |
|[PROP_ACCT_STAMP](prop_acct_stamp.md) <br/> |Renvoie le cachet du compte. |
|[PROP_ACCT_USER_DISPLAY_NAME](prop_acct_user_display_name.md) <br/> |Renvoie le nom complet de l’utilisateur. |
|[PROP_ACCT_USER_EMAIL_ADDR](prop_acct_user_email_addr.md) <br/> |Spécifie l’adresse e-mail du compte. |
|[PROP_MAPI_EMSMDB_UID](prop_mapi_emsmdb_uid.md) <br/> |Représente une structure [ACCT_BIN](acct_bin.md) qui contient l’UID d’un compte Exchange client. |
|[PROP_MAPI_IDENTITY_ENTRYID](prop_mapi_identity_entryid.md) <br/> |Récupère ou définit l’ID d’entrée du carnet d’adresses pour le compte. |
|[PROP_MAPI_TRANSPORT_FLAGS](prop_mapi_transport_flags.md) <br/> |Représente les paramètres de transport que Microsoft Outlook utilise pour déterminer les tâches de synchronisation nécessaires et pour désactiver les éléments d’interface utilisateur que le compte ne prend pas en charge. |
   
## <a name="remarks"></a>Remarques

Cette interface est renvoyée par **IOlkAccountManager::FindAccount** lors de la recherche d’un compte qui prend en charge **IOlkAccount** et **IOlkEnum::GetNext** lors de l’obtention du compte suivant dans un enumerator. 
  
## <a name="see-also"></a>Voir aussi

- [À propos de l'API de gestion de compte](about-the-account-management-api.md)  
- [Constantes (API de gestion des comptes)](constants-account-management-api.md)

