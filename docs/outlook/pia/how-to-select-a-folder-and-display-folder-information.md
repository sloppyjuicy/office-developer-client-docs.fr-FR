---
title: Sélection d’un dossier et affichage de ses informations
TOCTitle: Select a folder and display folder information
ms:assetid: 737b19bc-1efd-4ddb-86d0-72b3ab8eaf8c
ms:mtpsurl: https://msdn.microsoft.com/library/Ff184616(v=office.15)
ms:contentKeyID: 55119859
ms.date: 07/24/2014
mtps_version: v=office.15
ms.openlocfilehash: 17131ba769b5f8d1719011474dc2c06bf1084ca3
ms.sourcegitcommit: ef717c65d8dd41ababffb01eafc443c79950aed4
ms.translationtype: HT
ms.contentlocale: fr-FR
ms.lasthandoff: 10/04/2018
ms.locfileid: "25406476"
---
# <a name="select-a-folder-and-display-folder-information"></a><span data-ttu-id="dac37-102">Sélection d’un dossier et affichage de ses informations</span><span class="sxs-lookup"><span data-stu-id="dac37-102">Select a folder and display folder information</span></span>

<span data-ttu-id="dac37-103">Cet exemple montre comment afficher par programme les informations sur un dossier qu’un utilisateur sélectionne dans une liste des dossiers spécifiée.</span><span class="sxs-lookup"><span data-stu-id="dac37-103">This example shows how to programmatically display information about a folder that a user selects from a specified folder list.</span></span>

## <a name="example"></a><span data-ttu-id="dac37-104">Exemple</span><span class="sxs-lookup"><span data-stu-id="dac37-104">Example</span></span>

