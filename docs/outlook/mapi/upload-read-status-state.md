---
title: Télécharger état de lecture
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.localizationpriority: medium
ms.assetid: 4d45574e-df87-8c44-4aa7-d41b38406f0a
description: Dernière modification le 9 mars 2015
ms.openlocfilehash: 285f9b005c76d16aaeeedc0b095255c96bcc1680
ms.sourcegitcommit: a355e6b8898e9a1d66ca1bc808fe106e78dcb68f
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/22/2022
ms.locfileid: "63722045"
---
# <a name="upload-read-status-state"></a>Télécharger état de lecture

  
  
**S’applique à** : Outlook 2013 | Outlook 2016 
  
 Cette rubrique décrit ce qui se produit pendant l’état de lecture du chargement de la machine à états de réplication. 
  
## <a name="quick-info"></a>Informations rapides

|Propriété |Valeur |
|:-----|:-----|
|Identificateur d’état :  <br/> |**LR_SYNC_UPLOAD_MESSAGE_READ** <br/> |
|Structure de données associée :  <br/> |**[UPREAD](upread.md)** <br/> |
|À partir de cet état :  <br/> |[Télécharger table](upload-table-state.md) <br/> |
|À cet état :  <br/> |Télécharger table  <br/> |
   
> [!NOTE]
> La machine à états de réplication est une machine à états déterministe. Un client s’écartant d’un état à un autre doit finalement revenir au premier à partir du second. 
  
## <a name="description"></a>Description

Cet état initie le téléchargement de l’état de lecture des éléments dans un dossier spécifié dans un état de table de chargement précédent. Au cours de cet état, Outlook initialise la structure de données **UPREAD** associée avec les informations pour les éléments du dossier dont l’état de lecture a changé. Le client met ensuite à jour l’état de lecture de ces éléments sur le serveur comme étant lu ou non lu. 
  
Lorsque cet état se termine, Outlook les informations internes sur l’état de lecture de l’élément, ce qui empêche le téléchargement de l’état de lecture de l’élément à nouveau. La boutique locale revient à l’état de la table de chargement.
  
## <a name="see-also"></a>Voir aussi



[À propos de l’API de réplication](about-the-replication-api.md)
  
[Constantes MAPI](mapi-constants.md)
  
[À propos de la machine à états de réplication](about-the-replication-state-machine.md)
  
[SYNCSTATE](syncstate.md)

