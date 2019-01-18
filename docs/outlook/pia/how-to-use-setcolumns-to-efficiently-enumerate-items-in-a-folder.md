---
title: Utilisation de SetColumns pour énumérer efficacement les éléments d’un dossier
TOCTitle: Use SetColumns to efficiently enumerate items in a folder
ms:assetid: cd7c7758-8a9c-4f1c-a49c-9305d75be341
ms:mtpsurl: https://msdn.microsoft.com/library/Ff184641(v=office.15)
ms:contentKeyID: 55119921
ms.date: 07/24/2014
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: bdfccc6432d35b6f39564e4c87404cc57b6ea27e
ms.sourcegitcommit: d6695c94415fa47952ee7961a69660abc0904434
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/17/2019
ms.locfileid: "28708087"
---
# <a name="use-setcolumns-to-efficiently-enumerate-items-in-a-folder"></a>Utilisation de SetColumns pour énumérer efficacement les éléments d’un dossier

Cet exemple montre comment améliorer les performances de l'énumération de la collection [Items](https://msdn.microsoft.com/library/bb645287\(v=office.15\)) à l'aide de la méthode [SetColumns(String)](https://msdn.microsoft.com/library/bb610268\(v=office.15\)) pour mettre en cache certaines propriétés de chaque élément de la collection.

## <a name="example"></a>Exemple

> [!NOTE] 
> L’exemple de code suivant est un extrait de [programmation d’Applications pour Microsoft Office Outlook 2007](https://www.amazon.com/gp/product/0735622493?ie=UTF8&tag=msmsdn-20&linkCode=as2&camp=1789&creative=9325&creativeASIN=0735622493).

Pour énumérer les éléments d'une collection, utilisez la méthode **SetColumns** pour mettre en cache des propriétés sur la collection **Items**. **SetColumns** prend un argument qui est une chaîne délimitée par des virgules, représentant des noms de propriétés. Une fois que tous les éléments d'une collection ont été énumérés, appelez la méthode [ResetColumns()](https://msdn.microsoft.com/library/bb624355\(v=office.15\)) pour effacer le cache de propriétés.

Dans l’exemple de code suivant, EnumerateContactsWithSetColumns utilise la méthode **SetColumns** pour mettre en cache les propriétés [FileAs](https://msdn.microsoft.com/library/bb647792\(v=office.15\)), [CompanyName](https://msdn.microsoft.com/library/bb610212\(v=office.15\)) et [JobTitle](https://msdn.microsoft.com/library/bb609294\(v=office.15\)) des éléments du dossier Contacts. Nous vous recommandons de tester les chaînes vides ou une référence nulle dans la restriction.

Notez qu’un dossier Outlook peut contenir des éléments de différents types. Cet exemple de code permet d’utiliser la classe d’assistance OutlookItem, définie dans l’article [Créer une classe d’assistance pour accéder aux membres d’un élément courant Outlook](how-to-create-a-helper-class-to-access-common-outlook-item-members.md), pour appeler facilement la propriété OutlookItem.Class et vérifier la classe de message de chaque élément du sous-ensemble d’éléments filtrés dans le dossier, avant d’assumer que l’élément est un contact.

Si vous utilisez Visual Studio pour tester cet exemple de code, vous devez d’abord ajouter une référence au composant Bibliothèque d’objets Microsoft Outlook 15.0 et spécifier la variable lorsque vous importez l’espace de noms **Microsoft.Office.Interop.Outlook**. L'instruction **d’utilisation** ne doit pas se produire juste avant les fonctions de l'exemple de code, mais doit être ajoutée avant la déclaration publique. La ligne de code suivante montre comment effectuer l’importation et la tâche dans C\#.

```csharp
using Outlook = Microsoft.Office.Interop.Outlook;
```


```csharp
private void EnumerateContactsWithSetColumns()
{
    // Obtain Contacts folder
    Outlook.Folder folder =
        Application.Session.GetDefaultFolder(
        Outlook.OlDefaultFolders.olFolderContacts)
        as Outlook.Folder;
    string filter = "Not([CompanyName] Is Null)" +
        " AND Not([JobTitle] Is Null)";
    Outlook.Items items = folder.Items.Restrict(filter);
    items.SetColumns("FileAs, CompanyName, JobTitle");
    for (int i = 1; i <= items.Count; i++)
    {
        // Create an instance of OutlookItem
        OutlookItem myItem = new OutlookItem(items[i]);
        if (myItem.Class == Outlook.OlObjectClass.olContact)
        {
            // Use InnerObject to return ContactItem
            Outlook.ContactItem contact =
                myItem.InnerObject as Outlook.ContactItem;
            StringBuilder sb = new StringBuilder();
            sb.AppendLine(contact.FileAs);
            sb.AppendLine(contact.CompanyName);
            sb.AppendLine(contact.JobTitle);
            sb.AppendLine();
            Debug.WriteLine(sb.ToString());
        }
    }
    items.ResetColumns();
}
```

## <a name="see-also"></a>Voir aussi

- [Rechercher et filtrer](search-and-filter.md)