> [!NOTE] 
> <span data-ttu-id="dac37-105">L’exemple de code suivant est un extrait de la [programmation d’Applications pour Microsoft Office Outlook 2007](https://www.amazon.com/gp/product/0735622493?ie=UTF8&tag=msmsdn-20&linkCode=as2&camp=1789&creative=9325&creativeASIN=0735622493).</span><span class="sxs-lookup"><span data-stu-id="dac37-105">The following code example is an excerpt from  [Programming Applications for Microsoft Office Outlook 2007](https://www.amazon.com/gp/product/0735622493?ie=UTF8&tag=msmsdn-20&linkCode=as2&camp=1789&creative=9325&creativeASIN=0735622493)  , from Microsoft Press (ISBN 9780735622494, copyright Microsoft Press 2007, all rights reserved).</span></span>

<span data-ttu-id="dac37-106">Dans l’exemple de code suivant, ShowFolderInfo utilise la méthode [PickFolder()](https://msdn.microsoft.com/library/bb623484\(v=office.15\)) de l’objet [NameSpace](https://msdn.microsoft.com/library/bb645857\(v=office.15\)) pour afficher une boîte de dialogue **Sélection d’un dossier** à l’utilisateur et attend que celui-ci sélectionne un dossier.</span><span class="sxs-lookup"><span data-stu-id="dac37-106">In the following code example,   uses the PickFolder() method of the NameSpace object to display a Select Folder dialog box to the user, and waits for the user to select a folder.</span></span> <span data-ttu-id="dac37-107">Une fois que l’utilisateur a sélectionné un dossier, ses propriétés [EntryID](https://msdn.microsoft.com/library/bb646192\(v=office.15\)), [StoreID](https://msdn.microsoft.com/library/bb612609\(v=office.15\)), [UnReadItemCount](https://msdn.microsoft.com/library/bb610138\(v=office.15\)), [DefaultMessageClass](https://msdn.microsoft.com/library/bb646541\(v=office.15\)), [CurrentView](https://msdn.microsoft.com/library/bb612411\(v=office.15\)), [Name](https://msdn.microsoft.com/library/bb623727\(v=office.15\)) et [FolderPath](https://msdn.microsoft.com/library/bb647409\(v=office.15\)) sont affichées.</span><span class="sxs-lookup"><span data-stu-id="dac37-107">Once the user selects a folder, its [EntryID](https://msdn.microsoft.com/library/bb646192\(v=office.15\)) , [StoreID](https://msdn.microsoft.com/library/bb612609\(v=office.15\)) , [UnReadItemCount](https://msdn.microsoft.com/library/bb610138\(v=office.15\)) , [DefaultMessageClass](https://msdn.microsoft.com/library/bb646541\(v=office.15\)) , [CurrentView](https://msdn.microsoft.com/library/bb612411\(v=office.15\)) , [Name](https://msdn.microsoft.com/library/bb623727\(v=office.15\)) , and [FolderPath](https://msdn.microsoft.com/library/bb647409\(v=office.15\)) properties are displayed.</span></span> <span data-ttu-id="dac37-108">L’exemple appelle ensuite la méthode [GetFolderFromID](https://msdn.microsoft.com/library/bb647784\(v=office.15\)) pour créer un objet [Folder](https://msdn.microsoft.com/library/bb645774\(v=office.15\)) et afficher le dossier.</span><span class="sxs-lookup"><span data-stu-id="dac37-108">The example then calls the [GetFolderFromID](https://msdn.microsoft.com/library/bb647784\(v=office.15\)) method to create a new [Folder](https://msdn.microsoft.com/library/bb645774\(v=office.15\)) object and display the folder.</span></span>

<span data-ttu-id="dac37-109">Si vous utilisez Visual Studio pour tester cet exemple de code, vous devez d’abord ajouter une référence au composant Bibliothèque d’objets Microsoft Outlook 15.0 et spécifier la variable lorsque vous importez l’espace de noms **Microsoft.Office.Interop.Outlook**.</span><span class="sxs-lookup"><span data-stu-id="dac37-109">If you use Visual Studio to test this code example, you must first add a reference to the Microsoft Outlook 15.0 Object Library component and specify the   variable when you import the Microsoft.Office.Interop.Outlook namespace.</span></span> <span data-ttu-id="dac37-110">L'instruction **d’utilisation** ne doit pas se produire juste avant les fonctions de l'exemple de code, mais doit être ajoutée avant la déclaration publique.</span><span class="sxs-lookup"><span data-stu-id="dac37-110">The using statement must not occur directly before the functions in the code example but must be added before the public   declaration.</span></span> <span data-ttu-id="dac37-111">La ligne de code suivante montre comment effectuer l’importation et la tâche dans C\#.</span><span class="sxs-lookup"><span data-stu-id="dac37-111">The following line of code shows how to do the import and assignment in C#.</span></span>

```csharp
using Outlook = Microsoft.Office.Interop.Outlook;
```


```csharp
private void ShowFolderInfo()
{
    Outlook.Folder folder =
        Application.Session.PickFolder()
        as Outlook.Folder;
    if (folder != null)
    {
        StringBuilder sb = new StringBuilder();
        sb.AppendLine("Folder EntryID:");
        sb.AppendLine(folder.EntryID);
        sb.AppendLine();
        sb.AppendLine("Folder StoreID:");
        sb.AppendLine(folder.StoreID);
        sb.AppendLine();
        sb.AppendLine("Unread Item Count: "
            + folder.UnReadItemCount);
        sb.AppendLine("Default MessageClass: "
            + folder.DefaultMessageClass);
        sb.AppendLine("Current View: "
            + folder.CurrentView.Name);
        sb.AppendLine("Folder Path: "
            + folder.FolderPath);
        MessageBox.Show(sb.ToString(),
            "Folder Information",
            MessageBoxButtons.OK,
            MessageBoxIcon.Information);
        Outlook.Folder folderFromID =
            Application.Session.GetFolderFromID(
            folder.EntryID, folder.StoreID)
            as Outlook.Folder;
        folderFromID.Display();
    }
}
```

## <a name="see-also"></a><span data-ttu-id="dac37-112">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="dac37-112">See also</span></span>

- [<span data-ttu-id="dac37-113">Dossiers</span><span class="sxs-lookup"><span data-stu-id="dac37-113">Folders</span></span>](folders.md)

