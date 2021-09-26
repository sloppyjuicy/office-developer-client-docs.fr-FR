---
title: Énumération des éléments de la Boîte de réception selon l’heure de la dernière modification
TOCTitle: Enumerate items in the Inbox based on the last modification time
ms:assetid: 93a25143-def6-4832-bac2-3744558c2736
ms:mtpsurl: https://msdn.microsoft.com/library/Ff184626(v=office.15)
ms:contentKeyID: 55119920
ms.date: 07/24/2014
mtps_version: v=office.15
ms.localizationpriority: medium
ms.openlocfilehash: 2c6ce9d6c7321853aaed2cb5cbca737438fef27f
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/24/2021
ms.locfileid: "59629339"
---
# <a name="enumerate-items-in-the-inbox-based-on-the-last-modification-time"></a>Énumération des éléments de la Boîte de réception selon l’heure de la dernière modification

Cet exemple montre comment énumérer les éléments du dossier Boîte de réception selon l’heure de la dernière modification.

## <a name="example"></a>Exemple

> [!NOTE] 
> L’exemple de code suivant est un extrait de [programmation d’Applications pour Microsoft Office Outlook 2007](https://www.amazon.com/gp/product/0735622493?ie=UTF8&tag=msmsdn-20&linkCode=as2&camp=1789&creative=9325&creativeASIN=0735622493).

L’objet [Table](https://msdn.microsoft.com/library/bb652856\(v=office.15\)) représente un ensemble d’éléments d’un objet [Folder](https://msdn.microsoft.com/library/bb645774\(v=office.15\)) ou [Search](https://msdn.microsoft.com/library/bb612611\(v=office.15\)). Pour obtenir un objet **Table**, appelez la méthode [GetTable (Object, Object)](https://msdn.microsoft.com/library/bb612592\(v=office.15\)) sur un objet **Folder** ou **Search**. Chaque élément de l’élément **Table** renvoyé contient seulement un sous-ensemble par défaut des propriétés de l’élément. Chaque objet [Row](https://msdn.microsoft.com/library/bb610126\(v=office.15\)) peut être considéré comme un élément du dossier et chaque objet [Column](https://msdn.microsoft.com/library/bb609646\(v=office.15\)), comme une propriété d’un élément. La suppression, l'ajout et la modification de lignes ne sont pas prises en charge dans l'objet **Table**. Pour énumérer des éléments dans un objet **Table**, utilisez d'abord la propriété [EndOfTable](https://msdn.microsoft.com/library/bb647715\(v=office.15\)) pour voir si votre position actuelle est la fin du tableau. Si **EndOfTable** retourne **false**, utilisez la méthode [GetNextRow()](https://msdn.microsoft.com/library/bb609740\(v=office.15\)) pour retourner un objet **Row**, qui contient un nombre par défaut d'objets **Column**. Pour poursuivre l’itération directement dans l’objet **Table**, appelez la méthode **GetNextRow** jusqu’à ce que la propriété **EndOfTable** renvoie **true**.

Dans l’exemple de code suivant, DemoTableForInbox obtient un objet **Table** pour le dossier Boîte de réception, trie l’objet **Table** à l’aide de la propriété **LastModificationTime** et de la méthode [Sort(String, Object)](https://msdn.microsoft.com/library/bb652667\(v=office.15\)), et procède à l’itération dans le tableau pour écrire l’objet de chaque élément dans les écouteurs de suivi de la collection [Listeners](https://msdn.microsoft.com/library/system.diagnostics.debug.listeners.aspx).

Si vous utilisez Visual Studio pour tester cet exemple de code, vous devez d’abord ajouter une référence au composant Bibliothèque d’objets Microsoft Outlook 15.0 et spécifier la variable lorsque vous importez l’espace de noms **Microsoft.Office.Interop.Outlook**. L’instruction **using** ne doit pas se produire juste avant les fonctions de l’exemple de code, mais doit être ajoutée avant la déclaration publique. Le code suivant illustre l’importation et l’affectation dans C\#.

```csharp
using Outlook = Microsoft.Office.Interop.Outlook;
```


```csharp
private void DemoTableForInbox()
{
    //Obtain Inbox
    Outlook.Folder folder =
        Application.Session.GetDefaultFolder(
        Outlook.OlDefaultFolders.olFolderInbox)
        as Outlook.Folder;
    //Obtain Table using defaults
    Outlook.Table table =
        folder.GetTable(Type.Missing, Type.Missing);
    table.Sort("LastModificationTime",
        Outlook.OlSortOrder.olDescending);
    while (!table.EndOfTable)
    {
        Outlook.Row nextRow = table.GetNextRow();
        Debug.WriteLine(nextRow["Subject"]);
    }
}
```

## <a name="see-also"></a>Voir aussi

- [Rechercher et filtrer](search-and-filter.md)

