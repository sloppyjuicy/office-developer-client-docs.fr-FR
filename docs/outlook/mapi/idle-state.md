---
title: État inActif
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
localization_priority: Normal
ms.assetid: 46976bea-c6bb-2e37-2e67-4cbccaa03aec
description: Dernière modification le 9 mars 2015
ms.openlocfilehash: 3db4ead7e2485bbbae82f2a07659c934b394d6d5
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/28/2019
ms.locfileid: "33419477"
---
# <a name="idle-state"></a>État inActif

  
  
**S’applique à** : Outlook 2013 | Outlook 2016 
  
 Cette rubrique décrit ce qui se passe lors de l'état d'inactivité de la machine à États de réplication. 
  
## <a name="quick-info"></a>Informations rapides

|||
|:-----|:-----|
|Identificateur d'État:  <br/> |**LR_SYNC_IDLE** <br/> |
|Structure de données associée:  <br/> | *None*  <br/> |
|À partir de cet État:  <br/> | *Non applicable*  <br/> |
|À cet État:  <br/> |[Synchronisation de l’état](synchronize-state.md) <br/> |
   
> [!NOTE]
> L'ordinateur d'état de réplication est un ordinateur d'État déterministe. Un client qui se déplace d'un État à un autre doit finalement revenir au premier de ce dernier. 
  
## <a name="description"></a>Description

Rien ne se produit dans cet État. Un magasin local est dans cet état avant l'initialisation de la réplication et une fois la réplication terminée.
  
## <a name="see-also"></a>Voir aussi



[À propos de l’API de réplication](about-the-replication-api.md)
  
[Constantes MAPI](mapi-constants.md)
  
[À propos de la machine à états de réplication](about-the-replication-state-machine.md)
  
[SYNCSTATE](syncstate.md)

