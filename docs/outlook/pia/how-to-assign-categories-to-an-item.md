---
title: Affecter des catégories à un élément
TOCTitle: Assign categories to an item
ms:assetid: 4070801b-994a-46df-91fe-4efca834886e
ms:mtpsurl: https://msdn.microsoft.com/library/Ff424469(v=office.15)
ms:contentKeyID: 55119828
ms.date: 07/24/2014
mtps_version: v=office.15
ms.localizationpriority: medium
ms.openlocfilehash: 1e095837a25b07053e2f590fdabbd63d4baa5d70
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/24/2021
ms.locfileid: "59619381"
---
# <a name="assign-categories-to-an-item"></a>Affecter des catégories à un élément

Cet exemple montre comment affecter des catégories à un élément à l’aide de sa propriété **Categories**.

## <a name="example"></a>Exemple

> [!NOTE] 
> L’exemple de code suivant est un extrait de la [programmation d’Applications pour Microsoft Office Outlook 2007](https://www.amazon.com/gp/product/0735622493?ie=UTF8&tag=msmsdn-20&linkCode=as2&camp=1789&creative=9325&creativeASIN=0735622493).


Pour affecter des catégories à un élément, utilisez la propriété **Categories** de l’élément particulier. Cet exemple de code permet d’utiliser la classe d’assistance OutlookItem, définie dans la rubrique décrivant comment [créer une classe d’assistance pour permettre d’accéder aux membres éléments Outlook courants](how-to-create-a-helper-class-to-access-common-outlook-item-members.md), pour appeler facilement la propriété OutlookItem.**Categories** sans devoir d’abord distribuer l’élément. La propriété **Categories** obtient ou définit des catégories qui sont représentées par une chaîne délimitée par des virgules pouvant contenir jusqu’à 255 caractères. Les virgules et les espaces servent à séparer les valeurs de catégorie. Si vous affectez une catégorie qui ne figure pas dans la collection [Categories](https://msdn.microsoft.com/library/bb646607\(v=office.15\)) de l’objet [NameSpace](https://msdn.microsoft.com/library/bb645857\(v=office.15\)), la catégorie n’affiche pas de couleur.

Dans l’exemple de code suivant, AssignCategories crée une restriction pour les éléments qui contiennent ISV dans l’objet du message en utilisant d’abord une requête DASL pour filtrer les éléments de la Boîte de réception qui contiennent ISV dans l’objet. AssignCategories effectue ensuite une itération sur les éléments filtrés en utilisant la classe **OutlookItem** et, si la chaîne retournée par **item.Categories** n’est pas une référence null ou est déjà assignée à ISV, la catégorie ISV est assignée à l’élément.

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

## <a name="see-also"></a>Voir aussi

- [Catégories de couleurs](color-categories.md)

