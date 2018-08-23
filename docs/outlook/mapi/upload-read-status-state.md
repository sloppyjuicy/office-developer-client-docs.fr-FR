---
title: Télécharger l’état de lecture de statut
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
localization_priority: Normal
ms.assetid: 4d45574e-df87-8c44-4aa7-d41b38406f0a
description: Dernière modification le 09 mars 2015
ms.openlocfilehash: 41815a88fe1215d2a85a38592e04b0d0bbd43cc6
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/23/2018
ms.locfileid: "22573046"
---
# <a name="upload-read-status-state"></a>Télécharger l’état de lecture de statut

  
  
**S’applique à**: Outlook 2013 | Outlook 2016 
  
 Cette rubrique décrit ce qui se produit lors du téléchargement de lire l’état de l’ordinateur d’état de réplication. 
  
## <a name="quick-info"></a>Informations rapides

|||
|:-----|:-----|
|Identificateur d’état :  <br/> |**LR_SYNC_UPLOAD_MESSAGE_READ** <br/> |
|Structure de données associées :  <br/> |**[UPREAD](upread.md)** <br/> |
|À partir de cet état :  <br/> |[Télécharger l’état de la table](upload-table-state.md) <br/> |
|Avec cet état :  <br/> |Télécharger l’état de la table  <br/> |
   
> [!NOTE]
> L’ordinateur d’état de réplication est une machine à états déterministe. Un client au départ d’un état à l’autre doit renvoyer par la suite à l’ancienne à partir de ce dernier. 
  
## <a name="description"></a>Description

Cet état lance le téléchargement de l’état de lecture d’éléments dans un dossier spécifié dans un état de table de téléchargement précédent. Au cours de cet état, Outlook initialise la structure de données **UPREAD** associée avec des informations pour ces éléments dans le dossier dont l’état de lecture a été modifiée. Le client met à jour l’état de lecture de ces éléments sur le serveur comme étant lus ou non lus. 
  
Lorsque cet état se termine, Outlook efface les informations internes sur l’état de la lecture, empêche le téléchargement à nouveau l’état de lecture. Le magasin local renvoie l’état de la table de téléchargement.
  
## <a name="see-also"></a>Voir aussi



[À propos de l’API de réplication](about-the-replication-api.md)
  
[Constantes MAPI](mapi-constants.md)
  
[À propos de la machine à états de réplication](about-the-replication-state-machine.md)
  
[SYNCSTATE](syncstate.md)

