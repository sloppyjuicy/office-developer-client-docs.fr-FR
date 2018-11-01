---
title: Field.Size Property (DAO)
TOCTitle: Size Property
ms:assetid: 15e25201-87b6-f62f-ff18-259414a47891
ms:mtpsurl: https://msdn.microsoft.com/library/Ff845510(v=office.15)
ms:contentKeyID: 48543419
ms.date: 09/18/2015
mtps_version: v=office.15
f1_keywords:
- dao360.chm1052878
f1_categories:
- Office.Version=v15
ms.openlocfilehash: 53a76c26bca9d36b853c7aa6b0620788389cb765
ms.sourcegitcommit: c557bbcccf37a6011f89aae1ddd399dfe549d087
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 10/31/2018
ms.locfileid: "25886486"
---
# <a name="fieldsize-property-dao"></a>Field.Size Property (DAO)


**S’applique à**: Access 2013, Office 2013


Définit ou renvoie une valeur indiquant la taille maximale, en octets, d'un objet **[Field](field-object-dao.md)**.

## <a name="syntax"></a>Syntaxe

*expression* . Taille

*expression* Variable qui représente un objet **Field** .

## <a name="remarks"></a>Remarques

Pour un objet pas encore ajouté à la collection **[Fields](fields-collection-dao.md)**, cette propriété est en lecture/écriture.

Pour les champs (autres que les champs de type Mémo) qui contiennent des caractères, la propriété **Size** indique le nombre maximal de caractères que le champ peut contenir. Dans le cas de champs numériques, la propriété **Size** indique le nombre d'octets de stockage requis.

L'utilisation de la propriété **Size** dépend de l'objet qui contient la collection **Fields** à laquelle l'objet **Field** est ajouté, comme l'illustre le tableau suivant.

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p>Objet ajouté à</p></th>
<th><p>Utilisation</p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><strong>Index</strong></p></td>
<td><p>Non pris en charge</p></td>
</tr>
<tr class="even">
<td><p><strong>Objet QueryDef</strong></p></td>
<td><p>Lecture seule</p></td>
</tr>
<tr class="odd">
<td><p><strong>Recordset</strong></p></td>
<td><p>Lecture seule</p></td>
</tr>
<tr class="even">
<td><p><strong>Relation</strong></p></td>
<td><p>Non pris en charge</p></td>
</tr>
<tr class="odd">
<td><p><strong>TableDef</strong></p></td>
<td><p>Lecture seule</p></td>
</tr>
</tbody>
</table>


Lorsque vous créez un objet **Field** avec un type de données autre que Texte, le paramètre de la propriété **[Type](field-type-property-dao.md)** détermine automatiquement le paramètre de la propriété **Size**; vous n'avez pas besoin de la définir. Dans le cas d'un objet **Field** de type Texte, en revanche, vous pouvez définir pour la propriété **Size** un entier dont la valeur maximale correspond à la taille de texte maximale (255 pour les bases de données Microsoft Access). Si vous ne définissez pas la taille, le champ sera aussi grand que ne l'autorise la base de données.

Pour les objets **Field** de type Binaire long et Mémo, **Size** a toujours la valeur 0. Utilisez la propriété **[FieldSize](field-fieldsize-property-dao.md)** de l'objet **Field** pour déterminer la taille des données dans un enregistrement spécifique. La taille maximale d'un champ de type Binaire long et Mémo est uniquement limitée par vos ressources système ou la taille maximale autorisée par la base de données.

## <a name="example"></a>Exemple

Cet exemple illustre la propriété **Size** en énumérant les noms et les tailles des objets **Field** dans la table Employees (Employés).

```vb
    Sub SizeX() 
     
     Dim dbsNorthwind As Database 
     Dim tdfEmployees As TableDef 
     Dim fldNew As Field 
     Dim fldLoop As Field 
     
     Set dbsNorthwind = OpenDatabase("Northwind.mdb") 
     Set tdfEmployees = dbsNorthwind.TableDefs!Employees 
     
     With tdfEmployees 
     
     ' Create and append a new Field object to the 
     ' Employees table. 
     Set fldNew = .CreateField("FaxPhone") 
     fldNew.Type = dbText 
     fldNew.Size = 20 
     .Fields.Append fldNew 
     
     Debug.Print "TableDef: " & .Name 
     Debug.Print " Field.Name - Field.Type - Field.Size" 
     
     ' Enumerate Fields collection; print field names, 
     ' types, and sizes. 
     For Each fldLoop In .Fields 
     Debug.Print " " & fldLoop.Name & " - " & _ 
     fldLoop.Type & " - " & fldLoop.Size 
     Next fldLoop 
     
     ' Delete new field because this is a demonstration. 
     .Fields.Delete fldNew.Name 
     
     End With 
     
     dbsNorthwind.Close 
     
    End Sub
```
