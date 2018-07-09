---
title: Développement de XLL Excel
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: overview
keywords:
- compléments - [excel 2007], développement de XLL XLL - [Excel 2007,] - [Excel 2007], développement
localization_priority: Normal
ms.assetid: dd27ae4d-ef97-47db-885c-ddd955816900
description: 'S�applique �: Excel 2013�| Office 2013�| Visual Studio'
ms.openlocfilehash: cb2483b9cd1b11bcfeee81bba02b6d593e8818fc
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19782026"
---
# <a name="developing-excel-xlls"></a><span data-ttu-id="ddf4c-104">Développement de XLL Excel</span><span class="sxs-lookup"><span data-stu-id="ddf4c-104">Developing Excel XLLs</span></span>

<span data-ttu-id="ddf4c-105">**S’applique à**: Excel 2013 | Office 2013 | Visual Studio</span><span class="sxs-lookup"><span data-stu-id="ddf4c-105">**Applies to**: Excel 2013 | Office 2013 | Visual Studio</span></span> 
  
<span data-ttu-id="ddf4c-106">La raison principale pour l’écriture de Microsoft Excel XLL et à l’aide de l’API C consiste à créer des fonctions de feuille de calcul hautes performances.</span><span class="sxs-lookup"><span data-stu-id="ddf4c-106">The primary reason for writing Microsoft Excel XLLs and using the C API is to create high-performance worksheet functions.</span></span> <span data-ttu-id="ddf4c-107">Les applications des fonctions de hautes performances et, à compter d’Excel 2007, la possibilité d’écrire des interfaces multithreads aux ressources du serveur puissant : rendre un composant essentiel de l’extensibilité Excel.</span><span class="sxs-lookup"><span data-stu-id="ddf4c-107">The applications of high-performance functions—and, starting in Excel 2007, the ability to write multithreaded interfaces to powerful server resources—make it a very important part of Excel extensibility.</span></span> <span data-ttu-id="ddf4c-108">Les performances des XLL a été davantage améliorée dans Excel 2007 à l’ajout de nouveaux types de données et le plus important, la prise en charge multithread.</span><span class="sxs-lookup"><span data-stu-id="ddf4c-108">The performance of XLLs was further enhanced in Excel 2007 by the addition of new data types and, most important, support for multithreading.</span></span>
  
<span data-ttu-id="ddf4c-109">L’API C a aucune des fonctionnalités de développement rapide plus haut niveau de Microsoft Visual Basic pour Applications (VBA), COM ou Microsoft .NET Framework.</span><span class="sxs-lookup"><span data-stu-id="ddf4c-109">The C API has none of the higher-level rapid development features of Microsoft Visual Basic for Applications (VBA), COM, or the Microsoft .NET Framework.</span></span> <span data-ttu-id="ddf4c-110">Gestion de la mémoire est faible niveau et par conséquent place une plus grande responsabilité sur le développeur.</span><span class="sxs-lookup"><span data-stu-id="ddf4c-110">Memory management is low level, and therefore puts greater responsibility on the developer.</span></span> <span data-ttu-id="ddf4c-111">Nombreuses fonctionnalités d’Excel qui sont exposées par le biais de COM, en les rendant disponibles par le biais de VBA et le .NET Framework, ne sont pas exposées à l’API C.</span><span class="sxs-lookup"><span data-stu-id="ddf4c-111">Many Excel features that are exposed through COM, making them available through VBA and the .NET Framework, are not exposed to the C API.</span></span>


- [<span data-ttu-id="ddf4c-112">Concepts de programmation Excel</span><span class="sxs-lookup"><span data-stu-id="ddf4c-112">Excel Programming Concepts</span></span>](excel-programming-concepts.md)
  
- [<span data-ttu-id="ddf4c-113">Utilisation des DLL</span><span class="sxs-lookup"><span data-stu-id="ddf4c-113">Working with DLLs</span></span>](working-with-dlls.md)
  
- [<span data-ttu-id="ddf4c-114">Acc�s au code XLL dans Excel</span><span class="sxs-lookup"><span data-stu-id="ddf4c-114">Accessing XLL Code in Excel</span></span>](accessing-xll-code-in-excel.md)
  
- [<span data-ttu-id="ddf4c-115">Appel des fonctions XLL à partir de l’Assistant fonction ou remplacer des boîtes de dialogue</span><span class="sxs-lookup"><span data-stu-id="ddf4c-115">Call XLL Functions from the Function Wizard or Replace Dialog Boxes</span></span>](how-to-call-xll-functions-from-the-function-wizard-or-replace-dialog-boxes.md)
  
- [<span data-ttu-id="ddf4c-116">Appel dans Excel � partir du fichier DLL ou XLL</span><span class="sxs-lookup"><span data-stu-id="ddf4c-116">Calling into Excel from the DLL or XLL</span></span>](calling-into-excel-from-the-dll-or-xll.md)
  
- [<span data-ttu-id="ddf4c-117">Cr�ation de XLL</span><span class="sxs-lookup"><span data-stu-id="ddf4c-117">Creating XLLs</span></span>](creating-xlls.md)
  
- [<span data-ttu-id="ddf4c-118">�valuer les noms et les autres Expressions de formule de feuille de calcul</span><span class="sxs-lookup"><span data-stu-id="ddf4c-118">Evaluating Names and Other Worksheet Formula Expressions</span></span>](evaluating-names-and-other-worksheet-formula-expressions.md)
  
- [<span data-ttu-id="ddf4c-119">Multithread et gestion de la mémoire</span><span class="sxs-lookup"><span data-stu-id="ddf4c-119">Multithreading and Memory Management</span></span>](multithreading-and-memory-management.md)
  
- [<span data-ttu-id="ddf4c-120">Fonctions asynchrones définies par l’utilisateur</span><span class="sxs-lookup"><span data-stu-id="ddf4c-120">Asynchronous User-Defined Functions</span></span>](asynchronous-user-defined-functions.md)
  
- [<span data-ttu-id="ddf4c-121">Fonctions sécurisées pour le cluster</span><span class="sxs-lookup"><span data-stu-id="ddf4c-121">Cluster Safe Functions</span></span>](cluster-safe-functions.md)
  
- [<span data-ttu-id="ddf4c-122">Autorisation utilisateur sauts dans les opérations de longue durée</span><span class="sxs-lookup"><span data-stu-id="ddf4c-122">Permitting User Breaks in Lengthy Operations</span></span>](permitting-user-breaks-in-lengthy-operations.md)
  
- [<span data-ttu-id="ddf4c-123">Affichage des boîtes de dialogue à partir d’une DLL ou XLL</span><span class="sxs-lookup"><span data-stu-id="ddf4c-123">Displaying Dialog Boxes from Within a DLL or XLL</span></span>](displaying-dialog-boxes-from-within-a-dll-or-xll.md)
  
- [<span data-ttu-id="ddf4c-124">Instance d’Excel Access et les poignées de la fenêtre principale</span><span class="sxs-lookup"><span data-stu-id="ddf4c-124">Access Excel Instance and Main Window Handles</span></span>](how-to-access-excel-instance-and-main-window-handles.md)
  
- [<span data-ttu-id="ddf4c-125">Compatibilité descendante</span><span class="sxs-lookup"><span data-stu-id="ddf4c-125">Backward Compatibility</span></span>](backward-compatibility.md)
  

