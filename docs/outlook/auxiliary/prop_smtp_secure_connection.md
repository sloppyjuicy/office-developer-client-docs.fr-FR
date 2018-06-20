---
title: PROP_SMTP_SECURE_CONNECTION
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: overview
localization_priority: Normal
ms.assetid: e316a424-d789-4ce5-bcc6-263049f3659e
description: Spécifie le type de connexion chiffrée à utiliser pour un compte SMTP.
ms.openlocfilehash: e1c8c8dacf953407d4cbb114aa5ee0a4cdb6acf5
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19782825"
---
# <a name="propsmtpsecureconnection"></a>PROP_SMTP_SECURE_CONNECTION

Spécifie le type de connexion chiffrée à utiliser pour un compte SMTP.
  
## <a name="quick-info"></a>Informations rapides

|||
|:-----|:-----|
|Identificateur :  <br/> |0x020A  <br/> |
|Type de propriété :  <br/> |PT_DWORD  <br/> |
|Balise de propriété :  <br/> |0x020A0003  <br/> |
|Access :  <br/> |Lecture seule  <br/> |
   
## <a name="remarks"></a>Remarques

La valeur peut être une des constantes suivantes. Voir [constantes (gestion des comptes d’API)](constants-account-management-api.md) pour leurs valeurs. 
  
|**Constantes**|**Description**|
|:-----|:-----|
|**ENCRYPT_CONN_NO_SECURITY** <br/> |Ne pas utiliser un chiffrement.  <br/> |
|**ENCRYPT_CONN_SSL** <br/> |Utiliser le chiffrement de Secure Sockets Layer (SSL).  <br/> |
|**ENCRYPT_CONN_TLS** <br/> |Utiliser le protocole de chiffrement et d’authentification de sécurité TLS (Transport Layer).  <br/> |
|**ENCRYPT_CONN_AUTO** <br/> |Détecter automatiquement et utiliser la méthode de chiffrement pris en charge par le serveur de messagerie.  <br/> |
   
## <a name="see-also"></a>Voir aussi

- [Message de la gestion des téléchargements pour les comptes POP3](managing-message-downloads-for-pop3-accounts.md) 
- [Constantes (API de gestion des comptes)](constants-account-management-api.md)

