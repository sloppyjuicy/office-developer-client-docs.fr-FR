---
title: Méthode Recordset2.NextRecordset (DAO)
TOCTitle: NextRecordset Method
ms:assetid: 33288131-d4f3-0159-1736-f401346087f3
ms:mtpsurl: https://msdn.microsoft.com/library/Ff192318(v=office.15)
ms:contentKeyID: 48544096
ms.date: 09/18/2015
mtps_version: v=office.15
f1_keywords:
- dao360.chm1053575
f1_categories:
- Office.Version=v15
localization_priority: Normal
ms.openlocfilehash: 54d0e49dfbe9dc3fb87eb10af9eefe3aa2f83709
ms.sourcegitcommit: d6695c94415fa47952ee7961a69660abc0904434
ms.translationtype: Auto
ms.contentlocale: fr-FR
ms.lasthandoff: 01/17/2019
ms.locfileid: "28715927"
---
# <a name="recordset2nextrecordset-method-dao"></a>Méthode Recordset2.NextRecordset (DAO)


**S’applique à**: Access 2013, Office 2013

## <a name="syntax"></a>Syntaxe

*expression* . NextRecordset

*expression* Variable qui représente un objet **Recordset2** .

## <a name="return-value"></a>Valeur renvoyée

Booléen

## <a name="remarks"></a>Remarques

Dans un espace de travail ODBCDirect, vous pouvez ouvrir un **Recordset** contenant plusieurs requêtes sélection dans l’argument source de la **méthode OpenRecordset**, ou la propriété **[SQL](querydef-sql-property-dao.md)** d’une requête sélection objet **[QueryDef](querydef-object-dao.md)** , comme dans l’exemple suivant.

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
     Dim rstTemp As Recordset2 
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
 Dim rstTemp As Recordset2 
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

