---
title: Propriétés (gestion des comptes d’API)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: overview
localization_priority: Normal
ms.assetid: a5204ddd-5af4-4dd8-bc83-af96ac390786
description: Cette section décrit les propriétés de l’API de gestion de compte.
ms.openlocfilehash: abf7422d941f581f66a118c35d2b6ff3c03e8b6b
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19782855"
---
# <a name="properties-account-management-api"></a>Propriétés (gestion des comptes d’API)

Cette section décrit les propriétés de l’API de gestion de compte.
  
|**Propriété**|**Description**|
|:-----|:-----|
|[PidTagNextSendAcct](pidtagnextsendacct.md) <br/> |Il s’agit de l’horodatage compte secondaire « Envoyer » pour le message.  <br/> |
|[PidTagPrimarySendAccount](pidtagprimarysendaccount.md) <br/> |Il s’agit de la marque de « envoyer » de compte principal pour un message.  <br/> |
|[PROP_ACCT_DELIVERY_FOLDER](prop_acct_delivery_folder.md) <br/> |Représente l’identificateur d’entrée du dossier de remise par défaut pour le compte.  <br/> |
|[PROP_ACCT_DELIVERY_STORE](prop_acct_delivery_store.md) <br/> |Représente l’identificateur d’entrée de la banque de remise par défaut pour le compte.  <br/> |
|[PROP_ACCT_ID](prop_acct_id.md) <br/> |Retourne un identificateur qui identifie de manière unique un compte dans le profil dans lequel le compte est créé.  <br/> |
|[PROP_ACCT_IS_EXCH](prop_acct_is_exch.md) <br/> |True si le compte est un compte Exchange.  <br/> |
|[PROP_ACCT_MINI_UID](prop_acct_mini_uid.md) <br/> |Retourne un identificateur de compte qui est unique pour les profils Outlook.  <br/> |
|[PROP_ACCT_NAME](prop_acct_name.md) <br/> |Cette propriété renvoie ou définit le nom du compte.  <br/> |
|[PROP_ACCT_PREFERENCES_UID](prop_acct_preferences_uid.md) <br/> |Récupère l’identificateur unique (UID) de la section profil qui stocke les préférences.  <br/> |
|[PROP_ACCT_SEND_STAMP](prop_acct_send_stamp.md) <br/> |Renvoie le tampon de « envoyer » de compte.  <br/> |
|[PROP_ACCT_SENTITEMS_EID](prop_acct_sentitems_eid.md) <br/> |Représente l’identificateur d’entrée du dossier par défaut pour les éléments envoyés pour le compte.  <br/> |
|[PROP_ACCT_STAMP](prop_acct_stamp.md) <br/> |Renvoie les informations de compte.  <br/> |
|[PROP_ACCT_USER_EMAIL_ADDR](prop_acct_user_email_addr.md) <br/> |Spécifie l’adresse de messagerie pour le compte.  <br/> |
|[PROP_ACCT_USER_DISPLAY_NAME](prop_acct_user_display_name.md) <br/> |Cette propriété renvoie ou définit le nom complet de l’utilisateur.  <br/> |
|[PROP_INET_PASSWORD](prop_inet_password.md) <br/> |Représente le mot de passe utilisateur pour une boîte aux lettres Internet général.  <br/> |
|[PROP_INET_PORT](prop_inet_port.md) <br/> |Représente le numéro de port pour une boîte aux lettres Internet général.  <br/> |
|[PROP_INET_SERVER](prop_inet_server.md) <br/> |Représente le nom du serveur d’une boîte aux lettres Internet général.  <br/> |
|[PROP_INET_SSL](prop_inet_ssl.md) <br/> |Spécifie si Secure Sockets Layer (SSL) doit être utilisé pour une boîte aux lettres Internet général.  <br/> |
|[PROP_INET_USE_SPA](prop_inet_use_spa.md) <br/> |Spécifie si le mot de passe sécurisé (SPA) doit être utilisé pour une boîte aux lettres Internet général.  <br/> |
|[PROP_INET_USER](prop_inet_user.md) <br/> |Représente le nom d’utilisateur pour une boîte aux lettres Internet général.  <br/> |
|[PROP_MAPI_EMSMDB_UID](prop_mapi_emsmdb_uid.md) <br/> |Représente une structure [ACCT_BIN](acct_bin.md) qui contient l’UID d’un compte Exchange.  <br/> |
|[PROP_MAPI_IDENTITY_ENTRYID](prop_mapi_identity_entryid.md) <br/> |Récupère ou définit l’ID d’entrée de carnet d’adresses pour le compte.  <br/> |
|[PROP_MAPI_TRANSPORT_FLAGS](prop_mapi_transport_flags.md) <br/> |Représente les paramètres de transport Outlook utilise pour déterminer les tâches de synchronisation et pour désactiver les éléments de l’interface utilisateur du compte ne prenant pas en charge.  <br/> |
|[PROP_POP_LEAVE_ON_SERVER](prop_pop_leave_on_server.md) <br/> |Spécifie la conservation d’une copie d’un message sur le serveur pour un compte POP.  <br/> |
|[PROP_SMTP_AUTH_METHOD](prop_smtp_auth_method.md) <br/> |Spécifie la méthode d’authentification à utiliser pour le compte SMTP.  <br/> |
|[PROP_SMTP_PASSWORD](prop_smtp_password.md) <br/> |Représente le mot de passe du compte SMTP.  <br/> |
|[PROP_SMTP_PORT](prop_smtp_port.md) <br/> |Représente le numéro de port du compte SMTP.  <br/> |
|[PROP_SMTP_SECURE_CONNECTION](prop_smtp_secure_connection.md) <br/> |Spécifie le type de connexion chiffrée à utiliser pour un compte SMTP.  <br/> |
|[PROP_SMTP_SERVER](prop_smtp_server.md) <br/> |Représente le nom du serveur du compte SMTP.  <br/> |
|[PROP_SMTP_SSL](prop_smtp_ssl.md) <br/> |Spécifie s’il faut utiliser le protocole Secure Sockets Layer (SSL) pour le compte SMTP.  <br/> |
|[PROP_SMTP_USE_AUTH](prop_smtp_use_auth.md) <br/> |Spécifie s’il faut utiliser l’authentification pour le compte SMTP.  <br/> |
|[PROP_SMTP_USE_SPA](prop_smtp_use_spa.md) <br/> |Spécifie s’il faut utiliser l’authentification par mot de passe sécurisé (SPA) pour le compte SMTP.  <br/> |
|[PROP_SMTP_USER](prop_smtp_user.md) <br/> |Représente le nom de compte SMTP de l’utilisateur.  <br/> |
   

