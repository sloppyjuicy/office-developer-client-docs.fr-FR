---
title: État de la suppression de téléchargement
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
localization_priority: Normal
ms.assetid: dee566ad-b46d-1015-4b0b-6c3313060142
description: 'Derni�re modification�: lundi 9 mars 2015'
ms.openlocfilehash: ff957e649d5de64c65ac169b3bc413ac7b6c9491
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19787426"
---
# <a name="upload-delete-status-state"></a>État de la suppression de téléchargement

  
  
**S’applique à**: Outlook 
  
 Cette rubrique décrit le déroulement de l’état de l’état de téléchargement supprimer de l’ordinateur d’état de réplication. 
  
## <a name="quick-info"></a>Informations rapides

|||
|:-----|:-----|
|Identificateur d’état :  <br/> |**LR_SYNC_UPLOAD_MESSAGE_DEL** <br/> |
|Structure de données associées :  <br/> |**[UPDEL](updel.md)** <br/> |
|À partir de cet état :  <br/> |[Télécharger l’état de la table](upload-table-state.md) <br/> |
|Avec cet état :  <br/> |Télécharger l’état de la table  <br/> |
   
> [!NOTE]
> L’ordinateur d’état de réplication est une machine à états déterministe. Un client au départ d’un état à l’autre doit renvoyer par la suite à l’ancienne à partir de ce dernier. 
  
## <a name="description"></a>Description

Cet état lance la mise à jour sur un serveur, les éléments Outlook (courrier, calendrier, contact, tâche, une note ou journal) qui ont été supprimées dans un dossier sur un magasin local spécifié dans un état de table de téléchargement précédent. Au cours de cet état, Outlook initialise les membres de la structure de données **UPDEL** associée avec des informations pour les éléments qui ont été supprimé ou déplacé à partir du dossier. 
  
Le client puis supprime les éléments spécifiés dans le dossier sur le serveur. Pour distinguer les éléments qui ont été déplacés au lieu d’avoir été supprimé, le client doit vérifier les membres *pupmov* identifiés dans la structure **UPDEL** . 
  
Lorsque cet état se termine, Outlook efface les informations internes indiquant que l’élément a été supprimé ; Par conséquent, Outlook n’aura plus un enregistrement de l’élément. Le magasin local renvoie l’état de la table de téléchargement.
  
## <a name="see-also"></a>Voir aussi



[À propos de l’API de réplication](about-the-replication-api.md)
  
[Constantes MAPI](mapi-constants.md)
  
[Sur l’ordinateur de l’état de réplication](about-the-replication-state-machine.md)
  
[SYNCSTATE](syncstate.md)

