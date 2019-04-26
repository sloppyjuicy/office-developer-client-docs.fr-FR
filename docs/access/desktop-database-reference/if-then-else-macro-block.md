---
title: If...Then...Else, bloc de macro
TOCTitle: If...Then...Else macro block
ms:assetid: 0c4a4b7a-4fdb-9dbc-a94e-939a2ff1c0e5
ms:mtpsurl: https://msdn.microsoft.com/library/Ff845158(v=office.15)
ms:contentKeyID: 48543188
ms.date: 09/18/2015
mtps_version: v=office.15
localization_priority: Priority
ms.openlocfilehash: fb6cbd6cc925a3e4841d9e7d6d77332cc36c7a03
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: HT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32291893"
---
# <a name="ifthenelse-macro-block"></a><span data-ttu-id="f6695-102">If...Then...Else, bloc de macro</span><span class="sxs-lookup"><span data-stu-id="f6695-102">If...Then...Else macro block</span></span>


<span data-ttu-id="f6695-103">**S’applique à** : Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="f6695-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="f6695-104">Vous pouvez utiliser le bloc de macro **If** pour exécuter de façon conditionnelle un groupe d’actions, selon la valeur d’une expression.</span><span class="sxs-lookup"><span data-stu-id="f6695-104">You can use the **If** macro block to conditionally execute a group of actions, depending on the value of an expression.</span></span>

```vb
    If expression Then 
     Insert macro actions here ... 
    Else If expression 
     Insert macro actions here ... 
    Else 
     Insert macro actions here ... 
    End If
```

## <a name="setting"></a><span data-ttu-id="f6695-105">Paramètre</span><span class="sxs-lookup"><span data-stu-id="f6695-105">Setting</span></span>

<span data-ttu-id="f6695-106">Pour les deux **if** et **Else if**, les arguments suivants sont requis.</span><span class="sxs-lookup"><span data-stu-id="f6695-106">For both **If** and \*\* Else If\*\*, the following arguments are required.</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="f6695-107">Argument de l’action</span><span class="sxs-lookup"><span data-stu-id="f6695-107">Action argument</span></span></p></th>
<th><p><span data-ttu-id="f6695-108">Description</span><span class="sxs-lookup"><span data-stu-id="f6695-108">Description</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="f6695-109"><strong>Expression</strong></span><span class="sxs-lookup"><span data-stu-id="f6695-109"><strong>Expression</strong></span></span></p></td>
<td><p><span data-ttu-id="f6695-110">Condition que vous souhaitez tester.</span><span class="sxs-lookup"><span data-stu-id="f6695-110">The condition that you wish to test.</span></span> <span data-ttu-id="f6695-111">Il doit s’agir d’une expression évaluée à True ou False.</span><span class="sxs-lookup"><span data-stu-id="f6695-111">It must be an expression that evaluates to True or False.</span></span></p></td>
</tr>
</tbody>
</table>


## <a name="remarks"></a><span data-ttu-id="f6695-112">Remarques</span><span class="sxs-lookup"><span data-stu-id="f6695-112">Remarks</span></span>

<span data-ttu-id="f6695-p102">Lorsque vous sélectionnez le bloc de macro **If**, une zone de texte s'affiche afin de vous permettre d'entrer une expression qui représente la condition à tester. De plus, une zone de liste déroulante s'affiche, dans laquelle vous pouvez insérer une action de macro, sous laquelle le texte « End If » s'affiche automatiquement. If et End If entourent une zone dans laquelle vous pouvez entrer un groupe, ou bloc, d'actions. Le bloc s'exécute seulement si l'expression que vous entrez a la valeur True.</span><span class="sxs-lookup"><span data-stu-id="f6695-p102">When you select the **If** macro block, a textbox appears so that you can enter an expression that represents the condition you wish to test. In addition, a combo box appears where you can insert a macro action, below which the text "End If" automatically displays. The If and the End If bracket an area in which you can enter a group, or block, of actions. The block executes only if the expression that you enter is True.</span></span>

