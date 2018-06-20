---
title: Commandes, fonctions et états Excel
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: overview
keywords:
- États [excel 2007], [Excel 2007] de commandes, fonctions de feuille de calcul [Excel 2007], les fonctions de feuille macro [Excel 2007], États Excel
localization_priority: Normal
ms.assetid: 20f19aa4-f184-47be-bcdd-7ded78778974
description: 'S�applique �: Excel 2013�| Office 2013�| Visual Studio'
ms.openlocfilehash: 60977216663fb2492f425a9b7c855b77815f0e7b
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19782048"
---
# <a name="excel-commands-functions-and-states"></a><span data-ttu-id="1322c-104">Commandes, fonctions et états Excel</span><span class="sxs-lookup"><span data-stu-id="1322c-104">Excel Commands, Functions, and States</span></span>

 <span data-ttu-id="1322c-105">**S’applique à**: Excel 2013 | Office 2013 | Visual Studio</span><span class="sxs-lookup"><span data-stu-id="1322c-105">**Applies to**: Excel 2013 | Office 2013 | Visual Studio</span></span> 
  
<span data-ttu-id="1322c-106">Microsoft Excel reconnaît deux types de nouvelles fonctionnalités très différents : les fonctions et les commandes.</span><span class="sxs-lookup"><span data-stu-id="1322c-106">Microsoft Excel recognizes two very different types of added functionality: commands and functions.</span></span>
  
## <a name="commands"></a><span data-ttu-id="1322c-107">Commandes</span><span class="sxs-lookup"><span data-stu-id="1322c-107">Commands</span></span>

<span data-ttu-id="1322c-108">Dans Excel, les commandes ont les caractéristiques suivantes :</span><span class="sxs-lookup"><span data-stu-id="1322c-108">In Excel, commands have the following characteristics:</span></span>
  
- <span data-ttu-id="1322c-109">Ils permettent d’actions de la même manière que les utilisateurs.</span><span class="sxs-lookup"><span data-stu-id="1322c-109">They perform actions in the same way that users do.</span></span>
    
- <span data-ttu-id="1322c-110">Ils peuvent faire tout ce qu’un utilisateur peut faire (sujet aux limites de l’interface utilisée), telles que la modification des paramètres d’Excel, l’ouverture, fermeture et modifier des documents, lancement recalculs et ainsi de suite.</span><span class="sxs-lookup"><span data-stu-id="1322c-110">They can do anything a user can do (subject to the limits of the interface used), such as altering Excel settings, opening, closing, and editing documents, initiating recalculations, and so on.</span></span>
    
- <span data-ttu-id="1322c-111">Elles peuvent être définies à appeler lorsque certains événements interceptées se produisent.</span><span class="sxs-lookup"><span data-stu-id="1322c-111">They can be set up to be called when certain trapped events occur.</span></span>
    
- <span data-ttu-id="1322c-112">Ils peuvent afficher des boîtes de dialogue et interagir avec l’utilisateur.</span><span class="sxs-lookup"><span data-stu-id="1322c-112">They can display dialog boxes and interact with the user.</span></span>
    
- <span data-ttu-id="1322c-113">Ils peuvent être liés pour contrôler des objets afin qu’ils sont appelées lors de certaines actions sur cet objet, telles que clic gauche.</span><span class="sxs-lookup"><span data-stu-id="1322c-113">They can be linked to control objects so that they are called when some action is taken on that object, such as left-clicking.</span></span>
    
- <span data-ttu-id="1322c-114">Ils ne sont jamais appelés par Excel pendant le recalcul.</span><span class="sxs-lookup"><span data-stu-id="1322c-114">They are never called by Excel during a recalculation.</span></span>
    
- <span data-ttu-id="1322c-115">Elles ne peut pas être appelées par les fonctions pendant un nouveau calcul.</span><span class="sxs-lookup"><span data-stu-id="1322c-115">They cannot be called by functions during a recalculation.</span></span>
    
## <a name="functions"></a><span data-ttu-id="1322c-116">Fonctions</span><span class="sxs-lookup"><span data-stu-id="1322c-116">Functions</span></span>

<span data-ttu-id="1322c-117">Fonctions d’Excel procédez comme suit :</span><span class="sxs-lookup"><span data-stu-id="1322c-117">Functions in Excel do the following:</span></span>
  
- <span data-ttu-id="1322c-118">Ils prennent généralement des arguments et renvoient toujours un résultat.</span><span class="sxs-lookup"><span data-stu-id="1322c-118">They usually take arguments and always return a result.</span></span>
    
