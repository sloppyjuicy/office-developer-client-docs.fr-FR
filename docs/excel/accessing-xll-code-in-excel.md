---
title: Accès au code XLL dans Excel
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: overview
keywords:
- accéder au code xll [Excel 2007], XLL [Excel 2007] accéder au code, commandes [Excel 2007], inscription, fonctions [Excel 2007], inscription, appel des XLL à partir d’Excel, inscription de commandes [Excel 2007], inscription de fonctions [Excel 2007]
ms.assetid: 6e4bf1f3-8eca-4be5-9632-75355ac31d61
description: 'S’applique à : Excel 2013 | Office 2013 | Visual Studio'
localization_priority: Priority
ms.openlocfilehash: d1332b0dffc052404c75c4ec51d94879457c3da0
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: HT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32304185"
---
# <a name="accessing-xll-code-in-excel"></a><span data-ttu-id="21e36-104">Accès au code XLL dans Excel</span><span class="sxs-lookup"><span data-stu-id="21e36-104">Accessing XLL code in Excel</span></span>

<span data-ttu-id="21e36-105">**S’applique à**: Excel 2013 | Office 2013 | Visual Studio</span><span class="sxs-lookup"><span data-stu-id="21e36-105">**Applies to**: Excel 2013 | Office 2013 | Visual Studio</span></span> 
  
<span data-ttu-id="21e36-106">Pour être accessibles dans Microsoft Excel, les fonctions et les commandes contenues dans un XLL :</span><span class="sxs-lookup"><span data-stu-id="21e36-106">To be accessible in Microsoft Excel, the functions and commands that an XLL contains:</span></span>
  
- <span data-ttu-id="21e36-107">doivent être exportées par le XLL ;</span><span class="sxs-lookup"><span data-stu-id="21e36-107">Must be exported by the XLL.</span></span>
    
- <span data-ttu-id="21e36-108">doivent être inscrites avec Excel.</span><span class="sxs-lookup"><span data-stu-id="21e36-108">Must be registered with Excel.</span></span>
    
## <a name="registering-functions-and-commands-with-excel"></a><span data-ttu-id="21e36-109">Inscription de fonctions et de commandes avec Excel</span><span class="sxs-lookup"><span data-stu-id="21e36-109">Registering functions and commands with Excel</span></span>

<span data-ttu-id="21e36-110">L’inscription indique à Excel les points suivants concernant un point d’entrée DLL :</span><span class="sxs-lookup"><span data-stu-id="21e36-110">Registration tells Excel the following about a DLL entry point:</span></span>
  
- <span data-ttu-id="21e36-111">S’il est masqué ou, s’il s’agit d’une fonction, si elle est visible dans l’Assistant Fonction.</span><span class="sxs-lookup"><span data-stu-id="21e36-111">Whether it is hidden or, if a function, whether it is visible in the Function Wizard.</span></span>
    
- <span data-ttu-id="21e36-112">S’il peut être appelé uniquement à partir d’une feuille macro XLM ou à partir d’une feuille de calcul également.</span><span class="sxs-lookup"><span data-stu-id="21e36-112">Whether it is callable only from an XLM macro sheet, or also from a worksheet.</span></span>
    
- <span data-ttu-id="21e36-113">S’il s’agit d’une commande, si c’est une fonction de feuille de calcul ou une fonction équivalente à une feuille macro.</span><span class="sxs-lookup"><span data-stu-id="21e36-113">If a command, whether it is a worksheet function or a macro sheet equivalent function.</span></span>
    
- <span data-ttu-id="21e36-114">Son nom d’exportation XLL/DLL et le nom qu’Excel doit utiliser.</span><span class="sxs-lookup"><span data-stu-id="21e36-114">What its XLL/DLL export name is, and what name you want Excel to use.</span></span>
    
- <span data-ttu-id="21e36-115">S’il s’agit d’une fonction :</span><span class="sxs-lookup"><span data-stu-id="21e36-115">If it is a function:</span></span>
    
  - <span data-ttu-id="21e36-116">Quels types de données elle renvoie et prend comme arguments.</span><span class="sxs-lookup"><span data-stu-id="21e36-116">What data types it returns and takes as arguments.</span></span>
    
  - <span data-ttu-id="21e36-117">Si elle renvoie son résultat en modifiant un argument en place.</span><span class="sxs-lookup"><span data-stu-id="21e36-117">Whether it returns its result by modifying an argument in place.</span></span>
    
  - <span data-ttu-id="21e36-118">Si elle est volatile.</span><span class="sxs-lookup"><span data-stu-id="21e36-118">Whether it is volatile.</span></span>
    
  - <span data-ttu-id="21e36-119">Si elle est thread-safe (pris en charge à partir d’Excel 2007).</span><span class="sxs-lookup"><span data-stu-id="21e36-119">Whether it is thread safe (supported starting in Excel 2007).</span></span>
    
  - <span data-ttu-id="21e36-120">Le texte que l’Assistant Coller une fonction et l’éditeur de saisie semi-automatique doivent afficher pour appeler la fonction.</span><span class="sxs-lookup"><span data-stu-id="21e36-120">What text the Paste Function Wizard and AutoComplete editor should display to help with calling the function.</span></span>
    
  - <span data-ttu-id="21e36-121">Sous quelle catégorie de fonction elle doit être répertoriée.</span><span class="sxs-lookup"><span data-stu-id="21e36-121">Which function category it should be listed under.</span></span>
    
