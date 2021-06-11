---
title: Filtrer et afficher les éléments de boîte de réception modifiés le mois dernier
TOCTitle: Filter and display Inbox items modified in the last month
ms:assetid: ef6004dc-0b5a-4d1f-8937-1384d1dfc1ca
ms:mtpsurl: https://msdn.microsoft.com/library/Ff424482(v=office.15)
ms:contentKeyID: 55119886
ms.date: 07/24/2014
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: 77fe6e7df4cf67ed1ca2d62b8cf48f1b2873ccbe
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32320292"
---
# <a name="filter-and-display-inbox-items-modified-in-the-last-month"></a><span data-ttu-id="0bd44-102">Filtrer et afficher les éléments de boîte de réception modifiés le mois dernier</span><span class="sxs-lookup"><span data-stu-id="0bd44-102">Filter and display Inbox items modified in the last month</span></span>

<span data-ttu-id="0bd44-103">Cet exemple montre comment filtrer et afficher les éléments de boîte de réception qui ont été modifiés le mois dernier.</span><span class="sxs-lookup"><span data-stu-id="0bd44-103">This example shows how to filter and display Inbox items that were modified in the last month.</span></span>

## <a name="example"></a><span data-ttu-id="0bd44-104">Exemple</span><span class="sxs-lookup"><span data-stu-id="0bd44-104">Example</span></span>

