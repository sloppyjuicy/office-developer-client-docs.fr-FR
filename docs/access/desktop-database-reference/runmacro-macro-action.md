---
title: ExécuterMacro, action de macro
TOCTitle: RunMacro Macro Action
ms:assetid: 25966f20-8160-0821-b88a-ed08b7786fdc
ms:mtpsurl: https://msdn.microsoft.com/library/Ff191868(v=office.15)
ms:contentKeyID: 48543787
ms.date: 09/18/2015
mtps_version: v=office.15
f1_keywords:
- vbaac10.chm43195
f1_categories:
- Office.Version=v15
ms.openlocfilehash: 533ac6aff194296a9e4470e01672a8338dcbc318
ms.sourcegitcommit: 19aca09c5812cfb98b68b5d4604dcaa814479df7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 10/09/2018
ms.locfileid: "25472198"
---
# <a name="runmacro-macro-action"></a><span data-ttu-id="9905b-102">ExécuterMacro, action de macro</span><span class="sxs-lookup"><span data-stu-id="9905b-102">RunMacro Macro Action</span></span>


<span data-ttu-id="9905b-103">**S’applique à**: Access 2013 | Office 2013</span><span class="sxs-lookup"><span data-stu-id="9905b-103">**Applies to**: Access 2013 | Office 2013</span></span>

<span data-ttu-id="9905b-p101">Vous pouvez utiliser l'action **ExécuterMacro** pour exécuter une macro. La macro peut faire partie d'un groupe de macros.</span><span class="sxs-lookup"><span data-stu-id="9905b-p101">You can use the **RunMacro** action to run a macro. The macro can be in a macro group.</span></span>

<span data-ttu-id="9905b-106">Vous pouvez utiliser cette action dans les cas suivants :</span><span class="sxs-lookup"><span data-stu-id="9905b-106">You can use this action:</span></span>

  - <span data-ttu-id="9905b-107">Pour exécuter une macro à partir d'une autre macro.</span><span class="sxs-lookup"><span data-stu-id="9905b-107">To run a macro from within another macro.</span></span>

  - <span data-ttu-id="9905b-108">Pour exécuter une macro en fonction d'une condition définie.</span><span class="sxs-lookup"><span data-stu-id="9905b-108">To run a macro based on a certain condition.</span></span>

  - <span data-ttu-id="9905b-109">Pour attacher une macro à une commande de menu personnalisée.</span><span class="sxs-lookup"><span data-stu-id="9905b-109">To attach a macro to a custom menu command.</span></span>

## <a name="setting"></a><span data-ttu-id="9905b-110">Valeur</span><span class="sxs-lookup"><span data-stu-id="9905b-110">Setting</span></span>