<span data-ttu-id="21e36-122">Tout ceci est réalisé à l’aide de la fonction API C [xlfRegister](xlfregister-form-1.md), équivalente à la fonction XLM **REGISTER**.</span><span class="sxs-lookup"><span data-stu-id="21e36-122">This is all achieved using the C API function [xlfRegister](xlfregister-form-1.md), equivalent to the XLM function **REGISTER**.</span></span>
  
## <a name="calling-xll-functions-directly-from-excel"></a><span data-ttu-id="21e36-123">Appel des fonctions XLL directement à partir d’Excel</span><span class="sxs-lookup"><span data-stu-id="21e36-123">Calling XLL functions directly from Excel</span></span>

<span data-ttu-id="21e36-124">Une fois qu’elles sont inscrites, les fonctions de feuille de calcul et de feuille macro XLL peuvent être appelées de tout emplacement d’où une fonction intégrée peut être appelée :</span><span class="sxs-lookup"><span data-stu-id="21e36-124">Once they are registered, XLL worksheet and macro sheet functions can be called from anywhere a built-in function can be called from:</span></span>
  
- <span data-ttu-id="21e36-125">Une formule à cellule unique ou de tableau sur une feuille de calcul.</span><span class="sxs-lookup"><span data-stu-id="21e36-125">A single-cell or array formula on a worksheet.</span></span>
    
- <span data-ttu-id="21e36-126">Une formule à cellule unique ou de tableau sur une feuille macro.</span><span class="sxs-lookup"><span data-stu-id="21e36-126">A single-cell or array formula on a macro sheet.</span></span>
    
- <span data-ttu-id="21e36-127">La définition d’un nom défini.</span><span class="sxs-lookup"><span data-stu-id="21e36-127">The definition of a defined name.</span></span>
    
- <span data-ttu-id="21e36-128">Les champs de condition et de limite dans une boîte de dialogue de mise en forme conditionnelle.</span><span class="sxs-lookup"><span data-stu-id="21e36-128">The condition and limit fields in a conditional format dialog box.</span></span>
    
- <span data-ttu-id="21e36-129">À partir d’un autre complément via la fonction API C [xlUDF](xludf.md).</span><span class="sxs-lookup"><span data-stu-id="21e36-129">From another add-in via the C API function [xlUDF](xludf.md).</span></span>
    
- <span data-ttu-id="21e36-130">À partir de Visual Basic for Applications (VBA) via la méthode **Application.Run**.</span><span class="sxs-lookup"><span data-stu-id="21e36-130">From Visual Basic for Applications (VBA) via the **Application.Run** method.</span></span> 
    
<span data-ttu-id="21e36-131">Vous pouvez obtenir une référence à la cellule ou à la plage de cellules d’appel dans votre fonction à l’aide de la fonction API C **xlfCaller**.</span><span class="sxs-lookup"><span data-stu-id="21e36-131">You can obtain a reference to the calling cell or range of cells within your function using the C API function **xlfCaller**.</span></span> <span data-ttu-id="21e36-132">Si la fonction a été appelée à partir de l’expression de mise en forme conditionnelle de la cellule, une référence à la cellule ou aux cellules associée(s) vous est renvoyée, donc vous ne pouvez pas considérer que la formule de la cellule contient la fonction XLL.</span><span class="sxs-lookup"><span data-stu-id="21e36-132">If the function was called from the cell's conditional format expression, you are still returned a reference to the associated cell or cells, so you cannot assume that the cell's formula contains the XLL function.</span></span> <span data-ttu-id="21e36-133">Si votre fonction a été appelée à partir d’une fonction VBA définie par l’utilisateur (UDF), **xlfCaller** renvoie l’adresse des cellules qui ont appelé la fonction VBA.</span><span class="sxs-lookup"><span data-stu-id="21e36-133">If your function was called from a VBA user-defined function (UDF), **xlfCaller** again returns the address of the cells that called the VBA function.</span></span> <span data-ttu-id="21e36-134">Pour plus d'informations, consultez [xlfCaller](xlfcaller.md).</span><span class="sxs-lookup"><span data-stu-id="21e36-134">For more information, see [xlfCaller](xlfcaller.md).</span></span>
  
