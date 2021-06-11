---
title: Fonctions dans le fichier DLL générique
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: overview
keywords:
- generic dll [excel 2007], functions,functions [Excel 2007], Generic DLL
localization_priority: Normal
ms.assetid: 80ce2247-d69d-45b0-b5e2-4ff0d7078a2c
description: 'S’applique à : Excel 2013 | Office 2013 | Visual Studio'
ms.openlocfilehash: 3064e1a09ad8850e121da678f3702a6236574599
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/28/2019
ms.locfileid: "33420597"
---
# <a name="functions-in-the-generic-dll"></a><span data-ttu-id="fce06-104">Fonctions dans le fichier DLL générique</span><span class="sxs-lookup"><span data-stu-id="fce06-104">Functions in the Generic DLL</span></span>

 <span data-ttu-id="fce06-105">**S’applique à** : Excel 2013 | Office 2013 | Visual Studio</span><span class="sxs-lookup"><span data-stu-id="fce06-105">**Applies to**: Excel 2013 | Office 2013 | Visual Studio</span></span> 
  
<span data-ttu-id="fce06-106">Le dossier contient les Microsoft Visual Studio de projet et les fichiers de code source nécessaires pour compiler l’exemple `\EXAMPLES\GENERIC\` DLL GENERIC.xll.</span><span class="sxs-lookup"><span data-stu-id="fce06-106">The folder  `\EXAMPLES\GENERIC\` contains Microsoft Visual Studio project files and source code files that are needed to compile the example DLL GENERIC.xll.</span></span> <span data-ttu-id="fce06-107">Vous pouvez utiliser ce projet comme modèle pour écrire votre propre Microsoft Excel XL.</span><span class="sxs-lookup"><span data-stu-id="fce06-107">You can use this project as a template for writing your own Microsoft Excel XLLs.</span></span> <span data-ttu-id="fce06-108">Le code source de ce projet illustre de nombreuses fonctionnalités de l’API Excel C.</span><span class="sxs-lookup"><span data-stu-id="fce06-108">The source code in this project demonstrates many of the features of the Excel C API.</span></span> 
  
<span data-ttu-id="fce06-109">Lorsque vous chargez GENERIC.xll, il crée un menu **générique** avec quatre commandes :</span><span class="sxs-lookup"><span data-stu-id="fce06-109">When you load GENERIC.xll, it creates a new **Generic** menu with four commands:</span></span> 
  
- <span data-ttu-id="fce06-110">**Boîte** de dialogue : affiche une boîte Microsoft Excel dialogue.</span><span class="sxs-lookup"><span data-stu-id="fce06-110">**Dialog** - Displays a Microsoft Excel dialog box.</span></span> 
    
- <span data-ttu-id="fce06-111">**- Déplace** la sélection jusqu’à ce que vous appuyiez sur la **touche ÉCHAP.**</span><span class="sxs-lookup"><span data-stu-id="fce06-111">**Dance** - Moves the selection around until you press the **ESC** key.</span></span> 
    
- <span data-ttu-id="fce06-112">**Boîte de dialogue** native : affiche une boîte Windows dialogue.</span><span class="sxs-lookup"><span data-stu-id="fce06-112">**Native Dialog** - Displays a Windows dialog box.</span></span> 
    
- <span data-ttu-id="fce06-113">**Exit** : décharge GENERIC.xll et supprime le menu **générique.**</span><span class="sxs-lookup"><span data-stu-id="fce06-113">**Exit** - Unloads GENERIC.xll and removes the **Generic** menu.</span></span> 
    
<span data-ttu-id="fce06-114">GENERIC.xll fournit également trois fonctions de feuille de calcul, Func1, FuncSum et FuncFib, qui peuvent être utilisées chaque fois que GENERIC.xll est chargé.</span><span class="sxs-lookup"><span data-stu-id="fce06-114">GENERIC.xll also provides three worksheet functions, Func1, FuncSum, and FuncFib, which can be used whenever GENERIC.xll is loaded.</span></span> <span data-ttu-id="fce06-115">GENERIC.xll peut être chargé à l’aide du Gestionnaire de Excel, ou il est chargé s’il était actif à la fin normale de la dernière session Excel session.</span><span class="sxs-lookup"><span data-stu-id="fce06-115">GENERIC.xll can be loaded using the Add-in Manager, or it is loaded if it was active at the normal end of the last Excel session.</span></span>
  
<span data-ttu-id="fce06-116">Ce projet utilise la bibliothèque d’infrastructure (FRMWRK32.lib).</span><span class="sxs-lookup"><span data-stu-id="fce06-116">This project uses the framework library (FRMWRK32.lib).</span></span>
  
## <a name="in-this-section"></a><span data-ttu-id="fce06-117">Dans cette section</span><span class="sxs-lookup"><span data-stu-id="fce06-117">In this section</span></span>

[<span data-ttu-id="fce06-118">DIALOGMsgProc</span><span class="sxs-lookup"><span data-stu-id="fce06-118">DIALOGMsgProc</span></span>](dialogmsgproc.md)
  
[<span data-ttu-id="fce06-119">ExcelCursorProc</span><span class="sxs-lookup"><span data-stu-id="fce06-119">ExcelCursorProc</span></span>](excelcursorproc.md)
  
[<span data-ttu-id="fce06-120">HookExcelWindow</span><span class="sxs-lookup"><span data-stu-id="fce06-120">HookExcelWindow</span></span>](hookexcelwindow.md)
  
[<span data-ttu-id="fce06-121">UnhookExcelWindow</span><span class="sxs-lookup"><span data-stu-id="fce06-121">UnhookExcelWindow</span></span>](unhookexcelwindow.md)
  
[<span data-ttu-id="fce06-122">fShowDialog</span><span class="sxs-lookup"><span data-stu-id="fce06-122">fShowDialog</span></span>](fshowdialog.md)
  
[<span data-ttu-id="fce06-123">fDance</span><span class="sxs-lookup"><span data-stu-id="fce06-123">fDance</span></span>](fdance.md)
  
[<span data-ttu-id="fce06-124">fDialog/fDialog12</span><span class="sxs-lookup"><span data-stu-id="fce06-124">fDialog/fDialog12</span></span>](fdialog-fdialog12.md)
  
[<span data-ttu-id="fce06-125">fExit</span><span class="sxs-lookup"><span data-stu-id="fce06-125">fExit</span></span>](fexit.md)
  
[<span data-ttu-id="fce06-126">Func1</span><span class="sxs-lookup"><span data-stu-id="fce06-126">Func1</span></span>](func1.md)
  
[<span data-ttu-id="fce06-127">FuncSum</span><span class="sxs-lookup"><span data-stu-id="fce06-127">FuncSum</span></span>](funcsum.md)
  
[<span data-ttu-id="fce06-128">FuncFib</span><span class="sxs-lookup"><span data-stu-id="fce06-128">FuncFib</span></span>](funcfib.md)
  
## <a name="see-also"></a><span data-ttu-id="fce06-129">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="fce06-129">See also</span></span>



[<span data-ttu-id="fce06-130">Fonctions de la bibliothèque Framework</span><span class="sxs-lookup"><span data-stu-id="fce06-130">Functions in the Framework Library</span></span>](functions-in-the-framework-library.md)

