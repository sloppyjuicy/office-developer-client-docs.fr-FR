---
title: Télécharger l’état de la hiérarchie
description: Cette rubrique décrit ce qui se passe pendant l’état de la hiérarchie de téléchargement de l’ordinateur d’état de réplication.
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.localizationpriority: medium
ms.assetid: 8e0400ba-8530-e6ac-5de8-a62aeec5e10a
ms.openlocfilehash: 9913e49506a8d521ad5748ce30e385b6273c2568
ms.sourcegitcommit: f872848fbeb5b2353179ad4bf4eab23f61f87666
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/01/2022
ms.locfileid: "65816485"
---
# <a name="download-hierarchy-state"></a>Télécharger l’état de la hiérarchie

  
  
**S’applique à** : Outlook 2013 | Outlook 2016 
  
 Cette rubrique décrit ce qui se passe pendant l’état de la hiérarchie de téléchargement de l’ordinateur d’état de réplication. 
  
## <a name="quick-info"></a>Informations rapides

|Propriété |Valeur |
|:-----|:-----|
|Identificateur d’état :  <br/> |**LR_SYNC_DOWNLOAD_HIERARCHY** <br/> |
|Structure de données associée :  <br/> |**[DNHIER](dnhier.md)** <br/> |
|À partir de cet état :  <br/> |[Synchronisation de l’état](synchronize-state.md) <br/> |
|À cet état :  <br/> |Synchronisation de l’état  <br/> |
   
> [!NOTE]
> L’ordinateur d’état de réplication est un ordinateur d’état déterministe. Un client qui part d’un état à un autre doit finalement revenir au premier d’un autre état. 
  
## <a name="description"></a>Description

Cet état lance le téléchargement d’une arborescence de dossiers à partir d’un serveur vers le magasin local. 
  
Outlook initialise la structure de données **DNHIER** associée avec un pointeur vers la hiérarchie. Le client télécharge la hiérarchie et insère de nouveaux dossiers ou modifications dans les dossiers du magasin local. Le processus de téléchargement adopte microsoft Exchange synchronisation incrémentielle des modifications (ICS). Pour plus d’informations sur ICS, reportez-vous à [Critères d’évaluation ICS](https://msdn.microsoft.com/library/aa579252%28EXCHG.80%29.aspx).
  
Lorsque cet état se termine, le magasin local revient à l’état de synchronisation.
  
## <a name="see-also"></a>Voir aussi



[À propos de l’API de réplication](about-the-replication-api.md)
  
[À propos de la machine à états de réplication](about-the-replication-state-machine.md)
  
[SYNCSTATE](syncstate.md)

