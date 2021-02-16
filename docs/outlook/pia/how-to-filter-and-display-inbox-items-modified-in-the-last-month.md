---
title: Filtrer et afficher les éléments de boîte de réception modifiés le mois dernier
TOCTitle: Filter and display Inbox items modified in the last month
ms:assetid: ef6004dc-0b5a-4d1f-8937-1384d1dfc1ca
ms:mtpsurl: https://msdn.microsoft.com/library/Ff424482(v=office.15)
ms:contentKeyID: 55119886
ms.date: 07/24/2014
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: 77fe6e7df4cf67ed1ca2d62b8cf48f1b2873ccbe
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32320292"
---
# <a name="filter-and-display-inbox-items-modified-in-the-last-month"></a>Filtrer et afficher les éléments de boîte de réception modifiés le mois dernier

Cet exemple montre comment filtrer et afficher les éléments de boîte de réception qui ont été modifiés le mois dernier.

## <a name="example"></a>Exemple

> [!NOTE] 
> L’exemple de code suivant est un extrait de [programmation d’Applications pour Microsoft Office Outlook 2007](https://www.amazon.com/gp/product/0735622493?ie=UTF8&tag=msmsdn-20&linkCode=as2&camp=1789&creative=9325&creativeASIN=0735622493).

Le langage de requête recherche DAV et localisation (DASL) est basé sur l’implémentation de Microsoft Exchange de DASL dans Outlook. Il peut être utilisé pour renvoyer des résultats en fonction de propriété pour les recherches au niveau élément dans les données de dossier, tels que celui représenté par un [Objet](https://msdn.microsoft.com/library/bb652856\(v=office.15\)) du tableau. Les filtres DASL prennent en charge les comparaisons de chaînes, y compris la correspondance d'équivalence, de préfixe, de phrase et de sous-chaîne, à l'aide de l'opérateur d'égalité (=). Vous pouvez utiliser des requêtes DASL pour effectuer une comparaison de date-heure ainsi qu’un filtrage.

Les requêtes DASL effectuant toujours des comparaisons d'objet **DateTime** en temps UTC (Coordinated Universal Time), vous devez convertir la valeur de l'heure locale en temps UTC si vous voulez que la requête fonctionne correctement. Vous devez aussi convertir la valeur **DateTime** en une représentation sous forme de chaîne car les filtres DASL prennent en charge les comparaisons de chaînes. Vous pouvez effectuer la conversion **DateTime** de deux façons : à l'aide la méthode [LocalTimeToUTC(Object)](https://msdn.microsoft.com/library/bb645832\(v=office.15\)) de l'objet [Row](https://msdn.microsoft.com/library/bb610126\(v=office.15\)) ou à l'aide des macros **DateTime** d'Outlook.

La ligne de code suivante montre comment utiliser la méthode **LocalTimeToUTC** pour convertir la valeur de la propriété **LastModificationTime** (qui est une colonne par défaut dans tous les objets **Item**) en temps UTC.

```csharp
DateTime modified = nextRow.LocalTimeUTC(“LastModificationTime”);
```

Le tableau suivant répertorie les macros **DateTime** que vous pouvez utiliser pour retourner des chaînes filtrées qui comparent la valeur d'une propriété **DateTime** donnée avec une date relative ou une plage de dates spécifiées en temps UTC. La valeur de la propriété SchemaName représente toute propriété **DateTime** valide référencée par espace de noms.

<table>
<colgroup>
<col style="width: 33%" />
<col style="width: 33%" />
<col style="width: 33%" />
</colgroup>
<thead>
<tr class="header">
<th><p>Macro</p></th>
<th><p>Syntaxe</p></th>
<th><p>Description</p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p>aujourd’hui</p></td>
<td><p>% aujourdh’ui("SchemaName") %</p></td>
<td><p>Limite les éléments dont la valeur de propriété SchemaName égale à aujourd'hui.</p></td>
</tr>
<tr class="even">
<td><p>demain</p></td>
<td><p>%demain("SchemaName") %</p></td>
<td><p>Limite les éléments dont la valeur de propriété SchemaName égale à demain.</p></td>
</tr>
<tr class="odd">
<td><p>hier</p></td>
<td><p>%hier("SchemaName") %</p></td>
<td><p>Limite les éléments dont la valeur de propriété SchemaName égale à hier.</p></td>
</tr>
<tr class="even">
<td><p>7prochainsjours</p></td>
<td><p>% 7prochainsjours("SchemaName") %</p></td>
<td><p>Limite aux éléments ayant des valeurs de propriété SchemaName dans une plage équivalente aux sept prochains jours.</p></td>
</tr>
<tr class="odd">
<td><p>7derniersjours</p></td>
<td><p>%7derniersjours("SchemaName") %</p></td>
<td><p>Limite aux éléments ayant des valeurs de propriété SchemaName dans une plage équivalente aux sept derniers jours.</p></td>
</tr>
<tr class="even">
<td><p>semaineprochaine</p></td>
<td><p>% semaineprochaine("SchemaName") %</p></td>
<td><p>Limite aux éléments ayant des valeurs de propriété SchemaName dans une plage équivalente à la semaine prochaine.</p></td>
</tr>
<tr class="odd">
<td><p>semaineencours</p></td>
<td><p>%semaineencours("SchemaName") %</p></td>
<td><p>Limite aux éléments ayant des valeurs de propriété SchemaName dans une plage équivalente à cette semaine.</p></td>
</tr>
<tr class="even">
<td><p>semainedernière</p></td>
<td><p>%semainedernière("SchemaName") %</p></td>
<td><p>Limite aux éléments ayant des valeurs de propriété SchemaName dans une plage équivalente à la semaine dernière.</p></td>
</tr>
<tr class="odd">
<td><p>moisprochain</p></td>
<td><p>%moisprochain("SchemaName") %</p></td>
<td><p>Limite aux éléments ayant des valeurs de propriété SchemaName dans une plage équivalente au mois prochain.</p></td>
</tr>
<tr class="even">
<td><p>moisencours</p></td>
<td><p>%cemois("SchemaName") %</p></td>
<td><p>Limite aux éléments ayant des valeurs de propriété SchemaName dans une plage équivalente au mois en cours.</p></td>
</tr>
<tr class="odd">
<td><p>moisdernier</p></td>
<td><p>%moisdernier("SchemaName") %</p></td>
<td><p>Limite aux éléments ayant des valeurs de propriété SchemaName dans une plage équivalente au mois dernier.</p></td>
</tr>
</tbody>
</table>


Dans l'exemple suivant, DemoDASLDateMacro crée une requête DASL qui utilise la macro **DateTime lastmonth** pour filtrer des éléments de la boîte de réception (Inbox) de l'utilisateur qui ont été modifiés au cours du dernier mois. Il crée ensuite un **objet** du tableau avec ce filtre et énumère et affiche les lignes dans l’**objet** du tableau restreint.

Si vous utilisez Visual Studio pour tester cet exemple de code, vous devez d’abord ajouter une référence au composant Bibliothèque d’objets Microsoft Outlook 15.0 et spécifier la variable lorsque vous importez l’espace de noms **Microsoft.Office.Interop.Outlook**. L’instruction **using** ne doit pas se produire juste avant les fonctions de l’exemple de code, mais doit être ajoutée avant la déclaration publique. Le code suivant illustre l’importation et l’affectation dans C\#.

```csharp
using Outlook = Microsoft.Office.Interop.Outlook;
```


```csharp
private void DemoDASLDateMacro()
{
    string filter = "@SQL=" + "%lastmonth(" + "\"" +
        "DAV:getlastmodified" + "\"" + ")%";
    Outlook.Table table = Application.Session.GetDefaultFolder(
        Outlook.OlDefaultFolders.olFolderInbox).GetTable(
        filter, Outlook.OlTableContents.olUserItems);
    while (!table.EndOfTable)
    {
        Outlook.Row row = table.GetNextRow();
        Debug.WriteLine(row["Subject"]);
    }
}
```

## <a name="see-also"></a>Voir aussi

- [Rechercher et filtrer](search-and-filter.md)

