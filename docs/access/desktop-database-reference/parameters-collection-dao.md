---
title: Parameters, collection (DAO)
TOCTitle: Parameters Collection
ms:assetid: 52fc1ce4-7b3e-152d-7b6a-9c32a6470147
ms:mtpsurl: https://msdn.microsoft.com/library/Ff193967(v=office.15)
ms:contentKeyID: 48544862
ms.date: 09/18/2015
mtps_version: v=office.15
localization_priority: Priority
ms.openlocfilehash: 09f60cb8dde407aacbb19e6b2124151dbbf9b3c5
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: HT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32287894"
---
# <a name="parameters-collection-dao"></a><span data-ttu-id="821ef-102">Parameters, collection (DAO)</span><span class="sxs-lookup"><span data-stu-id="821ef-102">Parameters Collection (DAO)</span></span>

<span data-ttu-id="821ef-103">**S’applique à** : Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="821ef-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="821ef-104">Une collection **Parameters** contient tous les objets **Parameters** d’un objet **QueryDef**.</span><span class="sxs-lookup"><span data-stu-id="821ef-104">A **Parameters** collection contains all the **Parameter** objects of a **QueryDef** object.</span></span>

## <a name="remarks"></a><span data-ttu-id="821ef-105">Remarques</span><span class="sxs-lookup"><span data-stu-id="821ef-105">Remarks</span></span>

<span data-ttu-id="821ef-106">La collection **Parameters** fournit des informations relatives aux paramètres existants uniquement.</span><span class="sxs-lookup"><span data-stu-id="821ef-106">The **Parameters** collection provides information only about existing parameters.</span></span> <span data-ttu-id="821ef-107">Vous ne pouvez pas ajouter ou supprimer des objets de la collection **Parameters**.</span><span class="sxs-lookup"><span data-stu-id="821ef-107">You can't append objects to or delete objects from the **Parameters** collection.</span></span>

## <a name="example"></a><span data-ttu-id="821ef-108">Exemple</span><span class="sxs-lookup"><span data-stu-id="821ef-108">Example</span></span>

<span data-ttu-id="821ef-p102">Cet exemple démontre les objets **Parameter** et la collection **Parameters** en créant un objet **QueryDef** temporaire et en extrayant les données sur la base des modifications apportées aux objets **Parameters** de l'objet **QueryDef**. La procédure ParametersChange est requise pour exécuter cette opération.</span><span class="sxs-lookup"><span data-stu-id="821ef-p102">This example demonstrates **Parameter** objects and the **Parameters** collection by creating a temporary **QueryDef** and retrieving data based on changes made to the **QueryDef** object's **Parameters**. The ParametersChange procedure is required for this procedure to run.</span></span>

```vb
    Sub ParameterX() 
     
       Dim dbsNorthwind As Database 
       Dim qdfReport As QueryDef 
       Dim prmBegin As Parameter 
       Dim prmEnd As Parameter 
     
       Set dbsNorthwind = OpenDatabase("Northwind.mdb") 
     
       ' Create temporary QueryDef object with two  
       ' parameters. 
       Set qdfReport = dbsNorthwind.CreateQueryDef("", _ 
          "PARAMETERS dteBegin DateTime, dteEnd DateTime; " & _ 
          "SELECT EmployeeID, COUNT(OrderID) AS NumOrders " & _ 
          "FROM Orders WHERE ShippedDate BETWEEN " & _ 
          "[dteBegin] AND [dteEnd] GROUP BY EmployeeID " & _ 
          "ORDER BY EmployeeID") 
       Set prmBegin = qdfReport.Parameters!dteBegin 
       Set prmEnd = qdfReport.Parameters!dteEnd 
     
       ' Print report using specified parameter values. 
       ParametersChange qdfReport, prmBegin, #1/1/95#, _ 
          prmEnd, #6/30/95# 
       ParametersChange qdfReport, prmBegin, #7/1/95#, _ 
          prmEnd, #12/31/95# 
     
       dbsNorthwind.Close 
     
    End Sub 
     
    Sub ParametersChange(qdfTemp As QueryDef, _ 
       prmFirst As Parameter, dteFirst As Date, _ 
       prmLast As Parameter, dteLast As Date) 
       ' Report function for ParameterX. 
     
       Dim rstTemp As Recordset 
       Dim fldLoop As Field 
     
       ' Set parameter values and open recordset from  
       ' temporary QueryDef object. 
       prmFirst = dteFirst 
       prmLast = dteLast 
       Set rstTemp = _  
          qdfTemp.OpenRecordset(dbOpenForwardOnly) 
       Debug.Print "Period " & dteFirst & " to " & dteLast 
     
       ' Enumerate recordset. 
       Do While Not rstTemp.EOF 
     
          ' Enumerate Fields collection of recordset. 
          For Each fldLoop In rstTemp.Fields 
             Debug.Print " - " & fldLoop.Name & " = " & fldLoop; 
          Next fldLoop 
     
          Debug.Print 
          rstTemp.MoveNext 
       Loop 
     
       rstTemp.Close 
     
    End Sub 
```

