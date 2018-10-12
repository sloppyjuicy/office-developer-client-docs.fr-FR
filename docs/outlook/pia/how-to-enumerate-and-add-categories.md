---
title: Énumérer et ajouter des catégories
TOCTitle: Enumerate and add categories
ms:assetid: 17a94a01-c463-4332-851e-7d280c66d8c2
ms:mtpsurl: https://msdn.microsoft.com/library/Ff424467(v=office.15)
ms:contentKeyID: 55119829
ms.date: 07/24/2014
mtps_version: v=office.15
ms.openlocfilehash: 27fc8630c8e2eb0b491dbb5075f4c58aacec7f93
ms.sourcegitcommit: ef717c65d8dd41ababffb01eafc443c79950aed4
ms.translationtype: HT
ms.contentlocale: fr-FR
ms.lasthandoff: 10/04/2018
ms.locfileid: "25406245"
---
# <a name="enumerate-and-add-categories"></a>Énumérer et ajouter des catégories

Cet exemple montre comment énumérer les catégories et ajouter une catégorie à la liste de catégorie principale.

## <a name="example"></a>Exemple

> [!NOTE] 
> L’exemple de code suivant est un extrait de [Programmation d’Applications pour Microsoft Office Outlook 2007](https://www.amazon.com/gp/product/0735622493?ie=UTF8&tag=msmsdn-20&linkCode=as2&camp=1789&creative=9325&creativeASIN=0735622493).

Le modèle objet Outlook prend en charge des catégories qui simplifient l'organisation des éléments dans la boîte de réception d'un utilisateur. Pour conserver un niveau supérieur d’organisation, vous pouvez procédez comme suit :

- Classer les éléments Outlook et les afficher par catégorie.
- Appliquer plusieurs catégories de couleur à un élément Outlook unique.
- Grouper et trier des éléments Outlook par catégorie de couleur.
- Affecter des touches de raccourci à chaque catégorie de couleur, permettant ainsi aux utilisateurs de classer plus facilement les éléments.
- Créer, et changer les catégories de couleurs par programme ou par une action de l'utilisateur dans l'interface utilisateur d'Outlook.

Pour exposer la fonctionnalité des catégories, le modèle objet Outlook fournit un objet [Category](https://msdn.microsoft.com/library/bb623480\(v=office.15\)) qui représente une catégorie couleur définie par l'utilisateur dans la liste principale de catégories. La liste principale de catégories contient les catégories couleur qui sont présentées dans l'interface utilisateur d'Outlook. La liste est représentée par la collection [Categories](https://msdn.microsoft.com/library/bb623535\(v=office.15\)) de l'objet [NameSpace](https://msdn.microsoft.com/library/bb645857\(v=office.15\)) . Pour créer un objet **Category**, utilisez la méthode [Add(String, Object, Object)](https://msdn.microsoft.com/library/bb623093\(v=office.15\)) de la collection **Categories**. Lorsque vous créez un objet **Category**, un identificateur global unique (GUID, Globally Unique Identifier) est créé, et cet identificateur ne peut pas être modifié. Il est représenté par la propriété [CategoryID](https://msdn.microsoft.com/library/bb647100\(v=office.15\)). Cependant, vous pouvez changer le nom, la couleur et la touche de raccourci associés à une catégorie de couleur en définissant les propriétés [Name](https://msdn.microsoft.com/library/bb645577\(v=office.15\)), [Color](https://msdn.microsoft.com/library/bb612316\(v=office.15\)) et [ShortcutKey](https://msdn.microsoft.com/library/bb644944\(v=office.15\)), respectivement, de l'objet **Category**. Vous pouvez modifier la propriété **Color** en définissant ou en récupérant sa constante [OlCategoryColor](https://msdn.microsoft.com/library/bb608974\(v=office.15\)). Pour reproduire la couleur dans un contrôle personnalisé, utilisez les propriétés en lecture seule suivantes de l'objet **Category**:

  - [CategoryBorderColor](https://msdn.microsoft.com/library/bb610083\(v=office.15\))

  - [CategoryGradientBottomColor](https://msdn.microsoft.com/library/bb647357\(v=office.15\))

  - [CategoryGradientTopColor](https://msdn.microsoft.com/library/bb623975\(v=office.15\))

Ces propriétés renvoient une valeur **OLE\_COLOR** qui dépend de la propriété **Color** de l'objet **Category**.

Les éléments Outlook sont présentés en fonction du nom de la catégorie. Chaque élément objet possède une propriété **Category** qui stocke une chaîne séparée par des virgules représentant les noms de catégorie. (Par exemple, pour l'objet [MailItem](https://msdn.microsoft.com/library/bb643865\(v=office.15\)), il convient d'utiliser la propriété **MailItem**[Categories](https://msdn.microsoft.com/library/bb646442\(v=office.15\))). Cela vous permet d’ajouter une catégorie à l’élément, même si la catégorie n’apparaît pas dans la liste principale de catégories.


> [!NOTE]
> Si la propriété **Categories** d'un élément contient un nom de catégorie qui ne figure pas dans la collection **Categories** de l'objet **NameSpace**, le nom de catégorie associé à cet élément Outlook s'affiche, mais sans couleur associée. La propriété **Categories** sur un objet **Item** ne renvoie pas une collection **Categories**.

Dans l'exemple de code suivant, la première procédure, EnumerateCategories, récupère la liste principale de catégories de l'utilisateur actuel, représentée par la collection **Categories**. Elle énumère ensuite les objets **Category** dans cette collection, puis écrit les propriétés **Name** et **CategoryID** des écouteurs de suivi de la collection [Listeners](https://msdn.microsoft.com/library/system.diagnostics.debug.listeners.aspx). La deuxième procédure, AddACategory, récupère la liste principale de catégories de l'utilisateur actuel et utilise la méthode CategoryExists pour vérifier si une catégorie nommée « ISV » existe dans la collection. Si aucune catégorie n'existe sous le nom « ISV », AddACategory ajoute une catégorie nommée « ISV » à la liste principale de catégories et lui affecte la couleur bleu foncé à l'aide de la méthode **Add** de la collection **Categories**. Il désigne également CTRL + F11 comme touche de raccourci pour la catégorie.

```csharp
using Outlook = Microsoft.Office.Interop.Outlook;
```


```csharp
private void EnumerateCategories()
{
    Outlook.Categories categories =
        Application.Session.Categories;
    foreach (Outlook.Category category in categories)
    {
        Debug.WriteLine(category.Name);
        Debug.WriteLine(category.CategoryID);
    }
}

private void AddACategory()
{
    Outlook.Categories categories =
        Application.Session.Categories;
    if (!CategoryExists("ISV"))
    {
        Outlook.Category category = categories.Add("ISV",
            Outlook.OlCategoryColor.olCategoryColorDarkBlue,
            Outlook.OlCategoryShortcutKey.olCategoryShortcutKeyCtrlF11);
    }
}

private bool CategoryExists(string categoryName)
{
    try
    {
        Outlook.Category category = 
            Application.Session.Categories[categoryName];
        if(category != null)
        {
            return true;
        }
        else
        {
            return false;
        }
    }
    catch { return false; }
}
```

## <a name="see-also"></a>Voir aussi

- [Catégories de couleurs](color-categories.md)

