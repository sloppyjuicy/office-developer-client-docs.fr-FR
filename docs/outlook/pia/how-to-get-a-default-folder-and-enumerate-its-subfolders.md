---
title: Obtention d’un dossier par défaut et énumération de ses sous-dossiers
TOCTitle: Get a default folder and enumerate its subfolders
ms:assetid: 587e8392-cb03-442c-9058-1282f36dabdb
ms:mtpsurl: https://msdn.microsoft.com/library/Ff184610(v=office.15)
ms:contentKeyID: 55119857
ms.date: 07/24/2014
mtps_version: v=office.15
ms.openlocfilehash: 934b5f823127fde9fbbd3a49f41cedb791277e7e
ms.sourcegitcommit: ef717c65d8dd41ababffb01eafc443c79950aed4
ms.translationtype: HT
ms.contentlocale: fr-FR
ms.lasthandoff: 10/04/2018
ms.locfileid: "25407400"
---
# <a name="get-a-default-folder-and-enumerate-its-subfolders"></a><span data-ttu-id="72384-102">Obtention d’un dossier par défaut et énumération de ses sous-dossiers</span><span class="sxs-lookup"><span data-stu-id="72384-102">Get a default folder and enumerate its subfolders</span></span>

<span data-ttu-id="72384-103">Cet exemple montre comment obtenir un dossier par défaut dans la banque d’informations de l’utilisateur par défaut et comment énumérer ses sous-dossiers.</span><span class="sxs-lookup"><span data-stu-id="72384-103">This example shows how to obtain a default folder in the user’s default store and enumerate its subfolders.</span></span>

## <a name="example"></a><span data-ttu-id="72384-104">Exemple</span><span class="sxs-lookup"><span data-stu-id="72384-104">Example</span></span>

> [!NOTE] 
> <span data-ttu-id="72384-105">L’exemple de code suivant est un extrait de [programmation d’Applications pour Microsoft Office Outlook 2007](https://www.amazon.com/gp/product/0735622493?ie=UTF8&tag=msmsdn-20&linkCode=as2&camp=1789&creative=9325&creativeASIN=0735622493).</span><span class="sxs-lookup"><span data-stu-id="72384-105">The following code example is an excerpt from  [Programming Applications for Microsoft Office Outlook 2007](https://www.amazon.com/gp/product/0735622493?ie=UTF8&tag=msmsdn-20&linkCode=as2&camp=1789&creative=9325&creativeASIN=0735622493)  , from Microsoft Press (ISBN 9780735622494, copyright Microsoft Press 2007, all rights reserved).</span></span>

<span data-ttu-id="72384-106">Dans l’exemple de code suivant, GetRSSFeeds utilise la méthode [GetDefaultFolder(OlDefaultFolders)](https://msdn.microsoft.com/library/bb646473\(v=office.15\)) de l’objet [NameSpace](https://msdn.microsoft.com/library/bb645857\(v=office.15\)) pour obtenir le dossier racine RSS Feeds de l’utilisateur.</span><span class="sxs-lookup"><span data-stu-id="72384-106">In the following code example,   uses the GetDefaultFolder(OlDefaultFolders) method of the NameSpace object to obtain the user's RSS Feeds root folder.</span></span> <span data-ttu-id="72384-107">GetRSSFeeds affiche ensuite une zone de message qui contient les noms des dossiers pour tous les flux RSS du dossier RSS Feeds.</span><span class="sxs-lookup"><span data-stu-id="72384-107"> then displays a message box that contains the folder names for all RSS feeds in the RSS Feeds folder.</span></span>

<span data-ttu-id="72384-108">Si vous utilisez Visual Studio pour tester cet exemple de code, vous devez d’abord ajouter une référence au composant Bibliothèque d’objets Microsoft Outlook 15.0 et spécifier la variable lorsque vous importez l’espace de noms **Microsoft.Office.Interop.Outlook**.</span><span class="sxs-lookup"><span data-stu-id="72384-108">If you use Visual Studio to test this code example, you must first add a reference to the Microsoft Outlook 15.0 Object Library component and specify the   variable when you import the Microsoft.Office.Interop.Outlook namespace.</span></span> <span data-ttu-id="72384-109">L'instruction **d’utilisation** ne doit pas se produire juste avant les fonctions de l'exemple de code, mais doit être ajoutée avant la déclaration publique.</span><span class="sxs-lookup"><span data-stu-id="72384-109">The using statement must not occur directly before the functions in the code example but must be added before the public   declaration.</span></span> <span data-ttu-id="72384-110">La ligne de code suivante montre comment effectuer l’importation et la tâche dans C\#.</span><span class="sxs-lookup"><span data-stu-id="72384-110">The following line of code shows how to do the import and assignment in C#.</span></span>

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

## <a name="see-also"></a><span data-ttu-id="72384-111">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="72384-111">See also</span></span>

- [<span data-ttu-id="72384-112">Dossiers</span><span class="sxs-lookup"><span data-stu-id="72384-112">Folders</span></span>](folders.md)

