---
title: ClearMacroError, action de macro
TOCTitle: ClearMacroError macro action
ms:assetid: 1091747e-e957-38c6-6454-5169f091323e
ms:mtpsurl: https://msdn.microsoft.com/library/Ff845338(v=office.15)
ms:contentKeyID: 48543296
ms.date: 09/18/2015
mtps_version: v=office.15
f1_keywords:
- vbaac10.chm109100
f1_categories:
- Office.Version=v15
localization_priority: Normal
ms.openlocfilehash: f42386674ff76d550fb47a971860b4e1a5905236
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32296373"
---
# <a name="clearmacroerror-macro-action"></a><span data-ttu-id="0e2a5-102">ClearMacroError, action de macro</span><span class="sxs-lookup"><span data-stu-id="0e2a5-102">ClearMacroError macro action</span></span>


<span data-ttu-id="0e2a5-103">**S’applique à** : Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="0e2a5-103">**Applies to**: Access 2013, Office 2013</span></span>


<span data-ttu-id="0e2a5-104">Utilisez l'action **EffacerMacroErreur** pour effacer les informations sur une erreur qui sont stockées dans l'objet **MacroError**.</span><span class="sxs-lookup"><span data-stu-id="0e2a5-104">You can use the **ClearMacroError** action to clear information about an error that is stored in the **MacroError** object.</span></span>

## <a name="setting"></a><span data-ttu-id="0e2a5-105">Paramètre</span><span class="sxs-lookup"><span data-stu-id="0e2a5-105">Setting</span></span>

<span data-ttu-id="0e2a5-106">L’action **EffacerMacroErreur** ne possède aucun argument.</span><span class="sxs-lookup"><span data-stu-id="0e2a5-106">The **ClearMacroError** action does not have any arguments.</span></span>

## <a name="remarks"></a><span data-ttu-id="0e2a5-107">Remarques</span><span class="sxs-lookup"><span data-stu-id="0e2a5-107">Remarks</span></span>

- <span data-ttu-id="0e2a5-108">Lorsqu'une erreur se produit dans une macro, les informations sur l'erreur sont stockées dans l'objet **MacroError**.</span><span class="sxs-lookup"><span data-stu-id="0e2a5-108">When an error occurs in a macro, information about the error is stored in the **MacroError** object.</span></span> <span data-ttu-id="0e2a5-109">Si vous n’avez pas utilisé l’action **[SurErreur](onerror-macro-action.md)** pour supprimer les messages d’erreur, la macro s’arrête et les informations d’erreur s’affichent dans un message d’erreur standard.</span><span class="sxs-lookup"><span data-stu-id="0e2a5-109">If you have not used the **[OnError](onerror-macro-action.md)** action to suppress error messages, the macro stops and the error information is displayed in a standard error message.</span></span> <span data-ttu-id="0e2a5-110">Toutefois, si vous avez utilisé l’action **SurErreur** pour supprimer les messages d’erreur, vous pouvez utiliser les informations stockées dans l’objet **MacroError** dans une condition ou dans un message d’erreur personnalisé.</span><span class="sxs-lookup"><span data-stu-id="0e2a5-110">However, if you have used the **OnError** action to suppress error messages, you might want to use the information stored in the **MacroError** object in a condition or in a custom error message.</span></span>
    
  <span data-ttu-id="0e2a5-p102">Lorsqu'une erreur a été gérée, les informations stockées dans l'objet **MacroError** deviennent obsolètes. Il est alors conseillé d'effacer l'objet à l'aide de l'action **EffacerMacroErreur**, ce qui permet de réinitialiser à 0 le numéro d'erreur dans l'objet **MacroError** et de supprimer toutes les autres informations sur l'erreur, telles que sa description, le nom de la macro, ainsi que le nom, la condition et les arguments de l'action. Ainsi, vous pourrez réexaminer ultérieurement l'objet **MacroError** pour déterminer si une autre erreur s'est produite.</span><span class="sxs-lookup"><span data-stu-id="0e2a5-p102">After an error has been handled, the information in the **MacroError** object is out of date, so it is a good idea to clear the object by using the **ClearMacroError** action. Doing so resets the error number in the **MacroError** object to 0 and clears any other information about the error that is stored in the object, such as the error description, macro name, action name, condition, and arguments. This way, you can inspect the **MacroError** object again later to see if another error has occurred.</span></span>

