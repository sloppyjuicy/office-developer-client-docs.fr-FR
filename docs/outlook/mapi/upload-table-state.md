---
title: Charger l'état de la table
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
localization_priority: Normal
ms.assetid: fe167c90-c817-b627-0728-5c6393477c22
description: 'Derni�re modification�: lundi 9 mars 2015'
ms.openlocfilehash: a2a9b3f214c76b8ec965c84c4731e0dc57e83352
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32342839"
---
# <a name="upload-table-state"></a>Charger l'état de la table

  
  
**S’applique à** : Outlook 2013 | Outlook 2016 
  
 Cette rubrique décrit ce qui se passe lors de l'état de la table de chargement de la machine à États de réplication. 
  
## <a name="quick-info"></a>Informations rapides

|||
|:-----|:-----|
|Identificateur d'État:  <br/> |**LR_SYNC_UPLOAD_TABLE** <br/> |
|Structure de données associée:  <br/> |**[UPTBL](uptbl.md)** <br/> |
|À partir de cet État:  <br/> |[Synchroniser l'état du contenu](synchronize-contents-state.md) <br/> |
|À cet État:  <br/> |[Télécharger](upload-message-state.md)l'état du message, télécharger l'état de l'état de la [suppression](upload-delete-status-state.md), télécharger l'état de l'état de [lecture](upload-read-status-state.md)ou synchroniser l'état du contenu  <br/> |
   
> [!NOTE]
> L'ordinateur d'état de réplication est un ordinateur d'État déterministe. Un client qui se déplace d'un État à un autre doit finalement revenir au premier de ce dernier. 
  
## <a name="description"></a>Description

Cet État lance le téléchargement du contenu d'un dossier qui a été spécifié dans un état de contenu de synchronisation précédent. Le dossier peut être un dossier courrier, calendrier, contacts, tâches, notes ou journal. Dans cet État, Outlook crée une liste des éléments qui ont été ajoutés, modifiés, déplacés, supprimés ou marqués comme lus, et prépare les informations internes appropriées pour l'état du message de téléchargement correspondant, l'état de la suppression du téléchargement ou le statut de lecture du téléchargement. Etat.
  
Lorsque cet État est terminé, Outlook marque le dossier comme étant synchronisé, de sorte que le contenu ne soit pas téléchargé à nouveau tant qu'une autre modification n'est pas effectuée. Le magasin local revient à l'État Synchronize content.
  
## <a name="see-also"></a>Voir aussi



[À propos de l’API de réplication](about-the-replication-api.md)
  
[Constantes MAPI](mapi-constants.md)
  
[À propos de la machine à états de réplication](about-the-replication-state-machine.md)
  
[SYNCSTATE](syncstate.md)

