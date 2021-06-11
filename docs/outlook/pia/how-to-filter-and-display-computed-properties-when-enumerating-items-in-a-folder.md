---
title: Filtrer et afficher des propriétés calculées lors de l’énumération d’éléments dans un dossier
TOCTitle: Filter and display computed properties when enumerating items in a folder
ms:assetid: b068e625-ff12-444d-a30d-51a3acba3043
ms:mtpsurl: https://msdn.microsoft.com/library/Ff184632(v=office.15)
ms:contentKeyID: 55119922
ms.date: 07/24/2014
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: 1c1702ce816714b21da860aea3e49db8a3511701
ms.sourcegitcommit: e7b38e37a9d79becfd679e10420a19890165606d
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 05/29/2019
ms.locfileid: "34542638"
---
# <a name="filter-and-display-computed-properties-when-enumerating-items-in-a-folder"></a><span data-ttu-id="0ad22-102">Filtrer et afficher des propriétés calculées lors de l’énumération d’éléments dans un dossier</span><span class="sxs-lookup"><span data-stu-id="0ad22-102">Filter and display computed properties when enumerating items in a folder</span></span>

<span data-ttu-id="0ad22-103">Cet exemple montre comment filtrer et afficher des propriétés calculées lors de l’énumération d’éléments dans un dossier.</span><span class="sxs-lookup"><span data-stu-id="0ad22-103">This example shows how to filter and display computed properties when enumerating items in a folder.</span></span>

## <a name="example"></a><span data-ttu-id="0ad22-104">Exemple</span><span class="sxs-lookup"><span data-stu-id="0ad22-104">Example</span></span>