<br/>

L’exemple suivant montre comment créer une requête avec paramètres. Une requête nommée **myQuery** est créée avec deux paramètres nommés Param1 et Param2. <span data-ttu-id="821ef-113">Pour ce faire, la propriété SQL de la requête est définie sur une instruction SQL qui définit les paramètres.</span><span class="sxs-lookup"><span data-stu-id="821ef-113">To do this, the SQL property of the query is set to a Structured Query Language (SQL) statement that defines the parameters.</span></span>

<span data-ttu-id="821ef-114">**Exemple de code fourni par** [Microsoft Access 2010 Programmer’s Reference](https://www.amazon.com/Microsoft-Access-2010-Programmers-Reference/dp/8126528125).</span><span class="sxs-lookup"><span data-stu-id="821ef-114">**Sample code provided by** the [Microsoft Access 2010 Programmer’s Reference](https://www.amazon.com/Microsoft-Access-2010-Programmers-Reference/dp/8126528125).</span></span>

```vb
    Sub CreateQueryWithParameters()
    
        Dim dbs As DAO.Database
        Dim qdf As DAO.QueryDef
        Dim strSQL As String
    
        Set dbs = CurrentDb
        Set qdf = dbs.CreateQueryDef("myQuery")
        Application.RefreshDatabaseWindow
    
        strSQL = "PARAMETERS Param1 TEXT, Param2 INT; "
        strSQL = strSQL & "SELECT * FROM [Table1] "
        strSQL = strSQL & "WHERE [Field1] = [Param1] AND [Field2] = [Param2];"
        qdf.SQL = strSQL
    
        qdf.Close
        Set qdf = Nothing
        Set dbs = Nothing
    
    End Sub
```

<br/>

<span data-ttu-id="821ef-115">L’exemple suivant montre comment exécuter une requête avec paramètres.</span><span class="sxs-lookup"><span data-stu-id="821ef-115">The following example shows how to execute a parameter query.</span></span> <span data-ttu-id="821ef-116">La collection Parameters permet de définir le paramètre Organization de la requête myActionQuery avant l’exécution de celle-ci.</span><span class="sxs-lookup"><span data-stu-id="821ef-116">The Parameters collection is used to set the Organization parameter of the myActionQuery query before the query is executed.</span></span>

```vb
    Public Sub ExecParameterQuery()
    
        Dim dbs As DAO.Database
        Dim qdf As DAO.QueryDef
    
        Set dbs = CurrentDb
        Set qdf = dbs.QueryDefs("myActionQuery")
    
        'Set the value of the QueryDef's parameter
        qdf.Parameters("Organization").Value = "Microsoft"
    
        'Execute the query
        qdf.Execute dbFailOnError
    
        'Clean up
        qdf.Close
        Set qdf = Nothing
        Set dbs = Nothing
    
    End Sub
```

<br/>

<span data-ttu-id="821ef-117">L’exemple suivant montre comment ouvrir un objet Recordset basé sur une requête avec paramètres.</span><span class="sxs-lookup"><span data-stu-id="821ef-117">The following example shows how to open a Recordset that is based on a parameter query.</span></span>

```vb
    Dim dbs As DAO.Database
    Dim qdf As DAO.QueryDef
    Dim rst As DAO.Recordset
    
    Set dbs = CurrentDb
    
    'Get the parameter query
    Set qfd = dbs.QueryDefs("qryMyParameterQuery")
    
    'Supply the parameter value
    qdf.Parameters("EnterStartDate") = Date
    qdf.Parameters("EnterEndDate") = Date + 7
    
    'Open a Recordset based on the parameter query
    Set rst = qdf.OpenRecordset()
```
