---
title: QueryDef.Prepare, propriété (DAO)
TOCTitle: Prepare Property
ms:assetid: d5a285c4-bd00-028b-b785-f1890db29bab
ms:mtpsurl: https://msdn.microsoft.com/library/Ff835035(v=office.15)
ms:contentKeyID: 48547968
ms.date: 09/18/2015
mtps_version: v=office.15
f1_keywords:
- dao360.chm1101187
f1_categories:
- Office.Version=v15
localization_priority: Normal
ms.openlocfilehash: ac05510a218d1cf4cf925acc2ca8908b7bcbcd03
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32303268"
---
# <a name="querydefprepare-property-dao"></a><span data-ttu-id="8cc01-102">QueryDef.Prepare, propriété (DAO)</span><span class="sxs-lookup"><span data-stu-id="8cc01-102">QueryDef.Prepare property (DAO)</span></span>

<span data-ttu-id="8cc01-103">**S’applique à** : Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="8cc01-103">**Applies to**: Access 2013, Office 2013</span></span>

## <a name="syntax"></a><span data-ttu-id="8cc01-104">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="8cc01-104">Syntax</span></span>

<span data-ttu-id="8cc01-105">*.* Préparer</span><span class="sxs-lookup"><span data-stu-id="8cc01-105">*expression* .Prepare</span></span>

<span data-ttu-id="8cc01-106">*expression* Variable représentant un objet **QueryDef**.</span><span class="sxs-lookup"><span data-stu-id="8cc01-106">*expression* A variable that represents a **QueryDef** object.</span></span>

## <a name="remarks"></a><span data-ttu-id="8cc01-107">Remarques</span><span class="sxs-lookup"><span data-stu-id="8cc01-107">Remarks</span></span>

<span data-ttu-id="8cc01-p101">La propriété **Prepare** permet soit de créer une procédure stockée temporaire à partir de la requête et de l'exécuter ensuite, soit d'exécuter la requête directement. Par défaut, la propriété **Prepare** est définie sur **dbQPrepare**. Toutefois, vous pouvez la définir sur **dbQUnprepare** pour empêcher toute préparation de la requête. Dans ce cas, elle est exécutée à l'aide de l'API **SQLExecDirect**.</span><span class="sxs-lookup"><span data-stu-id="8cc01-p101">You can use the **Prepare** property to either have the server create a temporary stored procedure from your query and then execute it, or just have the query executed directly. By default the **Prepare** property is set to **dbQPrepare**. However, you can set this property to **dbQUnprepare** to prohibit preparing of the query. In this case, the query is executed using the **SQLExecDirect** API.</span></span>

<span data-ttu-id="8cc01-p102">La création d'une procédure stockée peut ralentir l'opération initiale, mais augmente les performances de toutes les références ultérieures à la requête. Toutefois, certaines requêtes ne peuvent pas être exécutées sous la forme d'une procédure stockée. Dans ce cas, vous devez définir la propriété **Prepare** sur **dbQUnprepare**.</span><span class="sxs-lookup"><span data-stu-id="8cc01-p102">Creating a stored procedure can slow down the initial operation, but increases performance of all subsequent references to the query. However, some queries cannot be executed in the form of stored procedures. In these cases, you must set the **Prepare** property to **dbQUnprepare**.</span></span>

<span data-ttu-id="8cc01-115">Si **prepare** est définie sur **dbQPrepare,** cela peut être effectué lorsque la requête est exécutée en attérialant l’argument options de la méthode **[Execute](querydef-execute-method-dao.md)** sur **dbExecDirect**.</span><span class="sxs-lookup"><span data-stu-id="8cc01-115">If **Prepare** is set to **dbQPrepare**, this can be overridden when the query is executed by setting the **[Execute](querydef-execute-method-dao.md)** method's options argument to **dbExecDirect**.</span></span>

> [!NOTE]
> <span data-ttu-id="8cc01-p103">[!REMARQUE] L'API **SQLPrepare** ODBC est invoqué dès que la propriété DAO **[SQL](querydef-sql-property-dao.md)** est définie. Par conséquent, pour améliorer les performances à l'aide de l'option **dbQUnprepare**, vous devez définir la propriété **Prepare** avant de définir la propriété **SQL**.</span><span class="sxs-lookup"><span data-stu-id="8cc01-p103">The ODBC **SQLPrepare** API is called as soon as the DAO **[SQL](querydef-sql-property-dao.md)** property is set. Therefore, if you want to improve performance using the **dbQUnprepare** option, you must set the **Prepare** property before setting the **SQL** property.</span></span>

## <a name="example"></a><span data-ttu-id="8cc01-118">Exemple</span><span class="sxs-lookup"><span data-stu-id="8cc01-118">Example</span></span>

<span data-ttu-id="8cc01-119">Cet exemple utilise la propriété **Prepare** pour spécifier qu'une requête doit être exécutée directement plutôt que de passer par la création préalable d'une procédure stockée sur le serveur.</span><span class="sxs-lookup"><span data-stu-id="8cc01-119">This example uses the **Prepare** property to specify that a query should be executed directly rather than first creating a temporary stored procedure on the server.</span></span>

```vb 
Sub PrepareX() 
 
 Dim wrkODBC As Workspace 
 Dim conPubs As Connection 
 Dim qdfTemp As QueryDef 
 Dim rstTemp As Recordset 
 
 ' Create ODBCDirect Workspace object and open Connection 
 ' object. 
 Set wrkODBC = CreateWorkspace("", _ 
 "admin", "", dbUseODBC) 
 
 ' Note: The DSN referenced below must be configured to 
 ' use Microsoft Windows NT Authentication Mode to 
 ' authorize user access to the Microsoft SQL Server. 
 Set conPubs = wrkODBC.OpenConnection("Publishers", , , _ 
 "ODBC;DATABASE=pubs;DSN=Publishers") 
 
 Set qdfTemp = conPubs.CreateQueryDef("") 
 
 With qdfTemp 
 ' Because you will only run this query once, specify 
 ' the ODBC SQLExecDirect API function. If you do 
 ' not set this property before you set the SQL 
 ' property, the ODBC SQLPrepare API function will 
 ' be called anyway which will nullify any 
 ' performance gain. 
 .Prepare = dbQUnprepare 
 .SQL = "UPDATE roysched " & _ 
 "SET royalty = royalty * 2 " & _ 
 "WHERE title_id LIKE 'BU____' OR " & _ 
 "title_id LIKE 'PC____'" 
 .Execute 
 End With 
 
 Debug.Print "Query results:" 
 
 ' Open recordset containing modified records. 
 Set rstTemp = conPubs.OpenRecordset( _ 
 "SELECT * FROM roysched " & _ 
 "WHERE title_id LIKE 'BU____' OR " & _ 
 "title_id LIKE 'PC____'") 
 
 ' Enumerate recordset. 
 With rstTemp 
 Do While Not .EOF 
 Debug.Print , !title_id, !lorange, _ 
 !hirange, !royalty 
 .MoveNext 
 Loop 
 .Close 
 End With 
 
 conPubs.Close 
 wrkODBC.Close 
 
```

