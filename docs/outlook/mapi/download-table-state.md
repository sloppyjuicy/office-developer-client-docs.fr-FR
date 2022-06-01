---
title: Télécharger l’état de la table
description: Cette rubrique décrit ce qui se passe pendant l’état de la table de téléchargement de l’ordinateur d’état de réplication.
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.localizationpriority: medium
ms.assetid: 5bcc8b0a-0ab7-6c3e-8334-9e83cf2882a7
ms.openlocfilehash: 0875a3d73b3b318e81cb94344cad569f5e47dd33
ms.sourcegitcommit: f872848fbeb5b2353179ad4bf4eab23f61f87666
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/01/2022
ms.locfileid: "65815883"
---
# <a name="download-table-state"></a>Télécharger l’état de la table

  
  
**S’applique à** : Outlook 2013 | Outlook 2016 
  
 Cette rubrique décrit ce qui se passe pendant l’état de la table de téléchargement de l’ordinateur d’état de réplication. 
  
## <a name="quick-info"></a>Informations rapides

|Propriété |Valeur |
|:-----|:-----|
|Identificateur d’état :  <br/> |**LR_SYNC_DOWNLOAD_TABLE** <br/> |
|Structure de données associée :  <br/> |**[DNTBL](dntbl.md)** <br/> |
|À partir de cet état :  <br/> |[Synchroniser l’état du contenu](synchronize-contents-state.md) <br/> |
|À cet état :  <br/> |Synchroniser l’état du contenu  <br/> |
   
> [!NOTE]
> L’ordinateur d’état de réplication est un ordinateur d’état déterministe. Un client qui part d’un état à un autre doit finalement revenir au premier d’un autre état. 
  
## <a name="description"></a>Description

Cet état lance le téléchargement d’un dossier. Pendant cet état, Outlook initialise la structure de données **DNTBL** associée avec des informations sur le dossier. Le client télécharge le contenu du dossier et met à jour le dossier sur le magasin local avec de nouveaux contenus, modifications ou suppressions à partir du serveur. Le processus de téléchargement adopte microsoft Exchange synchronisation incrémentielle des modifications (ICS). Pour plus d’informations sur ICS, reportez-vous à [Critères d’évaluation ICS](https://msdn.microsoft.com/library/aa579252%28EXCHG.80%29.aspx).
  
Lorsque cet état se termine, le magasin local retourne à l’état de synchronisation du contenu.
  
## <a name="see-also"></a>Voir aussi



[À propos de l’API de réplication](about-the-replication-api.md)
  
[Constantes MAPI](mapi-constants.md)
  
[À propos de la machine à états de réplication](about-the-replication-state-machine.md)
  
[SYNCSTATE](syncstate.md)

