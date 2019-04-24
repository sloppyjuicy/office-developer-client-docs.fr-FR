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
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32357399"
---
# <a name="enumerate-folders"></a><span data-ttu-id="41c8b-102">Énumération des dossiers</span><span class="sxs-lookup"><span data-stu-id="41c8b-102">Enumerate folders</span></span>

<span data-ttu-id="41c8b-103">Cet exemple montre comment énumérer les dossiers par itération dans une collection de dossiers.</span><span class="sxs-lookup"><span data-stu-id="41c8b-103">This example shows how to enumerate folders by iterating through a collection of folders.</span></span>

## <a name="example"></a><span data-ttu-id="41c8b-104">Exemple</span><span class="sxs-lookup"><span data-stu-id="41c8b-104">Example</span></span>

> [!NOTE] 
> <span data-ttu-id="41c8b-105">L’exemple de code suivant est un extrait de [programmation d’Applications pour Microsoft Office Outlook 2007](https://www.amazon.com/gp/product/0735622493?ie=UTF8&tag=msmsdn-20&linkCode=as2&camp=1789&creative=9325&creativeASIN=0735622493).</span><span class="sxs-lookup"><span data-stu-id="41c8b-105">The following code example is an excerpt from [Programming Applications for Microsoft Office Outlook 2007](https://www.amazon.com/gp/product/0735622493?ie=UTF8&tag=msmsdn-20&linkCode=as2&camp=1789&creative=9325&creativeASIN=0735622493).</span></span>

<span data-ttu-id="41c8b-106">Dans l’exemple de code suivant, la méthode EnumerateFoldersInDefaultStore obtient d’abord le dossier racine de la banque par défaut à l’aide de la méthode [GetRootFolder()](https://msdn.microsoft.com/library/bb645807\(v=office.15\)).</span><span class="sxs-lookup"><span data-stu-id="41c8b-106">In the following code example, the EnumerateFoldersInDefaultStore method first obtains the root folder for the default store by using the [GetRootFolder()](https://msdn.microsoft.com/library/bb645807\(v=office.15\)) method.</span></span> <span data-ttu-id="41c8b-107">Il appelle ensuite la méthode EnumerateFolders dans le dossier racine.</span><span class="sxs-lookup"><span data-stu-id="41c8b-107">It then calls the EnumerateFolders method on the root folder.</span></span> <span data-ttu-id="41c8b-108">EnumerateFolders prend un dossier racine et parcourt les dossiers de la banque par défaut représentée par le dossier racine.</span><span class="sxs-lookup"><span data-stu-id="41c8b-108">EnumerateFolders takes in a root folder and walks through the folders of the default store that the root folder represents.</span></span> <span data-ttu-id="41c8b-109">EnumerateFolders utilise d’abord la propriété [Folders](https://msdn.microsoft.com/library/bb646854\(v=office.15\)) pour obtenir les sous-dossiers de l’objet [Folder](https://msdn.microsoft.com/library/bb645774\(v=office.15\)) racine.</span><span class="sxs-lookup"><span data-stu-id="41c8b-109">EnumerateFolders first uses the [Folders](https://msdn.microsoft.com/library/bb646854\(v=office.15\)) property to obtain the subfolders of the root [Folder](https://msdn.microsoft.com/library/bb645774\(v=office.15\)) object.</span></span> <span data-ttu-id="41c8b-110">La méthode EnumerateFolders est ensuite appelée de manière récursive pour énumérer tous les dossiers d’une hiérarchie.</span><span class="sxs-lookup"><span data-stu-id="41c8b-110">EnumerateFolders is then called recursively to enumerate all the folders in a hierarchy.</span></span> <span data-ttu-id="41c8b-111">Pour finir, EnumerateFolders écrit la propriété [FolderPath](https://msdn.microsoft.com/library/bb647409\(v=office.15\)) de chaque **Folder** dans les écouteurs de suivi dans la collection [Listeners](https://msdn.microsoft.com/library/system.diagnostics.debug.listeners.aspx).</span><span class="sxs-lookup"><span data-stu-id="41c8b-111">Finally, EnumerateFolders writes the [FolderPath](https://msdn.microsoft.com/library/bb647409\(v=office.15\)) property of each **Folder** to the trace listeners in the [Listeners](https://msdn.microsoft.com/library/system.diagnostics.debug.listeners.aspx) collection.</span></span>

<span data-ttu-id="41c8b-112">Si vous utilisez Visual Studio pour tester cet exemple de code, vous devez d’abord ajouter une référence au composant Bibliothèque d’objets Microsoft Outlook 15.0 et spécifier la variable lorsque vous importez l’espace de noms **Microsoft.Office.Interop.Outlook**.</span><span class="sxs-lookup"><span data-stu-id="41c8b-112">If you use Visual Studio to test this code example, you must first add a reference to the Microsoft Outlook 15.0 Object Library component and specify the Outlook variable when you import the **Microsoft.Office.Interop.Outlook** namespace.</span></span> <span data-ttu-id="41c8b-113">L’instruction **using** ne doit pas se produire juste avant les fonctions de l’exemple de code, mais doit être ajoutée avant la déclaration publique.</span><span class="sxs-lookup"><span data-stu-id="41c8b-113">The **using** statement must not occur directly before the functions in the code example but must be added before the public Class declaration.</span></span> <span data-ttu-id="41c8b-114">Le code suivant illustre l’importation et l’affectation dans C\#.</span><span class="sxs-lookup"><span data-stu-id="41c8b-114">The following line of code shows how to do the import and assignment in C\#.</span></span>

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

## <a name="see-also"></a><span data-ttu-id="41c8b-115">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="41c8b-115">See also</span></span>

- [<span data-ttu-id="41c8b-116">Dossiers</span><span class="sxs-lookup"><span data-stu-id="41c8b-116">Folders</span></span>](folders.md)

