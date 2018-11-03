---
title: Objet relation (DAO)
TOCTitle: Relation Object
ms:assetid: 46d6dfaf-a97d-3abd-0b4b-396a41eb3be7
ms:mtpsurl: https://msdn.microsoft.com/library/Ff193195(v=office.15)
ms:contentKeyID: 48544578
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: 49e8cdb7586af93ca17782ba0cb1071036c38eeb
ms.sourcegitcommit: 38d0db57580cc5f4a0231c27b1643f8db5431ca3
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 11/02/2018
ms.locfileid: "25936951"
---
# <a name="relation-object-dao"></a>Objet relation (DAO)


**S’applique à**: Access 2013, Office 2013

Un objet **Relation** représente une relation entre des champs de tables ou de requêtes (bases de données de moteur de base de données Microsoft Access uniquement).

## <a name="remarks"></a>Remarques

Vous pouvez utiliser l'objet **Relation** pour créer des relations et examiner les relations existantes dans la base de données.

Grâce à un objet **Relation** et à ses propriétés, vous pouvez :

  - Indiquer une relation appliquée entre des champs de tables de base (mais pas une relation impliquant une requête ou une table liée).

  - Définir des relations non appliquées entre tout type de table ou de requête (natif ou lié).

  - Utiliser la propriété **Name** pour faire référence à la relation entre les champs dans la table primaire référencée et la table étrangère de référence.

  - Utiliser la propriété **Attributes** pour déterminer le type de relation entre les champs de la table (un-à-un ou un-à-plusieurs), ainsi que le mode d'application de l'intégrité référentielle.

  - Utiliser la propriété **Attributes** pour déterminer si le moteur de base de données Microsoft Access peut effectuer des opérations de mise à jour en cascade et de suppression en cascade dans des tables primaires et étrangères.

  - Utiliser la propriété **Attributes** pour déterminer si la relation entre les champs de la table est du type jointure gauche ou jointure droite.

  - Utiliser la propriété **Name** de tous les objets **Field** dans la collection **Fields** d'un objet **Relation** pour définir ou renvoyer les noms des champs dans la clé primaire de la table référencée ou les paramètres de propriété **ForeignName** des objets **Field** pour définir ou renvoyer les noms des champs dans la clé étrangère de la table de référence.

Si vous apportez des modifications contraires aux relations définies pour la base de données, une erreur interceptable se produit. Si vous demandez des opérations de mise à jour en cascade ou de suppression en cascade, le moteur de base de données Microsoft Access modifie également les tables de clé primaire ou de clé étrangère afin d'appliquer les relations définies.

Par exemple, la base de données Northwind contient une relation entre la table Orders et la table Customers. Le champ CustomerID de la table Customers représente la clé primaire et le champ CustomerID de la table Orders constitue la clé étrangère. Pour accepter un nouvel enregistrement dans la table Orders, le moteur de base de données Microsoft Access recherche dans la table Customers une correspondance pour le champ CustomerID de la table Orders. S'il ne trouve aucune correspondance, il refuse le nouvel enregistrement et une erreur interceptable se produit.

Lors de l'application de l'intégrité référentielle, un index unique doit déjà exister pour le champ clé de la table référencée. Le moteur de base de données Microsoft Access crée automatiquement un index en définissant la propriété **Foreign** pour qu'elle fasse office de clé étrangère dans la table de référence.

Pour créer un objet **Relation**, utilisez la méthode **CreateRelation**. Pour faire référence à un objet **Relation** dans une collection par son numéro ordinal ou par son paramètre de propriété **Name**, utilisez l'une des formes de syntaxe suivantes :

**Relations**(0)

**Relations** (« nom »)

**Relations**\!\[nom\]

## <a name="example"></a>Exemple

L'exemple ci-dessous indique comment un objet **Relation** existant peut déterminer l'entrée de données. La procédure tente d'ajouter un enregistrement dont le champ CategoryID est délibérément incorrect, ce qui déclenche la routine de traitement des erreurs.

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

L'exemple ci-dessous fait appel à la méthode **CreateRelation** pour créer un objet **Relation** entre l'objet **TableDef** Employees et un nouvel objet **TableDef** nommé Departments. Il montre également comment créer une **Relation** crée également nécessaires **index** dans la table étrangère (DepartmentsEmployees Index de la table Employees).

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
