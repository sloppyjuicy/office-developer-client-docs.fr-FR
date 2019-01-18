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
ms.sourcegitcommit: d6695c94415fa47952ee7961a69660abc0904434
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/17/2019
ms.locfileid: "28698707"
---
# <a name="display-selected-items-in-the-active-explorer"></a>Affichage des éléments sélectionnés dans l’Explorateur actif

Cet exemple montre comment utiliser la classe d’assistance OutlookItem pour afficher correctement tous les éléments sélectionnés dans la fenêtre de l’Explorateur actif.

## <a name="example"></a>Exemple

> [!NOTE] 
> L’exemple de code suivant est un extrait de [programmation d’Applications pour Microsoft Office Outlook 2007](https://www.amazon.com/gp/product/0735622493?ie=UTF8&tag=msmsdn-20&linkCode=as2&camp=1789&creative=9325&creativeASIN=0735622493).

L’objet [Selection](https://msdn.microsoft.com/library/bb612099\(v=office.15\)) contient l’ensemble des éléments Outlook sélectionnés dans l’Explorateur Outlook actif. Ni l’Explorateur actif, représenté par [ActiveExplorer()](https://msdn.microsoft.com/library/bb647410\(v=office.15\)), ni l’ensemble des éléments sélectionnés, n’indique le type des éléments sélectionnés. Normalement, il faut d’abord identifier le type d’élément, puis appeler la méthode **Display** spécifique pour ce type. Dans la mesure où la méthode **Display** est commune à tous les objets des éléments Outlook et où la classe d’assistance OutlookItem inclut cette méthode, vous pouvez tirer parti de la classe d’assistance, en déclarant une instance de l’objet OutlookItem, myItem, et en utilisant myItem.Display pour afficher chaque élément de la sélection. Vous pouvez en apprendre plus sur l’implémentation de la classe d’assistance OutlookItem dans l’article [Créer une classe d’assistance pour accéder aux membres d’élément courant Outlook](how-to-create-a-helper-class-to-access-common-outlook-item-members.md)

Si vous utilisez Visual Studio pour tester cet exemple de code, vous devez d’abord ajouter une référence au composant Bibliothèque d’objets Microsoft Outlook 15.0 et spécifier la variable lorsque vous importez l’espace de noms **Microsoft.Office.Interop.Outlook**. L'instruction **d’utilisation** ne doit pas se produire juste avant les fonctions de l'exemple de code, mais doit être ajoutée avant la déclaration publique. La ligne de code suivante montre comment effectuer l’importation et la tâche dans C\#.

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

## <a name="see-also"></a>Voir aussi

- [Créer une classe d’assistance pour accéder aux membres d’élément Outlook courant](how-to-create-a-helper-class-to-access-common-outlook-item-members.md)
- [Éléments Outlook généraux](general-outlook-items.md)

