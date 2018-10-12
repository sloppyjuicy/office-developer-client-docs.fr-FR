---
title: Obtenir un dossier à partir de son chemin d’accès
TOCTitle: Get a folder based on its folder path
ms:assetid: 613f2209-667c-48f0-82cf-86e3c9a24cb4
ms:mtpsurl: https://msdn.microsoft.com/library/Ff184612(v=office.15)
ms:contentKeyID: 55119858
ms.date: 07/24/2014
mtps_version: v=office.15
ms.openlocfilehash: b418cda3f689182cb7133af22e0f2fdc6ba834c2
ms.sourcegitcommit: ef717c65d8dd41ababffb01eafc443c79950aed4
ms.translationtype: HT
ms.contentlocale: fr-FR
ms.lasthandoff: 10/04/2018
ms.locfileid: "25407141"
---
# <a name="get-a-folder-based-on-its-folder-path"></a>Obtenir un dossier à partir de son chemin d’accès

Cet exemple illustre un chemin d’accès à un dossier et obtient le dossier associé.

## <a name="example"></a>Exemple

> [!NOTE] 
> L’exemple de code suivant est un extrait de [programmation d’Applications pour Microsoft Office Outlook 2007](https://www.amazon.com/gp/product/0735622493?ie=UTF8&tag=msmsdn-20&linkCode=as2&camp=1789&creative=9325&creativeASIN=0735622493).

Dans l’exemple de code suivant, la méthode GetKeyContacts utilise la propriété [GetRootFolder()](https://msdn.microsoft.com/library/bb645807\(v=office.15\)) pour obtenir le chemin d’accès du dossier Contacts\\Key Contacts. La méthode GetFolder est ensuite appelée en utilisant la propriété [FolderPath](https://msdn.microsoft.com/library/bb647409\(v=office.15\)) comme argument. Si GetFolder renvoie un dossier, un message s’affiche indiquant que le dossier Key Contacts a été trouvé. La méthode GetFolder prend un chemin d’accès à un dossier et renvoie l’objet [Folder](https://msdn.microsoft.com/library/bb645774\(v=office.15\)) correct. Pour ce faire, la propriété **FolderPath** est tout d'abord divisée en tableau de type string, puis ce tableau est utilisé pour trouver l'objet **Folder** correct en commençant par le haut de la propriété **FolderPath**. Si le dossier spécifié est introuvable, GetFolder renvoie une référence NULL.

Si vous utilisez Visual Studio pour tester cet exemple de code, vous devez d’abord ajouter une référence au composant Bibliothèque d’objets Microsoft Outlook 15.0 et spécifier la variable lorsque vous importez l’espace de noms **Microsoft.Office.Interop.Outlook**. L'instruction **d’utilisation** ne doit pas se produire juste avant les fonctions de l'exemple de code, mais doit être ajoutée avant la déclaration publique. La ligne de code suivante montre comment effectuer l’importation et la tâche dans C\#.

```csharp
using Outlook = Microsoft.Office.Interop.Outlook;
```


```csharp
private void GetKeyContacts()
{
    string folderPath =
        Application.Session.
        DefaultStore.GetRootFolder().FolderPath
        + @"\Contacts\Key Contacts";
    Outlook.Folder folder = GetFolder(folderPath);
    if (folder != null)
    {
        //Work with folder here
        Debug.WriteLine("Found Key Contacts");
    }
}

// Returns Folder object based on folder path
private Outlook.Folder GetFolder(string folderPath)
{
    Outlook.Folder folder;
    string backslash = @"\";
    try
    {
        if (folderPath.StartsWith(@"\\"))
        {
            folderPath = folderPath.Remove(0, 2);
        }
        String[] folders =
            folderPath.Split(backslash.ToCharArray());
        folder =
            Application.Session.Folders[folders[0]]
            as Outlook.Folder;
        if (folder != null)
        {
            for (int i = 1; i <= folders.GetUpperBound(0); i++)
            {
                Outlook.Folders subFolders = folder.Folders;
                folder = subFolders[folders[i]]
                    as Outlook.Folder;
                if (folder == null)
                {
                    return null;
                }
            }
        }
        return folder;
    }
    catch { return null; }
}        
```

## <a name="see-also"></a>Voir aussi

- [Dossiers](folders.md)

