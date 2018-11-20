---
title: Sous-requêtes SQL (Microsoft Access SQL)
TOCTitle: SQL subqueries (Microsoft Access SQL)
ms:assetid: 3b6c0a5d-ab24-e1cf-0175-3f8e68c2dfbf
ms:mtpsurl: https://msdn.microsoft.com/library/Ff192664(v=office.15)
ms:contentKeyID: 48544285
ms.date: 09/18/2015
mtps_version: v=office.15
f1_keywords:
- jetsql40.chm5277580
dev_langs:
- sql
f1_categories:
- Office.Version=v15
ms.openlocfilehash: 4efa4e92d7fab2dc8a4aae932ccb1ffe69c7c6c8
ms.sourcegitcommit: 45feafb3b55de0402dddf5548c0c1c43a0eabafd
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 11/07/2018
ms.locfileid: "26026098"
---
# <a name="sql-subqueries-microsoft-access-sql"></a><span data-ttu-id="a0e1b-102">Sous-requêtes SQL (Microsoft Access SQL)</span><span class="sxs-lookup"><span data-stu-id="a0e1b-102">SQL subqueries (Microsoft Access SQL)</span></span>


<span data-ttu-id="a0e1b-103">**S’applique à**: Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="a0e1b-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="a0e1b-104">Une sous-requête est une instruction [SELECT](select-statement-microsoft-access-sql.md) imbriquée dans une instruction SELECT, [SELECT…INTO](select-into-statement-microsoft-access-sql.md), [INSERT…INTO](insert-into-statement-microsoft-access-sql.md), [DELETE](delete-statement-microsoft-access-sql.md) ou [UPDATE](update-statement-microsoft-access-sql.md) ou imbriquée dans une autre sous-requête.</span><span class="sxs-lookup"><span data-stu-id="a0e1b-104">A subquery is a [SELECT](select-statement-microsoft-access-sql.md) statement nested inside a SELECT, [SELECT…INTO](select-into-statement-microsoft-access-sql.md), [INSERT…INTO](insert-into-statement-microsoft-access-sql.md), [DELETE](delete-statement-microsoft-access-sql.md), or [UPDATE](update-statement-microsoft-access-sql.md) statement or inside another subquery.</span></span>

## <a name="syntax"></a><span data-ttu-id="a0e1b-105">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="a0e1b-105">Syntax</span></span>

<span data-ttu-id="a0e1b-106">Vous pouvez utiliser trois variantes de syntaxe pour créer une sous-requête :</span><span class="sxs-lookup"><span data-stu-id="a0e1b-106">You can use three forms of syntax to create a subquery:</span></span>

<span data-ttu-id="a0e1b-107">*comparaison* \[ANY | TOUS LES | CERTAINS\] (*InstructionSQL*)</span><span class="sxs-lookup"><span data-stu-id="a0e1b-107">*comparison* \[ANY | ALL | SOME\] (*sqlstatement*)</span></span>

<span data-ttu-id="a0e1b-108">*expression* \[Pas\] IN (*InstructionSQL*)</span><span class="sxs-lookup"><span data-stu-id="a0e1b-108">*expression* \[NOT\] IN (*sqlstatement*)</span></span>

<span data-ttu-id="a0e1b-109">\[PAS\] EXISTS (*InstructionSQL*)</span><span class="sxs-lookup"><span data-stu-id="a0e1b-109">\[NOT\] EXISTS (*sqlstatement*)</span></span>

<span data-ttu-id="a0e1b-110">Une sous-requête est composée des arguments suivants :</span><span class="sxs-lookup"><span data-stu-id="a0e1b-110">A subquery has these parts:</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="a0e1b-111">Argument</span><span class="sxs-lookup"><span data-stu-id="a0e1b-111">Part</span></span></p></th>
<th><p><span data-ttu-id="a0e1b-112">Description</span><span class="sxs-lookup"><span data-stu-id="a0e1b-112">Description</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="a0e1b-113"><em>comparaison</em></span><span class="sxs-lookup"><span data-stu-id="a0e1b-113"><em>comparison</em></span></span></p></td>
<td><p><span data-ttu-id="a0e1b-114">Expression et opérateur de comparaison qui compare l'expression avec les résultats de la sous-requête.</span><span class="sxs-lookup"><span data-stu-id="a0e1b-114">An expression and a comparison operator that compares the expression with the results of the subquery.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="a0e1b-115"><em>expression</em></span><span class="sxs-lookup"><span data-stu-id="a0e1b-115"><em>expression</em></span></span></p></td>
<td><p><span data-ttu-id="a0e1b-116">Expression pour laquelle le jeu de résultats de la sous-requête est recherchée.</span><span class="sxs-lookup"><span data-stu-id="a0e1b-116">An expression for which the result set of the subquery is searched.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="a0e1b-117"><em>instructionsql</em></span><span class="sxs-lookup"><span data-stu-id="a0e1b-117"><em>sqlstatement</em></span></span></p></td>
<td><p><span data-ttu-id="a0e1b-p101">Instruction SELECT respectant le même format et les mêmes règles que les autres instructions SELECT. Elle doit figurer entre parenthèses.</span><span class="sxs-lookup"><span data-stu-id="a0e1b-p101">A SELECT statement, following the same format and rules as any other SELECT statement. It must be enclosed in parentheses.</span></span></p></td>
</tr>
</tbody>
</table>


