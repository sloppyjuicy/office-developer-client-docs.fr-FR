---
title: 'Field Object : DAO (Data Access Objects)'
TOCTitle: Field Object
ms:assetid: 47282ce2-9b49-ccf9-ad37-c4bb25cfd037
ms:mtpsurl: https://msdn.microsoft.com/library/Ff193203(v=office.15)
ms:contentKeyID: 48544587
ms.date: 09/18/2015
mtps_version: v=office.15
localization_priority: Priority
ms.openlocfilehash: c58896fb0d0a5c5a28844fdd3a6df922dd587f32
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: HT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32293041"
---
# <a name="field-object-dao"></a>Field Object (DAO)

**S’applique à** : Access 2013, Office 2013

Un objet **Field** représente une colonne de données avec un type de données courantes et un ensemble commun de propriétés.

## <a name="remarks"></a>Remarques

Les collections **Fields** des objets **Index**, **QueryDef**, **Relation** et **TableDef** contiennent les spécifications pour les champs que représentent ces objets. La collection **Fields** d'un objet **Recordset** représente les objets **Field** sur une ligne de données ou dans un enregistrement. Vous utilisez les objets **Field** dans un objet **Recordset** pour lire et définir des valeurs pour les champs dans l'enregistrement actuel de l'objet **Recordset**.

Dans un espace de travail Microsoft Access, vous manipulez un champ à l'aide d'un objet **Field** et de ses méthodes et propriétés. Par exemple, vous pouvez :

  - Utiliser la propriété **OrdinalPosition** pour définir ou renvoyer l'ordre de présentation de l'objet **Field** dans une collection **Fields**.

  - Utiliser la propriété **Value** d'un champ dans un objet **Recordset** pour définir ou renvoyer les données stockées.

  - Utiliser les méthodes **AppendChunk** et **GetChunk** et la propriété **FieldSize** pour obtenir ou définir une valeur dans un champ Objet OLE ou Mémo d'un objet **Recordset**.

  - Utiliser les propriétés **Type**, **Size** et **Attributes** pour déterminer le type de données qui peut être stocké dans le champ.

  - Utiliser les propriétés **SourceField** et **SourceTable** pour déterminer la source originale des données.

  - Utiliser la propriété **ForeignName** pour définir ou renvoyer des informations sur un champ externe dans un objet **Relation**.

  - Utiliser les propriétés **AllowZeroLength**, **DefaultValue**, **Required**, **ValidateOnSet**, **ValidationRule** ou **ValidationText** pour définir ou renvoyer les conditions de validation.

  - Utiliser la propriété **DefaultValue** d'un champ dans un objet **TableDef** pour définir la valeur par défaut pour ce champ lorsque de nouveaux enregistrements sont ajoutés.

Pour créer un objet **Field** dans un objet **Index**, **TableDef** ou **Relation**, utilisez la méthode **CreateField**.

Lorsque vous accédez à un objet **Field** dans le cadre d'un objet **Recordset**, les données de l'enregistrement actif sont affichées dans la propriété **Value** de l'objet **Field**. Pour manipuler les données dans l'objet **Recordset**, vous ne référencez généralement pas directement la collection **Fields**. Au lieu de cela, vous référencez indirectement la propriété **Value** de l'objet **Field** dans la collection **Fields** de l'objet **Recordset**.

Pour faire référence à un objet **Field** dans une collection par son numéro ordinal ou par son paramètre de propriété **Name**Name, utilisez l'une formes de syntaxe suivantes :

- **Fields**(0)

- **Fields**("nom")

- **Fields**\!\[nom\]

Avec les mêmes formes de syntaxe, vous pouvez également renvoyer à la propriété **Value** d'un objet **Field** que vous créez et ajoutez à une collection **Fields**. Le contexte de la référence de champ détermine si vous faites référence à l'objet **Field** ou à la propriété **Value** de l'objet **Field**.

## <a name="example"></a>Exemple

Cet exemple indique les propriétés valides pour un objet **Field** en fonction de l'emplacement de l'objet **Field** (par exemple, la collection **Fields** d'un objet **TableDef**, la collection **Fields** d'un objet **QueryDef**, etc.). La procédure FieldOutput est nécessaire à l'exécution de cette procédure.

