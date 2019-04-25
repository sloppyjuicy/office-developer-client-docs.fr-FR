---
title: SetLocalVar, action de macro
TOCTitle: SetLocalVar macro action
ms:assetid: 8a6af395-0f76-72e2-37f3-2cff22a38b3c
ms:mtpsurl: https://msdn.microsoft.com/library/Ff197097(v=office.15)
ms:contentKeyID: 48546190
ms.date: 09/18/2015
mtps_version: v=office.15
f1_keywords:
- vbaac10.chm176660
f1_categories:
- Office.Version=v15
localization_priority: Priority
ms.openlocfilehash: 091b9717b9a2e35cfc8d0c8555e28570628065ef
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: HT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32314587"
---
# <a name="setlocalvar-macro-action"></a><span data-ttu-id="64238-102">SetLocalVar, action de macro</span><span class="sxs-lookup"><span data-stu-id="64238-102">SetLocalVar macro action</span></span>

<span data-ttu-id="64238-103">**S’applique à** : Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="64238-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="64238-104">Le **DéfinirVarLocale** action crée une variable temporaire et définissez-la sur une valeur spécifique.</span><span class="sxs-lookup"><span data-stu-id="64238-104">The **SetLocalVar** action creates a temporary variable and set it to a specific value.</span></span>

## <a name="setting"></a><span data-ttu-id="64238-105">Paramètre</span><span class="sxs-lookup"><span data-stu-id="64238-105">Setting</span></span>

<span data-ttu-id="64238-106">L’action **DéfinirVarTemp** utilise les arguments suivants :</span><span class="sxs-lookup"><span data-stu-id="64238-106">The **SetLocalVar** action has the following arguments.</span></span>

<table>
<colgroup>
<col style="width: 33%" />
<col style="width: 33%" />
<col style="width: 33%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="64238-107">Argument</span><span class="sxs-lookup"><span data-stu-id="64238-107">argument</span></span></p></th>
<th><p><span data-ttu-id="64238-108">Obligatoire</span><span class="sxs-lookup"><span data-stu-id="64238-108">Required</span></span></p></th>
<th><p><span data-ttu-id="64238-109">Description</span><span class="sxs-lookup"><span data-stu-id="64238-109">Description</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="64238-110"><strong>Name</strong></span><span class="sxs-lookup"><span data-stu-id="64238-110"><strong>Name</strong></span></span></p></td>
<td><p><span data-ttu-id="64238-111">Oui</span><span class="sxs-lookup"><span data-stu-id="64238-111">Yes</span></span></p></td>
<td><p><span data-ttu-id="64238-112">Chaîne qui spécifie le nom de la variable.</span><span class="sxs-lookup"><span data-stu-id="64238-112">A string that specifies the name of the variable.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="64238-113"><strong>Expression</strong></span><span class="sxs-lookup"><span data-stu-id="64238-113"><strong>Expression</strong></span></span></p></td>
<td><p><span data-ttu-id="64238-114">Oui</span><span class="sxs-lookup"><span data-stu-id="64238-114">Yes</span></span></p></td>
<td><p><span data-ttu-id="64238-115">Expression destiné à être utilisé pour définir la valeur de cette variable temporaire.</span><span class="sxs-lookup"><span data-stu-id="64238-115">An expression that will be used to set the value for this temporary variable.</span></span> <span data-ttu-id="64238-116">Ne faites pas précéder l’expression d’un signe égal (=).</span><span class="sxs-lookup"><span data-stu-id="64238-116">Do not precede the expression with the equal sign (=).</span></span> <span data-ttu-id="64238-117">Vous pouvez cliquer sur le bouton <strong>Générer</strong> afin d’utiliser le <strong>Générateur d’expressions</strong> pour définir cet argument.</span><span class="sxs-lookup"><span data-stu-id="64238-117">You can click the <strong>Build</strong> button  to use the <strong>Expression Builder</strong> to set this argument.</span></span></p></td>
</tr>
</tbody>
</table>

## <a name="remarks"></a><span data-ttu-id="64238-118">Remarques</span><span class="sxs-lookup"><span data-stu-id="64238-118">Remarks</span></span>

<span data-ttu-id="64238-p102">Variables créés par le **DéfinirVarLocale** action peut être utilisée uniquement dans la macro dans lequel ils sont définis. Utilisez le \*\* [DéfinirVarTemp](settempvar-macro-action.md) \*\* action pour définir une variable qui peut être utilisée dans une autre macro dans une procédure événementielle ou dans un formulaire ou état.</span><span class="sxs-lookup"><span data-stu-id="64238-p102">Variables created by the **SetLocalVar** action can be used only in the macro in which they are defined. Use the **[SetTempVar](settempvar-macro-action.md)** action to define a variable that can be used in another macro, in an event procedure, or on a form or report.</span></span>

<span data-ttu-id="64238-p103">Une fois une variable temporaire a été créée, vous pouvez la consulter dans une expression. Par exemple, si vous avez créé une variable temporaire nommée TotalAmount, vous pouvez l’utiliser comme source contrôle pour une zone de texte à l’aide de la syntaxe suivante.</span><span class="sxs-lookup"><span data-stu-id="64238-p103">Once a temporary variable has been created, you can refer to it in an expression. For example, if you created a temporary variable named TotalAmount, you could use the variable as the control source for a text box by using the following syntax.</span></span>

`=[LocalVars]![TotalAmount]`

> [!NOTE]
> <span data-ttu-id="64238-123">Dans une macro de données, vous devez ne pas utiliser la collection VarLocale pour faire référence à une variable.</span><span class="sxs-lookup"><span data-stu-id="64238-123">In a Data Macro, you do not have to use the LocalVars collection to refer to a variable.</span></span> <span data-ttu-id="64238-124">Par exemple, si vous avez créé une variable temporaire dans une macro de données nommée TotalAmount, vous pouvez utiliser la variable comme source contrôle pour une zone de texte à l’aide de la syntaxe suivante : `=[TotalAmount]`.</span><span class="sxs-lookup"><span data-stu-id="64238-124">For example, if you created a temporary variable in a Data Macro named TotalAmount, you could use the variable as the control source for a text box by using the following syntax.</span></span>

