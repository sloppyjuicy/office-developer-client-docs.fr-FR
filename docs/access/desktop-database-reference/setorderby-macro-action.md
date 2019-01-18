---
title: SetOrderBy, action de macro
TOCTitle: SetOrderBy macro action
ms:assetid: 78f65ce9-b56f-f476-3bd6-f3307bc22a08
ms:mtpsurl: https://msdn.microsoft.com/library/Ff196152(v=office.15)
ms:contentKeyID: 48545765
ms.date: 09/18/2015
mtps_version: v=office.15
f1_keywords:
- vbaac10.chm98639
f1_categories:
- Office.Version=v15
localization_priority: Normal
ms.openlocfilehash: 86834cd8b6132e8939067c0e34037ca1b0ef8bad
ms.sourcegitcommit: d6695c94415fa47952ee7961a69660abc0904434
ms.translationtype: Auto
ms.contentlocale: fr-FR
ms.lasthandoff: 01/17/2019
ms.locfileid: "28704419"
---
# <a name="setorderby-macro-action"></a><span data-ttu-id="86bd0-102">SetOrderBy, action de macro</span><span class="sxs-lookup"><span data-stu-id="86bd0-102">SetOrderBy macro action</span></span>


<span data-ttu-id="86bd0-103">**S’applique à**: Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="86bd0-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="86bd0-104">Vous pouvez utiliser l'action **DéfinirOrdrePar** pour spécifier comment vous souhaitez trier les enregistrements d'un formulaire, d'un état, d'une table ou d'un résultat de requête.</span><span class="sxs-lookup"><span data-stu-id="86bd0-104">You can use the **SetOrderBy** action to specify how you want to sort records in a form, report, table, or query result.</span></span>

## <a name="setting"></a><span data-ttu-id="86bd0-105">Paramètre</span><span class="sxs-lookup"><span data-stu-id="86bd0-105">Setting</span></span>

<span data-ttu-id="86bd0-106">L'action **DéfinirOrdrePar** utilise les arguments suivants.</span><span class="sxs-lookup"><span data-stu-id="86bd0-106">The **SetOrderBy** action has the following arguments.</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="86bd0-107">Argument de l’action</span><span class="sxs-lookup"><span data-stu-id="86bd0-107">Action argument</span></span></p></th>
<th><p><span data-ttu-id="86bd0-108">Description</span><span class="sxs-lookup"><span data-stu-id="86bd0-108">Description</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="86bd0-109"><strong>Trier par</strong></span><span class="sxs-lookup"><span data-stu-id="86bd0-109"><strong>Order By</strong></span></span></p></td>
<td><p><span data-ttu-id="86bd0-110">Une expression de chaîne qui inclut le nom du champ ou des champs à partir desquels trier les enregistrements et les mots clés ASC ou DESC facultatifs.</span><span class="sxs-lookup"><span data-stu-id="86bd0-110">A string expression that includes the name of the field or fields on which to sort records and the optional ASC or DESC keywords.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="86bd0-111"><strong>Nom du contrôle</strong> :</span><span class="sxs-lookup"><span data-stu-id="86bd0-111"><strong>Control Name</strong></span></span></p></td>
<td><p><span data-ttu-id="86bd0-p101">S’il est fourni et que l’objet actif est un formulaire ou un état, il s’agit du nom du contrôle qui correspond au sous-formulaire ou sous-état qui sera trié. Si l’argument est vide et que l’objet actif est un formulaire ou un état, le formulaire ou l’état parent est trié.</span><span class="sxs-lookup"><span data-stu-id="86bd0-p101">If provided and the active object is a form or report, the name of the control that corresponds to the subform or subreport that will be sorted. If empty and the active object is a form or report, the parent form or report is sorted..</span></span></p></td>
</tr>
</tbody>
</table>


## <a name="remarks"></a><span data-ttu-id="86bd0-114">Notes</span><span class="sxs-lookup"><span data-stu-id="86bd0-114">Remarks</span></span>

<span data-ttu-id="86bd0-115">Lorsque vous exécutez cette action de macro, le tri est appliqué à la table, au formulaire, à l'état ou à la feuille de données (résultat de la requête) qui est actif et qui a le focus.</span><span class="sxs-lookup"><span data-stu-id="86bd0-115">When you run this macro action, the sort is applied to the table, form, report or datasheet (query result) that is active and has the focus.</span></span>

<span data-ttu-id="86bd0-p102">L'argument Trier par est le nom des champs sur lesquels vous souhaitez trier les enregistrements. Lorsque vous utilisez plusieurs noms de champs, séparez les noms par une virgule (,). La propriété **TriPar** de l'objet actif est utilisée pour enregistrer la valeur de tri et l'appliquer ultérieurement. Les valeurs de TriPar sont enregistrées avec les objets dans lesquels elles sont créées. Elles sont chargées automatiquement lors de l'ouverture de l'objet, mais elles ne sont pas appliquées automatiquement.</span><span class="sxs-lookup"><span data-stu-id="86bd0-p102">The Order By argument is the name of the field or fields on which you want to sort records. When you use more than one field name, separate the names with a comma (,). The **OrderBy** property of the active object is used to save the ordering value and apply it at a later time. OrderBy values are saved with the objects in which they are created. They are automatically loaded when the object is opened, but they aren't automatically applied.</span></span>

<span data-ttu-id="86bd0-121">Lorsque vous définissez l'argument Trier par en entrant un ou plusieurs noms de champs et que vous exécutez ensuite la macro, les enregistrements sont triés par défaut dans l'ordre croissant.</span><span class="sxs-lookup"><span data-stu-id="86bd0-121">When you set the Order By argument by entering one or more field names and then run the macro, the records are sorted by default in ascending order.</span></span>

<span data-ttu-id="86bd0-p103">Pour trier les enregistrements par ordre décroissant, tapez DESC à la fin de l'expression d'argument Trier par. Par exemple, pour trier des enregistrements clients par ordre décroissant par nom de contact, affectez à l'argument Trier par la valeur « NomContact DESC ». Pour trier les noms par Nom décroissant et Prénom croissant, affectez à l'argument Trier par la valeur « Nom DESC, Prénom ASC ».</span><span class="sxs-lookup"><span data-stu-id="86bd0-p103">To sort records in descending order, type DESC at the end of the Order By argument expression. For example, to sort customer records in descending order by contact name, set the Order By argument to "ContactName DESC". To sort names by LastName descending, and FirstName ascending, set the Order By argument to "LastName DESC, FirstName ASC".</span></span>

