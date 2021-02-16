---
title: PROP_SMTP_SECURE_CONNECTION
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: overview
localization_priority: Normal
ms.assetid: e316a424-d789-4ce5-bcc6-263049f3659e
description: Spécifie le type de connexion chiffrée à utiliser pour un compte SMTP.
ms.openlocfilehash: 67eae5c9c5ca1b7f664ceaac0463ef3f3c9a291a
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/28/2019
ms.locfileid: "33421283"
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

