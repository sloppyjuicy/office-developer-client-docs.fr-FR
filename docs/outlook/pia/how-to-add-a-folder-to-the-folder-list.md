---
title: Ajouter un dossier à la liste des dossiers
TOCTitle: Add a folder to the folder list
ms:assetid: f636a190-d966-4421-9977-0ead2bff5eee
ms:mtpsurl: https://msdn.microsoft.com/library/Ff184655(v=office.15)
ms:contentKeyID: 55119850
ms.date: 07/24/2014
mtps_version: v=office.15
ms.openlocfilehash: dc8ead207261cfd4835e230981d923211771de7b
ms.sourcegitcommit: ef717c65d8dd41ababffb01eafc443c79950aed4
ms.translationtype: HT
ms.contentlocale: fr-FR
ms.lasthandoff: 10/04/2018
ms.locfileid: "25405524"
---
# <a name="add-a-folder-to-the-folder-list"></a><span data-ttu-id="b85fe-102">Ajouter un dossier à la liste des dossiers</span><span class="sxs-lookup"><span data-stu-id="b85fe-102">Add a folder to the folder list</span></span>

<span data-ttu-id="b85fe-103">Cet exemple montre comment utiliser la méthode [Add(String, Object)](https://msdn.microsoft.com/library/bb645065\(v=office.15\)) pour ajouter un dossier à la liste des dossiers Outlook.</span><span class="sxs-lookup"><span data-stu-id="b85fe-103">This example shows how to use the [Add(String, Object)](https://msdn.microsoft.com/library/bb645065\(v=office.15\)) method to add a folder to the Outlook folder list.</span></span>

## <a name="example"></a><span data-ttu-id="b85fe-104">Exemple</span><span class="sxs-lookup"><span data-stu-id="b85fe-104">Example</span></span>

> [!NOTE] 
> <span data-ttu-id="b85fe-105">L’exemple de code suivant est un extrait de [programmation d’Applications pour Microsoft Office Outlook 2007](https://www.amazon.com/gp/product/0735622493?ie=UTF8&tag=msmsdn-20&linkCode=as2&camp=1789&creative=9325&creativeASIN=0735622493).</span><span class="sxs-lookup"><span data-stu-id="b85fe-105">The following code example is an excerpt from  [Programming Applications for Microsoft Office Outlook 2007](https://www.amazon.com/gp/product/0735622493?ie=UTF8&tag=msmsdn-20&linkCode=as2&camp=1789&creative=9325&creativeASIN=0735622493)  , from Microsoft Press (ISBN 9780735622494, copyright Microsoft Press 2007, all rights reserved).</span></span>


<span data-ttu-id="b85fe-106">Dans l’exemple de code suivant, **AddMyNewFolder** appelle la méthode **Add** de la collection [Folders](https://msdn.microsoft.com/library/bb612071\(v=office.15\)) pour ajouter un objet [Folder](https://msdn.microsoft.com/library/bb645774\(v=office.15\)) qui représente un dossier appelé « My New Folder » à la **Boîte de réception** dans la liste des dossiers d’Outlook.</span><span class="sxs-lookup"><span data-stu-id="b85fe-106">In the following code example,  \*\*\*\* calls the **Add** method of the [Folders](https://msdn.microsoft.com/library/bb612071\(v=office.15\)) collection to add a [Folder](https://msdn.microsoft.com/library/bb645774\(v=office.15\)) object that represents a folder called "My New Folder" to the **Inbox** in the Outlook folder list.</span></span> <span data-ttu-id="b85fe-107">« My New Folder » est ensuite affiché.</span><span class="sxs-lookup"><span data-stu-id="b85fe-107">"My New Folder" is then displayed.</span></span>

<span data-ttu-id="b85fe-108">Si vous utilisez Visual Studio pour tester cet exemple de code, vous devez d’abord ajouter une référence au composant Bibliothèque d’objets Microsoft Outlook 15.0 et spécifier la variable lorsque vous importez l’espace de noms **Microsoft.Office.Interop.Outlook**.</span><span class="sxs-lookup"><span data-stu-id="b85fe-108">If you use Visual Studio to test this code example, you must first add a reference to the Microsoft Outlook 15.0 Object Library component and specify the   variable when you import the Microsoft.Office.Interop.Outlook namespace.</span></span> <span data-ttu-id="b85fe-109">L'instruction **d’utilisation** ne doit pas se produire juste avant les fonctions de l'exemple de code, mais doit être ajoutée avant la déclaration publique.</span><span class="sxs-lookup"><span data-stu-id="b85fe-109">The using statement must not occur directly before the functions in the code example but must be added before the public   declaration.</span></span> <span data-ttu-id="b85fe-110">La ligne de code suivante montre comment effectuer l’importation et la tâche dans C\#.</span><span class="sxs-lookup"><span data-stu-id="b85fe-110">The following line of code shows how to do the import and assignment in C#.</span></span>

```csharp
using Outlook = Microsoft.Office.Interop.Outlook;
```


```csharp
private void AddMyNewFolder()
{
    Outlook.Folder folder =
        Application.Session.GetDefaultFolder(
        Outlook.OlDefaultFolders.olFolderInbox)
        as Outlook.Folder;
    Outlook.Folders folders = folder.Folders;
    try
    {
        Outlook.Folder newFolder = folders.Add(
            "My New Folder", Type.Missing)
            as Outlook.Folder;
        newFolder.Display();
    }
    catch
    {
        MessageBox.Show(
            "Could not add 'My New Folder'",
            "Add Folder",
            MessageBoxButtons.OK,
            MessageBoxIcon.Error);
    }
}
```

## <a name="see-also"></a><span data-ttu-id="b85fe-111">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="b85fe-111">See also</span></span>

- [<span data-ttu-id="b85fe-112">Dossiers</span><span class="sxs-lookup"><span data-stu-id="b85fe-112">Folders</span></span>](folders.md)

