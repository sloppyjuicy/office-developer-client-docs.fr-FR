---
title: Fields Collection (DAO)
TOCTitle: Fields Collection
ms:assetid: 4be3ba07-20c1-d958-c1b8-7dd8b4731f60
ms:mtpsurl: https://msdn.microsoft.com/library/Ff193530(v=office.15)
ms:contentKeyID: 48544702
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: 94c8ec6dd4493a717feb7a6f5d7402df624e9184
ms.sourcegitcommit: c557bbcccf37a6011f89aae1ddd399dfe549d087
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 10/31/2018
ms.locfileid: "25882440"
---
# <a name="fields-collection-dao"></a><span data-ttu-id="f80a2-102">Fields Collection (DAO)</span><span class="sxs-lookup"><span data-stu-id="f80a2-102">Fields Collection (DAO)</span></span>


<span data-ttu-id="f80a2-103">**S’applique à**: Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="f80a2-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="f80a2-104">Une collection **Fields** contient tous les objets **Field** stockés d'un objet **Index**, **QueryDef**, **Recordset**, **Relation** ou **TableDef**.</span><span class="sxs-lookup"><span data-stu-id="f80a2-104">A **Fields** collection contains all stored **Field** objects of an **Index**, **QueryDef**, **Recordset**, **Relation**, or **TableDef** object.</span></span>

## <a name="remarks"></a><span data-ttu-id="f80a2-105">Remarques</span><span class="sxs-lookup"><span data-stu-id="f80a2-105">Remarks</span></span>

<span data-ttu-id="f80a2-p101">Les collections **Fields** des objets **Index**, **QueryDef**, **Relation** et **TableDef** contiennent les spécifications pour les champs que représentent ces objets. La collection **Fields** d'un objet **Recordset** représente les objets **Field** sur une ligne de données ou dans un enregistrement. Vous utilisez les objets **Field** dans un objet **Recordset** pour lire et définir des valeurs pour les champs dans l'enregistrement actuel de l'objet **Recordset**.</span><span class="sxs-lookup"><span data-stu-id="f80a2-p101">The **Fields** collections of the **Index**, **QueryDef**, **Relation**, and **TableDef** objects contain the specifications for the fields those objects represent. The **Fields** collection of a **Recordset** object represents the **Field** objects in a row of data, or in a record. You use the **Field** objects in a **Recordset** object to read and to set values for the fields in the current record of the **Recordset** object.</span></span>

<span data-ttu-id="f80a2-109">Pour faire référence à un objet **Field** dans une collection par son numéro ordinal ou par son paramètre de propriété **Name**Name, utilisez l'une formes de syntaxe suivantes :</span><span class="sxs-lookup"><span data-stu-id="f80a2-109">To refer to a **Field** object in a collection by its ordinal number or by its **Name** property setting, use any of the following syntax forms:</span></span>

<span data-ttu-id="f80a2-110">**Fields**(0)</span><span class="sxs-lookup"><span data-stu-id="f80a2-110">**Fields**(0)</span></span>

<span data-ttu-id="f80a2-111">**Champs** (« nom »)</span><span class="sxs-lookup"><span data-stu-id="f80a2-111">**Fields**("name")</span></span>

<span data-ttu-id="f80a2-112">**Champs**\!\[nom\]</span><span class="sxs-lookup"><span data-stu-id="f80a2-112">**Fields**\!\[name\]</span></span>

<span data-ttu-id="f80a2-p102">Avec les mêmes formes de syntaxe, vous pouvez également renvoyer à la propriété **Value** d'un objet **Field** que vous créez et ajoutez à une collection **Fields**. Le contexte de la référence de champ détermine si vous faites référence à l'objet **Field** ou à la propriété **Value** de l'objet **Field**.</span><span class="sxs-lookup"><span data-stu-id="f80a2-p102">With the same syntax forms, you can also refer to the **Value** property of a **Field** object that you create and append to a **Fields** collection. The context of the field reference will determine whether you are referring to the **Field** object or the **Value** property of the **Field** object.</span></span>

## <a name="example"></a><span data-ttu-id="f80a2-115">Exemple</span><span class="sxs-lookup"><span data-stu-id="f80a2-115">Example</span></span>

<span data-ttu-id="f80a2-p103">Cet exemple indique les propriétés valides pour un objet **Field** en fonction de l'emplacement de l'objet **Field** (par exemple, la collection **Fields** d'un objet **TableDef**, la collection **Fields** d'un objet **QueryDef**, etc.). La procédure FieldOutput est nécessaire à l'exécution de cette procédure.</span><span class="sxs-lookup"><span data-stu-id="f80a2-p103">This example shows what properties are valid for a **Field** object depending on where the **Field** resides (for example, the **Fields** collection of a **TableDef**, the **Fields** collection of a **QueryDef**, and so forth). The FieldOutput procedure is required for this procedure to run.</span></span>

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

<span data-ttu-id="f80a2-p104">Cet exemple utilise la méthode **CreateField** pour créer trois objets **Fields** pour un objet **TableDef**. Il affiche ensuite les propriétés de ces objets **Field**, qui sont automatiquement définies par la méthode **CreateField**. (Les propriétés dont les valeurs sont vides lors de la création de **Field** ne sont pas affichées.)</span><span class="sxs-lookup"><span data-stu-id="f80a2-p104">This example uses the **CreateField** method to create three **Fields** for a new **TableDef**. It then displays the properties of those **Field** objects that are automatically set by the **CreateField** method. (Properties whose values are empty at the time of **Field** creation are not shown.)</span></span>

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
