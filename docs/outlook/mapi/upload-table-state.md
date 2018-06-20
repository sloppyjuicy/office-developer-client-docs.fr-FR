---
title: Table État du téléchargement
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
localization_priority: Normal
ms.assetid: fe167c90-c817-b627-0728-5c6393477c22
description: 'Derni�re modification�: lundi 9 mars 2015'
ms.openlocfilehash: 454df4dde2062d20855e4d9bceaf4400669693ac
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19787431"
---
# <a name="upload-table-state"></a>Table État du téléchargement

  
  
**S’applique à**: Outlook 
  
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
  
[Sur l’ordinateur de l’état de réplication](about-the-replication-state-machine.md)
  
[SYNCSTATE](syncstate.md)