## <a name="remarks"></a><span data-ttu-id="a0e1b-120">Notes</span><span class="sxs-lookup"><span data-stu-id="a0e1b-120">Remarks</span></span>

<span data-ttu-id="a0e1b-p102">Vous pouvez utiliser une sous-requête au lieu d'une expression, dans la liste de champs d'une instruction [WHERE](https://docs.microsoft.com/office/vba/access/Concepts/Structured-Query-Language/where-clause-microsoft-access-sql) ou dans une clause [HAVING](https://docs.microsoft.com/office/vba/access/concepts/structured-query-language/having-clause-microsoft-access-sql). Dans une sous-requête, vous utilisez une instruction SELECT pour fournir un jeu d'une ou plusieurs valeurs spécifiques à évaluer dans l'expression de la clause WHERE ou HAVING.</span><span class="sxs-lookup"><span data-stu-id="a0e1b-p102">You can use a subquery instead of an expression in the field list of a SELECT statement or in a [WHERE](https://docs.microsoft.com/office/vba/access/Concepts/Structured-Query-Language/where-clause-microsoft-access-sql) or [HAVING](https://docs.microsoft.com/office/vba/access/concepts/structured-query-language/having-clause-microsoft-access-sql) clause. In a subquery, you use a SELECT statement to provide a set of one or more specific values to evaluate in the WHERE or HAVING clause expression.</span></span>

<span data-ttu-id="a0e1b-p103">Utilisez les prédicats ANY ou SOME, qui sont synonymes, pour rechercher par comparaison les enregistrements de la requête principale en correspondance avec n'importe quel enregistrement de la sous-requête. Dans l'exemple suivant, la requête renvoie tous les produits dont le prix unitaire est supérieur au prix de n'importe quel produit vendu avec une remise de 25 pour cent ou davantage :</span><span class="sxs-lookup"><span data-stu-id="a0e1b-p103">Use the ANY or SOME predicate, which are synonymous, to retrieve records in the main query that satisfy the comparison with any records retrieved in the subquery. The following example returns all products whose unit price is greater than that of any product sold at a discount of 25 percent or more:</span></span>

```sql
SELECT * FROM Products 
WHERE UnitPrice > ANY 
(SELECT UnitPrice FROM OrderDetails 
WHERE Discount >= .25);
```

<span data-ttu-id="a0e1b-p104">Utilisez le prédicat [ALL](https://docs.microsoft.com/office/vba/access/Concepts/Structured-Query-Language/all-distinct-distinctrow-top-predicates-microsoft-access-sql) pour rechercher par comparaison uniquement les enregistrements de la requête principale en correspondance avec n'importe quel enregistrement de la sous-requête. Si dans l'exemple précédent, vous avez remplacé ANY par ALL, la requête ne renvoie que les produits dont le prix unitaire est supérieur aux prix de tous les produits vendus avec une remise de 25 pourcent ou davantage. La recherche est beaucoup plus restrictive.</span><span class="sxs-lookup"><span data-stu-id="a0e1b-p104">Use the [ALL](https://docs.microsoft.com/office/vba/access/Concepts/Structured-Query-Language/all-distinct-distinctrow-top-predicates-microsoft-access-sql) predicate to retrieve only those records in the main query that satisfy the comparison with all records retrieved in the subquery. If you changed ANY to ALL in the previous example, the query would return only those products whose unit price is greater than that of all products sold at a discount of 25 percent or more. This is much more restrictive.</span></span>

<span data-ttu-id="a0e1b-p105">Utilisez le prédicat IN pour rechercher les enregistrements de la requête principale pour lesquels on trouve des enregistrements avec une valeur identique dans la sous-requête. Dans l'exemple suivant, la requête renvoie tous les produits vendus avec une remise de 25 pour cent ou davantage :</span><span class="sxs-lookup"><span data-stu-id="a0e1b-p105">Use the IN predicate to retrieve only those records in the main query for which some record in the subquery contains an equal value. The following example returns all products with a discount of 25 percent or more:</span></span>

```sql
SELECT * FROM Products 
WHERE ProductID IN 
(SELECT ProductID FROM OrderDetails 
WHERE Discount >= .25);
```

<span data-ttu-id="a0e1b-130">À l'inverse, vous pouvez utiliser le prédicat NOT IN pour rechercher les enregistrements de la requête principale pour lesquels aucun enregistrement avec une ne contient une valeur identique dans la sous-requête.</span><span class="sxs-lookup"><span data-stu-id="a0e1b-130">Conversely, you can use NOT IN to retrieve only those records in the main query for which no record in the subquery contains an equal value.</span></span>

<span data-ttu-id="a0e1b-131">Utilisez le prédicat EXISTS (avec le mot réservé facultatif NOT) dans des comparaisons vrai/faux pour déterminer si la sous-requête renvoie des enregistrements</span><span class="sxs-lookup"><span data-stu-id="a0e1b-131">Use the EXISTS predicate (with the optional NOT reserved word) in true/false comparisons to determine whether the subquery returns any records.</span></span>

<span data-ttu-id="a0e1b-p106">Vous pouvez également utiliser des alias de nom de table dans une sous-requête pour faire référence à des tables répertoriées dans une clause [FROM](https://docs.microsoft.com/office/vba/access/Concepts/Structured-Query-Language/from-clause-microsoft-access-sql) en dehors de la sous-requête. Dans l'exemple suivant, la requête renvoie le nom des employés dont le salaires est supérieur ou égal au salaire moyen de l'ensemble des employés occupant le même poste. L'alias affecté à la table Employees est « T1 » :</span><span class="sxs-lookup"><span data-stu-id="a0e1b-p106">You can also use table name aliases in a subquery to refer to tables listed in a [FROM](https://docs.microsoft.com/office/vba/access/Concepts/Structured-Query-Language/from-clause-microsoft-access-sql) clause outside the subquery. The following example returns the names of employees whose salaries are equal to or greater than the average salary of all employees having the same job title. The Employees table is given the alias "T1":</span></span>

```sql
SELECT LastName,
FirstName, Title, Salary 
FROM Employees AS T1 
WHERE Salary >= (SELECT Avg(Salary) 
FROM Employees 
WHERE T1.Title = Employees.Title) Order by Title;
```

<span data-ttu-id="a0e1b-135">Dans l'exemple précédent, le mot réservé AS est facultatif.</span><span class="sxs-lookup"><span data-stu-id="a0e1b-135">In the preceding example, the AS reserved word is optional.</span></span>

<span data-ttu-id="a0e1b-p107">Certaines sous-requêtes sont autorisées dans les requêtes Analyse croisée mais uniquement comme prédicats (ceux de la clause WHERE). Les sous-requêtes ne sont pas autorisées dans les requêtes Analyse croisée pour ce qui concerne les sorties (dans la liste de SELECT)</span><span class="sxs-lookup"><span data-stu-id="a0e1b-p107">Some subqueries are allowed in crosstab queries— specifically, as predicates (those in the WHERE clause). Subqueries as output (those in the SELECT list) are not allowed in crosstab queries.</span></span>

## <a name="example"></a><span data-ttu-id="a0e1b-138">Exemple</span><span class="sxs-lookup"><span data-stu-id="a0e1b-138">Example</span></span>

<span data-ttu-id="a0e1b-139">Dans cet exemple, le nom et le contact de chaque client, qui a passé une commande dans le second trimestre de 1995, sont fournis.</span><span class="sxs-lookup"><span data-stu-id="a0e1b-139">This example lists the name and contact of every customer who placed an order in the second quarter of 1995.</span></span> <span data-ttu-id="a0e1b-140">Il appelle la procédure EnumFields que vous pouvez trouver dans l’exemple d’instruction SELECT.</span><span class="sxs-lookup"><span data-stu-id="a0e1b-140">It calls the EnumFields procedure, which you can find in the SELECT statement example.</span></span>

```vb
    Sub SubQueryX() 
     
        Dim dbs As Database, rst As Recordset 
     
        ' Modify this line to include the path to Northwind 
        ' on your computer. 
        Set dbs = OpenDatabase("Northwind.mdb") 
         
        ' List the name and contact of every customer  
        ' who placed an order in the second quarter of 
        ' 1995. 
        Set rst = dbs.OpenRecordset("SELECT ContactName," _ 
            & " CompanyName, ContactTitle, Phone" _ 
            & " FROM Customers" _ 
            & " WHERE CustomerID" _ 
            & " IN (SELECT CustomerID FROM Orders" _ 
            & " WHERE OrderDate Between #04/1/95#" _ 
            & " And #07/1/95#);") 
         
        ' Populate the Recordset. 
        rst.MoveLast 
         
        ' Call EnumFields to print the contents of the  
        ' Recordset. Pass the Recordset object and desired 
        ' field width. 
        EnumFields rst, 25 
     
        dbs.Close 
     
    End Sub
```
