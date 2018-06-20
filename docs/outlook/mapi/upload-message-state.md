---
title: Message d’état du téléchargement
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
localization_priority: Normal
ms.assetid: 7fdc1494-4f40-38bd-d363-144ca70e5906
description: 'Derni�re modification�: lundi 9 mars 2015'
ms.openlocfilehash: 752756cbcf6c1ce487188dd4b9ba55eee6506cd4
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19787427"
---
# <a name="upload-message-state"></a>Message d’état du téléchargement

  
  
**S’applique à**: Outlook 
  
 Cette rubrique décrit le déroulement de l’état du message de téléchargement de l’ordinateur d’état de réplication. 
  
## <a name="quick-info"></a>Informations rapides

|||
|:-----|:-----|
|Identificateur d’état :  <br/> |**LR_SYNC_UPLOAD_MESSAGE** <br/> |
|Structure de données associées :  <br/> |**[UPMSG](upmsg.md)** <br/> |
|À partir de cet état :  <br/> |[Télécharger l’état de la table](upload-table-state.md) <br/> |
|Avec cet état :  <br/> |Télécharger l’état de la table  <br/> |
   
> [!NOTE]
> L’ordinateur d’état de réplication est une machine à états déterministe. Un client au départ d’un état à l’autre doit renvoyer par la suite à l’ancienne à partir de ce dernier. 
  
## <a name="description"></a>Description

Cet état lance le téléchargement d’un élément Outlook (courrier, calendrier, contact, tâche, une note ou journal) qui est nouveau ou a été déplacé vers le dossier actif, ou qui ont été modifiée. Outlook initialise la structure de données correpsonding **UPMSG** avec les informations appropriées pour l’élément comme étant ajouté, déplacé ou modifié. 
  
Si l’élément a été ajouté ou déplacé, le client puis correctement ajoute ou met à jour l’élément sur le serveur. 
  
Si l’élément a été modifié, Outlook plus spécifie dans la structure de données **UPMSG** si les modifications sont dans un en-tête de message (dans ce cas, l’élément est l’en-tête de message), dans les propriétés d’élément ou dans l’élément lui-même qui nécessite de conflit résolution. Le client met à jour l’élément sur le serveur. 
  
Lorsque le téléchargement de l’élément se termine, Outlook indique que le message a été téléchargé, afin qu’il ne sera pas traité dans un téléchargement suivant. Le magasin local renvoie l’état de la table de téléchargement.
  
## <a name="see-also"></a>Voir aussi



[À propos de l’API de réplication](about-the-replication-api.md)
  
[Constantes MAPI](mapi-constants.md)
  
[Sur l’ordinateur de l’état de réplication](about-the-replication-state-machine.md)
  
[SYNCSTATE](syncstate.md)

