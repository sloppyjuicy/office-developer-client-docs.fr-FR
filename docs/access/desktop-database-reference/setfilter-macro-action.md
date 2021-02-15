---
title: SetFilter, action de macro
TOCTitle: SetFilter macro action
ms:assetid: dee699e2-0840-1612-23ce-199ef8d30566
ms:mtpsurl: https://msdn.microsoft.com/library/Ff835438(v=office.15)
ms:contentKeyID: 48548203
ms.date: 09/18/2015
mtps_version: v=office.15
f1_keywords:
- vbaac10.chm122943
f1_categories:
- Office.Version=v15
localization_priority: Normal
ms.openlocfilehash: ac1a2c8a603fb74b56d71f73605455ecdbc87035
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32308693"
---
# <a name="setfilter-macro-action"></a><span data-ttu-id="fecac-102">SetFilter, action de macro</span><span class="sxs-lookup"><span data-stu-id="fecac-102">SetFilter macro action</span></span>

<span data-ttu-id="fecac-103">**S’applique à** : Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="fecac-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="fecac-104">Vous pouvez utiliser l’action **AppliquerFiltre** pour appliquer un filtre aux enregistrements de la feuille de données, de l’état, de la table ou du formulaire actif.</span><span class="sxs-lookup"><span data-stu-id="fecac-104">You can use the **SetFilter** action to apply a filter to the records in the active datasheet, form, report, or table.</span></span>

## <a name="setting"></a><span data-ttu-id="fecac-105">Setting</span><span class="sxs-lookup"><span data-stu-id="fecac-105">Setting</span></span>

<span data-ttu-id="fecac-106">L’action **AppliquerFiltre** utilise les arguments suivants.</span><span class="sxs-lookup"><span data-stu-id="fecac-106">The **SetFilter** action has the following arguments.</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="fecac-107">Argument de l’action</span><span class="sxs-lookup"><span data-stu-id="fecac-107">Action argument</span></span></p></th>
<th><p><span data-ttu-id="fecac-108">Description</span><span class="sxs-lookup"><span data-stu-id="fecac-108">Description</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="fecac-109">Nom du filtre</span><span class="sxs-lookup"><span data-stu-id="fecac-109">Filter Name</span></span></p></td>
<td><p><span data-ttu-id="fecac-110">Si spécifié, il s’agit du nom d’une requête ou d’un filtre enregistré en tant que requête.</span><span class="sxs-lookup"><span data-stu-id="fecac-110">If provided, the name of a query or of a filter saved as a query.</span></span> <span data-ttu-id="fecac-111">Cet argument ou l’argument Condition Where est obligatoire dans une base de données cliente.</span><span class="sxs-lookup"><span data-stu-id="fecac-111">This argument or the WhereCondition argument is required in a client database.</span></span> <span data-ttu-id="fecac-112">Dans une base de données web, cet argument n’est pas disponible.</span><span class="sxs-lookup"><span data-stu-id="fecac-112">In a web database, this argument is not available.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="fecac-113">Condition Where</span><span class="sxs-lookup"><span data-stu-id="fecac-113">Where Condition</span></span></p></td>
<td><p><span data-ttu-id="fecac-114">S'il est fourni, une clause WHERE SQL qui limite les enregistrements d'une feuille de données, d'un formulaire, d'un état ou d'une table.</span><span class="sxs-lookup"><span data-stu-id="fecac-114">If provided, a SQL WHERE clause that restricts the records in the datasheet, form, report, or table.</span></span> <span data-ttu-id="fecac-115">Dans une base de données web, cet argument est obligatoire.</span><span class="sxs-lookup"><span data-stu-id="fecac-115">In a web database, this argument is required.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="fecac-116">Nom du contrôle</span><span class="sxs-lookup"><span data-stu-id="fecac-116">Control Name</span></span></p></td>
<td><p><span data-ttu-id="fecac-p103">Si spécifié, il s'agit du nom du contrôle qui correspond au sous-formulaire ou sous-état à filtrer. Si cet argument est vide, l'objet actif est filtré.</span><span class="sxs-lookup"><span data-stu-id="fecac-p103">If provided, the name of the control that corresponds to the subform or subreport to be filtered. If empty, the current object is filtered.</span></span></p></td>
</tr>
</tbody>
</table>


