---
title: État de Table de téléchargement
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
localization_priority: Normal
ms.assetid: 5bcc8b0a-0ab7-6c3e-8334-9e83cf2882a7
description: 'Derni�re modification�: lundi 9 mars 2015'
ms.openlocfilehash: 6a29cc131b4fe352b067e343376b2b705e8e3244
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19783219"
---
# <a name="download-table-state"></a>État de Table de téléchargement

  
  
**S’applique à**: Outlook 
  
 Cette rubrique décrit le déroulement de l’état du tableau de téléchargement de l’ordinateur d’état de réplication. 
  
## <a name="quick-info"></a>Informations rapides

|||
|:-----|:-----|
|Identificateur d’état :  <br/> |**LR_SYNC_DOWNLOAD_TABLE** <br/> |
|Structure de données associées :  <br/> |**[DNTBL](dntbl.md)** <br/> |
|À partir de cet état :  <br/> |[Synchroniser le contenu d’un état](synchronize-contents-state.md) <br/> |
|Avec cet état :  <br/> |Synchroniser le contenu d’un état  <br/> |
   
> [!NOTE]
> L’ordinateur d’état de réplication est une machine à états déterministe. Un client au départ d’un état à l’autre doit renvoyer par la suite à l’ancienne à partir de ce dernier. 
  
## <a name="description"></a>Description

Cet état lance le téléchargement d’un dossier. Au cours de cet état, Outlook initialise la structure de données **DNTBL** associée avec des informations sur le dossier. Le client télécharge le contenu du dossier et du stockage local le dossier des mises à jour avec le nouveau contenu, les modifications ou les suppressions à partir du serveur. Le processus de téléchargement adopte synchronisation modification incrémentielle (ICS) de Microsoft Exchange. Pour plus d’informations sur le partage de connexion Internet, voir [Critères d’évaluation de partage de connexion Internet](http://msdn.microsoft.com/en-us/library/aa579252%28EXCHG.80%29.aspx).
  
Lorsque cet état se termine, la banque locale renvoie à l’état du contenu synchroniser.
  
## <a name="see-also"></a>Voir aussi



[À propos de l’API de réplication](about-the-replication-api.md)
  
[Constantes MAPI](mapi-constants.md)
  
[Sur l’ordinateur de l’état de réplication](about-the-replication-state-machine.md)
  
[SYNCSTATE](syncstate.md)

