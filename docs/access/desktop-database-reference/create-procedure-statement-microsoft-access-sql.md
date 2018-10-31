---
title: Instruction CREATE PROCEDURE (Microsoft Access SQL)
TOCTitle: CREATE PROCEDURE statement (Microsoft Access SQL)
ms:assetid: 1fbb5267-9862-bfb4-6436-176152d7a6cd
ms:mtpsurl: https://msdn.microsoft.com/library/Ff845861(v=office.15)
ms:contentKeyID: 48543649
ms.date: 10/18/2018
mtps_version: v=office.15
dev_langs:
- sql
ms.openlocfilehash: 573ec86a573697ebe52886535f8544bbaab61d7d
ms.sourcegitcommit: 801b1b54786f7b0e5b0d35466e7ae8d1e840b26f
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 10/31/2018
ms.locfileid: "25861462"
---
# <a name="create-procedure-statement-microsoft-access-sql"></a>Instruction CREATE PROCEDURE (Microsoft Access SQL)

**S’applique à**: Access 2013 | Office 2013 

Crée une procédure stockée.

> [!NOTE]
> [!REMARQUE] Le moteur de base de données Microsoft Access ne prend pas en charge l'instruction CREATE PROCEDURE, ni les instructions DDL, avec des bases de données autres que celles de type Microsoft Jet.

## <a name="syntax"></a>Syntaxe

CREATE PROCEDURE *procédure* \[ *param1 type de données*\[, *param2 type de données*\[,... \] \] InstructionSQL AS

L'instruction CREATE PROCEDURE est composée des arguments suivants :

|Argument|Description|
|:---|:----------|
|*procédure*|Nom donné à la procédure. Ce nom doit respecter les conventions d'affectation des noms standard.|
|*param1*, *param2*|Noms de champs ou paramètres comportant de 1 à 255 caractères. Par exemple :
<br/><br/>`CREATE PROCEDURE Sales_By_Country [Beginning Date] DateTime, [Ending Date] DateTime;`<br/><br/>Pour plus d’informations sur les paramètres, voir [paramètres](parameters-declaration-microsoft-access-sql.md).|
|*typedonnées*|Un des principaux [types de données Microsoft Access SQL](sql-data-types.md) ou un de leurs synonymes.|
|*instructionsql*|Instruction SQL, telle que SELECT, UPDATE, DELETE, INSERT, CREATE TABLE, DROP TABLE, etc.|


## <a name="remarks"></a>Notes

Une procédure SQL se compose d'une clause PROCEDURE qui spécifie le nom de la procédure, d'une liste facultative de définitions de paramètres et d'une instruction SQL.

Le nom d'une procédure ne peut pas être le même que celui d'une table existante.

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
