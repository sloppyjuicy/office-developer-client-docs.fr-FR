---
title: Synchroniser l’état du contenu
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.localizationpriority: medium
ms.assetid: 52216bc3-8cbd-3856-ea46-78f7d0dd66ff
description: Cette rubrique décrit ce qui se produit pendant l’état de synchronisation du contenu de la machine à états de réplication.
ms.openlocfilehash: b39d2e031dcfcb9b5395104881536d13eb7dd1d8
ms.sourcegitcommit: 0a067f44281eddabff15fff565fb80eaa543b660
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/23/2022
ms.locfileid: "63763851"
---
# <a name="synchronize-contents-state"></a>Synchroniser l’état du contenu

**S’applique à** : Outlook 2013 | Outlook 2016
  
 Cette rubrique décrit ce qui se produit pendant l’état de synchronisation du contenu de la machine à états de réplication.
  
## <a name="quick-info"></a>Informations rapides

|Propriété |Valeur |
|:-----|:-----|
|Identificateur d’état :  <br/> |**LR_SYNC_CONTENTS** <br/> |
|Structure de données associée :  <br/> |**[SYNCCONT](synccont.md)** <br/> |
|À partir de cet état :  <br/> |[Synchronisation de l’état](synchronize-state.md) <br/> |
|À cet état :  <br/> |[Télécharger l’état de la table](download-table-state.md), [télécharger l’état de la table](upload-table-state.md) ou synchroniser l’état  <br/> |

> [!NOTE]
> La machine à états de réplication est une machine à états déterministe. Un client s’écartant d’un état à un autre doit finalement revenir au premier à partir du second.
  
## <a name="description"></a>Description

Cet état initie l’un des deux processus de réplication : le téléchargement du contenu des dossiers spécifiés sur un magasin local ou une synchronisation complète. Dans une synchronisation complète, pour chacun des dossiers spécifiés, le contenu est d’abord chargé, puis téléchargé. Selon les *ulFlags définies* dans la structure **[SYNC](sync.md)** correspondante à l’état de synchronisation précédent, Outlook initialise les membres [out] dans la structure **SYNCCONT** pour fournir des informations sur le contenu.
  
Par le biais de la même structure **SYNCCONT** , le client obtient le nombre de dossiers dont le contenu doit être téléchargé ou téléchargé. Le client parse en boucle dans chacun de ces dossiers en déplaçant la boutique locale vers l’état de la table de téléchargement pour télécharger un dossier, ou en déplaçant la boutique locale vers l’état de la table de téléchargement pour télécharger le dossier.
  
En outre, le client obtient les ID d’entrée pour les dossiers nécessitant une réplication.
  
Lorsque cet état se termine, Outlook nettoie ses informations internes. Le magasin local revient à l’état de synchronisation.
  
## <a name="see-also"></a>Voir aussi

[À propos de l’API de réplication](about-the-replication-api.md)  
[Constantes MAPI](mapi-constants.md)  
[À propos de la machine à états de réplication](about-the-replication-state-machine.md)  
[SYNCSTATE](syncstate.md)
