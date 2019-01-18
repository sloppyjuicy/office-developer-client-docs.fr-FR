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
localization_priority: Priority
ms.openlocfilehash: 7beda04d1f18014101f00078de1d125c1fd67a69
ms.sourcegitcommit: d6695c94415fa47952ee7961a69660abc0904434
ms.translationtype: Auto
ms.contentlocale: fr-FR
ms.lasthandoff: 01/17/2019
ms.locfileid: "28722871"
---
# <a name="sql-subqueries-microsoft-access-sql"></a>Sous-requêtes SQL (Microsoft Access SQL)


**S’applique à**: Access 2013, Office 2013

Une sous-requête est une instruction [SELECT](select-statement-microsoft-access-sql.md) imbriquée dans une instruction SELECT, [SELECT…INTO](select-into-statement-microsoft-access-sql.md), [INSERT…INTO](insert-into-statement-microsoft-access-sql.md), [DELETE](delete-statement-microsoft-access-sql.md) ou [UPDATE](update-statement-microsoft-access-sql.md) ou imbriquée dans une autre sous-requête.

## <a name="syntax"></a>Syntaxe

Vous pouvez utiliser trois variantes de syntaxe pour créer une sous-requête :

*comparaison* \[ANY | TOUS LES | CERTAINS\] (*InstructionSQL*)

*expression* \[Pas\] IN (*InstructionSQL*)

\[PAS\] EXISTS (*InstructionSQL*)

Une sous-requête est composée des arguments suivants :

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p>Argument</p></th>
<th><p>Description</p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><em>comparaison</em></p></td>
<td><p>Expression et opérateur de comparaison qui compare l'expression avec les résultats de la sous-requête.</p></td>
</tr>
<tr class="even">
<td><p><em>expression</em></p></td>
<td><p>Expression pour laquelle le jeu de résultats de la sous-requête est recherchée.</p></td>
</tr>
<tr class="odd">
<td><p><em>instructionsql</em></p></td>
<td><p>Instruction SELECT respectant le même format et les mêmes règles que les autres instructions SELECT. Elle doit figurer entre parenthèses.</p></td>
</tr>
</tbody>
</table>


## <a name="remarks"></a>Notes

Vous pouvez utiliser une sous-requête au lieu d'une expression, dans la liste de champs d'une instruction [WHERE](https://docs.microsoft.com/office/vba/access/Concepts/Structured-Query-Language/where-clause-microsoft-access-sql) ou dans une clause [HAVING](https://docs.microsoft.com/office/vba/access/concepts/structured-query-language/having-clause-microsoft-access-sql). Dans une sous-requête, vous utilisez une instruction SELECT pour fournir un jeu d'une ou plusieurs valeurs spécifiques à évaluer dans l'expression de la clause WHERE ou HAVING.

Utilisez les prédicats ANY ou SOME, qui sont synonymes, pour rechercher par comparaison les enregistrements de la requête principale en correspondance avec n'importe quel enregistrement de la sous-requête. Dans l'exemple suivant, la requête renvoie tous les produits dont le prix unitaire est supérieur au prix de n'importe quel produit vendu avec une remise de 25 pour cent ou davantage :

```sql
SELECT * FROM Products 
WHERE UnitPrice > ANY 
(SELECT UnitPrice FROM OrderDetails 
WHERE Discount >= .25);
```

Utilisez le prédicat [ALL](https://docs.microsoft.com/office/vba/access/Concepts/Structured-Query-Language/all-distinct-distinctrow-top-predicates-microsoft-access-sql) pour rechercher par comparaison uniquement les enregistrements de la requête principale en correspondance avec n'importe quel enregistrement de la sous-requête. Si dans l'exemple précédent, vous avez remplacé ANY par ALL, la requête ne renvoie que les produits dont le prix unitaire est supérieur aux prix de tous les produits vendus avec une remise de 25 pourcent ou davantage. La recherche est beaucoup plus restrictive.

Utilisez le prédicat IN pour rechercher les enregistrements de la requête principale pour lesquels on trouve des enregistrements avec une valeur identique dans la sous-requête. Dans l'exemple suivant, la requête renvoie tous les produits vendus avec une remise de 25 pour cent ou davantage :

```sql
SELECT * FROM Products 
WHERE ProductID IN 
(SELECT ProductID FROM OrderDetails 
WHERE Discount >= .25);
```

À l'inverse, vous pouvez utiliser le prédicat NOT IN pour rechercher les enregistrements de la requête principale pour lesquels aucun enregistrement avec une ne contient une valeur identique dans la sous-requête.

Utilisez le prédicat EXISTS (avec le mot réservé facultatif NOT) dans des comparaisons vrai/faux pour déterminer si la sous-requête renvoie des enregistrements

Vous pouvez également utiliser des alias de nom de table dans une sous-requête pour faire référence à des tables répertoriées dans une clause [FROM](https://docs.microsoft.com/office/vba/access/Concepts/Structured-Query-Language/from-clause-microsoft-access-sql) en dehors de la sous-requête. Dans l'exemple suivant, la requête renvoie le nom des employés dont le salaires est supérieur ou égal au salaire moyen de l'ensemble des employés occupant le même poste. L'alias affecté à la table Employees est « T1 » :

```sql
SELECT LastName,
FirstName, Title, Salary 
FROM Employees AS T1 
WHERE Salary >= (SELECT Avg(Salary) 
FROM Employees 
WHERE T1.Title = Employees.Title) Order by Title;
```

Dans l'exemple précédent, le mot réservé AS est facultatif.

Certaines sous-requêtes sont autorisées dans les requêtes Analyse croisée mais uniquement comme prédicats (ceux de la clause WHERE). Les sous-requêtes ne sont pas autorisées dans les requêtes Analyse croisée pour ce qui concerne les sorties (dans la liste de SELECT)

## <a name="example"></a>Exemple

Dans cet exemple, le nom et le contact de chaque client, qui a passé une commande dans le second trimestre de 1995, sont fournis. Il appelle la procédure EnumFields que vous pouvez trouver dans l’exemple d’instruction SELECT.

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
