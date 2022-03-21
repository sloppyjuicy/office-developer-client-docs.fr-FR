---
title: Télécharger l’état du tableau
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.localizationpriority: medium
ms.assetid: 5bcc8b0a-0ab7-6c3e-8334-9e83cf2882a7
description: Dernière modification le 9 mars 2015
ms.openlocfilehash: a4a4c9ef6fc6063835b9418c2bb19ed283b16e43
ms.sourcegitcommit: 241637561d21b7752ec690b5179e72b6703eaced
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/18/2022
ms.locfileid: "63630369"
---
# <a name="download-table-state"></a>Télécharger l’état du tableau

  
  
**S’applique à** : Outlook 2013 | Outlook 2016 
  
 Cette rubrique décrit ce qui se produit pendant l’état de la table de téléchargement de la machine à états de réplication. 
  
## <a name="quick-info"></a>Informations rapides

|Propriété |Valeur |
|:-----|:-----|
|Identificateur d’état :  <br/> |**LR_SYNC_DOWNLOAD_TABLE** <br/> |
|Structure de données associée :  <br/> |**[DNTBL](dntbl.md)** <br/> |
|À partir de cet état :  <br/> |[Synchroniser l’état du contenu](synchronize-contents-state.md) <br/> |
|À cet état :  <br/> |Synchroniser l’état du contenu  <br/> |
   
> [!NOTE]
> La machine à états de réplication est une machine à états déterministe. Un client s’écartant d’un état à un autre doit finalement revenir au premier à partir du second. 
  
## <a name="description"></a>Description

Cet état lance le téléchargement d’un dossier. Au cours de cet état, Outlook initialise la structure de données **DNTBL** associée avec des informations sur le dossier. Le client télécharge le contenu du dossier et met à jour le dossier sur la boutique locale avec de nouveaux contenus, modifications ou suppressions à partir du serveur. Le processus de téléchargement adopte Microsoft Exchange synchronisation incrémentielle des changements (ICS). Pour plus d’informations sur ICS, reportez-vous à [Critères d’évaluation ICS](https://msdn.microsoft.com/library/aa579252%28EXCHG.80%29.aspx).
  
Lorsque cet état se termine, la boutique locale revient à l’état de synchronisation du contenu.
  
## <a name="see-also"></a>Consultez aussi



[À propos de l’API de réplication](about-the-replication-api.md)
  
[Constantes MAPI](mapi-constants.md)
  
[À propos de la machine à états de réplication](about-the-replication-state-machine.md)
  
[SYNCSTATE](syncstate.md)