## <a name="remarks"></a><span data-ttu-id="fecac-119">Remarques</span><span class="sxs-lookup"><span data-stu-id="fecac-119">Remarks</span></span>

<span data-ttu-id="fecac-120">Dans une base de données Web, l’argument Condition Where ne peut pas commencer par un signe égal (=).</span><span class="sxs-lookup"><span data-stu-id="fecac-120">In a web database, the Where Condition argument cannot begin with an equal sign (=).</span></span>

<span data-ttu-id="fecac-121">Lorsque vous exécutez cette action, le filtre est appliqué à la table, au formulaire, à l'état ou à la feuille de données (par exemple les résultats de requête) qui est actif et qui a le focus.</span><span class="sxs-lookup"><span data-stu-id="fecac-121">When you run this action, the filter is applied to the table, form, report or datasheet (for example, query result) that is active and has the focus.</span></span>

<span data-ttu-id="fecac-p104">La propriété **Filtre** de l'objet actif est utilisée pour enregistrer l'argument Condition Where et l'appliquer ultérieurement. Les filtres sont enregistrés avec les objets dans lesquels ils sont créés. Ils sont chargés automatiquement lors de l'ouverture de l'objet, mais ils ne sont pas appliqués automatiquement.</span><span class="sxs-lookup"><span data-stu-id="fecac-p104">The **Filter** property of the active object is used to save the WhereCondition argument and apply it at a later time. Filters are saved with the objects in which they are created. They are automatically loaded when the object is opened, but they are not automatically applied.</span></span>

<span data-ttu-id="fecac-125">Dans une base de données cliente, pour appliquer automatiquement un filtre lors de l'ouverture de l'objet, affectez la valeur True à la propriété **FiltrerSurchargement**.</span><span class="sxs-lookup"><span data-stu-id="fecac-125">In a client database, to automatically apply a filter when the object is opened, set the **FilterOnLoad** property to True.</span></span>

<span data-ttu-id="fecac-126">Dans une base de données Web, pour appliquer automatiquement un filtre lors de l’ouverture de l’objet, ajoutez l’action **AppliquerFiltre** à une macro et ajoutez la macro à l’événement **SurChargement** de l’objet.</span><span class="sxs-lookup"><span data-stu-id="fecac-126">In a web database, to automatically apply a filter when the object is opened, add the **SetFilter** action to a macro, and add the macro to the object's **OnLoad** event.</span></span>

## <a name="example"></a><span data-ttu-id="fecac-127">Exemple</span><span class="sxs-lookup"><span data-stu-id="fecac-127">Example</span></span>

<span data-ttu-id="fecac-128">L’exemple suivant montre comment utiliser l’action DéfinirFiltre pour filtrer le formulaire dans lequel la macro est définie.</span><span class="sxs-lookup"><span data-stu-id="fecac-128">The following example shows how to use the SetFilter action to filter the form in which the macro is defined.</span></span>

<span data-ttu-id="fecac-129">**Exemple de code fourni par** [Microsoft Access 2010 Programmer’s Reference](https://www.amazon.com/Microsoft-Access-2010-Programmers-Reference/dp/8126528125).</span><span class="sxs-lookup"><span data-stu-id="fecac-129">**Sample code provided by** the [Microsoft Access 2010 Programmer’s Reference](https://www.amazon.com/Microsoft-Access-2010-Programmers-Reference/dp/8126528125).</span></span>

```vb
    OpenForm
        Form Name sfrmFoods
        View Form
        Filter Name
        Where Condition
        Data Mode
        Window Mode Normal
    
    SetFilter
        Filter Name
        Where Condtion =[display_name] Like "*cheese*"
        Control Name
```
