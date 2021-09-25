---
title: Multithreading et gestion de la mémoire
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
ms.localizationpriority: medium
ms.assetid: 6f7e052a-4270-4b83-b1ed-feabf6dbeaa2
description: 'S’applique à : Excel 2013 | Office 2013 | Visual Studio'
ms.openlocfilehash: 9e233d6db482c4671ee25cfb046e730a3d0e2376
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/24/2021
ms.locfileid: "59576715"
---
# <a name="multithreading-and-memory-management"></a>Multithreading et gestion de la mémoire

 **S’applique à**: Excel 2013 | Office 2013 | Visual Studio 
  
Une gestion appropriée de la mémoire est essentielle à la création de Microsoft Excel XLL fiables. Le fait de ne pas allouer les mémoires tampons appropriées et de les libérer lorsqu’elles ne sont plus nécessaires réduit les performances, crée une contention de ressources et déstabilise les Excel.
  
À partir Microsoft Office Excel 2007, vous pouvez configurer Excel pour utiliser jusqu’à 1 024 threads simultanés lors du recalcul. Dans certains cas, en particulier lorsque plusieurs processeurs sont disponibles ou avec des fonctions définies par l’utilisateur s’exécutant sur des serveurs en cluster, le multithreading peut améliorer les performances.
  
Les rubriques suivantes décrivent comment gérer la mémoire et les threads en XL :
  
- [Gestion de la mémoire dans Excel](memory-management-in-excel.md)
    
- [Le multithreading et la Contention de m�moire dans Excel](multithreading-and-memory-contention-in-excel.md)
    
- [Recalcul multithread dans Excel](multithreaded-recalculation-in-excel.md)
    
## <a name="see-also"></a>Voir aussi



[Développement de XLL de Excel](developing-excel-xlls.md)

