---
title: PROP_SMTP_SECURE_CONNECTION
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: overview
ms.localizationpriority: medium
ms.assetid: e316a424-d789-4ce5-bcc6-263049f3659e
description: Spécifie le type de connexion chiffrée à utiliser pour un compte SMTP.
ms.openlocfilehash: eb267e71f63bd02dc0268e06f62b288f56e4db11
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/24/2021
ms.locfileid: "59592731"
---
# <a name="prop_smtp_secure_connection"></a>PROP_SMTP_SECURE_CONNECTION

Spécifie le type de connexion chiffrée à utiliser pour un compte SMTP.
  
## <a name="quick-info"></a>Informations rapides

|||
|:-----|:-----|
|Identificateur :  <br/> |0x020A  <br/> |
|Type de propriété :  <br/> |PT_DWORD  <br/> |
|Balise de propriété :  <br/> |0x020A0003  <br/> |
|Accès :  <br/> |Lecture seule  <br/> |
   
## <a name="remarks"></a>Remarques

La valeur peut être l’une des constantes suivantes. Voir [constantes (API de gestion des comptes)](constants-account-management-api.md) pour leurs valeurs. 
  
|**Constants**|**Description**|
|:-----|:-----|
|**ENCRYPT_CONN_NO_SECURITY** <br/> |N’utilisez aucun chiffrement.  <br/> |
|**ENCRYPT_CONN_SSL** <br/> |Utiliser le chiffrement SSL (Secure Socket Layer).  <br/> |
|**ENCRYPT_CONN_TLS** <br/> |Utiliser le protocole de chiffrement et d’authentification TLS (Transport Layer Security).  <br/> |
|**ENCRYPT_CONN_AUTO** <br/> |Détectez et utilisez automatiquement la méthode de chiffrement prise en charge par le serveur de messagerie.  <br/> |
   
## <a name="see-also"></a>Voir aussi

- [Gestion des téléchargements de messages pour les comptes POP3](managing-message-downloads-for-pop3-accounts.md) 
- [Constantes (API de gestion des comptes)](constants-account-management-api.md)

