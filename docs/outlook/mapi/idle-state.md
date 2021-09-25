---
title: État inactif
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.localizationpriority: medium
ms.assetid: 46976bea-c6bb-2e37-2e67-4cbccaa03aec
description: Dernière modification le 9 mars 2015
ms.openlocfilehash: 67f3c24de34ebfe6b2b96fae0f64ff61037fc839
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/24/2021
ms.locfileid: "59561543"
---
# <a name="idle-state"></a>État inactif

  
  
**S’applique à** : Outlook 2013 | Outlook 2016 
  
 Cette rubrique décrit ce qui se produit pendant l’état d’inactivité de la machine à états de réplication. 
  
## <a name="quick-info"></a>Informations rapides

|||
|:-----|:-----|
|Identificateur d’état :  <br/> |**LR_SYNC_IDLE** <br/> |
|Structure de données associée :  <br/> | *Aucune*  <br/> |
|À partir de cet état :  <br/> | *Non applicable*  <br/> |
|À cet état :  <br/> |[Synchronisation de l’état](synchronize-state.md) <br/> |
   
> [!NOTE]
> La machine à états de réplication est une machine à états déterministe. Un client s’écartant d’un état à un autre doit finalement revenir au premier à partir du second. 
  
## <a name="description"></a>Description

Rien ne se passe dans cet état. Un magasin local est dans cet état avant le début de la réplication et une fois la réplication terminée.
  
## <a name="see-also"></a>Voir aussi



[À propos de l’API de réplication](about-the-replication-api.md)
  
[Constantes MAPI](mapi-constants.md)
  
[À propos de la machine à états de réplication](about-the-replication-state-machine.md)
  
[SYNCSTATE](syncstate.md)

