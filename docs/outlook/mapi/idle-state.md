---
title: État d’inactivité
description: Cette rubrique décrit ce qui se passe pendant l’état d’inactivité de la machine d’état de réplication. Les propriétés associées et leurs valeurs correspondantes sont fournies.
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.localizationpriority: medium
ms.assetid: 46976bea-c6bb-2e37-2e67-4cbccaa03aec
ms.openlocfilehash: 2a194dbec606b6dcb27cad350de9d31f8ef14f6b
ms.sourcegitcommit: f872848fbeb5b2353179ad4bf4eab23f61f87666
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/01/2022
ms.locfileid: "65815750"
---
# <a name="idle-state"></a>État d’inactivité

  
  
**S’applique à** : Outlook 2013 | Outlook 2016 
  
 Cette rubrique décrit ce qui se passe pendant l’état d’inactivité de la machine d’état de réplication. 
  
## <a name="quick-info"></a>Informations rapides

|Propriété|Valeur|
|:-----|:-----|
|Identificateur d’état :  <br/> |**LR_SYNC_IDLE** <br/> |
|Structure de données associée :  <br/> | *Aucune*  <br/> |
|À partir de cet état :  <br/> | *Non applicable*  <br/> |
|À cet état :  <br/> |[Synchronisation de l’état](synchronize-state.md) <br/> |
   
> [!NOTE]
> L’ordinateur d’état de réplication est un ordinateur d’état déterministe. Un client qui part d’un état à un autre doit finalement revenir au premier d’un autre état. 
  
## <a name="description"></a>Description

Rien ne se passe dans cet état. Un magasin local est dans cet état avant le lancement de la réplication et une fois la réplication terminée.
  
## <a name="see-also"></a>Voir aussi



[À propos de l’API de réplication](about-the-replication-api.md)
  
[Constantes MAPI](mapi-constants.md)
  
[À propos de la machine à états de réplication](about-the-replication-state-machine.md)
  
[SYNCSTATE](syncstate.md)

