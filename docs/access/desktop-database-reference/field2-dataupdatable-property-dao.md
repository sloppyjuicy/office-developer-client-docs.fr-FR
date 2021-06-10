---
title: Field2.DataUpdatable, propriété (DAO)
TOCTitle: DataUpdatable Property
ms:assetid: e6619c4e-26b1-777b-f0de-78fed3dbc890
ms:mtpsurl: https://msdn.microsoft.com/library/Ff835966(v=office.15)
ms:contentKeyID: 48548377
ms.date: 09/18/2015
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: 88a57ff2daeaaaab202daad55f01eebc6bdf86dd
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32292838"
---
# <a name="field2dataupdatable-property-dao"></a><span data-ttu-id="eb597-102">Field2.DataUpdatable, propriété (DAO)</span><span class="sxs-lookup"><span data-stu-id="eb597-102">Field2.DataUpdatable property (DAO)</span></span>


<span data-ttu-id="eb597-103">**S’applique à** : Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="eb597-103">**Applies to**: Access 2013, Office 2013</span></span>


<span data-ttu-id="eb597-104">Renvoie une donnée indiquant si la donnée du champ représenté par un objet **Field2** peut être mise à jour.</span><span class="sxs-lookup"><span data-stu-id="eb597-104">Returns a value that indicates whether the data in the field represented by a **Field2** object is updatable.</span></span>

## <a name="syntax"></a><span data-ttu-id="eb597-105">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="eb597-105">Syntax</span></span>

<span data-ttu-id="eb597-106">*.* DataUpdatable</span><span class="sxs-lookup"><span data-stu-id="eb597-106">*expression* .DataUpdatable</span></span>

<span data-ttu-id="eb597-107">*expression* une variable qui représente une **champ2** objet.</span><span class="sxs-lookup"><span data-stu-id="eb597-107">*expression* A variable that represents a **Field2** object.</span></span>

## <a name="remarks"></a><span data-ttu-id="eb597-108">Remarques</span><span class="sxs-lookup"><span data-stu-id="eb597-108">Remarks</span></span>

<span data-ttu-id="eb597-p101">Cette propriété permet de déterminer si vous pouvez modifier le paramètre de propriété **[Value](field-value-property-dao.md)** d'un objet **Field2**. Cette propriété est toujours **False** sur un objet **Field2** dont la propriété **[Attributes](field-attributes-property-dao.md)** est **dbAutoIncrField**.</span><span class="sxs-lookup"><span data-stu-id="eb597-p101">Use this property to determine whether you can change the **[Value](field-value-property-dao.md)** property setting of a **Field2** object. This property is always **False** on a **Field2** object whose **[Attributes](field-attributes-property-dao.md)** property is **dbAutoIncrField**.</span></span>

<span data-ttu-id="eb597-111">Vous pouvez utiliser la propriété **DataUpdatable** sur des objets **Field2** ajoutés à la collection **[Fields](fields-collection-dao.md)** des objets **[QueryDef](querydef-object-dao.md)**, **[Recordset](recordset-object-dao.md)** et **[Relation](relation-object-dao.md)**, mais pas à la collection **Fields** des objets **[Index](index-object-dao.md)** ou **[TableDef](tabledef-object-dao.md)**.</span><span class="sxs-lookup"><span data-stu-id="eb597-111">You can use the **DataUpdatable** property on **Field2** objects that are appended to the **[Fields](fields-collection-dao.md)** collection of **[QueryDef](querydef-object-dao.md)**, **[Recordset](recordset-object-dao.md)**, and **[Relation](relation-object-dao.md)** objects, but not the **Fields** collection of **[Index](index-object-dao.md)** or **[TableDef](tabledef-object-dao.md)** objects.</span></span>

## <a name="example"></a><span data-ttu-id="eb597-112">Exemple</span><span class="sxs-lookup"><span data-stu-id="eb597-112">Example</span></span>

<span data-ttu-id="eb597-p102">Cet exemple démontre la propriété **DataUpdatable** utilisant le premier champ de six objets **Recordsets** différents. La fonction DataOutput est indispensable pour l'exécution de cette procédure.</span><span class="sxs-lookup"><span data-stu-id="eb597-p102">This example demonstrates the **DataUpdatable** property using the first field from six different **Recordsets**. The DataOutput function is required for this procedure to run.</span></span>

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

