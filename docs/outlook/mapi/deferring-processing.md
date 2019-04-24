---
title: Report de traitement
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: a791b95f-56ad-493a-9ba5-fb4c7dd80e89
description: 'Dernière modification : 23 juillet 2011'
ms.openlocfilehash: 2d3fbf8f7a725f121579066001715fb0bc6beba0
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32336931"
---
# <a name="deferring-processing"></a>Report de traitement

  
  
**S’applique à** : Outlook 2013 | Outlook 2016 
  
TransMettez l'indicateur MAPI_DEFERRED_ERRORS aux appels de méthode autant que possible. De nombreux appels de méthode MAPI ont été optimisés pour accepter cet indicateur, ce qui a pour effet de reporter la tâche demandée jusqu'à ce que plusieurs tâches puissent être exécutées en même temps ou que vous ne puissiez plus attendre les résultats.
  
Par exemple, si vous transmettez MAPI_DEFERRED_ERRORS à [IMsgStore:: OpenEntry](imsgstore-openentry.md) pour ouvrir un dossier, l'ouverture du dossier et un éventuel appel distant peut être repoussé jusqu'à ce que vous appeliez un autre appel au **GetHierarchyTable** du dossier ou ** Méthodes GetProps** . **GetHierarchyTable** et **GetProps** requièrent le retour de données du fournisseur de services, une tâche qui doit être exécutée immédiatement. 
  
Un autre moyen de différer le traitement est simplement de ne pas passer un appel. En étant conscient de l'utilisateur et lorsque l'utilisateur peut percevoir une décharge sur les ressources ou le temps de traitement, vous pouvez déterminer quand il est judicieux d'effectuer des appels. Il est possible d'améliorer les performances en effectuant des appels à la fois lorsque l'utilisateur ne les remarquera pas ou en ne les apportant pas du tout.
  
Par exemple, considérez la situation lorsque vous recevez plusieurs notifications par seconde d'une banque de messages qui déplace un grand nombre de messages. Un indicateur de progression s'affiche pour indiquer le pourcentage d'achèvement de l'opération. En règle générale, les utilisateurs ne considèrent pas que cette opération est lente avant que quelques secondes ne se soient écoulées. Par conséquent, si vous mettez à jour l'indicateur de progression, n'effectuez aucune modification pendant au moins quatre secondes après l'initialisation de l'opération de déplacement. Cela permet de gagner du temps dans les cas courants où l'opération est rapide et d'informer les utilisateurs en temps opportun lorsque l'opération est lente.
  

