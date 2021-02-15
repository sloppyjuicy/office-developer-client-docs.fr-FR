---
title: Database.CreateRelation method (DAO)
TOCTitle: CreateRelation Method
ms:assetid: e240c7e3-c293-5e19-afcc-34d9a5549c64
ms:mtpsurl: https://msdn.microsoft.com/library/Ff835692(v=office.15)
ms:contentKeyID: 48548279
ms.date: 09/18/2015
mtps_version: v=office.15
f1_keywords:
- dao360.chm1052969
f1_categories:
- Office.Version=v15
localization_priority: Normal
ms.openlocfilehash: 365835bc579a431d34b65cd27ed4de4e12bca309
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32294952"
---
# <a name="databasecreaterelation-method-dao"></a>Database.CreateRelation method (DAO)

**S’applique à** : Access 2013, Office 2013

Crée un objet **[Relation](relation-object-dao.md)** (espaces de travail Microsoft Access uniquement). .

## <a name="syntax"></a>Syntaxe

*.* CreateRelation(***Name***, ***Table***, ***ForeignTable***, ***Attributes***)

*expression* Variable qui représente un objet **Database**.

## <a name="parameters"></a>Paramètres

<table>
<colgroup>
<col style="width: 25%" />
<col style="width: 25%" />
<col style="width: 25%" />
<col style="width: 25%" />
</colgroup>
<thead>
<tr class="header">
<th><p>Nom</p></th>
<th><p>Obligatoire/facultatif</p></th>
<th><p>Type de données</p></th>
<th><p>Description</p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><em>Name</em></p></td>
<td><p>Facultatif</p></td>
<td><p><strong>Variant</strong></p></td>
<td><p><strong>Variant</strong> (sous-type <strong>String</strong>) qui identifie par un nom unique le nouvel objet <strong>Relation</strong>. Voir la <strong><a href="connection-name-property-dao.md">propriété Name</a></strong> pour plus d’informations sur les noms de <strong>relation valides.</strong></p></td>
</tr>
<tr class="even">
<td><p><em>Tableau</em></p></td>
<td><p>Facultatif</p></td>
<td><p><strong>Variant</strong></p></td>
<td><p><strong>Variant</strong> (sous-type <strong>String</strong>) représentant le nom de la table primaire dans la relation. Si la table n’existe pas avant que vous ajoutiez l’objet <strong>Relation</strong>, une erreur d’exécution se produit.</p></td>
</tr>
<tr class="odd">
<td><p><em>ForeignTable</em></p></td>
<td><p>Facultatif</p></td>
<td><p><strong>Variant</strong></p></td>
<td><p><strong>Variant</strong> (sous-type <strong>String</strong>) représentant le nom de la table étrangère dans la relation. Si la table n’existe pas avant que vous ajoutiez l’objet <strong>Relation</strong>, une erreur d’exécution se produit.</p></td>
</tr>
<tr class="even">
<td><p><em>Attributs</em></p></td>
<td><p>Facultatif</p></td>
<td><p><strong>Variant</strong></p></td>
<td><p>Constante ou combinaison de constantes contenant des informations sur le type de relation. Pour plus <strong><a href="field-attributes-property-dao.md">d’informations,</a></strong> voir la propriété Attributes.</p></td>
</tr>
</tbody>
</table>


## <a name="return-value"></a>Valeur renvoyée

Relation

## <a name="remarks"></a>Remarques

L'objet **Relation** fournit des informations au moteur de base de données Microsoft Access sur la relation entre les champs dans deux objets **[TableDef](tabledef-object-dao.md)** ou **[QueryDef](querydef-object-dao.md)**. Vous pouvez implémenter l'intégrité référentielle en utilisant la propriété **Attributes**.

Si vous omettez un ou plusieurs arguments facultatifs avec la méthode **CreateRelation**, vous pouvez utiliser une instruction d'affectation appropriée pour définir ou redéfinir la propriété correspondante avant d'ajouter le nouvel objet à la collection. Après l'ajout de l'objet, il est impossible de modifier les paramètres de ses propriétés. Pour plus d'informations, consultez les rubriques des différentes propriétés.

Avant de pouvoir appeler la méthode **[Append](fields-append-method-dao.md)** sur un objet **Relation**, vous devez ajouter les objets **[Field](field-object-dao.md)** appropriés pour définir la relation des tables de clé primaire et étrangère.

Si le nom fait référence à un objet qui est déjà membre de la collection ou si les noms d’objets **Field** fournis dans la collection **Fields** subordonnée ne sont pas valides, une erreur d’utilisation se produit lorsque vous utilisez la méthode **Append.**

Vous ne pouvez ni établir ni conserver de relation entre une table répliquée et une table locale.

Pour supprimer un objet **Relation** de la collection **[Relations](relations-collection-dao.md)**, appelez la méthode **[Delete](fields-delete-method-dao.md)** sur la collection.

## <a name="example"></a>Exemple

Cet exemple utilise la méthode **CreateRelation** pour créer une **Relation** entre l'objet **TableDef** Employees et un nouvel objet **TableDef** appelé Departments. Cet exemple illustre également comment la création d'une nouvelle **Relation** entraîne la création de tout **Indexes** nécessaire dans la table étrangère (l'index DepartmentsEmployees de la table Employees).

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
