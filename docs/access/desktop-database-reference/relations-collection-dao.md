---
title: Relations Collection (DAO)
TOCTitle: Relations Collection
ms:assetid: 8929b5cc-cf52-03f2-8cf5-7f45276d258e
ms:mtpsurl: https://msdn.microsoft.com/library/Ff197067(v=office.15)
ms:contentKeyID: 48546153
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: 590f3ac4298363ba04b0b00db165b9dcdc06ea11
ms.sourcegitcommit: 19aca09c5812cfb98b68b5d4604dcaa814479df7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 10/09/2018
ms.locfileid: "25470482"
---
# <a name="relations-collection-dao"></a><span data-ttu-id="73b9a-102">Relations Collection (DAO)</span><span class="sxs-lookup"><span data-stu-id="73b9a-102">Relations Collection (DAO)</span></span>


<span data-ttu-id="73b9a-103">**S’applique à**: Access 2013 | Office 2013</span><span class="sxs-lookup"><span data-stu-id="73b9a-103">**Applies to**: Access 2013 | Office 2013</span></span>

<span data-ttu-id="73b9a-104">Une collection **Relations** contient les objets **Relation** stockés d'un objet **Database** (bases de données de moteur de base de données Microsoft Access uniquement).</span><span class="sxs-lookup"><span data-stu-id="73b9a-104">A **Relations** collection contains stored **Relation** objects of a **Database** object (Microsoft Access database engine databases only).</span></span>

## <a name="remarks"></a><span data-ttu-id="73b9a-105">Remarques</span><span class="sxs-lookup"><span data-stu-id="73b9a-105">Remarks</span></span>

<span data-ttu-id="73b9a-p101">L'objet **Relation** permet de créer des nouvelles relations et d'examiner les relations existantes de votre base de données. Pour ajouter un objet **Relation** à la collection **Relations**, il convient d'abord de le créer à l'aide de la méthode **CreateRelation**, puis de l'ajouter à la collection **Relations** à l'aide de la méthode **Append**. Ce faisant, vous enregistrez l'objet **Relation** lorsque vous fermez l'objet **Database**. Pour supprimer un objet **Relation** de la collection, utilisez la méthode **Delete**.</span><span class="sxs-lookup"><span data-stu-id="73b9a-p101">You can use the **Relation** object to create new relationships and examine existing relationships in your database. To add a **Relation** object to the **Relations** collection, first create it with the **CreateRelation** method, and then append it to the **Relations** collection with the **Append** method. This will save the **Relation** object when you close the **Database** object. To remove a **Relation** object from the collection, use the **Delete** method.</span></span>

<span data-ttu-id="73b9a-110">Pour faire référence à un objet **Relation** d'une collection par son numéro ordinal ou par son paramètre de propriété **Name**, utilisez l'une des syntaxes suivantes :</span><span class="sxs-lookup"><span data-stu-id="73b9a-110">To refer to a **Relation** object in a collection by its ordinal number or by its **Name** property setting, use any of the following syntax forms:</span></span>

<span data-ttu-id="73b9a-111">**Relations**(0)</span><span class="sxs-lookup"><span data-stu-id="73b9a-111">**Relations**(0)</span></span>

<span data-ttu-id="73b9a-112">**Relations** (« nom »)</span><span class="sxs-lookup"><span data-stu-id="73b9a-112">**Relations**("name")</span></span>

<span data-ttu-id="73b9a-113">**Relations**\!\[nom\]</span><span class="sxs-lookup"><span data-stu-id="73b9a-113">**Relations**\!\[name\]</span></span>

## <a name="example"></a><span data-ttu-id="73b9a-114">Exemple</span><span class="sxs-lookup"><span data-stu-id="73b9a-114">Example</span></span>

<span data-ttu-id="73b9a-p102">L'exemple ci-dessous indique comment un objet **Relation** existant peut déterminer l'entrée de données. La procédure tente d'ajouter un enregistrement dont le champ CategoryID est délibérément incorrect, ce qui déclenche la routine de traitement des erreurs.</span><span class="sxs-lookup"><span data-stu-id="73b9a-p102">This example shows how an existing **Relation** object can control data entry. The procedure attempts to add a record with a deliberately incorrect CategoryID; this triggers the error-handling routine.</span></span>

