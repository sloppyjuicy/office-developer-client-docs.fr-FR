---
title: Accès au code XLL dans Excel
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: overview
keywords:
- accès au code xll [excel 2007], XLL [Excel 2007], accès au code, commandes [Excel 2007], inscription, fonctions [Excel 2007], l’enregistrement, l’appel XLL à partir d’Excel, inscription commandes [Excel 2007], enregistrement de fonctions [Excel 2007]
localization_priority: Normal
ms.assetid: 6e4bf1f3-8eca-4be5-9632-75355ac31d61
description: 'S�applique �: Excel 2013�| Office 2013�| Visual Studio'
ms.openlocfilehash: 1523f9e8213cb955f1bfd995c42f921b001299fe
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19782014"
---
# <a name="accessing-xll-code-in-excel"></a><span data-ttu-id="c3ae7-104">Accès au code XLL dans Excel</span><span class="sxs-lookup"><span data-stu-id="c3ae7-104">Accessing XLL code in Excel</span></span>

<span data-ttu-id="c3ae7-105">**S’applique à**: Excel 2013 | Office 2013 | Visual Studio</span><span class="sxs-lookup"><span data-stu-id="c3ae7-105">**Applies to**: Excel 2013 | Office 2013 | Visual Studio</span></span> 
  
<span data-ttu-id="c3ae7-106">Pour être accessibles dans Microsoft Excel, les fonctions et les commandes qui contient un XLL :</span><span class="sxs-lookup"><span data-stu-id="c3ae7-106">To be accessible in Microsoft Excel, the functions and commands that an XLL contains:</span></span>
  
- <span data-ttu-id="c3ae7-107">Doivent être exportées par la XLL.</span><span class="sxs-lookup"><span data-stu-id="c3ae7-107">Must be exported by the XLL.</span></span>
    
- <span data-ttu-id="c3ae7-108">Doit être enregistré avec Excel.</span><span class="sxs-lookup"><span data-stu-id="c3ae7-108">Must be registered with Excel.</span></span>
    
## <a name="registering-functions-and-commands-with-excel"></a><span data-ttu-id="c3ae7-109">Inscription des fonctions et les commandes dans Excel</span><span class="sxs-lookup"><span data-stu-id="c3ae7-109">Registering functions and commands with Excel</span></span>

<span data-ttu-id="c3ae7-110">Enregistrement indique à Excel ce qui suit sur un point d’entrée DLL :</span><span class="sxs-lookup"><span data-stu-id="c3ae7-110">Registration tells Excel the following about a DLL entry point:</span></span>
  
- <span data-ttu-id="c3ae7-111">Si elle est masquée ou, si une fonction, si elle est visible dans l’Assistant fonction.</span><span class="sxs-lookup"><span data-stu-id="c3ae7-111">Whether it is hidden or, if a function, whether it is visible in the Function Wizard.</span></span>
    
- <span data-ttu-id="c3ae7-112">Il est ou non être appelée uniquement à partir d’une feuille de macro XLM ou à partir d’une feuille de calcul.</span><span class="sxs-lookup"><span data-stu-id="c3ae7-112">Whether it is callable only from an XLM macro sheet, or also from a worksheet.</span></span>
    
- <span data-ttu-id="c3ae7-113">Si une commande, si elle est une fonction de feuille de calcul ou une fonction équivalents de feuille macro.</span><span class="sxs-lookup"><span data-stu-id="c3ae7-113">If a command, whether it is a worksheet function or a macro sheet equivalent function.</span></span>
    
- <span data-ttu-id="c3ae7-114">Quel est son nom d’exportation DLL ou XLL et le nom que vous souhaitez utiliser.</span><span class="sxs-lookup"><span data-stu-id="c3ae7-114">What its XLL/DLL export name is, and what name you want Excel to use.</span></span>
    
