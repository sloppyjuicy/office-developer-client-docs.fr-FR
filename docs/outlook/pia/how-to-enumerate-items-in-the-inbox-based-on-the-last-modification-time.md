---
title: Énumération des éléments de la Boîte de réception selon l’heure de la dernière modification
TOCTitle: Enumerate items in the Inbox based on the last modification time
ms:assetid: 93a25143-def6-4832-bac2-3744558c2736
ms:mtpsurl: https://msdn.microsoft.com/library/Ff184626(v=office.15)
ms:contentKeyID: 55119920
ms.date: 07/24/2014
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: 0a568209caf172fbab26af1441ba7c208562ae19
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32320355"
---
# <a name="enumerate-items-in-the-inbox-based-on-the-last-modification-time"></a><span data-ttu-id="1130c-102">Énumération des éléments de la Boîte de réception selon l’heure de la dernière modification</span><span class="sxs-lookup"><span data-stu-id="1130c-102">Enumerate items in the Inbox based on the last modification time</span></span>

<span data-ttu-id="1130c-103">Cet exemple montre comment énumérer les éléments du dossier Boîte de réception selon l’heure de la dernière modification.</span><span class="sxs-lookup"><span data-stu-id="1130c-103">This example shows how to enumerate items in the Inbox folder based on the last modification time.</span></span>

## <a name="example"></a><span data-ttu-id="1130c-104">Exemple</span><span class="sxs-lookup"><span data-stu-id="1130c-104">Example</span></span>

