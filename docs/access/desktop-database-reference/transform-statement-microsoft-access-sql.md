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
ms.localizationpriority: high
ms.openlocfilehash: 7194b383f5275daf5501f31833ec0a3f68fa58bd
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: HT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/24/2021
ms.locfileid: "59621730"
---
# <a name="transform-statement-microsoft-access-sql"></a>TRANSFORM, instruction (Microsoft Access SQL)

**S’applique à** : Access 2013, Office 2013

Créer une requête Analyse croisée

## <a name="syntax"></a>Syntaxe

TRANSFORM *aggfunctionselectstatement* PIVOT *pivotfield* \[IN (*value1*\[, *value2*\[, …\]\])\]

L’instruction TRANSFORM est composée des éléments suivants :

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p>Quitter</p></th>
<th><p>Description</p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><em>aggfunction</em></p></td>
<td><p>Fonction d’agrégation SQL qui s’applique aux données sélectionnées.</p></td>
</tr>
<tr class="even">
<td><p><em>selectstatement</em></p></td>
<td><p>Instruction SELECT.</p></td>
</tr>
<tr class="odd">
<td><p><em>pivotfield</em></p></td>
<td><p>Champ ou  que vous souhaitez utiliser pour créer des en-têtes de colonne dans le jeu de résultats de la requête.</p></td>
</tr>
<tr class="even">
<td><p><em>value1</em>, <em>value2</em></p></td>
<td><p>Valeurs fixes utilisées pour créer des en-têtes de colonne.</p></td>
</tr>
</tbody>
</table>

## <a name="remarks"></a>Remarques

Lorsque vous synthétisez les données à l’aide d’une requête Analyse croisée, vous sélectionnez des valeurs dans les champs ou expressions spécifiés comme en-têtes de colonne afin de pouvoir afficher les données dans un format plus compact qu’avec une .

L’instruction TRANSFORM est facultative, mais lorsqu’elle est incluse, il s’agit de la première instruction d’une chaîne SQL. Elle précède une instruction SELECT qui spécifie les champs utilisés comme en-têtes de ligne, et une clause GROUP BY qui spécifie le regroupement des lignes. Vous pouvez également inclure d’autres clauses, telles que WHERE, pour spécifier des critères de sélection ou de tri supplémentaires. Vous pouvez aussi utiliser des sous-requêtes comme prédicats (celles disponibles dans la clause WHERE) dans une requête Analyse croisée.

Les valeurs renvoyées dans *pivotfield* sont utilisées comme en-têtes de colonne dans le jeu de résultats de la requête. Par exemple, le croisement dynamique des chiffres de ventes du mois dans une requête Analyse croisée permet de créer 12 colonnes. Vous pouvez restreindre *pivotfield* pour créer des en-têtes à partir des valeurs fixes (*value1*, *value2*) répertoriées dans la clause facultative IN. Vous pouvez également inclure des valeurs fixes pour lesquelles aucune donnée n’existe afin de créer des colonnes supplémentaires.

## <a name="example"></a>Exemple

Cet exemple utilise la clause SQL transformer pour créer une requête analyse croisée affichant le nombre de commandes prises par chaque employé pour chaque trimestre calendrier 1994. La fonction SQLTRANSFORMOutput est requise pour exécuter cette procédure.

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

Cet exemple utilise la clause SQL transformer pour créer une requête analyse croisée légèrement plus complexe montrant le montant en euros total des commandes prises par chaque employé pour chaque trimestre calendrier 1994. La fonction SQLTRANSFORMOutput est requise pour exécuter cette procédure.

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
