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
# <a name="databasecreaterelation-method-dao"></a><span data-ttu-id="86279-102">Database.CreateRelation method (DAO)</span><span class="sxs-lookup"><span data-stu-id="86279-102">Database.CreateRelation method (DAO)</span></span>

<span data-ttu-id="86279-103">**S’applique à** : Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="86279-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="86279-p101">Crée un nouvel objet **[Relation](relation-object-dao.md)** (Espaces de travail Microsoft Access uniquement).</span><span class="sxs-lookup"><span data-stu-id="86279-p101">Creates a new **[Relation](relation-object-dao.md)** object (Microsoft Access workspaces only). .</span></span>

## <a name="syntax"></a><span data-ttu-id="86279-106">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="86279-106">Syntax</span></span>

<span data-ttu-id="86279-107">*.* CreateRelation(***Name***, ***Table***, ***ForeignTable***, ***Attributes***)</span><span class="sxs-lookup"><span data-stu-id="86279-107">*expression* .CreateRelation(***Name***, ***Table***, ***ForeignTable***, ***Attributes***)</span></span>

<span data-ttu-id="86279-108">*expression* Variable qui représente un objet **Database**.</span><span class="sxs-lookup"><span data-stu-id="86279-108">*expression* A variable that represents a **Database** object.</span></span>

## <a name="parameters"></a><span data-ttu-id="86279-109">Paramètres</span><span class="sxs-lookup"><span data-stu-id="86279-109">Parameters</span></span>

<table>
<colgroup>
<col style="width: 25%" />
<col style="width: 25%" />
<col style="width: 25%" />
<col style="width: 25%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="86279-110">Nom</span><span class="sxs-lookup"><span data-stu-id="86279-110">Name</span></span></p></th>
<th><p><span data-ttu-id="86279-111">Obligatoire/facultatif</span><span class="sxs-lookup"><span data-stu-id="86279-111">Required/optional</span></span></p></th>
<th><p><span data-ttu-id="86279-112">Type de données</span><span class="sxs-lookup"><span data-stu-id="86279-112">Data type</span></span></p></th>
<th><p><span data-ttu-id="86279-113">Description</span><span class="sxs-lookup"><span data-stu-id="86279-113">Description</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="86279-114"><em>Name</em></span><span class="sxs-lookup"><span data-stu-id="86279-114"><em>Name</em></span></span></p></td>
<td><p><span data-ttu-id="86279-115">Facultatif</span><span class="sxs-lookup"><span data-stu-id="86279-115">Optional</span></span></p></td>
<td><p><span data-ttu-id="86279-116"><strong>Variant</strong></span><span class="sxs-lookup"><span data-stu-id="86279-116"><strong>Variant</strong></span></span></p></td>
<td><p><span data-ttu-id="86279-p102"><strong>Variant</strong> (sous-type <strong>String</strong>) qui identifie par un nom unique le nouvel objet <strong>Relation</strong>. Consultez la propriété <strong><a href="connection-name-property-dao.md">Name</a></strong> pour plus d’informations sur les noms d’objets <strong>Relation</strong> valides.</span><span class="sxs-lookup"><span data-stu-id="86279-p102">A <strong>Variant</strong> (<strong>String</strong> subtype) that uniquely names the new <strong>Relation</strong> object. See the <strong><a href="connection-name-property-dao.md">Name</a></strong> property for details on valid <strong>Relation</strong> names.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="86279-119"><em>Tableau</em></span><span class="sxs-lookup"><span data-stu-id="86279-119"><em>Table</em></span></span></p></td>
<td><p><span data-ttu-id="86279-120">Facultatif</span><span class="sxs-lookup"><span data-stu-id="86279-120">Optional</span></span></p></td>
<td><p><span data-ttu-id="86279-121"><strong>Variant</strong></span><span class="sxs-lookup"><span data-stu-id="86279-121"><strong>Variant</strong></span></span></p></td>
<td><p><span data-ttu-id="86279-p103"><strong>Variant</strong> (sous-type <strong>String</strong>) représentant le nom de la table primaire dans la relation. Si la table n’existe pas avant que vous ajoutiez l’objet <strong>Relation</strong>, une erreur d’exécution se produit.</span><span class="sxs-lookup"><span data-stu-id="86279-p103">A <strong>Variant</strong> (<strong>String</strong> subtype) that names the primary table in the relation. If the table doesn't exist before you append the <strong>Relation</strong> object, a run-time error occurs.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="86279-124"><em>ForeignTable</em></span><span class="sxs-lookup"><span data-stu-id="86279-124"><em>ForeignTable</em></span></span></p></td>
<td><p><span data-ttu-id="86279-125">Facultatif</span><span class="sxs-lookup"><span data-stu-id="86279-125">Optional</span></span></p></td>
<td><p><span data-ttu-id="86279-126"><strong>Variant</strong></span><span class="sxs-lookup"><span data-stu-id="86279-126"><strong>Variant</strong></span></span></p></td>
<td><p><span data-ttu-id="86279-p104"><strong>Variant</strong> (sous-type <strong>String</strong>) représentant le nom de la table étrangère dans la relation. Si la table n’existe pas avant que vous ajoutiez l’objet <strong>Relation</strong>, une erreur d’exécution se produit.</span><span class="sxs-lookup"><span data-stu-id="86279-p104">A <strong>Variant</strong> (<strong>String</strong> subtype) that names the foreign table in the relation. If the table doesn't exist before you append the <strong>Relation</strong> object, a run-time error occurs.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="86279-129"><em>Attributs</em></span><span class="sxs-lookup"><span data-stu-id="86279-129"><em>Attributes</em></span></span></p></td>
<td><p><span data-ttu-id="86279-130">Facultatif</span><span class="sxs-lookup"><span data-stu-id="86279-130">Optional</span></span></p></td>
<td><p><span data-ttu-id="86279-131"><strong>Variant</strong></span><span class="sxs-lookup"><span data-stu-id="86279-131"><strong>Variant</strong></span></span></p></td>
<td><p><span data-ttu-id="86279-132">Constante ou combinaison de constantes contenant des informations sur le type de relation.</span><span class="sxs-lookup"><span data-stu-id="86279-132">A constant or combination of constants that contains information about the relationship type.</span></span> <span data-ttu-id="86279-133">Pour plus <strong><a href="field-attributes-property-dao.md">d’informations,</a></strong> voir la propriété Attributes.</span><span class="sxs-lookup"><span data-stu-id="86279-133">See the <strong><a href="field-attributes-property-dao.md">Attributes</a></strong> property for details.</span></span></p></td>
</tr>
</tbody>
</table>


