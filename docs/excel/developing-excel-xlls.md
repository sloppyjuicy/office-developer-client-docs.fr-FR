---
title: Développement de fichiers XLL Excel
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: overview
keywords:
- compléments - [Excel 2007], développer des fichiers XLL - [Excel 2007], fichiers XLL - [Excel 2007], développer
ms.assetid: dd27ae4d-ef97-47db-885c-ddd955816900
description: 'S’applique à : Excel 2013 | Office 2013 | Visual Studio'
localization_priority: Priority
ms.openlocfilehash: d05041f2629694c4a96240ea83b6e84b17f9be38
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: HT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32301658"
---
# <a name="developing-excel-xlls"></a><span data-ttu-id="cfc7e-104">Développement de fichiers XLL Excel</span><span class="sxs-lookup"><span data-stu-id="cfc7e-104">Developing Excel XLLs</span></span>

<span data-ttu-id="cfc7e-105">**S’applique à**: Excel 2013 | Office 2013 | Visual Studio</span><span class="sxs-lookup"><span data-stu-id="cfc7e-105">**Applies to**: Excel 2013 | Office 2013 | Visual Studio</span></span> 
  
<span data-ttu-id="cfc7e-106">La principale raison d’écrire des fichiers XLL Microsoft Excel et d’utiliser l’API C est de créer des fonctions de feuille de calcul hautes performances.</span><span class="sxs-lookup"><span data-stu-id="cfc7e-106">The primary reason for writing Microsoft Excel XLLs and using the C API is to create high-performance worksheet functions.</span></span> <span data-ttu-id="cfc7e-107">Les applications des fonctions hautes performances (et dans Excel 2007, la possibilité d’écrire des interfaces multithreads vers des ressources serveur puissantes) en font un axe essentiel de l’extensibilité d’Excel.</span><span class="sxs-lookup"><span data-stu-id="cfc7e-107">The applications of high-performance functions—and, starting in Excel 2007, the ability to write multithreaded interfaces to powerful server resources—make it a very important part of Excel extensibility.</span></span> <span data-ttu-id="cfc7e-108">Les performances des fichiers XLL ont été davantage améliorées dans Excel 2007 grâce à l’ajout de nouveaux types de données et, surtout, à la prise en charge du multithreading.</span><span class="sxs-lookup"><span data-stu-id="cfc7e-108">The performance of XLLs was further enhanced in Excel 2007 by the addition of new data types and, most important, support for multithreading.</span></span>
  
<span data-ttu-id="cfc7e-109">L’API C ne possède aucune des fonctionnalités de développement rapide de niveau supérieur de Microsoft Visual Basic pour Applications (VBA), COM ou Microsoft .NET Framework.</span><span class="sxs-lookup"><span data-stu-id="cfc7e-109">The C API has none of the higher-level rapid development features of Microsoft Visual Basic for Applications (VBA), COM, or the Microsoft .NET Framework.</span></span> <span data-ttu-id="cfc7e-110">La gestion de la mémoire opère à faible niveau et, par conséquent, fait peser plus de responsabilités sur le développeur.</span><span class="sxs-lookup"><span data-stu-id="cfc7e-110">Memory management is low level, and therefore puts greater responsibility on the developer.</span></span> <span data-ttu-id="cfc7e-111">La plupart des fonctionnalités d’Excel exposées par le biais de COM, ce qui les rend accessibles par le biais de .NET Framework et de VBA, ne sont pas exposées à l’API C.</span><span class="sxs-lookup"><span data-stu-id="cfc7e-111">Many Excel features that are exposed through COM, making them available through VBA and the .NET Framework, are not exposed to the C API.</span></span>


- [<span data-ttu-id="cfc7e-112">Concepts de programmation Excel</span><span class="sxs-lookup"><span data-stu-id="cfc7e-112">Excel Programming Concepts</span></span>](excel-programming-concepts.md)
  
- [<span data-ttu-id="cfc7e-113">Utilisation des fichiers DLL</span><span class="sxs-lookup"><span data-stu-id="cfc7e-113">Working with DLLs</span></span>](working-with-dlls.md)
  
- [<span data-ttu-id="cfc7e-114">Accés au code XLL dans Excel</span><span class="sxs-lookup"><span data-stu-id="cfc7e-114">Accessing XLL Code in Excel</span></span>](accessing-xll-code-in-excel.md)
  
- [<span data-ttu-id="cfc7e-115">Appel des fonctions XLL à partir de l’Assistant Fonction ou des boîtes de dialogue Remplacer</span><span class="sxs-lookup"><span data-stu-id="cfc7e-115">Call XLL Functions from the Function Wizard or Replace Dialog Boxes</span></span>](how-to-call-xll-functions-from-the-function-wizard-or-replace-dialog-boxes.md)
  
- [<span data-ttu-id="cfc7e-116">Appel dans Excel � partir du fichier DLL ou XLL</span><span class="sxs-lookup"><span data-stu-id="cfc7e-116">Calling into Excel from the DLL or XLL</span></span>](calling-into-excel-from-the-dll-or-xll.md)
  
- [<span data-ttu-id="cfc7e-117">Création de XLL</span><span class="sxs-lookup"><span data-stu-id="cfc7e-117">Creating XLLs</span></span>](creating-xlls.md)
  
- [<span data-ttu-id="cfc7e-118">Évaluer les noms et les autres Expressions de formule de feuille de calcul</span><span class="sxs-lookup"><span data-stu-id="cfc7e-118">Evaluating Names and Other Worksheet Formula Expressions</span></span>](evaluating-names-and-other-worksheet-formula-expressions.md)
  
- [<span data-ttu-id="cfc7e-119">Multithreading et gestion de la mémoire</span><span class="sxs-lookup"><span data-stu-id="cfc7e-119">Multithreading and Memory Management</span></span>](multithreading-and-memory-management.md)
  
- [<span data-ttu-id="cfc7e-120">Fonctions asynchrones définies par l’utilisateur</span><span class="sxs-lookup"><span data-stu-id="cfc7e-120">Asynchronous User-Defined Functions</span></span>](asynchronous-user-defined-functions.md)
  
- [<span data-ttu-id="cfc7e-121">Fonctions sécurisées pour le cluster</span><span class="sxs-lookup"><span data-stu-id="cfc7e-121">Cluster Safe Functions</span></span>](cluster-safe-functions.md)
  
- [<span data-ttu-id="cfc7e-122">Autorisation des interruptions utilisateur lors des opérations très longues</span><span class="sxs-lookup"><span data-stu-id="cfc7e-122">Permitting User Breaks in Lengthy Operations</span></span>](permitting-user-breaks-in-lengthy-operations.md)
  
- [<span data-ttu-id="cfc7e-123">Affichage des boîtes de dialogue dans un fichier DLL ou XLL</span><span class="sxs-lookup"><span data-stu-id="cfc7e-123">Displaying Dialog Boxes from Within a DLL or XLL</span></span>](displaying-dialog-boxes-from-within-a-dll-or-xll.md)
  
- [<span data-ttu-id="cfc7e-124">Accès à l’instance Excel et aux handles de fenêtre principaux</span><span class="sxs-lookup"><span data-stu-id="cfc7e-124">Access Excel Instance and Main Window Handles</span></span>](how-to-access-excel-instance-and-main-window-handles.md)
  
- [<span data-ttu-id="cfc7e-125">Compatibilité descendante</span><span class="sxs-lookup"><span data-stu-id="cfc7e-125">Backward Compatibility</span></span>](backward-compatibility.md)
  

