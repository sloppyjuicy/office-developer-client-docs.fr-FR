---
title: Charger l’état de la table
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
localization_priority: Normal
ms.assetid: fe167c90-c817-b627-0728-5c6393477c22
description: Dernière modification le 9 mars 2015
ms.openlocfilehash: a2a9b3f214c76b8ec965c84c4731e0dc57e83352
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/28/2019
ms.locfileid: "33405820"
---
# <a name="upload-table-state"></a>Charger l’état de la table

  
  
**S’applique à** : Outlook 2013 | Outlook 2016 
  
 Cette rubrique décrit ce qui se produit pendant l’état de la table de chargement de la machine à états de réplication. 
  
## <a name="quick-info"></a>Informations rapides

|||
|:-----|:-----|
|Identificateur d’état :  <br/> |**LR_SYNC_UPLOAD_TABLE** <br/> |
|Structure de données associée :  <br/> |**[UPTBL](uptbl.md)** <br/> |
|À partir de cet état :  <br/> |[Synchroniser l’état du contenu](synchronize-contents-state.md) <br/> |
|À cet état :  <br/> |[Télécharger l’état du message,](upload-message-state.md) [télécharger l’état de suppression](upload-delete-status-state.md)d’état, télécharger [l’état de](upload-read-status-state.md)lecture ou synchroniser l’état du contenu  <br/> |
   
> [!NOTE]
> La machine à états de réplication est une machine à états déterministe. Un client s’écartant d’un état à un autre doit finalement revenir au premier à partir du second. 
  
## <a name="description"></a>Description

Cet état lance le téléchargement du contenu d’un dossier qui a été spécifié dans un état de synchronisation de contenu précédent. Le dossier peut être un dossier de courrier, de calendrier, de contacts, de tâches, de notes ou de journal. Au cours de cet état, Outlook crée une liste d’éléments qui ont été ajoutés, modifiés, déplacés, supprimés ou marqués comme lus, et prépare les informations internes appropriées pour l’état du message de chargement, l’état de suppression de téléchargement ou l’état de lecture correspondant.
  
Lorsque cet état se termine, Outlook marque le dossier comme ayant son contenu synchronisé, afin que le contenu ne soit pas chargé à nouveau tant qu’une autre modification n’est pas apportée. La boutique locale revient à l’état de synchronisation du contenu.
  
## <a name="see-also"></a>Voir aussi



[À propos de l’API de réplication](about-the-replication-api.md)
  
[Constantes MAPI](mapi-constants.md)
  
[À propos de la machine à états de réplication](about-the-replication-state-machine.md)
  
[SYNCSTATE](syncstate.md)