- <span data-ttu-id="0e2a5-114">L'objet **MacroError** est automatiquement effacé à l'issue d'une macro. Il n'est donc pas nécessaire d'utiliser l'action **EffacerMacroErreur** à la fin d'une macro.</span><span class="sxs-lookup"><span data-stu-id="0e2a5-114">The **MacroError** object is automatically cleared when any macro ends, so you do not need to use the **ClearMacroError** action at the end of a macro.</span></span>

- <span data-ttu-id="0e2a5-p103">L'objet **MacroError** ne contient des informations que sur une seule erreur à la fois. Si plusieurs erreurs se sont produites dans une macro, l'objet **MacroError** ne contient des informations que sur la dernière erreur.</span><span class="sxs-lookup"><span data-stu-id="0e2a5-p103">The **MacroError** object contains information about only one error at a time. If more than one error has occurred in a macro, the **MacroError** object contains information only about the last error.</span></span>

- <span data-ttu-id="0e2a5-117">Pour exécuter l'action **EffacerMacroErreur** dans un module Visual Basic pour Applications (VBA), utilisez la méthode **ClearMacroError** de l'objet **DoCmd**.</span><span class="sxs-lookup"><span data-stu-id="0e2a5-117">To run the **ClearMacroError** action in a VBA module, use the **ClearMacroError** method of the **DoCmd** object.</span></span>

## <a name="example"></a><span data-ttu-id="0e2a5-118">Exemple</span><span class="sxs-lookup"><span data-stu-id="0e2a5-118">Example</span></span>

<span data-ttu-id="0e2a5-119">La macro suivante utilise l'action **SurErreur** avec l'argument **Suivant** pour supprimer les messages d'erreur, puis utilise l'action **OuvrirFormulaire** pour ouvrir un formulaire.</span><span class="sxs-lookup"><span data-stu-id="0e2a5-119">The following macro uses the **OnError** action with the **Next** argument to suppress error messages, and then uses the **OpenForm** action to open a form.</span></span> <span data-ttu-id="0e2a5-120">Pour les besoins de cet exemple, une erreur a été délibérément créée en utilisant l'action **AtteindreEnregistrement** pour revenir à l'enregistrement précédent.</span><span class="sxs-lookup"><span data-stu-id="0e2a5-120">For this example, an error is deliberately created by using the **GoToRecord** action to go to the previous record.</span></span> <span data-ttu-id="0e2a5-121">La condition **\[ MacroError \] . \[ La \] \< \> numéro 0** teste **l’objet MacroError.**</span><span class="sxs-lookup"><span data-stu-id="0e2a5-121">The condition **\[MacroError\].\[Number\]\<\>0** tests the **MacroError** object.</span></span> <span data-ttu-id="0e2a5-122">Si une erreur s'est produite, le numéro de l'erreur est une valeur non nulle et l'action **ZoneMessage** s'exécute.</span><span class="sxs-lookup"><span data-stu-id="0e2a5-122">If an error has occurred, the error number is non-zero, and the **MessageBox** action runs.</span></span> <span data-ttu-id="0e2a5-123">La zone de message affiche le nom de l'action à l'origine de l'erreur (dans le cas présent, l'action **AtteindreEnregistrement** ) et le numéro de l'erreur est affiché.</span><span class="sxs-lookup"><span data-stu-id="0e2a5-123">The message box displays the name of the action that caused the error (in this case, the **GoToRecord** action), and the error number is displayed.</span></span> <span data-ttu-id="0e2a5-124">Pour finir, l’action **EffacerMacroErreur** est exécutée afin d’effacer l’objet **MacroError**.</span><span class="sxs-lookup"><span data-stu-id="0e2a5-124">Finally, running the **ClearMacroError** action clears the **MacroError** object.</span></span>

