---
title: Affichage des éléments sélectionnés dans l’Explorateur actif
TOCTitle: Display selected items in the active Explorer
ms:assetid: 31bb217b-8b45-4b50-942e-b6c2a7f13c83
ms:mtpsurl: https://msdn.microsoft.com/library/Dn292517(v=office.15)
ms:contentKeyID: 55119844
ms.date: 07/24/2014
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: b722bcb404f987a6f07a9fe305046ea6673dc231
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32356384"
---
# <a name="display-selected-items-in-the-active-explorer"></a><span data-ttu-id="18d4e-102">Affichage des éléments sélectionnés dans l’Explorateur actif</span><span class="sxs-lookup"><span data-stu-id="18d4e-102">Display selected items in the active Explorer</span></span>

<span data-ttu-id="18d4e-103">Cet exemple montre comment utiliser la classe d’assistance OutlookItem pour afficher correctement tous les éléments sélectionnés dans la fenêtre de l’Explorateur actif.</span><span class="sxs-lookup"><span data-stu-id="18d4e-103">This example shows how to use the OutlookItem helper class to conveniently display all the items selected in the active Explorer window.</span></span>

## <a name="example"></a><span data-ttu-id="18d4e-104">Exemple</span><span class="sxs-lookup"><span data-stu-id="18d4e-104">Example</span></span>

> [!NOTE] 
> <span data-ttu-id="18d4e-105">L’exemple de code suivant est un extrait de [programmation d’Applications pour Microsoft Office Outlook 2007](https://www.amazon.com/gp/product/0735622493?ie=UTF8&tag=msmsdn-20&linkCode=as2&camp=1789&creative=9325&creativeASIN=0735622493).</span><span class="sxs-lookup"><span data-stu-id="18d4e-105">The following code example is an excerpt from [Programming Applications for Microsoft Office Outlook 2007](https://www.amazon.com/gp/product/0735622493?ie=UTF8&tag=msmsdn-20&linkCode=as2&camp=1789&creative=9325&creativeASIN=0735622493).</span></span>

<span data-ttu-id="18d4e-106">L’objet [Selection](https://msdn.microsoft.com/library/bb612099\(v=office.15\)) contient l’ensemble des éléments Outlook sélectionnés dans l’Explorateur Outlook actif.</span><span class="sxs-lookup"><span data-stu-id="18d4e-106">The [Selection](https://msdn.microsoft.com/library/bb612099\(v=office.15\)) object contains the set of Outlook items currently selected in the active Outlook explorer.</span></span> <span data-ttu-id="18d4e-107">Ni l’Explorateur actif, représenté par [ActiveExplorer()](https://msdn.microsoft.com/library/bb647410\(v=office.15\)), ni l’ensemble des éléments sélectionnés, n’indique le type des éléments sélectionnés.</span><span class="sxs-lookup"><span data-stu-id="18d4e-107">Neither the active explorer, represented by [ActiveExplorer()](https://msdn.microsoft.com/library/bb647410\(v=office.15\)), nor the set of selected items indicates the type of the items that are selected.</span></span> <span data-ttu-id="18d4e-108">Normalement, il faut d’abord identifier le type d’élément, puis appeler la méthode **Display** spécifique pour ce type.</span><span class="sxs-lookup"><span data-stu-id="18d4e-108">Normally, you would have to first identify the item type and then call the specific **Display** method for that type.</span></span> <span data-ttu-id="18d4e-109">Dans la mesure où la méthode **Display** est commune à tous les objets des éléments Outlook et où la classe d’assistance OutlookItem inclut cette méthode, vous pouvez tirer parti de la classe d’assistance, en déclarant une instance de l’objet OutlookItem, myItem, et en utilisant myItem.Display pour afficher chaque élément de la sélection.</span><span class="sxs-lookup"><span data-stu-id="18d4e-109">Because the **Display** method is common to all Outlook items objects and the OutlookItem helper class includes this method, you can take advantage of the helper class, by declaring an instance of the OutlookItem object, myItem, and using myItem.Display to display each item in the selection.</span></span> <span data-ttu-id="18d4e-110">Vous pouvez en apprendre plus sur l’implémentation de la classe d’assistance OutlookItem dans l’article [Créer une classe d’assistance pour accéder aux membres d’élément courant Outlook](how-to-create-a-helper-class-to-access-common-outlook-item-members.md)</span><span class="sxs-lookup"><span data-stu-id="18d4e-110">You can see the implementation of the OutlookItem helper class in [Create a Helper Class to Access Common Outlook Item Members](how-to-create-a-helper-class-to-access-common-outlook-item-members.md)</span></span>

<span data-ttu-id="18d4e-111">Si vous utilisez Visual Studio pour tester cet exemple de code, vous devez d’abord ajouter une référence au composant Bibliothèque d’objets Microsoft Outlook 15.0 et spécifier la variable lorsque vous importez l’espace de noms **Microsoft.Office.Interop.Outlook**.</span><span class="sxs-lookup"><span data-stu-id="18d4e-111">If you use Visual Studio to test this code example, you must first add a reference to the Microsoft Outlook 15.0 Object Library component and specify the Outlook variable when you import the **Microsoft.Office.Interop.Outlook** namespace.</span></span> <span data-ttu-id="18d4e-112">L’instruction **using** ne doit pas se produire juste avant les fonctions de l’exemple de code, mais doit être ajoutée avant la déclaration publique.</span><span class="sxs-lookup"><span data-stu-id="18d4e-112">The **using** statement must not occur directly before the functions in the code example but must be added before the public Class declaration.</span></span> <span data-ttu-id="18d4e-113">Le code suivant illustre l’importation et l’affectation dans C\#.</span><span class="sxs-lookup"><span data-stu-id="18d4e-113">The following line of code shows how to do the import and assignment in C\#.</span></span>

```csharp
using Outlook = Microsoft.Office.Interop.Outlook;
```


```csharp
private void DisplaySelectedItems()
{
    Outlook.Selection selection =
        Application.ActiveExplorer().Selection;
    for (int i = 1; i <= selection.Count; i++)
    {
        OutlookItem myItem = new OutlookItem(selection[i]);
        myItem.Display();
    }
}
```

## <a name="see-also"></a><span data-ttu-id="18d4e-114">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="18d4e-114">See also</span></span>

- [<span data-ttu-id="18d4e-115">Créer une classe d’assistance pour accéder aux membres d’élément Outlook courant</span><span class="sxs-lookup"><span data-stu-id="18d4e-115">Create a Helper class to access common Outlook item members</span></span>](how-to-create-a-helper-class-to-access-common-outlook-item-members.md)
- [<span data-ttu-id="18d4e-116">Éléments Outlook généraux</span><span class="sxs-lookup"><span data-stu-id="18d4e-116">General Outlook items</span></span>](general-outlook-items.md)

