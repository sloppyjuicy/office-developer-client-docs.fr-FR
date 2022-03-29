---
title: Télécharger Supprimer l’état
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.localizationpriority: medium
ms.assetid: dee566ad-b46d-1015-4b0b-6c3313060142
description: Cette rubrique décrit ce qui se produit lors de l’état de suppression de téléchargement de la machine à états de réplication.
ms.openlocfilehash: ffcdbb44f2053278bc43c40403ef6cb2ec8665a7
ms.sourcegitcommit: 331e2bc18fb14cc9868d28ca29cb5eda85c8f154
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/25/2022
ms.locfileid: "64455481"
---
# <a name="upload-delete-status-state"></a>Télécharger Supprimer l’état

**S’applique à** : Outlook 2013 | Outlook 2016
  
 Cette rubrique décrit ce qui se produit lors de l’état de suppression de téléchargement de la machine à états de réplication.
  
## <a name="quick-info"></a>Informations rapides

|Propriété |Valeur |
|:-----|:-----|
|Identificateur d’état :  <br/> |**LR_SYNC_UPLOAD_MESSAGE_DEL** <br/> |
|Structure de données associée :  <br/> |**[UPDEL](updel.md)** <br/> |
|À partir de cet état :  <br/> |[Télécharger table](upload-table-state.md) <br/> |
|À cet état :  <br/> |Télécharger table  <br/> |

> [!NOTE]
> La machine à états de réplication est une machine à états déterministe. Un client s’écartant d’un état à un autre doit finalement revenir au premier à partir du second.
  
## <a name="description"></a>Description

Cet état lance la mise à jour sur un serveur des éléments Outlook (courrier, calendrier, contact, tâche, note ou journal) qui ont été supprimés dans un dossier d’une boutique locale spécifié dans un état de table de chargement précédent. Au cours de cet état, Outlook initialise les membres de la structure de données **UPDEL** associée avec les informations des éléments qui ont été supprimés ou déplacés du dossier.
  
Le client supprime ensuite les éléments spécifiés dans le dossier sur le serveur. Pour distinguer les éléments qui ont été déplacés au lieu d’avoir été supprimés, le client doit vérifier les *membresmov* identifiés dans la structure **UPDEL** .
  
Lorsque cet état se termine, Outlook efface les informations internes indiquant que l’élément a été supprimé ; par conséquent, Outlook n’aura plus d’enregistrement de l’élément. La boutique locale revient à l’état de la table de chargement.
  
## <a name="see-also"></a>Voir aussi

[À propos de l’API de réplication](about-the-replication-api.md)
  
[Constantes MAPI](mapi-constants.md)
  
[À propos de la machine à états de réplication](about-the-replication-state-machine.md)
  
[SYNCSTATE](syncstate.md)
