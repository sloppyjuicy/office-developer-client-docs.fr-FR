---
title: Obtention d’un dossier par défaut et énumération de ses sous-dossiers
TOCTitle: Get a default folder and enumerate its subfolders
ms:assetid: 587e8392-cb03-442c-9058-1282f36dabdb
ms:mtpsurl: https://msdn.microsoft.com/library/Ff184610(v=office.15)
ms:contentKeyID: 55119857
ms.date: 07/24/2014
mtps_version: v=office.15
ms.localizationpriority: medium
ms.openlocfilehash: 8a42e0c330aeb02f203bd1fde287e6a76cfd9c44
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/24/2021
ms.locfileid: "59609046"
---
# <a name="get-a-default-folder-and-enumerate-its-subfolders"></a>Obtention d’un dossier par défaut et énumération de ses sous-dossiers

Cet exemple montre comment obtenir un dossier par défaut dans la banque d’informations de l’utilisateur par défaut et comment énumérer ses sous-dossiers.

## <a name="example"></a>Exemple

> [!NOTE] 
> L’exemple de code suivant est un extrait de [programmation d’Applications pour Microsoft Office Outlook 2007](https://www.amazon.com/gp/product/0735622493?ie=UTF8&tag=msmsdn-20&linkCode=as2&camp=1789&creative=9325&creativeASIN=0735622493).

Dans l’exemple de code suivant, GetRSSFeeds utilise la méthode [GetDefaultFolder(OlDefaultFolders)](https://msdn.microsoft.com/library/bb646473\(v=office.15\)) de l’objet [NameSpace](https://msdn.microsoft.com/library/bb645857\(v=office.15\)) pour obtenir le dossier racine RSS Feeds de l’utilisateur. GetRSSFeeds affiche ensuite une zone de message qui contient les noms des dossiers pour tous les flux RSS du dossier RSS Feeds.

Si vous utilisez Visual Studio pour tester cet exemple de code, vous devez d’abord ajouter une référence au composant Bibliothèque d’objets Microsoft Outlook 15.0 et spécifier la variable lorsque vous importez l’espace de noms **Microsoft.Office.Interop.Outlook**. L’instruction **using** ne doit pas se produire juste avant les fonctions de l’exemple de code, mais doit être ajoutée avant la déclaration publique. Le code suivant illustre l’importation et l’affectation dans C\#.

```csharp
using Outlook = Microsoft.Office.Interop.Outlook;
```


```csharp
private void GetRSSFeeds()
{
    Outlook.Folder folder =
        Application.Session.GetDefaultFolder(
        Outlook.OlDefaultFolders.olFolderRssFeeds)
        as Outlook.Folder;
    if (folder != null)
    {
        if (folder.Folders.Count > 0)
        {
            StringBuilder sb = new StringBuilder();
            foreach (Outlook.Folder subfolder
                in folder.Folders)
            {
                sb.AppendLine(subfolder.Name);
            }
            MessageBox.Show(sb.ToString(),
                "RSS Feeds",
                MessageBoxButtons.OK,
                MessageBoxIcon.Information);
        }
    }
}
```

## <a name="see-also"></a>Voir aussi

- [Dossiers](folders.md)

