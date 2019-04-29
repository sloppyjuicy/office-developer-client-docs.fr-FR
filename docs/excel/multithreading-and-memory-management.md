---
title: Multithreading et gestion de la mémoire
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: 6f7e052a-4270-4b83-b1ed-feabf6dbeaa2
description: 'S’applique à : Excel 2013 | Office 2013 | Visual Studio'
ms.openlocfilehash: f387d5ddb184c681ab5e005a6eb24058f6f52f9a
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/28/2019
ms.locfileid: "33414465"
---
# <a name="multithreading-and-memory-management"></a>Multithreading et gestion de la mémoire

 **S’applique à** : Excel 2013 | Office 2013 | Visual Studio 
  
Une gestion correcte de la mémoire est essentielle pour créer des compléments XLL fiables pour Microsoft Excel. L'imPossibilité d'allouer des mémoires tampons de mémoire appropriées et de les libérer lorsqu'elles ne sont plus nécessaires réduit les performances, crée une contention de ressources et déstabilise Excel.
  
À partir de Microsoft Office Excel 2007, vous pouvez configurer Excel pour utiliser jusqu'à 1 024 threads simultanés lors du recalcul. Dans certains cas, en particulier lorsque plusieurs processeurs sont disponibles ou lorsque des fonctions définies par l'utilisateur s'exécutent sur des serveurs en cluster, le multithreading peut améliorer les performances.
  
Les rubriques suivantes décrivent comment gérer la mémoire et les threads dans les XLL:
  
- [Gestion de la mémoire dans Excel](memory-management-in-excel.md)
    
- [Le multithreading et la Contention de m�moire dans Excel](multithreading-and-memory-contention-in-excel.md)
    
- [Recalcul multithread dans Excel](multithreaded-recalculation-in-excel.md)
    
## <a name="see-also"></a>Voir aussi



[Développement de XLL de Excel](developing-excel-xlls.md)

