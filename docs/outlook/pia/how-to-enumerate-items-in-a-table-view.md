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
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32320383"
---
# <a name="enumerate-items-in-a-table-view"></a><span data-ttu-id="8d4b4-102">Énumération des éléments dans un affichage tableau</span><span class="sxs-lookup"><span data-stu-id="8d4b4-102">Enumerate items in a table view</span></span>

<span data-ttu-id="8d4b4-103">Cet exemple énumère les éléments dans un affichage tableau à l’aide de la méthode [GetTable()](https://msdn.microsoft.com/library/ff184699\(v=office.15\)).</span><span class="sxs-lookup"><span data-stu-id="8d4b4-103">This example enumerates items in a table view by using the [GetTable()](https://msdn.microsoft.com/library/ff184699\(v=office.15\)) method.</span></span>

## <a name="example"></a><span data-ttu-id="8d4b4-104">Exemple</span><span class="sxs-lookup"><span data-stu-id="8d4b4-104">Example</span></span>

<span data-ttu-id="8d4b4-p101">L'exemple de code suivant obtient un objet [Table](https://msdn.microsoft.com/library/bb652856\(v=office.15\)) à partir de l'affichage actuel du dossier Boîte de réception. L'exemple de code définit le dossier actif de l'explorateur actif sur la Boîte de réception, puis vérifie que l'affichage actuel de la Boîte de réception est un tableau. Si effectivement l'affichage actuel est un tableau, l'exemple de code appelle la méthode [GetTable()](https://msdn.microsoft.com/library/ff184699\(v=office.15\)) et affiche chaque élément représenté par chaque ligne dans l'objet **Table** retourné.</span><span class="sxs-lookup"><span data-stu-id="8d4b4-p101">The following code example obtains a [Table](https://msdn.microsoft.com/library/bb652856\(v=office.15\)) object from the current view of the Inbox folder. The code example sets the current folder of the active explorer to the Inbox, and then checks that the current view of the Inbox is a table view. If the current view is a table, the code example calls the [GetTable()](https://msdn.microsoft.com/library/ff184699\(v=office.15\)) method and displays each item represented by each row in the returned **Table**.</span></span>

<span data-ttu-id="8d4b4-108">Si vous utilisez Visual Studio pour tester cet exemple de code, vous devez d’abord ajouter une référence au composant Bibliothèque d’objets Microsoft Outlook 15.0 et spécifier la variable lorsque vous importez l’espace de noms **Microsoft.Office.Interop.Outlook**.</span><span class="sxs-lookup"><span data-stu-id="8d4b4-108">If you use Visual Studio to test this code example, you must first add a reference to the Microsoft Outlook 15.0 Object Library component and specify the Outlook variable when you import the **Microsoft.Office.Interop.Outlook** namespace.</span></span> <span data-ttu-id="8d4b4-109">L’instruction **using** ne doit pas se produire juste avant les fonctions de l’exemple de code, mais doit être ajoutée avant la déclaration publique.</span><span class="sxs-lookup"><span data-stu-id="8d4b4-109">The **using** statement must not occur directly before the functions in the code example but must be added before the public Class declaration.</span></span> <span data-ttu-id="8d4b4-110">Le code suivant illustre l’importation et l’affectation dans C\#.</span><span class="sxs-lookup"><span data-stu-id="8d4b4-110">The following line of code shows how to do the import and assignment in C\#.</span></span>

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

## <a name="see-also"></a><span data-ttu-id="8d4b4-111">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="8d4b4-111">See also</span></span>

- [<span data-ttu-id="8d4b4-112">Affichages</span><span class="sxs-lookup"><span data-stu-id="8d4b4-112">Views</span></span>](views.md)

