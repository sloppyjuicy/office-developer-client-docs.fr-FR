---
title: Énumération des éléments dans un affichage tableau
TOCTitle: Enumerate items in a table view
ms:assetid: c7d9a667-cfec-49c1-af7a-4c8063991588
ms:mtpsurl: https://msdn.microsoft.com/library/Ff184640(v=office.15)
ms:contentKeyID: 55119900
ms.date: 07/24/2014
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: b3bde66fd07a39aa8a63219876b9bdbcf72e00f7
ms.sourcegitcommit: d6695c94415fa47952ee7961a69660abc0904434
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/17/2019
ms.locfileid: "28717677"
---
# <a name="enumerate-items-in-a-table-view"></a>Énumération des éléments dans un affichage tableau

Cet exemple énumère les éléments dans un affichage tableau à l’aide de la méthode [GetTable()](https://msdn.microsoft.com/library/ff184699\(v=office.15\)).

## <a name="example"></a>Exemple

L'exemple de code suivant obtient un objet [Table](https://msdn.microsoft.com/library/bb652856\(v=office.15\)) à partir de l'affichage actuel du dossier Boîte de réception. L'exemple de code définit le dossier actif de l'explorateur actif sur la Boîte de réception, puis vérifie que l'affichage actuel de la Boîte de réception est un tableau. Si effectivement l'affichage actuel est un tableau, l'exemple de code appelle la méthode [GetTable()](https://msdn.microsoft.com/library/ff184699\(v=office.15\)) et affiche chaque élément représenté par chaque ligne dans l'objet **Table** retourné.

Si vous utilisez Visual Studio pour tester cet exemple de code, vous devez d’abord ajouter une référence au composant Bibliothèque d’objets Microsoft Outlook 15.0 et spécifier la variable lorsque vous importez l’espace de noms **Microsoft.Office.Interop.Outlook**. L'instruction **d’utilisation** ne doit pas se produire juste avant les fonctions de l'exemple de code, mais doit être ajoutée avant la déclaration publique. La ligne de code suivante montre comment effectuer l’importation et la tâche dans C\#.

```csharp
using Outlook = Microsoft.Office.Interop.Outlook;
```


```csharp
private void DemoViewGetTable()
{
    // Obtain Inbox.
    Outlook.Folder inbox =
        Application.Session.GetDefaultFolder(
        Outlook.OlDefaultFolders.olFolderInbox)
        as Outlook.Folder;
    // Set ActiveExplorer.CurrentFolder to Inbox.
    // Inbox must be current folder
    // for View.GetTable to work correctly.
    Application.ActiveExplorer().CurrentFolder = inbox;
    // Ensure that current view is TableView.
    if (inbox.CurrentView.ViewType == 
        Outlook.OlViewType.olTableView)
    {
        Outlook.TableView view = 
            inbox.CurrentView as Outlook.TableView;
        // No arguments needed for View.GetTable.
        Outlook.Table table = view.GetTable();
        Debug.WriteLine("View Count=" 
            + table.GetRowCount().ToString());
        while (!table.EndOfTable)
        {
            // First row in Table.
            Outlook.Row nextRow = table.GetNextRow();
            Debug.WriteLine(nextRow["Subject"]
                + " Modified: "
                + nextRow["LastModificationTime"]);
        }
    }
}
```

## <a name="see-also"></a>Voir aussi

- [Affichages](views.md)

