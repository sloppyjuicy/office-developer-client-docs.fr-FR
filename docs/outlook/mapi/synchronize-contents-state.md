---
title: Synchroniser l'état du contenu
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
localization_priority: Normal
ms.assetid: 52216bc3-8cbd-3856-ea46-78f7d0dd66ff
description: Dernière modification le 9 mars 2015
ms.openlocfilehash: 3ebe1f5f48f9becdf01ea184c2b76fa2c8fa21e8
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/28/2019
ms.locfileid: "33438469"
---
# <a name="synchronize-contents-state"></a>Synchroniser l'état du contenu

  
  
**S’applique à** : Outlook 2013 | Outlook 2016 
  
 Cette rubrique décrit ce qui se passe lors de l'État synchroniser le contenu de la machine à États de réplication. 
  
## <a name="quick-info"></a>Informations rapides

|||
|:-----|:-----|
|Identificateur d'État:  <br/> |**LR_SYNC_CONTENTS** <br/> |
|Structure de données associée:  <br/> |**[SYNCCONT](synccont.md)** <br/> |
|À partir de cet État:  <br/> |[Synchronisation de l’état](synchronize-state.md) <br/> |
|À cet État:  <br/> |[Télécharger](download-table-state.md)l'état de la table, charger l'état de la [table](upload-table-state.md)ou synchroniser l'État  <br/> |
   
> [!NOTE]
> L'ordinateur d'état de réplication est un ordinateur d'État déterministe. Un client qui se déplace d'un État à un autre doit finalement revenir au premier de ce dernier. 
  
## <a name="description"></a>Description

Cet État lance l'un des deux processus de réplication suivants: le téléchargement du contenu de dossiers spécifiés dans un magasin local ou une synchronisation complète. Dans une synchronisation complète, le contenu des dossiers spécifiés est chargé en premier, puis téléchargé. Selon le *ulFlags* défini dans la structure de **[synchronisation](sync.md)** correspondante dans l'état de synchronisation précédent, Outlook initialise les membres [out] dans la structure **SYNCCONT** pour fournir des informations sur le contenu. 
  
Par le biais de la même structure **SYNCCONT** , le client obtient le nombre de dossiers dont le contenu doit être chargé ou téléchargé. Le client parcourt chacun de ces dossiers en déplacant le magasin local vers l'état de la table de chargement pour télécharger un dossier ou en déplacant le magasin local vers l'état de téléchargement de la table pour télécharger le dossier. 
  
En outre, le client obtient des ID d'entrée pour les dossiers qui nécessitent une réplication.
  
Lorsque cet État prend fin, Outlook nettoie ses informations internes. Le magasin local revient à l'État Synchronize.
  
## <a name="see-also"></a>Voir aussi



[À propos de l’API de réplication](about-the-replication-api.md)
  
[Constantes MAPI](mapi-constants.md)
  
[À propos de la machine à états de réplication](about-the-replication-state-machine.md)
  
[SYNCSTATE](syncstate.md)

