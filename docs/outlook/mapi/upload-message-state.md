---
title: Télécharger État du message
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.localizationpriority: medium
ms.assetid: 7fdc1494-4f40-38bd-d363-144ca70e5906
description: Dernière modification le 9 mars 2015
ms.openlocfilehash: f8ab2d0326e8948cb27f67376238caff50935ba2
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/24/2021
ms.locfileid: "59578409"
---
# <a name="upload-message-state"></a>Télécharger État du message

  
  
**S’applique à** : Outlook 2013 | Outlook 2016 
  
 Cette rubrique décrit ce qui se produit pendant le chargement de l’état du message de la machine à états de réplication. 
  
## <a name="quick-info"></a>Informations rapides

|||
|:-----|:-----|
|Identificateur d’état :  <br/> |**LR_SYNC_UPLOAD_MESSAGE** <br/> |
|Structure de données associée :  <br/> |**[UPMSG](upmsg.md)** <br/> |
|À partir de cet état :  <br/> |[Télécharger table](upload-table-state.md) <br/> |
|À cet état :  <br/> |Télécharger table  <br/> |
   
> [!NOTE]
> La machine à états de réplication est une machine à états déterministe. Un client s’écartant d’un état à un autre doit finalement revenir au premier à partir du second. 
  
## <a name="description"></a>Description

Cet état lance le téléchargement d’un élément Outlook (courrier, calendrier, contact, tâche, note ou journal) qui est nouveau ou qui a été déplacé vers le dossier actuel ou qui a été modifié. Outlook initialise la structure de données **UPMSG** corrélée avec les informations appropriées pour l’élément comme étant ajouté, déplacé ou modifié. 
  
Si l’élément a été ajouté ou déplacé, le client ajoute ou met à jour correctement l’élément sur le serveur. 
  
Si l’élément a été modifié, Outlook spécifie dans la structure de données **UPMSG** si les modifications sont dans un en-tête de message (auquel cas l’élément est l’en-tête du message), dans les propriétés de l’élément ou dans l’élément lui-même nécessitant une résolution de conflit. Le client met ensuite à jour l’élément sur le serveur. 
  
Lorsque le chargement de l’élément se termine, Outlook remarque que le message a été téléchargé, afin qu’il ne soit pas traitée dans un téléchargement ultérieur. La boutique locale revient à l’état de la table de chargement.
  
## <a name="see-also"></a>Voir aussi



[À propos de l’API de réplication](about-the-replication-api.md)
  
[Constantes MAPI](mapi-constants.md)
  
[À propos de la machine à états de réplication](about-the-replication-state-machine.md)
  
[SYNCSTATE](syncstate.md)