- <span data-ttu-id="c3ae7-115">S’il s’agit d’une fonction :</span><span class="sxs-lookup"><span data-stu-id="c3ae7-115">If it is a function:</span></span>
    
  - <span data-ttu-id="c3ae7-116">Quelles données types de retours et prend comme arguments.</span><span class="sxs-lookup"><span data-stu-id="c3ae7-116">What data types it returns and takes as arguments.</span></span>
    
  - <span data-ttu-id="c3ae7-117">Si elle renvoie son résultat en modifiant un argument en place.</span><span class="sxs-lookup"><span data-stu-id="c3ae7-117">Whether it returns its result by modifying an argument in place.</span></span>
    
  - <span data-ttu-id="c3ae7-118">Si elle est volatile.</span><span class="sxs-lookup"><span data-stu-id="c3ae7-118">Whether it is volatile.</span></span>
    
  - <span data-ttu-id="c3ae7-119">Si elle est thread-safe (commençant pris en charge dans Excel 2007).</span><span class="sxs-lookup"><span data-stu-id="c3ae7-119">Whether it is thread safe (supported starting in Excel 2007).</span></span>
    
  - <span data-ttu-id="c3ae7-120">Quel éditeur de saisie semi-automatique et de l’Assistant fonction Coller de texte doivent s’afficher pour contribuer à l’appel de la fonction.</span><span class="sxs-lookup"><span data-stu-id="c3ae7-120">What text the Paste Function Wizard and AutoComplete editor should display to help with calling the function.</span></span>
    
  - <span data-ttu-id="c3ae7-121">Fonction catégorie, qu'elle doit être répertoriée sous.</span><span class="sxs-lookup"><span data-stu-id="c3ae7-121">Which function category it should be listed under.</span></span>
    
<span data-ttu-id="c3ae7-122">Tout cela à l’aide de l’API C fonction [xlfRegister](xlfregister-form-1.md), équivalente à la fonction XLM **inscrire**.</span><span class="sxs-lookup"><span data-stu-id="c3ae7-122">This is all achieved using the C API function [xlfRegister](xlfregister-form-1.md), equivalent to the XLM function **REGISTER**.</span></span>
  
## <a name="calling-xll-functions-directly-from-excel"></a><span data-ttu-id="c3ae7-123">Appel de fonctions XLL directement à partir d’Excel</span><span class="sxs-lookup"><span data-stu-id="c3ae7-123">Calling XLL functions directly from Excel</span></span>

<span data-ttu-id="c3ae7-124">Une fois qu’ils sont enregistrés, fonctions de feuille de macro et de feuille de calcul XLL peuvent être appelées à partir de n’importe où de qu'une fonction intégrée peut être appelée à partir :</span><span class="sxs-lookup"><span data-stu-id="c3ae7-124">Once they are registered, XLL worksheet and macro sheet functions can be called from anywhere a built-in function can be called from:</span></span>
  
- <span data-ttu-id="c3ae7-125">Une formule de cellule unique ou un tableau dans une feuille de calcul.</span><span class="sxs-lookup"><span data-stu-id="c3ae7-125">A single-cell or array formula on a worksheet.</span></span>
    
- <span data-ttu-id="c3ae7-126">Une formule de cellule unique ou un tableau dans une feuille macro.</span><span class="sxs-lookup"><span data-stu-id="c3ae7-126">A single-cell or array formula on a macro sheet.</span></span>
    
- <span data-ttu-id="c3ae7-127">La définition d’un nom défini.</span><span class="sxs-lookup"><span data-stu-id="c3ae7-127">The definition of a defined name.</span></span>
    
- <span data-ttu-id="c3ae7-128">Les champs condition et limite dans une boîte de dialogue Mise en forme conditionnelle.</span><span class="sxs-lookup"><span data-stu-id="c3ae7-128">The condition and limit fields in a conditional format dialog box.</span></span>
    
