---
title: TRANSFORM, instruction (Microsoft Access SQL)
TOCTitle: TRANSFORM Statement (Microsoft Access SQL)
ms:assetid: 419770b1-c833-959d-a84d-56c68764799f
ms:mtpsurl: https://msdn.microsoft.com/library/Ff192901(v=office.15)
ms:contentKeyID: 48544455
ms.date: 09/18/2015
mtps_version: v=office.15
f1_keywords:
- jetsql40.chm5277581
f1_categories:
- Office.Version=v15
ms.openlocfilehash: 6d05f278e38cc8cf132cf06605703dfa99eb8728
ms.sourcegitcommit: 19aca09c5812cfb98b68b5d4604dcaa814479df7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 10/09/2018
ms.locfileid: "25471516"
---
# <a name="transform-statement-microsoft-access-sql"></a>TRANSFORM, instruction (Microsoft Access SQL)

**S’applique à**: Access 2013 | Office 2013

Crée une requête Analyse croisée.

## <a name="syntax"></a>Syntaxe

TRANSFORM *fonctionagrégationinstructionselect* PIVOT *pivotfield* \[IN (*valeur1*\[, *valeur2*\[,... \]\])\]

L'instruction TRANSFORM est composée des arguments suivants :

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
<td><p><em>fonctionagrégation</em></p></td>
<td><p><a href="sql-aggregate-functions-sql.md">Fonction d’agrégation SQL</a> agissant sur les données sélectionnées.</p></td>
</tr>
<tr class="even">
<td><p><em>instructionselect</em></p></td>
<td><p>Une instruction <a href="select-statement-microsoft-access-sql.md">SELECT</a>.</p></td>
</tr>
<tr class="odd">
<td><p><em>champpivot</em></p></td>
<td><p>Champ ou expression que vous voulez utilisez pour créer les en-têtes de colonne dans le jeu de résultats de la requête.</p></td>
</tr>
<tr class="even">
<td><p><em>valeur1</em>, <em>valeur2</em></p></td>
<td><p>Valeurs fixes utilisées pour créer des en-têtes de colonne.</p></td>
</tr>
</tbody>
</table>

## <a name="remarks"></a>Notes

Lorsque vous synthétisez des données à l'aide d'une requête Analyse croisée, vous sélectionnez des valeurs à partir de champs ou d'expressions spécifiés comme en-têtes de colonne. Ainsi, vous pouvez voir les données sous un format plus condensé qu'avec une requête Sélection.

L'instruction TRANSFORM est facultative mais, si elle est employée, elle doit venir en première position dans une chaîne SQL. Elle précède une instruction SELECT, qui spécifie les champs servant d'en-têtes de ligne ainsi qu'une clause [GROUP BY](https://msdn.microsoft.com/library/ff837271\(v=office.15\)) spécifiant le mode de regroupement des lignes. Vous pouvez éventuellement ajouter d'autres clauses, par exemple une clause [WHERE](https://msdn.microsoft.com/library/ff195245\(v=office.15\)) précisant des critères de sélection ou de tri supplémentaires. Vous pouvez aussi utiliser des sous-requêtes comme prédicats, particulièrement ceux dans la clause WHERE, dans une requête Analyse croisée.

Les valeurs renvoyées dans *pivotfield* sont utilisées comme en-têtes de colonne dans le jeu de résultats de la requête. Par exemple, créer une requête Analyse croisée en prenant le mois de vente comme base de sélection pour obtenir les chiffres des ventes produira douze colonnes. Vous pouvez restreindre *pivotfield* pour que les en-têtes ne soient créés qu'à partir des valeurs fixes (*valeur1*, *valeur2* ) répertoriées dans la clause IN facultative. Vous pouvez également ajouter des valeurs fixes sans données correspondantes de manière à créer des colonnes supplémentaires.

## <a name="example"></a>Exemple

Dans cet exemple la clause SQL TRANSFORM est utilisée pour créer une requête Analyse croisée qui indique le nombre de commandes prises par chaque employé pour chaque trimestre de 1994. La fonction SQLTRANSFORMOutput est nécessaire pour que la procédure puisse s'exécuter.

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

Dans cet exemple, la clause SQL TRANSFORM est utilisée pour créer une requête Analyse croisée légèrement plus complexe qui indique le montant total en dollar des commandes prises par chaque employé pour chaque trimestre de 1994. La fonction SQLTRANSFORMOutput est nécessaire pour que la procédure puisse s'exécuter..

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
