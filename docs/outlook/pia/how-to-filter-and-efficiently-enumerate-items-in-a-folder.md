---
title: Énumération efficace et filtrage des éléments d’un dossier
TOCTitle: Filter and efficiently enumerate items in a folder
ms:assetid: efee7704-b7d9-4586-a72e-4e960ec1ffdb
ms:mtpsurl: https://msdn.microsoft.com/library/Bb612664(v=office.15)
ms:contentKeyID: 55119884
ms.date: 07/24/2014
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: e1d5b293f89c453886cafd9effc3fb5205f9696c
ms.sourcegitcommit: e7b38e37a9d79becfd679e10420a19890165606d
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 05/29/2019
ms.locfileid: "34542596"
---
# <a name="filter-and-efficiently-enumerate-items-in-a-folder"></a><span data-ttu-id="46ecd-102">Énumération efficace et filtrage des éléments d’un dossier</span><span class="sxs-lookup"><span data-stu-id="46ecd-102">Filter and efficiently enumerate items in a folder</span></span>

<span data-ttu-id="46ecd-103">Cet exemple montre comment utiliser l'objet [Table](https://msdn.microsoft.com/library/bb652856\(v=office.15\)) pour filtrer les éléments de la Boîte de réception ayant des pièces jointes et comment énumérer efficacement ces éléments en affichant les propriétés sélectionnées de chaque élément.</span><span class="sxs-lookup"><span data-stu-id="46ecd-103">This example shows how to use the [Table](https://msdn.microsoft.com/library/bb652856\(v=office.15\)) object to filter for items in the Inbox that have attachments, and efficiently enumerate such items, displaying selected properties for each item.</span></span>

## <a name="example"></a><span data-ttu-id="46ecd-104">Exemple</span><span class="sxs-lookup"><span data-stu-id="46ecd-104">Example</span></span>

<span data-ttu-id="46ecd-105">L’exemple de code spécifie la propriété **PR\_HASATTACH** avec l’espace de noms MAPI et utilise cette propriété pour créer le filtre initial dans la méthode [GetTable](https://msdn.microsoft.com/library/bb612592\(v=office.15\)) de la Boîte de réception.</span><span class="sxs-lookup"><span data-stu-id="46ecd-105">The code sample specifies the property **PR\_HASATTACH** with the MAPI namespace, and uses the property to create the initial filter in the [GetTable](https://msdn.microsoft.com/library/bb612592\(v=office.15\)) method on the Inbox.</span></span> <span data-ttu-id="46ecd-106">L’objet **Table** d’un type d’élément a des colonnes par défaut qui représentent certaines propriétés de ce type d’élément.</span><span class="sxs-lookup"><span data-stu-id="46ecd-106">A **Table** object for an item type has default columns representing certain properties of that item type.</span></span> <span data-ttu-id="46ecd-107">Pour personnaliser les colonnes, cet exemple commence par appeler la méthode [RemoveAll](https://msdn.microsoft.com/library/bb611528\(v=office.15\)) sur la collection [Columns](https://msdn.microsoft.com/library/bb646214\(v=office.15\)) de cet objet **Table**, puis appelle la méthode [Add](https://msdn.microsoft.com/library/bb652865\(v=office.15\)) sur la collection **Columns** afin d'ajouter les propriétés **EntryID**, **Subject** et **ReceivedTime** en utilisant les noms de propriétés intégrées, sachant que la colonne **ReceivedTime** stocke des valeurs exprimées dans la date et l'heure locales.</span><span class="sxs-lookup"><span data-stu-id="46ecd-107">To customize the columns, this example first calls the [RemoveAll](https://msdn.microsoft.com/library/bb611528\(v=office.15\)) method on the [Columns](https://msdn.microsoft.com/library/bb646214\(v=office.15\)) collection of that **Table**, and then calls the [Add](https://msdn.microsoft.com/library/bb652865\(v=office.15\)) method on the **Columns** collection to add the **EntryID**, **Subject**, and **ReceivedTime** properties using the built-in property names, with the **ReceivedTime** column storing values in local date-time representation.</span></span> 

<span data-ttu-id="46ecd-108">La méthode **Columns.Add** est ensuite appelée une nouvelle fois pour ajouter la propriété **ReceiveTime** en spécifiant son espace de noms MAPI afin que cette colonne stocke la valeur en tant que valeur de date et heure UTC (Universal Coordinated Time).</span><span class="sxs-lookup"><span data-stu-id="46ecd-108">The example then calls **Columns.Add** one more time to add the **ReceiveTime** property specifying its MAPI namespace so that this column will store the value as a Universal Coordinated Time (UTC) date-time value.</span></span> <span data-ttu-id="46ecd-109">Enfin, l’exemple énumère chaque élément dans l’objet Table, en affichant la valeur des quatre propriétés spécifiées en tant que colonnes du tableau.</span><span class="sxs-lookup"><span data-stu-id="46ecd-109">Finally, the example enumerates each item in the Table, displaying the value of each of the four properties specified as the table columns.</span></span>

<span data-ttu-id="46ecd-110">Si vous utilisez Visual Studio pour tester cet exemple de code, vous devez d’abord ajouter une référence au composant Bibliothèque d’objets Microsoft Outlook 15.0 et spécifier la variable lorsque vous importez l’espace de noms **Microsoft.Office.Interop.Outlook**.</span><span class="sxs-lookup"><span data-stu-id="46ecd-110">If you use Visual Studio to test this code example, you must first add a reference to the Microsoft Outlook 15.0 Object Library component and specify the Outlook variable when you import the **Microsoft.Office.Interop.Outlook** namespace.</span></span> <span data-ttu-id="46ecd-111">L'instruction **Importer** ou **utilisation** ne doit pas se produire juste avant les fonctions de l'exemple de code, mais doit être ajoutée avant la déclaration publique.</span><span class="sxs-lookup"><span data-stu-id="46ecd-111">The **Imports** or **using** statement must not occur directly before the functions in the code example but must be added before the public Class declaration.</span></span> <span data-ttu-id="46ecd-112">Les lignes de code suivantes montrent comment effectuer l’importation et l’affectation dans Visual Basic et dans C\#.</span><span class="sxs-lookup"><span data-stu-id="46ecd-112">The following lines of code show how to do the import and assignment in Visual Basic and C\#.</span></span>

```vb
Imports Outlook = Microsoft.Office.Interop.Outlook
```


```csharp
using Outlook = Microsoft.Office.Interop.Outlook;
```


```vb
Private Sub DemoTableColumns()
    Const PR_HAS_ATTACH As String = _
        "http://schemas.microsoft.com/mapi/proptag/0x0E1B000B"
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
        "http://schemas.microsoft.com/mapi/proptag/0x0E1B000B";
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

## <a name="see-also"></a><span data-ttu-id="46ecd-113">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="46ecd-113">See also</span></span>

- [<span data-ttu-id="46ecd-114">Rechercher et filtrer</span><span class="sxs-lookup"><span data-stu-id="46ecd-114">Search and filter</span></span>](search-and-filter.md)

