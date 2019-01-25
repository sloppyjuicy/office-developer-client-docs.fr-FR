---
title: États, fonctions et commandes Excel
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: overview
keywords:
- états [Excel 2007], commandes [Excel 2007], fonctions de feuille de calcul [Excel 2007], fonctions de feuille macro [Excel 2007], états Excel
ms.assetid: 20f19aa4-f184-47be-bcdd-7ded78778974
description: 'S’applique à : Excel 2013 | Office 2013 | Visual Studio'
localization_priority: Priority
ms.openlocfilehash: c941ba7445f1f0598bf044b5f177ad576df0137c
ms.sourcegitcommit: d6695c94415fa47952ee7961a69660abc0904434
ms.translationtype: HT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/17/2019
ms.locfileid: "28716235"
---
# <a name="excel-commands-functions-and-states"></a><span data-ttu-id="d6b4a-104">États, fonctions et commandes Excel</span><span class="sxs-lookup"><span data-stu-id="d6b4a-104">Excel Commands, Functions, and States</span></span>

 <span data-ttu-id="d6b4a-105">**S’applique à**: Excel 2013 | Office 2013 | Visual Studio</span><span class="sxs-lookup"><span data-stu-id="d6b4a-105">**Applies to**: Excel 2013 | Office 2013 | Visual Studio</span></span> 
  
<span data-ttu-id="d6b4a-106">Microsoft Excel reconnaît deux types de fonctionnalités ajoutées très différents : les commandes et les fonctions.</span><span class="sxs-lookup"><span data-stu-id="d6b4a-106">Microsoft Excel recognizes two very different types of added functionality: commands and functions.</span></span>
  
## <a name="commands"></a><span data-ttu-id="d6b4a-107">Commandes</span><span class="sxs-lookup"><span data-stu-id="d6b4a-107">Commands</span></span>

<span data-ttu-id="d6b4a-108">Dans Excel, les commandes présentent les caractéristiques suivantes :</span><span class="sxs-lookup"><span data-stu-id="d6b4a-108">In Excel, commands have the following characteristics:</span></span>
  
- <span data-ttu-id="d6b4a-109">Elles effectuent des actions de la même façon que les utilisateurs.</span><span class="sxs-lookup"><span data-stu-id="d6b4a-109">They perform actions in the same way that users do.</span></span>
    
- <span data-ttu-id="d6b4a-110">Elles peuvent faire tout ce qu’un utilisateur peut faire (dans les limites de l’interface utilisée) : changer des paramètres Excel, ouvrir, fermer et modifier des documents, démarrer des recalculs, etc.</span><span class="sxs-lookup"><span data-stu-id="d6b4a-110">They can do anything a user can do (subject to the limits of the interface used), such as altering Excel settings, opening, closing, and editing documents, initiating recalculations, and so on.</span></span>
    
- <span data-ttu-id="d6b4a-111">Elles peuvent être configurées pour être appelées lorsque certains événements bloqués se produisent.</span><span class="sxs-lookup"><span data-stu-id="d6b4a-111">They can be set up to be called when certain trapped events occur.</span></span>
    
- <span data-ttu-id="d6b4a-112">Elles peuvent afficher des boîtes de dialogue et interagir avec l’utilisateur.</span><span class="sxs-lookup"><span data-stu-id="d6b4a-112">They can display dialog boxes and interact with the user.</span></span>
    
- <span data-ttu-id="d6b4a-113">Elles peuvent être liées pour contrôler des objets afin d’être appelées lorsqu’une action est effectuée sur cet objet (clic gauche, par exemple).</span><span class="sxs-lookup"><span data-stu-id="d6b4a-113">They can be linked to control objects so that they are called when some action is taken on that object, such as left-clicking.</span></span>
    
- <span data-ttu-id="d6b4a-114">Elles ne sont jamais appelés par Excel lors d’un recalcul.</span><span class="sxs-lookup"><span data-stu-id="d6b4a-114">They are never called by Excel during a recalculation.</span></span>
    
- <span data-ttu-id="d6b4a-115">Elle ne peuvent pas être appelées par des fonctions lors d’un recalcul.</span><span class="sxs-lookup"><span data-stu-id="d6b4a-115">They cannot be called by functions during a recalculation.</span></span>
    
## <a name="functions"></a><span data-ttu-id="d6b4a-116">Fonctions</span><span class="sxs-lookup"><span data-stu-id="d6b4a-116">Functions</span></span>

<span data-ttu-id="d6b4a-117">Les fonctions dans Excel présentent les caractéristiques suivantes :</span><span class="sxs-lookup"><span data-stu-id="d6b4a-117">Functions in Excel do the following:</span></span>
  
