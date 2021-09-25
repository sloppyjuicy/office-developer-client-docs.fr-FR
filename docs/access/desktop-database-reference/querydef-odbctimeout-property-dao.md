---
title: Propriété QueryDef.ODBCTimeout (DAO)
TOCTitle: ODBCTimeout Property
ms:assetid: b251c4fb-64a8-aa95-deed-64425df3e00c
ms:mtpsurl: https://msdn.microsoft.com/library/Ff822019(v=office.15)
ms:contentKeyID: 48547166
ms.date: 09/18/2015
mtps_version: v=office.15
f1_keywords:
- dao360.chm1053052
f1_categories:
- Office.Version=v15
ms.localizationpriority: medium
ms.openlocfilehash: a79f403d49db1137d8b67d2dc7fb27b3ea140fc3
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/24/2021
ms.locfileid: "59589238"
---
# <a name="querydefodbctimeout-property-dao"></a>Propriété QueryDef.ODBCTimeout (DAO)


**S’applique à** : Access 2013, Office 2013

Indique le nombre de secondes d'attente avant que ne survienne une erreur d'expiration lors de l'exécution d'un objet **[QueryDef](querydef-object-dao.md)** sur une base de données ODBC.

## <a name="syntax"></a>Syntaxe

*.* ODBCTimeout

*expression* Variable représentant un objet **QueryDef**.

## <a name="remarks"></a>Remarques

Lorsque la propriété **ODBCTimeout** est définie sur -1, le délai d'expiration revient par défaut au paramètre courant de la propriété **[QueryTimeout](database-querytimeout-property-dao.md)** de l'objet **[Connection](connection-object-dao.md)** ou **[Database](database-object-dao.md)** contenant l'objet **QueryDef**. Lorsque la propriété **ODBCTimeout** est définie sur 0, aucune erreur d'expiration ne survient.

Lorsque vous utilisez une base de données ODBC, comme Microsoft SQL Server, des retards peuvent survenir à cause d'un trafic réseau important ou d'une utilisation soutenue du serveur ODBC. Plutôt que d'attendre indéfiniment, vous pouvez définir le délai d'attente avant de renvoyer une erreur.

La définition de la propriété **ODBCTimeout** d'un objet **QueryDef** écrase la valeur spécifiée par la propriété **QueryTimeout** de l'objet **Connection** ou **Database** contenant l'objet **QueryDef**, mais uniquement cet objet **QueryDef**.

## <a name="example"></a>Exemple

Cet exemple utilise les propriétés **ODBCTimeout** et **QueryTimeout** pour montrer comment le paramètre **QueryTimeout** d'un objet **Database** définit le paramètre **ODBCTimeout** par défaut sur tout objet **QueryDef** créé à partir de l'objet **Database**.

```vb 
Sub ODBCTimeoutX() 
 
 Dim dbsCurrent As Database 
 Dim qdfStores As QueryDef 
 Dim rstStores As Recordset 
 
 Set dbsCurrent = OpenDatabase("Northwind.mdb") 
 
 ' Change the default QueryTimeout of the Northwind 
 ' database. 
 Debug.Print "Default QueryTimeout of Database: " & _ 
 dbsCurrent.QueryTimeout 
 dbsCurrent.QueryTimeout = 30 
 Debug.Print "New QueryTimeout of Database: " & _ 
 dbsCurrent.QueryTimeout 
 
 ' Create a new QueryDef object. 
 Set qdfStores = dbsCurrent.CreateQueryDef("Stores", _ 
 "SELECT * FROM stores") 
 
 ' Note: The DSN referenced below must be configured to 
 ' use Microsoft Windows NT Authentication Mode to 
 ' authorize user access to the SQL Server. 
 qdfStores.Connect = _ 
 "ODBC;DATABASE=pubs;DSN=Publishers" 
 
 ' Change the ODBCTimeout setting of the new QueryDef 
 ' object from its default setting. 
 Debug.Print "Default ODBCTimeout of QueryDef: " & _ 
 qdfStores.ODBCTimeout 
 qdfStores.ODBCTimeout = 0 
 Debug.Print "New ODBCTimeout of QueryDef: " & _ 
 qdfStores.ODBCTimeout 
 
 ' Execute the query and display the results. 
 Set rstStores = qdfStores.OpenRecordset() 
 
 Debug.Print "Contents of recordset:" 
 With rstStores 
 Do While Not .EOF 
 Debug.Print , .Fields(0), .Fields(1) 
 .MoveNext 
 Loop 
 .Close 
 End With 
 
 ' Delete new QueryDef because this is a demonstration. 
 dbsCurrent.QueryDefs.Delete qdfStores.Name 
 dbsCurrent.Close 
 
End Sub 
 
```

