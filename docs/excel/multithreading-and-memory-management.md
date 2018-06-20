---
title: Multithread et gestion de la mémoire
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: 6f7e052a-4270-4b83-b1ed-feabf6dbeaa2
description: 'S�applique �: Excel 2013�| Office 2013�| Visual Studio'
ms.openlocfilehash: 4f5495648c9012b0e028358037090f7e10ef5219
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19782177"
---
# <a name="multithreading-and-memory-management"></a>Multithread et gestion de la mémoire

 **S’applique à**: Excel 2013 | Office 2013 | Visual Studio 
  
Manipulation de mémoire est indispensable pour la création de compléments XLL fiables pour Microsoft Excel. Échec pour allouer des mémoires tampons appropriées et les libérer lorsqu’ils ne sont plus nécessaires réduit les performances, crée des conflits de ressources et déstabilise Excel.
  
À partir de Microsoft Office Excel 2007, vous pouvez configurer Excel pour utiliser jusqu'à 1 024 threads simultanés lorsque le recalcul. Dans certains cas, en particulier lorsque plusieurs processeurs sont disponibles ou définis par l’utilisateur avec les fonctions en cours d’exécution sur les serveurs en cluster, le multithreading peuvent améliorer les performances.
  
Les rubriques suivantes expliquent comment gérer les threads dans les XLL et mémoire :
  
- [Gestion de la m�moire dans Excel](memory-management-in-excel.md)
    
- [Le multithreading et la Contention de m�moire dans Excel](multithreading-and-memory-contention-in-excel.md)
    
- [Recalcul multithread dans Excel](multithreaded-recalculation-in-excel.md)
    
## <a name="see-also"></a>Voir aussi



[D�veloppement de XLL de Excel 2013](developing-excel-xlls.md)

