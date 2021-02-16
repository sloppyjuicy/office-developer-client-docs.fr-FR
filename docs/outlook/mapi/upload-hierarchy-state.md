---
title: Charger l’état de la hiérarchie
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
localization_priority: Normal
ms.assetid: e39c4198-4913-5e86-900a-32e5ba5d801c
description: Dernière modification le 9 mars 2015
ms.openlocfilehash: f789f4d7bbaf585d0d80f2208c35313542dfc191
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/28/2019
ms.locfileid: "33415424"
---
# <a name="upload-hierarchy-state"></a>Charger l’état de la hiérarchie

  
  
**S’applique à** : Outlook 2013 | Outlook 2016 
  
 Cette rubrique décrit ce qui se produit pendant l’état de la hiérarchie de chargement de la machine à états de réplication. 
  
## <a name="quick-info"></a>Informations rapides

|||
|:-----|:-----|
|Identificateur d’état :  <br/> |**LR_SYNC_UPLOAD_HIERARCHY** <br/> |
|Structure de données associée :  <br/> |**[UPHIER](uphier.md)** <br/> |
|À partir de cet état :  <br/> |[Synchronisation de l’état](synchronize-state.md) <br/> |
|À cet état :  <br/> |[Charger l’état du](upload-folder-state.md)dossier ou synchroniser l’état  <br/> |
   
> [!NOTE]
> La machine à états de réplication est une machine à états déterministe. Un client qui quitte un état vers un autre doit finalement revenir au premier à partir du second. 
  
## <a name="description"></a>Description

Cet état lance le téléchargement d’une hiérarchie d’arborescence de dossiers qui a été spécifiée dans un état de synchronisation précédent. Outlook détermine le nombre de dossiers qui ont été créés ou modifiés dans cette hiérarchie et initialise  *cEnt*  dans **UPHIER**. Outlook conserve également le nombre de dossiers téléchargés avec un autre *iEnt membre.* Pour télécharger chacun des dossiers  *cEnt,*  le client place la boutique locale dans l’état du dossier de chargement, en revenir à l’état de hiérarchie de chargement une fois le chargement du dossier terminé. 
  
Lorsque l’état de la hiérarchie de chargement se termine, le magasin local revient à l’état de synchronisation.
  
## <a name="see-also"></a>Voir aussi



[À propos de l’API de réplication](about-the-replication-api.md)
  
[Constantes MAPI](mapi-constants.md)
  
[À propos de la machine à états de réplication](about-the-replication-state-machine.md)
  
[SYNCSTATE](syncstate.md)