- <span data-ttu-id="d6b4a-118">Elles prennent généralement des arguments et renvoient toujours un résultat.</span><span class="sxs-lookup"><span data-stu-id="d6b4a-118">They usually take arguments and always return a result.</span></span>
    
- <span data-ttu-id="d6b4a-119">Elles peuvent être entrées dans une ou plusieurs cellules dans une formule Excel.</span><span class="sxs-lookup"><span data-stu-id="d6b4a-119">They can be entered into one or more cells as part of an Excel formula.</span></span>
    
- <span data-ttu-id="d6b4a-120">Elles peuvent être utilisées dans des définitions de nom défini.</span><span class="sxs-lookup"><span data-stu-id="d6b4a-120">They can be used in defined name definitions.</span></span>
    
- <span data-ttu-id="d6b4a-121">Elles peuvent être utilisées dans la limite de mise en forme conditionnelle et les expressions de seuil.</span><span class="sxs-lookup"><span data-stu-id="d6b4a-121">They can be used in conditional formatting limit and threshold expressions.</span></span>
    
- <span data-ttu-id="d6b4a-122">Elles peuvent être appelées par des commandes.</span><span class="sxs-lookup"><span data-stu-id="d6b4a-122">They can be called by commands.</span></span>
    
- <span data-ttu-id="d6b4a-123">Elles ne peuvent pas appeler de commandes.</span><span class="sxs-lookup"><span data-stu-id="d6b4a-123">They cannot call commands.</span></span>
    
<span data-ttu-id="d6b4a-124">Excel fait une distinction supplémentaire entre les fonctions de feuille de calcul définies par l’utilisateur et les fonctions définies par l’utilisateur qui sont conçues pour fonctionner sur des feuilles macro.</span><span class="sxs-lookup"><span data-stu-id="d6b4a-124">Excel makes a further distinction between user-defined worksheet functions and user-defined functions that are designed to work on macro sheets.</span></span> <span data-ttu-id="d6b4a-125">Excel ne limite pas les fonctions de feuille macro définies par l’utilisateur uniquement à une utilisation sur des feuilles macro : ces fonctions peuvent être utilisées partout où une fonction de feuille de calcul normale peut être utilisée.</span><span class="sxs-lookup"><span data-stu-id="d6b4a-125">Excel does not limit user-defined macro sheet functions only to being used on macro sheets: these functions can be used anywhere a normal worksheet function can be used.</span></span>
  
### <a name="worksheet-functions"></a><span data-ttu-id="d6b4a-126">Fonctions de feuille de calcul</span><span class="sxs-lookup"><span data-stu-id="d6b4a-126">Worksheet Functions</span></span>

<span data-ttu-id="d6b4a-127">Les fonctions de feuille de calcul Excel présentent les caractéristiques suivantes :</span><span class="sxs-lookup"><span data-stu-id="d6b4a-127">The following is true of Excel worksheet functions:</span></span>
  
- <span data-ttu-id="d6b4a-128">Elles ne peuvent pas accéder aux fonctions d’informations de feuille macro.</span><span class="sxs-lookup"><span data-stu-id="d6b4a-128">They cannot access macro sheet information functions.</span></span>
    
- <span data-ttu-id="d6b4a-129">Elles ne peuvent pas obtenir les valeurs de cellules non calculées.</span><span class="sxs-lookup"><span data-stu-id="d6b4a-129">They cannot obtain the values of uncalculated cells.</span></span>
    
- <span data-ttu-id="d6b4a-130">Elles peuvent être écrites et inscrites comme thread-safe à partir d’Excel 2007.</span><span class="sxs-lookup"><span data-stu-id="d6b4a-130">They can be written and registered as thread-safe starting in Excel 2007.</span></span>
    
### <a name="macro-sheet-functions"></a><span data-ttu-id="d6b4a-131">Fonctions de feuille macro</span><span class="sxs-lookup"><span data-stu-id="d6b4a-131">Macro-Sheet Functions</span></span>

<span data-ttu-id="d6b4a-132">Les fonctions de feuille macro Excel présentent les caractéristiques suivantes :</span><span class="sxs-lookup"><span data-stu-id="d6b4a-132">The following is true of Excel macro-sheet functions:</span></span>
  
- <span data-ttu-id="d6b4a-133">Elles peuvent accéder aux fonctions d’informations de feuille macro.</span><span class="sxs-lookup"><span data-stu-id="d6b4a-133">They can access macro sheet information functions.</span></span>
    
- <span data-ttu-id="d6b4a-134">Elles peuvent obtenir les valeurs de cellules non calculées, y compris les valeurs des cellules d’appel.</span><span class="sxs-lookup"><span data-stu-id="d6b4a-134">They can obtain the values of uncalculated cells including the values of the calling cells.</span></span>
    