<span data-ttu-id="9905b-111">L'action **ExécuterMacro** accepte les arguments suivants.</span><span class="sxs-lookup"><span data-stu-id="9905b-111">The **RunMacro** action has the following arguments.</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="9905b-112">Argument de l’action</span><span class="sxs-lookup"><span data-stu-id="9905b-112">Action argument</span></span></p></th>
<th><p><span data-ttu-id="9905b-113">Description</span><span class="sxs-lookup"><span data-stu-id="9905b-113">Description</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="9905b-114"><strong>Nom macro</strong></span><span class="sxs-lookup"><span data-stu-id="9905b-114"><strong>Macro Name</strong></span></span></p></td>
<td><p><span data-ttu-id="9905b-115">Nom de la macro à exécuter.</span><span class="sxs-lookup"><span data-stu-id="9905b-115">The name of the macro to run.</span></span> <span data-ttu-id="9905b-116">La zone <strong>Nom de la Macro</strong> dans la section <strong>Arguments de l’Action</strong> du volet Générateur de Macro affiche toutes les macros (et groupes de macros) dans la base de données en cours.</span><span class="sxs-lookup"><span data-stu-id="9905b-116">The <strong>Macro Name</strong> box in the <strong>Action Arguments</strong> section of the Macro Builder pane shows all macros (and macro groups) in the current database.</span></span> <span data-ttu-id="9905b-117">Si la macro est dans un groupe de macros, elle est répertoriée sous le nom du groupe de macros dans la liste en tant que <em>nomgroupemacros</em>. <em>nommacro</em>.</span><span class="sxs-lookup"><span data-stu-id="9905b-117">If the macro is in a macro group, it's listed under the macro group name in the list as <em>macrogroupname</em>.<em>macroname</em>.</span></span> <span data-ttu-id="9905b-118">Cet argument est obligatoire.</span><span class="sxs-lookup"><span data-stu-id="9905b-118">This is a required argument.</span></span> <span data-ttu-id="9905b-119">Si vous exécutez une macro contenant l’action <strong>ExécuterMacro</strong> dans une base de données bibliothèque, Microsoft Access recherche la macro portant ce nom dans la base de données bibliothèque, et non pas dans la base de données active.</span><span class="sxs-lookup"><span data-stu-id="9905b-119">If you run a macro containing the <strong>RunMacro</strong> action in a library database, Microsoft Access looks for the macro with this name in the library database and doesn't look for it in the current database.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="9905b-120"><strong>Nombre de répétitions</strong></span><span class="sxs-lookup"><span data-stu-id="9905b-120"><strong>Repeat Count</strong></span></span></p></td>
<td><p><span data-ttu-id="9905b-p103">Nombre maximal d’exécutions de la macro. Si vous laissez cet argument vide (et que l’argument <strong>Expression de répétition</strong> est également vide), la macro s’exécute une seule fois.</span><span class="sxs-lookup"><span data-stu-id="9905b-p103">The maximum number of times the macro will run. If you leave this argument blank (and the <strong>Repeat Expression</strong> argument is also blank), the macro runs once.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="9905b-123"><strong>Expression de répétition</strong></span><span class="sxs-lookup"><span data-stu-id="9905b-123"><strong>Repeat Expression</strong></span></span></p></td>
<td><p><span data-ttu-id="9905b-p104">Expression qui renvoie <strong>Vrai</strong> (–1) ou <strong>Faux</strong> (0). La macro arrête de s’exécuter si l’expression renvoie <strong>Faux</strong>. Cette expression est évaluée à chaque exécution de la macro.</span><span class="sxs-lookup"><span data-stu-id="9905b-p104">An expression that evaluates to <strong>True</strong> (–1) or <strong>False</strong> (0). The macro stops running if the expression evaluates to <strong>False</strong>. The expression is evaluated each time the macro runs.</span></span></p></td>
</tr>
</tbody>
</table>


## <a name="remarks"></a><span data-ttu-id="9905b-127">Notes</span><span class="sxs-lookup"><span data-stu-id="9905b-127">Remarks</span></span>

<span data-ttu-id="9905b-128">Si vous entrez le nom d'un groupe de macros dans l'argument **Nom de macro**, Access exécute la première macro du groupe.</span><span class="sxs-lookup"><span data-stu-id="9905b-128">If you enter a macro group name for the **Macro Name** argument, Access runs the first macro in the macro group.</span></span>

<span data-ttu-id="9905b-p105">Pour l'essentiel, cette action équivaut à cliquer sur le bouton **Exécuter une macro** dans l'onglet **Outils de base de données**, à sélectionner une macro, puis à cliquer sur **OK**. Toutefois, cette commande n'exécute la macro qu'une seule fois tandis que l'action **ExécuterMacro** permet d'exécuter une macro autant de fois que vous le souhaitez.</span><span class="sxs-lookup"><span data-stu-id="9905b-p105">This action is similar to clicking **Run Macro** on the **Database Tools** tab, selecting a macro, and clicking **OK**. However, this command runs the macro only once, whereas the **RunMacro** action can run a macro as many times as you want.</span></span>


