---
title: Field2.Size Property (DAO)
TOCTitle: Size Property
ms:assetid: e252759a-cea9-25cb-667d-80b422fbf97e
ms:mtpsurl: https://msdn.microsoft.com/library/Ff835700(v=office.15)
ms:contentKeyID: 48548282
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: ffca40d22d77a604e4c0b794a8070fb444d44a32
ms.sourcegitcommit: 19aca09c5812cfb98b68b5d4604dcaa814479df7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 10/09/2018
ms.locfileid: "25471594"
---
# <a name="field2size-property-dao"></a>Field2.Size Property (DAO)


**S’applique à**: Access 2013 | Office 2013


Définit ou renvoie une valeur qui indique la taille maximale, en octets, d'un objet **Field2**.

## <a name="syntax"></a>Syntaxe

*expression* . Taille

*expression* Variable qui représente un objet **Field2** .

## <a name="remarks"></a>Remarques

Pour un objet pas encore ajouté à la collection **[Fields](fields-collection-dao.md)**, cette propriété est en lecture/écriture.

Pour les champs (autres que Mémo) contenant des chaînes de caractères, la propriété **Size** indique le nombre de caractères maximal du champ. Pour les champs numériques, la propriété **Size** indique le nombre d'octets de stockage requis.

L'utilisation de la propriété **Size** dépend de l'objet contenant la collection **Fields** à laquelle l'objet **Field2** est ajouté, comme illustré dans le tableau suivant.

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


Lorsque vous créez un objet **Field2** contenant un type de données autre que Texte, le paramètre de propriété **Type** détermine automatiquement le paramètre de propriété **Size**; vous n'avez pas besoin de le définir. En revanche, pour un objet **Field2** contenant des données de type Texte, vous pouvez définir **Size** sur tout entier jusqu'à la taille de texte maximum (255 pour les bases de données de moteur de base de données Microsoft Access). Si vous ne définissez aucune taille, le champ est aussi grand que le permet la base de données.

Pour les objets **Field2** de type Mémo et Binaire long, **Size** est toujours définie sur 0. Utilisez la propriété **FieldSize** de l'objet **Field2** pour déterminer la taille des données d'un enregistrement spécifique. La taille maximale d'un champ Mémo ou Binaire long est limitée uniquement par les ressources de votre système ou la taille maximale autorisée par la base de données.

## <a name="example"></a>Exemple

Cet exemple illustre la propriété **Size** en énumérant les noms et tailles des objets **Field2** de la table Employees.

```vb
    Sub SizeX() 
     
     Dim dbsNorthwind As Database 
     Dim tdfEmployees As TableDef 
     Dim fldNew As Field2 
     Dim fldLoop As Field2 
     
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
