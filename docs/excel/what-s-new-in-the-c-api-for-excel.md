---
title: Nouveautés de l'API C pour Excel
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: overview
keywords:
- API c [Excel 2007], nouveautés
localization_priority: Normal
ms.assetid: f11552e1-b8ea-4933-b6fc-c452b07eb59d
description: 'S’applique à : Excel 2013 | Office 2013 | Visual Studio'
ms.openlocfilehash: 64e3933ec25f0771db5bd36bbf57f3f259cdc8a1
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/28/2019
ms.locfileid: "33439687"
---
# <a name="whats-new-in-the-c-api-for-excel"></a><span data-ttu-id="57f93-104">Nouveautés de l'API C pour Excel</span><span class="sxs-lookup"><span data-stu-id="57f93-104">What's New in the C API for Excel</span></span>

 <span data-ttu-id="57f93-105">**S’applique à** : Excel 2013 | Office 2013 | Visual Studio</span><span class="sxs-lookup"><span data-stu-id="57f93-105">**Applies to**: Excel 2013 | Office 2013 | Visual Studio</span></span> 
  
<span data-ttu-id="57f93-106">Conjointement avec Microsoft Excel 2013, le kit de développement logiciel (SDK) XLL Microsoft Excel 2013 inclut la prise en charge des fonctionnalités suivantes.</span><span class="sxs-lookup"><span data-stu-id="57f93-106">In conjunction with Microsoft Excel 2013, the Microsoft Excel 2013 XLL Software Development Kit (SDK) includes support for the following features.</span></span>
  
- <span data-ttu-id="57f93-107">**Nouvelles fonctions**</span><span class="sxs-lookup"><span data-stu-id="57f93-107">**New Functions**</span></span>
    
    <span data-ttu-id="57f93-108">Le kit de développement XLL Microsoft Excel 2013 prend en charge le rappel de toutes les nouvelles fonctions de feuille de calcul dans Excel 2013.</span><span class="sxs-lookup"><span data-stu-id="57f93-108">The Microsoft Excel 2013 XLL SDK supports calling back to all of the new worksheet functions in Excel 2013.</span></span> <span data-ttu-id="57f93-109">Pour plus d'informations sur l'appel de fonctions Excel 2013, consultez [la rubrique appel dans Excel à partir de la dll ou XLL](calling-into-excel-from-the-dll-or-xll.md).</span><span class="sxs-lookup"><span data-stu-id="57f93-109">For more information about calling Excel 2013 functions, see [Calling into Excel from the DLL or XLL](calling-into-excel-from-the-dll-or-xll.md).</span></span>
    
- <span data-ttu-id="57f93-110">**Fonctions asynchrones définies par l'utilisateur**</span><span class="sxs-lookup"><span data-stu-id="57f93-110">**Asynchronous User-defined Functions**</span></span>
    
    <span data-ttu-id="57f93-111">Excel 2013 prend en charge l'appel de fonctions définies par l'utilisateur (UDF) de manière asynchrone, ce qui peut améliorer les performances en permettant l'exécution de plusieurs calculs en même temps.</span><span class="sxs-lookup"><span data-stu-id="57f93-111">Excel 2013 supports calling user-defined functions (UDF) asynchronously, which can improve performance by enabling several calculations to run at the same time.</span></span> <span data-ttu-id="57f93-112">Pour plus d'informations sur les fonctions définies par l'utilisateur asynchrones, voir [Asynchronous User-Defined Functions](asynchronous-user-defined-functions.md).</span><span class="sxs-lookup"><span data-stu-id="57f93-112">For more information about asynchronous UDFs, see [Asynchronous User-Defined Functions](asynchronous-user-defined-functions.md).</span></span>
    
- <span data-ttu-id="57f93-113">**Connecteurs de cluster**</span><span class="sxs-lookup"><span data-stu-id="57f93-113">**Cluster Connectors**</span></span>
    
    <span data-ttu-id="57f93-114">Les connecteurs de cluster permettent aux UDF de s'exécuter sur des clusters de calcul à hautes performances.</span><span class="sxs-lookup"><span data-stu-id="57f93-114">Cluster connectors enable UDFs to run on high-performance compute clusters.</span></span> <span data-ttu-id="57f93-115">Pour plus d'informations sur la création de connecteurs de cluster, voir [développement de connecteurs de cluster Excel](developing-excel-cluster-connectors.md).</span><span class="sxs-lookup"><span data-stu-id="57f93-115">For more information about creating cluster connectors, see [Developing Excel Cluster Connectors](developing-excel-cluster-connectors.md).</span></span>
    
    > [!NOTE]
    > <span data-ttu-id="57f93-116">Les compléments XLL que vous envisagez d'exécuter sur des clusters de calcul doivent appeler uniquement des fonctions sécurisées pour le cluster.</span><span class="sxs-lookup"><span data-stu-id="57f93-116">XLL add-ins that you intend to run on compute clusters must call only cluster-safe functions.</span></span> <span data-ttu-id="57f93-117">Pour plus d'informations sur les fonctions que vous pouvez utiliser, reportez-vous à la rubrique [Excel XLL SDK API Reference](excel-xll-sdk-api-function-reference.md) and [cluster safe](cluster-safe-functions.md)functions.</span><span class="sxs-lookup"><span data-stu-id="57f93-117">For more information about the functions you can use, see [Excel XLL SDK API Function Reference](excel-xll-sdk-api-function-reference.md) and [Cluster Safe Functions](cluster-safe-functions.md).</span></span> 
  
- <span data-ttu-id="57f93-118">**Prise en charge de 64 bits**</span><span class="sxs-lookup"><span data-stu-id="57f93-118">**64-bit Support**</span></span>
    
    <span data-ttu-id="57f93-119">Vous pouvez maintenant compiler et lier les XLL 32 bits et 64 bits.</span><span class="sxs-lookup"><span data-stu-id="57f93-119">You can now compile and link both 32-bit and 64-bit XLLs.</span></span> <span data-ttu-id="57f93-120">Pour plus d'informations, consultez la rubrique [creatIng XLL](creating-xlls.md).</span><span class="sxs-lookup"><span data-stu-id="57f93-120">For more information, see [Creating XLLs](creating-xlls.md).</span></span>
    
## <a name="see-also"></a><span data-ttu-id="57f93-121">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="57f93-121">See also</span></span>



[<span data-ttu-id="57f93-122">Développement de XLL de Excel</span><span class="sxs-lookup"><span data-stu-id="57f93-122">Developing Excel XLLs</span></span>](developing-excel-xlls.md)
  
[<span data-ttu-id="57f93-123">Programmation avec l�API C dans Excel</span><span class="sxs-lookup"><span data-stu-id="57f93-123">Programming with the C API in Excel</span></span>](programming-with-the-c-api-in-excel.md)
  
[<span data-ttu-id="57f93-124">Le multithreading et la Contention de m�moire dans Excel</span><span class="sxs-lookup"><span data-stu-id="57f93-124">Multithreading and Memory Contention in Excel</span></span>](multithreading-and-memory-contention-in-excel.md)


[<span data-ttu-id="57f93-125">Mise en route avec le Kit de d�veloppement logiciel XLL Excel 2013</span><span class="sxs-lookup"><span data-stu-id="57f93-125">Getting Started with the Excel XLL SDK</span></span>](getting-started-with-the-excel-xll-sdk.md)

