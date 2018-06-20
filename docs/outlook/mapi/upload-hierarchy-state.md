---
title: Hiérarchie d’état du téléchargement
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
localization_priority: Normal
ms.assetid: e39c4198-4913-5e86-900a-32e5ba5d801c
description: 'Derni�re modification�: lundi 9 mars 2015'
ms.openlocfilehash: d53790cb51b660c781190cf41ca317c823a021e8
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19787432"
---
# <a name="upload-hierarchy-state"></a>Hiérarchie d’état du téléchargement

  
  
**S’applique à**: Outlook 
  
 Cette rubrique décrit le déroulement de l’état de la hiérarchie de téléchargement de l’ordinateur d’état de réplication. 
  
## <a name="quick-info"></a>Informations rapides

|||
|:-----|:-----|
|Identificateur d’état :  <br/> |**LR_SYNC_UPLOAD_HIERARCHY** <br/> |
|Structure de données associées :  <br/> |**[UPHIER](uphier.md)** <br/> |
|À partir de cet état :  <br/> |[État de synchronisation](synchronize-state.md) <br/> |
|Avec cet état :  <br/> |[Télécharger l’état du dossier](upload-folder-state.md), ou l’état de synchronisation  <br/> |
   
> [!NOTE]
> L’ordinateur d’état de réplication est une machine à états déterministe. Un client au départ d’un état à l’autre doit renvoyer par la suite à l’ancienne à partir de ce dernier. 
  
## <a name="description"></a>Description

Cet état lance téléchargement d’une hiérarchie de dossiers qui a été spécifiée dans une synchroniser l’état. Outlook détermine le nombre de dossiers qui ont été créés ou modifiés dans cette hiérarchie et initialise *cEnt* dans **UPHIER**. Outlook conserve également le nombre de dossiers téléchargés avec un autre membre *iEnt* . Pour chacun des dossiers *cEnt* télécharger, le client déplace le magasin local dans l’état du dossier téléchargement, renvoi à l’état de la hiérarchie de téléchargement lorsque le téléchargement du dossier se termine. 
  
Lorsque l’état de la hiérarchie de téléchargement se termine, la banque locale renvoie l’état de synchronisation.
  
## <a name="see-also"></a>Voir aussi



[À propos de l’API de réplication](about-the-replication-api.md)
  
[Constantes MAPI](mapi-constants.md)
  
[Sur l’ordinateur de l’état de réplication](about-the-replication-state-machine.md)
  
[SYNCSTATE](syncstate.md)

