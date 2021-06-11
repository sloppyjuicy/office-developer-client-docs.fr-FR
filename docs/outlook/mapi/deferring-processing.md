---
title: Report du traitement
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: a791b95f-56ad-493a-9ba5-fb4c7dd80e89
description: 'Derniére modification : samedi 23 juillet 2011'
ms.openlocfilehash: 2d3fbf8f7a725f121579066001715fb0bc6beba0
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/28/2019
ms.locfileid: "33430930"
---
# <a name="deferring-processing"></a>Report du traitement

  
  
**S’applique à** : Outlook 2013 | Outlook 2016 
  
Passez l’indicateur MAPI_DEFERRED_ERRORS aux appels de méthode autant que possible. De nombreux appels de méthode MAPI ont été optimisés pour accepter cet indicateur, ce qui a pour effet que le fournisseur ajournait la tâche demandée jusqu’à ce que plusieurs tâches soient effectuées en même temps ou que vous ne pouvez plus attendre les résultats.
  
Par exemple, si vous passez MAPI_DEFERRED_ERRORS à [IMsgStore::OpenEntry](imsgstore-openentry.md) pour ouvrir un dossier, l’ouverture du dossier et un appel distant possible peuvent être reportés jusqu’à ce que vous appelez à nouveau les méthodes **GetHierarchyTable** ou **GetProps** du dossier. **GetHierarchyTable** et **GetProps** nécessitent le retour des données du fournisseur de services, une tâche qui doit être effectuée immédiatement. 
  
Une autre façon de différer le traitement consiste simplement à ne pas effectuer d’appel. En étant conscient de l’utilisateur et du moment où il peut percevoir un drainage des ressources ou du temps de traitement, vous pouvez déterminer quand il est logique d’effectuer des appels. Il est possible d’améliorer les performances en faisant des appels à un moment où l’utilisateur ne le remarque pas ou en ne les rendant pas du tout.
  
Par exemple, prenons la situation dans laquelle vous recevez plus d’une notification par seconde à partir d’une boutique de messages qui déplace un grand nombre de messages. Un indicateur de progression s’affiche pour indiquer le pourcentage d’achèvement de l’opération. En règle générale, les utilisateurs ne percevoiraient pas cette opération comme lente tant que quelques secondes n’ont pas été écoulées. Par conséquent, si vous met à jour l’indicateur de progression, n’a lieu aucune modification avant au moins quatre secondes après le lancement de l’opération de déplacement. Cela permet de gagner du temps dans les cas courants où l’opération est rapide et d’informer les utilisateurs en temps voulu lorsque l’opération est lente.
  

