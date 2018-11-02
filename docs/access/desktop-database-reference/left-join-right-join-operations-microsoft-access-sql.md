---
title: LEFT JOIN, RIGHT JOIN, opérations (Microsoft Access SQL)
TOCTitle: LEFT JOIN, RIGHT JOIN operations (Microsoft Access SQL)
ms:assetid: 9c10525f-98b1-fd4f-8b40-07a32c5c6502
ms:mtpsurl: https://msdn.microsoft.com/library/Ff198084(v=office.15)
ms:contentKeyID: 48546586
ms.date: 09/18/2015
mtps_version: v=office.15
dev_langs:
- sql
ms.openlocfilehash: a16df1e26e4ab5617e6bf76aa93a11a936ccb49b
ms.sourcegitcommit: d7248f803002b31cf7fc561b03530199a9b0a8fd
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 11/02/2018
ms.locfileid: "25925897"
---
# <a name="left-join-right-join-operations-microsoft-access-sql"></a><span data-ttu-id="308e2-102">LEFT JOIN, RIGHT JOIN, opérations (Microsoft Access SQL)</span><span class="sxs-lookup"><span data-stu-id="308e2-102">LEFT JOIN, RIGHT JOIN operations (Microsoft Access SQL)</span></span>

<span data-ttu-id="308e2-103">**S’applique à**: Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="308e2-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="308e2-104">Combine les enregistrements source-table lorsqu'ils sont utilisés dans une clause [FROM](https://msdn.microsoft.com/library/ff836674\(v=office.15\)).</span><span class="sxs-lookup"><span data-stu-id="308e2-104">Combines source-table records when used in any [FROM](https://msdn.microsoft.com/library/ff836674\(v=office.15\)) clause.</span></span>

## <a name="syntax"></a><span data-ttu-id="308e2-105">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="308e2-105">Syntax</span></span>

<span data-ttu-id="308e2-106">FROM *table1* \[ gauche | DROITE \] JOIN *table2* ON *Table1.champ1* *OpérateurComparaison Table2.champ2*</span><span class="sxs-lookup"><span data-stu-id="308e2-106">FROM *table1* \[ LEFT | RIGHT \] JOIN *table2* ON *table1.field1* *compopr table2.field2*</span></span>

<span data-ttu-id="308e2-107">Les opérations LEFT JOIN et RIGHT JOIN sont composées des arguments suivants :</span><span class="sxs-lookup"><span data-stu-id="308e2-107">The LEFT JOIN and RIGHT JOIN operations have these parts:</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="308e2-108">Élément</span><span class="sxs-lookup"><span data-stu-id="308e2-108">Part</span></span></p></th>
<th><p><span data-ttu-id="308e2-109">Description</span><span class="sxs-lookup"><span data-stu-id="308e2-109">Description</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="308e2-110"><em>table1</em>, <em>table2</em></span><span class="sxs-lookup"><span data-stu-id="308e2-110"><em>table1</em>, <em>table2</em></span></span></p></td>
<td><p><span data-ttu-id="308e2-111">Noms des tables à partir desquelles les enregistrements sont combinés.</span><span class="sxs-lookup"><span data-stu-id="308e2-111">The names of the tables from which records are combined.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="308e2-112"><em>champ1</em>, <em>champ2</em></span><span class="sxs-lookup"><span data-stu-id="308e2-112"><em>field1</em>, <em>field2</em></span></span></p></td>
<td><p><span data-ttu-id="308e2-p101">Noms des champs joints. Les champs doivent être du même type et doivent contenir le même type de données, mais il ne doivent pas obligatoirement avoir le même nom.</span><span class="sxs-lookup"><span data-stu-id="308e2-p101">The names of the fields that are joined. The fields must be of the same data type and contain the same kind of data, but they do not need to have the same name.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="308e2-115"><em>opérateurcomparaison</em></span><span class="sxs-lookup"><span data-stu-id="308e2-115"><em>compopr</em></span></span></p></td>
<td><p><span data-ttu-id="308e2-116">Tout opérateur de comparaison relationnel : &quot;=,&quot; &quot; &lt;,&quot; &quot; &gt;,&quot; &quot; &lt;=,&quot; &quot; &gt;=&quot; ou &quot; &lt; &gt;.&quot;</span><span class="sxs-lookup"><span data-stu-id="308e2-116">Any relational comparison operator: &quot;=,&quot; &quot;&lt;,&quot; &quot;&gt;,&quot; &quot;&lt;=,&quot; &quot;&gt;=,&quot; or &quot;&lt;&gt;.&quot;</span></span></p></td>
</tr>
</tbody>
</table>


