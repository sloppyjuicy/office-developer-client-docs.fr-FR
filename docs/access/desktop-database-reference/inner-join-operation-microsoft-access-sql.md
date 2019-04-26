---
title: INNER JOIN, opération (Microsoft Access SQL)
TOCTitle: INNER JOIN operation (Microsoft Access SQL)
ms:assetid: 8d16c74c-02c6-12b7-b180-3e7744ef65f3
ms:mtpsurl: https://msdn.microsoft.com/library/Ff197346(v=office.15)
ms:contentKeyID: 48546247
ms.date: 09/18/2015
mtps_version: v=office.15
f1_keywords:
- jetsql40.chm5277574
dev_langs:
- sql
f1_categories:
- Office.Version=v15
localization_priority: Priority
ms.openlocfilehash: 6ff2ad40d318801ecec2332b53b41f327c20fbc5
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: HT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32291399"
---
# <a name="inner-join-operation-microsoft-access-sql"></a><span data-ttu-id="c3f15-102">INNER JOIN, opération (Microsoft Access SQL)</span><span class="sxs-lookup"><span data-stu-id="c3f15-102">INNER JOIN Operation (Microsoft Access SQL)</span></span>


<span data-ttu-id="c3f15-103">**S’applique à** : Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="c3f15-103">**Applies to**: Access 2013, Office 2013</span></span>


<span data-ttu-id="c3f15-104">Combine les enregistrements de deux tables chaque fois qu’un champ commun contient des valeurs correspondantes.</span><span class="sxs-lookup"><span data-stu-id="c3f15-104">Combines records from two tables whenever there are matching values in a common field.</span></span>

## <a name="syntax"></a><span data-ttu-id="c3f15-105">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="c3f15-105">Syntax</span></span>

<span data-ttu-id="c3f15-106">FROM *table1* INNER JOIN *table2* ON *table1*.*champ1* *compopr table2*.*champ2*</span><span class="sxs-lookup"><span data-stu-id="c3f15-106">FROM *table1* INNER JOIN *table2* ON *table1*.\*field1 \**compopr table2*.*field2*</span></span>

<span data-ttu-id="c3f15-107">L'opération INNER JOIN est composée des arguments suivants :</span><span class="sxs-lookup"><span data-stu-id="c3f15-107">The INNER JOIN operation has these parts:</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="c3f15-108">Partie</span><span class="sxs-lookup"><span data-stu-id="c3f15-108">Part</span></span></p></th>
<th><p><span data-ttu-id="c3f15-109">Description</span><span class="sxs-lookup"><span data-stu-id="c3f15-109">Description</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="c3f15-110"><em>table1</em>, <em>table2</em></span><span class="sxs-lookup"><span data-stu-id="c3f15-110"><em>table1</em>  ,  <em>table2</em></span></span></p></td>
<td><p><span data-ttu-id="c3f15-111">Nom des tables dont les enregistrements sont combinés.</span><span class="sxs-lookup"><span data-stu-id="c3f15-111">The names of the tables from which records are combined.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="c3f15-112"><em>champ1</em>, <em>champ2</em></span><span class="sxs-lookup"><span data-stu-id="c3f15-112"><em>field1</em>  ,  <em>field2</em></span></span></p></td>
<td><p><span data-ttu-id="c3f15-p101">Noms des champs joints. S'ils ne sont pas numériques, les champs doivent être du même type et contenir le même type de données, mais il ne doivent pas obligatoirement avoir le même nom.</span><span class="sxs-lookup"><span data-stu-id="c3f15-p101">The names of the fields that are joined. If they are not numeric, the fields must be of the same data type and contain the same kind of data, but they do not have to have the same name.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="c3f15-115"><em>oprcomp</em></span><span class="sxs-lookup"><span data-stu-id="c3f15-115"><em>compopr</em></span></span></p></td>
<td><p><span data-ttu-id="c3f15-116">Tout opérateur de comparaison relationnelles : &quot;=,&quot; &quot;&lt;,&quot; &quot;&gt;,&quot; &quot;&lt;=,&quot; &quot;&gt;=,&quot; ou &quot;&lt;&gt;.&quot;</span><span class="sxs-lookup"><span data-stu-id="c3f15-116">Any relational comparison operator: &quot;=,&quot; &quot;&lt;,&quot; &quot;&gt;,&quot; &quot;&lt;=,&quot; &quot;&gt;=,&quot; or &quot;&lt;&gt;.&quot;</span></span></p></td>
</tr>
</tbody>
</table>


