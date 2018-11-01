---
title: Database.QueryTimeout Property (DAO)
TOCTitle: QueryTimeout Property
ms:assetid: c83ca852-715a-c853-429b-80a15c3fc39b
ms:mtpsurl: https://msdn.microsoft.com/library/Ff823170(v=office.15)
ms:contentKeyID: 48547648
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: e924dfb89cb67ffa4bc8ec29d0c24a7c61fcb5b5
ms.sourcegitcommit: c557bbcccf37a6011f89aae1ddd399dfe549d087
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 10/31/2018
ms.locfileid: "25887963"
---
# <a name="databasequerytimeout-property-dao"></a><span data-ttu-id="3cc09-102">Database.QueryTimeout Property (DAO)</span><span class="sxs-lookup"><span data-stu-id="3cc09-102">Database.QueryTimeout Property (DAO)</span></span>


<span data-ttu-id="3cc09-103">**S’applique à**: Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="3cc09-103">**Applies to**: Access 2013, Office 2013</span></span>


<span data-ttu-id="3cc09-104">Définit ou retourne une valeur qui spécifie le nombre de secondes d'attente avant qu'une erreur de délai d'attente soit générée lors de l'exécution d'une requête sur une source de données ODBC.</span><span class="sxs-lookup"><span data-stu-id="3cc09-104">Sets or returns a value that specifies the number of seconds to wait before a timeout error occurs when a query is executed on an ODBC data source.</span></span>

## <a name="syntax"></a><span data-ttu-id="3cc09-105">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="3cc09-105">Syntax</span></span>

<span data-ttu-id="3cc09-106">*expression* . QueryTimeout</span><span class="sxs-lookup"><span data-stu-id="3cc09-106">*expression* .QueryTimeout</span></span>

<span data-ttu-id="3cc09-107">*expression* Variable qui représente un objet de **base de données** .</span><span class="sxs-lookup"><span data-stu-id="3cc09-107">*expression* A variable that represents a **Database** object.</span></span>

## <a name="remarks"></a><span data-ttu-id="3cc09-108">Remarques</span><span class="sxs-lookup"><span data-stu-id="3cc09-108">Remarks</span></span>

<span data-ttu-id="3cc09-109">La valeur par défaut est 60.</span><span class="sxs-lookup"><span data-stu-id="3cc09-109">The default value is 60.</span></span>

<span data-ttu-id="3cc09-p101">Lorsque vous utilisez une base de données ODBC, telle que Microsoft SQL Server, le trafic réseau ou une utilisation intensive du serveur ODBC peut entraîner des délais. Au lieu d'attendre indéfiniment, vous pouvez définir le délai d'attente.</span><span class="sxs-lookup"><span data-stu-id="3cc09-p101">When you're using an ODBC database, such as Microsoft SQL Server, there may be delays due to network traffic or heavy use of the ODBC server. Rather than waiting indefinitely, you can specify how long to wait.</span></span>

<span data-ttu-id="3cc09-p102">Si la propriété **QueryTimeout** est utilisée avec un objet **[Connection](connection-object-dao.md)** ou **[Database](database-object-dao.md)**, elle spécifie une valeur globale pour toutes les requêtes associées à la base de données. Vous pouvez remplacer cette valeur pour une requête donnée en paramétrant la propriété **ODBCTimeout** de l'objet **[QueryDef](querydef-object-dao.md)** spécifique.</span><span class="sxs-lookup"><span data-stu-id="3cc09-p102">When you use **QueryTimeout** with a **[Connection](connection-object-dao.md)** or **[Database](database-object-dao.md)** object, it specifies a global value for all queries associated with the database. You can override this value for a specific query by setting the **ODBCTimeout** property of the particular **[QueryDef](querydef-object-dao.md)** object.</span></span>

## <a name="example"></a><span data-ttu-id="3cc09-114">Exemple</span><span class="sxs-lookup"><span data-stu-id="3cc09-114">Example</span></span>

<span data-ttu-id="3cc09-115">L'exemple ci-dessous fait appel aux propriétés **ODBCTimeout** et **QueryTimeout** pour indiquer comment le paramètre **QueryTimeout** d'un objet **Database** définit le paramètre **ODBCTimeout** par défaut des objets **QueryDef** créés à partir de l'objet **Database**.</span><span class="sxs-lookup"><span data-stu-id="3cc09-115">This example uses the **ODBCTimeout** and **QueryTimeout** properties to show how the **QueryTimeout** setting on a **Database** object sets the default **ODBCTimeout** setting on any **QueryDef** objects created from the **Database** object.</span></span>

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

