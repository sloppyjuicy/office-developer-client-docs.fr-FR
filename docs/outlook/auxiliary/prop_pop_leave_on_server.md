---
title: PROP_POP_LEAVE_ON_SERVER
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: overview
localization_priority: Normal
ms.assetid: 22d7c1e8-48b9-4768-b4de-9a9f32a3aabb
description: Spécifie de laisser une copie d’un message sur le serveur pour un compte POP.
ms.openlocfilehash: e1bbddea0f10c07d630676960d1b330f6055e137
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/28/2019
ms.locfileid: "33410944"
---
# <a name="prop_pop_leave_on_server"></a>PROP_POP_LEAVE_ON_SERVER

Spécifie de laisser une copie d’un message sur le serveur pour un compte POP.
  
## <a name="quick-info"></a>Informations rapides

|||
|:-----|:-----|
|Identificateur :  <br/> |0x1000  <br/> |
|Type de propriété :  <br/> |PT_DWORD  <br/> |
|Balise de propriété :  <br/> |0x10000003  <br/> |
|Accès :  <br/> |Lecture seule  <br/> |
   
## <a name="remarks"></a>Remarques

Le tableau suivant répertorie les valeurs possibles. Pour plus d’informations sur les [constantes, voir Constantes (API](constants-account-management-api.md) de gestion des comptes). 
  
|**Valeurs possibles**|**Description**|
|:-----|:-----|
|**LEAVE_ON_SERVER** <br/> |Laisse une copie du message sur le serveur POP après avoir téléchargé le message sur un appareil.  <br/> |
|**REMOVE_AFTER** <br/> |Supprime le message du serveur POP après l’avoir téléchargé sur un appareil.  <br/> |
|**REMOVE_ON_NUKE** <br/> |Supprime le message du serveur POP uniquement après que l’utilisateur a supprimé le message du dossier Éléments supprimés.  <br/> |
|**GET_REMOVE_AFTER_DAYS**( _ul_)  <br/> |Obtient le nombre de jours après lesquels le message sera supprimé du serveur POP.  <br/> |
|**SET_REMOVE_AFTER_DAYS**( _jours_)  <br/> |Définit le nombre de jours après lesquels le message sera supprimé du serveur POP.  <br/> |
   
## <a name="see-also"></a>Voir aussi

- [Gestion des téléchargements de messages pour les comptes POP3](managing-message-downloads-for-pop3-accounts.md) 
- [Constantes (API de gestion des comptes)](constants-account-management-api.md)

