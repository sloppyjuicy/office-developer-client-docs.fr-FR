---
title: Télécharger État de la hiérarchie
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.localizationpriority: medium
ms.assetid: e39c4198-4913-5e86-900a-32e5ba5d801c
description: Dernière modification le 9 mars 2015
ms.openlocfilehash: f765d62565e24437b477c46fe115c6b5427939cf
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/24/2021
ms.locfileid: "59619553"
---
# <a name="upload-hierarchy-state"></a>Télécharger État de la hiérarchie

  
  
**S’applique à** : Outlook 2013 | Outlook 2016 
  
 Cette rubrique décrit ce qui se produit pendant l’état de la hiérarchie de chargement de la machine à états de réplication. 
  
## <a name="quick-info"></a>Informations rapides

|||
|:-----|:-----|
|Identificateur d’état :  <br/> |**LR_SYNC_UPLOAD_HIERARCHY** <br/> |
|Structure de données associée :  <br/> |**[UPHIER](uphier.md)** <br/> |
|À partir de cet état :  <br/> |[Synchronisation de l’état](synchronize-state.md) <br/> |
|À cet état :  <br/> |[Télécharger’état du dossier](upload-folder-state.md)ou synchroniser l’état  <br/> |
   
> [!NOTE]
> La machine à états de réplication est une machine à états déterministe. Un client qui quitte un état vers un autre doit finalement revenir au premier à partir du second. 
  
## <a name="description"></a>Description

Cet état lance le téléchargement d’une hiérarchie d’arborescence de dossiers qui a été spécifiée dans un état de synchronisation précédent. Outlook détermine le nombre de dossiers qui ont été créés ou modifiés dans cette hiérarchie et initialise *cEnt* dans **UPHIER**. Outlook également le nombre de dossiers téléchargés avec un autre *iEnt membre.* Pour télécharger chacun des dossiers  *cEnt,*  le client place la boutique locale dans l’état du dossier de chargement, en revenir à l’état de hiérarchie de chargement une fois le chargement du dossier terminé. 
  
Lorsque l’état de la hiérarchie de chargement se termine, le magasin local revient à l’état de synchronisation.
  
## <a name="see-also"></a>Voir aussi



[À propos de l’API de réplication](about-the-replication-api.md)
  
[Constantes MAPI](mapi-constants.md)
  
[À propos de la machine à états de réplication](about-the-replication-state-machine.md)
  
[SYNCSTATE](syncstate.md)

