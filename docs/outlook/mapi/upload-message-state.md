---
title: Charger l'état du message
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
localization_priority: Normal
ms.assetid: 7fdc1494-4f40-38bd-d363-144ca70e5906
description: Dernière modification le 9 mars 2015
ms.openlocfilehash: 61cda23557a501a2651385d192f1dc7432ef1cb5
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/28/2019
ms.locfileid: "33433800"
---
# <a name="upload-message-state"></a>Charger l'état du message

  
  
**S’applique à** : Outlook 2013 | Outlook 2016 
  
 Cette rubrique décrit ce qui se passe lors de l'état du message de téléchargement de la machine à États de réplication. 
  
## <a name="quick-info"></a>Informations rapides

|||
|:-----|:-----|
|Identificateur d'État:  <br/> |**LR_SYNC_UPLOAD_MESSAGE** <br/> |
|Structure de données associée:  <br/> |**[UPMSG](upmsg.md)** <br/> |
|À partir de cet État:  <br/> |[Charger l'état de la table](upload-table-state.md) <br/> |
|À cet État:  <br/> |Charger l'état de la table  <br/> |
   
> [!NOTE]
> L'ordinateur d'état de réplication est un ordinateur d'État déterministe. Un client qui se déplace d'un État à un autre doit finalement revenir au premier de ce dernier. 
  
## <a name="description"></a>Description

Cet État lance le téléchargement d'un élément Outlook (courrier, calendrier, contact, tâche, note ou journal) qui est nouveau ou qui a été déplacé vers le dossier actif ou qui a été modifié. Outlook initialise la structure de données correpsonding **UPMSG** avec les informations appropriées pour l'élément comme étant ajoutée, déplacée ou modifiée. 
  
Si l'élément a été ajouté ou déplacé, le client ajoute ou met à jour de manière appropriée l'élément sur le serveur. 
  
Si l'élément a été modifié, Outlook spécifie, dans la structure de données **UPMSG** , si les modifications figurent dans un en-tête de message (auquel cas l'élément est l'en-tête du message), dans les propriétés de l'élément ou dans l'élément lui-même qui nécessite un conflit. résolution. Le client met ensuite à jour l'élément sur le serveur. 
  
Une fois le téléchargement de l'élément terminé, Outlook note que le message a été téléchargé, afin qu'il ne soit pas traité lors d'un téléchargement ultérieur. Le magasin local revient à l'état de la table de chargement.
  
## <a name="see-also"></a>Voir aussi



[À propos de l’API de réplication](about-the-replication-api.md)
  
[Constantes MAPI](mapi-constants.md)
  
[À propos de la machine à états de réplication](about-the-replication-state-machine.md)
  
[SYNCSTATE](syncstate.md)

