---
title: CREATE PROCEDURE, instruction (Microsoft Access SQL)
TOCTitle: CREATE PROCEDURE statement (Microsoft Access SQL)
ms:assetid: 1fbb5267-9862-bfb4-6436-176152d7a6cd
ms:mtpsurl: https://msdn.microsoft.com/library/Ff845861(v=office.15)
ms:contentKeyID: 48543649
ms.date: 10/18/2018
mtps_version: v=office.15
dev_langs:
- sql
localization_priority: Priority
ms.openlocfilehash: f223e164bd36a6a1a76140a28dd57cd2005e4a20
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: HT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32295401"
---
# <a name="create-procedure-statement-microsoft-access-sql"></a>CREATE PROCEDURE, instruction (Microsoft Access SQL)

**S’applique à** : Access 2013, Office 2013 

Crée une procédure stockée.

> [!NOTE]
> Le moteur de base de données Microsoft Access ne prend pas en charge l'instruction CREATE PROCEDURE, ni les instructions DDL, avec des bases de données autres que celles de type Microsoft Jet.

## <a name="syntax"></a>Syntaxe

CREATE PROCEDURE *procedure* \[*param1 datatype*\[, *param2 datatype*\[, …\]\] AS sqlstatement

L’instruction CREATE PROCEDURE comprend les parties suivantes :

|Quitter|Description|
|:---|:----------|
|*procedure*|Nom de la procédure. Ce nom doit respecter les conventions d'affectation des noms standard.|
|*param1*, *param2*|De un à 255 noms de champs ou paramètres. Par exemple :<br/><br/>`CREATE PROCEDURE Sales_By_Country [Beginning Date] DateTime, [Ending Date] DateTime;`<br/><br/>Pour plus d’informations sur les paramètres, voir [PARAMETERS](parameters-declaration-microsoft-access-sql.md).|
|*datatype*|Un des principaux [types de données Microsoft Access SQL](sql-data-types.md) ou un de leurs synonymes.|
|*sqlstatement*|Instruction SQL telle que SELECT, UPDATE, DELETE, INSERT, CREATE TABLE, DROP TABLE, etc.|


## <a name="remarks"></a>Remarques

Une procédure SQL se compose d’une clause PROCEDURE (spécifiant le nom de la procédure), d’une liste facultative de définitions de paramètres et d’une instruction SQL unique.

Le nom d’une procédure ne peut pas être identique au nom d’une table existante.

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
        EnumFields rst, 15 
         
        ' Delete the QueryDef because this is a 
        ' demonstration. 
        dbs.QueryDefs.Delete "NewQry" 
         
        dbs.Close 
     
    End Sub
```
