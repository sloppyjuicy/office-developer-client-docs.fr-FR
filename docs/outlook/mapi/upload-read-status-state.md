---
title: État de la lecture de téléchargement
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
localization_priority: Normal
ms.assetid: 4d45574e-df87-8c44-4aa7-d41b38406f0a
description: 'Derni�re modification�: lundi 9 mars 2015'
ms.openlocfilehash: 172eaf47d305cf6e4d1ba54ceb4ac4b4feab80e8
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19787429"
---
# <a name="upload-read-status-state"></a>État de la lecture de téléchargement

  
  
**S’applique à**: Outlook 
  
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
  
[Sur l’ordinateur de l’état de réplication](about-the-replication-state-machine.md)
  
[SYNCSTATE](syncstate.md)

