---
title: Field.OrdinalPosition, propriété (DAO)
TOCTitle: OrdinalPosition Property
ms:assetid: 07f2344e-2a72-33d8-be47-b37d76ecca47
ms:mtpsurl: https://msdn.microsoft.com/library/Ff845002(v=office.15)
ms:contentKeyID: 48543088
ms.date: 09/18/2015
mtps_version: v=office.15
ms.localizationpriority: medium
ms.openlocfilehash: 1a709b8c9f138be50b71911854a05af69e6bbf50
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/24/2021
ms.locfileid: "59622346"
---
# <a name="fieldordinalposition-property-dao"></a>Field.OrdinalPosition, propriété (DAO)


**S’applique à** : Access 2013, Office 2013

Définit ou renvoie la position relative d'un objet **[Field](field-object-dao.md)** au sein d'une collection **[Fields](fields-collection-dao.md)**.

## <a name="syntax"></a>Syntaxe

*.* OrdinalPosition

*expression* Variable qui représente un objet **Field**.

## <a name="remarks"></a>Remarques

Pour un objet pas encore ajouté à la collection **Fields**, cette propriété est en lecture/écriture.

La valeur par défaut est 0.

La disponibilité de la propriété **OrdinalPosition** dépend de l'objet contenant la collection **Fields**, comme illustré dans le tableau suivant.

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p>Si la collection Fields appartient à un</p></th>
<th><p>Alors OrdinalPosition est</p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p>objet <strong>Index</strong></p></td>
<td><p>Non reconnu</p></td>
</tr>
<tr class="even">
<td><p>objet <strong>QueryDef</strong></p></td>
<td><p>Lecture seule</p></td>
</tr>
<tr class="odd">
<td><p>objet <strong>Recordset</strong></p></td>
<td><p>Lecture seule</p></td>
</tr>
<tr class="even">
<td><p>objet <strong>Relation</strong></p></td>
<td><p>Non pris en charge</p></td>
</tr>
<tr class="odd">
<td><p>objet <strong>TableDef</strong></p></td>
<td><p>Lecture/écriture</p></td>
</tr>
</tbody>
</table>


En règle générale, la position ordinale d'un objet ajouté à une collection dépend de l'ordre dans lequel vous ajoutez l'objet. Le premier objet est ajouté a la première position (0), le second à la seconde position (1) et ainsi de suite. Le dernier objet ajouté se trouve à la position ordinale : 1, où nombre est le nombre d’objets dans la collection, tel que spécifié par le paramètre de propriété **[Count.](containers-count-property-dao.md)**

La propriété **OrdinalPosition** vous permet de spécifier une position ordinale pour les nouveaux objets **Field** qui diffère de l'ordre dans lequel vous les ajoutez à une collection. Ceci vous permet de spécifier un ordre de champs pour vos tables, requêtes et jeux d'enregistrements lorsque vous les utilisez dans une application. Par exemple, l’ordre dans lequel les champs sont renvoyés dans une requête SELECT est déterminé par les valeurs actuelles de la \* **propriété OrdinalPosition.**

Vous pouvez à tout moment redéfinir l'ordre de renvoi des champs dans les jeux d'enregistrements en définissant la propriété **OrdinalPosition** sur tout entier positif.

Deux champs **Field** ou plus peuvent avoir la même valeur de propriété **OrdinalPosition**, auquel cas ils sont classés par ordre alphabétique. Par exemple, si vous avez un champ appelé Age défini sur 4 et un second champ appelé Poids sur 4, Poids est renvoyé après Age.

Vous pouvez spécifier un nombre supérieur au nombre de champs moins 1. Le champ est renvoyé dans un ordre relatif au nombre le plus élevé. Par exemple, si vous définissez la propriété **OrdinalPosition** d'un champ sur 20 (et qu'il n'y a que 5 champs) et si vous avez défini la propriété **OrdinalPosition** des deux autres champs sur 10 et 30, respectivement, le champ défini sur 20 est renvoyé entre les champs définis sur 10 et 30.

> [!NOTE]
> [!REMARQUE] Même si la collection **Fields** d'un objet [TableDef](tabledef-object-dao.md) n'a pas été rafraîchie, l'ordre des champs dans un objet [Recordset](recordset-object-dao.md) ouvert à partir de l'objet **TableDef** reflète les données **OrdinalPosition** de l'objet **TableDef**. Un objet **Recordset** de type table a les mêmes données **OrdinalPosition** en tant que table sous-jacente, mais tout autre type d'objet **Recordset** a des nouvelles données **OrdinalPosition** (commençant par 0) qui suivent l'ordre déterminé par les données **OrdinalPosition** de l'objet **TableDef**.

## <a name="example"></a>Exemple

Cet exemple modifie les valeurs de propriété **OrdinalPosition** de la **TableDef** Employees afin de contrôler l'ordre des **Field** du **Recordset** résultant. En définissant la **OrdinalPosition** de tous les **Fields** sur 1, tous les **Fields** des **Recordset** résultants sont classés par ordre alphabétique. Notez que les valeurs **OrdinalPosition** du **Recordset** ne correspondent pas à celles de la **TableDef**, mais reflètent simplement le résultat final des modifications de **TableDef**.

```vb
    Sub OrdinalPositionX() 
     
     Dim dbsNorthwind As Database 
     Dim tdfEmployees As TableDef 
     Dim aintPosition() As Integer 
     Dim astrFieldName() As String 
     Dim intTemp As Integer 
     Dim fldTemp As Field 
     Dim rstEmployees As Recordset 
     
     Set dbsNorthwind = OpenDatabase("Northwind.mdb") 
     Set tdfEmployees = dbsNorthwind.TableDefs("Employees") 
     
     With tdfEmployees 
     ' Display and store original OrdinalPosition data. 
     Debug.Print _ 
     "Original OrdinalPosition data in TableDef." 
     ReDim aintPosition(0 To .Fields.Count - 1) As Integer 
     ReDim astrFieldName(0 To .Fields.Count - 1) As String 
     For intTemp = 0 To .Fields.Count - 1 
     aintPosition(intTemp) = _ 
     .Fields(intTemp).OrdinalPosition 
     astrFieldName(intTemp) = .Fields(intTemp).Name 
     Debug.Print , aintPosition(intTemp), _ 
     astrFieldName(intTemp) 
     Next intTemp 
     
     ' Change OrdinalPosition data. 
     For Each fldTemp In .Fields 
     fldTemp.OrdinalPosition = 1 
     Next fldTemp 
     
     ' Open new Recordset object to show how the 
     ' OrdinalPosition data has affected the record order. 
     Debug.Print _ 
     "OrdinalPosition data from resulting Recordset." 
     Set rstEmployees = dbsNorthwind.OpenRecordset( _ 
     "SELECT * FROM Employees") 
     For Each fldTemp In rstEmployees.Fields 
     Debug.Print , fldTemp.OrdinalPosition, fldTemp.Name 
     Next fldTemp 
     rstEmployees.Close 
     
     ' Restore original OrdinalPosition data because this is 
     ' a demonstration. 
     For intTemp = 0 To .Fields.Count - 1 
     .Fields(astrFieldName(intTemp)).OrdinalPosition = _ 
     aintPosition(intTemp) 
     Next intTemp 
     
     End With 
     
     dbsNorthwind.Close 
     
    End Sub
```
