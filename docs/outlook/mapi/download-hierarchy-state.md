---
title: Télécharger l’état de la hiérarchie
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
localization_priority: Normal
ms.assetid: 8e0400ba-8530-e6ac-5de8-a62aeec5e10a
description: Dernière modification le 9 mars 2015
ms.openlocfilehash: 45535eef75c6fc091c02ec35b669675a51e4cf48
ms.sourcegitcommit: ef717c65d8dd41ababffb01eafc443c79950aed4
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 10/04/2018
ms.locfileid: "25384856"
---
# <a name="download-hierarchy-state"></a>Télécharger l’état de la hiérarchie

  
  
**S’applique à** : Outlook 2013 | Outlook 2016 
  
 Cette rubrique décrit le déroulement de l’état de hiérarchie de téléchargement de l’ordinateur d’état de réplication. 
  
## <a name="quick-info"></a>Informations rapides

|||
|:-----|:-----|
|Identificateur d’état :  <br/> |**LR_SYNC_DOWNLOAD_HIERARCHY** <br/> |
|Structure de données associées :  <br/> |**[DNHIER](dnhier.md)** <br/> |
|À partir de cet état :  <br/> |[État de synchronisation](synchronize-state.md) <br/> |
|Avec cet état :  <br/> |État de synchronisation  <br/> |
   
> [!NOTE]
> L’ordinateur d’état de réplication est une machine à états déterministe. Un client au départ d’un état à l’autre doit renvoyer par la suite à l’ancienne à partir de ce dernier. 
  
## <a name="description"></a>Description

Cet état lance le téléchargement d’une hiérarchie d’arborescence de dossiers à partir d’un serveur dans le magasin local. 
  
Outlook initialise la structure de données **DNHIER** associée avec un pointeur vers la hiérarchie. Le client télécharge la hiérarchie et insérer des dossiers ou des modifications de dossiers dans le magasin local. Le processus de téléchargement adopte synchronisation modification incrémentielle (ICS) de Microsoft Exchange. Pour plus d’informations sur le partage de connexion Internet, voir [Critères d’évaluation de partage de connexion Internet](https://msdn.microsoft.com/library/aa579252%28EXCHG.80%29.aspx).
  
Lorsque cet état se termine, la banque locale renvoie l’état de synchronisation.
  
## <a name="see-also"></a>Voir aussi



[À propos de l’API de réplication](about-the-replication-api.md)
  
[À propos de la machine à états de réplication](about-the-replication-state-machine.md)
  
[SYNCSTATE](syncstate.md)