```vb
    Sub FieldX() 
     
     Dim dbsNorthwind As Database 
     Dim rstEmployees As Recordset 
     Dim fldTableDef As Field 
     Dim fldQueryDef As Field 
     Dim fldRecordset As Field 
     Dim fldRelation As Field 
     Dim fldIndex As Field 
     Dim prpLoop As Property 
     
     Set dbsNorthwind = OpenDatabase("Northwind.mdb") 
     Set rstEmployees = _ 
     dbsNorthwind.OpenRecordset("Employees") 
     
     ' Assign a Field object from different Fields 
     ' collections to object variables. 
     Set fldTableDef = _ 
     dbsNorthwind.TableDefs(0).Fields(0) 
     Set fldQueryDef =dbsNorthwind.QueryDefs(0).Fields(0) 
     Set fldRecordset = rstEmployees.Fields(0) 
     Set fldRelation =dbsNorthwind.Relations(0).Fields(0) 
     Set fldIndex = _ 
     dbsNorthwind.TableDefs(0).Indexes(0).Fields(0) 
     
     ' Print report. 
     FieldOutput "TableDef", fldTableDef 
     FieldOutput "QueryDef", fldQueryDef 
     FieldOutput "Recordset", fldRecordset 
     FieldOutput "Relation", fldRelation 
     FieldOutput "Index", fldIndex 
     
     rstEmployees.Close 
     dbsNorthwind.Close 
     
    End Sub 
     
    Sub FieldOutput(strTemp As String, fldTemp As Field) 
     ' Report function for FieldX. 
     
     Dim prpLoop As Property 
     
     Debug.Print "Valid Field properties in " & strTemp 
     
     ' Enumerate Properties collection of passed Field 
     ' object. 
     For Each prpLoop In fldTemp.Properties 
     ' Some properties are invalid in certain 
     ' contexts (the Value property in the Fields 
     ' collection of a TableDef for example). Any 
     ' attempt to use an invalid property will 
     ' trigger an error. 
     On Error Resume Next 
     Debug.Print " " & prpLoop.Name & " = " & _ 
     prpLoop.Value 
     On Error GoTo 0 
     Next prpLoop 
     
    End Sub 
```

<br/>

Cet exemple utilise la méthode **CreateField** pour créer trois objets **Fields** pour un objet **TableDef**. Il affiche ensuite les propriétés de ces objets **Field**, qui sont automatiquement définies par la méthode **CreateField** (les propriétés dont les valeurs sont vides lors de la création de **Field** ne sont pas affichées).

```vb
    Sub CreateFieldX() 
     
     Dim dbsNorthwind As Database 
     Dim tdfNew As TableDef 
     Dim fldLoop As Field 
     Dim prpLoop As Property 
     
     Set dbsNorthwind = OpenDatabase("Northwind.mdb") 
     
     Set tdfNew = dbsNorthwind.CreateTableDef("NewTableDef") 
     
     ' Create and append new Field objects for the new 
     ' TableDef object. 
     With tdfNew 
     ' The CreateField method will set a default Size 
     ' for a new Field object if one is not specified. 
     .Fields.Append .CreateField("TextField", dbText) 
     .Fields.Append .CreateField("IntegerField", dbInteger) 
     .Fields.Append .CreateField("DateField", dbDate) 
     End With 
     
     dbsNorthwind.TableDefs.Append tdfNew 
     
     Debug.Print "Properties of new Fields in " & tdfNew.Name 
     
     ' Enumerate Fields collection to show the properties of 
     ' the new Field objects. 
     For Each fldLoop In tdfNew.Fields 
     Debug.Print " " & fldLoop.Name 
     
     For Each prpLoop In fldLoop.Properties 
     ' Properties that are invalid in the context of 
     ' TableDefs will trigger an error if an attempt 
     ' is made to read their values. 
     On Error Resume Next 
     Debug.Print " " & prpLoop.Name & " - " & _ 
     IIf(prpLoop = "", "[empty]", prpLoop) 
     On Error GoTo 0 
     Next prpLoop 
     
     Next fldLoop 
     
     ' Delete new TableDef because this is a demonstration. 
     dbsNorthwind.TableDefs.Delete tdfNew.Name 
     dbsNorthwind.Close 
     
    End Sub
```