> [!NOTE] 
> <span data-ttu-id="1130c-105">L’exemple de code suivant est un extrait de [programmation d’Applications pour Microsoft Office Outlook 2007](https://www.amazon.com/gp/product/0735622493?ie=UTF8&tag=msmsdn-20&linkCode=as2&camp=1789&creative=9325&creativeASIN=0735622493).</span><span class="sxs-lookup"><span data-stu-id="1130c-105">The following code example is an excerpt from [Programming Applications for Microsoft Office Outlook 2007](https://www.amazon.com/gp/product/0735622493?ie=UTF8&tag=msmsdn-20&linkCode=as2&camp=1789&creative=9325&creativeASIN=0735622493).</span></span>

<span data-ttu-id="1130c-106">L’objet [Table](https://msdn.microsoft.com/library/bb652856\(v=office.15\)) représente un ensemble d’éléments d’un objet [Folder](https://msdn.microsoft.com/library/bb645774\(v=office.15\)) ou [Search](https://msdn.microsoft.com/library/bb612611\(v=office.15\)).</span><span class="sxs-lookup"><span data-stu-id="1130c-106">The [Table](https://msdn.microsoft.com/library/bb652856\(v=office.15\)) object represents a set of items from a [Folder](https://msdn.microsoft.com/library/bb645774\(v=office.15\)) or [Search](https://msdn.microsoft.com/library/bb612611\(v=office.15\)) object.</span></span> <span data-ttu-id="1130c-107">Pour obtenir un objet **Table**, appelez la méthode [GetTable (Object, Object)](https://msdn.microsoft.com/library/bb612592\(v=office.15\)) sur un objet **Folder** ou **Search**.</span><span class="sxs-lookup"><span data-stu-id="1130c-107">To obtain a **Table**, call the [GetTable(Object, Object)](https://msdn.microsoft.com/library/bb612592\(v=office.15\)) method on a **Folder** or **Search** object.</span></span> <span data-ttu-id="1130c-108">Chaque élément de l’élément **Table** renvoyé contient seulement un sous-ensemble par défaut des propriétés de l’élément.</span><span class="sxs-lookup"><span data-stu-id="1130c-108">Each item in the returned **Table** contains only a default subset of the item’s properties.</span></span> <span data-ttu-id="1130c-109">Chaque objet [Row](https://msdn.microsoft.com/library/bb610126\(v=office.15\)) peut être considéré comme un élément du dossier et chaque objet [Column](https://msdn.microsoft.com/library/bb609646\(v=office.15\)), comme une propriété d’un élément.</span><span class="sxs-lookup"><span data-stu-id="1130c-109">Each [Row](https://msdn.microsoft.com/library/bb610126\(v=office.15\)) object can be regarded as an item in the folder, and each [Column](https://msdn.microsoft.com/library/bb609646\(v=office.15\)) object as a property of an item.</span></span> <span data-ttu-id="1130c-110">La suppression, l'ajout et la modification de lignes ne sont pas prises en charge dans l'objet **Table**.</span><span class="sxs-lookup"><span data-stu-id="1130c-110">Removing, adding, or changing rows is not supported in the **Table**.</span></span> <span data-ttu-id="1130c-111">Pour énumérer des éléments dans un objet **Table**, utilisez d'abord la propriété [EndOfTable](https://msdn.microsoft.com/library/bb647715\(v=office.15\)) pour voir si votre position actuelle est la fin du tableau.</span><span class="sxs-lookup"><span data-stu-id="1130c-111">To enumerate items in a **Table**, first use the [EndOfTable](https://msdn.microsoft.com/library/bb647715\(v=office.15\)) property to see whether your current position is at the end of the table.</span></span> <span data-ttu-id="1130c-112">Si **EndOfTable** retourne **false**, utilisez la méthode [GetNextRow()](https://msdn.microsoft.com/library/bb609740\(v=office.15\)) pour retourner un objet **Row**, qui contient un nombre par défaut d'objets **Column**.</span><span class="sxs-lookup"><span data-stu-id="1130c-112">If **EndOfTable** returns **false**, use the [GetNextRow()](https://msdn.microsoft.com/library/bb609740\(v=office.15\)) method to return a **Row**, which contains a default number of **Column** objects.</span></span> <span data-ttu-id="1130c-113">Pour poursuivre l’itération directement dans l’objet **Table**, appelez la méthode **GetNextRow** jusqu’à ce que la propriété **EndOfTable** renvoie **true**.</span><span class="sxs-lookup"><span data-stu-id="1130c-113">You continue iterating in a forward manner through the **Table** by calling **GetNextRow** until **EndOfTable** returns **true**.</span></span>

<span data-ttu-id="1130c-114">Dans l’exemple de code suivant, DemoTableForInbox obtient un objet **Table** pour le dossier Boîte de réception, trie l’objet **Table** à l’aide de la propriété **LastModificationTime** et de la méthode [Sort(String, Object)](https://msdn.microsoft.com/library/bb652667\(v=office.15\)), et procède à l’itération dans le tableau pour écrire l’objet de chaque élément dans les écouteurs de suivi de la collection [Listeners](https://msdn.microsoft.com/library/system.diagnostics.debug.listeners.aspx).</span><span class="sxs-lookup"><span data-stu-id="1130c-114">In the following code example, DemoTableForInbox obtains a **Table** object for the Inbox folder, sorts the **Table** object by using the **LastModificationTime** property and [Sort(String, Object)](https://msdn.microsoft.com/library/bb652667\(v=office.15\)) method, and iterates through the table to write the subject of each item to the trace listeners of the [Listeners](https://msdn.microsoft.com/library/system.diagnostics.debug.listeners.aspx) collection.</span></span>

<span data-ttu-id="1130c-115">Si vous utilisez Visual Studio pour tester cet exemple de code, vous devez d’abord ajouter une référence au composant Bibliothèque d’objets Microsoft Outlook 15.0 et spécifier la variable lorsque vous importez l’espace de noms **Microsoft.Office.Interop.Outlook**.</span><span class="sxs-lookup"><span data-stu-id="1130c-115">If you use Visual Studio to test this code example, you must first add a reference to the Microsoft Outlook 15.0 Object Library component and specify the Outlook variable when you import the **Microsoft.Office.Interop.Outlook** namespace.</span></span> <span data-ttu-id="1130c-116">L’instruction **using** ne doit pas se produire juste avant les fonctions de l’exemple de code, mais doit être ajoutée avant la déclaration publique.</span><span class="sxs-lookup"><span data-stu-id="1130c-116">The **using** statement must not occur directly before the functions in the code example but must be added before the public Class declaration.</span></span> <span data-ttu-id="1130c-117">Le code suivant illustre l’importation et l’affectation dans C\#.</span><span class="sxs-lookup"><span data-stu-id="1130c-117">The following line of code shows how to do the import and assignment in C\#.</span></span>

```csharp
using Outlook = Microsoft.Office.Interop.Outlook;
```


```csharp
private void DemoTableForInbox()
{
    //Obtain Inbox
    Outlook.Folder folder =
        Application.Session.GetDefaultFolder(
        Outlook.OlDefaultFolders.olFolderInbox)
        as Outlook.Folder;
    //Obtain Table using defaults
    Outlook.Table table =
        folder.GetTable(Type.Missing, Type.Missing);
    table.Sort("LastModificationTime",
        Outlook.OlSortOrder.olDescending);
    while (!table.EndOfTable)
    {
        Outlook.Row nextRow = table.GetNextRow();
        Debug.WriteLine(nextRow["Subject"]);
    }
}
```

## <a name="see-also"></a><span data-ttu-id="1130c-118">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="1130c-118">See also</span></span>

- [<span data-ttu-id="1130c-119">Rechercher et filtrer</span><span class="sxs-lookup"><span data-stu-id="1130c-119">Search and filter</span></span>](search-and-filter.md)