- <span data-ttu-id="c3ae7-129">À partir d’un autre complément par le biais de l’API C fonctionner [xlUDF](xludf.md).</span><span class="sxs-lookup"><span data-stu-id="c3ae7-129">From another add-in via the C API function [xlUDF](xludf.md).</span></span>
    
- <span data-ttu-id="c3ae7-130">À partir de Visual Basic pour Applications (VBA) via la méthode **application.Run appropriée** .</span><span class="sxs-lookup"><span data-stu-id="c3ae7-130">From Visual Basic for Applications (VBA) via the **Application.Run** method.</span></span> 
    
<span data-ttu-id="c3ae7-131">Vous pouvez obtenir une référence à la cellule ou plage de cellules appelant au sein de votre fonction à l’aide de la fonction de API C **xlfCaller**.</span><span class="sxs-lookup"><span data-stu-id="c3ae7-131">You can obtain a reference to the calling cell or range of cells within your function using the C API function **xlfCaller**.</span></span> <span data-ttu-id="c3ae7-132">Si la fonction a été appelée à partir de l’expression de mise en forme conditionnelle de la cellule, vous revenez toujours une référence à la cellule associée ou les cellules, afin que vous ne pouvez pas supposer que la formule de cellule contient la fonction XLL.</span><span class="sxs-lookup"><span data-stu-id="c3ae7-132">If the function was called from the cell's conditional format expression, you are still returned a reference to the associated cell or cells, so you cannot assume that the cell's formula contains the XLL function.</span></span> <span data-ttu-id="c3ae7-133">Si la fonction a été appelée à partir d’une fonction définie par l’utilisateur VBA (UDF), **xlfCaller** renvoie à nouveau l’adresse des cellules qui a appelé la fonction VBA.</span><span class="sxs-lookup"><span data-stu-id="c3ae7-133">If your function was called from a VBA user-defined function (UDF), **xlfCaller** again returns the address of the cells that called the VBA function.</span></span> <span data-ttu-id="c3ae7-134">Pour plus d’informations, voir [xlfCaller](xlfcaller.md).</span><span class="sxs-lookup"><span data-stu-id="c3ae7-134">For more information, see [xlfCaller](xlfcaller.md).</span></span>
  
> [!NOTE]
> <span data-ttu-id="c3ae7-135">Excel appelle également le code de la fonction XLL dans les boîtes de dialogue **Assistant fonction de collage** et **Remplacer** .</span><span class="sxs-lookup"><span data-stu-id="c3ae7-135">Excel also calls XLL function code from the **Paste Function Wizard** and **Replace** dialog boxes.</span></span> <span data-ttu-id="c3ae7-136">Vous devrez peut-être restreindre de votre code normal en cours d’exécution dans le cas de la boîte de dialogue **Arguments de la fonction Coller** , en particulier où votre fonction peut prendre beaucoup de temps à exécuter.</span><span class="sxs-lookup"><span data-stu-id="c3ae7-136">You might need to restrict your code's normal running in the case of the **Paste Function Arguments** dialog box, especially where your function can take a long time to execute.</span></span> <span data-ttu-id="c3ae7-137">Pour détecter si votre fonction est appelée à partir d’une de ces boîtes de dialogue, vous devez implémenter du code dans votre projet qui parcourt toutes les fenêtres ouvertes pour déterminer si la fenêtre frontal est une de ces boîtes de dialogue et, le cas échéant, laquelle.</span><span class="sxs-lookup"><span data-stu-id="c3ae7-137">To detect if your function is being called from either of these dialog boxes, you must implement some code in your project that iterates through all the open windows to determine if the front window is one of these dialog boxes, and, if so, which one.</span></span> 
  
## <a name="calling-xll-commands-directly-from-excel"></a><span data-ttu-id="c3ae7-138">Appeler des commandes XLL directement à partir d’Excel</span><span class="sxs-lookup"><span data-stu-id="c3ae7-138">Calling XLL commands directly from Excel</span></span>

