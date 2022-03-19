---
title: Filtrage et affichage des propriétés à valeurs multiples pendant l’énumération des éléments d’un dossier
TOCTitle: Filter and display multivalued properties when enumerating items in a folder
ms:assetid: 62dd2120-5c85-44b3-89ec-c4ca85aa2964
ms:mtpsurl: https://msdn.microsoft.com/library/Ff184613(v=office.15)
ms:contentKeyID: 55119887
ms.date: 07/24/2014
mtps_version: v=office.15
ms.localizationpriority: medium
ms.openlocfilehash: aef5ebc4e3599fdfd96fc851a289a367b4290765
ms.sourcegitcommit: 241637561d21b7752ec690b5179e72b6703eaced
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/18/2022
ms.locfileid: "63634855"
---
# <a name="filter-and-display-multivalued-properties-when-enumerating-items-in-a-folder"></a>Filtrage et affichage des propriétés à valeurs multiples pendant l’énumération des éléments d’un dossier

Cet exemple montre comment filtrer et afficher des propriétés à valeurs multiples pendant l’énumération d’éléments dans un dossier.

## <a name="example"></a>Exemple

> [!NOTE] 
> L’exemple de code suivant est un extrait de [programmation d’Applications pour Microsoft Office Outlook 2007](https://www.amazon.com/gp/product/0735622493?ie=UTF8&tag=msmsdn-20&linkCode=as2&camp=1789&creative=9325&creativeASIN=0735622493).

L'objet [Table](https://msdn.microsoft.com/library/bb652856\(v=office.15\)) représente un ensemble de données d'éléments issues d'un objet [Folder](https://msdn.microsoft.com/library/bb645774\(v=office.15\)) ou [Search](https://msdn.microsoft.com/library/bb612611\(v=office.15\)) . Lorsqu'une propriété binaire, date ou à valeurs multiples est ajoutée en premier lieu à un objet **Table**, la façon de référencer cette propriété affecte son type et son format. Comme les références des noms intégrés retournent parfois une valeur de colonne différente par rapport à une référence à un espace de noms, vous devez déterminer si la propriété est référencée par son nom intégré explicite (s'il existe) ou par un espace de noms (indépendamment de l'existence d'un nom intégré explicite). Le tableau suivant montre la différence dans la représentation de la valeur d'une propriété (en termes de type et de format) selon le type de la propriété d'origine.

<table>
<colgroup>
<col />
<col />
<col />
</colgroup>
<thead>
<tr class="header">
<th><p>Type</p></th>
<th><p>Type en retour si la propriété spécifiée utilise un nom intégré</p></th>
<th><p>Type de retour si la propriété spécifiée utilise un espace de noms</p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p>Binaire <b>(PT_BINARY)</b></p></td>
<td><p>String</p></td>
<td><p>Tableau d’octets</p></td>
</tr>
<tr class="even">
<td><p>Date <b>(PT_SYSTIME)</b></p></td>
<td><p>Local <b>DateTime</b></p></td>
<td><p>UTC <b>DateTime</b></p></td>
</tr>
<tr class="odd">
<td><p>À valeurs multiples (également appelé type mot clé), comme la propriété <b>Categories</b> <b>(PT_MV_STRING8)</b></p></td>
<td><p>Chaîne qui contient des valeurs séparées par des virgules</p></td>
<td><p>Tableau à une dimension qui contient un élément pour chaque mot clé</p></td>
</tr>
</tbody>
</table>


L'exemple de code suivant montre comment ajouter une propriété d'espace de noms de chaîne MAPI à l'objet **Table** et comment les propriétés à valeurs multiples affectent les valeurs retournées dans un objet [Column](https://msdn.microsoft.com/library/bb609646\(v=office.15\)) . La procédure TableMultiValuedProperties filtre l’objet **Table** pour trouver les lignes où la propriété [Categories](https://msdn.microsoft.com/library/bb646607\(v=office.15\)) n’est pas une référence null. La propriété **Categories** est représentée par une propriété qui utilise l’espace de noms de la chaîne MAPI. Un filtre DASL est construit pour les éléments ayant des catégories (le filtre réel retourne les catégories n'ayant pas une référence null). Une colonne **Categories** est ensuite ajoutée à l’objet **Table** en concaténant le spécificateur de type, 0000001f, avec la constante categoriesProperty. Enfin, l'objet **Column** qui représente la propriété **Categories** contient un tableau unidimensionnel de chaînes où chaque élément représente une catégorie assignée à l'élément. Les propriétés **Categories** et **Subject** de l’élément sont écrites sur les écouteurs de suivi de la collection [Listeners](https://msdn.microsoft.com/library/system.diagnostics.debug.listeners.aspx).

Si vous utilisez Visual Studio pour tester cet exemple de code, vous devez d’abord ajouter une référence au composant Bibliothèque d'objets Microsoft Outlook 15.0 et spécifier la variable Outlook lorsque vous importez l’espace de noms **Microsoft.Office.Interop.Outlook**. L’instruction **using** ne doit pas se produire juste avant les fonctions de l’exemple de code, mais doit être ajoutée avant la déclaration Class publique. La ligne de code suivante montre comment effectuer l’importation et l’affectation dans C \#.

```csharp
using Outlook = Microsoft.Office.Interop.Outlook;
```


```csharp
private void TableMultiValuedProperties()
{
    const string categoriesProperty =
        "http://schemas.microsoft.com/mapi/string/"
        + "{00020329-0000-0000-C000-000000000046}/Keywords";
    // Inbox
    Outlook.Folder folder =
        Application.Session.GetDefaultFolder(
        Outlook.OlDefaultFolders.olFolderInbox)
        as Outlook.Folder;
    // Call GetTable with filter for categories
    string filter = "@SQL="
        + "Not(" + "\"" + categoriesProperty
        + "\"" + " Is Null)";
    Outlook.Table table =
        folder.GetTable(filter,
        Outlook.OlTableContents.olUserItems);
    // Add categories column and append type specifier
    table.Columns.Add(categoriesProperty + "/0000001F");
    while (!table.EndOfTable)
    {
        Outlook.Row nextRow = table.GetNextRow();
        string[] categories =
            (string[])nextRow[categoriesProperty + "/0000001F"];
        Debug.WriteLine("Subject: " + nextRow["Subject"]);
        Debug.Write("Categories: ");
        foreach (string category in categories)
        {
            Debug.Write("\t" + category);
        }
        Debug.WriteLine("\n");
    }
}
```

## <a name="see-also"></a>Voir aussi

- [Rechercher et filtrer](search-and-filter.md)