<table>
<colgroup>
<col style="width: 33%" />
<col style="width: 33%" />
<col style="width: 33%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="0e2a5-125">Condition</span><span class="sxs-lookup"><span data-stu-id="0e2a5-125">Condition</span></span></p></th>
<th><p><span data-ttu-id="0e2a5-126">Action</span><span class="sxs-lookup"><span data-stu-id="0e2a5-126">Action</span></span></p></th>
<th><p><span data-ttu-id="0e2a5-127">Arguments</span><span class="sxs-lookup"><span data-stu-id="0e2a5-127">Arguments</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p></p></td>
<td><p><span data-ttu-id="0e2a5-128"><strong>OnError</strong></span><span class="sxs-lookup"><span data-stu-id="0e2a5-128"><strong>OnError</strong></span></span></p></td>
<td><p><span data-ttu-id="0e2a5-129"><strong>Atteindre</strong> : <strong>Suivant</strong></span><span class="sxs-lookup"><span data-stu-id="0e2a5-129"><strong>Go to</strong>: <strong>Next</strong></span></span></p></td>
</tr>
<tr class="even">
<td><p></p></td>
<td><p><span data-ttu-id="0e2a5-130"><strong>OpenForm</strong></span><span class="sxs-lookup"><span data-stu-id="0e2a5-130"><strong>OpenForm</strong></span></span></p></td>
<td><p><span data-ttu-id="0e2a5-131"><strong>Nom du</strong>formulaire :<strong>CategoryForm View</strong>: <strong>Mode FormWindow</strong>: <strong>Normal</strong></span><span class="sxs-lookup"><span data-stu-id="0e2a5-131"><strong>Form Name</strong>: CategoryForm<strong>View</strong>: <strong>FormWindow Mode</strong>: <strong>Normal</strong></span></span></p></td>
</tr>
<tr class="odd">
<td><p></p></td>
<td><p><span data-ttu-id="0e2a5-132"><strong>GoToRecord</strong></span><span class="sxs-lookup"><span data-stu-id="0e2a5-132"><strong>GoToRecord</strong></span></span></p></td>
<td><p><span data-ttu-id="0e2a5-133"><strong>Type d’objet</strong>: <strong>FormObject Name</strong>: CategoryForm<strong>Record</strong>: Previous</span><span class="sxs-lookup"><span data-stu-id="0e2a5-133"><strong>Object Type</strong>: <strong>FormObject Name</strong>: CategoryForm<strong>Record</strong>: Previous</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="0e2a5-134">[MacroError]. [Number] &lt; &gt; 0</span><span class="sxs-lookup"><span data-stu-id="0e2a5-134">[MacroError].[Number]&lt;&gt;0</span></span></p></td>
<td><p><span data-ttu-id="0e2a5-135"><strong>MessageBox</strong></span><span class="sxs-lookup"><span data-stu-id="0e2a5-135"><strong>MessageBox</strong></span></span></p></td>
<td><p><span data-ttu-id="0e2a5-136"><strong>Message</strong>: = &quot; Error # &quot; &amp; [MacroError].[ Number] &amp; &quot; on &quot; &amp; [MacroError].[ ActionName]. &amp; &quot; &quot; <strong>Beep</strong>: <strong>YesType</strong>: Information</span><span class="sxs-lookup"><span data-stu-id="0e2a5-136"><strong>Message</strong>: =&quot;Error # &quot; &amp; [MacroError].[Number] &amp; &quot; on &quot; &amp; [MacroError].[ActionName] &amp; &quot; action.&quot;<strong>Beep</strong>: <strong>YesType</strong>: Information</span></span></p></td>
</tr>
<tr class="odd">
<td><p></p></td>
<td><p><span data-ttu-id="0e2a5-137"><strong>ClearMacroError</strong></span><span class="sxs-lookup"><span data-stu-id="0e2a5-137"><strong>ClearMacroError</strong></span></span></p></td>
<td><p></p></td>
</tr>
</tbody>
</table>

