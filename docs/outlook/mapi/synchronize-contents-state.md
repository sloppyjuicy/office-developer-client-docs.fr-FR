---
title: Synchroniser l’état du contenu
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
localization_priority: Normal
ms.assetid: 52216bc3-8cbd-3856-ea46-78f7d0dd66ff
description: Dernière modification le 09 mars 2015
ms.openlocfilehash: a2bdbeb39cce1e62569f364875c3828cdd530c63
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/23/2018
ms.locfileid: "22577246"
---
# <a name="synchronize-contents-state"></a>Synchroniser l’état du contenu

  
  
**S’applique à**: Outlook 2013 | Outlook 2016 
  
 Cette rubrique décrit le déroulement de l’état du contenu de synchroniser de l’ordinateur d’état de réplication. 
  
## <a name="quick-info"></a>Informations rapides

|||
|:-----|:-----|
|Identificateur d’état :  <br/> |**LR_SYNC_CONTENTS** <br/> |
|Structure de données associées :  <br/> |**[SYNCCONT](synccont.md)** <br/> |
|À partir de cet état :  <br/> |[État de synchronisation](synchronize-state.md) <br/> |
|Avec cet état :  <br/> |[Table état du téléchargement](download-table-state.md), [Téléchargez l’état de la table](upload-table-state.md), ou l’état de synchronisation  <br/> |
   
> [!NOTE]
> L’ordinateur d’état de réplication est une machine à états déterministe. Un client au départ d’un état à l’autre doit renvoyer par la suite à l’ancienne à partir de ce dernier. 
  
## <a name="description"></a>Description

Cet état lance un des deux processus de réplication : télécharger le contenu de spécifiées dossiers dans un magasin local ou une synchronisation complète. Dans une synchronisation complète, pour chacun des dossiers spécifiés, le contenu est téléchargées en premier et puis téléchargé. Selon *ulFlags* définie dans la structure de **[synchronisation](sync.md)** correspondante dans le précédent synchroniser état, Outlook initialise [out] les membres de la structure **SYNCCONT** pour fournir des informations sur le contenu. 
  
Par le biais de la même structure **SYNCCONT** , le client obtient le nombre de dossiers dont le contenu téléchargé ou téléchargé. Le client parcourt en boucle chacun de ces dossiers par déplacement du magasin local à l’état de la table de téléchargement pour télécharger un dossier ou le déplacement du magasin local à l’état de table de téléchargement pour télécharger le dossier. 
  
En outre, le client obtient les identificateurs d’entrée pour les dossiers nécessitant la réplication.
  
Lorsque cet état se termine, Outlook nettoie ses informations internes. Le magasin local renvoie l’état de synchronisation.
  
## <a name="see-also"></a>Voir aussi



[À propos de l’API de réplication](about-the-replication-api.md)
  
[Constantes MAPI](mapi-constants.md)
  
[À propos de la machine à états de réplication](about-the-replication-state-machine.md)
  
[SYNCSTATE](syncstate.md)