<span data-ttu-id="c3ae7-139">Une fois qu’ils sont enregistrés, commandes XLL peuvent être appelées dans toutes les méthodes que les autres macros définies par l’utilisateur peuvent être appelées :</span><span class="sxs-lookup"><span data-stu-id="c3ae7-139">Once they are registered, XLL commands can be called in all the ways that other user-defined macros can be called:</span></span>
  
- <span data-ttu-id="c3ae7-140">Par associé à un objet de contrôle incorporé dans une feuille de calcul.</span><span class="sxs-lookup"><span data-stu-id="c3ae7-140">By being associated with a control object embedded on a worksheet.</span></span>
    
- <span data-ttu-id="c3ae7-141">Dans la boîte de dialogue Exécuter une Macro.</span><span class="sxs-lookup"><span data-stu-id="c3ae7-141">From the Run Macro dialog box.</span></span>
    
- <span data-ttu-id="c3ae7-142">À partir d’une macro VBA définies par l’utilisateur à l’aide de la méthode **Application.Run** .</span><span class="sxs-lookup"><span data-stu-id="c3ae7-142">From a VBA user-defined macro using the **Application.Run** method.</span></span> 
    
- <span data-ttu-id="c3ae7-143">À partir d’un élément de menu personnalisé ou une barre d’outils.</span><span class="sxs-lookup"><span data-stu-id="c3ae7-143">From a customized menu item or toolbar.</span></span>
    
- <span data-ttu-id="c3ae7-144">À l’aide d’une séquence de touches de raccourci définie lors de l’inscription de la commande.</span><span class="sxs-lookup"><span data-stu-id="c3ae7-144">Using a shortcut keystroke set up when registering the command.</span></span>
    
- <span data-ttu-id="c3ae7-145">La commande à exécuter lorsqu’un événement spécifié est interceptée.</span><span class="sxs-lookup"><span data-stu-id="c3ae7-145">As the command to be run when a specified event is trapped.</span></span>
    
> [!NOTE]
> <span data-ttu-id="c3ae7-146">Commandes XLL sont masquées en ce sens qu’ils n’apparaissent pas dans la liste des macros disponibles dans les boîtes de dialogue Excel.</span><span class="sxs-lookup"><span data-stu-id="c3ae7-146">XLL commands are hidden in that they do not appear on the list of available macros in Excel dialog boxes.</span></span> <span data-ttu-id="c3ae7-147">Mais ils peuvent être entrés manuellement dans le champ nom de macro.</span><span class="sxs-lookup"><span data-stu-id="c3ae7-147">But they can be entered manually into the macro name field.</span></span> <span data-ttu-id="c3ae7-148">Excel suppose que le nom enregistré en tant que ces boîtes de dialogue, pas le nom d’exportation de la DLL.</span><span class="sxs-lookup"><span data-stu-id="c3ae7-148">Excel expects the registered-as name in these dialog boxes, not the DLL export name.</span></span> 
  
<span data-ttu-id="c3ae7-149">Toutes les commandes XLL auprès d’Excel sont utilisés par Microsoft Excel pour être sous la forme suivante :</span><span class="sxs-lookup"><span data-stu-id="c3ae7-149">All XLL commands registered with Excel are assumed by Excel to be of the following form:</span></span>
  
```cs
short WINAPI xll_cmd_name(void)
{
// Function code...
    return 1;
}

```

<span data-ttu-id="c3ae7-p104">[!REMARQUE] Excel ignore la valeur de renvoi, sauf si elle est appel�e � partir d�une feuille macro XLM, auquel cas la valeur de retour est convertie en **TRUE** ou **FALSE**. Vous devez par cons�quent renvoyer 1 si votre commande a �t� ex�cut�e correctement, et 0 si elle a �chou� ou a �t� annul�e par l�utilisateur.</span><span class="sxs-lookup"><span data-stu-id="c3ae7-p104">Excel ignores the return value unless it is called from an XLM macro sheet, in which case the return value is converted to **TRUE** or **FALSE**. You should therefore return 1 if your command executed successfully, and 0 if it failed or was canceled by the user.</span></span>
  
