---
title: SetWarnings, action de macro
TOCTitle: SetWarnings macro action
ms:assetid: ff95b919-b1ee-c0a0-851d-71894851bb1d
ms:mtpsurl: https://msdn.microsoft.com/library/Ff837313(v=office.15)
ms:contentKeyID: 48548965
ms.date: 09/18/2015
mtps_version: v=office.15
f1_keywords:
- vbaac10.chm165020
f1_categories:
- Office.Version=v15
localization_priority: Normal
ms.openlocfilehash: acf541bde41c282b752532cb74d5ec4fa4a13ca9
ms.sourcegitcommit: d6695c94415fa47952ee7961a69660abc0904434
ms.translationtype: Auto
ms.contentlocale: fr-FR
ms.lasthandoff: 01/17/2019
ms.locfileid: "28710404"
---
# <a name="setwarnings-macro-action"></a><span data-ttu-id="d963f-102">SetWarnings, action de macro</span><span class="sxs-lookup"><span data-stu-id="d963f-102">SetWarnings macro action</span></span>

<span data-ttu-id="d963f-103">**S’applique à**: Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="d963f-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="d963f-104">L'action **Avertissements** permet d'activer ou de désactiver les messages système.</span><span class="sxs-lookup"><span data-stu-id="d963f-104">You can use the **SetWarnings** action to turn system messages on or off.</span></span>

> [!NOTE]
> <span data-ttu-id="d963f-105">[!REMARQUE] Cette action ne sera pas autorisée si la base de données n'est pas approuvée.</span><span class="sxs-lookup"><span data-stu-id="d963f-105">This action will not be allowed if the database is not trusted.</span></span> 

## <a name="setting"></a><span data-ttu-id="d963f-106">Valeur</span><span class="sxs-lookup"><span data-stu-id="d963f-106">Setting</span></span>

<span data-ttu-id="d963f-107">L'action **Avertissements** utilise les arguments suivants :</span><span class="sxs-lookup"><span data-stu-id="d963f-107">The **SetWarnings** action has the following argument.</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="d963f-108">Argument de l’action</span><span class="sxs-lookup"><span data-stu-id="d963f-108">Action argument</span></span></p></th>
<th><p><span data-ttu-id="d963f-109">Description</span><span class="sxs-lookup"><span data-stu-id="d963f-109">Description</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="d963f-110"><strong>Avertissements actifs</strong></span><span class="sxs-lookup"><span data-stu-id="d963f-110"><strong>Warnings On</strong></span></span></p></td>
<td><p><span data-ttu-id="d963f-p101">Spécifie si les messages système sont affichés. Cliquez sur <strong>Oui</strong> pour activer les messages système ou sur <strong>Non</strong> pour les désactiver dans la zone <strong>Avertissements actifs</strong> de la section <strong>Arguments de l’action</strong> du Générateur de macro. La valeur par défaut est <strong>Non</strong>.</span><span class="sxs-lookup"><span data-stu-id="d963f-p101">Specifies whether system messages are displayed. Click <strong>Yes</strong> (to turn on system messages) or <strong>No</strong> (to turn off system messages) in the <strong>Warnings On</strong> box in the <strong>Action Arguments</strong> section of the Macro Builder Pane. The default is <strong>No</strong>.</span></span></p></td>
</tr>
</tbody>
</table>


## <a name="remarks"></a><span data-ttu-id="d963f-114">Remarques</span><span class="sxs-lookup"><span data-stu-id="d963f-114">Remarks</span></span>

<span data-ttu-id="d963f-p102">Vous pouvez utiliser cette action pour empêcher que les avertissements modaux et les boîtes de message n'interrompent la macro. Néanmoins, des messages d'erreur sont toujours affichés, et Microsoft Access affiche les boîtes de dialogue nécessitant la saisie de données, et non l'activation d'un bouton (tel que **OK**, **Annuler**, **Oui** ou **Non**) , par exemple, une boîte de dialogue dans laquelle vous devez entrer des chaînes de texte ou sélectionner une ou plusieurs options.</span><span class="sxs-lookup"><span data-stu-id="d963f-p102">You can use this action to prevent modal warnings and message boxes from stopping the macro. However, error messages are always displayed. Also, Microsoft Access displays any dialog boxes that require input other than just choosing a button (such as **OK**, **Cancel**, **Yes**, or **No**) — for example, any dialog box that requires you to enter text or select one of several options.</span></span>

<span data-ttu-id="d963f-p103">Exécuter cette action avec l'argument **Avertissements actifs** défini sur **Non** équivaut à appuyer sur la touche Entrée chaque fois qu'un avertissement ou une boîte de message s'affiche. En règle générale, la réponse à l'avertissement ou au message s'effectue en cliquant sur **OK** ou sur le bouton **Oui**.</span><span class="sxs-lookup"><span data-stu-id="d963f-p103">Carrying out this action with the **Warnings On** argument set to **No** has the same effect as pressing ENTER whenever a warning or message box is displayed. Typically, an **OK** or **Yes** button is chosen in response to the warning or message.</span></span>

<span data-ttu-id="d963f-120">À la fin de l'exécution de la macro, l'affichage des messages système est automatiquement réactivé dans Access.</span><span class="sxs-lookup"><span data-stu-id="d963f-120">When the macro finishes, Access automatically turns the display of system messages back on.</span></span>

<span data-ttu-id="d963f-p104">Cette action est souvent utilisée conjointement avec l'action **Écho**, qui masque les résultats d'une macro jusqu'à la fin de son exécution. Vous pouvez également utiliser l'action **Avertissements** pour masquer les avertissements et les boîtes de message.</span><span class="sxs-lookup"><span data-stu-id="d963f-p104">Often, you'll use this action with the **Echo** action, which hides the results of a macro until it's finished. You can use the **SetWarnings** action to hide the warnings and message boxes as well.</span></span>

> [!WARNING]
> <span data-ttu-id="d963f-p105">[!ATTENTION] Bien que l'action **Avertissements** permette de simplifier les interactions avec les macros, il est conseillé d'agir prudemment lors de la désactivation des messages système. Dans certains cas, vous choisirez d'interrompre l'exécution d'une macro lors de l'affichage d'un avertissement. Par conséquent, à moins d'être certain des résultats de toutes les actions de macro, l'utilisation de cette action n'est pas conseillée.</span><span class="sxs-lookup"><span data-stu-id="d963f-p105">Although the **SetWarnings** action can simplify interactions with macros, you must be careful about turning system messages off. In some situations, you won't want to continue a macro if a certain warning message is displayed. Unless you're confident of the outcome of all macro actions, you should avoid using this action.</span></span>

<span data-ttu-id="d963f-126">Pour exécuter l'action **Avertissements** dans un module Visual Basic pour Applications (VBA), utilisez la méthode **SetWarnings** de l'objet **DoCmd**.</span><span class="sxs-lookup"><span data-stu-id="d963f-126">To run the **SetWarnings** action in a Visual Basic for Applications (VBA) module, use the **SetWarnings** method of the **DoCmd** object.</span></span>

