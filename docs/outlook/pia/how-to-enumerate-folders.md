---
title: Énumération des dossiers
TOCTitle: Enumerate folders
ms:assetid: 564730f9-3da3-4eff-b207-64ac4fec632d
ms:mtpsurl: https://msdn.microsoft.com/library/Ff184607(v=office.15)
ms:contentKeyID: 55119855
ms.date: 07/24/2014
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: 0fe79f78ba1aab1e54df0b0bc88fa0c55c73e187
ms.sourcegitcommit: d6695c94415fa47952ee7961a69660abc0904434
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/17/2019
ms.locfileid: "28710250"
---
# <a name="enumerate-folders"></a>Énumération des dossiers

Cet exemple montre comment énumérer les dossiers par itération dans une collection de dossiers.

## <a name="example"></a>Exemple

> [!NOTE] 
> L’exemple de code suivant est un extrait de [programmation d’Applications pour Microsoft Office Outlook 2007](https://www.amazon.com/gp/product/0735622493?ie=UTF8&tag=msmsdn-20&linkCode=as2&camp=1789&creative=9325&creativeASIN=0735622493).

Dans l’exemple de code suivant, la méthode EnumerateFoldersInDefaultStore obtient d’abord le dossier racine de la banque par défaut à l’aide de la méthode [GetRootFolder()](https://msdn.microsoft.com/library/bb645807\(v=office.15\)). Il appelle ensuite la méthode EnumerateFolders dans le dossier racine. EnumerateFolders prend un dossier racine et parcourt les dossiers de la banque par défaut représentée par le dossier racine. EnumerateFolders utilise d’abord la propriété [Folders](https://msdn.microsoft.com/library/bb646854\(v=office.15\)) pour obtenir les sous-dossiers de l’objet [Folder](https://msdn.microsoft.com/library/bb645774\(v=office.15\)) racine. La méthode EnumerateFolders est ensuite appelée de manière récursive pour énumérer tous les dossiers d’une hiérarchie. Pour finir, EnumerateFolders écrit la propriété [FolderPath](https://msdn.microsoft.com/library/bb647409\(v=office.15\)) de chaque **Folder** dans les écouteurs de suivi dans la collection [Listeners](https://msdn.microsoft.com/library/system.diagnostics.debug.listeners.aspx).

Si vous utilisez Visual Studio pour tester cet exemple de code, vous devez d’abord ajouter une référence au composant Bibliothèque d’objets Microsoft Outlook 15.0 et spécifier la variable lorsque vous importez l’espace de noms **Microsoft.Office.Interop.Outlook**. L'instruction **d’utilisation** ne doit pas se produire juste avant les fonctions de l'exemple de code, mais doit être ajoutée avant la déclaration publique. La ligne de code suivante montre comment effectuer l’importation et la tâche dans C\#.

```csharp
using Outlook = Microsoft.Office.Interop.Outlook;
```


```csharp
private void EnumerateFoldersInDefaultStore()
{
    Outlook.Folder root =
        Application.Session.
        DefaultStore.GetRootFolder() as Outlook.Folder;
    EnumerateFolders(root);
}

// Uses recursion to enumerate Outlook subfolders.
private void EnumerateFolders(Outlook.Folder folder)
{
    Outlook.Folders childFolders =
        folder.Folders;
    if (childFolders.Count > 0)
    {
        foreach (Outlook.Folder childFolder in childFolders)
        {
            // Write the folder path.
            Debug.WriteLine(childFolder.FolderPath);
            // Call EnumerateFolders using childFolder.
            EnumerateFolders(childFolder);
        }
    }
}               
```

## <a name="see-also"></a>Voir aussi

- [Dossiers](folders.md)

