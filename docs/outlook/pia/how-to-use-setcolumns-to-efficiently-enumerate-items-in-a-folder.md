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
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32338037"
---
# <a name="use-setcolumns-to-efficiently-enumerate-items-in-a-folder"></a><span data-ttu-id="363a0-102">Utilisation de SetColumns pour énumérer efficacement les éléments d’un dossier</span><span class="sxs-lookup"><span data-stu-id="363a0-102">Use SetColumns to efficiently enumerate items in a folder</span></span>

<span data-ttu-id="363a0-103">Cet exemple montre comment améliorer les performances de l'énumération de la collection [Items](https://msdn.microsoft.com/library/bb645287\(v=office.15\)) à l'aide de la méthode [SetColumns(String)](https://msdn.microsoft.com/library/bb610268\(v=office.15\)) pour mettre en cache certaines propriétés de chaque élément de la collection.</span><span class="sxs-lookup"><span data-stu-id="363a0-103">This example shows how to improve the performance of enumerating the [Items](https://msdn.microsoft.com/library/bb645287\(v=office.15\)) collection by using the [SetColumns(String)](https://msdn.microsoft.com/library/bb610268\(v=office.15\)) method to cache certain properties of each item in the collection.</span></span>

## <a name="example"></a><span data-ttu-id="363a0-104">Exemple</span><span class="sxs-lookup"><span data-stu-id="363a0-104">Example</span></span>

> [!NOTE] 
> <span data-ttu-id="363a0-105">L’exemple de code suivant est un extrait de [programmation d’Applications pour Microsoft Office Outlook 2007](https://www.amazon.com/gp/product/0735622493?ie=UTF8&tag=msmsdn-20&linkCode=as2&camp=1789&creative=9325&creativeASIN=0735622493).</span><span class="sxs-lookup"><span data-stu-id="363a0-105">The following code example is an excerpt from [Programming Applications for Microsoft Office Outlook 2007](https://www.amazon.com/gp/product/0735622493?ie=UTF8&tag=msmsdn-20&linkCode=as2&camp=1789&creative=9325&creativeASIN=0735622493).</span></span>

<span data-ttu-id="363a0-p101">Pour énumérer les éléments d'une collection, utilisez la méthode **SetColumns** pour mettre en cache des propriétés sur la collection **Items**. **SetColumns** prend un argument qui est une chaîne délimitée par des virgules, représentant des noms de propriétés. Une fois que tous les éléments d'une collection ont été énumérés, appelez la méthode [ResetColumns()](https://msdn.microsoft.com/library/bb624355\(v=office.15\)) pour effacer le cache de propriétés.</span><span class="sxs-lookup"><span data-stu-id="363a0-p101">To enumerate items in a collection, use the **SetColumns** method to cache properties on the **Items** collection. **SetColumns** takes an argument that is a comma-delimited string that represents property names. Once all items in the collection have been enumerated, call the [ResetColumns()](https://msdn.microsoft.com/library/bb624355\(v=office.15\)) method to clear the property cache.</span></span>

<span data-ttu-id="363a0-109">Dans l’exemple de code suivant, EnumerateContactsWithSetColumns utilise la méthode **SetColumns** pour mettre en cache les propriétés [FileAs](https://msdn.microsoft.com/library/bb647792\(v=office.15\)), [CompanyName](https://msdn.microsoft.com/library/bb610212\(v=office.15\)) et [JobTitle](https://msdn.microsoft.com/library/bb609294\(v=office.15\)) des éléments du dossier Contacts.</span><span class="sxs-lookup"><span data-stu-id="363a0-109">In the following code example, EnumerateContactsWithSetColumns uses the **SetColumns** method to cache the [FileAs](https://msdn.microsoft.com/library/bb647792\(v=office.15\)), [CompanyName](https://msdn.microsoft.com/library/bb610212\(v=office.15\)), and [JobTitle](https://msdn.microsoft.com/library/bb609294\(v=office.15\)) properties of items in the Contacts folder.</span></span> <span data-ttu-id="363a0-110">Nous vous recommandons de tester les chaînes vides ou une référence nulle dans la restriction.</span><span class="sxs-lookup"><span data-stu-id="363a0-110">Note that you must test for empty strings or a null reference in the restriction.</span></span>

<span data-ttu-id="363a0-111">Notez qu’un dossier Outlook peut contenir des éléments de différents types.</span><span class="sxs-lookup"><span data-stu-id="363a0-111">Note that an Outlook folder can possibly contain items of different types.</span></span> <span data-ttu-id="363a0-112">Cet exemple de code permet d’utiliser la classe d’assistance OutlookItem, définie dans l’article [Créer une classe d’assistance pour accéder aux membres d’un élément courant Outlook](how-to-create-a-helper-class-to-access-common-outlook-item-members.md), pour appeler facilement la propriété OutlookItem.Class et vérifier la classe de message de chaque élément du sous-ensemble d’éléments filtrés dans le dossier, avant d’assumer que l’élément est un contact.</span><span class="sxs-lookup"><span data-stu-id="363a0-112">This code sample makes use of the OutlookItem helper class, defined in [Create a Helper Class to Access Common Outlook Item Members](how-to-create-a-helper-class-to-access-common-outlook-item-members.md), to conveniently call the OutlookItem.Class property to verify the message class of each item in the filtered subset of items in the folder, before assuming the item is a contact item.</span></span>

<span data-ttu-id="363a0-113">Si vous utilisez Visual Studio pour tester cet exemple de code, vous devez d’abord ajouter une référence au composant Bibliothèque d’objets Microsoft Outlook 15.0 et spécifier la variable lorsque vous importez l’espace de noms **Microsoft.Office.Interop.Outlook**.</span><span class="sxs-lookup"><span data-stu-id="363a0-113">If you use Visual Studio to test this code example, you must first add a reference to the Microsoft Outlook 15.0 Object Library component and specify the Outlook variable when you import the **Microsoft.Office.Interop.Outlook** namespace.</span></span> <span data-ttu-id="363a0-114">L’instruction **using** ne doit pas se produire juste avant les fonctions de l’exemple de code, mais doit être ajoutée avant la déclaration publique.</span><span class="sxs-lookup"><span data-stu-id="363a0-114">The **using** statement must not occur directly before the functions in the code example but must be added before the public Class declaration.</span></span> <span data-ttu-id="363a0-115">Le code suivant illustre l’importation et l’affectation dans C\#.</span><span class="sxs-lookup"><span data-stu-id="363a0-115">The following line of code shows how to do the import and assignment in C\#.</span></span>

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

## <a name="see-also"></a><span data-ttu-id="363a0-116">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="363a0-116">See also</span></span>

- [<span data-ttu-id="363a0-117">Rechercher et filtrer</span><span class="sxs-lookup"><span data-stu-id="363a0-117">Search and filter</span></span>](search-and-filter.md)