## <a name="remarks"></a><span data-ttu-id="c3f15-117">Remarques</span><span class="sxs-lookup"><span data-stu-id="c3f15-117">Remarks</span></span>

<span data-ttu-id="c3f15-p102">Vous pouvez utiliser une opération INNER JOIN dans n'importe quelle clause [FROM](https://docs.microsoft.com/office/vba/access/Concepts/Structured-Query-Language/from-clause-microsoft-access-sql). Il s'agit du type de jointure le plus courant. Les jointures internes combinent les enregistrements de deux tables lorsque des valeurs correspondent dans un champ commun aux deux tables.</span><span class="sxs-lookup"><span data-stu-id="c3f15-p102">You can use an INNER JOIN operation in any [FROM](https://docs.microsoft.com/office/vba/access/Concepts/Structured-Query-Language/from-clause-microsoft-access-sql) clause. This is the most common type of join. Inner joins combine records from two tables whenever there are matching values in a field common to both tables.</span></span>

<span data-ttu-id="c3f15-p103">Vous pouvez utiliser INNER JOIN avec les tables Departments et Employees pour sélectionner tous les employés dans chaque service. En revanche, pour sélectionner tous les services (même si aucun employé n'est affecté à certains services) ou tous les employés (même si certains d'entre eux ne sont pas affectés à un service), vous pouvez utiliser une opération [LEFT JOIN ou RIGHT JOIN](left-join-right-join-operations-microsoft-access-sql.md) afin de créer une jointure externe.</span><span class="sxs-lookup"><span data-stu-id="c3f15-p103">You can use INNER JOIN with the Departments and Employees tables to select all the employees in each department. In contrast, to select all departments (even if some have no employees assigned to them) or all employees (even if some are not assigned to a department), you can use a [LEFT JOIN or RIGHT JOIN](left-join-right-join-operations-microsoft-access-sql.md) operation to create an outer join.</span></span>

<span data-ttu-id="c3f15-123">Si vous essayez de joindre des champs contenant des données de type Mémo ou Objet OLE, une erreur se produit.</span><span class="sxs-lookup"><span data-stu-id="c3f15-123">If you try to join fields containing Memo or OLE Object data, an error occurs.</span></span>

<span data-ttu-id="c3f15-p104">Vous pouvez joindre deux champs numériques quelconques de types similaires. Par exemple, vous pouvez opérer une jointure sur des champs NuméroAuto et Long parce qu’ils sont de types similaires. En revanche, vous ne pouvez pas joindre des types de champs Simple et Double.</span><span class="sxs-lookup"><span data-stu-id="c3f15-p104">You can join any two numeric fields of like types. For example, you can join on AutoNumber and Long fields because they are like types. However, you cannot join Single and Double types of fields.</span></span>

<span data-ttu-id="c3f15-127">L’exemple suivant montre comment joindre les tables Categories (Catégories) et Products (Produits) sur le champ CategoryID :</span><span class="sxs-lookup"><span data-stu-id="c3f15-127">The following example shows how you could join the Categories and Products tables on the CategoryID field:</span></span>

```sql
SELECT CategoryName, ProductName 
FROM Categories INNER JOIN Products 
ON Categories.CategoryID = Products.CategoryID;
```

<span data-ttu-id="c3f15-128">Dans l'exemple précédent, CategoryID est le champ joint, mais il n'est pas inclus dans le résultat de la requête, car il n'est pas inclus dans l'instruction [SELECT](select-statement-microsoft-access-sql.md).</span><span class="sxs-lookup"><span data-stu-id="c3f15-128">In the preceding example, CategoryID is the joined field, but it is not included in the query output because it is not included in the [SELECT](select-statement-microsoft-access-sql.md) statement.</span></span> <span data-ttu-id="c3f15-129">Pour inclure le champ joint, incluez le nom du champ dans l’instruction SELECT : dans ce cas, Categories.CategoryID.</span><span class="sxs-lookup"><span data-stu-id="c3f15-129">To include the joined field, include the field name in the SELECT statement — in this case, Categories.CategoryID.</span></span>

<span data-ttu-id="c3f15-130">Vous pouvez également lier plusieurs clauses ON dans une instruction JOIN, en utilisant la syntaxe suivante :</span><span class="sxs-lookup"><span data-stu-id="c3f15-130">You can also link several ON clauses in a JOIN statement, using the following syntax:</span></span>

<span data-ttu-id="c3f15-131">SELECT *fields* FROM *table1* INNER JOIN *table2* ON *table1*.*champ1* *compopr* *table2*.*champ1* AND ON *table1*.*champ2* *compopr* *table2*.*champ2*) OR ON *table1*.*champ3* *compopr* *table2*.*champ3*)\];</span><span class="sxs-lookup"><span data-stu-id="c3f15-131">SELECT *fields* 
FROM *table1* INNER JOIN *table2* 
ON *table1*.*field1 \* *compopr \* *table2*.*field1* AND 
ON *table1*.*field2 \* *compopr \* *table2*.*field2*) OR 
ON *table1*.*field3 \* *compopr \* *table2*.*field3*)];</span></span>