> [!NOTE]
> <span data-ttu-id="21e36-135">Excel appelle également le code de fonction XLL à partir de l’**Assistant Coller une fonction** et des boîtes de dialogue **Remplacer**.</span><span class="sxs-lookup"><span data-stu-id="21e36-135">Excel also calls XLL function code from the **Paste Function Wizard** and **Replace** dialog boxes.</span></span> <span data-ttu-id="21e36-136">Vous devrez peut-être restreindre l’exécution normale de votre code dans le cas de la boîte de dialogue des **arguments Coller une fonction**, notamment lorsque l’exécution de votre fonction peut être longue.</span><span class="sxs-lookup"><span data-stu-id="21e36-136">You might need to restrict your code's normal running in the case of the **Paste Function Arguments** dialog box, especially where your function can take a long time to execute.</span></span> <span data-ttu-id="21e36-137">Pour détecter si votre fonction est appelée à partir de ces boîtes de dialogue, vous devez implémenter du code dans votre projet qui se reproduit dans toutes les fenêtres ouvertes pour déterminer si la première fenêtre est l’une de ces boîtes de dialogue et, si c’est le cas, laquelle.</span><span class="sxs-lookup"><span data-stu-id="21e36-137">To detect if your function is being called from either of these dialog boxes, you must implement some code in your project that iterates through all the open windows to determine if the front window is one of these dialog boxes, and, if so, which one.</span></span> 
  
## <a name="calling-xll-commands-directly-from-excel"></a><span data-ttu-id="21e36-138">Appel de commandes XLL directement à partir d’Excel</span><span class="sxs-lookup"><span data-stu-id="21e36-138">Calling XLL commands directly from Excel</span></span>

<span data-ttu-id="21e36-139">Une fois qu’elles sont inscrites, les commandes XLL peuvent être appelées à l’aide de toutes les autres méthodes utilisées pour appeler d’autres macros définies par l’utilisateur :</span><span class="sxs-lookup"><span data-stu-id="21e36-139">Once they are registered, XLL commands can be called in all the ways that other user-defined macros can be called:</span></span>
  
- <span data-ttu-id="21e36-140">En les associant à un objet de contrôle incorporé sur une feuille de calcul.</span><span class="sxs-lookup"><span data-stu-id="21e36-140">By being associated with a control object embedded on a worksheet.</span></span>
    
- <span data-ttu-id="21e36-141">À partir de la boîte de dialogue Exécuter une macro.</span><span class="sxs-lookup"><span data-stu-id="21e36-141">From the Run Macro dialog box.</span></span>
    
- <span data-ttu-id="21e36-142">À partir d’une macro définie par l’utilisateur VBA à l’aide la méthode **Application.Run**.</span><span class="sxs-lookup"><span data-stu-id="21e36-142">From a VBA user-defined macro using the **Application.Run** method.</span></span> 
    
- <span data-ttu-id="21e36-143">À partir d’un élément de menu personnalisé ou de la barre d’outils.</span><span class="sxs-lookup"><span data-stu-id="21e36-143">From a customized menu item or toolbar.</span></span>
    
- <span data-ttu-id="21e36-144">À l’aide d’une combinaison de touches de définie lors de l’inscription de la commande.</span><span class="sxs-lookup"><span data-stu-id="21e36-144">Using a shortcut keystroke set up when registering the command.</span></span>
    
- <span data-ttu-id="21e36-145">En tant que commande à exécuter lorsqu’un événement spécifié est bloqué.</span><span class="sxs-lookup"><span data-stu-id="21e36-145">As the command to be run when a specified event is trapped.</span></span>
    
> [!NOTE]
> <span data-ttu-id="21e36-146">Les commandes XLL sont masquées dans le sens où elles n’apparaissent pas dans la liste des macros disponibles dans les boîtes de dialogue Excel.</span><span class="sxs-lookup"><span data-stu-id="21e36-146">XLL commands are hidden in that they do not appear on the list of available macros in Excel dialog boxes.</span></span> <span data-ttu-id="21e36-147">Cependant, elles peuvent être entrées manuellement dans le champ du nom de la macro.</span><span class="sxs-lookup"><span data-stu-id="21e36-147">But they can be entered manually into the macro name field.</span></span> <span data-ttu-id="21e36-148">Dans Excel, le nom sous lequel la commande a été inscrite doit être entré dans ces boîtes de dialogue, et non le nom d’exportation DLL.</span><span class="sxs-lookup"><span data-stu-id="21e36-148">Excel expects the registered-as name in these dialog boxes, not the DLL export name.</span></span> 
  
