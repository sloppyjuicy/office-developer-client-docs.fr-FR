---
title: Énumération des dossiers
TOCTitle: Enumerate folders
ms:assetid: 564730f9-3da3-4eff-b207-64ac4fec632d
ms:mtpsurl: https://msdn.microsoft.com/library/Ff184607(v=office.15)
ms:contentKeyID: 55119855
ms.date: 07/24/2014
mtps_version: v=office.15
ms.openlocfilehash: 91165754ccd86ebff07ec99e60f0ad1a167dea05
ms.sourcegitcommit: ef717c65d8dd41ababffb01eafc443c79950aed4
ms.translationtype: HT
ms.contentlocale: fr-FR
ms.lasthandoff: 10/04/2018
ms.locfileid: "25406252"
---
# <a name="enumerate-folders"></a><span data-ttu-id="c2135-102">Énumération des dossiers</span><span class="sxs-lookup"><span data-stu-id="c2135-102">Enumerate folders</span></span>

<span data-ttu-id="c2135-103">Cet exemple montre comment énumérer les dossiers par itération dans une collection de dossiers.</span><span class="sxs-lookup"><span data-stu-id="c2135-103">This example shows how to enumerate folders by iterating through a collection of folders.</span></span>

## <a name="example"></a><span data-ttu-id="c2135-104">Exemple</span><span class="sxs-lookup"><span data-stu-id="c2135-104">Example</span></span>

> [!NOTE] 
> <span data-ttu-id="c2135-105">L’exemple de code suivant est un extrait de [programmation d’Applications pour Microsoft Office Outlook 2007](https://www.amazon.com/gp/product/0735622493?ie=UTF8&tag=msmsdn-20&linkCode=as2&camp=1789&creative=9325&creativeASIN=0735622493).</span><span class="sxs-lookup"><span data-stu-id="c2135-105">The following code example is an excerpt from  [Programming Applications for Microsoft Office Outlook 2007](https://www.amazon.com/gp/product/0735622493?ie=UTF8&tag=msmsdn-20&linkCode=as2&camp=1789&creative=9325&creativeASIN=0735622493)  , from Microsoft Press (ISBN 9780735622494, copyright Microsoft Press 2007, all rights reserved).</span></span>

<span data-ttu-id="c2135-106">Dans l’exemple de code suivant, la méthode EnumerateFoldersInDefaultStore obtient d’abord le dossier racine de la banque par défaut à l’aide de la méthode [GetRootFolder()](https://msdn.microsoft.com/library/bb645807\(v=office.15\)).</span><span class="sxs-lookup"><span data-stu-id="c2135-106">In the following code example, the   method first obtains the root folder for the default store by using the GetRootFolder() method.</span></span> <span data-ttu-id="c2135-107">Il appelle ensuite la méthode EnumerateFolders dans le dossier racine.</span><span class="sxs-lookup"><span data-stu-id="c2135-107">It then calls the   method on the root folder.</span></span> <span data-ttu-id="c2135-108">EnumerateFolders prend un dossier racine et parcourt les dossiers de la banque par défaut représentée par le dossier racine.</span><span class="sxs-lookup"><span data-stu-id="c2135-108"> takes in a root folder and walks through the folders of the default store that the root folder represents.</span></span> <span data-ttu-id="c2135-109">EnumerateFolders utilise d’abord la propriété [Folders](https://msdn.microsoft.com/library/bb646854\(v=office.15\)) pour obtenir les sous-dossiers de l’objet [Folder](https://msdn.microsoft.com/library/bb645774\(v=office.15\)) racine.</span><span class="sxs-lookup"><span data-stu-id="c2135-109"> first uses the Folders property to obtain the subfolders of the root Folder object.</span></span> <span data-ttu-id="c2135-110">La méthode EnumerateFolders est ensuite appelée de manière récursive pour énumérer tous les dossiers d’une hiérarchie.</span><span class="sxs-lookup"><span data-stu-id="c2135-110"> is then called recursively to enumerate all the folders in a hierarchy.</span></span> <span data-ttu-id="c2135-111">Pour finir, EnumerateFolders écrit la propriété [FolderPath](https://msdn.microsoft.com/library/bb647409\(v=office.15\)) de chaque **Folder** dans les écouteurs de suivi dans la collection [Listeners](https://msdn.microsoft.com/library/system.diagnostics.debug.listeners.aspx).</span><span class="sxs-lookup"><span data-stu-id="c2135-111">Finally,   writes the FolderPath property of each Folder to the trace listeners in the Listeners collection.</span></span>

<span data-ttu-id="c2135-112">Si vous utilisez Visual Studio pour tester cet exemple de code, vous devez d’abord ajouter une référence au composant Bibliothèque d’objets Microsoft Outlook 15.0 et spécifier la variable lorsque vous importez l’espace de noms **Microsoft.Office.Interop.Outlook**.</span><span class="sxs-lookup"><span data-stu-id="c2135-112">If you use Visual Studio to test this code example, you must first add a reference to the Microsoft Outlook 15.0 Object Library component and specify the   variable when you import the Microsoft.Office.Interop.Outlook namespace.</span></span> <span data-ttu-id="c2135-113">L'instruction **d’utilisation** ne doit pas se produire juste avant les fonctions de l'exemple de code, mais doit être ajoutée avant la déclaration publique.</span><span class="sxs-lookup"><span data-stu-id="c2135-113">The using statement must not occur directly before the functions in the code example but must be added before the public   declaration.</span></span> <span data-ttu-id="c2135-114">La ligne de code suivante montre comment effectuer l’importation et la tâche dans C\#.</span><span class="sxs-lookup"><span data-stu-id="c2135-114">The following line of code shows how to do the import and assignment in C#.</span></span>

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

## <a name="see-also"></a><span data-ttu-id="c2135-115">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="c2135-115">See also</span></span>

- [<span data-ttu-id="c2135-116">Dossiers</span><span class="sxs-lookup"><span data-stu-id="c2135-116">Folders</span></span>](folders.md)