> [!NOTE] 
> <span data-ttu-id="0ad22-105">L’exemple de code suivant est un extrait de [Programmation d’Applications pour Microsoft Office Outlook 2007](https://www.amazon.com/gp/product/0735622493?ie=UTF8&tag=msmsdn-20&linkCode=as2&camp=1789&creative=9325&creativeASIN=0735622493).</span><span class="sxs-lookup"><span data-stu-id="0ad22-105">The following code example is an excerpt from [Programming Applications for Microsoft Office Outlook 2007](https://www.amazon.com/gp/product/0735622493?ie=UTF8&tag=msmsdn-20&linkCode=as2&camp=1789&creative=9325&creativeASIN=0735622493).</span></span>


<span data-ttu-id="0ad22-p101">L'objet [Table](https://msdn.microsoft.com/library/bb652856\(v=office.15\)) représente un ensemble de données d'éléments provenant d'un objet [Folder](https://msdn.microsoft.com/library/bb645774\(v=office.15\)) ou [Search](https://msdn.microsoft.com/library/bb612611\(v=office.15\)) . L'objet [Row](https://msdn.microsoft.com/library/bb610126\(v=office.15\)) représente des lignes de données d'un objet **Table**. L'objet [Columns](https://msdn.microsoft.com/library/bb646214\(v=office.15\)) représente des propriétés de l'objet **Table**. Vous pouvez ajouter certaines propriétés à l'objet **Table** à l'aide de la méthode [Add(String)](https://msdn.microsoft.com/library/bb652865\(v=office.15\)) de l'objet **Columns**. Vous pouvez filtrer certaines propriétés à l'aide de la méthode [Restrict(String)](https://msdn.microsoft.com/library/bb612178\(v=office.15\)) de l'objet **Table**. Cependant, certaines propriétés ne peuvent pas être ajoutées à l'objet **Table** à l'aide de **Columns.Add**, ni être filtrées à l'aide de la méthode **Restrict**. Le tableau suivant indique si les propriétés sont prises en charge pour l'objet **Table** lorsque vous utilisez la méthode **Columns.Add** ou la méthode **Restrict**.</span><span class="sxs-lookup"><span data-stu-id="0ad22-p101">The [Table](https://msdn.microsoft.com/library/bb652856\(v=office.15\)) object represents a set of item data from a [Folder](https://msdn.microsoft.com/library/bb645774\(v=office.15\)) or [Search](https://msdn.microsoft.com/library/bb612611\(v=office.15\)) object. The [Row](https://msdn.microsoft.com/library/bb610126\(v=office.15\)) object represents rows of data in a **Table**. The [Columns](https://msdn.microsoft.com/library/bb646214\(v=office.15\)) object represents properties of the **Table**. You can add certain properties to the **Table** object by using the [Add(String)](https://msdn.microsoft.com/library/bb652865\(v=office.15\)) method of the **Columns** object. You can filter certain properties by using the [Restrict(String)](https://msdn.microsoft.com/library/bb612178\(v=office.15\)) method of the **Table** object. However, some properties cannot be added to the **Table** object by using **Columns.Add**, nor can they be filtered by using the **Restrict** method. The following table describes whether properties are supported for the **Table** object when you use the **Columns.Add** or **Restrict** method.</span></span>

<table>
<colgroup>
<col style="width: 33%" />
<col style="width: 33%" />
<col style="width: 33%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="0ad22-113">Propriété</span><span class="sxs-lookup"><span data-stu-id="0ad22-113">Property</span></span></p></th>
<th><p><span data-ttu-id="0ad22-114">Pour Columns.Add</span><span class="sxs-lookup"><span data-stu-id="0ad22-114">For Columns.Add</span></span></p></th>
<th><p><span data-ttu-id="0ad22-115">Pour Restrict</span><span class="sxs-lookup"><span data-stu-id="0ad22-115">For Restrict</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="0ad22-116">Propriétés binaires telle que <b>EntryID</b>.</span><span class="sxs-lookup"><span data-stu-id="0ad22-116">Binary properties such as <b>EntryID</b>.</span></span></p></td>
<td><p><span data-ttu-id="0ad22-117">Prise en charge par propriété intégrée ou espace de noms.</span><span class="sxs-lookup"><span data-stu-id="0ad22-117">Supported via built-in or namespace property.</span></span></p></td>
<td><p><span data-ttu-id="0ad22-p102">Non prise en charge. Outlook génère une erreur.</span><span class="sxs-lookup"><span data-stu-id="0ad22-p102">Not supported. Outlook will raise an error.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="0ad22-120">Propriétés Body, dont <b>Body</b> et <b>HTMLBody</b>, et représentation d’espace de noms de ces propriétés, dont <b>PR_RTF_COMPRESSED</b>.</span><span class="sxs-lookup"><span data-stu-id="0ad22-120">Body properties, including <b>Body</b> and <b>HTMLBody</b>, and namespace representation of those properties, including <b>PR_RTF_COMPRESSED</b>.</span></span></p></td>
<td><p><span data-ttu-id="0ad22-121">La propriété <b>Body</b> est prise en charge à condition qu’uniquement les 255 premiers octets de la valeur soient stockés dans un objet <b>Table</b>.</span><span class="sxs-lookup"><span data-stu-id="0ad22-121">The <b>Body</b> property is supported with a condition that only the first 255 bytes of the value are stored in a <b>Table</b> object.</span></span> <span data-ttu-id="0ad22-122">Les autres propriétés qui représentent le contenu de corps de texte en HTML ou RTF ne sont pas prises en charge.</span><span class="sxs-lookup"><span data-stu-id="0ad22-122">Other properties that represent the body content in HTML or RTF are not supported.</span></span> <span data-ttu-id="0ad22-123">Étant donné que seuls les 255 premiers octets du <b>Body</b> sont retournés, si vous voulez obtenir tout le contenu du corps d’un élément texte ou HTML, utilisez l’<b>EntryID</b> de l’élément dans la méthode <a href="https://msdn.microsoft.com/library/bb644121(v=office.15)">GetItemFromID(String, Object)</a> pour obtenir l’objet d’élément.</span><span class="sxs-lookup"><span data-stu-id="0ad22-123">Because only the first 255 bytes of <b>Body</b> are returned, if you want to obtain the full body content of an item in text or HTML, use the item’s <b>EntryID</b> in the <a href="https://msdn.microsoft.com/library/bb644121(v=office.15)">GetItemFromID(String, Object)</a> method to obtain the item object.</span></span> <span data-ttu-id="0ad22-124">Récupérez ensuite toute la valeur du <b>Body</b> via l’objet d’élément.</span><span class="sxs-lookup"><span data-stu-id="0ad22-124">Then retrieve the full value of <b>Body</b> through the item object.</span></span></p></td>
<td><p><span data-ttu-id="0ad22-p104">Seule la propriété <b>Body</b> représentée au format texte est prise en charge dans un filtre. Cela signifie que la propriété doit être référencée dans un filtre DASL (DAV Searching and Locating) sous la forme <em>urn:schemas:http-mail:textdescription</em>, et vous ne pouvez filtrer sur aucune des balises HTML du corps. Pour améliorer les performances, utilisez les mots clés de l’indexeur du contexte dans le filtre de façon à établir des correspondances avec les chaînes du corps.</span><span class="sxs-lookup"><span data-stu-id="0ad22-p104">Only the <b>Body</b> property represented in text is supported in a filter. This means that the property must be referenced in a DAV Searching and Locating (DASL) filter as <em>urn:schemas:http-mail:textdescription</em>, and you cannot filter on any HTML tags in the body. To improve performance, use context indexer keywords in the filter to match strings in the body.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="0ad22-128">Propriétés de l’ordinateur, telles que <b>AutoResolvedWinner</b> et <b>BodyFormat</b>.</span><span class="sxs-lookup"><span data-stu-id="0ad22-128">Computer properties, such as <b>AutoResolvedWinner</b> and <b>BodyFormat</b>.</span></span></p></td>
<td><p><span data-ttu-id="0ad22-129">Non prise en charge.</span><span class="sxs-lookup"><span data-stu-id="0ad22-129">Not supported.</span></span></p></td>
<td><p><span data-ttu-id="0ad22-130">Non prise en charge.</span><span class="sxs-lookup"><span data-stu-id="0ad22-130">Not supported.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="0ad22-131">Propriétés à valeurs multiples, telles que <b>Categories</b>, <b>Children</b>, <b>Companies</b>, et <b>VotingOptions</b>.</span><span class="sxs-lookup"><span data-stu-id="0ad22-131">Multivalued properties, such as <b>Categories</b>, <b>Children</b>, <b>Companies</b>, and <b>VotingOptions</b>.</span></span></p></td>
<td><p><span data-ttu-id="0ad22-132">Prise en charge.</span><span class="sxs-lookup"><span data-stu-id="0ad22-132">Supported.</span></span></p></td>
<td><p><span data-ttu-id="0ad22-133">Prise en charge à condition que vous puissiez créer une requête DASL en utilisant la représentation d’espace de noms.</span><span class="sxs-lookup"><span data-stu-id="0ad22-133">Supported, provided that you can create a DASL query by using the namespace representation.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="0ad22-134">Propriétés qui retournent un objet, telles que <b>Attachments</b>, <b>Parent</b>, <b>Recipients</b>, <b>RecurrencePattern</b>, et <b> UserProperties</b>.</span><span class="sxs-lookup"><span data-stu-id="0ad22-134">Properties that return an object, such as <b>Attachments</b>, <b>Parent</b>, <b>Recipients</b>, <b>RecurrencePattern</b>, and <b>UserProperties</b>.</span></span></p></td>
<td><p><span data-ttu-id="0ad22-135">Non prise en charge.</span><span class="sxs-lookup"><span data-stu-id="0ad22-135">Not supported.</span></span></p></td>
<td><p><span data-ttu-id="0ad22-136">Non prise en charge.</span><span class="sxs-lookup"><span data-stu-id="0ad22-136">Not supported.</span></span></p></td>
</tr>
</tbody>
</table>


<span data-ttu-id="0ad22-p105">Le tableau suivant répertorie les propriétés connues comme étant non valides qui ne peuvent pas être ajoutées à l'objet **Table** à l'aide de **Columns.Add**. Si vous tentez d'ajouter une propriété de cette liste, Outlook générera une erreur.</span><span class="sxs-lookup"><span data-stu-id="0ad22-p105">The following table lists known invalid properties that cannot be added to the **Table** object by using **Columns.Add**. If you attempt to add a property from this list, Outlook will raise an error.</span></span>

<table>
<colgroup>
<col style="width: 33%" />
<col style="width: 33%" />
<col style="width: 33%" />
</colgroup>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="0ad22-139">AutoResolvedWinner</span><span class="sxs-lookup"><span data-stu-id="0ad22-139">AutoResolvedWinner</span></span></p></td>
<td><p><span data-ttu-id="0ad22-140">BodyFormat</span><span class="sxs-lookup"><span data-stu-id="0ad22-140">BodyFormat</span></span></p></td>
<td><p><span data-ttu-id="0ad22-141">Classe</span><span class="sxs-lookup"><span data-stu-id="0ad22-141">Class</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="0ad22-142">Sociétés</span><span class="sxs-lookup"><span data-stu-id="0ad22-142">Companies</span></span></p></td>
<td><p><span data-ttu-id="0ad22-143">ContactNames</span><span class="sxs-lookup"><span data-stu-id="0ad22-143">ContactNames</span></span></p></td>
<td><p><span data-ttu-id="0ad22-144">DLName</span><span class="sxs-lookup"><span data-stu-id="0ad22-144">DLName</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="0ad22-145">DownloadState</span><span class="sxs-lookup"><span data-stu-id="0ad22-145">DownloadState</span></span></p></td>
<td><p><span data-ttu-id="0ad22-146">FlagIcon</span><span class="sxs-lookup"><span data-stu-id="0ad22-146">FlagIcon</span></span></p></td>
<td><p><span data-ttu-id="0ad22-147">HtmlBody</span><span class="sxs-lookup"><span data-stu-id="0ad22-147">HtmlBody</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="0ad22-148">InternetCodePage</span><span class="sxs-lookup"><span data-stu-id="0ad22-148">InternetCodePage</span></span></p></td>
<td><p><span data-ttu-id="0ad22-149">IsConflict</span><span class="sxs-lookup"><span data-stu-id="0ad22-149">IsConflict</span></span></p></td>
<td><p><span data-ttu-id="0ad22-150">IsMarkedAsTask</span><span class="sxs-lookup"><span data-stu-id="0ad22-150">IsMarkedAsTask</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="0ad22-151">MeetingWorkspaceURL</span><span class="sxs-lookup"><span data-stu-id="0ad22-151">MeetingWorkspaceURL</span></span></p></td>
<td><p><span data-ttu-id="0ad22-152">MemberCount</span><span class="sxs-lookup"><span data-stu-id="0ad22-152">MemberCount</span></span></p></td>
<td><p><span data-ttu-id="0ad22-153">Autorisation</span><span class="sxs-lookup"><span data-stu-id="0ad22-153">Permission</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="0ad22-154">PermissionService</span><span class="sxs-lookup"><span data-stu-id="0ad22-154">PermissionService</span></span></p></td>
<td><p><span data-ttu-id="0ad22-155">RecurrenceState</span><span class="sxs-lookup"><span data-stu-id="0ad22-155">RecurrenceState</span></span></p></td>
<td><p><span data-ttu-id="0ad22-156">ResponseState</span><span class="sxs-lookup"><span data-stu-id="0ad22-156">ResponseState</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="0ad22-157">Saved</span><span class="sxs-lookup"><span data-stu-id="0ad22-157">Saved</span></span></p></td>
<td><p><span data-ttu-id="0ad22-158">Messages envoyés</span><span class="sxs-lookup"><span data-stu-id="0ad22-158">Sent</span></span></p></td>
<td><p><span data-ttu-id="0ad22-159">Envoyé</span><span class="sxs-lookup"><span data-stu-id="0ad22-159">Submitted</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="0ad22-160">TaskSubject</span><span class="sxs-lookup"><span data-stu-id="0ad22-160">TaskSubject</span></span></p></td>
<td><p><span data-ttu-id="0ad22-161">Non lus</span><span class="sxs-lookup"><span data-stu-id="0ad22-161">Unread</span></span></p></td>
<td><p><span data-ttu-id="0ad22-162">VotingOptions</span><span class="sxs-lookup"><span data-stu-id="0ad22-162">VotingOptions</span></span></p></td>
</tr>
</tbody>
</table>


<span data-ttu-id="0ad22-163">Bien que certaines propriétés calculées ne peuvent pas être ajoutées à la colonne définie pour un tableau, l’exemple de code suivant contourne cette restriction.</span><span class="sxs-lookup"><span data-stu-id="0ad22-163">Although some computed properties cannot be added to the column set for a table, the following code example works around this limitation.</span></span> <span data-ttu-id="0ad22-164">GetToDoItems utilise une requête DASL pour limiter les éléments qui apparaissent dans l'objet **Table**.</span><span class="sxs-lookup"><span data-stu-id="0ad22-164">GetToDoItems uses a DASL query to restrict the items that appear in the **Table**.</span></span> <span data-ttu-id="0ad22-165">Si la propriété calculée a une représentation d'espace de noms, celle-ci peut être utilisée pour créer une requête DASL qui limite le retour par l'objet **Table** de lignes pour une valeur spécifiée de la propriété calculée.</span><span class="sxs-lookup"><span data-stu-id="0ad22-165">If the computed property has a namespace representation, the namespace representation is used to create a DASL query that restricts the **Table** object to return rows for a specified value of the computed property.</span></span> <span data-ttu-id="0ad22-166">GetToDoItems obtient des éléments dans la Boîte de réception où la valeur de la propriété [IsMarkedAsTask](https://msdn.microsoft.com/library/bb623631\(v=office.15\)) est égale à **true**, puis affecte des valeurs à certaines propriétés de tâche, telles que [TaskSubject](https://msdn.microsoft.com/library/bb643880\(v=office.15\)), [TaskDueDate](https://msdn.microsoft.com/library/bb623035\(v=office.15\)), [TaskStartDate](https://msdn.microsoft.com/library/bb610832\(v=office.15\)) et [TaskCompletedDate](https://msdn.microsoft.com/library/bb624055\(v=office.15\)).</span><span class="sxs-lookup"><span data-stu-id="0ad22-166">GetToDoItems gets items in the Inbox where the value of the [IsMarkedAsTask](https://msdn.microsoft.com/library/bb623631\(v=office.15\)) property is equal to **true**, and then assigns values to certain task properties such as [TaskSubject](https://msdn.microsoft.com/library/bb643880\(v=office.15\)), [TaskDueDate](https://msdn.microsoft.com/library/bb623035\(v=office.15\)), [TaskStartDate](https://msdn.microsoft.com/library/bb610832\(v=office.15\)), and [TaskCompletedDate](https://msdn.microsoft.com/library/bb624055\(v=office.15\)).</span></span> <span data-ttu-id="0ad22-167">Enfin, ces propriétés sont écrites sur les écouteurs de trace de la collection [Listeners](https://msdn.microsoft.com/library/system.diagnostics.debug.listeners.aspx).</span><span class="sxs-lookup"><span data-stu-id="0ad22-167">Finally, those properties are written to the trace listeners of the [Listeners](https://msdn.microsoft.com/library/system.diagnostics.debug.listeners.aspx) collection.</span></span>

<span data-ttu-id="0ad22-168">Si vous utilisez Visual Studio pour tester cet exemple de code, vous devez d’abord ajouter une référence au composant Bibliothèque d’objets Microsoft Outlook 15.0 et spécifier la variable lorsque vous importez l’espace de noms **Microsoft.Office.Interop.Outlook**.</span><span class="sxs-lookup"><span data-stu-id="0ad22-168">If you use Visual Studio to test this code example, you must first add a reference to the Microsoft Outlook 15.0 Object Library component and specify the Outlook variable when you import the **Microsoft.Office.Interop.Outlook** namespace.</span></span> <span data-ttu-id="0ad22-169">L’instruction **using** ne doit pas se produire juste avant les fonctions de l’exemple de code, mais doit être ajoutée avant la déclaration publique.</span><span class="sxs-lookup"><span data-stu-id="0ad22-169">The **using** statement must not occur directly before the functions in the code example but must be added before the public Class declaration.</span></span> <span data-ttu-id="0ad22-170">Le code suivant illustre l’importation et l’affectation dans C\#.</span><span class="sxs-lookup"><span data-stu-id="0ad22-170">The following line of code shows how to do the import and assignment in C\#.</span></span>

```csharp
using Outlook = Microsoft.Office.Interop.Outlook;
```


```csharp
private void GetToDoItems()
{
    // Obtain Inbox
    Outlook.Folder folder =
        Application.Session.GetDefaultFolder(
        Outlook.OlDefaultFolders.olFolderInbox)
        as Outlook.Folder;
    // DASL filter for IsMarkedAsTask
    string filter = "@SQL=" + "\"" +
        "http://schemas.microsoft.com/mapi/proptag/0x0E2B0003"
        + "\"" + " = 1";
    Outlook.Table table =
        folder.GetTable(filter,
        Outlook.OlTableContents.olUserItems);
    table.Columns.Add("TaskStartDate");
    table.Columns.Add("TaskDueDate");
    table.Columns.Add("TaskCompletedDate");
    // Use GUID/ID to represent TaskSubject
    table.Columns.Add(
        "http://schemas.microsoft.com/mapi/id/" +
        "{00062008-0000-0000-C000-000000000046}/85A4001E");
    while (!table.EndOfTable)
    {
        Outlook.Row nextRow = table.GetNextRow();
        StringBuilder sb = new StringBuilder();
        sb.AppendLine("Task Subject: " + nextRow[9]);
        sb.AppendLine("Start Date: "
            + nextRow["TaskStartDate"]);
        sb.AppendLine("Due Date: "
            + nextRow["TaskDueDate"]);
        sb.AppendLine("Completed Date: "
            + nextRow["TaskCompletedDate"]);
        sb.AppendLine();
        Debug.WriteLine(sb.ToString());
    }
}
```

## <a name="see-also"></a><span data-ttu-id="0ad22-171">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="0ad22-171">See also</span></span>

- [<span data-ttu-id="0ad22-172">Rechercher et filtrer</span><span class="sxs-lookup"><span data-stu-id="0ad22-172">Search and filter</span></span>](search-and-filter.md)