## <a name="return-value"></a><span data-ttu-id="86279-134">Valeur renvoyée</span><span class="sxs-lookup"><span data-stu-id="86279-134">Return value</span></span>

<span data-ttu-id="86279-135">Relation</span><span class="sxs-lookup"><span data-stu-id="86279-135">Relation</span></span>

## <a name="remarks"></a><span data-ttu-id="86279-136">Remarques</span><span class="sxs-lookup"><span data-stu-id="86279-136">Remarks</span></span>

<span data-ttu-id="86279-p106">L'objet **Relation** fournit des informations au moteur de base de données Microsoft Access sur la relation entre les champs dans deux objets **[TableDef](tabledef-object-dao.md)** ou **[QueryDef](querydef-object-dao.md)**. Vous pouvez implémenter l'intégrité référentielle en utilisant la propriété **Attributes**.</span><span class="sxs-lookup"><span data-stu-id="86279-p106">The **Relation** object provides information to the Microsoft Access database engine about the relationship between fields in two **[TableDef](tabledef-object-dao.md)** or **[QueryDef](querydef-object-dao.md)** objects. You can implement referential integrity by using the **Attributes** property.</span></span>

<span data-ttu-id="86279-p107">Si vous omettez un ou plusieurs arguments facultatifs avec la méthode **CreateRelation**, vous pouvez utiliser une instruction d'affectation appropriée pour définir ou redéfinir la propriété correspondante avant d'ajouter le nouvel objet à la collection. Après l'ajout de l'objet, il est impossible de modifier les paramètres de ses propriétés. Pour plus d'informations, consultez les rubriques des différentes propriétés.</span><span class="sxs-lookup"><span data-stu-id="86279-p107">If you omit one or more of the optional parts when you use the **CreateRelation** method, you can use an appropriate assignment statement to set or reset the corresponding property before you append the new object to a collection. After you append the object, you can't alter any of its property settings. See the individual property topics for more details.</span></span>

<span data-ttu-id="86279-142">Avant de pouvoir appeler la méthode **[Append](fields-append-method-dao.md)** sur un objet **Relation**, vous devez ajouter les objets **[Field](field-object-dao.md)** appropriés pour définir la relation des tables de clé primaire et étrangère.</span><span class="sxs-lookup"><span data-stu-id="86279-142">Before you can use the **[Append](fields-append-method-dao.md)** method on a **Relation** object, you must append the appropriate **[Field](field-object-dao.md)** objects to define the primary and foreign key relationship tables.</span></span>

<span data-ttu-id="86279-143">Si le nom fait référence à un objet qui est déjà membre de la collection ou si les noms d’objets **Field** fournis dans la collection **Fields** subordonnée ne sont pas valides, une erreur d’utilisation se produit lorsque vous utilisez la méthode **Append.**</span><span class="sxs-lookup"><span data-stu-id="86279-143">If name refers to an object that is already a member of the collection or if the **Field** object names provided in the subordinate **Fields** collection are invalid, a run-time error occurs when you use the **Append** method.</span></span>

<span data-ttu-id="86279-144">Vous ne pouvez ni établir ni conserver de relation entre une table répliquée et une table locale.</span><span class="sxs-lookup"><span data-stu-id="86279-144">You can't establish or maintain a relationship between a replicated table and a local table.</span></span>

<span data-ttu-id="86279-145">Pour supprimer un objet **Relation** de la collection **[Relations](relations-collection-dao.md)**, appelez la méthode **[Delete](fields-delete-method-dao.md)** sur la collection.</span><span class="sxs-lookup"><span data-stu-id="86279-145">To remove a **Relation** object from the **[Relations](relations-collection-dao.md)** collection, use the **[Delete](fields-delete-method-dao.md)** method on the collection.</span></span>

## <a name="example"></a><span data-ttu-id="86279-146">Exemple</span><span class="sxs-lookup"><span data-stu-id="86279-146">Example</span></span>

<span data-ttu-id="86279-p108">Cet exemple utilise la méthode **CreateRelation** pour créer une **Relation** entre l'objet **TableDef** Employees et un nouvel objet **TableDef** appelé Departments. Cet exemple illustre également comment la création d'une nouvelle **Relation** entraîne la création de tout **Indexes** nécessaire dans la table étrangère (l'index DepartmentsEmployees de la table Employees).</span><span class="sxs-lookup"><span data-stu-id="86279-p108">This example uses the **CreateRelation** method to create a **Relation** between the Employees **TableDef** and a new **TableDef** called Departments. This example also demonstrates how creating a new **Relation** will also create any necessary **Indexes** in the foreign table (the DepartmentsEmployees Index in the Employees table).</span></span>

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