<span data-ttu-id="f6695-p103">Pour évaluer une expression différente lorsque la première expression est False, vous pouvez cliquer sur **Ajouter Sinon si** pour insérer un bloc **Else If** facultatif. Vous devez entrer une expression évaluée à True ou False. Dans ce cas, le bloc s'exécute uniquement si l'expression a la valeur True et que la première expression a la valeur False.</span><span class="sxs-lookup"><span data-stu-id="f6695-p103">To evaluate a different expression when the first expression is false, you can click **Add Else If** to insert an optional **Else If** block. You must enter an expression that evaluates to True or False. In this case, the block executes only if the expression is True and the first expression is False.</span></span>

<span data-ttu-id="f6695-120">Vous pouvez ajouter autant de blocs **Else if** que vous le souhaitez à un bloc If.</span><span class="sxs-lookup"><span data-stu-id="f6695-120">You can add as many **Else If** blocks as you like to an If block.</span></span>

<span data-ttu-id="f6695-p104">Vous pouvez cliquer sur **Ajouter Sinon** pour insérer un bloc **Else** facultatif. Dans ce cas, les actions que vous insérez sous **Else** forment le bloc **Else**, qui s'exécute uniquement lorsque les actions plus haut ne s'exécutent pas. Vous pouvez ajouter un seul bloc **Else** à un bloc **If**.</span><span class="sxs-lookup"><span data-stu-id="f6695-p104">You can click **Add Else** to insert an optional **Else** block. In this case, the actions that you insert below the **Else** form the **Else** block, which executes only when the actions above do not. You can add a single **Else** block to an **If** block.</span></span>

<span data-ttu-id="f6695-124">Dans l’exemple de code suivant, les actions de macro dans le premier bloc s’exécutent si la valeur de \[Status\] est supérieure à 0.</span><span class="sxs-lookup"><span data-stu-id="f6695-124">In the following code example, the macro actions in the first block execute if the value of [Status] is greater than 0.</span></span> <span data-ttu-id="f6695-125">Si la valeur de \[Status\] n’est pas supérieure à 0, l’expression qui suit le **Else if** est évaluée.</span><span class="sxs-lookup"><span data-stu-id="f6695-125">If the value of [Status] is not greater than 0, the expression that follows the Else If is evaluated.</span></span> <span data-ttu-id="f6695-126">Les actions de macro dans le bloc **Else if** s’exécutent si la valeur de \[Status\] est égale à 0.</span><span class="sxs-lookup"><span data-stu-id="f6695-126">The macro actions in the Else If block execute if the value of [Status] is equal to 0.</span></span> <span data-ttu-id="f6695-127">Pour finir, si ni le premier ni le deuxième bloc ne s'exécutent, les actions du bloc **Else** s'exécutent.</span><span class="sxs-lookup"><span data-stu-id="f6695-127">Finally, if neither the first block nor the second block execute, the actions in the **Else** block execute.</span></span>

```vb
    If [Status] > 0 Then 
     Insert macro actions here ... 
    Else If [Status] = 0 
     Insert macro actions here ... 
    Else 
     Insert macro actions here ... 
    End If
```

<span data-ttu-id="f6695-128">Vous pouvez imbriquer des blocs **If**.</span><span class="sxs-lookup"><span data-stu-id="f6695-128">You can nest **If** blocks.</span></span> <span data-ttu-id="f6695-129">Il peut être préférable d'imbriquer un bloc **If** dans un bloc **If** si vous souhaitez évaluer une deuxième expression lorsque la première expression a la valeur True.</span><span class="sxs-lookup"><span data-stu-id="f6695-129">You should consider nesting an **If** block within an **If** block if you want to evaluate a second expression when the first expression is True.</span></span> <span data-ttu-id="f6695-130">Dans l’exemple de code suivant, le bloc interne **If** s’exécute uniquement si la valeur de \[Status\] est à la fois supérieure à 0 *et* supérieure à 100.</span><span class="sxs-lookup"><span data-stu-id="f6695-130">In the following code example, the inner If block only executes when the value of [Status] is both greater than 0  and  greater than 100.</span></span>

```vb
    If [Status] > 0 Then 
     Insert macro actions here ... 
     If [Status] > 100 
     Insert macro actions here ... 
     EndifEnd If
```
