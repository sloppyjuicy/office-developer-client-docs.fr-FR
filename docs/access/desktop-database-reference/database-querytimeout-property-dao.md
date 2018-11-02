---
title: Propriété Database.QueryTimeout (DAO)
TOCTitle: QueryTimeout Property
ms:assetid: c83ca852-715a-c853-429b-80a15c3fc39b
ms:mtpsurl: https://msdn.microsoft.com/library/Ff823170(v=office.15)
ms:contentKeyID: 48547648
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: d928864d729cdfb40f44d496e983bf86413d57f7
ms.sourcegitcommit: d7248f803002b31cf7fc561b03530199a9b0a8fd
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 11/02/2018
ms.locfileid: "25925274"
---
# <a name="databasequerytimeout-property-dao"></a>Propriété Database.QueryTimeout (DAO)


**S’applique à**: Access 2013, Office 2013


Définit ou retourne une valeur qui spécifie le nombre de secondes d'attente avant qu'une erreur de délai d'attente soit générée lors de l'exécution d'une requête sur une source de données ODBC.

## <a name="syntax"></a>Syntaxe

*expression* . QueryTimeout

*expression* Variable qui représente un objet de **base de données** .

## <a name="remarks"></a>Remarques

La valeur par défaut est 60.

Lorsque vous utilisez une base de données ODBC, telle que Microsoft SQL Server, le trafic réseau ou une utilisation intensive du serveur ODBC peut entraîner des délais. Au lieu d'attendre indéfiniment, vous pouvez définir le délai d'attente.

Si la propriété **QueryTimeout** est utilisée avec un objet **[Connection](connection-object-dao.md)** ou **[Database](database-object-dao.md)**, elle spécifie une valeur globale pour toutes les requêtes associées à la base de données. Vous pouvez remplacer cette valeur pour une requête donnée en paramétrant la propriété **ODBCTimeout** de l'objet **[QueryDef](querydef-object-dao.md)** spécifique.

## <a name="example"></a>Exemple

L'exemple ci-dessous fait appel aux propriétés **ODBCTimeout** et **QueryTimeout** pour indiquer comment le paramètre **QueryTimeout** d'un objet **Database** définit le paramètre **ODBCTimeout** par défaut des objets **QueryDef** créés à partir de l'objet **Database**.

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