<span data-ttu-id="c3f15-132">Vous pouvez également imbriquer des instructions JOIN en utilisant la syntaxe suivante :</span><span class="sxs-lookup"><span data-stu-id="c3f15-132">You can also nest JOIN statements using the following syntax:</span></span>

<span data-ttu-id="c3f15-133">SELECT *champ* FROM *table1* INNER JOIN (*table2* INNER JOIN \[( \]*table3* \[INNER JOIN \[( \]*tablex* \[INNER JOIN …)\] ON *table3*.*champ3* *compopr* *tablex*.*champx*)\] ON *table2*.*champ2* *compopr* *table3*.*champ3*) ON *table1*.*champ1* *compopr* *table2*.*champ2*;</span><span class="sxs-lookup"><span data-stu-id="c3f15-133">SELECT fields 
FROM table1 INNER JOIN 
(table2 INNER JOIN [( ]table3 
[INNER JOIN [( ]tablex [INNER JOIN …)]  
ON table3.field3  compopr  tablex.fieldx)] 
ON table2.field2  compopr  table3.field3)  
ON table1.field1  compopr  table2.field2;</span></span>

<span data-ttu-id="c3f15-134">Une jointure gauche (LEFT JOIN) ou droite (RIGHT JOIN) peut être imbriquée dans une jointure interne, mais une jointure interne ne peut pas être imbriquée dans une jointure gauche ou droite.</span><span class="sxs-lookup"><span data-stu-id="c3f15-134">A LEFT JOIN or a RIGHT JOIN may be nested inside an INNER JOIN, but an INNER JOIN may not be nested inside a LEFT JOIN or a RIGHT JOIN.</span></span>

## <a name="example"></a><span data-ttu-id="c3f15-135">Exemple</span><span class="sxs-lookup"><span data-stu-id="c3f15-135">Example</span></span>

<span data-ttu-id="c3f15-p106">Dans cet exemple, deux jointures équivalentes sont créées : une entre les tables Order Details et Orders et une autre entre les tables Orders et Employees. Ceci est nécessaire, car la table Employees ne contient pas de données de ventes et la table Order Details ne contient pas de données relatives aux employés. La requête produit une liste des employés avec le montant total de leurs ventes.</span><span class="sxs-lookup"><span data-stu-id="c3f15-p106">This example creates two equi-joins: one between the Order Details and Orders tables and another between the Orders and Employees tables. This is necessary because the Employees table does not contain sales data, and the Order Details table does not contain employee data. The query produces a list of employees and their total sales.</span></span>

<span data-ttu-id="c3f15-139">Cet exemple appelle la procédure EnumFields, que vous trouverez dans l’exemple d’instruction SELECT.</span><span class="sxs-lookup"><span data-stu-id="c3f15-139">This example calls the EnumFields procedure, which you can find in the SELECT statement example.</span></span>

```vb
    Sub InnerJoinX() 
     
        Dim dbs As Database, rst As Recordset 
     
        ' Modify this line to include the path to Northwind 
        ' on your computer. 
        Set dbs = OpenDatabase("Northwind.mdb") 
         
        ' Create a join between the Order Details and  
        ' Orders tables and another between the Orders and  
        ' Employees tables. Get a list of employees and  
        ' their total sales. 
        Set rst = dbs.OpenRecordset("SELECT DISTINCTROW " _ 
            & "Sum(UnitPrice * Quantity) AS Sales, " _ 
            & "(FirstName & Chr(32) & LastName) AS Name " _ 
            & "FROM Employees INNER JOIN(Orders " _ 
            & "INNER JOIN [Order Details] " _ 
            & "ON [Order Details].OrderID = " _ 
            & "Orders.OrderID ) " _ 
            & "ON Orders.EmployeeID = " _ 
            & "Employees.EmployeeID " _ 
            & "GROUP BY (FirstName & Chr(32) & LastName);") 
         
        ' Populate the Recordset. 
        rst.MoveLast 
         
        ' Call EnumFields to print the contents of the  
        ' Recordset. Pass the Recordset object and desired 
        ' field width. 
        EnumFields rst, 20 
     
        dbs.Close 
     
    End Sub
```
