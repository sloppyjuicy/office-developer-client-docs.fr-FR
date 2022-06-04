---
title: Charger l’état de lecture
description: Décrit ce qui se passe pendant l’état de lecture du chargement de l’ordinateur d’état de réplication dans Outlook 2013 et Outlook 2016.
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.localizationpriority: medium
ms.assetid: 4d45574e-df87-8c44-4aa7-d41b38406f0a
ms.openlocfilehash: a17a884dd4fa4d7e54b58d7a3aa9310d19464986
ms.sourcegitcommit: eb83b72d14a07ac316c71e8208397d1c7046f6df
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/04/2022
ms.locfileid: "65894053"
---
# <a name="upload-read-status-state"></a>Charger l’état de lecture

  
  
**S’applique à** : Outlook 2013 | Outlook 2016 
  
 Cette rubrique décrit ce qui se passe lors du chargement de l’état de lecture de l’ordinateur d’état de réplication. 
  
## <a name="quick-info"></a>Informations rapides

|Propriété |Valeur |
|:-----|:-----|
|Identificateur d’état :  <br/> |**LR_SYNC_UPLOAD_MESSAGE_READ** <br/> |
|Structure de données associée :  <br/> |**[UPREAD](upread.md)** <br/> |
|À partir de cet état :  <br/> |[Charger l’état de la table](upload-table-state.md) <br/> |
|À cet état :  <br/> |Charger l’état de la table  <br/> |
   
> [!NOTE]
> L’ordinateur d’état de réplication est un ordinateur d’état déterministe. Un client qui part d’un état à un autre doit finalement revenir au premier d’un autre état. 
  
## <a name="description"></a>Description

Cet état lance le chargement de l’état de lecture des éléments d’un dossier spécifié dans un état de table de chargement précédent. Dans cet état, Outlook initialise la structure de données **UPREAD** associée avec des informations pour les éléments du dossier dont l’état de lecture a changé. Le client met ensuite à jour l’état de lecture de ces éléments sur le serveur comme étant lus ou non lus. 
  
Lorsque cet état se termine, Outlook efface les informations internes sur l’état de lecture de l’élément, ce qui empêche le chargement de l’état de lecture de l’élément. Le magasin local retourne à l’état de la table de chargement.
  
## <a name="see-also"></a>Voir aussi



[À propos de l’API de réplication](about-the-replication-api.md)
  
[Constantes MAPI](mapi-constants.md)
  
[À propos de la machine à états de réplication](about-the-replication-state-machine.md)
  
[SYNCSTATE](syncstate.md)