<span data-ttu-id="c3ae7-152">Vous pouvez obtenir des informations sur la façon dont votre commande a été appelée à l’aide de l’API C fonctionner **xlfCaller**.</span><span class="sxs-lookup"><span data-stu-id="c3ae7-152">You can obtain information about how your command was invoked using the C API function **xlfCaller**.</span></span> <span data-ttu-id="c3ae7-153">Pour plus d’informations, voir [xlfCaller](xlfcaller.md).</span><span class="sxs-lookup"><span data-stu-id="c3ae7-153">For more information, see [xlfCaller](xlfcaller.md).</span></span>
  
<span data-ttu-id="c3ae7-154">À compter d’interface utilisateur d’Excel 2007 est très différent des versions antérieures.</span><span class="sxs-lookup"><span data-stu-id="c3ae7-154">Starting in Excel 2007 user interface is very different from earlier versions.</span></span> <span data-ttu-id="c3ae7-155">Les fonctions API C qui autorisent l’ajout et la suppression des barres de menus, menus, sous-menus, éléments de menu, barres d’outils personnalisées et des boutons de barre d’outils sont toujours pris en charge la plupart des cas.</span><span class="sxs-lookup"><span data-stu-id="c3ae7-155">The C API functions that permit the addition and deletion of custom menu bars, menus, submenus, menu items, custom toolbars and toolbar buttons are still supported in most cases.</span></span> <span data-ttu-id="c3ae7-156">Toutefois, ils peuvent toujours faites pas l’élément ajouté disponibles d’une manière qui connaissent vos utilisateurs.</span><span class="sxs-lookup"><span data-stu-id="c3ae7-156">However, they may not always make the added item available in a way that your users are familiar with.</span></span> <span data-ttu-id="c3ae7-157">Vous devez vérifier avec soin que toute fonctionnalité ajoutée est toujours accessible ou implémenter une personnalisation spécifique à la version.</span><span class="sxs-lookup"><span data-stu-id="c3ae7-157">You should carefully check that any added functionality is still accessible, or implement a version-specific customization.</span></span> <span data-ttu-id="c3ae7-158">Démarrage de l’interface utilisateur dans Excel 2007 mieux personnalisé à l’aide d’un module de code managé qui peut ensuite être étroitement à vos commandes XLL.</span><span class="sxs-lookup"><span data-stu-id="c3ae7-158">Starting in Excel 2007 the user interface is best customized by using a managed code module that can then be tightly coupled to your XLL commands.</span></span>
  
## <a name="see-also"></a><span data-ttu-id="c3ae7-159">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="c3ae7-159">See also</span></span>

- [<span data-ttu-id="c3ae7-160">Cr�ation de XLL</span><span class="sxs-lookup"><span data-stu-id="c3ae7-160">Creating XLLs</span></span>](creating-xlls.md)
- [<span data-ttu-id="c3ae7-161">Appel des fonctions XLL à partir de l’Assistant fonction ou remplacer des boîtes de dialogue</span><span class="sxs-lookup"><span data-stu-id="c3ae7-161">Call XLL Functions from the Function Wizard or Replace Dialog Boxes</span></span>](how-to-call-xll-functions-from-the-function-wizard-or-replace-dialog-boxes.md)
- [<span data-ttu-id="c3ae7-162">Gestionnaire de compléments et les fonctions de l’Interface XLL</span><span class="sxs-lookup"><span data-stu-id="c3ae7-162">Add-in Manager and XLL Interface Functions</span></span>](add-in-manager-and-xll-interface-functions.md)
- [<span data-ttu-id="c3ae7-163">D�veloppement de XLL de Excel 2013</span><span class="sxs-lookup"><span data-stu-id="c3ae7-163">Developing Excel XLLs</span></span>](developing-excel-xlls.md)