> [!NOTE] 
> <span data-ttu-id="0bd44-105">L’exemple de code suivant est un extrait de [programmation d’Applications pour Microsoft Office Outlook 2007](https://www.amazon.com/gp/product/0735622493?ie=UTF8&tag=msmsdn-20&linkCode=as2&camp=1789&creative=9325&creativeASIN=0735622493).</span><span class="sxs-lookup"><span data-stu-id="0bd44-105">The following code example is an excerpt from [Programming Applications for Microsoft Office Outlook 2007](https://www.amazon.com/gp/product/0735622493?ie=UTF8&tag=msmsdn-20&linkCode=as2&camp=1789&creative=9325&creativeASIN=0735622493).</span></span>

<span data-ttu-id="0bd44-106">Le langage de requête recherche DAV et localisation (DASL) est basé sur l’implémentation de Microsoft Exchange de DASL dans Outlook.</span><span class="sxs-lookup"><span data-stu-id="0bd44-106">DAV Searching and Locating (DASL) query language is based on the Microsoft Exchange implementation of DASL in Outlook.</span></span> <span data-ttu-id="0bd44-107">Il peut être utilisé pour renvoyer des résultats en fonction de propriété pour les recherches au niveau élément dans les données de dossier, tels que celui représenté par un [Objet](https://msdn.microsoft.com/library/bb652856\(v=office.15\)) du tableau.</span><span class="sxs-lookup"><span data-stu-id="0bd44-107">It can be used to return property-based results for item-level searches in folder data, such as that represented by a [Table](https://msdn.microsoft.com/library/bb652856\(v=office.15\)) object.</span></span> <span data-ttu-id="0bd44-108">Les filtres DASL prennent en charge les comparaisons de chaînes, y compris la correspondance d'équivalence, de préfixe, de phrase et de sous-chaîne, à l'aide de l'opérateur d'égalité (=).</span><span class="sxs-lookup"><span data-stu-id="0bd44-108">DASL filters support string comparisons, including equivalence, prefix, phrase, and substring matching, by using the equal (=) operator.</span></span> <span data-ttu-id="0bd44-109">Vous pouvez utiliser des requêtes DASL pour effectuer une comparaison de date-heure ainsi qu’un filtrage.</span><span class="sxs-lookup"><span data-stu-id="0bd44-109">You can use DASL queries to perform date-time comparison and filtering.</span></span>

<span data-ttu-id="0bd44-p102">Les requêtes DASL effectuant toujours des comparaisons d'objet **DateTime** en temps UTC (Coordinated Universal Time), vous devez convertir la valeur de l'heure locale en temps UTC si vous voulez que la requête fonctionne correctement. Vous devez aussi convertir la valeur **DateTime** en une représentation sous forme de chaîne car les filtres DASL prennent en charge les comparaisons de chaînes. Vous pouvez effectuer la conversion **DateTime** de deux façons : à l'aide la méthode [LocalTimeToUTC(Object)](https://msdn.microsoft.com/library/bb645832\(v=office.15\)) de l'objet [Row](https://msdn.microsoft.com/library/bb610126\(v=office.15\)) ou à l'aide des macros **DateTime** d'Outlook.</span><span class="sxs-lookup"><span data-stu-id="0bd44-p102">Because DASL queries always perform **DateTime** comparisons in Coordinated Universal Time (UTC), you must convert the local time value to UTC if you want the query to operate correctly. You must also convert the **DateTime** value to a string representation because DASL filters support string comparisons. You can make the **DateTime** conversion in two ways: by using the [LocalTimeToUTC(Object)](https://msdn.microsoft.com/library/bb645832\(v=office.15\)) method of the [Row](https://msdn.microsoft.com/library/bb610126\(v=office.15\)) object, or by using Outlook **DateTime** macros to make the conversion.</span></span>

<span data-ttu-id="0bd44-113">La ligne de code suivante montre comment utiliser la méthode **LocalTimeToUTC** pour convertir la valeur de la propriété **LastModificationTime** (qui est une colonne par défaut dans tous les objets **Item**) en temps UTC.</span><span class="sxs-lookup"><span data-stu-id="0bd44-113">The following line of code shows how to use the **LocalTimeToUTC** method to convert the value of the **LastModificationTime** property (which is a default column in all **Item** objects) to UTC.</span></span>

```csharp
DateTime modified = nextRow.LocalTimeUTC(“LastModificationTime”);
```

<span data-ttu-id="0bd44-114">Le tableau suivant répertorie les macros **DateTime** que vous pouvez utiliser pour retourner des chaînes filtrées qui comparent la valeur d'une propriété **DateTime** donnée avec une date relative ou une plage de dates spécifiées en temps UTC.</span><span class="sxs-lookup"><span data-stu-id="0bd44-114">The following table lists the **DateTime** macros you can use to return filtered strings that compare the value of a given **DateTime** property with a specified relative date or date range in UTC.</span></span> <span data-ttu-id="0bd44-115">La valeur de la propriété SchemaName représente toute propriété **DateTime** valide référencée par espace de noms.</span><span class="sxs-lookup"><span data-stu-id="0bd44-115">The SchemaName property value represents any valid **DateTime** property referenced by namespace.</span></span>

<table>
<colgroup>
<col style="width: 33%" />
<col style="width: 33%" />
<col style="width: 33%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="0bd44-116">Macro</span><span class="sxs-lookup"><span data-stu-id="0bd44-116">Macro</span></span></p></th>
<th><p><span data-ttu-id="0bd44-117">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="0bd44-117">Syntax</span></span></p></th>
<th><p><span data-ttu-id="0bd44-118">Description</span><span class="sxs-lookup"><span data-stu-id="0bd44-118">Description</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="0bd44-119">aujourd’hui</span><span class="sxs-lookup"><span data-stu-id="0bd44-119">today</span></span></p></td>
<td><p><span data-ttu-id="0bd44-120">% aujourdh’ui("SchemaName") %</span><span class="sxs-lookup"><span data-stu-id="0bd44-120">%today(“SchemaName”)%</span></span></p></td>
<td><p><span data-ttu-id="0bd44-121">Limite les éléments dont la valeur de propriété SchemaName égale à aujourd'hui.</span><span class="sxs-lookup"><span data-stu-id="0bd44-121">Restricts for items with a SchemaName property value equal to today.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="0bd44-122">demain</span><span class="sxs-lookup"><span data-stu-id="0bd44-122">tomorrow</span></span></p></td>
<td><p><span data-ttu-id="0bd44-123">%demain("SchemaName") %</span><span class="sxs-lookup"><span data-stu-id="0bd44-123">%tomorrow(“SchemaName”)%</span></span></p></td>
<td><p><span data-ttu-id="0bd44-124">Limite les éléments dont la valeur de propriété SchemaName égale à demain.</span><span class="sxs-lookup"><span data-stu-id="0bd44-124">Restricts for items with a SchemaName property value equal to tomorrow.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="0bd44-125">hier</span><span class="sxs-lookup"><span data-stu-id="0bd44-125">yesterday</span></span></p></td>
<td><p><span data-ttu-id="0bd44-126">%hier("SchemaName") %</span><span class="sxs-lookup"><span data-stu-id="0bd44-126">%yesterday(“SchemaName”)%</span></span></p></td>
<td><p><span data-ttu-id="0bd44-127">Limite les éléments dont la valeur de propriété SchemaName égale à hier.</span><span class="sxs-lookup"><span data-stu-id="0bd44-127">Restricts for items with a SchemaName property value equal to yesterday.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="0bd44-128">7prochainsjours</span><span class="sxs-lookup"><span data-stu-id="0bd44-128">next7days</span></span></p></td>
<td><p><span data-ttu-id="0bd44-129">% 7prochainsjours("SchemaName") %</span><span class="sxs-lookup"><span data-stu-id="0bd44-129">%next7days(“SchemaName”)%</span></span></p></td>
<td><p><span data-ttu-id="0bd44-130">Limite aux éléments ayant des valeurs de propriété SchemaName dans une plage équivalente aux sept prochains jours.</span><span class="sxs-lookup"><span data-stu-id="0bd44-130">Restricts for items with SchemaName property values in a range equivalent to the next seven days.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="0bd44-131">7derniersjours</span><span class="sxs-lookup"><span data-stu-id="0bd44-131">last7days</span></span></p></td>
<td><p><span data-ttu-id="0bd44-132">%7derniersjours("SchemaName") %</span><span class="sxs-lookup"><span data-stu-id="0bd44-132">%last7days(“SchemaName”)%</span></span></p></td>
<td><p><span data-ttu-id="0bd44-133">Limite aux éléments ayant des valeurs de propriété SchemaName dans une plage équivalente aux sept derniers jours.</span><span class="sxs-lookup"><span data-stu-id="0bd44-133">Restricts for items with SchemaName property values in a range equivalent to the last seven days.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="0bd44-134">semaineprochaine</span><span class="sxs-lookup"><span data-stu-id="0bd44-134">nextweek</span></span></p></td>
<td><p><span data-ttu-id="0bd44-135">% semaineprochaine("SchemaName") %</span><span class="sxs-lookup"><span data-stu-id="0bd44-135">%nextweek(“SchemaName”)%</span></span></p></td>
<td><p><span data-ttu-id="0bd44-136">Limite aux éléments ayant des valeurs de propriété SchemaName dans une plage équivalente à la semaine prochaine.</span><span class="sxs-lookup"><span data-stu-id="0bd44-136">Restricts for items with SchemaName property values in a range equivalent to next week.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="0bd44-137">semaineencours</span><span class="sxs-lookup"><span data-stu-id="0bd44-137">thisweek</span></span></p></td>
<td><p><span data-ttu-id="0bd44-138">%semaineencours("SchemaName") %</span><span class="sxs-lookup"><span data-stu-id="0bd44-138">%thisweek(“SchemaName”)%</span></span></p></td>
<td><p><span data-ttu-id="0bd44-139">Limite aux éléments ayant des valeurs de propriété SchemaName dans une plage équivalente à cette semaine.</span><span class="sxs-lookup"><span data-stu-id="0bd44-139">Restricts for items with SchemaName property values in a range equivalent to this week.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="0bd44-140">semainedernière</span><span class="sxs-lookup"><span data-stu-id="0bd44-140">lastweek</span></span></p></td>
<td><p><span data-ttu-id="0bd44-141">%semainedernière("SchemaName") %</span><span class="sxs-lookup"><span data-stu-id="0bd44-141">%lastweek(“SchemaName”)%</span></span></p></td>
<td><p><span data-ttu-id="0bd44-142">Limite aux éléments ayant des valeurs de propriété SchemaName dans une plage équivalente à la semaine dernière.</span><span class="sxs-lookup"><span data-stu-id="0bd44-142">Restricts for items with SchemaName property values in a range equivalent to last week.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="0bd44-143">moisprochain</span><span class="sxs-lookup"><span data-stu-id="0bd44-143">nextmonth</span></span></p></td>
<td><p><span data-ttu-id="0bd44-144">%moisprochain("SchemaName") %</span><span class="sxs-lookup"><span data-stu-id="0bd44-144">%nextmonth(“SchemaName”)%</span></span></p></td>
<td><p><span data-ttu-id="0bd44-145">Limite aux éléments ayant des valeurs de propriété SchemaName dans une plage équivalente au mois prochain.</span><span class="sxs-lookup"><span data-stu-id="0bd44-145">Restricts for items with SchemaName property values in a range equivalent to next month.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="0bd44-146">moisencours</span><span class="sxs-lookup"><span data-stu-id="0bd44-146">thismonth</span></span></p></td>
<td><p><span data-ttu-id="0bd44-147">%cemois("SchemaName") %</span><span class="sxs-lookup"><span data-stu-id="0bd44-147">%thismonth(“SchemaName”)%</span></span></p></td>
<td><p><span data-ttu-id="0bd44-148">Limite aux éléments ayant des valeurs de propriété SchemaName dans une plage équivalente au mois en cours.</span><span class="sxs-lookup"><span data-stu-id="0bd44-148">Restricts for items with SchemaName property values in a range equivalent to this month.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="0bd44-149">moisdernier</span><span class="sxs-lookup"><span data-stu-id="0bd44-149">lastmonth</span></span></p></td>
<td><p><span data-ttu-id="0bd44-150">%moisdernier("SchemaName") %</span><span class="sxs-lookup"><span data-stu-id="0bd44-150">%lastmonth(“SchemaName”)%</span></span></p></td>
<td><p><span data-ttu-id="0bd44-151">Limite aux éléments ayant des valeurs de propriété SchemaName dans une plage équivalente au mois dernier.</span><span class="sxs-lookup"><span data-stu-id="0bd44-151">Restricts for items with SchemaName property values in a range equivalent to last month.</span></span></p></td>
</tr>
</tbody>
</table>


<span data-ttu-id="0bd44-152">Dans l'exemple suivant, DemoDASLDateMacro crée une requête DASL qui utilise la macro **DateTime lastmonth** pour filtrer des éléments de la boîte de réception (Inbox) de l'utilisateur qui ont été modifiés au cours du dernier mois.</span><span class="sxs-lookup"><span data-stu-id="0bd44-152">In the following example, DemoDASLDateMacro creates a DASL query that uses the **lastmonthDateTime** macro to filter for items in the user’s Inbox that were modified in the last month.</span></span> <span data-ttu-id="0bd44-153">Il crée ensuite un **objet** du tableau avec ce filtre et énumère et affiche les lignes dans l’**objet** du tableau restreint.</span><span class="sxs-lookup"><span data-stu-id="0bd44-153">It then creates a **Table** object with that filter, and enumerates and displays the rows in the restricted **Table** object.</span></span>

<span data-ttu-id="0bd44-154">Si vous utilisez Visual Studio pour tester cet exemple de code, vous devez d’abord ajouter une référence au composant Bibliothèque d’objets Microsoft Outlook 15.0 et spécifier la variable lorsque vous importez l’espace de noms **Microsoft.Office.Interop.Outlook**.</span><span class="sxs-lookup"><span data-stu-id="0bd44-154">If you use Visual Studio to test this code example, you must first add a reference to the Microsoft Outlook 15.0 Object Library component and specify the Outlook variable when you import the **Microsoft.Office.Interop.Outlook** namespace.</span></span> <span data-ttu-id="0bd44-155">L’instruction **using** ne doit pas se produire juste avant les fonctions de l’exemple de code, mais doit être ajoutée avant la déclaration publique.</span><span class="sxs-lookup"><span data-stu-id="0bd44-155">The **using** statement must not occur directly before the functions in the code example but must be added before the public Class declaration.</span></span> <span data-ttu-id="0bd44-156">Le code suivant illustre l’importation et l’affectation dans C\#.</span><span class="sxs-lookup"><span data-stu-id="0bd44-156">The following line of code shows how to do the import and assignment in C\#.</span></span>

```csharp
using Outlook = Microsoft.Office.Interop.Outlook;
```


```csharp
private void DemoDASLDateMacro()
{
    string filter = "@SQL=" + "%lastmonth(" + "\"" +
        "DAV:getlastmodified" + "\"" + ")%";
    Outlook.Table table = Application.Session.GetDefaultFolder(
        Outlook.OlDefaultFolders.olFolderInbox).GetTable(
        filter, Outlook.OlTableContents.olUserItems);
    while (!table.EndOfTable)
    {
        Outlook.Row row = table.GetNextRow();
        Debug.WriteLine(row["Subject"]);
    }
}
```

## <a name="see-also"></a><span data-ttu-id="0bd44-157">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="0bd44-157">See also</span></span>

- [<span data-ttu-id="0bd44-158">Rechercher et filtrer</span><span class="sxs-lookup"><span data-stu-id="0bd44-158">Search and filter</span></span>](search-and-filter.md)

