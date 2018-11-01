---
title: Recordset.NextRecordset Method (DAO)
TOCTitle: NextRecordset Method
ms:assetid: 4a3a6176-0aa0-efb6-b175-dbe23e266abc
ms:mtpsurl: https://msdn.microsoft.com/library/Ff193483(v=office.15)
ms:contentKeyID: 48544664
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: 75dd4059aa9d06e2e6552b0ab7945373add55c76
ms.sourcegitcommit: c557bbcccf37a6011f89aae1ddd399dfe549d087
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 10/31/2018
ms.locfileid: "25872360"
---
# <a name="recordsetnextrecordset-method-dao"></a>Recordset.NextRecordset Method (DAO)


**S’applique à**: Access 2013, Office 2013

## <a name="syntax"></a>Syntaxe

*expression* . NextRecordset

*expression* Variable qui représente un objet **Recordset** .

### <a name="return-value"></a>Valeur renvoyée

Boolean

## <a name="remarks"></a>Remarques

Dans un espace de travail ODBCDirect, vous pouvez ouvrir un **[Recordset](recordset-object-dao.md)** contenant plusieurs requêtes sélection dans l’argument source de la **méthode OpenRecordset**, ou la propriété **[SQL](querydef-sql-property-dao.md)** d’une requête sélection objet **[QueryDef](querydef-object-dao.md)** , comme dans l’exemple suivant.

```sql
    SELECT LastName, FirstName FROM Authors 
    WHERE LastName = 'Smith'; 
    SELECT Title, ISBN FROM Titles 
    WHERE Pub_ID = 9999 
```

L'objet **Recordset** renvoyé s'ouvre en affichant les résultats de la première requête. Pour obtenir les jeux d'enregistrements résultant des requêtes suivantes, utilisez la méthode **NextRecordset**.

Si d'autres enregistrements sont disponibles (c'est-à-dire, si l'appel **OpenRecordset** ou la propriété **SQL** contenait une autre requête Sélection), les enregistrements renvoyés par la requête suivante sont chargés dans l'objet **Recordset**, et **NextRecordset** renvoie la valeur **True**, indiquant que les enregistrements sont disponibles. Si aucun autre enregistrement n'est disponible (c'est-à-dire, si les résultats de la dernière requête Sélection ont été chargés dans l'objet **Recordset**), **NextRecordset** renvoie la valeur **False**, et l'objet **Recordset** est vide.

Vous pouvez également utiliser la méthode **[Cancel](connection-cancel-method-dao.md)** pour vider un objet **Recordset** de son contenu. Toutefois, **Cancel** vide également les enregistrements supplémentaires qui n'ont pas encore été chargés.

## <a name="example"></a>Exemple

L'exemple ci-dessous utilise la méthode **NextRecordset** pour afficher les données à partir d'une requête SELECT composée. La propriété **DefaultCursorDriver** doit être définie sur la valeur **dbUseODBCCursor** en cas d'exécution de ce type de requête. La méthode **NextRecordset** renvoie la valeur **True** même si une partie ou l'ensemble des instructions SELECT renvoient des enregistrements nuls. Elle ne renvoie la valeur **False** qu'une fois toutes les clauses SQL vérifiées.

```vb
    Sub NextRecordsetX() 
     
     Dim wrkODBC As Workspace 
     Dim conPubs As Connection 
     Dim rstTemp As Recordset 
     Dim intCount As Integer 
     Dim booNext As Boolean 
     
     ' Create ODBCDirect Workspace object and open Connection 
     ' object. The DefaultCursorDriver setting is required 
     ' when using compound SQL statements. 
     Set wrkODBC = CreateWorkspace("", _ 
     "admin", "", dbUseODBC) 
     wrkODBC.DefaultCursorDriver = dbUseODBCCursor 
     
     ' Note: The DSN referenced below must be set to 
     ' use Microsoft Windows NT Authentication Mode to 
     ' authorize user access to the Microsoft SQL Server. 
     Set conPubs = wrkODBC.OpenConnection("Publishers", , , _ 
     "ODBC;DATABASE=pubs;DSN=Publishers") 
     
     ' Construct compound SELECT statement. 
     Set rstTemp = conPubs.OpenRecordset("SELECT * " & _ 
     "FROM authors; " & _ 
     "SELECT * FROM stores; " & _ 
     "SELECT * FROM jobs") 
     
     ' Try printing results from each of the three SELECT 
     ' statements. 
     booNext = True 
     intCount = 1 
     With rstTemp 
     Do While booNext 
     Debug.Print "Contents of recordset #" & intCount 
     Do While Not .EOF 
     Debug.Print , .Fields(0), .Fields(1) 
     .MoveNext 
     Loop 
     booNext = .NextRecordset 
     Debug.Print " rstTemp.NextRecordset = " & _ 
     booNext 
     intCount = intCount + 1 
     Loop 
     End With 
     
     rstTemp.Close 
     conPubs.Close 
     wrkODBC.Close 
     
    End Sub 
```

<br/>

Une autre façon d'accomplir la même tâche serait de créer une instruction préparée contenant l'instruction SQL composée. La propriété **CacheSize** de l'objet **QueryDef** doit avoir la valeur 1, et l'objet **Recordset** doit être de type avant uniquement et en lecture seule.

```vb 
Sub NextRecordsetX2() 
 
 Dim wrkODBC As Workspace 
 Dim conPubs As Connection 
 Dim qdfTemp As QueryDef 
 Dim rstTemp As Recordset 
 Dim intCount As Integer 
 Dim booNext As Boolean 
 
 ' Create ODBCDirect Workspace object and open Connection 
 ' object. The DefaultCursorDriver setting is required 
 ' when using compound SQL statements. 
 Set wrkODBC = CreateWorkspace("", _ 
 "admin", "", dbUseODBC) 
 wrkODBC.DefaultCursorDriver = dbUseODBCCursor 
 
 ' Note: The DSN referenced below must be set to 
 ' use Microsoft Windows NT Authentication Mode to 
 ' authorize user access to the Microsoft SQL Server. 
 Set conPubs = wrkODBC.OpenConnection("Publishers", , , _ 
 "ODBC;DATABASE=pubs;DSN=Publishers") 
 
 ' Create a temporary stored procedure with a compound 
 ' SELECT statement. 
 Set qdfTemp = conPubs.CreateQueryDef("", _ 
 "SELECT * FROM authors; " & _ 
 "SELECT * FROM stores; " & _ 
 "SELECT * FROM jobs") 
 ' Set CacheSize and open Recordset object with arguments 
 ' that will allow access to multiple recordsets. 
 qdfTemp.CacheSize = 1 
 Set rstTemp = qdfTemp.OpenRecordset(dbOpenForwardOnly, _ 
 dbReadOnly) 
 
 ' Try printing results from each of the three SELECT 
 ' statements. 
 booNext = True 
 intCount = 1 
 With rstTemp 
 Do While booNext 
 Debug.Print "Contents of recordset #" & intCount 
 Do While Not .EOF 
 Debug.Print , .Fields(0), .Fields(1) 
 .MoveNext 
 Loop 
 booNext = .NextRecordset 
 Debug.Print " rstTemp.NextRecordset = " & _ 
 booNext 
 intCount = intCount + 1 
 Loop 
 End With 
 
 rstTemp.Close 
 qdfTemp.Close 
 conPubs.Close 
 wrkODBC.Close 
 
End Sub 
 
```

