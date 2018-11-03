---
title: Objet relation (DAO)
TOCTitle: Relation Object
ms:assetid: 46d6dfaf-a97d-3abd-0b4b-396a41eb3be7
ms:mtpsurl: https://msdn.microsoft.com/library/Ff193195(v=office.15)
ms:contentKeyID: 48544578
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: cfabb36e539aaff1f6e12d431d2cfcfe79ff5d04
ms.sourcegitcommit: d7248f803002b31cf7fc561b03530199a9b0a8fd
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 11/02/2018
ms.locfileid: "25928086"
---
# <a name="relation-object-dao"></a><span data-ttu-id="a51b7-102">Objet relation (DAO)</span><span class="sxs-lookup"><span data-stu-id="a51b7-102">Relation object (DAO)</span></span>


<span data-ttu-id="a51b7-103">**S’applique à**: Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="a51b7-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="a51b7-104">Un objet **Relation** représente une relation entre des champs de tables ou de requêtes (bases de données de moteur de base de données Microsoft Access uniquement).</span><span class="sxs-lookup"><span data-stu-id="a51b7-104">A **Relation** object represents a relationship between fields in tables or queries (Microsoft Access database engine databases only).</span></span>

## <a name="remarks"></a><span data-ttu-id="a51b7-105">Remarques</span><span class="sxs-lookup"><span data-stu-id="a51b7-105">Remarks</span></span>

<span data-ttu-id="a51b7-106">Vous pouvez utiliser l'objet **Relation** pour créer des relations et examiner les relations existantes dans la base de données.</span><span class="sxs-lookup"><span data-stu-id="a51b7-106">You can use the **Relation** object to create new relationships and examine existing relationships in your database.</span></span>

<span data-ttu-id="a51b7-107">Grâce à un objet **Relation** et à ses propriétés, vous pouvez :</span><span class="sxs-lookup"><span data-stu-id="a51b7-107">Using a **Relation** object and its properties, you can:</span></span>

  - <span data-ttu-id="a51b7-108">Indiquer une relation appliquée entre des champs de tables de base (mais pas une relation impliquant une requête ou une table liée).</span><span class="sxs-lookup"><span data-stu-id="a51b7-108">Specify an enforced relationship between fields in base tables (but not a relationship that involves a query or a linked table).</span></span>

  - <span data-ttu-id="a51b7-109">Définir des relations non appliquées entre tout type de table ou de requête (natif ou lié).</span><span class="sxs-lookup"><span data-stu-id="a51b7-109">Establish unenforced relationships between any type of table or query— native or linked.</span></span>

  - <span data-ttu-id="a51b7-110">Utiliser la propriété **Name** pour faire référence à la relation entre les champs dans la table primaire référencée et la table étrangère de référence.</span><span class="sxs-lookup"><span data-stu-id="a51b7-110">Use the **Name** property to refer to the relationship between the fields in the referenced primary table and the referencing foreign table.</span></span>

  - <span data-ttu-id="a51b7-111">Utiliser la propriété **Attributes** pour déterminer le type de relation entre les champs de la table (un-à-un ou un-à-plusieurs), ainsi que le mode d'application de l'intégrité référentielle.</span><span class="sxs-lookup"><span data-stu-id="a51b7-111">Use the **Attributes** property to determine whether the relationship between fields in the table is one-to-one or one-to-many and how to enforce referential integrity.</span></span>

  - <span data-ttu-id="a51b7-112">Utiliser la propriété **Attributes** pour déterminer si le moteur de base de données Microsoft Access peut effectuer des opérations de mise à jour en cascade et de suppression en cascade dans des tables primaires et étrangères.</span><span class="sxs-lookup"><span data-stu-id="a51b7-112">Use the **Attributes** property to determine whether the Microsoft Access database engine can perform cascading update and cascading delete operations on primary and foreign tables.</span></span>

  - <span data-ttu-id="a51b7-113">Utiliser la propriété **Attributes** pour déterminer si la relation entre les champs de la table est du type jointure gauche ou jointure droite.</span><span class="sxs-lookup"><span data-stu-id="a51b7-113">Use the **Attributes** property to determine whether the relationship between fields in the table is left join or right join.</span></span>

  - <span data-ttu-id="a51b7-114">Utiliser la propriété **Name** de tous les objets **Field** dans la collection **Fields** d'un objet **Relation** pour définir ou renvoyer les noms des champs dans la clé primaire de la table référencée ou les paramètres de propriété **ForeignName** des objets **Field** pour définir ou renvoyer les noms des champs dans la clé étrangère de la table de référence.</span><span class="sxs-lookup"><span data-stu-id="a51b7-114">Use the **Name** property of all **Field** objects in the **Fields** collection of a **Relation** object to set or return the names of the fields in the primary key of the referenced table, or the **ForeignName** property settings of the **Field** objects to set or return the names of the fields in the foreign key of the referencing table.</span></span>