- <span data-ttu-id="d6b4a-135">Elles ne sont pas considérées comme thread-safe à partir d’Excel 2007.</span><span class="sxs-lookup"><span data-stu-id="d6b4a-135">They are not considered thread safe starting in Excel 2007.</span></span>
    
<span data-ttu-id="d6b4a-136">C’est au moment où vous inscrivez la fonction que sont déterminés tous les éléments suivants : comment Excel traite une fonction définie par l’utilisateur (UDF), ce qu’il autorise la fonction à faire et comment il recalcule la fonction.</span><span class="sxs-lookup"><span data-stu-id="d6b4a-136">How Excel treats a user-defined function (UDF), what it permits the function to do, and how it recalculates the function are all determined when you register the function.</span></span> <span data-ttu-id="d6b4a-137">Si une fonction est inscrite comme fonction de feuille de calcul mais qu’elle tente de faire quelque chose que seule une feuille macro peut faire, l’opération échoue.</span><span class="sxs-lookup"><span data-stu-id="d6b4a-137">If a function is registered as a worksheet function but tries to do something that only a macro-sheet function can do, the operation fails.</span></span> <span data-ttu-id="d6b4a-138">À partir d’Excel 2007, si une fonction de feuille de calcul inscrite comme thread-safe tente d’appeler une fonction de feuille macro, là encore, l’opération échoue.</span><span class="sxs-lookup"><span data-stu-id="d6b4a-138">Starting in Excel 2007, if a worksheet function registered as thread safe tries to call a macro sheet function, again, the operation fails.</span></span>
  
<span data-ttu-id="d6b4a-139">Excel traite les fonctions définies par l’utilisateur Microsoft Visual Basic for Applications (VBA) comme des fonctions équivalentes aux fonctions de feuilles macro. En effet, elles peuvent accéder aux informations d’espace de travail et à la valeur de cellules non calculées, et ne sont pas considérées comme thread-safe à partir d’Excel 2007.</span><span class="sxs-lookup"><span data-stu-id="d6b4a-139">Excel treats Microsoft Visual Basic for Applications (VBA) UDFs as macro sheet-equivalent functions, in that they can access workspace information and the value of uncalculated cells, and they are not considered as thread safe starting in Excel 2007.</span></span>
  
## <a name="excel-states"></a><span data-ttu-id="d6b4a-140">États Excel</span><span class="sxs-lookup"><span data-stu-id="d6b4a-140">Excel States</span></span>

<span data-ttu-id="d6b4a-141">Excel peut être dans de nombreux états à un moment donné, selon les actions de l’utilisateur, un processus externe, un événement bloqué exécutant une macro ou un événement de maintenance interne Excel chronométré comme **Autosave**.</span><span class="sxs-lookup"><span data-stu-id="d6b4a-141">Excel can be in one of a number of states at any given time depending on the actions of the user, an external process, a trapped event running a macro, or a timed Excel housekeeping event such as **Autosave**.</span></span>
  
<span data-ttu-id="d6b4a-142">Les états de l’utilisateur sont les suivants :</span><span class="sxs-lookup"><span data-stu-id="d6b4a-142">The states that the user experiences are as follows:</span></span>
  
- <span data-ttu-id="d6b4a-143">**Prêt :** Aucune commande ni macro n’est en cours d’exécution.</span><span class="sxs-lookup"><span data-stu-id="d6b4a-143">**Ready state:** No commands or macros are being run.</span></span> <span data-ttu-id="d6b4a-144">Aucune boîte de dialogue n’est affichée.</span><span class="sxs-lookup"><span data-stu-id="d6b4a-144">No dialog boxes are being displayed.</span></span> <span data-ttu-id="d6b4a-145">Aucune cellule n’est en cours de modification et l’utilisateur n’est pas au milieu d’une opération couper/copier et coller.</span><span class="sxs-lookup"><span data-stu-id="d6b4a-145">No cells are being edited and the user is not in the middle of a cut/copy and paste operation.</span></span> <span data-ttu-id="d6b4a-146">Aucun objet incorporé n’est utilisé.</span><span class="sxs-lookup"><span data-stu-id="d6b4a-146">No embedded object has focus.</span></span> 
    
- <span data-ttu-id="d6b4a-147">**Mode Édition :** L’utilisateur a commencé à taper des caractères d’entrée valides dans une cellule déverrouillée ou non protégée ou a utilisé la touche **F2** sur une ou plusieurs cellules déverrouillées ou non protégées.</span><span class="sxs-lookup"><span data-stu-id="d6b4a-147">**Edit mode:** The user has started to type valid input characters into an unlocked or unprotected cell, or has pressed **F2** on one or more unlocked or unprotected cells.</span></span> 
    
