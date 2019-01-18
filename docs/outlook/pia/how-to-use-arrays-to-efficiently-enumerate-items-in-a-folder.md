---
title: Utilisation des tableaux pour énumérer efficacement les éléments d’un dossier
TOCTitle: Use arrays to efficiently enumerate items in a folder
ms:assetid: 05a73225-ad0d-4d52-90b6-448d220348df
ms:mtpsurl: https://msdn.microsoft.com/library/Ff184588(v=office.15)
ms:contentKeyID: 55119885
ms.date: 07/24/2014
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: be65e2818f22e6da289ef8b8da483c2747f941a5
ms.sourcegitcommit: d6695c94415fa47952ee7961a69660abc0904434
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/17/2019
ms.locfileid: "28717208"
---
# <a name="use-arrays-to-efficiently-enumerate-items-in-a-folder"></a><span data-ttu-id="01fef-102">Utilisation des tableaux pour énumérer efficacement les éléments d’un dossier</span><span class="sxs-lookup"><span data-stu-id="01fef-102">Use arrays to efficiently enumerate items in a folder</span></span>

<span data-ttu-id="01fef-103">Cet exemple montre comment énumérer efficacement les éléments dans un objet [Folder](https://msdn.microsoft.com/library/bb645774\(v=office.15\)) à l’aide de la méthode [GetArray(Int32)](https://msdn.microsoft.com/library/bb608928\(v=office.15\)).</span><span class="sxs-lookup"><span data-stu-id="01fef-103">This example shows how to efficiently enumerate items in a [Folder](https://msdn.microsoft.com/library/bb645774\(v=office.15\)) object by using the [GetArray(Int32)](https://msdn.microsoft.com/library/bb608928\(v=office.15\)) method.</span></span>

## <a name="example"></a><span data-ttu-id="01fef-104">Exemple</span><span class="sxs-lookup"><span data-stu-id="01fef-104">Example</span></span>

> [!NOTE] 
> <span data-ttu-id="01fef-105">L’exemple de code suivant est un extrait de [programmation d’Applications pour Microsoft Office Outlook 2007](https://www.amazon.com/gp/product/0735622493?ie=UTF8&tag=msmsdn-20&linkCode=as2&camp=1789&creative=9325&creativeASIN=0735622493).</span><span class="sxs-lookup"><span data-stu-id="01fef-105">The following code example is an excerpt from [Programming Applications for Microsoft Office Outlook 2007](https://www.amazon.com/gp/product/0735622493?ie=UTF8&tag=msmsdn-20&linkCode=as2&camp=1789&creative=9325&creativeASIN=0735622493).</span></span>

<span data-ttu-id="01fef-106">Dans l’exemple de code suivant, DemoGetArrayForTable obtient un objet [Table](https://msdn.microsoft.com/library/bb652856\(v=office.15\)) d’un objet **Folder** à l’aide de la méthode [GetTable(Object, Object)](https://msdn.microsoft.com/library/bb612592\(v=office.15\)).</span><span class="sxs-lookup"><span data-stu-id="01fef-106">In the following code example, DemoGetArrayForTable gets a [Table](https://msdn.microsoft.com/library/bb652856\(v=office.15\)) object from a **Folder** object by using the [GetTable(Object, Object)](https://msdn.microsoft.com/library/bb612592\(v=office.15\)) method.</span></span> <span data-ttu-id="01fef-107">DemoGetArrayForTable utilise ensuite la méthode **GetArray** pour renvoyer un objet [Array](https://msdn.microsoft.com/library/system.array.aspx) qui contient des éléments pour chaque ligne du tableau.</span><span class="sxs-lookup"><span data-stu-id="01fef-107">DemoGetArrayForTable then uses the **GetArray** method to return an [Array](https://msdn.microsoft.com/library/system.array.aspx) object that contains elements for every row in the table.</span></span> <span data-ttu-id="01fef-108">L’objet **Array** renvoyé est un tableau à deux dimensions qui représente un ensemble de valeurs de ligne et de colonne issues de l’objet **Table**.</span><span class="sxs-lookup"><span data-stu-id="01fef-108">The returned **Array** object is a two-dimensional array that represents a set of row and column values from the **Table**.</span></span> <span data-ttu-id="01fef-109">Il s’agit d’un tableau de base zéro, et non de base un comme c’est le cas des collections Outlook.</span><span class="sxs-lookup"><span data-stu-id="01fef-109">The array is zero-based, instead of one-based as is the case with Outlook collections.</span></span> <span data-ttu-id="01fef-110">Une fois que l’objet **Array** est obtenu, le code utilise une boucle for pour énumérer le contenu du tableau.</span><span class="sxs-lookup"><span data-stu-id="01fef-110">Once the **Array** object is obtained, the code uses a for loop to enumerate through the table.</span></span>

<span data-ttu-id="01fef-111">Si vous utilisez Visual Studio pour tester cet exemple de code, vous devez d’abord ajouter une référence au composant Bibliothèque d’objets Microsoft Outlook 15.0 et spécifier la variable lorsque vous importez l’espace de noms **Microsoft.Office.Interop.Outlook**.</span><span class="sxs-lookup"><span data-stu-id="01fef-111">If you use Visual Studio to test this code example, you must first add a reference to the Microsoft Outlook 15.0 Object Library component and specify the Outlook variable when you import the **Microsoft.Office.Interop.Outlook** namespace.</span></span> <span data-ttu-id="01fef-112">L'instruction **d’utilisation** ne doit pas se produire juste avant les fonctions de l'exemple de code, mais doit être ajoutée avant la déclaration publique.</span><span class="sxs-lookup"><span data-stu-id="01fef-112">The **using** statement must not occur directly before the functions in the code example but must be added before the public Class declaration.</span></span> <span data-ttu-id="01fef-113">La ligne de code suivante montre comment effectuer l’importation et la tâche dans C\#.</span><span class="sxs-lookup"><span data-stu-id="01fef-113">The following line of code shows how to do the import and assignment in C\#.</span></span>

```csharp
using Outlook = Microsoft.Office.Interop.Outlook;
```


```csharp
private void DemoGetArrayForTable()
{
    // Obtain Inbox
    Outlook.Folder folder =
        Application.Session.GetDefaultFolder(
        Outlook.OlDefaultFolders.olFolderInbox)
        as Outlook.Folder;
    Outlook.Table table =
        folder.GetTable("", Outlook.OlTableContents.olUserItems);
    Array tableArray = table.GetArray(table.GetRowCount()) as Array;
    for (int i = 0; i <= tableArray.GetUpperBound(0); i++)
    {
        for (int j = 0; j <= tableArray.GetUpperBound(1); j++)
        {
            Debug.WriteLine(tableArray.GetValue(i, j));
        }
    }
}
```

## <a name="see-also"></a><span data-ttu-id="01fef-114">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="01fef-114">See also</span></span>

- [<span data-ttu-id="01fef-115">Rechercher et filtrer</span><span class="sxs-lookup"><span data-stu-id="01fef-115">Search and filter</span></span>](search-and-filter.md)

