---
title: Si... Ensuite... Else Macro Block (Access custom web app)
manager: kelbow
ms.date: 09/05/2017
ms.audience: Developer
ms.topic: overview
localization_priority: Normal
ms.assetid: 18d28dc1-c41f-47c6-b5c7-258d5f877d01
description: Vous pouvez utiliser le bloc de macro If pour exécuter de façon conditionnelle un groupe d’actions, selon la valeur d’une expression.
ms.openlocfilehash: 6fe82e2c42f8e5d93cdc26798e7572e32d6cdc7e
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/28/2019
ms.locfileid: "33434493"
---
# <a name="ifthenelse-macro-block-access-custom-web-app"></a><span data-ttu-id="13a62-103">Si... Ensuite... Else Macro Block (Access custom web app)</span><span class="sxs-lookup"><span data-stu-id="13a62-103">If...Then...Else Macro Block (Access custom web app)</span></span>

<span data-ttu-id="13a62-104">Vous pouvez utiliser le bloc de macro **If** pour exécuter de façon conditionnelle un groupe d’actions, selon la valeur d’une expression.</span><span class="sxs-lookup"><span data-stu-id="13a62-104">You can use the **If** macro block to conditionally execute a group of actions, depending on the value of an expression.</span></span> 
  
> [!IMPORTANT]
> <span data-ttu-id="13a62-p101">Microsoft ne recommande plus la création et l'utilisation d'applications web Access dans SharePoint. En guise d'alternative, vous pouvez utiliser [Microsoft PowerApps](https://powerapps.microsoft.com/en-us/) pour générer des solutions d'entreprise sans code pour le web et les appareils mobiles.</span><span class="sxs-lookup"><span data-stu-id="13a62-p101">Microsoft no longer recommends creating and using Access web apps in SharePoint. As an alternative, consider using [Microsoft PowerApps](https://powerapps.microsoft.com/en-us/) to build no-code business solutions for the web and mobile devices.</span></span> 
  
## <a name="syntax"></a><span data-ttu-id="13a62-107">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="13a62-107">Syntax</span></span>

```vb
IfexpressionThen 
 Insert macro actions here ... 
Else Ifexpression  
 Insert macro actions here ... 
Else 
 Insert macro actions here ... 
End If
```

## <a name="setting"></a><span data-ttu-id="13a62-108">Setting</span><span class="sxs-lookup"><span data-stu-id="13a62-108">Setting</span></span>

<span data-ttu-id="13a62-109">For both **If** and \*\* Else If \*\*, the following arguments are required.</span><span class="sxs-lookup"><span data-stu-id="13a62-109">For both **If** and \*\* Else If \*\*, the following arguments are required.</span></span> 
  
|<span data-ttu-id="13a62-110">**Argument de l'action**</span><span class="sxs-lookup"><span data-stu-id="13a62-110">**Action argument**</span></span>|<span data-ttu-id="13a62-111">**Description**</span><span class="sxs-lookup"><span data-stu-id="13a62-111">**Description**</span></span>|
|:-----|:-----|
|<span data-ttu-id="13a62-112">**Expression**</span><span class="sxs-lookup"><span data-stu-id="13a62-112">**Expression**</span></span> <br/> |<span data-ttu-id="13a62-113">Condition que vous souhaitez tester.</span><span class="sxs-lookup"><span data-stu-id="13a62-113">The condition that you wish to test.</span></span> <span data-ttu-id="13a62-114">Il doit s’agir d’une expression évaluée à True ou False.</span><span class="sxs-lookup"><span data-stu-id="13a62-114">It must be an expression that evaluates to True or False.</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="13a62-115">Remarques</span><span class="sxs-lookup"><span data-stu-id="13a62-115">Remarks</span></span>

<span data-ttu-id="13a62-p103">Lorsque vous sélectionnez le bloc de macro **If**, une zone de texte s'affiche afin de vous permettre d'entrer une expression qui représente la condition à tester. De plus, une zone de liste déroulante s'affiche, dans laquelle vous pouvez insérer une action de macro, sous laquelle le texte « End If » s'affiche automatiquement. If et End If entourent une zone dans laquelle vous pouvez entrer un groupe, ou bloc, d'actions. Le bloc s'exécute seulement si l'expression que vous entrez a la valeur True.</span><span class="sxs-lookup"><span data-stu-id="13a62-p103">When you select the **If** macro block, a textbox appears so that you can enter an expression that represents the condition you wish to test. In addition, a combo box appears where you can insert a macro action, below which the text "End If" automatically displays. The If and the End If bracket an area in which you can enter a group, or block, of actions. The block executes only if the expression that you enter is True.</span></span> 
  
<span data-ttu-id="13a62-p104">Pour évaluer une expression différente lorsque la première expression est False, vous pouvez cliquer sur **Ajouter Sinon si** pour insérer un bloc **Else If** facultatif. Vous devez entrer une expression évaluée à True ou False. Dans ce cas, le bloc s'exécute uniquement si l'expression a la valeur True et que la première expression a la valeur False.</span><span class="sxs-lookup"><span data-stu-id="13a62-p104">To evaluate a different expression when the first expression is false, you can click **Add Else If** to insert an optional **Else If** block. You must enter an expression that evaluates to True or False. In this case, the block executes only if the expression is True and the first expression is False.</span></span> 
  
<span data-ttu-id="13a62-123">Vous pouvez ajouter autant de blocs **Else if** que vous le souhaitez à un bloc If.</span><span class="sxs-lookup"><span data-stu-id="13a62-123">You can add as many **Else If** blocks as you like to an If block.</span></span> 
  
<span data-ttu-id="13a62-p105">Vous pouvez cliquer sur **Ajouter Sinon** pour insérer un bloc **Else** facultatif. Dans ce cas, les actions que vous insérez sous **Else** forment le bloc **Else**, qui s'exécute uniquement lorsque les actions plus haut ne s'exécutent pas. Vous pouvez ajouter un seul bloc **Else** à un bloc **If**.</span><span class="sxs-lookup"><span data-stu-id="13a62-p105">You can click **Add Else** to insert an optional **Else** block. In this case, the actions that you insert below the **Else** form the **Else** block, which executes only when the actions above do not. You can add a single **Else** block to an **If** block.</span></span> 
  
<span data-ttu-id="13a62-p106">Dans l'exemple de code suivant, les actions de macro du premier bloc s'exécutent si la valeur de [Status] est supérieure à 0. Si la valeur de [Status] n'est pas supérieure à 0, l'expression qui suit **Else If** est évaluée. Les actions de macro du bloc **Else If** s'exécutent si la valeur de [Status] est égale à 0. Pour finir, si ni le premier ni le deuxième bloc ne s'exécutent, les actions du bloc **Else** s'exécutent.</span><span class="sxs-lookup"><span data-stu-id="13a62-p106">In the following code example, the macro actions in the first block execute if the value of [Status] is greater than 0. If the value of [Status] is not greater than 0, the expression that follows the **Else If** is evaluated. The macro actions in the **Else If** block execute if the value of [Status] is equal to 0. Finally, if neither the first block nor the second block execute, the actions in the **Else** block execute.</span></span> 
  
```vb
If[Status] > 0Then 
 Insert macro actions here ... 
Else If[Status] = 0  
 Insert macro actions here ... 
Else 
 Insert macro actions here ... 
End If
```

<span data-ttu-id="13a62-p107">Vous pouvez imbriquer des blocs **If**. Il peut être préférable d'imbriquer un bloc **If** dans un bloc **If** si vous souhaitez évaluer une deuxième expression lorsque la première expression a la valeur True. Dans l'exemple de code suivant, le bloc **If** interne s'exécute uniquement lorsque la valeur de [Status] est à la fois supérieure à 0  *et*  supérieure à 100.</span><span class="sxs-lookup"><span data-stu-id="13a62-p107">You can nest **If** blocks. You should consider nesting an **If** block within an **If** block if you want to evaluate a second expression when the first expression is True. In the following code example, the inner **If** block only executes when the value of [Status] is both greater than 0  *and*  greater than 100.</span></span> 
  

