---
title: Propriété Field.DataUpdatable (DAO)
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
localization_priority: Normal
ms.openlocfilehash: 8678b825f509f483bf70d3aa2f3d767dbf7b0e32
ms.sourcegitcommit: d6695c94415fa47952ee7961a69660abc0904434
ms.translationtype: Auto
ms.contentlocale: fr-FR
ms.lasthandoff: 01/17/2019
ms.locfileid: "28698280"
---
# <a name="fielddataupdatable-property-dao"></a><span data-ttu-id="0dfdd-102">Propriété Field.DataUpdatable (DAO)</span><span class="sxs-lookup"><span data-stu-id="0dfdd-102">Field.DataUpdatable property (DAO)</span></span>


<span data-ttu-id="0dfdd-103">**S’applique à**: Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="0dfdd-103">**Applies to**: Access 2013, Office 2013</span></span>


<span data-ttu-id="0dfdd-104">Renvoie une valeur qui indique si les données du champ représenté par un objet **[Field](field-object-dao.md)** peuvent être modifiées.</span><span class="sxs-lookup"><span data-stu-id="0dfdd-104">Returns a value that indicates whether the data in the field represented by a **[Field](field-object-dao.md)** object is updatable.</span></span>

## <a name="syntax"></a><span data-ttu-id="0dfdd-105">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="0dfdd-105">Syntax</span></span>

<span data-ttu-id="0dfdd-106">*expression* . DataUpdatable</span><span class="sxs-lookup"><span data-stu-id="0dfdd-106">*expression* .DataUpdatable</span></span>

<span data-ttu-id="0dfdd-107">*expression* Variable qui représente un objet **Field** .</span><span class="sxs-lookup"><span data-stu-id="0dfdd-107">*expression* A variable that represents a **Field** object.</span></span>

## <a name="remarks"></a><span data-ttu-id="0dfdd-108">Remarques</span><span class="sxs-lookup"><span data-stu-id="0dfdd-108">Remarks</span></span>

<span data-ttu-id="0dfdd-p101">Cette propriété vous permet de déterminer si vous pouvez modifier le paramètre de la propriété **[Value](field-value-property-dao.md)** pour un objet **Field**. Elle correspond toujours à la valeur **False** pour un objet **Field** dont la propriété **[Attributes](field-attributes-property-dao.md)** est **dbAutoIncrField**.</span><span class="sxs-lookup"><span data-stu-id="0dfdd-p101">Use this property to determine whether you can change the **[Value](field-value-property-dao.md)** property setting of a **Field** object. This property is always **False** on a **Field** object whose **[Attributes](field-attributes-property-dao.md)** property is **dbAutoIncrField**.</span></span>

<span data-ttu-id="0dfdd-111">Vous pouvez utiliser la propriété **DataUpdatable** sur les objets **Field** ajoutés à la collection **[Fields](fields-collection-dao.md)** des objets **[QueryDef](querydef-object-dao.md)**, **[Recordset](recordset-object-dao.md)** et **[Relation](relation-object-dao.md)**, mais pas à la collection **Fields** de l'objet **[Index](index-object-dao.md)** ou **[TableDef](tabledef-object-dao.md)**.</span><span class="sxs-lookup"><span data-stu-id="0dfdd-111">You can use the **DataUpdatable** property on **Field** objects that are appended to the **[Fields](fields-collection-dao.md)** collection of **[QueryDef](querydef-object-dao.md)**, **[Recordset](recordset-object-dao.md)**, and **[Relation](relation-object-dao.md)** objects, but not the **Fields** collection of **[Index](index-object-dao.md)** or **[TableDef](tabledef-object-dao.md)** objects.</span></span>

## <a name="example"></a><span data-ttu-id="0dfdd-112">Exemple</span><span class="sxs-lookup"><span data-stu-id="0dfdd-112">Example</span></span>

<span data-ttu-id="0dfdd-p102">Cet exemple démontre la propriété **DataUpdatable** utilisant le premier champ de six objets **Recordsets** différents. La fonction DataOutput est indispensable pour l'exécution de cette procédure.</span><span class="sxs-lookup"><span data-stu-id="0dfdd-p102">This example demonstrates the **DataUpdatable** property using the first field from six different **Recordsets**. The DataOutput function is required for this procedure to run.</span></span>

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

