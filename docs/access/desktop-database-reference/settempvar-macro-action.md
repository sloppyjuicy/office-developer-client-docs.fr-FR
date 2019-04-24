---
title: SetTempVar, action de macro
TOCTitle: SetTempVar macro action
ms:assetid: 9c3b7bee-02c5-efbf-1276-4c4a1f7802d9
ms:mtpsurl: https://msdn.microsoft.com/library/Ff198102(v=office.15)
ms:contentKeyID: 48546593
ms.date: 09/18/2015
mtps_version: v=office.15
f1_keywords:
- vbaac10.chm150219
f1_categories:
- Office.Version=v15
localization_priority: Normal
ms.openlocfilehash: b630304774e521162687d4c78a6a97cf18ddb419
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32306519"
---
# <a name="settempvar-macro-action"></a><span data-ttu-id="1a7b3-102">SetTempVar, action de macro</span><span class="sxs-lookup"><span data-stu-id="1a7b3-102">SetTempVar macro action</span></span>


<span data-ttu-id="1a7b3-103">**S’applique à** : Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="1a7b3-103">**Applies to**: Access 2013, Office 2013</span></span>



<span data-ttu-id="1a7b3-p101">L'action **DéfinirVarTemp** permet de créer une variable temporaire et de la définir sur une valeur spécifique. La variable peut ensuite être utilisée en tant que condition ou argument dans les actions suivantes, dans une autre macro, dans une procédure événementielle, ou dans un formulaire ou un état.</span><span class="sxs-lookup"><span data-stu-id="1a7b3-p101">You can use the **SetTempVar** action to create a temporary variable and set it to a specific value. The variable can then be used as a condition or argument in subsequent actions, or you can use the variable in another macro, in an event procedure, or on a form or report.</span></span>

## <a name="setting"></a><span data-ttu-id="1a7b3-106">Setting</span><span class="sxs-lookup"><span data-stu-id="1a7b3-106">Setting</span></span>

<span data-ttu-id="1a7b3-107">L’action **DéfinirVarTemp** utilise les arguments suivants :</span><span class="sxs-lookup"><span data-stu-id="1a7b3-107">The **SetTempVar** action has the following arguments.</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="1a7b3-108">Argument de l’action</span><span class="sxs-lookup"><span data-stu-id="1a7b3-108">Action argument</span></span></p></th>
<th><p><span data-ttu-id="1a7b3-109">Description</span><span class="sxs-lookup"><span data-stu-id="1a7b3-109">Description</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="1a7b3-110"><strong>Nom</strong></span><span class="sxs-lookup"><span data-stu-id="1a7b3-110"><strong>Name</strong></span></span></p></td>
<td><p><span data-ttu-id="1a7b3-111">Entrez le nom de la variable temporaire.</span><span class="sxs-lookup"><span data-stu-id="1a7b3-111">Enter the name of the temporary variable.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="1a7b3-112"><strong>Expression</strong></span><span class="sxs-lookup"><span data-stu-id="1a7b3-112"><strong>Expression</strong></span></span></p></td>
<td><p><span data-ttu-id="1a7b3-113">Expression qui permet de définir la valeur de cette variable temporaire.</span><span class="sxs-lookup"><span data-stu-id="1a7b3-113">Enter an expression that will be used to set the value for this temporary variable.</span></span> <span data-ttu-id="1a7b3-114">Ne faites pas précéder l'expression du signe<strong>=</strong>égal ().</span><span class="sxs-lookup"><span data-stu-id="1a7b3-114">Do not precede the expression with the equal (<strong>=</strong>) sign.</span></span> <span data-ttu-id="1a7b3-115">Vous pouvez cliquer sur le bouton <strong>générer</strong></span><span class="sxs-lookup"><span data-stu-id="1a7b3-115">You can click the <strong>Build</strong> button</span></span> <img src="media/access-build-button.gif" title="buildbut_ZA06047218" alt="buildbut_ZA06047218" /> <span data-ttu-id="1a7b3-117">pour utiliser le générateur d'expression afin de définir cet argument.</span><span class="sxs-lookup"><span data-stu-id="1a7b3-117">to use the Expression Builder to set this argument.</span></span></p></td>
</tr>
</tbody>
</table>


## <a name="remarks"></a><span data-ttu-id="1a7b3-118">Remarques</span><span class="sxs-lookup"><span data-stu-id="1a7b3-118">Remarks</span></span>

- <span data-ttu-id="1a7b3-p103">Vous pouvez définir jusqu'à 255 variables temporaires simultanément. Si vous ne supprimez pas une variable temporaire, elle reste en mémoire jusqu'à la fermeture de la base de données. Il est conseillé de supprimer les variables temporaires lorsque vous n'en avez plus besoin. Pour supprimer une variable temporaire unique, utilisez l'action **[SupprimerVarTemp](removetempvar-macro-action.md)** et définissez son argument sur le nom de la variable temporaire à supprimer. Pour supprimer plusieurs variables temporaires en une opération, utilisez l'action **SupprimerToutesVarTemp**.</span><span class="sxs-lookup"><span data-stu-id="1a7b3-p103">You can have up to 255 temporary variables defined at one time. If you do not remove a temporary variable, it will remain in memory until you close the database. It is a good practice to remove temporary variables when you are finished using them. To remove a single temporary variable, use the **[RemoveTempVar](removetempvar-macro-action.md)** action and set its argument to the name of the temporary variable that you want to remove. If you have more than one temporary variable and you want to remove them all at once, use the **RemoveAllTempVars** action.</span></span>

