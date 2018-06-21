---
title: Quelles sont les nouveautés de l’API C pour Excel
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: overview
keywords:
- api c [excel 2007], quelles sont les nouveautés
localization_priority: Normal
ms.assetid: f11552e1-b8ea-4933-b6fc-c452b07eb59d
description: 'S�applique �: Excel 2013�| Office 2013�| Visual Studio'
ms.openlocfilehash: e80b667296af59f4d3f18238cd498830fcdc35a4
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/21/2018
ms.locfileid: "19782194"
---
# <a name="whats-new-in-the-c-api-for-excel"></a><span data-ttu-id="f48ee-104">Quelles sont les nouveautés de l’API C pour Excel</span><span class="sxs-lookup"><span data-stu-id="f48ee-104">What's New in the C API for Excel</span></span>

 <span data-ttu-id="f48ee-105">**S’applique à**: Excel 2013 | Office 2013 | Visual Studio</span><span class="sxs-lookup"><span data-stu-id="f48ee-105">**Applies to**: Excel 2013 | Office 2013 | Visual Studio</span></span> 
  
<span data-ttu-id="f48ee-106">Conjointement avec Microsoft Excel 2013, le Kit de développement de logiciel (SDK) de Microsoft Excel 2013 XLL prend en charge les fonctionnalités suivantes.</span><span class="sxs-lookup"><span data-stu-id="f48ee-106">In conjunction with Microsoft Excel 2013, the Microsoft Excel 2013 XLL Software Development Kit (SDK) includes support for the following features.</span></span>
  
- <span data-ttu-id="f48ee-107">**Nouvelles fonctions**</span><span class="sxs-lookup"><span data-stu-id="f48ee-107">**New Functions**</span></span>
    
    <span data-ttu-id="f48ee-108">Le SDK XLL Microsoft Excel 2013 prend en charge les rappels à toutes les nouvelles fonctions de feuille de calcul dans Excel 2013.</span><span class="sxs-lookup"><span data-stu-id="f48ee-108">The Microsoft Excel 2013 XLL SDK supports calling back to all of the new worksheet functions in Excel 2013.</span></span> <span data-ttu-id="f48ee-109">Pour plus d’informations sur l’appel de fonctions Excel 2013, voir [appel dans Excel à partir de la DLL ou XLL](calling-into-excel-from-the-dll-or-xll.md).</span><span class="sxs-lookup"><span data-stu-id="f48ee-109">For more information about calling Excel 2013 functions, see [Calling into Excel from the DLL or XLL](calling-into-excel-from-the-dll-or-xll.md).</span></span>
    
- <span data-ttu-id="f48ee-110">**Fonctions asynchrones définies par l’utilisateur**</span><span class="sxs-lookup"><span data-stu-id="f48ee-110">**Asynchronous User-defined Functions**</span></span>
    
    <span data-ttu-id="f48ee-111">Excel 2013 prend en charge l’appel de fonctions définies par l’utilisateur (UDF) en mode asynchrone, qui peut améliorer les performances en activant plusieurs calculs à exécuter en même temps.</span><span class="sxs-lookup"><span data-stu-id="f48ee-111">Excel 2013 supports calling user-defined functions (UDF) asynchronously, which can improve performance by enabling several calculations to run at the same time.</span></span> <span data-ttu-id="f48ee-112">Pour plus d’informations sur les UDF asynchrones, voir [Fonctions Asynchronous User-Defined](asynchronous-user-defined-functions.md).</span><span class="sxs-lookup"><span data-stu-id="f48ee-112">For more information about asynchronous UDFs, see [Asynchronous User-Defined Functions](asynchronous-user-defined-functions.md).</span></span>
    
- <span data-ttu-id="f48ee-113">**Connecteurs de cluster**</span><span class="sxs-lookup"><span data-stu-id="f48ee-113">**Cluster Connectors**</span></span>
    
    <span data-ttu-id="f48ee-114">Connecteurs de cluster activer les UDF à exécuter sur les clusters de calcul hautes performances.</span><span class="sxs-lookup"><span data-stu-id="f48ee-114">Cluster connectors enable UDFs to run on high-performance compute clusters.</span></span> <span data-ttu-id="f48ee-115">Pour plus d’informations sur la création de connecteurs de cluster, voir [Développement de connecteurs de Cluster Excel](developing-excel-cluster-connectors.md).</span><span class="sxs-lookup"><span data-stu-id="f48ee-115">For more information about creating cluster connectors, see [Developing Excel Cluster Connectors](developing-excel-cluster-connectors.md).</span></span>
    
    > [!NOTE]
    > <span data-ttu-id="f48ee-116">Compléments XLL que vous souhaitez exécuter sur les clusters de calcul doivent appeler uniquement des fonctions sécurisées pour le cluster.</span><span class="sxs-lookup"><span data-stu-id="f48ee-116">XLL add-ins that you intend to run on compute clusters must call only cluster-safe functions.</span></span> <span data-ttu-id="f48ee-117">Pour plus d’informations sur les fonctions que vous pouvez utiliser, voir [Référence des fonctions API Excel XLL SDK](excel-xll-sdk-api-function-reference.md) et des [Fonctions sécurisées pour le Cluster](cluster-safe-functions.md).</span><span class="sxs-lookup"><span data-stu-id="f48ee-117">For more information about the functions you can use, see [Excel XLL SDK API Function Reference](excel-xll-sdk-api-function-reference.md) and [Cluster Safe Functions](cluster-safe-functions.md).</span></span> 
  
- <span data-ttu-id="f48ee-118">**prise en charge 64 bits**</span><span class="sxs-lookup"><span data-stu-id="f48ee-118">**64-bit Support**</span></span>
    
    <span data-ttu-id="f48ee-119">Vous pouvez maintenant compiler et lier XLL 32 bits et 64 bits.</span><span class="sxs-lookup"><span data-stu-id="f48ee-119">You can now compile and link both 32-bit and 64-bit XLLs.</span></span> <span data-ttu-id="f48ee-120">Pour plus d’informations, voir [Création de XLL](creating-xlls.md).</span><span class="sxs-lookup"><span data-stu-id="f48ee-120">For more information, see [Creating XLLs](creating-xlls.md).</span></span>
    
## <a name="see-also"></a><span data-ttu-id="f48ee-121">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="f48ee-121">See also</span></span>



[<span data-ttu-id="f48ee-122">D�veloppement de XLL de Excel 2013</span><span class="sxs-lookup"><span data-stu-id="f48ee-122">Developing Excel XLLs</span></span>](developing-excel-xlls.md)
  
[<span data-ttu-id="f48ee-123">Programmation avec l�API�C dans Excel</span><span class="sxs-lookup"><span data-stu-id="f48ee-123">Programming with the C API in Excel</span></span>](programming-with-the-c-api-in-excel.md)
  
[<span data-ttu-id="f48ee-124">Le multithreading et la Contention de m�moire dans Excel</span><span class="sxs-lookup"><span data-stu-id="f48ee-124">Multithreading and Memory Contention in Excel</span></span>](multithreading-and-memory-contention-in-excel.md)


[<span data-ttu-id="f48ee-125">Mise en route avec le Kit de d�veloppement logiciel XLL Excel 2013</span><span class="sxs-lookup"><span data-stu-id="f48ee-125">Getting Started with the Excel XLL SDK</span></span>](getting-started-with-the-excel-xll-sdk.md)