- <span data-ttu-id="1322c-119">Ils peuvent être saisis dans une ou plusieurs cellules en tant que partie d’une formule Excel.</span><span class="sxs-lookup"><span data-stu-id="1322c-119">They can be entered into one or more cells as part of an Excel formula.</span></span>
    
- <span data-ttu-id="1322c-120">Ils peuvent être utilisés dans les définitions de nom défini.</span><span class="sxs-lookup"><span data-stu-id="1322c-120">They can be used in defined name definitions.</span></span>
    
- <span data-ttu-id="1322c-121">Ils peuvent être utilisés dans la limite de mise en forme conditionnelle et d’expressions de seuil.</span><span class="sxs-lookup"><span data-stu-id="1322c-121">They can be used in conditional formatting limit and threshold expressions.</span></span>
    
- <span data-ttu-id="1322c-122">Ils peuvent être appelées par les commandes.</span><span class="sxs-lookup"><span data-stu-id="1322c-122">They can be called by commands.</span></span>
    
- <span data-ttu-id="1322c-123">Ils ne peuvent pas appeler des commandes.</span><span class="sxs-lookup"><span data-stu-id="1322c-123">They cannot call commands.</span></span>
    
<span data-ttu-id="1322c-124">Excel établit une distinction supplémentaire entre les fonctions de feuille de calcul défini par l’utilisateur et des fonctions définies par l’utilisateur sont conçues pour fonctionner dans des feuilles macro.</span><span class="sxs-lookup"><span data-stu-id="1322c-124">Excel makes a further distinction between user-defined worksheet functions and user-defined functions that are designed to work on macro sheets.</span></span> <span data-ttu-id="1322c-125">Excel ne limite pas les fonctions de feuille macro définie par l’utilisateur uniquement à utilisé dans les feuilles de macro : ces fonctions peuvent être utilisées n’importe où une fonction de feuille de calcul normale peut être utilisée.</span><span class="sxs-lookup"><span data-stu-id="1322c-125">Excel does not limit user-defined macro sheet functions only to being used on macro sheets: these functions can be used anywhere a normal worksheet function can be used.</span></span>
  
### <a name="worksheet-functions"></a><span data-ttu-id="1322c-126">Objet Worksheet Functions</span><span class="sxs-lookup"><span data-stu-id="1322c-126">Worksheet Functions</span></span>

<span data-ttu-id="1322c-127">Vous trouverez ci-dessous des fonctions de feuille de calcul Excel :</span><span class="sxs-lookup"><span data-stu-id="1322c-127">The following is true of Excel worksheet functions:</span></span>
  
- <span data-ttu-id="1322c-128">Ils ne peut pas accéder aux fonctions d’information de feuille de macro.</span><span class="sxs-lookup"><span data-stu-id="1322c-128">They cannot access macro sheet information functions.</span></span>
    
- <span data-ttu-id="1322c-129">Ils ne peuvent pas obtenir les valeurs des cellules non calculées.</span><span class="sxs-lookup"><span data-stu-id="1322c-129">They cannot obtain the values of uncalculated cells.</span></span>
    
- <span data-ttu-id="1322c-130">Ils peuvent être écrites et enregistrés en tant que thread-safe à compter d’Excel 2007.</span><span class="sxs-lookup"><span data-stu-id="1322c-130">They can be written and registered as thread-safe starting in Excel 2007.</span></span>
    
### <a name="macro-sheet-functions"></a><span data-ttu-id="1322c-131">Fonctions de feuille macro</span><span class="sxs-lookup"><span data-stu-id="1322c-131">Macro-Sheet Functions</span></span>

<span data-ttu-id="1322c-132">Vous trouverez ci-dessous des fonctions de feuille macro Excel :</span><span class="sxs-lookup"><span data-stu-id="1322c-132">The following is true of Excel macro-sheet functions:</span></span>
  
- <span data-ttu-id="1322c-133">Ils peuvent accéder des fonctions d’information feuille macro.</span><span class="sxs-lookup"><span data-stu-id="1322c-133">They can access macro sheet information functions.</span></span>
    
- <span data-ttu-id="1322c-134">Ils peuvent obtenir les valeurs des cellules non calculées, y compris les valeurs des cellules d’appel.</span><span class="sxs-lookup"><span data-stu-id="1322c-134">They can obtain the values of uncalculated cells including the values of the calling cells.</span></span>
    
