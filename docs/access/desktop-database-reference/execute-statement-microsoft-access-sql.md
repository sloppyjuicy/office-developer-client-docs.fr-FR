---
title: EXECUTE, instruction (Microsoft Access SQL)
TOCTitle: EXECUTE statement (Microsoft Access SQL)
ms:assetid: 9ec4d9ee-db2a-0319-3ccf-c035d67a1496
ms:mtpsurl: https://msdn.microsoft.com/library/Ff198330(v=office.15)
ms:contentKeyID: 48546667
ms.date: 10/18/2018
mtps_version: v=office.15
f1_keywords:
- jetsql40.chm5277471
f1_categories:
- Office.Version=v15
ms.localizationpriority: high
ms.openlocfilehash: fda44d6b78b089f144216eb224ff3d2812b528be
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: HT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/24/2021
ms.locfileid: "59612189"
---
# <a name="execute-statement-microsoft-access-sql"></a>EXECUTE, instruction (Microsoft Access SQL)

**S’applique à** : Access 2013, Office 2013

Utilisée pour invoquer l'exécution d'une procédure.

## <a name="syntax"></a>Syntaxe

EXECUTE *procédure* \[*param1*\[, *param2*\[, …\]\]

L’instruction EXECUTE est composée des éléments suivants :

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
<td><p><em>procedure</em></p></td>
<td><p>Nom de la procédure à exécuter.</p></td>
</tr>
<tr class="even">
<td><p><em>param1, param2, …</em></p></td>
<td><p>Valeurs des paramètres définis par la procédure.</p></td>
</tr>
</tbody>
</table>


## <a name="example"></a>Exemple

Cet exemple nomme la requête CategoryList et appelle la procédure EnumFields, que vous pouvez trouver dans l'exemple d'instruction SELECT.

```vb
    Sub ProcedureX() 
     
        Dim dbs As Database, rst As Recordset 
        Dim qdf As QueryDef, strSql As String 
         
        ' Modify this line to include the path to Northwind 
        ' on your computer. 
        Set dbs = OpenDatabase("Northwind.mdb") 
         
        strSql = "PROCEDURE CategoryList; " _ 
            & "SELECT DISTINCTROW CategoryName, " _ 
            & "CategoryID FROM Categories " _ 
            & "ORDER BY CategoryName;" 
         
        ' Create a named QueryDef based on the SQL 
        ' statement. 
        Set qdf = dbs.CreateQueryDef("NewQry", strSql) 
     
        ' Create a temporary snapshot-type Recordset. 
        Set rst = qdf.OpenRecordset(dbOpenSnapshot) 
     
        ' Populate the Recordset. 
        rst.MoveLast 
                 
        ' Call EnumFields to print the contents of the  
        ' Recordset. Pass the Recordset object and desired 
        ' field width. 
        Execute EnumFields rst, 15 
         
        ' Delete the QueryDef because this is a 
        ' demonstration. 
        dbs.QueryDefs.Delete "NewQry" 
         
        dbs.Close 
     
    End Sub
```
