---
title: Report de traitement
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: a791b95f-56ad-493a-9ba5-fb4c7dd80e89
description: 'Derni�re modification�: samedi 23 juillet 2011'
ms.openlocfilehash: 8f26fc6a51c3abdb4d4d009183fa8263ce97b261
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19783127"
---
# <a name="deferring-processing"></a>Report de traitement

  
  
**S’applique à**: Outlook 
  
Passez l’indicateur MAPI_DEFERRED_ERRORS pour les appels de méthode autant que possible. Beaucoup d’appels de méthode MAPI ont été optimisés pour accepter cet indicateur, à l’origine du fournisseur à soit attendre la tâche demandée plusieurs tâches peuvent être effectuées à la fois, ou vous pouvez attendre ne sont plus les résultats.
  
Par exemple, si vous transmettez MAPI_DEFERRED_ERRORS à [IMsgStore::OpenEntry](imsgstore-openentry.md) pour ouvrir un dossier, l’ouverture du dossier et un appel à distance possible peut être différée jusqu'à ce que vous effectuez un autre appel comme un appel du dossier **GetHierarchyTable** ou ** GetProps** méthodes. À la fois **GetHierarchyTable** et **GetProps** requièrent le retour de données à partir du fournisseur de service, une tâche qui doit être exécutée immédiatement. 
  
Une autre manière de différer le traitement est simplement ne pas pour émettre un appel. En ayant connaissance de l’utilisateur et de l’utilisateur peut percevoir une charge de ressources ou de temps de traitement, vous pouvez déterminer quand il est judicieux de passer des appels. Il existe une opportunité pour améliorer les performances en effectuant des appels, soit à la fois lorsque l’utilisateur ne remarqueront ou ne pas les rendant tout.
  
Par exemple, considérez la situation lorsque vous recevez une plusieurs notification par seconde à partir d’une banque de messages est de déplacer un grand nombre de messages. Un indicateur de progression est affiché pour indiquer le pourcentage d’achèvement de l’opération. Les utilisateurs généralement pas voit cette opération pour être lente jusqu'à ce que quelques secondes se sont écoulées. Par conséquent, si vous mettez à jour l’indicateur de progression, n’apportez aucune modification jusqu’au moins quatre secondes après l’ouverture de l’opération de déplacement. Cela gagner du temps dans les cas lorsque l’opération est rapide et informer les utilisateurs en temps voulu lorsque l’opération est lente.
  