```vb
    Sub RelationX() 
     
     Dim dbsNorthwind As Database 
     Dim rstProducts As Recordset 
     Dim prpLoop As Property 
     Dim fldLoop As Field 
     Dim errLoop As Error 
     
     Set dbsNorthwind = OpenDatabase("Northwind.mdb") 
     Set rstProducts = dbsNorthwind.OpenRecordset("Products") 
     
     ' Print a report showing all the different parts of 
     ' the relation and where each part is stored. 
     With dbsNorthwind.Relations!CategoriesProducts 
     Debug.Print "Properties of " & .Name & " Relation" 
     Debug.Print " Table = " & .Table 
     Debug.Print " ForeignTable = " & .ForeignTable 
     Debug.Print "Fields of " & .Name & " Relation" 
     With .Fields!CategoryID 
     Debug.Print " " & .Name 
     Debug.Print " Name = " & .Name 
     Debug.Print " ForeignName = " & .ForeignName 
     End With 
     End With 
     
     ' Attempt to add a record that violates the relation. 
     With rstProducts 
     .AddNew 
     !ProductName = "Trygve's Lutefisk" 
     !CategoryID = 10 
     On Error GoTo Err_Relation 
     .Update 
     On Error GoTo 0 
     .Close 
     End With 
     
     dbsNorthwind.Close 
     
     Exit Sub 
     
    Err_Relation: 
     
     ' Notify user of any errors that result from 
     ' the invalid data. 
     If DBEngine.Errors.Count > 0 Then 
     For Each errLoop In DBEngine.Errors 
     MsgBox "Error number: " & errLoop.Number & _ 
     vbCr & errLoop.Description 
     Next errLoop 
     End If 
     
     Resume Next 
     
    End Sub 
```

<br/>

<span data-ttu-id="73b9a-p103">L'exemple ci-dessous fait appel à la méthode **CreateRelation** pour créer un objet **Relation** entre l'objet **TableDef** Employees et un nouvel objet **TableDef** nommé Departments. Il illustre également comment la création d'un objet **Relation** entraîne celle des objets **Indexes** nécessaires dans la table étrangère (index DepartmentsEmployees de la table Employees).</span><span class="sxs-lookup"><span data-stu-id="73b9a-p103">This example uses the **CreateRelation** method to create a **Relation** between the Employees **TableDef** and a new **TableDef** called Departments. This example also demonstrates how creating a new **Relation** will also create any necessary **Indexes** in the foreign table (the DepartmentsEmployees Index in the Employees table).</span></span>

```vb
    Sub CreateRelationX() 
     
     Dim dbsNorthwind As Database 
     Dim tdfEmployees As TableDef 
     Dim tdfNew As TableDef 
     Dim idxNew As Index 
     Dim relNew As Relation 
     Dim idxLoop As Index 
     
     Set dbsNorthwind = OpenDatabase("Northwind.mdb") 
     
     With dbsNorthwind 
     ' Add new field to Employees table. 
     Set tdfEmployees = .TableDefs!Employees 
     tdfEmployees.Fields.Append _ 
     tdfEmployees.CreateField("DeptID", dbInteger, 2) 
     
     ' Create new Departments table. 
     Set tdfNew = .CreateTableDef("Departments") 
     
     With tdfNew 
     ' Create and append Field objects to Fields 
     ' collection of the new TableDef object. 
     .Fields.Append .CreateField("DeptID", dbInteger, 2) 
     .Fields.Append .CreateField("DeptName", dbText, 20) 
     
     ' Create Index object for Departments table. 
     Set idxNew = .CreateIndex("DeptIDIndex") 
     ' Create and append Field object to Fields 
     ' collection of the new Index object. 
     idxNew.Fields.Append idxNew.CreateField("DeptID") 
     ' The index in the primary table must be Unique in 
     ' order to be part of a Relation. 
     idxNew.Unique = True 
     .Indexes.Append idxNew 
     End With 
     
     .TableDefs.Append tdfNew 
     
     ' Create EmployeesDepartments Relation object, using 
     ' the names of the two tables in the relation. 
     Set relNew = .CreateRelation("EmployeesDepartments", _ 
     tdfNew.Name, tdfEmployees.Name, _ 
     dbRelationUpdateCascade) 
     
     ' Create Field object for the Fields collection of the 
     ' new Relation object. Set the Name and ForeignName 
     ' properties based on the fields to be used for the 
     ' relation. 
     relNew.Fields.Append relNew.CreateField("DeptID") 
     relNew.Fields!DeptID.ForeignName = "DeptID" 
     .Relations.Append relNew 
     
     ' Print report. 
     Debug.Print "Properties of " & relNew.Name & _ 
     " Relation" 
     Debug.Print " Table = " & relNew.Table 
     Debug.Print " ForeignTable = " & _ 
     relNew.ForeignTable 
     Debug.Print "Fields of " & relNew.Name & " Relation" 
     
     With relNew.Fields!DeptID 
     Debug.Print " " & .Name 
     Debug.Print " Name = " & .Name 
     Debug.Print " ForeignName = " & .ForeignName 
     End With 
     
     Debug.Print "Indexes in " & tdfEmployees.Name & _ 
     " TableDef" 
     For Each idxLoop In tdfEmployees.Indexes 
     Debug.Print " " & idxLoop.Name & _ 
     ", Foreign = " & idxLoop.Foreign 
     Next idxLoop 
     
     ' Delete new objects because this is a demonstration. 
     .Relations.Delete relNew.Name 
     .TableDefs.Delete tdfNew.Name 
     tdfEmployees.Fields.Delete "DeptID" 
     .Close 
     End With 
     
    End Sub
```
