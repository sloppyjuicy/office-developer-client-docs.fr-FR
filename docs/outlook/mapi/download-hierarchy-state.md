---
title: Télécharger l'état de la hiérarchie
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
localization_priority: Normal
ms.assetid: 8e0400ba-8530-e6ac-5de8-a62aeec5e10a
description: 'Derni�re modification�: lundi 9 mars 2015'
ms.openlocfilehash: 45535eef75c6fc091c02ec35b669675a51e4cf48
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32337008"
---
# <a name="download-hierarchy-state"></a>Télécharger l'état de la hiérarchie

  
  
**S’applique à** : Outlook 2013 | Outlook 2016 
  
 Cette rubrique décrit ce qui se passe lors de l'état de la hiérarchie de téléchargement de la machine à États de réplication. 
  
## <a name="quick-info"></a>Informations rapides

|||
|:-----|:-----|
|Identificateur d'État:  <br/> |**LR_SYNC_DOWNLOAD_HIERARCHY** <br/> |
|Structure de données associée:  <br/> |**[DNHIER](dnhier.md)** <br/> |
|À partir de cet État:  <br/> |[Synchronisation de l’état](synchronize-state.md) <br/> |
|À cet État:  <br/> |Synchronisation de l’état  <br/> |
   
> [!NOTE]
> L'ordinateur d'état de réplication est un ordinateur d'État déterministe. Un client qui se déplace d'un État à un autre doit finalement revenir au premier de ce dernier. 
  
## <a name="description"></a>Description

Cet État lance le téléchargement d'une hiérarchie d'arborescence de dossiers à partir d'un serveur vers le magasin local. 
  
Outlook initialise la structure de données **DNHIER** associée à l'aide d'un pointeur vers la hiérarchie. Le client télécharge la hiérarchie et insère de nouveaux dossiers ou des modifications apportées aux dossiers dans la banque locale. Le processus de téléchargement adopte la synchronisation des modifications incrémentielles Microsoft Exchange (ICS). Pour plus d’informations sur ICS, reportez-vous à [Critères d’évaluation ICS](https://msdn.microsoft.com/library/aa579252%28EXCHG.80%29.aspx).
  
Lorsque cet État se termine, le magasin local revient à l'État Synchronize.
  
## <a name="see-also"></a>Voir aussi



[À propos de l’API de réplication](about-the-replication-api.md)
  
[À propos de la machine à états de réplication](about-the-replication-state-machine.md)
  
[SYNCSTATE](syncstate.md)