- <span data-ttu-id="1a7b3-124">Les variables temporaires sont des variables globales.</span><span class="sxs-lookup"><span data-stu-id="1a7b3-124">Temporary variables are global.</span></span> <span data-ttu-id="1a7b3-125">Après la création d'une variable temporaire, vous pouvez y faire référence dans une procédure événementielle, un module Visual Basic pour Applications (VBA), une requête ou une expression.</span><span class="sxs-lookup"><span data-stu-id="1a7b3-125">Once a temporary variable has been created, you can refer to it in an event procedure, a Visual Basic for Applications (VBA) module, a query, or an expression.</span></span> <span data-ttu-id="1a7b3-126">Par exemple, si vous avez créé une variable temporaire nommée *MyVar*, vous pouvez utiliser la variable comme source de contrôle pour une zone de texte à l'aide de la syntaxe suivante:</span><span class="sxs-lookup"><span data-stu-id="1a7b3-126">For example, if you created a temporary variable named *MyVar*, you could use the variable as the control source for a text box by using the following syntax:</span></span>
    
  `=[TempVars]![MyVar]`
    
  > [!NOTE]
  > <span data-ttu-id="1a7b3-127">[!REMARQUE] Dans les macros, requêtes et procédures événementielles, il n'est pas nécessaire d'insérer un signe égal devant l'expression.</span><span class="sxs-lookup"><span data-stu-id="1a7b3-127">In macros, queries and event procedures, you do not need to precede the expression with an equal sign.</span></span>
 
  <span data-ttu-id="1a7b3-128">Vous pouvez également faire référence aux variables temporaires dans les compléments ou les bases de données référencées.</span><span class="sxs-lookup"><span data-stu-id="1a7b3-128">You can also refer to temporary variables in any add-ins or referenced databases.</span></span>

- <span data-ttu-id="1a7b3-129">Pour exécuter l’action **DéfinirVarTemp** dans un module VBA, utilisez la méthode **Add** de l’objet **TempVars**.</span><span class="sxs-lookup"><span data-stu-id="1a7b3-129">To run the **SetTempVar** action in a VBA module, use the **Add** method of the **TempVars** object.</span></span>

## <a name="example"></a><span data-ttu-id="1a7b3-130">Exemple</span><span class="sxs-lookup"><span data-stu-id="1a7b3-130">Example</span></span>

<span data-ttu-id="1a7b3-131">La macro suivante explique comment créer une variable temporaire, en utilisant d’abord l’action **DéfinirVarTemp**, puis la variable temporaire dans une condition et une boîte de message et, enfin, en supprimant la variable temporaire.</span><span class="sxs-lookup"><span data-stu-id="1a7b3-131">The following macro demonstrates how to create a temporary variable by using the **SetTempVar** action, then using the temporary variable in a condition and a message box, and then removing the temporary variable.</span></span>

<table>
<colgroup>
<col style="width: 33%" />
<col style="width: 33%" />
<col style="width: 33%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="1a7b3-132">Condition</span><span class="sxs-lookup"><span data-stu-id="1a7b3-132">Condition</span></span></p></th>
<th><p><span data-ttu-id="1a7b3-133">Action</span><span class="sxs-lookup"><span data-stu-id="1a7b3-133">Action</span></span></p></th>
<th><p><span data-ttu-id="1a7b3-134">Arguments</span><span class="sxs-lookup"><span data-stu-id="1a7b3-134">Arguments</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p></p></td>
<td><p><span data-ttu-id="1a7b3-135"><strong>DéfinirVarTemp</strong></span><span class="sxs-lookup"><span data-stu-id="1a7b3-135"><strong>SetTempVar</strong></span></span></p></td>
<td><p><span data-ttu-id="1a7b3-136"><strong>Name</strong>: MyVar<strong>expression</strong>: InputBox (&quot;entrez un nombre différent de zéro)&quot;.</span><span class="sxs-lookup"><span data-stu-id="1a7b3-136"><strong>Name</strong>: MyVar<strong>Expression</strong>: InputBox(&quot;Enter a non-zero number.&quot;)</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="1a7b3-137">[TempVars]![MaVar] &lt;&gt;0</span><span class="sxs-lookup"><span data-stu-id="1a7b3-137">[TempVars]![MyVar]&lt;&gt;0</span></span></p></td>
<td><p><span data-ttu-id="1a7b3-138"><strong>MessageBox</strong></span><span class="sxs-lookup"><span data-stu-id="1a7b3-138"><strong>MessageBox</strong></span></span></p></td>
<td><p><span data-ttu-id="1a7b3-139"><strong>Message</strong>: =&quot;vous avez &quot; &amp; entré [TempVars]! Mavar &amp; &quot;. &quot; <strong>Bip</strong>: <strong>YesType</strong>: <strong>informations</strong></span><span class="sxs-lookup"><span data-stu-id="1a7b3-139"><strong>Message</strong>: =&quot;You entered &quot; &amp; [TempVars]![MyVar] &amp; &quot;.&quot;<strong>Beep</strong>: <strong>YesType</strong>: <strong>Information</strong></span></span></p></td>
</tr>
<tr class="odd">
<td><p></p></td>
<td><p><span data-ttu-id="1a7b3-140"><strong>SupprimerVarTemp</strong></span><span class="sxs-lookup"><span data-stu-id="1a7b3-140"><strong>RemoveTempVar</strong></span></span></p></td>
<td><p><span data-ttu-id="1a7b3-141"><strong>Nom</strong>: MaVar</span><span class="sxs-lookup"><span data-stu-id="1a7b3-141"><strong>Name</strong>: MyVar</span></span></p></td>
</tr>
</tbody>
</table>