## <a name="remarks"></a><span data-ttu-id="308e2-117">Notes</span><span class="sxs-lookup"><span data-stu-id="308e2-117">Remarks</span></span>

<span data-ttu-id="308e2-p102">Utilisez une opération LEFT JOIN pour créer une jointure externe gauche. Les jointures externes gauche comprennent tous les enregistrements de la première des deux tables (la table de gauche), même si aucune valeur de cette table ne correspond aux enregistrements dans la seconde table (la table de droite).</span><span class="sxs-lookup"><span data-stu-id="308e2-p102">Use a LEFT JOIN operation to create a left outer join. Left outer joins include all of the records from the first (left) of two tables, even if there are no matching values for records in the second (right) table.</span></span>

<span data-ttu-id="308e2-p103">Utilisez une opération RIGHT JOIN pour créer une jointure externe droite. Les jointures externes droite comprennent tous les enregistrements de la seconde table (la table de droite), même si aucune valeur de cette table ne correspond aux enregistrements dans la première table (la table de gauche).</span><span class="sxs-lookup"><span data-stu-id="308e2-p103">Use a RIGHT JOIN operation to create a right outer join. Right outer joins include all of the records from the second (right) of two tables, even if there are no matching values for records in the first (left) table.</span></span>

<span data-ttu-id="308e2-p104">Vous pouvez par exemple utiliser LEFT JOIN avec les tables Departments (services) (gauche) et Employees (employés) (droite) pour sélectionner tous les services, y compris ceux auxquels aucun employé n'est assigné. Pour sélectionner tous les employés, y compris ceux qui ne sont pas assignés à un service, utilisez RIGHT JOIN.</span><span class="sxs-lookup"><span data-stu-id="308e2-p104">For example, you could use LEFT JOIN with the Departments (left) and Employees (right) tables to select all departments, including those that have no employees assigned to them. To select all employees, including those who are not assigned to a department, you would use RIGHT JOIN.</span></span>

<span data-ttu-id="308e2-p105">L'exemple suivant montre comment vous pouvez joindre les tables Categories (catégories) et Products (produits) sur le champ CategoryID. La requête produit une liste de toutes les catégories, y compris celles qui ne contiennent aucun produit :</span><span class="sxs-lookup"><span data-stu-id="308e2-p105">The following example shows how you could join the Categories and Products tables on the CategoryID field. The query produces a list of all categories, including those that contain no products:</span></span>

```sql
SELECT CategoryName, 
ProductName 
FROM Categories LEFT JOIN Products 
ON Categories.CategoryID = Products.CategoryID;
```

<span data-ttu-id="308e2-126">Dans cet exemple, CategoryID est le champ joint, mais il n'est pas inclus dans les résultats de la requête, car il n'est pas inclus dans l'instruction [SELECT](select-statement-microsoft-access-sql.md).</span><span class="sxs-lookup"><span data-stu-id="308e2-126">In this example, CategoryID is the joined field, but it is not included in the query results because it is not included in the [SELECT](select-statement-microsoft-access-sql.md) statement.</span></span> <span data-ttu-id="308e2-127">Pour inclure le champ joint, entrez le nom du champ dans l’instruction SELECT — dans SELECT.</span><span class="sxs-lookup"><span data-stu-id="308e2-127">To include the joined field, enter the field name in the SELECT statement — in this case, Categories.CategoryID.</span></span>

