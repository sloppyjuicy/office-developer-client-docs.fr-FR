---
title: Télécharger l'état de l'état de suppression
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
localization_priority: Normal
ms.assetid: dee566ad-b46d-1015-4b0b-6c3313060142
description: 'Derni�re modification�: lundi 9 mars 2015'
ms.openlocfilehash: dda9d23a572446a5fa79a9500eb69558b6e0debd
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32357707"
---
# <a name="upload-delete-status-state"></a>Télécharger l'état de l'état de suppression

  
  
**S’applique à** : Outlook 2013 | Outlook 2016 
  
 Cette rubrique décrit ce qui se passe lors de l'état de l'état de suppression du chargement de l'ordinateur d'état de réplication. 
  
## <a name="quick-info"></a>Informations rapides

|||
|:-----|:-----|
|Identificateur d'État:  <br/> |**LR_SYNC_UPLOAD_MESSAGE_DEL** <br/> |
|Structure de données associée:  <br/> |**[UPDEL](updel.md)** <br/> |
|À partir de cet État:  <br/> |[Charger l'état de la table](upload-table-state.md) <br/> |
|À cet État:  <br/> |Charger l'état de la table  <br/> |
   
> [!NOTE]
> L'ordinateur d'état de réplication est un ordinateur d'État déterministe. Un client qui se déplace d'un État à un autre doit finalement revenir au premier de ce dernier. 
  
## <a name="description"></a>Description

Cet État lance la mise à jour sur un serveur de ces éléments Outlook (courrier, calendrier, contact, tâche, note ou journal) qui ont été supprimés dans un dossier d'un magasin local spécifié dans un état de tableau de téléchargement précédent. Dans cet État, Outlook initialise les membres de la structure de données **UPDEL** associée avec les informations relatives aux éléments qui ont été supprimés ou déplacés du dossier. 
  
Le client supprime ensuite les éléments spécifiés dans le dossier sur le serveur. Pour distinguer les éléments qui ont été déplacés au lieu d'avoir été supprimés, le client doit vérifier les membres du *pupmov* identifiés dans la structure **UPDEL** . 
  
Lorsque cet État prend fin, Outlook efface les informations internes indiquant que l'élément a été supprimé; par conséquent, Outlook ne dispose plus de l'enregistrement de l'élément. Le magasin local revient à l'état de la table de chargement.
  
## <a name="see-also"></a>Voir aussi



[À propos de l’API de réplication](about-the-replication-api.md)
  
[Constantes MAPI](mapi-constants.md)
  
[À propos de la machine à états de réplication](about-the-replication-state-machine.md)
  
[SYNCSTATE](syncstate.md)

