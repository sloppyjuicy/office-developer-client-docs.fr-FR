---
title: Collection Fields (DAO)
TOCTitle: Fields Collection
ms:assetid: 4be3ba07-20c1-d958-c1b8-7dd8b4731f60
ms:mtpsurl: https://msdn.microsoft.com/library/Ff193530(v=office.15)
ms:contentKeyID: 48544702
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: 79515c413918bca1b83d18abec41c78f3fd52447
ms.sourcegitcommit: d7248f803002b31cf7fc561b03530199a9b0a8fd
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 11/02/2018
ms.locfileid: "25921237"
---
# <a name="fields-collection-dao"></a>Collection Fields (DAO)


**S’applique à**: Access 2013, Office 2013

Une collection **Fields** contient tous les objets **Field** stockés d'un objet **Index**, **QueryDef**, **Recordset**, **Relation** ou **TableDef**.

## <a name="remarks"></a>Remarques

Les collections **Fields** des objets **Index**, **QueryDef**, **Relation** et **TableDef** contiennent les spécifications pour les champs que représentent ces objets. La collection **Fields** d'un objet **Recordset** représente les objets **Field** sur une ligne de données ou dans un enregistrement. Vous utilisez les objets **Field** dans un objet **Recordset** pour lire et définir des valeurs pour les champs dans l'enregistrement actuel de l'objet **Recordset**.

Pour faire référence à un objet **Field** dans une collection par son numéro ordinal ou par son paramètre de propriété **Name**Name, utilisez l'une formes de syntaxe suivantes :

**Fields**(0)

**Champs** (« nom »)

**Champs**\!\[nom\]

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

Cet exemple utilise la méthode **CreateField** pour créer trois objets **Fields** pour un objet **TableDef**. Il affiche ensuite les propriétés de ces objets **Field**, qui sont automatiquement définies par la méthode **CreateField**. (Les propriétés dont les valeurs sont vides lors de la création de **Field** ne sont pas affichées.)

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
