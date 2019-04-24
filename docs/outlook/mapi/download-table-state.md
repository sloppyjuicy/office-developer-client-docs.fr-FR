---
title: Télécharger l'état de la table
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
localization_priority: Normal
ms.assetid: 5bcc8b0a-0ab7-6c3e-8334-9e83cf2882a7
description: 'Derni�re modification�: lundi 9 mars 2015'
ms.openlocfilehash: 7451d159ef97ef9d8160b386ec5bf88fb388706e
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32338338"
---
# <a name="download-table-state"></a>Télécharger l'état de la table

  
  
**S’applique à** : Outlook 2013 | Outlook 2016 
  
 Cette rubrique décrit ce qui se passe lors de l'état de la table de téléchargement de la machine à États de réplication. 
  
## <a name="quick-info"></a>Informations rapides

|||
|:-----|:-----|
|Identificateur d'État:  <br/> |**LR_SYNC_DOWNLOAD_TABLE** <br/> |
|Structure de données associée:  <br/> |**[DNTBL](dntbl.md)** <br/> |
|À partir de cet État:  <br/> |[Synchroniser l'état du contenu](synchronize-contents-state.md) <br/> |
|À cet État:  <br/> |Synchroniser l'état du contenu  <br/> |
   
> [!NOTE]
> L'ordinateur d'état de réplication est un ordinateur d'État déterministe. Un client qui se déplace d'un État à un autre doit finalement revenir au premier de ce dernier. 
  
## <a name="description"></a>Description

Cet État lance le téléchargement d'un dossier. Dans cet État, Outlook initialise la structure de données **DNTBL** associée avec des informations sur le dossier. Le client télécharge le contenu du dossier et met à jour le dossier sur le magasin local avec le nouveau contenu, les modifications ou les suppressions à partir du serveur. Le processus de téléchargement adopte la synchronisation des modifications incrémentielles Microsoft Exchange (ICS). Pour plus d’informations sur ICS, reportez-vous à [Critères d’évaluation ICS](https://msdn.microsoft.com/library/aa579252%28EXCHG.80%29.aspx).
  
Lorsque cet État se termine, le magasin local revient à l'État Synchronize content.
  
## <a name="see-also"></a>Voir aussi



[À propos de l’API de réplication](about-the-replication-api.md)
  
[Constantes MAPI](mapi-constants.md)
  
[À propos de la machine à états de réplication](about-the-replication-state-machine.md)
  
[SYNCSTATE](syncstate.md)

