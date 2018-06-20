---
title: PROP_POP_LEAVE_ON_SERVER
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: overview
localization_priority: Normal
ms.assetid: 22d7c1e8-48b9-4768-b4de-9a9f32a3aabb
description: Spécifie la conservation d’une copie d’un message sur le serveur pour un compte POP.
ms.openlocfilehash: 9f986ff60a5824ece0a8bb91619323b58ec8b87a
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19782816"
---
# <a name="proppopleaveonserver"></a>PROP_POP_LEAVE_ON_SERVER

Spécifie la conservation d’une copie d’un message sur le serveur pour un compte POP.
  
## <a name="quick-info"></a>Informations rapides

|||
|:-----|:-----|
|Identificateur :  <br/> |0 x 1000  <br/> |
|Type de propriété :  <br/> |PT_DWORD  <br/> |
|Balise de propriété :  <br/> |0x10000003  <br/> |
|Access :  <br/> |Lecture seule  <br/> |
   
## <a name="remarks"></a>Remarques

Le tableau suivant répertorie les valeurs possibles. Pour plus d’informations sur l’une des constantes, voir [constantes (gestion des comptes d’API)](constants-account-management-api.md) . 
  
|**Valeurs possibles**|**Description**|
|:-----|:-----|
|**LEAVE_ON_SERVER** <br/> |Laisse une copie du message sur le serveur POP après avoir téléchargé le message sur un périphérique.  <br/> |
|**REMOVE_AFTER** <br/> |Supprime le message à partir du serveur POP après le téléchargement pour un périphérique.  <br/> |
|**REMOVE_ON_NUKE** <br/> |Supprime le message à partir du serveur POP uniquement une fois que l’utilisateur supprime le message à partir du dossier éléments supprimés.  <br/> |
|**GET_REMOVE_AFTER_DAYS** ( _ul_)  <br/> |Obtient le nombre de jours après lequel le message sera supprimé du serveur POP.  <br/> |
|**SET_REMOVE_AFTER_DAYS** ( _jours_)  <br/> |Définit le nombre de jours après lequel le message sera supprimé du serveur POP.  <br/> |
   
## <a name="see-also"></a>Voir aussi

- [Message de la gestion des téléchargements pour les comptes POP3](managing-message-downloads-for-pop3-accounts.md) 
- [Constantes (API de gestion des comptes)](constants-account-management-api.md)