> [!TIP]
> <P><span data-ttu-id="9905b-131">[!CONSEIL] Vous pouvez utiliser les arguments <STRONG>Nombre de répétitions</STRONG> et <STRONG>Expression de répétition</STRONG> pour déterminer le nombre de fois que la macro doit s'exécuter :</span><span class="sxs-lookup"><span data-stu-id="9905b-131">You can use the <STRONG>Repeat Count</STRONG> and <STRONG>Repeat Expression</STRONG> arguments to determine how many times the macro runs:</span></span></P>



  - <span data-ttu-id="9905b-132">Si vous laissez les deux arguments vides, la macro s'exécute une seule fois.</span><span class="sxs-lookup"><span data-stu-id="9905b-132">If you leave both arguments blank, the macro runs once.</span></span>

  - <span data-ttu-id="9905b-133">Si vous entrez un nombre dans la zone de l'argument **Répéter compte** et que vous ne spécifiez rien pour l'argument **Répéter expression**, la macro s'exécute le nombre de fois spécifié.</span><span class="sxs-lookup"><span data-stu-id="9905b-133">If you enter a number for **Repeat Count** but leave **Repeat Expression** blank, the macro runs the specified number of times.</span></span>

  - <span data-ttu-id="9905b-134">Si vous ne spécifiez rien pour **Répéter compte** et que vous entrez une expression dans la zone **Répéter expression**, la macro s'exécute jusqu'à ce que l'expression corresponde à **Faux**.</span><span class="sxs-lookup"><span data-stu-id="9905b-134">If you leave **Repeat Count** blank but enter an expression for **Repeat Expression**, the macro runs until the expression evaluates to **False**.</span></span>

  - <span data-ttu-id="9905b-135">Si vous spécifiez des valeurs pour les deux arguments, la macro s'exécute le nombre de fois spécifié dans **Répéter compte** ou jusqu'à ce que **Répéter expression** corresponde à **Faux**, selon la valeur atteinte en premier.</span><span class="sxs-lookup"><span data-stu-id="9905b-135">If you enter values for both arguments, the macro runs the number of times specified in **Repeat Count** or until **Repeat Expression** evaluates to **False**, whichever occurs first.</span></span>

<span data-ttu-id="9905b-p106">Lorsque vous exécutez une macro contenant l'action **ExécuterMacro** et qu'elle atteint l'action **ExécuterMacro**, Access exécute la macro appelée. Lorsque la macro appelée a terminé de s'exécuter, Access retourne à la macro d'origine et exécute l'action suivante.</span><span class="sxs-lookup"><span data-stu-id="9905b-p106">When you run a macro containing the **RunMacro** action, and it reaches the **RunMacro** action, Access runs the called macro. When the called macro has finished, Access returns to the original macro and runs the next action.</span></span>


> [!NOTE]
> <UL>
> <LI>
> <P><span data-ttu-id="9905b-138">Vous pouvez appeler une macro du même groupe de macros ou d'un autre groupe de macros.</span><span class="sxs-lookup"><span data-stu-id="9905b-138">You can call a macro in the same macro group or in another macro group.</span></span></P>
> <LI>
> <P><span data-ttu-id="9905b-p107">Vous pouvez imbriquer les macros. En d'autres termes, vous pouvez exécuter la macro A qui appelle à son tour la macro B, et ainsi de suite. Dans chaque cas, lorsque la macro appelée est terminée, Access retourne à la macro qui l'a appelée et exécute l'action suivante dans la macro.</span><span class="sxs-lookup"><span data-stu-id="9905b-p107">You can nest macros. That is, you can run macro A, which in turn calls macro B, and so on. In each case, when the called macro has finished, Access returns to the macro that called it and runs the next action in that macro.</span></span></P></LI></UL>



<span data-ttu-id="9905b-142">Pour exécuter l'action **ExécuterMacro** dans un module Visual Basic pour Applications (VBA), utilisez la méthode **RunMacro** de l'objet **DoCmd**.</span><span class="sxs-lookup"><span data-stu-id="9905b-142">To run the **RunMacro** action in a Visual Basic for Applications (VBA) module, use the **RunMacro** method of the **DoCmd** object.</span></span>

