---
title: Télécharger message
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.localizationpriority: medium
ms.assetid: 7fdc1494-4f40-38bd-d363-144ca70e5906
description: Cette rubrique décrit ce qui se produit pendant le chargement de l’état du message de la machine à états de réplication.
ms.openlocfilehash: 6da06208f4a64f03173990f97788de7fd11781a9
ms.sourcegitcommit: 331e2bc18fb14cc9868d28ca29cb5eda85c8f154
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/25/2022
ms.locfileid: "64455194"
---
# <a name="upload-message-state"></a>Télécharger message

  
  
**S’applique à** : Outlook 2013 | Outlook 2016 
  
 Cette rubrique décrit ce qui se produit pendant le chargement de l’état du message de la machine à états de réplication. 
  
## <a name="quick-info"></a>Informations rapides

|Propriété |Valeur |
|:-----|:-----|
|Identificateur d’état :  <br/> |**LR_SYNC_UPLOAD_MESSAGE** <br/> |
|Structure de données associée :  <br/> |**[UPMSG](upmsg.md)** <br/> |
|À partir de cet état :  <br/> |[Télécharger table](upload-table-state.md) <br/> |
|À cet état :  <br/> |Télécharger table  <br/> |
   
> [!NOTE]
> La machine à états de réplication est une machine à états déterministe. Un client s’écartant d’un état à un autre doit finalement revenir au premier à partir du second. 
  
## <a name="description"></a>Description

Cet état lance le téléchargement d’un élément Outlook (courrier, calendrier, contact, tâche, note ou journal) qui est nouveau ou qui a été déplacé vers le dossier actuel ou qui a été modifié. Outlook initialise la structure de données **UPMSG** corrélée avec les informations appropriées pour l’élément comme ajouté, déplacé ou modifié. 
  
Si l’élément a été ajouté ou déplacé, le client ajoute ou met à jour correctement l’élément sur le serveur. 
  
Si l’élément a été modifié, Outlook spécifie dans la structure de données **UPMSG** si les modifications sont dans un en-tête de message (auquel cas l’élément est l’en-tête du message), dans les propriétés de l’élément ou dans l’élément lui-même nécessitant une résolution de conflit. Le client met ensuite à jour l’élément sur le serveur. 
  
Lorsque le chargement de l’élément se termine, Outlook remarque que le message a été téléchargé, afin qu’il ne soit pas traitée lors d’un téléchargement ultérieur. La boutique locale revient à l’état de la table de chargement.
  
## <a name="see-also"></a>Voir aussi



[À propos de l’API de réplication](about-the-replication-api.md)
  
[Constantes MAPI](mapi-constants.md)
  
[À propos de la machine à états de réplication](about-the-replication-state-machine.md)
  
[SYNCSTATE](syncstate.md)

