---
title: PROP_POP_LEAVE_ON_SERVER
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: overview
ms.localizationpriority: medium
ms.assetid: 22d7c1e8-48b9-4768-b4de-9a9f32a3aabb
description: Spécifie de laisser une copie d’un message sur le serveur pour un compte POP.
ms.openlocfilehash: 0dc90def351b08fda71154bd8e6784557c70706e
ms.sourcegitcommit: a355e6b8898e9a1d66ca1bc808fe106e78dcb68f
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/22/2022
ms.locfileid: "63724878"
---
# <a name="prop_pop_leave_on_server"></a>PROP_POP_LEAVE_ON_SERVER

Spécifie de laisser une copie d’un message sur le serveur pour un compte POP.
  
## <a name="quick-info"></a>Informations rapides

|Propriété |Valeur |
|:-----|:-----|
|Identificateur :  <br/> |0x1000  <br/> |
|Type de propriété :  <br/> |PT_DWORD  <br/> |
|Balise de propriété :  <br/> |0x10000003  <br/> |
|Accès :  <br/> |Lecture seule  <br/> |
   
## <a name="remarks"></a>Remarques

Le tableau suivant répertorie les valeurs possibles. Pour plus [d’informations sur les constantes, voir Constantes (API](constants-account-management-api.md) de gestion des comptes). 
  
|**Valeurs possibles**|**Description**|
|:-----|:-----|
|**LEAVE_ON_SERVER** <br/> |Laisse une copie du message sur le serveur POP après avoir téléchargé le message sur un appareil. |
|**REMOVE_AFTER** <br/> |Supprime le message du serveur POP après l’avoir téléchargé sur un appareil. |
|**REMOVE_ON_NUKE** <br/> |Supprime le message du serveur POP uniquement après que l’utilisateur l’a supprimé du dossier Éléments supprimés. |
|**GET_REMOVE_AFTER_DAYS**( _ul_)  <br/> |Obtient le nombre de jours après lesquels le message sera supprimé du serveur POP. |
|**SET_REMOVE_AFTER_DAYS**( _days_)  <br/> |Définit le nombre de jours après lesquels le message sera supprimé du serveur POP. |
   
## <a name="see-also"></a>Voir aussi

- [Gestion des téléchargements de messages pour les comptes POP3](managing-message-downloads-for-pop3-accounts.md) 
- [Constantes (API de gestion des comptes)](constants-account-management-api.md)

