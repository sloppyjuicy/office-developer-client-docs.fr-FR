---
title: Field.DataUpdatable Property (DAO)
TOCTitle: DataUpdatable Property
ms:assetid: 08ca57b6-2d7c-36b4-7d51-b76ac5467163
ms:mtpsurl: https://msdn.microsoft.com/library/Ff845029(v=office.15)
ms:contentKeyID: 48543104
ms.date: 09/18/2015
mtps_version: v=office.15
f1_keywords:
- dao360.chm1052988
f1_categories:
- Office.Version=v15
ms.openlocfilehash: 6993baffbff17da762932c137693ae53c169135d
ms.sourcegitcommit: 19aca09c5812cfb98b68b5d4604dcaa814479df7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 10/09/2018
ms.locfileid: "25469744"
---
# <a name="fielddataupdatable-property-dao"></a>Field.DataUpdatable Property (DAO)


**S’applique à**: Access 2013 | Office 2013


Renvoie une valeur qui indique si les données du champ représenté par un objet **[Field](field-object-dao.md)** peuvent être modifiées.

## <a name="syntax"></a>Syntaxe

*expression* . DataUpdatable

*expression* Variable qui représente un objet **Field** .

## <a name="remarks"></a>Remarques

Cette propriété vous permet de déterminer si vous pouvez modifier le paramètre de la propriété **[Value](field-value-property-dao.md)** pour un objet **Field**. Elle correspond toujours à la valeur **False** pour un objet **Field** dont la propriété **[Attributes](field-attributes-property-dao.md)** est **dbAutoIncrField**.

Vous pouvez utiliser la propriété **DataUpdatable** sur les objets **Field** ajoutés à la collection **[Fields](fields-collection-dao.md)** des objets **[QueryDef](querydef-object-dao.md)**, **[Recordset](recordset-object-dao.md)** et **[Relation](relation-object-dao.md)**, mais pas à la collection **Fields** de l'objet **[Index](index-object-dao.md)** ou **[TableDef](tabledef-object-dao.md)**.

## <a name="example"></a>Exemple

Cet exemple démontre la propriété **DataUpdatable** utilisant le premier champ de six objets **Recordsets** différents. La fonction DataOutput est indispensable pour l'exécution de cette procédure.

```vb 
Sub DataUpdatableX() 
 
 Dim dbsNorthwind As Database 
 Dim rstNorthwind As Recordset 
 
 Set dbsNorthwind = OpenDatabase("Northwind.mdb") 
 
 With dbsNorthwind 
 ' Open and print report about a table-type Recordset. 
 Set rstNorthwind = .OpenRecordset("Employees") 
 DataOutput rstNorthwind 
 
 ' Open and print report about a dynaset-type Recordset. 
 Set rstNorthwind = .OpenRecordset("Employees", _ 
 dbOpenDynaset) 
 DataOutput rstNorthwind 
 
 ' Open and print report about a snapshot-type Recordset. 
 Set rstNorthwind = .OpenRecordset("Employees", _ 
 dbOpenSnapshot) 
 DataOutput rstNorthwind 
 
 ' Open and print report about a forward-only-type Recordset. 
 Set rstNorthwind = .OpenRecordset("Employees", _ 
 dbOpenForwardOnly) 
 DataOutput rstNorthwind 
 
 ' Open and print report about a Recordset based on 
 ' a select query. 
 Set rstNorthwind = _ 
 .OpenRecordset("Current Product List") 
 DataOutput rstNorthwind 
 
 ' Open and print report about a Recordset based on a 
 ' select query that calculates totals. 
 Set rstNorthwind = .OpenRecordset("Order Subtotals") 
 DataOutput rstNorthwind 
 
 .Close 
 End With 
 
End Sub 
 
Function DataOutput(rstTemp As Recordset) 
 
 With rstTemp 
 Debug.Print "Recordset: " & .Name & ", "; 
 Select Case .Type 
 Case dbOpenTable 
 Debug.Print "dbOpenTable" 
 Case dbOpenDynaset 
 Debug.Print "dbOpenDynaset" 
 Case dbOpenSnapshot 
 Debug.Print "dbOpenSnapshot" 
 Case dbOpenForwardOnly 
 Debug.Print "dbOpenForwardOnly" 
 End Select 
 Debug.Print " Field: " & .Fields(0).Name & ", " & _ 
 "DataUpdatable = " & .Fields(0).DataUpdatable 
 Debug.Print 
 .Close 
 End With 
 
End Function 
 
```