<span data-ttu-id="21e36-149">Toutes les commandes XLL inscrites avec Excel sont considérées par Excel comme étant de la forme suivante :</span><span class="sxs-lookup"><span data-stu-id="21e36-149">All XLL commands registered with Excel are assumed by Excel to be of the following form:</span></span>
  
```cs
short WINAPI xll_cmd_name(void)
{
// Function code...
    return 1;
}

```

<span data-ttu-id="21e36-p104">Excel ignore la valeur de renvoi, sauf si elle est appel�e � partir d�une feuille macro XLM, auquel cas la valeur de retour est convertie en **TRUE** ou **FALSE**. Vous devez par cons�quent renvoyer 1 si votre commande a �t� ex�cut�e correctement, et 0 si elle a �chou� ou a �t� annul�e par l�utilisateur.</span><span class="sxs-lookup"><span data-stu-id="21e36-p104">Excel ignores the return value unless it is called from an XLM macro sheet, in which case the return value is converted to **TRUE** or **FALSE**. You should therefore return 1 if your command executed successfully, and 0 if it failed or was canceled by the user.</span></span>
  
<span data-ttu-id="21e36-152">Vous pouvez obtenir des informations sur la manière dont votre commande a été appelée à l’aide de la fonction API C **xlfCaller**.</span><span class="sxs-lookup"><span data-stu-id="21e36-152">You can obtain information about how your command was invoked using the C API function **xlfCaller**.</span></span> <span data-ttu-id="21e36-153">Pour plus d'informations, consultez [xlfCaller](xlfcaller.md).</span><span class="sxs-lookup"><span data-stu-id="21e36-153">For more information, see [xlfCaller](xlfcaller.md).</span></span>
  
<span data-ttu-id="21e36-154">À partir d’Excel 2007, l’interface utilisateur est très différente des versions antérieures.</span><span class="sxs-lookup"><span data-stu-id="21e36-154">Starting in Excel 2007 user interface is very different from earlier versions.</span></span> <span data-ttu-id="21e36-155">Les fonctions API C qui autorisent l’ajout et la suppression de barres de menus, menus, sous-menus, éléments de menu, barres d’outils et boutons de barre d’outils personnalisés sont toujours prises en charge dans la plupart des cas.</span><span class="sxs-lookup"><span data-stu-id="21e36-155">The C API functions that permit the addition and deletion of custom menu bars, menus, submenus, menu items, custom toolbars and toolbar buttons are still supported in most cases.</span></span> <span data-ttu-id="21e36-156">Toutefois, il se peut qu’elles ne rendent pas toujours disponible l’élément ajouté de la même façon que ce à quoi vos utilisateurs sont habitués.</span><span class="sxs-lookup"><span data-stu-id="21e36-156">However, they may not always make the added item available in a way that your users are familiar with.</span></span> <span data-ttu-id="21e36-157">Vous devez vérifier soigneusement que toute fonction ajoutée est toujours accessible, ou implémenter une personnalisation propre à la version.</span><span class="sxs-lookup"><span data-stu-id="21e36-157">You should carefully check that any added functionality is still accessible, or implement a version-specific customization.</span></span> <span data-ttu-id="21e36-158">À partir d’Excel 2007, l’interface utilisateur est mieux personnalisée à l’aide d’un module de code managé qui peut être étroitement associé à vos commandes XLL.</span><span class="sxs-lookup"><span data-stu-id="21e36-158">Starting in Excel 2007 the user interface is best customized by using a managed code module that can then be tightly coupled to your XLL commands.</span></span>
  
## <a name="see-also"></a><span data-ttu-id="21e36-159">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="21e36-159">See also</span></span>

- [<span data-ttu-id="21e36-160">Création de XLL</span><span class="sxs-lookup"><span data-stu-id="21e36-160">Creating XLLs</span></span>](creating-xlls.md)
- [<span data-ttu-id="21e36-161">Appel des fonctions XLL à partir de l’Assistant Fonction ou des boîtes de dialogue Remplacer</span><span class="sxs-lookup"><span data-stu-id="21e36-161">Call XLL Functions from the Function Wizard or Replace Dialog Boxes</span></span>](how-to-call-xll-functions-from-the-function-wizard-or-replace-dialog-boxes.md)
- [<span data-ttu-id="21e36-162">Fonctions du Gestionnaire de compléments et de l’interface XLL</span><span class="sxs-lookup"><span data-stu-id="21e36-162">Add-in Manager and XLL Interface Functions</span></span>](add-in-manager-and-xll-interface-functions.md)
- [<span data-ttu-id="21e36-163">Développement de XLL de Excel</span><span class="sxs-lookup"><span data-stu-id="21e36-163">Developing Excel XLLs</span></span>](developing-excel-xlls.md)



