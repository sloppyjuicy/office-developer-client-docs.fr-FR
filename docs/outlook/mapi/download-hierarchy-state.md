---
title: Télécharger l’état de la hiérarchie
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.localizationpriority: medium
ms.assetid: 8e0400ba-8530-e6ac-5de8-a62aeec5e10a
description: Dernière modification le 9 mars 2015
ms.openlocfilehash: 4875d4a511bb2e5a547b12fd8fc2c74c284c9af7
ms.sourcegitcommit: 241637561d21b7752ec690b5179e72b6703eaced
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/18/2022
ms.locfileid: "63634043"
---
# <a name="download-hierarchy-state"></a>Télécharger l’état de la hiérarchie

  
  
**S’applique à** : Outlook 2013 | Outlook 2016 
  
 Cette rubrique décrit ce qui se produit pendant l’état de la hiérarchie de téléchargement de la machine à états de réplication. 
  
## <a name="quick-info"></a>Informations rapides

|Propriété |Valeur |
|:-----|:-----|
|Identificateur d’état :  <br/> |**LR_SYNC_DOWNLOAD_HIERARCHY** <br/> |
|Structure de données associée :  <br/> |**[DNHIER](dnhier.md)** <br/> |
|À partir de cet état :  <br/> |[Synchronisation de l’état](synchronize-state.md) <br/> |
|À cet état :  <br/> |Synchronisation de l’état  <br/> |
   
> [!NOTE]
> La machine à états de réplication est une machine à états déterministe. Un client s’écartant d’un état à un autre doit finalement revenir au premier à partir du second. 
  
## <a name="description"></a>Description

Cet état lance le téléchargement d’une hiérarchie d’arborescences de dossiers à partir d’un serveur vers le magasin local. 
  
Outlook initialise la structure **de données DNHIER** associée avec un pointeur vers la hiérarchie. Le client télécharge la hiérarchie et insère de nouveaux dossiers ou modifications dans les dossiers de la boutique locale. Le processus de téléchargement adopte Microsoft Exchange synchronisation incrémentielle des changements (ICS). Pour plus d’informations sur ICS, reportez-vous à [Critères d’évaluation ICS](https://msdn.microsoft.com/library/aa579252%28EXCHG.80%29.aspx).
  
Lorsque cet état se termine, le magasin local revient à l’état de synchronisation.
  
## <a name="see-also"></a>Consultez aussi



[À propos de l’API de réplication](about-the-replication-api.md)
  
[À propos de la machine à états de réplication](about-the-replication-state-machine.md)
  
[SYNCSTATE](syncstate.md)

