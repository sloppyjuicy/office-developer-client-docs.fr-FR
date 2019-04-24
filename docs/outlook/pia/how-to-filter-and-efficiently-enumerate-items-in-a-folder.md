---
title: Énumération efficace et filtrage des éléments d’un dossier
TOCTitle: Filter and efficiently enumerate items in a folder
ms:assetid: efee7704-b7d9-4586-a72e-4e960ec1ffdb
ms:mtpsurl: https://msdn.microsoft.com/library/Bb612664(v=office.15)
ms:contentKeyID: 55119884
ms.date: 07/24/2014
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: 35215c24a9b953bf8406b268a6169abbd536202b
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32320306"
---
# <a name="filter-and-efficiently-enumerate-items-in-a-folder"></a>Énumération efficace et filtrage des éléments d’un dossier

Cet exemple montre comment utiliser l'objet [Table](https://msdn.microsoft.com/library/bb652856\(v=office.15\)) pour filtrer les éléments de la Boîte de réception ayant des pièces jointes et comment énumérer efficacement ces éléments en affichant les propriétés sélectionnées de chaque élément.

## <a name="example"></a>Exemple

L’exemple de code spécifie la propriété **PR\_HASATTACH** avec l’espace de noms MAPI et utilise cette propriété pour créer le filtre initial dans la méthode [GetTable](https://msdn.microsoft.com/library/bb612592\(v=office.15\)) de la Boîte de réception. L’objet **Table** d’un type d’élément a des colonnes par défaut qui représentent certaines propriétés de ce type d’élément. Pour personnaliser les colonnes, cet exemple commence par appeler la méthode [RemoveAll](https://msdn.microsoft.com/library/bb611528\(v=office.15\)) sur la collection [Columns](https://msdn.microsoft.com/library/bb646214\(v=office.15\)) de cet objet **Table**, puis appelle la méthode [Add](https://msdn.microsoft.com/library/bb652865\(v=office.15\)) sur la collection **Columns** afin d'ajouter les propriétés **EntryID**, **Subject** et **ReceivedTime** en utilisant les noms de propriétés intégrées, sachant que la colonne **ReceivedTime** stocke des valeurs exprimées dans la date et l'heure locales. 

La méthode **Columns.Add** est ensuite appelée une nouvelle fois pour ajouter la propriété **ReceiveTime** en spécifiant son espace de noms MAPI afin que cette colonne stocke la valeur en tant que valeur de date et heure UTC (Universal Coordinated Time). Enfin, l’exemple énumère chaque élément dans l’objet Table, en affichant la valeur des quatre propriétés spécifiées en tant que colonnes du tableau.

Si vous utilisez Visual Studio pour tester cet exemple de code, vous devez d’abord ajouter une référence au composant Bibliothèque d’objets Microsoft Outlook 15.0 et spécifier la variable lorsque vous importez l’espace de noms **Microsoft.Office.Interop.Outlook**. L'instruction **Importer** ou **utilisation** ne doit pas se produire juste avant les fonctions de l'exemple de code, mais doit être ajoutée avant la déclaration publique. Les lignes de code suivantes montrent comment effectuer l’importation et l’affectation dans Visual Basic et dans C\#.

```vb
Imports Outlook = Microsoft.Office.Interop.Outlook
```


```csharp
using Outlook = Microsoft.Office.Interop.Outlook;
```


```vb
Private Sub DemoTableColumns()
    Const PR_HAS_ATTACH As String = _
        "https://schemas.microsoft.com/mapi/proptag/0x0E1B000B"
    ' Obtain Inbox
    Dim folder As Outlook.Folder = _
        CType(Application.Session.GetDefaultFolder( _
        Outlook.OlDefaultFolders.olFolderInbox), _
        Outlook.Folder)
    ' Create filter
    Dim filter As String = "@SQL=" & Chr(34) _
        & PR_HAS_ATTACH & Chr(34) & " = 1"
    Dim table As Outlook.Table = _
        folder.GetTable(filter, _
        Outlook.OlTableContents.olUserItems)
    ' Remove default columns
    table.Columns.RemoveAll()
    ' Add using built-in name
    table.Columns.Add("EntryID")
    table.Columns.Add("Subject")
    table.Columns.Add("ReceivedTime")
    table.Sort("ReceivedTime", Outlook.OlSortOrder.olDescending)
    ' Add using namespace
    ' Date received
    table.Columns.Add( _
        "urn:schemas:httpmail:datereceived")
    While Not (table.EndOfTable)
        Dim nextRow As Outlook.Row = table.GetNextRow()
        Dim sb As StringBuilder = New StringBuilder()
        sb.AppendLine(nextRow("Subject").ToString())
        ' Reference column by name 
        sb.AppendLine("Received (Local): " _
            & nextRow("ReceivedTime").ToString())
        ' Reference column by index
        sb.AppendLine("Received (UTC): " & nextRow(4).ToString())
        sb.AppendLine()
        Debug.WriteLine(sb.ToString())
    End While
End Sub
```


```csharp
private void DemoTableColumns()
{
    const string PR_HAS_ATTACH =
        "https://schemas.microsoft.com/mapi/proptag/0x0E1B000B";
    // Obtain Inbox
    Outlook.Folder folder =
        Application.Session.GetDefaultFolder(
        Outlook.OlDefaultFolders.olFolderInbox)
        as Outlook.Folder;
    // Create filter
    string filter = "@SQL=" + "\""
        + PR_HAS_ATTACH + "\"" + " = 1";
    Outlook.Table table =
        folder.GetTable(filter,
        Outlook.OlTableContents.olUserItems);
    // Remove default columns
    table.Columns.RemoveAll();
    // Add using built-in name
    table.Columns.Add("EntryID");
    table.Columns.Add("Subject");
    table.Columns.Add("ReceivedTime");
    table.Sort("ReceivedTime", Outlook.OlSortOrder.olDescending);
    // Add using namespace
    // Date received
    table.Columns.Add(
        "urn:schemas:httpmail:datereceived");
    while (!table.EndOfTable)
    {
        Outlook.Row nextRow = table.GetNextRow();
        StringBuilder sb = new StringBuilder();
        sb.AppendLine(nextRow["Subject"].ToString());
        // Reference column by name 
        sb.AppendLine("Received (Local): "
            + nextRow["ReceivedTime"]);
        // Reference column by index
        sb.AppendLine("Received (UTC): " + nextRow[4]);
        sb.AppendLine();
        Debug.WriteLine(sb.ToString());
    }
}
```

## <a name="see-also"></a>Voir aussi

- [Rechercher et filtrer](search-and-filter.md)

