---
title: Filtrer et afficher des propriétés calculées lors de l’énumération d’éléments dans un dossier
TOCTitle: Filter and display computed properties when enumerating items in a folder
ms:assetid: b068e625-ff12-444d-a30d-51a3acba3043
ms:mtpsurl: https://msdn.microsoft.com/library/Ff184632(v=office.15)
ms:contentKeyID: 55119922
ms.date: 07/24/2014
mtps_version: v=office.15
ms.localizationpriority: medium
ms.openlocfilehash: c7f3159c8ec8f2086c93dd1d7f8224d2b389d527
ms.sourcegitcommit: 241637561d21b7752ec690b5179e72b6703eaced
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/18/2022
ms.locfileid: "63634512"
---
# <a name="filter-and-display-computed-properties-when-enumerating-items-in-a-folder"></a>Filtrer et afficher des propriétés calculées lors de l’énumération d’éléments dans un dossier

Cet exemple montre comment filtrer et afficher des propriétés calculées lors de l’énumération d’éléments dans un dossier.

## <a name="example"></a>Exemple

> [!NOTE] 
> L’exemple de code suivant est un extrait de [Programmation d’Applications pour Microsoft Office Outlook 2007](https://www.amazon.com/gp/product/0735622493?ie=UTF8&tag=msmsdn-20&linkCode=as2&camp=1789&creative=9325&creativeASIN=0735622493).


L'objet [Table](https://msdn.microsoft.com/library/bb652856\(v=office.15\)) représente un ensemble de données d'éléments provenant d'un objet [Folder](https://msdn.microsoft.com/library/bb645774\(v=office.15\)) ou [Search](https://msdn.microsoft.com/library/bb612611\(v=office.15\)) . L'objet [Row](https://msdn.microsoft.com/library/bb610126\(v=office.15\)) représente des lignes de données d'un objet **Table**. L'objet [Columns](https://msdn.microsoft.com/library/bb646214\(v=office.15\)) représente des propriétés de l'objet **Table**. Vous pouvez ajouter certaines propriétés à l'objet **Table** à l'aide de la méthode [Add(String)](https://msdn.microsoft.com/library/bb652865\(v=office.15\)) de l'objet **Columns**. Vous pouvez filtrer certaines propriétés à l'aide de la méthode [Restrict(String)](https://msdn.microsoft.com/library/bb612178\(v=office.15\)) de l'objet **Table**. Cependant, certaines propriétés ne peuvent pas être ajoutées à l'objet **Table** à l'aide de **Columns.Add**, ni être filtrées à l'aide de la méthode **Restrict**. Le tableau suivant indique si les propriétés sont prises en charge pour l'objet **Table** lorsque vous utilisez la méthode **Columns.Add** ou la méthode **Restrict**.

<table>
<colgroup>
<col />
<col />
<col />
</colgroup>
<thead>
<tr class="header">
<th><p>Propriété</p></th>
<th><p>Pour Columns.Add</p></th>
<th><p>Pour Restrict</p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p>Propriétés binaires telle que <b>EntryID</b>.</p></td>
<td><p>Prise en charge par propriété intégrée ou espace de noms.</p></td>
<td><p>Non prise en charge. Outlook génère une erreur.</p></td>
</tr>
<tr class="even">
<td><p>Propriétés Body, dont <b>Body</b> et <b>HTMLBody</b>, et représentation d’espace de noms de ces propriétés, dont <b>PR_RTF_COMPRESSED</b>.</p></td>
<td><p>La propriété <b>Body</b> est prise en charge à condition qu’uniquement les 255 premiers octets de la valeur soient stockés dans un objet <b>Table</b>. Les autres propriétés qui représentent le contenu de corps de texte en HTML ou RTF ne sont pas prises en charge. Étant donné que seuls les 255 premiers octets du <b>Body</b> sont retournés, si vous voulez obtenir tout le contenu du corps d’un élément texte ou HTML, utilisez l’<b>EntryID</b> de l’élément dans la méthode <a href="https://msdn.microsoft.com/library/bb644121(v=office.15)">GetItemFromID(String, Object)</a> pour obtenir l’objet d’élément. Récupérez ensuite toute la valeur du <b>Body</b> via l’objet d’élément.</p></td>
<td><p>Seule la propriété <b>Body</b> représentée au format texte est prise en charge dans un filtre. Cela signifie que la propriété doit être référencée dans un filtre DASL (DAV Searching and Locating) sous la forme <em>urn:schemas:http-mail:textdescription</em>, et vous ne pouvez filtrer sur aucune des balises HTML du corps. Pour améliorer les performances, utilisez les mots clés de l’indexeur du contexte dans le filtre de façon à établir des correspondances avec les chaînes du corps.</p></td>
</tr>
<tr class="odd">
<td><p>Propriétés de l’ordinateur, telles que <b>AutoResolvedWinner</b> et <b>BodyFormat</b>.</p></td>
<td><p>Non prise en charge.</p></td>
<td><p>Non prise en charge.</p></td>
</tr>
<tr class="even">
<td><p>Propriétés à valeurs multiples, telles que <b>Categories</b>, <b>Children</b>, <b>Companies</b>, et <b>VotingOptions</b>.</p></td>
<td><p>Prise en charge.</p></td>
<td><p>Prise en charge à condition que vous puissiez créer une requête DASL en utilisant la représentation d’espace de noms.</p></td>
</tr>
<tr class="odd">
<td><p>Propriétés qui retournent un objet, telles que <b>Attachments</b>, <b>Parent</b>, <b>Recipients</b>, <b>RecurrencePattern</b>, et <b> UserProperties</b>.</p></td>
<td><p>Non prise en charge.</p></td>
<td><p>Non prise en charge.</p></td>
</tr>
</tbody>
</table>


Le tableau suivant répertorie les propriétés connues comme étant non valides qui ne peuvent pas être ajoutées à l'objet **Table** à l'aide de **Columns.Add**. Si vous tentez d'ajouter une propriété de cette liste, Outlook générera une erreur.

<table>
<colgroup>
<col />
<col />
<col />
</colgroup>
<tbody>
<tr class="odd">
<td><p>AutoResolvedWinner</p></td>
<td><p>BodyFormat</p></td>
<td><p>Classe</p></td>
</tr>
<tr class="even">
<td><p>Sociétés</p></td>
<td><p>ContactNames</p></td>
<td><p>DLName</p></td>
</tr>
<tr class="odd">
<td><p>DownloadState</p></td>
<td><p>FlagIcon</p></td>
<td><p>HtmlBody</p></td>
</tr>
<tr class="even">
<td><p>InternetCodePage</p></td>
<td><p>IsConflict</p></td>
<td><p>IsMarkedAsTask</p></td>
</tr>
<tr class="odd">
<td><p>MeetingWorkspaceURL</p></td>
<td><p>MemberCount</p></td>
<td><p>Autorisation</p></td>
</tr>
<tr class="even">
<td><p>PermissionService</p></td>
<td><p>RecurrenceState</p></td>
<td><p>ResponseState</p></td>
</tr>
<tr class="odd">
<td><p>Saved</p></td>
<td><p>Messages envoyés</p></td>
<td><p>Envoyé</p></td>
</tr>
<tr class="even">
<td><p>TaskSubject</p></td>
<td><p>Non lus</p></td>
<td><p>VotingOptions</p></td>
</tr>
</tbody>
</table>


Bien que certaines propriétés calculées ne peuvent pas être ajoutées à la colonne définie pour un tableau, l’exemple de code suivant contourne cette restriction. GetToDoItems utilise une requête DASL pour limiter les éléments qui apparaissent dans l'objet **Table**. Si la propriété calculée a une représentation d'espace de noms, celle-ci peut être utilisée pour créer une requête DASL qui limite le retour par l'objet **Table** de lignes pour une valeur spécifiée de la propriété calculée. GetToDoItems obtient des éléments dans la Boîte de réception où la valeur de la propriété [IsMarkedAsTask](https://msdn.microsoft.com/library/bb623631\(v=office.15\)) est égale à **true**, puis affecte des valeurs à certaines propriétés de tâche, telles que [TaskSubject](https://msdn.microsoft.com/library/bb643880\(v=office.15\)), [TaskDueDate](https://msdn.microsoft.com/library/bb623035\(v=office.15\)), [TaskStartDate](https://msdn.microsoft.com/library/bb610832\(v=office.15\)) et [TaskCompletedDate](https://msdn.microsoft.com/library/bb624055\(v=office.15\)). Enfin, ces propriétés sont écrites sur les écouteurs de trace de la collection [Listeners](https://msdn.microsoft.com/library/system.diagnostics.debug.listeners.aspx).

Si vous utilisez Visual Studio pour tester cet exemple de code, vous devez d’abord ajouter une référence au composant Bibliothèque d'objets Microsoft Outlook 15.0 et spécifier la variable Outlook lorsque vous importez l’espace de noms **Microsoft.Office.Interop.Outlook**. L’instruction **using** ne doit pas se produire juste avant les fonctions de l’exemple de code, mais doit être ajoutée avant la déclaration Class publique. La ligne de code suivante montre comment effectuer l’importation et l’affectation dans C \#.

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

## <a name="see-also"></a>Voir aussi

- [Rechercher et filtrer](search-and-filter.md)