<span data-ttu-id="a51b7-p101">Si vous apportez des modifications contraires aux relations définies pour la base de données, une erreur interceptable se produit. Si vous demandez des opérations de mise à jour en cascade ou de suppression en cascade, le moteur de base de données Microsoft Access modifie également les tables de clé primaire ou de clé étrangère afin d'appliquer les relations définies.</span><span class="sxs-lookup"><span data-stu-id="a51b7-p101">If you make changes that violate the relationships established for the database, a trappable error occurs. If you request cascading update or cascading delete operations, the Microsoft Access database engine also modifies the primary key or foreign key tables to enforce the relationships you establish.</span></span>

<span data-ttu-id="a51b7-p102">Par exemple, la base de données Northwind contient une relation entre la table Orders et la table Customers. Le champ CustomerID de la table Customers représente la clé primaire et le champ CustomerID de la table Orders constitue la clé étrangère. Pour accepter un nouvel enregistrement dans la table Orders, le moteur de base de données Microsoft Access recherche dans la table Customers une correspondance pour le champ CustomerID de la table Orders. S'il ne trouve aucune correspondance, il refuse le nouvel enregistrement et une erreur interceptable se produit.</span><span class="sxs-lookup"><span data-stu-id="a51b7-p102">For example, the Northwind database contains a relationship between an Orders table and a Customers table. The CustomerID field of the Customers table is the primary key, and the CustomerID field of the Orders table is the foreign key. For the Microsoft Access database engine to accept a new record in the Orders table, it searches the Customers table for a match on the CustomerID field of the Orders table. If the Microsoft Access database engine doesn't find a match, it doesn't accept the new record, and a trappable error occurs.</span></span>

<span data-ttu-id="a51b7-p103">Lors de l'application de l'intégrité référentielle, un index unique doit déjà exister pour le champ clé de la table référencée. Le moteur de base de données Microsoft Access crée automatiquement un index en définissant la propriété **Foreign** pour qu'elle fasse office de clé étrangère dans la table de référence.</span><span class="sxs-lookup"><span data-stu-id="a51b7-p103">When you enforce referential integrity, a unique index must already exist for the key field of the referenced table. The Microsoft Access database engine automatically creates an index with the **Foreign** property set to act as the foreign key in the referencing table.</span></span>

<span data-ttu-id="a51b7-p104">Pour créer un objet **Relation**, utilisez la méthode **CreateRelation**. Pour faire référence à un objet **Relation** dans une collection par son numéro ordinal ou par son paramètre de propriété **Name**, utilisez l'une des formes de syntaxe suivantes :</span><span class="sxs-lookup"><span data-stu-id="a51b7-p104">To create a new **Relation** object, use the **CreateRelation** method. To refer to a **Relation** object in a collection by its ordinal number or by its **Name** property setting, use any of the following syntax forms:</span></span>

<span data-ttu-id="a51b7-125">**Relations**(0)</span><span class="sxs-lookup"><span data-stu-id="a51b7-125">**Relations**(0)</span></span>

<span data-ttu-id="a51b7-126">**Relations** (« nom »)</span><span class="sxs-lookup"><span data-stu-id="a51b7-126">**Relations**("name")</span></span>

<span data-ttu-id="a51b7-127">**Relations**\!\[nom\]</span><span class="sxs-lookup"><span data-stu-id="a51b7-127">**Relations**\!\[name\]</span></span>

## <a name="example"></a><span data-ttu-id="a51b7-128">Exemple</span><span class="sxs-lookup"><span data-stu-id="a51b7-128">Example</span></span>

<span data-ttu-id="a51b7-p105">L'exemple ci-dessous indique comment un objet **Relation** existant peut déterminer l'entrée de données. La procédure tente d'ajouter un enregistrement dont le champ CategoryID est délibérément incorrect, ce qui déclenche la routine de traitement des erreurs.</span><span class="sxs-lookup"><span data-stu-id="a51b7-p105">This example shows how an existing **Relation** object can control data entry. The procedure attempts to add a record with a deliberately incorrect CategoryID; this triggers the error-handling routine.</span></span>

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

<span data-ttu-id="a51b7-p106">L'exemple ci-dessous fait appel à la méthode **CreateRelation** pour créer un objet **Relation** entre l'objet **TableDef** Employees et un nouvel objet **TableDef** nommé Departments. Il illustre également comment la création d'un objet **Relation** entraîne celle des objets **Indexes** nécessaires dans la table étrangère (index DepartmentsEmployees de la table Employees).</span><span class="sxs-lookup"><span data-stu-id="a51b7-p106">This example uses the **CreateRelation** method to create a **Relation** between the Employees **TableDef** and a new **TableDef** called Departments. This example also demonstrates how creating a new **Relation** will also create any necessary **Indexes** in the foreign table (the DepartmentsEmployees Index in the Employees table).</span></span>

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