- <span data-ttu-id="1322c-135">Ils ne sont pas considérées thread fiables à compter d’Excel 2007.</span><span class="sxs-lookup"><span data-stu-id="1322c-135">They are not considered thread safe starting in Excel 2007.</span></span>
    
<span data-ttu-id="1322c-136">Comment Excel traite une fonction définie par l’utilisateur (UDF), ce qui permet la fonction faire et comment il recalcule la fonction sont déterminés tout lorsque vous enregistrez la fonction.</span><span class="sxs-lookup"><span data-stu-id="1322c-136">How Excel treats a user-defined function (UDF), what it permits the function to do, and how it recalculates the function are all determined when you register the function.</span></span> <span data-ttu-id="1322c-137">Si une fonction est enregistrée comme une fonction de feuille de calcul mais tente de faire quelque chose que seule une fonction de feuille macro, l’opération échoue.</span><span class="sxs-lookup"><span data-stu-id="1322c-137">If a function is registered as a worksheet function but tries to do something that only a macro-sheet function can do, the operation fails.</span></span> <span data-ttu-id="1322c-138">À compter d’Excel 2007, si une fonction de feuille de calcul enregistrée en tant que thread-safe tente d’appeler une fonction de feuille macro, là encore, l’opération échoue.</span><span class="sxs-lookup"><span data-stu-id="1322c-138">Starting in Excel 2007, if a worksheet function registered as thread safe tries to call a macro sheet function, again, the operation fails.</span></span>
  
<span data-ttu-id="1322c-139">Excel traite Microsoft Visual Basic pour Applications (VBA) UDF en tant que fonctions équivalent de la feuille de macro, dans la mesure où ils peuvent accéder aux informations de l’espace de travail et la valeur de cellules non calculées, et ils ne sont pas considérées comme thread fiables à compter d’Excel 2007.</span><span class="sxs-lookup"><span data-stu-id="1322c-139">Excel treats Microsoft Visual Basic for Applications (VBA) UDFs as macro sheet-equivalent functions, in that they can access workspace information and the value of uncalculated cells, and they are not considered as thread safe starting in Excel 2007.</span></span>
  
## <a name="excel-states"></a><span data-ttu-id="1322c-140">États Excel</span><span class="sxs-lookup"><span data-stu-id="1322c-140">Excel States</span></span>

<span data-ttu-id="1322c-141">Excel peut être dans un des différents États à un moment donné en fonction des actions de l’utilisateur, un processus externe, un événement interceptée exécutant une macro ou un événement de maintenance Excel chronométré comme **enregistrement automatique**.</span><span class="sxs-lookup"><span data-stu-id="1322c-141">Excel can be in one of a number of states at any given time depending on the actions of the user, an external process, a trapped event running a macro, or a timed Excel housekeeping event such as **Autosave**.</span></span>
  
<span data-ttu-id="1322c-142">Les états possibles d’une expérience de l’utilisateur sont les suivantes :</span><span class="sxs-lookup"><span data-stu-id="1322c-142">The states that the user experiences are as follows:</span></span>
  
- <span data-ttu-id="1322c-143">**Prêt état :** Aucun commandes ou des macros ne sont en cours d’exécution.</span><span class="sxs-lookup"><span data-stu-id="1322c-143">**Ready state:** No commands or macros are being run.</span></span> <span data-ttu-id="1322c-144">Aucune boîte de dialogue n’est affichés.</span><span class="sxs-lookup"><span data-stu-id="1322c-144">No dialog boxes are being displayed.</span></span> <span data-ttu-id="1322c-145">Aucune cellule n’est en cours de modification et l’utilisateur n’est pas au milieu d’une opération de couper/copier et coller.</span><span class="sxs-lookup"><span data-stu-id="1322c-145">No cells are being edited and the user is not in the middle of a cut/copy and paste operation.</span></span> <span data-ttu-id="1322c-146">Aucun objet incorporé n’a le focus.</span><span class="sxs-lookup"><span data-stu-id="1322c-146">No embedded object has focus.</span></span> 
    
- <span data-ttu-id="1322c-147">**En mode édition :** L’utilisateur a commencé à taper les caractères d’entrée valides dans une cellule déverrouillée ou non protégée, ou a appuyé sur **F2** sur une ou plusieurs cellules déverrouillées ou non protégées.</span><span class="sxs-lookup"><span data-stu-id="1322c-147">**Edit mode:** The user has started to type valid input characters into an unlocked or unprotected cell, or has pressed **F2** on one or more unlocked or unprotected cells.</span></span> 
    
