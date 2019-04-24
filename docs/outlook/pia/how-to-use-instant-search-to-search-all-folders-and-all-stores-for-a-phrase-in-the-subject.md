---
title: Utilisation de la recherche instantanée pour rechercher une expression employée dans l’objet dans tous les dossiers et toutes les banques
TOCTitle: Use instant search to search all folders and all stores for a phrase in the subject
ms:assetid: d3152bfa-6e7d-4b68-8c7e-e2e155a92b49
ms:mtpsurl: https://msdn.microsoft.com/library/Ff424478(v=office.15)
ms:contentKeyID: 55119923
ms.date: 07/24/2014
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: 07b0ba7a1d488dc1c7e1fcf0e9ae487b04b88755
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32335370"
---
# <a name="use-instant-search-to-search-all-folders-and-all-stores-for-a-phrase-in-the-subject"></a>Utiliser la recherche instantanée pour effectuer une recherche dans tous les dossiers et tous les magasins pour une expression dans l’objet

Cet exemple utilise la recherche instantanée pour rechercher une phrase dans l'objet à travers tous les dossiers et toutes les banques, puis affiche les éléments dans une fenêtre d'explorateur.

## <a name="example"></a>Exemple

> [!NOTE] 
> L’exemple de code suivant est un extrait de [programmation d’Applications pour Microsoft Office Outlook 2007](https://www.amazon.com/gp/product/0735622493?ie=UTF8&tag=msmsdn-20&linkCode=as2&camp=1789&creative=9325&creativeASIN=0735622493).

La recherche instantanée est une fonctionnalité de Microsoft Outlook qui permet d’effectuer des recherches en émettant des requêtes qui renvoient des résultats en fonction du contenu. Une fois que votre requête a été traitée, les résultats peuvent être retournés dans différents objets, y compris l'objet [Table](https://msdn.microsoft.com/library/bb652856\(v=office.15\)) , la collection [Items](https://msdn.microsoft.com/library/bb645287\(v=office.15\)) et l'objet [Search](https://msdn.microsoft.com/library/bb612611\(v=office.15\)) . Vous pouvez écrire du code qui utilise la recherche instantanée à l'aide de la syntaxe AQS (Advanced Query Syntax), qui est disponible avec Microsoft Windows Desktop Search. AQS est un des trois langages de requête pris en charge par Outlook. Il est puissant, mais limité à la méthode [Search(String, OlSearchScope)](https://msdn.microsoft.com/library/bb610561\(v=office.15\)) de l’objet [Explorer](https://msdn.microsoft.com/library/bb623678\(v=office.15\)). Vous ne pouvez pas utiliser AQS pour fournir une restriction pour des objets **Table** ou **Item**. En outre, les résultats renvoyés par une requête AQS peuvent être affichés uniquement dans l’interface utilisateur Outlook. Le tableau suivant répertorie les trois langages de requête pris en charge par Outlook ; cette rubrique ne montrera cependant que l’utilisation d’AQS.

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p>Langage de requête</p></th>
<th><p>Description</p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p>AQS</p></td>
<td><p>AQS est utilisé par Windows Desktop Search et est le langage de recherche pour la fonction de recherche instantanée dans Outlook.</p></td>
</tr>
<tr class="even">
<td><p>DASL</p></td>
<td><p>Le langage de recherche DASL (DAV Search and Locating) est basé sur l’implémentation Microsoft Exchange de DASL dans Outlook. DASL peut être utilisé pour retourner des résultats dans l’objet <b>Table</b>. </p></td>
</tr>
<tr class="odd">
<td><p>Jet</p></td>
<td><p>Le langage de requête Jet offre un langage de requête simple pour Outlook, et il est basé sur Microsoft Jet Expression Service. Jet est utilisé pour créer des chaînes de filtre pour les méthodes <b>Restrict</b> de la collection <b>Items</b> et l’objet <b>Table</b>.</p></td>
</tr>
</tbody>
</table>


Dans l’exemple de code suivant, DemoInstantSearch obtient tous les dossiers de messagerie électronique de tous les magasins où l’indexation est activée à l’aide de la propriété [IsInstantSearchEnabled](https://msdn.microsoft.com/library/bb609793\(v=office.15\)) de l’objet [Store](https://msdn.microsoft.com/library/bb609139\(v=office.15\)). Il utilise ensuite la méthode **Search** de l’objet **Explorer** pour filtrer tous les éléments qui contiennent la phrase exacte « Office 2007 » dans l’objet et qui ont été reçus au cours du mois dernier. Enfin, les résultats de la recherche sont affichés dans une fenêtre distincte de l’explorateur.

Si vous utilisez Visual Studio pour tester cet exemple de code, vous devez d’abord ajouter une référence au composant Bibliothèque d’objets Microsoft Outlook 15.0 et spécifier la variable lorsque vous importez l’espace de noms **Microsoft.Office.Interop.Outlook**. L’instruction **using** ne doit pas se produire juste avant les fonctions de l’exemple de code, mais doit être ajoutée avant la déclaration publique. Le code suivant illustre l’importation et l’affectation dans C\#.

```csharp
using Outlook = Microsoft.Office.Interop.Outlook;
```


```csharp
private void DemoInstantSearch()
{
    if (Application.Session.DefaultStore.IsInstantSearchEnabled)
    {
        Outlook.Explorer explorer = Application.Explorers.Add(
            Application.Session.GetDefaultFolder(
            Outlook.OlDefaultFolders.olFolderInbox)
            as Outlook.Folder,
            Outlook.OlFolderDisplayMode.olFolderDisplayNormal);
        string filter = "subject:" +
            "\"" + "Office 2007" + "\"" +
            " received:(last month)";
        explorer.Search(filter,
            Outlook.OlSearchScope.olSearchScopeAllFolders);
        explorer.Display();
    }
}
```

## <a name="see-also"></a>Voir aussi

- [Rechercher et filtrer](search-and-filter.md)

