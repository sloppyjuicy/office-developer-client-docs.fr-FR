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
# <a name="multithreading-and-memory-management"></a><span data-ttu-id="ed60e-103">Multithread et gestion de la mémoire</span><span class="sxs-lookup"><span data-stu-id="ed60e-103">Multithreading and Memory Management</span></span>

 <span data-ttu-id="ed60e-104">**S’applique à**: Excel 2013 | Office 2013 | Visual Studio</span><span class="sxs-lookup"><span data-stu-id="ed60e-104">**Applies to**: Excel 2013 | Office 2013 | Visual Studio</span></span> 
  
<span data-ttu-id="ed60e-105">Manipulation de mémoire est indispensable pour la création de compléments XLL fiables pour Microsoft Excel.</span><span class="sxs-lookup"><span data-stu-id="ed60e-105">Proper handling of memory is vital to creating reliable XLL add-ins for Microsoft Excel.</span></span> <span data-ttu-id="ed60e-106">Échec pour allouer des mémoires tampons appropriées et les libérer lorsqu’ils ne sont plus nécessaires réduit les performances, crée des conflits de ressources et déstabilise Excel.</span><span class="sxs-lookup"><span data-stu-id="ed60e-106">Failure to allocate appropriate memory buffers and free them when they are no longer needed reduces performance, creates resource contention, and destabilizes Excel.</span></span>
  
<span data-ttu-id="ed60e-107">À partir de Microsoft Office Excel 2007, vous pouvez configurer Excel pour utiliser jusqu'à 1 024 threads simultanés lorsque le recalcul.</span><span class="sxs-lookup"><span data-stu-id="ed60e-107">Beginning with Microsoft Office Excel 2007, you can configure Excel to use up to 1,024 concurrent threads when recalculating.</span></span> <span data-ttu-id="ed60e-108">Dans certains cas, en particulier lorsque plusieurs processeurs sont disponibles ou définis par l’utilisateur avec les fonctions en cours d’exécution sur les serveurs en cluster, le multithreading peuvent améliorer les performances.</span><span class="sxs-lookup"><span data-stu-id="ed60e-108">In some cases, especially when multiple processors are available or with user-defined functions running on clustered servers, multithreading can improve performance.</span></span>
  
<span data-ttu-id="ed60e-109">Les rubriques suivantes expliquent comment gérer les threads dans les XLL et mémoire :</span><span class="sxs-lookup"><span data-stu-id="ed60e-109">The following topics describe how to manage memory and threads in XLLs:</span></span>
  
- [<span data-ttu-id="ed60e-110">Gestion de la m�moire dans Excel</span><span class="sxs-lookup"><span data-stu-id="ed60e-110">Memory Management in Excel</span></span>](memory-management-in-excel.md)
    
- [<span data-ttu-id="ed60e-111">Le multithreading et la Contention de m�moire dans Excel</span><span class="sxs-lookup"><span data-stu-id="ed60e-111">Multithreading and Memory Contention in Excel</span></span>](multithreading-and-memory-contention-in-excel.md)
    
- [<span data-ttu-id="ed60e-112">Recalcul multithread dans Excel</span><span class="sxs-lookup"><span data-stu-id="ed60e-112">Multithreaded Recalculation in Excel</span></span>](multithreaded-recalculation-in-excel.md)
    
## <a name="see-also"></a><span data-ttu-id="ed60e-113">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="ed60e-113">See also</span></span>



[<span data-ttu-id="ed60e-114">D�veloppement de XLL de Excel 2013</span><span class="sxs-lookup"><span data-stu-id="ed60e-114">Developing Excel XLLs</span></span>](developing-excel-xlls.md)

