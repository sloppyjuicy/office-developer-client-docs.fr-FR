---
title: Utilisation des tableaux pour énumérer efficacement les éléments d’un dossier
TOCTitle: Use arrays to efficiently enumerate items in a folder
ms:assetid: 05a73225-ad0d-4d52-90b6-448d220348df
ms:mtpsurl: https://msdn.microsoft.com/library/Ff184588(v=office.15)
ms:contentKeyID: 55119885
ms.date: 07/24/2014
mtps_version: v=office.15
ms.localizationpriority: medium
ms.openlocfilehash: dbe2852de11c34401e1653d8e2b0b25d36e19b37
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/24/2021
ms.locfileid: "59560465"
---
# <a name="use-arrays-to-efficiently-enumerate-items-in-a-folder"></a>Utilisation des tableaux pour énumérer efficacement les éléments d’un dossier

Cet exemple montre comment énumérer efficacement les éléments dans un objet [Folder](https://msdn.microsoft.com/library/bb645774\(v=office.15\)) à l’aide de la méthode [GetArray(Int32)](https://msdn.microsoft.com/library/bb608928\(v=office.15\)).

## <a name="example"></a>Exemple

> [!NOTE] 
> L’exemple de code suivant est un extrait de [programmation d’Applications pour Microsoft Office Outlook 2007](https://www.amazon.com/gp/product/0735622493?ie=UTF8&tag=msmsdn-20&linkCode=as2&camp=1789&creative=9325&creativeASIN=0735622493).

Dans l’exemple de code suivant, DemoGetArrayForTable obtient un objet [Table](https://msdn.microsoft.com/library/bb652856\(v=office.15\)) d’un objet **Folder** à l’aide de la méthode [GetTable(Object, Object)](https://msdn.microsoft.com/library/bb612592\(v=office.15\)). DemoGetArrayForTable utilise ensuite la méthode **GetArray** pour renvoyer un objet [Array](https://msdn.microsoft.com/library/system.array.aspx) qui contient des éléments pour chaque ligne du tableau. L’objet **Array** renvoyé est un tableau à deux dimensions qui représente un ensemble de valeurs de ligne et de colonne issues de l’objet **Table**. Il s’agit d’un tableau de base zéro, et non de base un comme c’est le cas des collections Outlook. Une fois que l’objet **Array** est obtenu, le code utilise une boucle for pour énumérer le contenu du tableau.

Si vous utilisez Visual Studio pour tester cet exemple de code, vous devez d’abord ajouter une référence au composant Bibliothèque d’objets Microsoft Outlook 15.0 et spécifier la variable lorsque vous importez l’espace de noms **Microsoft.Office.Interop.Outlook**. L’instruction **using** ne doit pas se produire juste avant les fonctions de l’exemple de code, mais doit être ajoutée avant la déclaration publique. Le code suivant illustre l’importation et l’affectation dans C\#.

```csharp
using Outlook = Microsoft.Office.Interop.Outlook;
```


```csharp
private void DemoGetArrayForTable()
{
    // Obtain Inbox
    Outlook.Folder folder =
        Application.Session.GetDefaultFolder(
        Outlook.OlDefaultFolders.olFolderInbox)
        as Outlook.Folder;
    Outlook.Table table =
        folder.GetTable("", Outlook.OlTableContents.olUserItems);
    Array tableArray = table.GetArray(table.GetRowCount()) as Array;
    for (int i = 0; i <= tableArray.GetUpperBound(0); i++)
    {
        for (int j = 0; j <= tableArray.GetUpperBound(1); j++)
        {
            Debug.WriteLine(tableArray.GetValue(i, j));
        }
    }
}
```

## <a name="see-also"></a>Voir aussi

- [Rechercher et filtrer](search-and-filter.md)

