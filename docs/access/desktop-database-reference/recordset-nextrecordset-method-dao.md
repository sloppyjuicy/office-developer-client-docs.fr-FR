---
title: Méthode Recordset.NextRecordset (DAO)
TOCTitle: NextRecordset Method
ms:assetid: 4a3a6176-0aa0-efb6-b175-dbe23e266abc
ms:mtpsurl: https://msdn.microsoft.com/library/Ff193483(v=office.15)
ms:contentKeyID: 48544664
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: e4a6cf889e7676895534b053e8aacd4bb0eada89
ms.sourcegitcommit: d7248f803002b31cf7fc561b03530199a9b0a8fd
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 11/02/2018
ms.locfileid: "25919352"
---
# <a name="recordsetnextrecordset-method-dao"></a><span data-ttu-id="c0c89-102">Méthode Recordset.NextRecordset (DAO)</span><span class="sxs-lookup"><span data-stu-id="c0c89-102">Recordset.NextRecordset method (DAO)</span></span>


<span data-ttu-id="c0c89-103">**S’applique à**: Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="c0c89-103">**Applies to**: Access 2013, Office 2013</span></span>

## <a name="syntax"></a><span data-ttu-id="c0c89-104">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="c0c89-104">Syntax</span></span>

<span data-ttu-id="c0c89-105">*expression* . NextRecordset</span><span class="sxs-lookup"><span data-stu-id="c0c89-105">*expression* .NextRecordset</span></span>

<span data-ttu-id="c0c89-106">*expression* Variable qui représente un objet **Recordset** .</span><span class="sxs-lookup"><span data-stu-id="c0c89-106">*expression* A variable that represents a **Recordset** object.</span></span>

### <a name="return-value"></a><span data-ttu-id="c0c89-107">Valeur renvoyée</span><span class="sxs-lookup"><span data-stu-id="c0c89-107">Return value</span></span>

<span data-ttu-id="c0c89-108">Boolean</span><span class="sxs-lookup"><span data-stu-id="c0c89-108">Boolean</span></span>

## <a name="remarks"></a><span data-ttu-id="c0c89-109">Remarques</span><span class="sxs-lookup"><span data-stu-id="c0c89-109">Remarks</span></span>

<span data-ttu-id="c0c89-110">Dans un espace de travail ODBCDirect, vous pouvez ouvrir un **[Recordset](recordset-object-dao.md)** contenant plusieurs requêtes sélection dans l’argument source de la **méthode OpenRecordset**, ou la propriété **[SQL](querydef-sql-property-dao.md)** d’une requête sélection objet **[QueryDef](querydef-object-dao.md)** , comme dans l’exemple suivant.</span><span class="sxs-lookup"><span data-stu-id="c0c89-110">In an ODBCDirect workspace, you can open a **[Recordset](recordset-object-dao.md)** containing more than one select query in the source argument of **OpenRecordset**, or the **[SQL](querydef-sql-property-dao.md)** property of a select query **[QueryDef](querydef-object-dao.md)** object, as in the following example.</span></span>

```sql
    SELECT LastName, FirstName FROM Authors 
    WHERE LastName = 'Smith'; 
    SELECT Title, ISBN FROM Titles 
    WHERE Pub_ID = 9999 
```

<span data-ttu-id="c0c89-p101">L'objet **Recordset** renvoyé s'ouvre en affichant les résultats de la première requête. Pour obtenir les jeux d'enregistrements résultant des requêtes suivantes, utilisez la méthode **NextRecordset**.</span><span class="sxs-lookup"><span data-stu-id="c0c89-p101">The returned **Recordset** will open with the results of the first query. To obtain the result sets of records from subsequent queries, use the **NextRecordset** method.</span></span>

<span data-ttu-id="c0c89-p102">Si d'autres enregistrements sont disponibles (c'est-à-dire, si l'appel **OpenRecordset** ou la propriété **SQL** contenait une autre requête Sélection), les enregistrements renvoyés par la requête suivante sont chargés dans l'objet **Recordset**, et **NextRecordset** renvoie la valeur **True**, indiquant que les enregistrements sont disponibles. Si aucun autre enregistrement n'est disponible (c'est-à-dire, si les résultats de la dernière requête Sélection ont été chargés dans l'objet **Recordset**), **NextRecordset** renvoie la valeur **False**, et l'objet **Recordset** est vide.</span><span class="sxs-lookup"><span data-stu-id="c0c89-p102">If more records are available (that is, there was another select query in the **OpenRecordset** call or in the **SQL** property), the records returned from the next query will be loaded into the **Recordset**, and **NextRecordset** will return **True**, indicating that the records are available. When no more records are available (that is, results of the last select query have been loaded into the **Recordset**), then **NextRecordset** will return **False**, and the **Recordset** will be empty.</span></span>

<span data-ttu-id="c0c89-p103">Vous pouvez également utiliser la méthode **[Cancel](connection-cancel-method-dao.md)** pour vider un objet **Recordset** de son contenu. Toutefois, **Cancel** vide également les enregistrements supplémentaires qui n'ont pas encore été chargés.</span><span class="sxs-lookup"><span data-stu-id="c0c89-p103">You can also use the **[Cancel](connection-cancel-method-dao.md)** method to flush the contents of a **Recordset**. However, **Cancel** also flushes any additional records not yet loaded.</span></span>

## <a name="example"></a><span data-ttu-id="c0c89-117">Exemple</span><span class="sxs-lookup"><span data-stu-id="c0c89-117">Example</span></span>

<span data-ttu-id="c0c89-p104">L'exemple ci-dessous utilise la méthode **NextRecordset** pour afficher les données à partir d'une requête SELECT composée. La propriété **DefaultCursorDriver** doit être définie sur la valeur **dbUseODBCCursor** en cas d'exécution de ce type de requête. La méthode **NextRecordset** renvoie la valeur **True** même si une partie ou l'ensemble des instructions SELECT renvoient des enregistrements nuls. Elle ne renvoie la valeur **False** qu'une fois toutes les clauses SQL vérifiées.</span><span class="sxs-lookup"><span data-stu-id="c0c89-p104">This example uses the **NextRecordset** method to view the data from a compound SELECT query. The **DefaultCursorDriver** property must be set to **dbUseODBCCursor** when executing such queries. The **NextRecordset** method will return **True** even if some or all of the SELECT statements return zero records; it will return **False** only after all the individual SQL clauses have been checked.</span></span>

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

<span data-ttu-id="c0c89-p105">Une autre façon d'accomplir la même tâche serait de créer une instruction préparée contenant l'instruction SQL composée. La propriété **CacheSize** de l'objet **QueryDef** doit avoir la valeur 1, et l'objet **Recordset** doit être de type avant uniquement et en lecture seule.</span><span class="sxs-lookup"><span data-stu-id="c0c89-p105">Another way to accomplish the same task would be to create a prepared statement containing the compound SQL statement. The **CacheSize** property of the **QueryDef** object must be set to 1, and the **Recordset** object must be forward-only and read-only.</span></span>

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

