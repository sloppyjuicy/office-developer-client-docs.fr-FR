---
title: PROP_SMTP_AUTH_METHOD
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: overview
localization_priority: Normal
ms.assetid: 4202cafc-9011-406d-90b3-8dabf531c90b
description: Spécifie la méthode d’authentification à utiliser pour le compte SMTP.
ms.openlocfilehash: bb5adeb1fe73ed8b7ab69ca584215b44e1a9e4b7
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/28/2019
ms.locfileid: "33434640"
---
# <a name="prop_smtp_auth_method"></a>PROP_SMTP_AUTH_METHOD

Spécifie la méthode d’authentification à utiliser pour le compte SMTP.
  
## <a name="quick-info"></a>Informations rapides

|||
|:-----|:-----|
|Identificateur :  <br/> |0x0208  <br/> |
|Type de propriété :  <br/> |PT_DWORD  <br/> |
|Balise de propriété :  <br/> |0x02080003  <br/> |
|Accès :  <br/> |Lecture seule  <br/> |
   
## <a name="remarks"></a>Remarques

La valeur est un masque de bits des constantes suivantes. Voir [constantes (API de gestion des comptes)](constants-account-management-api.md) pour leurs valeurs. 
  
- **SMTP_AUTH_SAME_AS_POP** signifie utiliser les mêmes informations d’identification que mon serveur de messagerie entrant, comme fourni par les PROP_INET_USER [et](prop_inet_user.md) [PROP_INET_PASSWORD](prop_inet_password.md).
    
- **SMTP_AUTH_USER_PASS** signifie utiliser les informations d’identification fournies par les [PROP_SMTP_USER](prop_smtp_user.md) et [PROP_SMTP_PASSWORD](prop_smtp_password.md).
    
- **SMTP_AUTH_RECEIVE_BEFORE_SEND** demande à l’utilisateur de se connecter au serveur de messagerie entrant avant d’envoyer des messages. 
    
## <a name="see-also"></a>Voir aussi

- [Gestion des téléchargements de messages pour les comptes POP3](managing-message-downloads-for-pop3-accounts.md)  
- [Constantes (API de gestion des comptes)](constants-account-management-api.md)

