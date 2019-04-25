---
title: TRANSFORM, instruction (Microsoft Access SQL)
TOCTitle: TRANSFORM statement (Microsoft Access SQL)
ms:assetid: 419770b1-c833-959d-a84d-56c68764799f
ms:mtpsurl: https://msdn.microsoft.com/library/Ff192901(v=office.15)
ms:contentKeyID: 48544455
ms.date: 10/18/2018
mtps_version: v=office.15
f1_keywords:
- jetsql40.chm5277581
f1_categories:
- Office.Version=v15
localization_priority: Priority
ms.openlocfilehash: 9abe91d4ce6996a725e246da6922015d15a8bd39
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: HT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32314041"
---
# <a name="transform-statement-microsoft-access-sql"></a><span data-ttu-id="8b901-102">TRANSFORM, instruction (Microsoft Access SQL)</span><span class="sxs-lookup"><span data-stu-id="8b901-102">TRANSFORM Statement (Microsoft Access SQL)</span></span>

<span data-ttu-id="8b901-103">**S’applique à** : Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="8b901-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="8b901-104">Créer une requête Analyse croisée</span><span class="sxs-lookup"><span data-stu-id="8b901-104">Creates a crosstab query.</span></span>

## <a name="syntax"></a><span data-ttu-id="8b901-105">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="8b901-105">Syntax</span></span>

<span data-ttu-id="8b901-106">TRANSFORM *aggfunctionselectstatement* PIVOT *pivotfield* \[IN (*value1*\[, *value2*\[, …\]\])\]</span><span class="sxs-lookup"><span data-stu-id="8b901-106">TRANSFORM aggfunction selectstatement
    PIVOT pivotfield [IN (value1[, value2[, …]])]</span></span>

<span data-ttu-id="8b901-107">L’instruction TRANSFORM est composée des éléments suivants :</span><span class="sxs-lookup"><span data-stu-id="8b901-107">The TRANSFORM statement has these parts:</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="8b901-108">Quitter</span><span class="sxs-lookup"><span data-stu-id="8b901-108">Part</span></span></p></th>
<th><p><span data-ttu-id="8b901-109">Description</span><span class="sxs-lookup"><span data-stu-id="8b901-109">Description</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="8b901-110"><em>aggfunction</em></span><span class="sxs-lookup"><span data-stu-id="8b901-110"><em>aggfunction</em></span></span></p></td>
<td><p><span data-ttu-id="8b901-111">Fonction d’agrégation SQL qui s’applique aux données sélectionnées.</span><span class="sxs-lookup"><span data-stu-id="8b901-111">An <a href="sql-aggregate-functions-sql.md">SQL aggregate function</a> that operates on the selected data.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="8b901-112"><em>selectstatement</em></span><span class="sxs-lookup"><span data-stu-id="8b901-112">AS <em>selectstatement</em></span></span></p></td>
<td><p><span data-ttu-id="8b901-113">Instruction SELECT.</span><span class="sxs-lookup"><span data-stu-id="8b901-113">A <a href="select-statement-microsoft-access-sql.md">SELECT</a> statement.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="8b901-114"><em>pivotfield</em></span><span class="sxs-lookup"><span data-stu-id="8b901-114"><em>PivotField</em></span></span></p></td>
<td><p><span data-ttu-id="8b901-115">Champ ou  que vous souhaitez utiliser pour créer des en-têtes de colonne dans le jeu de résultats de la requête.</span><span class="sxs-lookup"><span data-stu-id="8b901-115">The field or expression you want to use to create column headings in the query's result set.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="8b901-116"><em>value1</em>, <em>value2</em></span><span class="sxs-lookup"><span data-stu-id="8b901-116"><em>value1</em>, <em>value2</em></span></span></p></td>
<td><p><span data-ttu-id="8b901-117">Valeurs fixes utilisées pour créer des en-têtes de colonne.</span><span class="sxs-lookup"><span data-stu-id="8b901-117">Fixed values used to create column headings.</span></span></p></td>
</tr>
</tbody>
</table>

## <a name="remarks"></a><span data-ttu-id="8b901-118">Remarques</span><span class="sxs-lookup"><span data-stu-id="8b901-118">Remarks</span></span>

