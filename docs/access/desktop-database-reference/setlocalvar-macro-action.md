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
ms.openlocfilehash: b257473d2acd3d17f30a3fdd579d213dcd39487b
ms.sourcegitcommit: 1dd744993ecb4bed241ace874ad26edaef1778b8
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 11/06/2018
ms.locfileid: "25996901"
---
# <a name="setlocalvar-macro-action"></a><span data-ttu-id="987f4-102">SetLocalVar, action de macro</span><span class="sxs-lookup"><span data-stu-id="987f4-102">SetLocalVar macro action</span></span>

<span data-ttu-id="987f4-103">**S’applique à**: Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="987f4-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="987f4-104">L'action **DéfinirVarLocale** crée une variable temporaire et lui affecte une valeur spécifique.</span><span class="sxs-lookup"><span data-stu-id="987f4-104">The **SetLocalVar** action creates a temporary variable and set it to a specific value.</span></span>

## <a name="setting"></a><span data-ttu-id="987f4-105">Paramètre</span><span class="sxs-lookup"><span data-stu-id="987f4-105">Setting</span></span>

<span data-ttu-id="987f4-106">L'action **DéfinirVarLocale** utilise les arguments suivants.</span><span class="sxs-lookup"><span data-stu-id="987f4-106">The **SetLocalVar** action has the following arguments.</span></span>

<table>
<colgroup>
<col style="width: 33%" />
<col style="width: 33%" />
<col style="width: 33%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="987f4-107">Argument</span><span class="sxs-lookup"><span data-stu-id="987f4-107">Argument</span></span></p></th>
<th><p><span data-ttu-id="987f4-108">Obligatoire</span><span class="sxs-lookup"><span data-stu-id="987f4-108">Required</span></span></p></th>
<th><p><span data-ttu-id="987f4-109">Description</span><span class="sxs-lookup"><span data-stu-id="987f4-109">Description</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="987f4-110"><strong>Name</strong></span><span class="sxs-lookup"><span data-stu-id="987f4-110"><strong>Name</strong></span></span></p></td>
<td><p><span data-ttu-id="987f4-111">Oui</span><span class="sxs-lookup"><span data-stu-id="987f4-111">Yes</span></span></p></td>
<td><p><span data-ttu-id="987f4-112">Chaîne qui spécifie le nom de la variable.</span><span class="sxs-lookup"><span data-stu-id="987f4-112">A string that specifies the name of the variable.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="987f4-113"><strong>Expression</strong></span><span class="sxs-lookup"><span data-stu-id="987f4-113"><strong>Expression</strong></span></span></p></td>
<td><p><span data-ttu-id="987f4-114">Oui</span><span class="sxs-lookup"><span data-stu-id="987f4-114">Yes</span></span></p></td>
<td><p><span data-ttu-id="987f4-115">Une expression qui sera utilisée pour définir la valeur de cette variable temporaire.</span><span class="sxs-lookup"><span data-stu-id="987f4-115">An expression that will be used to set the value for this temporary variable.</span></span> <span data-ttu-id="987f4-116">Ne faites pas précéder l’expression avec le signe égal (=).</span><span class="sxs-lookup"><span data-stu-id="987f4-116">Do not precede the expression with the equal sign (=).</span></span> <span data-ttu-id="987f4-117">Vous pouvez cliquer sur le bouton <strong>Générer</strong> pour utiliser le <strong>Générateur d’Expression</strong> pour définir cet argument.</span><span class="sxs-lookup"><span data-stu-id="987f4-117">You can click the <strong>Build</strong> button to use the <strong>Expression Builder</strong> to set this argument.</span></span></p></td>
</tr>
</tbody>
</table>

## <a name="remarks"></a><span data-ttu-id="987f4-118">Notes</span><span class="sxs-lookup"><span data-stu-id="987f4-118">Remarks</span></span>

<span data-ttu-id="987f4-p102">Les variables créées par l'action **DéfinirVarLocale** peuvent être utilisées uniquement dans la macro dans laquelle elles sont définies. Utilisez l'action **[DéfinirVarTemp](settempvar-macro-action.md)** pour définir une variable qui peut être utilisée dans une autre macro, dans une procédure événementielle ou dans un formulaire ou un état.</span><span class="sxs-lookup"><span data-stu-id="987f4-p102">Variables created by the **SetLocalVar** action can be used only in the macro in which they are defined. Use the **[SetTempVar](settempvar-macro-action.md)** action to define a variable that can be used in another macro, in an event procedure, or on a form or report.</span></span>

<span data-ttu-id="987f4-p103">Une fois qu'une variable temporaire a été créée, vous pouvez la référencer dans une expression. Par exemple, si vous avez créé une variable temporaire nommée TotalAmount, vous pouvez l'utiliser comme source contrôle pour une zone de texte à l'aide de la syntaxe suivante.</span><span class="sxs-lookup"><span data-stu-id="987f4-p103">Once a temporary variable has been created, you can refer to it in an expression. For example, if you created a temporary variable named TotalAmount, you could use the variable as the control source for a text box by using the following syntax.</span></span>

`=[LocalVars]![TotalAmount]`

> [!NOTE]
> <span data-ttu-id="987f4-123">[!REMARQUE] Dans une macro de données, vous n'êtes pas obligé d'utiliser la collection LocalVars pour faire référence à une variable.</span><span class="sxs-lookup"><span data-stu-id="987f4-123">In a Data Macro, you do not have to use the LocalVars collection to refer to a variable.</span></span> <span data-ttu-id="987f4-124">Par exemple, si vous avez créé une variable temporaire dans une Macro de données nommée montant total, vous pouvez utiliser la variable comme source de contrôle pour une zone de texte à l’aide de la syntaxe suivante : `=[TotalAmount]`.</span><span class="sxs-lookup"><span data-stu-id="987f4-124">For example, if you created a temporary variable in a Data Macro named TotalAmount, you could use the variable as the control source for a text box by using the following syntax: `=[TotalAmount]`.</span></span>