- <span data-ttu-id="1322c-148">**Mode Couper/copier et coller :** L’utilisateur a Couper ou copier une cellule ou plage de cellules et n’a pas encore collé les ou a collée à l’aide de la boîte de dialogue Collage spécial qui permet à plusieurs opérations de collage.</span><span class="sxs-lookup"><span data-stu-id="1322c-148">**Cut/copy and paste mode:** The user has cut or copied a cell or range of cells and has not yet pasted them, or has pasted them using the paste-special dialog box, which enables multiple paste operations.</span></span> 
    
- <span data-ttu-id="1322c-149">**En mode point :** L’utilisateur modifie une formule et sélectionne les cellules dont les adresses sont ajoutés à la formule en cours de modification.</span><span class="sxs-lookup"><span data-stu-id="1322c-149">**Point mode:** The user is editing a formula and is selecting cells whose addresses are added to the formula being edited.</span></span> 
    
<span data-ttu-id="1322c-150">L’utilisateur peut désactiver le mode édition, point et couper/copier en appuyant sur la touche **ÉCHAP** , ce qui rétablit l’état prêt Excel.</span><span class="sxs-lookup"><span data-stu-id="1322c-150">The user can clear the edit, point, and cut/copy modes by pressing the **ESC** key, which returns Excel to its ready state.</span></span> <span data-ttu-id="1322c-151">Autres événements peuvent désactiver ces États, telles que les suivantes :</span><span class="sxs-lookup"><span data-stu-id="1322c-151">Other events can clear these states, such as the following:</span></span> 
  
- <span data-ttu-id="1322c-152">L’utilisateur ouvre une boîte de dialogue intégrée.</span><span class="sxs-lookup"><span data-stu-id="1322c-152">The user opens a built-in dialog box.</span></span>
    
- <span data-ttu-id="1322c-153">L’utilisateur lance un nouveau calcul.</span><span class="sxs-lookup"><span data-stu-id="1322c-153">The user initiates a recalculation.</span></span>
    
- <span data-ttu-id="1322c-154">L’utilisateur exécute une commande.</span><span class="sxs-lookup"><span data-stu-id="1322c-154">The user runs a command.</span></span>
    
- <span data-ttu-id="1322c-155">Excel effectue une opération **d’enregistrement** .</span><span class="sxs-lookup"><span data-stu-id="1322c-155">Excel performs an **Autosave** operation.</span></span> 
    
- <span data-ttu-id="1322c-156">Un événement de minuterie est intercepté.</span><span class="sxs-lookup"><span data-stu-id="1322c-156">A timer event is trapped.</span></span>
    
<span data-ttu-id="1322c-157">L’exemple précédent est important pour complément aux développeurs.</span><span class="sxs-lookup"><span data-stu-id="1322c-157">The last example is of importance to add-in developers.</span></span> <span data-ttu-id="1322c-158">Vous devez tenir compte l’impact de l’utilisation d’Excel où événement timer fréquents intercepte normale est définie et exécutée.</span><span class="sxs-lookup"><span data-stu-id="1322c-158">You should consider the impact of the normal usability of Excel where frequent timer event traps are being set and executed.</span></span> <span data-ttu-id="1322c-159">Lorsqu’il s’agit d’une part importante de la fonctionnalité de votre complément, vous devez fournir aux utilisateurs un moyen de suspension, afin qu’ils puissent couper/copier et coller normalement lorsqu’ils ont besoin de facilement accessible.</span><span class="sxs-lookup"><span data-stu-id="1322c-159">When this is an important part of your add-in's functionality, you should provide users with an easily accessible way of suspending it, so that they can cut/copy and paste normally when they need to.</span></span>
  
## <a name="see-also"></a><span data-ttu-id="1322c-160">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="1322c-160">See also</span></span>



[<span data-ttu-id="1322c-161">Concepts de programmation Excel</span><span class="sxs-lookup"><span data-stu-id="1322c-161">Excel Programming Concepts</span></span>](excel-programming-concepts.md)
  
[<span data-ttu-id="1322c-162">Autorisation utilisateur sauts dans les opérations de longue durée</span><span class="sxs-lookup"><span data-stu-id="1322c-162">Permitting User Breaks in Lengthy Operations</span></span>](permitting-user-breaks-in-lengthy-operations.md)

