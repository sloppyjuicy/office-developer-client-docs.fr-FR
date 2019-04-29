---
title: Télécharger l'état de l'état de lecture
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
localization_priority: Normal
ms.assetid: 4d45574e-df87-8c44-4aa7-d41b38406f0a
description: Dernière modification le 9 mars 2015
ms.openlocfilehash: e8ad2acf019df3f07060c8e8c71a62afd3fca03c
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/28/2019
ms.locfileid: "33431539"
---
# <a name="upload-read-status-state"></a>Télécharger l'état de l'état de lecture

  
  
**S’applique à** : Outlook 2013 | Outlook 2016 
  
 Cette rubrique décrit ce qui se passe lors de l'état de lecture de téléchargement de l'ordinateur d'état de réplication. 
  
## <a name="quick-info"></a>Informations rapides

|||
|:-----|:-----|
|Identificateur d'État:  <br/> |**LR_SYNC_UPLOAD_MESSAGE_READ** <br/> |
|Structure de données associée:  <br/> |**[UPREAD](upread.md)** <br/> |
|À partir de cet État:  <br/> |[Charger l'état de la table](upload-table-state.md) <br/> |
|À cet État:  <br/> |Charger l'état de la table  <br/> |
   
> [!NOTE]
> L'ordinateur d'état de réplication est un ordinateur d'État déterministe. Un client qui se déplace d'un État à un autre doit finalement revenir au premier de ce dernier. 
  
## <a name="description"></a>Description

Cet État lance le téléchargement de l'état de lecture des éléments dans un dossier spécifié dans un état de tableau de téléchargement précédent. Dans cet État, Outlook initialise la structure de données de la **lecture** associée avec les informations de ces éléments dans le dossier dont le statut de lecture a changé. Le client met ensuite à jour l'état de lecture de ces éléments sur le serveur comme étant lus ou non lus. 
  
Lorsque cet État est terminé, Outlook efface les informations internes relatives à l'état de lecture de l'élément, ce qui empêche le chargement de l'état de lecture de l'élément. Le magasin local revient à l'état de la table de chargement.
  
## <a name="see-also"></a>Voir aussi



[À propos de l’API de réplication](about-the-replication-api.md)
  
[Constantes MAPI](mapi-constants.md)
  
[À propos de la machine à états de réplication](about-the-replication-state-machine.md)
  
[SYNCSTATE](syncstate.md)

