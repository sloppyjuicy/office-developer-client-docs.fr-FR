---
title: Multithreading et gestion de la mémoire
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
ms.localizationpriority: medium
ms.assetid: 6f7e052a-4270-4b83-b1ed-feabf6dbeaa2
ms.openlocfilehash: c3ca2913661575ebe8ac075950a9560c846ef348
ms.sourcegitcommit: 193df57ebf141020852d2ebc8cf0931edb71574a
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/25/2022
ms.locfileid: "62198280"
---
# <a name="multithreading-and-memory-management"></a>Multithreading et gestion de la mémoire

 **S’applique à**: Excel 2013 | Office 2013 | Visual Studio 
  
Une gestion appropriée de la mémoire est essentielle à la création de Microsoft Excel XLL fiables. Si vous n’allouez pas les mémoires tampons appropriées et que vous les libérez lorsqu’elles ne sont plus nécessaires, vous réduisez les performances, créez une contention de ressources et déstabilisez les Excel.
  
À partir Microsoft Office Excel 2007, vous pouvez configurer Excel pour utiliser jusqu’à 1 024 threads simultanés lors du recalcul. Dans certains cas, en particulier lorsque plusieurs processeurs sont disponibles ou avec des fonctions définies par l’utilisateur s’exécutant sur des serveurs en cluster, le multithreading peut améliorer les performances.
  
Les rubriques suivantes décrivent comment gérer la mémoire et les threads dans les XL :
  
- [Gestion de la mémoire dans Excel](memory-management-in-excel.md)
    
- [Le multithreading et la Contention de m�moire dans Excel](multithreading-and-memory-contention-in-excel.md)
    
- [Recalcul multithread dans Excel](multithreaded-recalculation-in-excel.md)
    
## <a name="see-also"></a>Voir aussi



[Développement de XLL de Excel 2013](developing-excel-xlls.md)

