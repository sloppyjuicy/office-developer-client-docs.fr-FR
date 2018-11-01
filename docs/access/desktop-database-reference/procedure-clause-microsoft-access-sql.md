---
title: PROCEDURE, clause (Microsoft Access SQL)
TOCTitle: PROCEDURE Clause (Microsoft Access SQL)
ms:assetid: a718802c-9260-88d5-ec29-d5e5594927b0
ms:mtpsurl: https://msdn.microsoft.com/library/Ff821342(v=office.15)
ms:contentKeyID: 48546872
ms.date: 09/18/2015
mtps_version: v=office.15
f1_keywords:
- jetsql40.chm5277578
dev_langs:
- sql
f1_categories:
- Office.Version=v15
ms.openlocfilehash: 63b38a469c5de60588783381c24c61296b177bdd
ms.sourcegitcommit: c557bbcccf37a6011f89aae1ddd399dfe549d087
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 10/31/2018
ms.locfileid: "25877988"
---
# <a name="procedure-clause-microsoft-access-sql"></a>PROCEDURE, clause (Microsoft Access SQL)

**S’applique à**: Access 2013, Office 2013

Définit un nom et des paramètres facultatifs pour une requête.

> [!NOTE]
> [!REMARQUE] La clause PROCEDURE a été remplacée par l'instruction PROCEDURE. Bien que la clause PROCEDURE demeure prise en charge, l'instruction PROCEDURE étend les possibilités de la clause PROCEDURE et constitue la syntaxe recommandée.

## <a name="syntax"></a>Syntaxe

*Nom* de la procédure \[ *param1 type de données*\[, *param2 type de données*\[,...\]\]

La clause PROCEDURE est composée des arguments suivants :

|Argument |Description |
|:----|:-----------|
|*name* |Nom donné à la procédure. Ce nom doit respecter les conventions d'affectation des noms standard.|
|*param1*, *param2* |Un ou plusieurs noms de champ ou paramètres. Par exemple :
<br/><br/>`PROCEDURE Sales_By_Country [Beginning Date] DateTime, [Ending Date] DateTime;`<br/><br/>Pour plus d’informations sur les paramètres, voir [paramètres](parameters-declaration-microsoft-access-sql.md).|
|*typedonnées* | Un des principaux [types de données Microsoft Access SQL](sql-data-types.md) ou un de leurs synonymes. |


## <a name="remarks"></a>Notes

Une procédure SQL se compose d'une clause PROCEDURE (qui spécifie le nom de la procédure), d'une liste facultative de définitions de paramètres et d'une seule instruction SQL. Par exemple, la procédure Get\_composant\_nombre peut s’exécuter une requête qui Récupère un nombre spécifié de composant.

> [!NOTE]
> - Si la clause comporte plusieurs définitions de champ (autrement dit, des paires *param-typedonnées* ), séparez-les par des virgules.
> - La clause PROCEDURE doit être suivie d'une instruction SQL (par exemple une instruction [SELECT](select-statement-microsoft-access-sql.md) ou [UPDATE](update-statement-microsoft-access-sql.md)).

## <a name="example"></a>Exemple

Cet exemple, la requête categoryList est nommée et la procédure EnumFields que vous pouvez trouver dans l’exemple d’instruction SELECT.

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
        EnumFields rst, 15 
         
        ' Delete the QueryDef because this is a 
        ' demonstration. 
        dbs.QueryDefs.Delete "NewQry" 
         
        dbs.Close 
     
    End Sub
```
