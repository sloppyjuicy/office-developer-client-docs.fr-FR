---
title: PROP_SMTP_AUTH_METHOD
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: overview
localization_priority: Normal
ms.assetid: 4202cafc-9011-406d-90b3-8dabf531c90b
description: Spécifie la méthode d’authentification à utiliser pour le compte SMTP.
ms.openlocfilehash: 0c52f1eeca8f7ac3e63cccf712dd672c2247be6a
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19782829"
---
# <a name="propsmtpauthmethod"></a>PROP_SMTP_AUTH_METHOD

Spécifie la méthode d’authentification à utiliser pour le compte SMTP.
  
## <a name="quick-info"></a>Informations rapides

|||
|:-----|:-----|
|Identificateur :  <br/> |0x0208  <br/> |
|Type de propriété :  <br/> |PT_DWORD  <br/> |
|Balise de propriété :  <br/> |0x02080003  <br/> |
|Access :  <br/> |Lecture seule  <br/> |
   
## <a name="remarks"></a>Remarques

La valeur est un masque binaire composé des constantes suivantes. Voir [constantes (gestion des comptes d’API)](constants-account-management-api.md) pour leurs valeurs. 
  
- **SMTP_AUTH_SAME_AS_POP** consiste à utiliser les mêmes informations d’identification en tant que serveur de courrier entrant, fourni par [PROP_INET_USER](prop_inet_user.md) et [PROP_INET_PASSWORD](prop_inet_password.md).
    
- **SMTP_AUTH_USER_PASS** signifie utilisant les informations d’identification fournie par [PROP_SMTP_USER](prop_smtp_user.md) et [PROP_SMTP_PASSWORD](prop_smtp_password.md).
    
- **SMTP_AUTH_RECEIVE_BEFORE_SEND** signifie que la demande de l’utilisateur à se connecter au serveur de messagerie entrant avant l’envoi du courrier. 
    
## <a name="see-also"></a>Voir aussi

- [Message de la gestion des téléchargements pour les comptes POP3](managing-message-downloads-for-pop3-accounts.md)  
- [Constantes (API de gestion des comptes)](constants-account-management-api.md)

