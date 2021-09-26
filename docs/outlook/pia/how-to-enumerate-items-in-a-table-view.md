---
title: Énumération des éléments dans un affichage tableau
TOCTitle: Enumerate items in a table view
ms:assetid: c7d9a667-cfec-49c1-af7a-4c8063991588
ms:mtpsurl: https://msdn.microsoft.com/library/Ff184640(v=office.15)
ms:contentKeyID: 55119900
ms.date: 07/24/2014
mtps_version: v=office.15
ms.localizationpriority: medium
ms.openlocfilehash: 1ff7ab9309388c2f83f843240dd6246490085c8b
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/24/2021
ms.locfileid: "59583176"
---
# <a name="enumerate-items-in-a-table-view"></a>Énumération des éléments dans un affichage tableau

Cet exemple énumère les éléments dans un affichage tableau à l’aide de la méthode [GetTable()](https://msdn.microsoft.com/library/ff184699\(v=office.15\)).

## <a name="example"></a>Exemple

L'exemple de code suivant obtient un objet [Table](https://msdn.microsoft.com/library/bb652856\(v=office.15\)) à partir de l'affichage actuel du dossier Boîte de réception. L'exemple de code définit le dossier actif de l'explorateur actif sur la Boîte de réception, puis vérifie que l'affichage actuel de la Boîte de réception est un tableau. Si effectivement l'affichage actuel est un tableau, l'exemple de code appelle la méthode [GetTable()](https://msdn.microsoft.com/library/ff184699\(v=office.15\)) et affiche chaque élément représenté par chaque ligne dans l'objet **Table** retourné.

Si vous utilisez Visual Studio pour tester cet exemple de code, vous devez d’abord ajouter une référence au composant Bibliothèque d’objets Microsoft Outlook 15.0 et spécifier la variable lorsque vous importez l’espace de noms **Microsoft.Office.Interop.Outlook**. L’instruction **using** ne doit pas se produire juste avant les fonctions de l’exemple de code, mais doit être ajoutée avant la déclaration publique. Le code suivant illustre l’importation et l’affectation dans C\#.

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

