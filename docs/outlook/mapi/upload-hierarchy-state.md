---
title: Charger l'état de la hiérarchie
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
localization_priority: Normal
ms.assetid: e39c4198-4913-5e86-900a-32e5ba5d801c
description: 'Derni�re modification�: lundi 9 mars 2015'
ms.openlocfilehash: f789f4d7bbaf585d0d80f2208c35313542dfc191
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32286314"
---
# <a name="upload-hierarchy-state"></a>Charger l'état de la hiérarchie

  
  
**S’applique à** : Outlook 2013 | Outlook 2016 
  
 Cette rubrique décrit ce qui se passe lors de l'état de la hiérarchie de téléchargement de la machine à États de réplication. 
  
## <a name="quick-info"></a>Informations rapides

|||
|:-----|:-----|
|Identificateur d'État:  <br/> |**LR_SYNC_UPLOAD_HIERARCHY** <br/> |
|Structure de données associée:  <br/> |**[UPHIER](uphier.md)** <br/> |
|À partir de cet État:  <br/> |[Synchronisation de l’état](synchronize-state.md) <br/> |
|À cet État:  <br/> |[Charger l'état du dossier](upload-folder-state.md)ou synchroniser l'État  <br/> |
   
> [!NOTE]
> L'ordinateur d'état de réplication est un ordinateur d'État déterministe. Un client qui fait passer un État à un autre doit finalement revenir au premier de ce dernier. 
  
## <a name="description"></a>Description

Cet État lance le téléchargement d'une hiérarchie d'arborescence de dossiers qui a été spécifiée dans un état de synchronisation précédent. Outlook détermine le nombre de dossiers qui ont été créés ou modifiés dans cette hiérarchie et qui initialisent le **** *pourcentage* dans la valeur de la valeur de. Outlook conserve également le nombre de dossiers téléchargés avec un autre membre *iEnt* . Pour télécharger chacun des dossiers *cents* , le client déplace la banque locale dans l'état du dossier de chargement, en retournant à l'état de la hiérarchie de chargement une fois le téléchargement du dossier terminé. 
  
Une fois l'état de la hiérarchie de téléchargement terminé, le magasin local revient à l'État Synchronize.
  
## <a name="see-also"></a>Voir aussi



[À propos de l’API de réplication](about-the-replication-api.md)
  
[Constantes MAPI](mapi-constants.md)
  
[À propos de la machine à états de réplication](about-the-replication-state-machine.md)
  
[SYNCSTATE](syncstate.md)

