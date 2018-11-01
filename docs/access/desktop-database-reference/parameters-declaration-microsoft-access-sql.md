---
title: PARAMETERS, déclaration (Microsoft Access SQL)
TOCTitle: PARAMETERS Declaration (Microsoft Access SQL)
ms:assetid: 0dcaad68-6a5f-93dc-e62a-b82b36e1e69c
ms:mtpsurl: https://msdn.microsoft.com/library/Ff845220(v=office.15)
ms:contentKeyID: 48543230
ms.date: 09/18/2015
mtps_version: v=office.15
f1_keywords:
- jetsql40.chm5277577
dev_langs:
- sql
f1_categories:
- Office.Version=v15
ms.openlocfilehash: 24212ce3a29c0e30fae1dad7566ef93815f8a03f
ms.sourcegitcommit: c557bbcccf37a6011f89aae1ddd399dfe549d087
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 10/31/2018
ms.locfileid: "25876776"
---
# <a name="parameters-declaration-microsoft-access-sql"></a>PARAMETERS, déclaration (Microsoft Access SQL)


**S’applique à**: Access 2013, Office 2013

Déclare le nom et le type de données de chaque paramètre d'une requête Paramètre.

## <a name="syntax"></a>Syntaxe

PARAMETERS *nom typedonnées* \[, *nom typedonnées* \[,...\]\]

La déclaration PARAMETERS est composée des arguments suivants :

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
<td><p><em>nom</em></p></td>
<td><p>Nom du paramètre. Affecté à la propriété <strong>Name</strong> de l'objet <strong>Parameter</strong> et servant à identifier ce paramètre dans la collection <strong>Parameters</strong>. Vous pouvez utiliser le <em>nom</em> sous forme de chaîne qui est affichée dans une boîte de dialogue pendant que votre application exécute la requête. Utilisez des crochets ([ ]) pour encadrer les textes contenant des espaces ou des signes de ponctuation. Par exemple, [prix bas] et [lancer l’état avec les month?] sont des arguments valides de <em>nom</em> .</p></td>
</tr>
<tr class="even">
<td><p><em>typedonnées</em></p></td>
<td><p>Un des principaux <a href="sql-data-types.md">types de données Microsoft Access SQL</a> ou un de leurs synonymes.</p></td>
</tr>
</tbody>
</table>


## <a name="remarks"></a>Notes

Pour les requêtes que vous exécutez régulièrement, vous pouvez utiliser une déclaration PARAMETERS pour créer une requête Paramètre. La création d'une requête Paramètre peut faciliter l'automatisation du processus de modification des critères de requête. Avec une requête Paramètre, votre code devra fournir les paramètres à chaque exécution de la requête.

La déclaration PARAMETERS est facultative mais précède, lorsqu'elle est incluse, toute autre instruction, y compris l'instruction [SELECT](select-statement-microsoft-access-sql.md).

Si la déclaration implique plusieurs paramètres, séparez-les par des virgules. Dans l'exemple qui suit, les paramètres sont au nombre de deux :

```sql
PARAMETERS [Low price] Currency, [Beginning date] DateTime;
```

Vous pouvez utiliser *nom* mais pas le *type de données* dans une clause [WHERE](https://msdn.microsoft.com/library/ff195245\(v=office.15\)) ou [HAVING](https://msdn.microsoft.com/library/ff193795\(v=office.15\)) . L'exemple suivant attend deux paramètres, puis applique les critères aux enregistrements de la table Orders :

```sql
PARAMETERS [Low price] Currency, 
[Beginning date] DateTime; 
SELECT OrderID, OrderAmount
FROM Orders 
WHERE OrderAmount > [Low price] 
AND OrderDate >= [Beginning date];
```

## <a name="example"></a>Exemple

Dans l'exemple suivant, l'utilisateur doit fournir un nom de poste qui est ensuite utilisé comme critère de la requête.

Cet exemple appelle la procédure EnumFields que vous pouvez trouver dans l'exemple d'instruction [SELECT](select-statement-microsoft-access-sql.md).

```vb
    Sub ParametersX() 
     
        Dim dbs As Database, qdf As QueryDef 
        Dim rst As Recordset 
        Dim strSql As String, strParm As String 
        Dim strMessage As String 
        Dim intCommand As Integer 
         
        ' Modify this line to include the path to Northwind 
        ' on your computer. 
        Set dbs = OpenDatabase("NorthWind.mdb") 
         
        ' Define the parameters clause. 
        strParm = "PARAMETERS [Employee Title] CHAR; " 
     
        ' Define an SQL statement with the parameters 
        ' clause. 
        strSql = strParm & "SELECT LastName, FirstName, " _ 
            & "EmployeeID " _ 
            & "FROM Employees " _ 
            & "WHERE Title =[Employee Title];" 
         
        ' Create a QueryDef object based on the  
        ' SQL statement. 
        Set qdf = dbs.CreateQueryDef _ 
            ("Find Employees", strSql) 
         
        Do While True 
            strMessage = "Find Employees by Job " _ 
                & "title:" & Chr(13) _ 
                & "  Choose Job Title:" & Chr(13) _ 
                & "   1 - Sales Manager" & Chr(13) _ 
                & "   2 - Sales Representative" & Chr(13) _ 
                & "   3 - Inside Sales Coordinator" 
             
            intCommand = Val(InputBox(strMessage)) 
             
            Select Case intCommand 
                Case 1 
                    qdf("Employee Title") = _ 
                        "Sales Manager" 
                Case 2 
                    qdf("Employee Title") = _ 
                        "Sales Representative" 
                Case 3 
                    qdf("Employee Title") = _ 
                        "Inside Sales Coordinator" 
                Case Else 
                    Exit Do 
            End Select 
             
            ' Create a temporary snapshot-type Recordset. 
            Set rst = qdf.OpenRecordset(dbOpenSnapshot) 
     
            ' Populate the Recordset. 
            rst.MoveLast 
                 
            ' Call EnumFields to print the contents of the  
            ' Recordset. Pass the Recordset object and desired 
            ' field width. 
            EnumFields rst, 12 
     
        Loop 
         
        ' Delete the QueryDef because this is a 
        ' demonstration. 
        dbs.QueryDefs.Delete "Find Employees" 
         
        dbs.Close 
     
    End Sub
```