- <span data-ttu-id="d6b4a-148">**Mode Couper/copier et coller :** L’utilisateur a coupé ou copié une cellule ou une plage de cellules et ne l’a pas encore collée ou l’a collée en utilisant la boîte de dialogue Collage spécial, qui permet plusieurs opérations de collage.</span><span class="sxs-lookup"><span data-stu-id="d6b4a-148">**Cut/copy and paste mode:** The user has cut or copied a cell or range of cells and has not yet pasted them, or has pasted them using the paste-special dialog box, which enables multiple paste operations.</span></span> 
    
- <span data-ttu-id="d6b4a-149">**Mode Pointer :** L’utilisateur modifie une formule et sélectionne des cellules dont les adresses sont ajoutées à la formule en cours de modification.</span><span class="sxs-lookup"><span data-stu-id="d6b4a-149">**Point mode:** The user is editing a formula and is selecting cells whose addresses are added to the formula being edited.</span></span> 
    
<span data-ttu-id="d6b4a-150">L’utilisateur peut effacer les modes Édition, Pointer et Couper/copier en appuyant sur la touche **Échap**. Excel revient dans l’état Prêt.</span><span class="sxs-lookup"><span data-stu-id="d6b4a-150">The user can clear the edit, point, and cut/copy modes by pressing the **ESC** key, which returns Excel to its ready state.</span></span> <span data-ttu-id="d6b4a-151">D’autres événements peuvent effacer ces états, tels que :</span><span class="sxs-lookup"><span data-stu-id="d6b4a-151">Other events can clear these states, such as the following:</span></span> 
  
- <span data-ttu-id="d6b4a-152">L’utilisateur ouvre une boîte de dialogue prédéfinie.</span><span class="sxs-lookup"><span data-stu-id="d6b4a-152">The user opens a built-in dialog box.</span></span>
    
- <span data-ttu-id="d6b4a-153">L’utilisateur lance un recalcul.</span><span class="sxs-lookup"><span data-stu-id="d6b4a-153">The user initiates sharing a Sway.</span></span>
    
- <span data-ttu-id="d6b4a-154">L’utilisateur exécute une commande.</span><span class="sxs-lookup"><span data-stu-id="d6b4a-154">The user runs a command.</span></span>
    
- <span data-ttu-id="d6b4a-155">Excel effectue une opération **Autosave** (enregistrement automatique).</span><span class="sxs-lookup"><span data-stu-id="d6b4a-155">Excel performs an **Autosave** operation.</span></span> 
    
- <span data-ttu-id="d6b4a-156">Un événement de minuteur est bloqué.</span><span class="sxs-lookup"><span data-stu-id="d6b4a-156">A timer event is trapped.</span></span>
    
<span data-ttu-id="d6b4a-157">Le dernier exemple est important pour les développeurs de compléments.</span><span class="sxs-lookup"><span data-stu-id="d6b4a-157">The last example is of importance to add-in developers.</span></span> <span data-ttu-id="d6b4a-158">Vous devez tenir compte de l’impact de l’utilisation d’Excel normale lorsque des captures d’événement de minuteur fréquentes sont définies et exécutées.</span><span class="sxs-lookup"><span data-stu-id="d6b4a-158">You should consider the impact of the normal usability of Excel where frequent timer event traps are being set and executed.</span></span> <span data-ttu-id="d6b4a-159">Lorsqu’il s’agit d’une partie importante des fonctionnalités de votre complément, vous devez fournir aux utilisateurs un moyen facilement accessible de l’interrompre pour qu’ils puissent couper/copier et coller normalement lorsqu’ils en ont besoin.</span><span class="sxs-lookup"><span data-stu-id="d6b4a-159">When this is an important part of your add-in's functionality, you should provide users with an easily accessible way of suspending it, so that they can cut/copy and paste normally when they need to.</span></span>
  
## <a name="see-also"></a><span data-ttu-id="d6b4a-160">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="d6b4a-160">See also</span></span>



[<span data-ttu-id="d6b4a-161">Concepts de programmation Excel</span><span class="sxs-lookup"><span data-stu-id="d6b4a-161">Excel Programming Concepts</span></span>](excel-programming-concepts.md)
  
[<span data-ttu-id="d6b4a-162">Autorisation des interruptions utilisateur lors des opérations très longues</span><span class="sxs-lookup"><span data-stu-id="d6b4a-162">Permitting user breaks in lengthy operations</span></span>](permitting-user-breaks-in-lengthy-operations.md)