> [!NOTE]
> - <span data-ttu-id="308e2-128">[!REMARQUE] Pour créer une requête qui n'indique que les enregistrements dans lesquels les données dans les champs joints sont identiques, utilisez une opération [INNER JOIN](inner-join-operation-microsoft-access-sql.md).</span><span class="sxs-lookup"><span data-stu-id="308e2-128">To create a query that includes only records in which the data in the joined fields is the same, use an [INNER JOIN](inner-join-operation-microsoft-access-sql.md) operation.</span></span>
> - <span data-ttu-id="308e2-p107">Une jointure LEFT JOIN ou RIGHT JOIN peut être imbriquée dans une jointure INNER JOIN, mais une jointure INNER JOIN ne peut pas être imbriquée dans une jointure LEFT JOIN ou RIGHT JOIN. Reportez-vous à la section concernant l'imbrication de jointures dans la rubrique INNER JOIN pour savoir comment imbriquer des jointures dans d'autres jointures.</span><span class="sxs-lookup"><span data-stu-id="308e2-p107">A LEFT JOIN or a RIGHT JOIN can be nested inside an INNER JOIN, but an INNER JOIN cannot be nested inside a LEFT JOIN or a RIGHT JOIN. See the discussion of nesting in the INNER JOIN topic to see how to nest joins within other joins.</span></span>
> - <span data-ttu-id="308e2-p108">Vous pouvez lier plusieurs clauses ON. Reportez-vous à la section concernant la liaison de clauses dans la rubrique INNER JOIN pour savoir comment procéder.</span><span class="sxs-lookup"><span data-stu-id="308e2-p108">You can link multiple ON clauses. See the discussion of clause linking in the INNER JOIN topic to see how this is done.</span></span>
> - <span data-ttu-id="308e2-133">Si vous essayez de joindre des champs contenant des données de type Mémo ou Objet OLE, une erreur se produit.</span><span class="sxs-lookup"><span data-stu-id="308e2-133">If you try to join fields containing Memo or OLE Object data, an error occurs.</span></span>

## <a name="example"></a><span data-ttu-id="308e2-134">Exemple</span><span class="sxs-lookup"><span data-stu-id="308e2-134">Example</span></span>

<span data-ttu-id="308e2-135">Cet exemple montre comment :</span><span class="sxs-lookup"><span data-stu-id="308e2-135">This example:</span></span>
- <span data-ttu-id="308e2-136">Suppose l’existence de champs hypothétiques de nom du service et l’ID de service dans la table Employees.</span><span class="sxs-lookup"><span data-stu-id="308e2-136">Assumes the existence of hypothetical Department Name and Department ID fields in an Employees table.</span></span> <span data-ttu-id="308e2-137">Notez que ces champs n'existent pas dans la table Employees de la base de données Northwind.</span><span class="sxs-lookup"><span data-stu-id="308e2-137">Note that these fields do not actually exist in the Northwind database Employees table.</span></span>

- <span data-ttu-id="308e2-138">Sélectionne tous les départements, y compris ceux sans employés.</span><span class="sxs-lookup"><span data-stu-id="308e2-138">Selects all departments, including those without employees.</span></span>

- <span data-ttu-id="308e2-139">Appelle la procédure EnumFields que vous pouvez trouver dans l’exemple d’instruction SELECT.</span><span class="sxs-lookup"><span data-stu-id="308e2-139">Calls the EnumFields procedure, which you can find in the SELECT statement example.</span></span>


```vb
    Sub LeftRightJoinX() 
     
        Dim dbs As Database, rst As Recordset 
     
        ' Modify this line to include the path to Northwind 
        ' on your computer. 
        Set dbs = OpenDatabase("Northwind.mdb") 
         
        ' Select all departments, including those  
        ' without employees. 
        Set rst = dbs.OpenRecordset _ 
            ("SELECT [Department Name], " _ 
            & "FirstName & Chr(32) & LastName AS Name " _ 
            & "FROM Departments LEFT JOIN Employees " _ 
            & "ON Departments.[Department ID] = " _ 
            & "Employees.[Department ID] " _ 
            & "ORDER BY [Department Name];") 
         
        ' Populate the Recordset. 
        rst.MoveLast 
         
        ' Call EnumFields to print the contents of the  
        ' Recordset. Pass the Recordset object and desired 
        ' field width. 
        EnumFields rst, 20 
     
        dbs.Close 
     
    End Sub
```
