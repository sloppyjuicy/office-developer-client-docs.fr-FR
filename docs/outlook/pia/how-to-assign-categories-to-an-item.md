---
title: Affecter des catégories à un élément
TOCTitle: Assign categories to an item
ms:assetid: 4070801b-994a-46df-91fe-4efca834886e
ms:mtpsurl: https://msdn.microsoft.com/library/Ff424469(v=office.15)
ms:contentKeyID: 55119828
ms.date: 07/24/2014
mtps_version: v=office.15
ms.openlocfilehash: 762fd5954e6ec47aed24a9c91b41839f6d292cd9
ms.sourcegitcommit: ef717c65d8dd41ababffb01eafc443c79950aed4
ms.translationtype: HT
ms.contentlocale: fr-FR
ms.lasthandoff: 10/04/2018
ms.locfileid: "25407190"
---
# <a name="assign-categories-to-an-item"></a><span data-ttu-id="3454e-102">Affecter des catégories à un élément</span><span class="sxs-lookup"><span data-stu-id="3454e-102">Assign categories to an item</span></span>

<span data-ttu-id="3454e-103">Cet exemple montre comment affecter des catégories à un élément à l’aide de sa propriété **Categories**.</span><span class="sxs-lookup"><span data-stu-id="3454e-103">This example shows how to assign categories to an item by using its **Categories** property.</span></span>

## <a name="example"></a><span data-ttu-id="3454e-104">Exemple</span><span class="sxs-lookup"><span data-stu-id="3454e-104">Example</span></span>

> [!NOTE] 
> <span data-ttu-id="3454e-105">L’exemple de code suivant est un extrait de la [programmation d’Applications pour Microsoft Office Outlook 2007](https://www.amazon.com/gp/product/0735622493?ie=UTF8&tag=msmsdn-20&linkCode=as2&camp=1789&creative=9325&creativeASIN=0735622493).</span><span class="sxs-lookup"><span data-stu-id="3454e-105">The following code example is an excerpt from  [Programming Applications for Microsoft Office Outlook 2007](https://www.amazon.com/gp/product/0735622493?ie=UTF8&tag=msmsdn-20&linkCode=as2&camp=1789&creative=9325&creativeASIN=0735622493)  , from Microsoft Press (ISBN 9780735622494, copyright Microsoft Press 2007, all rights reserved).</span></span>


<span data-ttu-id="3454e-106">Pour affecter des catégories à un élément, utilisez la propriété **Categories** de l’élément particulier.</span><span class="sxs-lookup"><span data-stu-id="3454e-106">To assign categories to an item, use the particular item's **Categories** property.</span></span> <span data-ttu-id="3454e-107">Cet exemple de code permet d’utiliser la classe d’assistance OutlookItem, définie dans la rubrique décrivant comment [créer une classe d’assistance pour permettre d’accéder aux membres éléments Outlook courants](how-to-create-a-helper-class-to-access-common-outlook-item-members.md), pour appeler facilement la propriété OutlookItem.**Categories** sans devoir d’abord distribuer l’élément.</span><span class="sxs-lookup"><span data-stu-id="3454e-107">This code sample makes use of the OutlookItem helper class, defined in [Create a Helper Class to Access Common Outlook Item Members](how-to-create-a-helper-class-to-access-common-outlook-item-members.md), to conveniently call the OutlookItem.**Categories** property without having to first cast the item.</span></span> <span data-ttu-id="3454e-108">La propriété **Categories** obtient ou définit des catégories qui sont représentées par une chaîne délimitée par des virgules pouvant contenir jusqu’à 255 caractères.</span><span class="sxs-lookup"><span data-stu-id="3454e-108">This property gets or sets categories that are represented by a comma-delimited string that can contain a maximum of 255 characters.</span></span> <span data-ttu-id="3454e-109">Les virgules et les espaces servent à séparer les valeurs de catégorie.</span><span class="sxs-lookup"><span data-stu-id="3454e-109">The commas and spaces are used to separate the category values.</span></span> <span data-ttu-id="3454e-110">Si vous affectez une catégorie qui ne figure pas dans la collection [Categories](https://msdn.microsoft.com/library/bb646607\(v=office.15\)) de l’objet [NameSpace](https://msdn.microsoft.com/library/bb645857\(v=office.15\)), la catégorie n’affiche pas de couleur.</span><span class="sxs-lookup"><span data-stu-id="3454e-110">Assigning a category that is not in the [Categories](https://msdn.microsoft.com/library/bb646607\(v=office.15\)) collection of the [NameSpace](https://msdn.microsoft.com/library/bb645857\(v=office.15\)) object will result in the category not displaying a color.</span></span>

<span data-ttu-id="3454e-p102">Dans l’exemple de code suivant, AssignCategories crée une restriction pour les éléments qui contiennent ISV dans l’objet du message en utilisant d’abord une requête DASL pour filtrer les éléments de la Boîte de réception qui contiennent ISV dans l’objet. AssignCategories effectue ensuite une itération sur les éléments filtrés en utilisant la classe **OutlookItem** et, si la chaîne retournée par **item.Categories** n’est pas une référence null ou est déjà assignée à ISV, la catégorie ISV est assignée à l’élément.</span><span class="sxs-lookup"><span data-stu-id="3454e-p102">In the following code example, AssignCategories creates a restriction for items that contain “ISV” in the subject by first using a DAV Searching and Locating (DASL) query to filter items in the Inbox that contain “ISV” in the subject. AssignCategories then iterates through the filtered items by using the **OutlookItem** class and, if the string returned by **item.Categories** is not a null reference or was already assigned to the ISV, the ISV category is assigned to the item.</span></span>

```csharp
using Outlook = Microsoft.Office.Interop.Outlook;
```

```csharp
private void AssignCategories()
{
    string filter = "@SQL=" + "\"" + "urn:schemas:httpmail:subject"
        + "\"" + " ci_phrasematch 'ISV'";
    Outlook.Items items =
        Application.Session.GetDefaultFolder(
        Outlook.OlDefaultFolders.olFolderInbox).Items.Restrict(filter);
    for (int i = 1; i <= items.Count; i++)
    {
        OutlookItem item = new OutlookItem(items[i]);
        string existingCategories = item.Categories;
        if (String.IsNullOrEmpty(existingCategories))
        {
            item.Categories = "ISV";
        }
        else
        {
            if (item.Categories.Contains("ISV") == false)
            {
                item.Categories = existingCategories + ", ISV";
            }
        }
        item.Save();
    }
}
```

## <a name="see-also"></a><span data-ttu-id="3454e-113">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="3454e-113">See also</span></span>

- [<span data-ttu-id="3454e-114">Catégories de couleurs</span><span class="sxs-lookup"><span data-stu-id="3454e-114">Color Categories</span></span>](color-categories.md)

