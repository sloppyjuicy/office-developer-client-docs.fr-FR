---
title: Fonctions de la DLL générique
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: overview
keywords:
- dll générique [excel 2007], fonctions, [Excel 2007], DLL générique
localization_priority: Normal
ms.assetid: 80ce2247-d69d-45b0-b5e2-4ff0d7078a2c
description: 'S�applique �: Excel 2013�| Office 2013�| Visual Studio'
ms.openlocfilehash: e78f276e58ca1c98786e28ed5167762cf0bfdf7f
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19782144"
---
# <a name="functions-in-the-generic-dll"></a><span data-ttu-id="7569b-104">Fonctions de la DLL générique</span><span class="sxs-lookup"><span data-stu-id="7569b-104">Functions in the Generic DLL</span></span>

 <span data-ttu-id="7569b-105">**S’applique à**: Excel 2013 | Office 2013 | Visual Studio</span><span class="sxs-lookup"><span data-stu-id="7569b-105">**Applies to**: Excel 2013 | Office 2013 | Visual Studio</span></span> 
  
<span data-ttu-id="7569b-106">Le dossier `\EXAMPLES\GENERIC\` contient les fichiers de projet Microsoft Visual Studio et des fichiers de code source qui sont nécessaires pour compiler l’exemple de DLL GENERIC.xll.</span><span class="sxs-lookup"><span data-stu-id="7569b-106">The folder  `\EXAMPLES\GENERIC\` contains Microsoft Visual Studio project files and source code files that are needed to compile the example DLL GENERIC.xll.</span></span> <span data-ttu-id="7569b-107">Vous pouvez utiliser ce projet comme modèle pour écrire vos propres solutions de XLL Microsoft Excel.</span><span class="sxs-lookup"><span data-stu-id="7569b-107">You can use this project as a template for writing your own Microsoft Excel XLLs.</span></span> <span data-ttu-id="7569b-108">Le code source dans ce projet illustre de nombreuses fonctionnalités de l’API C Excel.</span><span class="sxs-lookup"><span data-stu-id="7569b-108">The source code in this project demonstrates many of the features of the Excel C API.</span></span> 
  
<span data-ttu-id="7569b-109">Lorsque vous chargez GENERIC.xll, il crée un nouveau menu **générique** avec quatre commandes :</span><span class="sxs-lookup"><span data-stu-id="7569b-109">When you load GENERIC.xll, it creates a new **Generic** menu with four commands:</span></span> 
  
- <span data-ttu-id="7569b-110">**Boîte de dialogue** - affiche une boîte de dialogue Microsoft Excel.</span><span class="sxs-lookup"><span data-stu-id="7569b-110">**Dialog** - Displays a Microsoft Excel dialog box.</span></span> 
    
- <span data-ttu-id="7569b-111">**Danse** - déplace la sélection jusqu'à ce que vous appuyez sur la touche **ÉCHAP** .</span><span class="sxs-lookup"><span data-stu-id="7569b-111">**Dance** - Moves the selection around until you press the **ESC** key.</span></span> 
    
- <span data-ttu-id="7569b-112">**Boîte de dialogue native** - affiche une boîte de dialogue Windows.</span><span class="sxs-lookup"><span data-stu-id="7569b-112">**Native Dialog** - Displays a Windows dialog box.</span></span> 
    
- <span data-ttu-id="7569b-113">**Exit** - GENERIC.xll décharge et supprime le menu **générique** .</span><span class="sxs-lookup"><span data-stu-id="7569b-113">**Exit** - Unloads GENERIC.xll and removes the **Generic** menu.</span></span> 
    
<span data-ttu-id="7569b-114">GENERIC.xll fournit également trois fonctions de feuille de calcul, Func1, FuncSum et FuncFib, qui peut être utilisé chaque fois que GENERIC.xll est chargé.</span><span class="sxs-lookup"><span data-stu-id="7569b-114">GENERIC.xll also provides three worksheet functions, Func1, FuncSum, and FuncFib, which can be used whenever GENERIC.xll is loaded.</span></span> <span data-ttu-id="7569b-115">GENERIC.xll peuvent être chargés à l’aide du Gestionnaire de compléments, ou elle est chargée si elle a été actif à la fin de la dernière session Excel normale.</span><span class="sxs-lookup"><span data-stu-id="7569b-115">GENERIC.xll can be loaded using the Add-in Manager, or it is loaded if it was active at the normal end of the last Excel session.</span></span>
  
<span data-ttu-id="7569b-116">Ce projet utilise la bibliothèque framework (FRMWRK32.lib).</span><span class="sxs-lookup"><span data-stu-id="7569b-116">This project uses the framework library (FRMWRK32.lib).</span></span>
  
## <a name="in-this-section"></a><span data-ttu-id="7569b-117">Dans cette section</span><span class="sxs-lookup"><span data-stu-id="7569b-117">In this section</span></span>

[<span data-ttu-id="7569b-118">DIALOGMsgProc</span><span class="sxs-lookup"><span data-stu-id="7569b-118">DIALOGMsgProc</span></span>](dialogmsgproc.md)
  
[<span data-ttu-id="7569b-119">ExcelCursorProc</span><span class="sxs-lookup"><span data-stu-id="7569b-119">ExcelCursorProc</span></span>](excelcursorproc.md)
  
[<span data-ttu-id="7569b-120">HookExcelWindow</span><span class="sxs-lookup"><span data-stu-id="7569b-120">HookExcelWindow</span></span>](hookexcelwindow.md)
  
[<span data-ttu-id="7569b-121">UnhookExcelWindow</span><span class="sxs-lookup"><span data-stu-id="7569b-121">UnhookExcelWindow</span></span>](unhookexcelwindow.md)
  
[<span data-ttu-id="7569b-122">fShowDialog</span><span class="sxs-lookup"><span data-stu-id="7569b-122">fShowDialog</span></span>](fshowdialog.md)
  
[<span data-ttu-id="7569b-123">fDance</span><span class="sxs-lookup"><span data-stu-id="7569b-123">fDance</span></span>](fdance.md)
  
[<span data-ttu-id="7569b-124">fDialog/fDialog12</span><span class="sxs-lookup"><span data-stu-id="7569b-124">fDialog/fDialog12</span></span>](fdialog-fdialog12.md)
  
[<span data-ttu-id="7569b-125">fExit</span><span class="sxs-lookup"><span data-stu-id="7569b-125">fExit</span></span>](fexit.md)
  
[<span data-ttu-id="7569b-126">Func1</span><span class="sxs-lookup"><span data-stu-id="7569b-126">Func1</span></span>](func1.md)
  
[<span data-ttu-id="7569b-127">FuncSum</span><span class="sxs-lookup"><span data-stu-id="7569b-127">FuncSum</span></span>](funcsum.md)
  
[<span data-ttu-id="7569b-128">FuncFib</span><span class="sxs-lookup"><span data-stu-id="7569b-128">FuncFib</span></span>](funcfib.md)
  
## <a name="see-also"></a><span data-ttu-id="7569b-129">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="7569b-129">See also</span></span>



[<span data-ttu-id="7569b-130">Fonctions de la bibliothèque Framework</span><span class="sxs-lookup"><span data-stu-id="7569b-130">Functions in the Framework Library</span></span>](functions-in-the-framework-library.md)

