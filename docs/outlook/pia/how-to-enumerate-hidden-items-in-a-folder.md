---
title: Énumération des éléments masqués d’un dossier
TOCTitle: Enumerate hidden items in a folder
ms:assetid: dafad1fb-94ce-4584-b5d1-2de5fad2f72a
ms:mtpsurl: https://msdn.microsoft.com/library/Ff184645(v=office.15)
ms:contentKeyID: 55119888
ms.date: 07/24/2014
mtps_version: v=office.15
ms.localizationpriority: medium
ms.openlocfilehash: 1404f1ebfc1196624a0bc8e9f8ddb661080781a3
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/24/2021
ms.locfileid: "59590743"
---
# <a name="enumerate-hidden-items-in-a-folder"></a>Énumération des éléments masqués d’un dossier

Cet exemple montre comment trouver et énumérer les éléments masqués d’un dossier.

## <a name="example"></a>Exemple

> [!NOTE] 
> L’exemple de code suivant est un extrait de [programmation d’Applications pour Microsoft Office Outlook 2007](https://www.amazon.com/gp/product/0735622493?ie=UTF8&tag=msmsdn-20&linkCode=as2&camp=1789&creative=9325&creativeASIN=0735622493).

L’objet [Table](https://msdn.microsoft.com/library/bb652856\(v=office.15\)), qui représente un ensemble d’éléments d’un dossier, peut contenir des éléments masqués. Pour renvoyer les éléments masqués d’un dossier, définissez le paramètre *TableContents* de la méthode [GetTable(Object, Object)](https://msdn.microsoft.com/library/bb612592\(v=office.15\)) de l’objet [MAPIFolder](https://msdn.microsoft.com/library/bb624369\(v=office.15\)) sur [olHiddenItems](https://msdn.microsoft.com/library/bb622801\(v=office.15\)). Dans l’exemple de code suivant, TableForInboxHiddenItems obtient les éléments masqués d’un dossier Boîte de réception, et écrit les valeurs des propriétés [Subject](https://msdn.microsoft.com/library/bb611353\(v=office.15\)) et [MessageClass](https://msdn.microsoft.com/library/bb645845\(v=office.15\)) pour chaque élément masqué sur les écouteurs de suivi de la collection [Listeners](https://msdn.microsoft.com/library/system.diagnostics.debug.listeners.aspx).

Si vous utilisez Visual Studio pour tester cet exemple de code, vous devez d’abord ajouter une référence au composant Bibliothèque d’objets Microsoft Outlook 15.0 et spécifier la variable lorsque vous importez l’espace de noms **Microsoft.Office.Interop.Outlook**. L’instruction **using** ne doit pas se produire juste avant les fonctions de l’exemple de code, mais doit être ajoutée avant la déclaration publique. Le code suivant illustre l’importation et l’affectation dans C\#.

```csharp
using Outlook = Microsoft.Office.Interop.Outlook;
```


```csharp
private void TableForInboxHiddenItems()
{
    // Inbox
    Outlook.Folder folder =
        Application.Session.GetDefaultFolder(
        Outlook.OlDefaultFolders.olFolderInbox)
        as Outlook.Folder;
    // Call GetTable with OlTableContents.olHiddenItems
    Outlook.Table table =
        folder.GetTable("",
        Outlook.OlTableContents.olHiddenItems);
    while (!table.EndOfTable)
    {
        Outlook.Row nextRow = table.GetNextRow();
        // Test for null subject
        if (nextRow["Subject"] == null)
        {
            Debug.WriteLine(nextRow["MessageClass"]);
        }
        else
        {
            Debug.WriteLine(nextRow["Subject"] + " "
                + nextRow["MessageClass"]);
        }
    }
}
```

## <a name="see-also"></a>Voir aussi

-[Recherche et filtrage](search-and-filter.md)

