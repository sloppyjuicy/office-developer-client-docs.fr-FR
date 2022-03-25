---
title: PROP_SMTP_AUTH_METHOD
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: overview
ms.localizationpriority: medium
ms.assetid: 4202cafc-9011-406d-90b3-8dabf531c90b
description: Spécifie la méthode d’authentification à utiliser pour le compte SMTP.
ms.openlocfilehash: 6e2bf4b971e116ecfc0f88541425a48333f46791
ms.sourcegitcommit: a355e6b8898e9a1d66ca1bc808fe106e78dcb68f
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/22/2022
ms.locfileid: "63721534"
---
# <a name="prop_smtp_auth_method"></a>PROP_SMTP_AUTH_METHOD

Spécifie la méthode d’authentification à utiliser pour le compte SMTP.
  
## <a name="quick-info"></a>Informations rapides

|Propriété |Valeur |
|:-----|:-----|
|Identificateur :  <br/> |0x0208  <br/> |
|Type de propriété :  <br/> |PT_DWORD  <br/> |
|Balise de propriété :  <br/> |0x02080003  <br/> |
|Accès :  <br/> |Lecture seule  <br/> |
   
## <a name="remarks"></a>Remarques

La valeur est un masque de bits des constantes suivantes. Voir [constantes (API de gestion des comptes)](constants-account-management-api.md) pour leurs valeurs. 
  
- **SMTP_AUTH_SAME_AS_POP** signifie utiliser les mêmes informations d’identification que mon serveur de messagerie entrant, telles que fournies [par](prop_inet_user.md) les PROP_INET_USER et [PROP_INET_PASSWORD](prop_inet_password.md).
    
- **SMTP_AUTH_USER_PASS** signifie utiliser les informations d’identification fournies par les [PROP_SMTP_USER et](prop_smtp_user.md) [PROP_SMTP_PASSWORD](prop_smtp_password.md).
    
- **SMTP_AUTH_RECEIVE_BEFORE_SEND** demande à l’utilisateur de se connecter au serveur de courrier entrant avant d’envoyer des messages. 
    
## <a name="see-also"></a>Voir aussi

- [Gestion des téléchargements de messages pour les comptes POP3](managing-message-downloads-for-pop3-accounts.md)  
- [Constantes (API de gestion des comptes)](constants-account-management-api.md)