<span data-ttu-id="8b901-119">Lorsque vous synthétisez les données à l’aide d’une requête Analyse croisée, vous sélectionnez des valeurs dans les champs ou expressions spécifiés comme en-têtes de colonne afin de pouvoir afficher les données dans un format plus compact qu’avec une .</span><span class="sxs-lookup"><span data-stu-id="8b901-119">When you summarize data using a crosstab query, you select values from specified fields or expressions as column headings so you can view data in a more compact format than with a select query.</span></span>

<span data-ttu-id="8b901-p101">L’instruction TRANSFORM est facultative, mais lorsqu’elle est incluse, il s’agit de la première instruction d’une chaîne SQL. Elle précède une instruction SELECT qui spécifie les champs utilisés comme en-têtes de ligne, et une clause GROUP BY qui spécifie le regroupement des lignes. Vous pouvez également inclure d’autres clauses, telles que WHERE, pour spécifier des critères de sélection ou de tri supplémentaires. Vous pouvez aussi utiliser des sous-requêtes comme prédicats (celles disponibles dans la clause WHERE) dans une requête Analyse croisée.</span><span class="sxs-lookup"><span data-stu-id="8b901-p101">TRANSFORM is optional but when included is the first statement in an SQL string. It precedes a SELECT statement that specifies the fields used as row headings and a [GROUP BY](https://docs.microsoft.com/office/vba/access/Concepts/Structured-Query-Language/group-by-clause-microsoft-access-sql) clause that specifies row grouping. Optionally, you can include other clauses, such as [WHERE](https://docs.microsoft.com/office/vba/access/Concepts/Structured-Query-Language/where-clause-microsoft-access-sql), that specify additional selection or sorting criteria. You can also use subqueries as predicates — specifically, those in the WHERE clause — in a crosstab query.</span></span>

<span data-ttu-id="8b901-p102">Les valeurs renvoyées dans *pivotfield* sont utilisées comme en-têtes de colonne dans le jeu de résultats de la requête. Par exemple, le croisement dynamique des chiffres de ventes du mois dans une requête Analyse croisée permet de créer 12 colonnes. Vous pouvez restreindre *pivotfield* pour créer des en-têtes à partir des valeurs fixes (*value1*, *value2*) répertoriées dans la clause facultative IN. Vous pouvez également inclure des valeurs fixes pour lesquelles aucune donnée n’existe afin de créer des colonnes supplémentaires.</span><span class="sxs-lookup"><span data-stu-id="8b901-p102">The values returned in *pivotfield* are used as column headings in the query's result set. For example, pivoting the sales figures on the month of the sale in a crosstab query would create 12 columns. You can restrict *pivotfield* to create headings from fixed values (*value1*, *value2* ) listed in the optional IN clause. You can also include fixed values for which no data exists to create additional columns.</span></span>

## <a name="example"></a><span data-ttu-id="8b901-128">Exemple</span><span class="sxs-lookup"><span data-stu-id="8b901-128">Example</span></span>

<span data-ttu-id="8b901-p103">Cet exemple utilise la clause SQL transformer pour créer une requête analyse croisée affichant le nombre de commandes prises par chaque employé pour chaque trimestre calendrier 1994. La fonction SQLTRANSFORMOutput est requise pour exécuter cette procédure.</span><span class="sxs-lookup"><span data-stu-id="8b901-p103">This example uses the SQL TRANSFORM clause to create a crosstab query showing the number of orders taken by each employee for each calendar quarter of 1994. The SQLTRANSFORMOutput function is required for this procedure to run.</span></span>

```vb
    Sub TransformX1() 
     
        Dim dbs As Database 
        Dim strSQL As String 
        Dim qdfTRANSFORM As QueryDef 
     
        strSQL = "PARAMETERS prmYear SHORT; TRANSFORM " _ 
            & "Count(OrderID) " _ 
            & "SELECT FirstName & "" "" & LastName AS " _ 
            & "FullName FROM Employees INNER JOIN Orders " _ 
            & "ON Employees.EmployeeID = " _ 
            & "Orders.EmployeeID WHERE DatePart " _ 
            & "(""yyyy"", OrderDate) = [prmYear] " 
       
           strSQL = strSQL & "GROUP BY FirstName & " _ 
            & """ "" & LastName " _ 
            & "ORDER BY FirstName & "" "" & LastName " _ 
            & "PIVOT DatePart(""q"", OrderDate)" 
         
        ' Modify this line to include the path to Northwind 
        ' on your computer. 
        Set dbs = OpenDatabase("Northwind.mdb") 
     
        Set qdfTRANSFORM = dbs.CreateQueryDef _ 
            ("", strSQL) 
         
        SQLTRANSFORMOutput qdfTRANSFORM, 1994 
         
        dbs.Close 
     
    End Sub
```

<br/>

<span data-ttu-id="8b901-p104">Cet exemple utilise la clause SQL transformer pour créer une requête analyse croisée légèrement plus complexe montrant le montant en euros total des commandes prises par chaque employé pour chaque trimestre calendrier 1994. La fonction SQLTRANSFORMOutput est requise pour exécuter cette procédure.</span><span class="sxs-lookup"><span data-stu-id="8b901-p104">This example uses the SQL TRANSFORM clause to create a slightly more complex crosstab query showing the total dollar amount of orders taken by each employee for each calendar quarter of 1994. The SQLTRANSFORMOutput function is required for this procedure to run.</span></span>

```vb
    Sub TransformX2() 
     
        Dim dbs As Database 
        Dim strSQL As String 
        Dim qdfTRANSFORM As QueryDef 
     
        strSQL = "PARAMETERS prmYear SMALLINT; TRANSFORM " _ 
            & "Sum(Subtotal) SELECT FirstName & "" """ _ 
            & "& LastName AS FullName " _ 
            & "FROM Employees INNER JOIN " _ 
            & "(Orders INNER JOIN [Order Subtotals] " _ 
            & "ON Orders.OrderID = " _ 
            & "[Order Subtotals].OrderID) " _ 
            & "ON Employees.EmployeeID = " _ 
            & "Orders.EmployeeID WHERE DatePart" _ 
            & "(""yyyy"", OrderDate) = [prmYear] " 
        
           strSQL = strSQL & "GROUP BY FirstName & "" """ _ 
            & "& LastName " _ 
            & "ORDER BY FirstName & "" "" & LastName " _ 
            & "PIVOT DatePart(""q"",OrderDate)"         
             
        ' Modify this line to include the path to Northwind 
        ' on your computer. 
        Set dbs = OpenDatabase("Northwind.mdb") 
     
        Set qdfTRANSFORM = dbs.CreateQueryDef _ 
            ("", strSQL) 
         
        SQLTRANSFORMOutput qdfTRANSFORM, 1994 
         
        dbs.Close 
     
    End Sub 
     
    Function SQLTRANSFORMOutput(qdfTemp As QueryDef, _ 
        intYear As Integer) 
         
        Dim rstTRANSFORM As Recordset 
        Dim fldLoop As Field 
        Dim booFirst As Boolean 
     
        qdfTemp.PARAMETERS!prmYear = intYear 
        Set rstTRANSFORM = qdfTemp.OpenRecordset() 
         
        Debug.Print qdfTemp.SQL 
        Debug.Print 
        Debug.Print , , "Quarter" 
     
        With rstTRANSFORM 
            booFirst = True 
            For Each fldLoop In .Fields 
                If booFirst = True Then 
                    Debug.Print fldLoop.Name 
                    Debug.Print , ; 
                    booFirst = False 
                Else 
                    Debug.Print , fldLoop.Name; 
                End If 
            Next fldLoop 
            Debug.Print 
             
            Do While Not .EOF 
                booFirst = True 
                For Each fldLoop In .Fields 
                    If booFirst = True Then 
                        Debug.Print fldLoop 
                        Debug.Print , ; 
                        booFirst = False 
                    Else 
                        Debug.Print , fldLoop; 
                    End If 
                Next fldLoop 
                Debug.Print 
                .MoveNext 
            Loop 
        End With 
         
    End Function
```
