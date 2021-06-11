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
# <a name="multithreading-and-memory-management"></a><span data-ttu-id="4f695-103">Multithreading et gestion de la mémoire</span><span class="sxs-lookup"><span data-stu-id="4f695-103">Multithreading and Memory Management</span></span>

 <span data-ttu-id="4f695-104">**S’applique à** : Excel 2013 | Office 2013 | Visual Studio</span><span class="sxs-lookup"><span data-stu-id="4f695-104">**Applies to**: Excel 2013 | Office 2013 | Visual Studio</span></span> 
  
<span data-ttu-id="4f695-105">Une gestion appropriée de la mémoire est essentielle à la création de Microsoft Excel XLL fiables.</span><span class="sxs-lookup"><span data-stu-id="4f695-105">Proper handling of memory is vital to creating reliable XLL add-ins for Microsoft Excel.</span></span> <span data-ttu-id="4f695-106">Le fait de ne pas allouer les mémoires tampons appropriées et de les libérer lorsqu’elles ne sont plus nécessaires réduit les performances, crée une contention de ressources et déstabilise les Excel.</span><span class="sxs-lookup"><span data-stu-id="4f695-106">Failure to allocate appropriate memory buffers and free them when they are no longer needed reduces performance, creates resource contention, and destabilizes Excel.</span></span>
  
<span data-ttu-id="4f695-107">À partir Microsoft Office Excel 2007, vous pouvez configurer Excel pour utiliser jusqu’à 1 024 threads simultanés lors du recalcul.</span><span class="sxs-lookup"><span data-stu-id="4f695-107">Beginning with Microsoft Office Excel 2007, you can configure Excel to use up to 1,024 concurrent threads when recalculating.</span></span> <span data-ttu-id="4f695-108">Dans certains cas, en particulier lorsque plusieurs processeurs sont disponibles ou avec des fonctions définies par l’utilisateur s’exécutant sur des serveurs en cluster, le multithreading peut améliorer les performances.</span><span class="sxs-lookup"><span data-stu-id="4f695-108">In some cases, especially when multiple processors are available or with user-defined functions running on clustered servers, multithreading can improve performance.</span></span>
  
<span data-ttu-id="4f695-109">Les rubriques suivantes décrivent comment gérer la mémoire et les threads en XL :</span><span class="sxs-lookup"><span data-stu-id="4f695-109">The following topics describe how to manage memory and threads in XLLs:</span></span>
  
- [<span data-ttu-id="4f695-110">Gestion de la mémoire dans Excel</span><span class="sxs-lookup"><span data-stu-id="4f695-110">Memory Management in Excel</span></span>](memory-management-in-excel.md)
    
- [<span data-ttu-id="4f695-111">Le multithreading et la Contention de m�moire dans Excel</span><span class="sxs-lookup"><span data-stu-id="4f695-111">Multithreading and Memory Contention in Excel</span></span>](multithreading-and-memory-contention-in-excel.md)
    
- [<span data-ttu-id="4f695-112">Recalcul multithread dans Excel</span><span class="sxs-lookup"><span data-stu-id="4f695-112">Multithreaded Recalculation in Excel</span></span>](multithreaded-recalculation-in-excel.md)
    
## <a name="see-also"></a><span data-ttu-id="4f695-113">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="4f695-113">See also</span></span>



[<span data-ttu-id="4f695-114">Développement de XLL de Excel</span><span class="sxs-lookup"><span data-stu-id="4f695-114">Developing Excel XLLs</span></span>](developing-excel-xlls.md)

