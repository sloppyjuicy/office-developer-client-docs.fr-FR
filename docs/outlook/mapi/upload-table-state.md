---
title: Télécharger l’état de la table
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
localization_priority: Normal
ms.assetid: fe167c90-c817-b627-0728-5c6393477c22
description: Dernière modification le 09 mars 2015
ms.openlocfilehash: bd54c30e8701a13637235e28ddcfef4c21d10a2b
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/23/2018
ms.locfileid: "22576980"
---
# <a name="upload-table-state"></a>Télécharger l’état de la table

  
  
**S’applique à**: Outlook 2013 | Outlook 2016 
  
 Cette rubrique décrit le déroulement de l’état du tableau de téléchargement de l’ordinateur d’état de réplication. 
  
## <a name="quick-info"></a>Informations rapides

|||
|:-----|:-----|
|Identificateur d’état :  <br/> |**LR_SYNC_UPLOAD_TABLE** <br/> |
|Structure de données associées :  <br/> |**[UPTBL](uptbl.md)** <br/> |
|À partir de cet état :  <br/> |[Synchroniser le contenu d’un état](synchronize-contents-state.md) <br/> |
|Avec cet état :  <br/> |[Télécharger l’état du message](upload-message-state.md), [téléchargement supprimer état](upload-delete-status-state.md), [lire l’état de téléchargement](upload-read-status-state.md), ou de synchroniser le contenu d’un état  <br/> |
   
> [!NOTE]
> L’ordinateur d’état de réplication est une machine à états déterministe. Un client au départ d’un état à l’autre doit renvoyer par la suite à l’ancienne à partir de ce dernier. 
  
## <a name="description"></a>Description

Cet état lance le téléchargement du contenu d’un dossier qui a été spécifié dans un état de contenu précédente synchroniser. Le dossier peut être un dossier de courrier, calendrier, contacts, tâches, notes ou journal. Au cours de cet état, Outlook crée une liste d’éléments qui ont été ajoutées, modifiées, déplacé, supprimé ou marqués comme étant en lecture et prépare les informations appropriées internes de l’état du message de téléchargement correspondant, télécharger l’état de la suppression ou charger l’état de lecture état.
  
Lorsque cet état se termine, Outlook marque le dossier comme ayant son contenu synchronisées, afin que le contenu n’est téléchargé à nouveau jusqu'à ce qu’un autre est modifiée. Le magasin local renvoie à l’état du contenu synchroniser.
  
## <a name="see-also"></a>Voir aussi



[À propos de l’API de réplication](about-the-replication-api.md)
  
[Constantes MAPI](mapi-constants.md)
  
[À propos de la machine à états de réplication](about-the-replication-state-machine.md)
  
[SYNCSTATE](syncstate.md)

